# How was the search query optimized from 3500ms to 95ms at Compel?

## The query
- Simple LIKE search with `startswith` pattern (e.g., `WHERE name LIKE 'query%'`)
- Case-insensitive: needed to match regardless of input case
- No full-text search, no autocomplete — basic prefix matching

## Root causes of 3500ms latency
1. **LOWER() on both sides**: PostgreSQL was calling `LOWER()` on both the column and the search term at query time — expensive on millions of rows
2. **JOINs**: Items were joined with manufacturers (producers) via foreign keys — unnecessary for search
3. **Sequential scan**: no effective index usage due to the LOWER() function call and JOINs

## Optimizations applied

### 1. Pre-normalized data (LOWER at write time)
- Data came from AXAPTA in mixed case
- Solution: during import, convert search fields to lowercase **before saving** to the database
- This eliminated the need for `LOWER()` at query time
- Index could now be used directly on the pre-lowered column

### 2. Denormalization — new SearchItem entity
- Original: Item entity + Manufacturer entity, joined by FK (foreign key)
- Problem: JOIN on millions of rows for every search query
- Solution: created a new **SearchItem** domain entity — a flattened version of Item with the search field embedded
- Removed the FK relationship and JOINs entirely
- This was a **domain-driven design decision**, not just a DB trick — the business needed a dedicated search concept

### 3. Index on the search column
- Added an index (B-tree or GIN — exact type not recalled) on the pre-lowered search column
- With LOWER() eliminated and JOINs removed, the index was now effective

## Result
- 3500ms → 95ms (x36 improvement)
- Verified via EXPLAIN ANALYZE

## Pagination
- No pagination on this service
- Large result sets were handled by a different mechanism (separate story)

## Key interview insight
- The optimization was **layered**: each change contributed, but the biggest win was architectural (removing JOINs via denormalization)
- Pre-computing LOWER() at write time is a classic read-optimization trade-off: slightly more work on write, massively less work on read
- Framing as a domain concept (SearchItem) rather than a "denormalized table" shows DDD thinking

## GAPS
- Exact index type (B-tree vs GIN) — not recalled
- Whether a functional index (e.g., `CREATE INDEX ON items (LOWER(name))`) was considered as an alternative to pre-lowering
- How large result sets were handled without pagination — separate story, not yet covered
- Whether EXPLAIN ANALYZE results were saved/documented
