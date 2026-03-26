# How were BDD practices introduced at Compel and how did they reduce bugs by 70%?

## The problem
- Company had **incompetent system analysts** — they didn't understand industry practices
- Requirements were poorly specified, leading to bugs from misunderstood business rules
- Domain is extremely complex: electronic components, compliance, sanctions, access control
- Edge cases were frequently missed in requirements

## BDD as a solution for analyst training
- Kirill realized that BDD format (Given/When/Then) was **easier for analysts to think in**
- Instead of writing traditional specs, analysts could structure requirements as scenarios
- BDD became both a requirements format AND a test specification

## Evolution of the BDD process

### Phase 1: Analysts + QA write BDD
- Analysts took business requirements and wrote BDD scenarios with testers
- This was an improvement but still siloed

### Phase 2: Collaborative BDD sessions
- Introduced **cross-functional BDD sessions** with:
  - System analyst
  - Frontend developer
  - Backend developer
  - QA/Tester
- During sessions, the team would:
  - Synchronize understanding of requirements
  - Write BDD scenarios together
  - Discover edge cases from different perspectives (dev sees technical edges, QA sees failure modes, analyst knows business rules)
- After the session:
  - QA → writes test cases based on BDD
  - Developers → write code based on BDD
  - Analyst → formalizes and updates requirements documentation (often correcting on the fly during BDD sessions)

## Why BDD worked especially well in this domain
- Complex domain: electronic components, compliance, sanctions
- Business rules are critical — compliance violations are costly
- BDD scenarios are **committed to code** — living documentation
- "What is written with a pen cannot be cut with an axe" — BDD as source of truth
- New team members can read BDD to understand business rules

## Impact: -70% bug rate
- Better requirement coverage: edge cases caught during BDD sessions before coding
- Shared understanding: fewer "I thought it should work differently" bugs
- BDD scenarios = acceptance tests for business logic
- [INTERPRETATION] The 70% reduction likely comes from fewer requirements-related bugs, not fewer technical bugs

## Measurement: how -70% was calculated
- Counted **number of backend bugs** before and after BDD introduction
- Tracked statistics over time — still maintaining this data to this day
- After BDD was introduced on frontend too, similar improvement observed
- Acknowledged: "controversial metric" (bug count alone can be debated), but consistent trend

## Tooling
- **Behave** library (Python BDD framework)
- PyCharm's built-in Behave integration
- `.feature` files (Gherkin syntax) committed to the repository
- BDD scenarios are executable automated tests, not just documentation

## GAPS
- How many BDD sessions per sprint/feature — not specified
- Whether .feature files run in CI pipeline automatically — not specified
- Bug tracking tool used (Jira? YouTrack? GitLab issues?) — not specified
