# How was the CSV import restructured to eliminate joins at Compel?

## Context: dual infrastructure
- Dev/Stage: hosted on Selectel, migrated to Kafka (incremental updates)
- Production: hosted on separate servers at a different provider (HRD?), still used CSV file import
- The same codebase had to support BOTH Kafka and CSV import paths

## Original architecture (two entities)
- Two CSV files imported into two separate database tables
- A JOIN between these tables was required for search functionality
- JOIN on 15-20M rows caused visible performance degradation

## Optimization: merge into one entity
- Kafka pipeline was already working with a new single-entity table structure
- CSV import needed to catch up with this new structure
- Solution: import data from **two CSV files into one table** directly
- Eliminated the JOIN entirely — same denormalization approach as the search optimization

## Memory optimization during merge
- Initial approach: held both CSV files in memory simultaneously → memory issues
- Iteration 1: held only one file in memory at a time
- Iteration 2: used mapping/dictionary approach to optimize memory usage
- Measured memory consumption at each step
- Final solution: efficient single-pass merge with controlled memory footprint

## Where compiled languages could help
- The CSV parsing and data transformation ("data grinding") is a CPU-bound operation
- This is a concrete place where Go/Rust could provide benefit if load increased
- However, at current scale Python performance was sufficient
- There are also other services that do heavy data serialization/transformation where Go/Rust could be applied

## Key engineering insight
- The real optimization came from **architectural change** (removing JOIN via denormalization), not from language-level optimization
- Language switch (Python → Go/Rust) would be a micro-optimization compared to the architectural win

## GAPS
- Exact memory consumption numbers (before/after optimization) — not specified
- Whether the mapping approach used generators/streaming or loaded into dict — not specified
- Import time impact of merging two files into one table — "slightly longer" but not quantified
