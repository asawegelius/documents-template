# Requirement coverage

## Scope and revision

- Scope: Define included domains and exclusions.
- Revision: Record the commit or pull request revision being assessed.
- Maintainer: Responsible role or person.
- Updated: ISO 8601 date.

## Coverage

| Requirement | Use case | Test case | Criteria checked | Execution | Evidence | Gap / next action |
|:------------|:---------|:----------|:-----------------|:----------|:---------|:------------------|
| REQ-DOMAIN-001 | UC-DOMAIN-001 | TEST-DOMAIN-001 | AC-1 | not_run | — | Execute; identify any remaining criteria |
| REQ-DOMAIN-002 | — | — | — | — | — | Test design missing; assign follow-up |

## Guidance

- Begin with every in-scope requirement, including constraints without a use case.
- Use relative links for actual records and evidence.
- Add rows for multiple tests. List all acceptance criteria or explicitly expose unchecked ones.
- Derive relationships from canonical metadata; do not create relationships here.
- Use `not_run`, `passed`, `failed` or `blocked` only for existing test cases.
- A `passed` case verifies only the criteria its expected results actually cover, for the tested revision and environment.
- Do not call a requirement verified while relevant criteria or execution evidence are missing.
- Exclude `templates/` and `examples/` from live coverage.
- This view is maintained manually for now. See [CONVENTIONS.md](../CONVENTIONS.md).
