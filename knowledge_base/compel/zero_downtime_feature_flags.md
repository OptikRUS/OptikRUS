# How was zero downtime achieved with dual pipeline and feature flags at Compel?

## Dual pipeline architecture
- Two data ingestion implementations behind a common abstraction:
  1. **KafkaStorage** — consumes events from Kafka via Faust-streaming framework
  2. **CSVFileStorage** — imports data from CSV files (legacy approach)
- Both classes implemented the same interface/abstract base class

## Feature flag mechanism
- Simple boolean flag at application startup: `USE_KAFKA = True/False`
- When `True` → Kafka consumer class injected via dependency injection
- When `False` → CSV file import class injected instead
- Dependency injection via FastAPI's `Depends` system

## Why two pipelines existed simultaneously
- Dev/Stage environments: hosted on Selectel, migrated to Kafka (`USE_KAFKA=True`)
- Production: hosted on different servers at another provider, initially stayed on CSV import (`USE_KAFKA=False`)
- The same codebase worked in both environments — no separate branches or deployments
- This enabled **gradual migration** without production risk

## Zero downtime guarantee
- Kafka path: incremental updates, no table locks, no bulk operations
- CSV path: single transaction (as described in bulk import case)
- Feature flag allowed instant rollback: flip `USE_KAFKA=False` if Kafka had issues
- No dual-write or dual-read complexity — clean switch between two implementations

## Key interview insight
- This is a textbook **Strategy pattern** with dependency injection
- Simple, pragmatic approach — no complex feature flag service (LaunchDarkly etc.)
- Enabled safe production migration with zero coordination overhead
- [INTERPRETATION] The "zero downtime" claim combines: MVCC for CSV path + incremental updates for Kafka path + instant rollback capability via flag
