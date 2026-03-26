# How does the Kafka event pipeline work at Compel and how is lag handled?

## Architecture overview
- Source: AXAPTA (ERP) → Kafka topics → microservices → PostgreSQL
- Event types: CREATE, UPDATE, DELETE, SNAPSHOT
- Each consumer filters events by type and processes them accordingly
- Consumers: 2-3 per topic typically
- Framework: **Faust (Faust-streaming)** — Python Kafka framework

## Delivery semantics
- Effectively **at-least-once with skip-on-invalid**
- Initially built with retries for full delivery guarantee
- In practice: the producer (AXAPTA side) sent invalid/garbage messages
- Decision: **skip invalid messages** instead of retrying forever
- Kirill advocated that the **producer should guarantee valid data** so that every consumer doesn't have to independently validate — but the AXAPTA team didn't always follow this
- No transactional exactly-once semantics configured at Kafka level

## Partition key
- **AXAPTA ID** of the component — unique identifier from the ERP system
- Used for both partitioning and idempotent updates/deletes
- This guarantees ordering of events for the same component within a partition

## Consumer lag: when and why it happens
- Lag occurred **only during full snapshot re-imports** (16-19M events)
- Snapshot re-imports were rare — done 1-2 times per environment (Dev/Stage/Prod) when connecting a new service
- This was essentially a one-time operation, not a recurring issue
- During lag: nothing crashed, system continued to work, lag gradually decreased and stabilized
- Monitoring: Kafka UI on Dev/Stage, available across all environments

## Idempotency and deduplication
- No deduplication problem because the system was designed with **idempotency**
- Events were filtered by type in the consumer: CREATE, UPDATE, DELETE, SNAPSHOT
- Each event type had its own processing logic
- AXAPTA ID served as the idempotency key for updates and deletes

## Partitioning strategy
- Typically 1-3 partitions per topic
- When lag grew significantly during snapshot imports, the team **increased partition count**
- Since snapshot imports were rare, no need for aggressive partition optimization
- Partition scaling was reactive, not proactive — pragmatic given the low frequency of full imports

## Cross-team consulting: fixing snapshot abuse
- Another team was doing **frequent full snapshot re-imports** into Kafka — a legacy habit from CSV file-based imports
- Kirill's team discovered this when they connected to that team's topic and noticed constant snapshot loads
- Kirill was asked to join that team and help fix the problem
- Solution: educated the team to stop treating Kafka like a file dump — instead, AXAPTA should emit granular events (UPDATE, DELETE) for individual component changes
- This was a **cultural/process fix**, not just a technical one — changing the team's mental model from batch to event-driven

## Key insight for interviews
- The Kafka migration itself was the strategic solution to replace bulk CSV imports
- Full snapshots were a transitional tool for bootstrapping new services, not a steady-state pattern
- Real-time incremental updates (CREATE/UPDATE/DELETE events from AXAPTA) were the target architecture
- Producer quality matters: "garbage in, garbage out" — advocated for producer-side validation

## GAPS
- Consumer group configuration details — not specified
- Kafka retention policy and topic configuration — not specified
- Whether consumer offset management was automatic or manual (Faust default) — not specified
- Dead letter queue for invalid messages — not mentioned, unclear if skipped messages were logged
