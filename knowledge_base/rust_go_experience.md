# What is Kirill's experience with Rust/Go and compiled languages for backend optimization?

## Go experience
- The team at Compel considered learning Go for practical use
- Planned to write an **i18n service** in Go as a training project
- Rationale for choosing i18n: the service is simple enough that if the Go experiment failed, it could be quickly rewritten in any other language (even Rust)
- Kirill started learning Go independently
- Built a simple web server with a database for i18n functionality
- Learning paused after the initial prototype

## Current readiness
- Has foundational Go knowledge (web server + DB interaction)
- Confident in ability to quickly build Go services with AI assistance
- No production Go code deployed

## Rust experience
- GAPS: No hands-on Rust experience mentioned
- Rust was referenced only as a theoretical alternative ("could rewrite in Rust if needed")

## Where would compiled languages be applied in Compel's architecture?

### Identified CPU-bound bottlenecks
1. **CSV parsing and data transformation** — merging two CSV files (15-20M rows each) into one table, with mapping/dict lookups. This is a concrete CPU-bound operation where Go/Rust would help
2. **Data serialization services** — some services do heavy data "grinding" (serialization/deserialization). These could benefit from compiled languages at higher scale
3. **Pydantic validation on large payloads** — [INTERPRETATION] not explicitly mentioned but implied by the data pipeline volume

### Why Python was sufficient
- Primary bottlenecks were I/O-bound (PostgreSQL queries, Kafka consumption)
- The biggest wins came from **architectural changes** (denormalization, removing JOINs) not language-level optimization
- Current load (~100 RPS, ~10 users on import service) did not stress Python's CPU limits
- [INTERPRETATION] The correct answer for interviews: "I would profile first, identify CPU-bound hotspots, and only then consider compiled extensions — because in our case, architecture changes gave 36x improvement without changing language"
