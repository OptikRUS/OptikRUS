# How does the bulk import optimization work internally at Compel?

## Context
- Table: ~15-20M rows, 4 columns (search components)
- Data source: CSV file from AXAPTA/ERP
- Stack: SQLAlchemy + PostgreSQL
- Data size: ~200-300 MB (small despite row count)
- Import frequency: periodic full refresh
- Concurrent users: ~10 (very low load on this service)

## Algorithm (step by step)
1. BEGIN transaction (SQLAlchemy session)
2. DELETE all existing rows from the table
3. DROP indexes on the table
4. Bulk INSERT from CSV file (~15-20M rows)
5. REBUILD indexes (CREATE INDEX)
6. COMMIT transaction

## Why this works without downtime
- PostgreSQL MVCC: readers see the old snapshot until COMMIT
- During the entire 40-minute import, other services continue reading the **previous version** of data
- After COMMIT, new data atomically becomes the "current" version
- Old tuples become eligible for VACUUM cleanup

## Failure handling
- If anything fails mid-import (OOM, connection loss, etc.), the entire transaction rolls back
- No partial state — either all new data is committed, or nothing changes
- Old data remains intact and available to readers

## DROP INDEX CONCURRENTLY — why not used
- `DROP INDEX CONCURRENTLY` cannot run inside a transaction (PostgreSQL limitation)
- The team needed zero-downtime guarantee, which the transaction approach provided
- Decision was validated by an external database specialist who confirmed this was the optimal approach

## Lock behavior and real-world impact
- FACT: DROP INDEX takes ACCESS EXCLUSIVE lock on the table (PostgreSQL internals)
- FACT: The service had ~10 concurrent users — very low load
- FACT: The team did not observe any read blocking or queuing in practice
- The low concurrency meant that even if locks were briefly held, the impact was negligible and unnoticeable
- [INTERPRETATION] With higher concurrency, this approach would likely cause visible lock contention

## Evolution: migration to Kafka
- Later the team migrated from bulk CSV import to **Kafka-based incremental updates**
- Components were updated one-by-one via Kafka events instead of full table refresh
- This eliminated the need for the bulk import pattern entirely
- The bulk import was a pragmatic first solution; Kafka was the strategic long-term solution

## Bloat and table growth
- No bloat issues encountered in practice
- Table size is bounded by the domain: catalog of electronic components, grows slowly
- Team verified with business stakeholders that the dataset would not grow significantly
- 4 columns × 20M rows ≈ 200-300 MB — not enough to cause storage pressure

## WAL impact
- No replication lag or disk space issues observed
- Data volume is small in absolute terms (~200-300 MB of actual data)

## GAPS
- Exact transaction isolation level used (READ COMMITTED vs SERIALIZABLE?) — not specified
- Whether autovacuum was tuned after these large transactions — not discussed
- Whether the table was partitioned or a simple heap table — not specified
- Exact timing of lock acquisition vs. lock release within the transaction — not measured
