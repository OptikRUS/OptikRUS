# How was the microservice template built and why did it speed up deployment 2x?

## Context
- When Kirill joined Compel, it was clear there would be many new microservices (15-20 total)
- Each new service required repetitive setup: project structure, configs, DB init, Kafka init, CI/CD, etc.
- Manual setup was error-prone: copy-paste mistakes, forgotten changes, inconsistencies

## Two approaches tried

### Company-wide template (abandoned)
- Initial attempt: create a universal template for all teams in the company
- Didn't work — different teams had different needs and conventions

### Team-specific template via GitLab (adopted)
- Created a template specific to Kirill's team
- Deployed via **GitLab** — press a button, project scaffolding is created
- Simpler and more tailored than the company-wide approach

### Alternative: Cookiecutter (used by other teams)
- Other teams in the company used **Cookiecutter** for scaffolding
- Cookiecutter advantage: interactive prompts — "Do you need a database? Kafka?" → generates only relevant modules
- This was convenient: select components, get a ready-made project with only what you need

## What the template included
- Project structure (FastAPI app skeleton)
- Database setup (if needed)
- Kafka consumer/producer setup (if needed)
- CI/CD pipeline configuration
- Common dependencies and configurations
- [INTERPRETATION] Likely also included: linting, testing setup, Docker/docker-compose, health checks

## Why 2x faster deployment
- Before: manually copy an existing service, rename everything, remove unnecessary parts, configure CI/CD → error-prone and time-consuming
- After: press a button → get a working project skeleton in minutes
- The "2x" is about **time to first deployment of a new service**, not runtime performance

## GitLab mechanism
- Used **GitLab's project initialization from a template repository**
- Press a button → new project created from the template repo with all scaffolding

## GAPS
- Whether the template was versioned and how updates propagated to existing services — not specified
- How many services were actually created using the template — not specified
- Whether the template included observability setup (logging, metrics, tracing) — not specified
