# Templates

Canonical reusable starting documents. Copy them into project folders; keep live records out of this directory.

## Core traceability templates

| Template | Destination | Responsibility |
|:---------|:------------|:---------------|
| [Requirement](requirements-template.md) | `requirements/` | One testable requirement with acceptance criteria |
| [Use case](use-case-template.md) | `use-cases/` | Actor goal and main/alternative flows |
| [Test case](test-case-template.md) | `test-cases/` | Verification design and execution evidence |
| [ADR](adr-template.md) | `decisions/` | Decision context, alternatives and consequences |
| [Coverage matrix](traceability-matrix-template.md) | `traceability/` | Derived requirement coverage and gaps |

Core records use the YAML metadata and relationships defined in [CONVENTIONS.md](../CONVENTIONS.md). Follow the [worked example](../examples/README.md).

## Supporting templates

Choose and document a destination folder when adopting these templates. Their current formats are descriptive Markdown; they do not yet share the core metadata contract.

- [Service overview](service-overview-template.md)
- [API contract](api-contract-template.md)
- [Database design review](database-design-review-template.md)
- [State model](state-model-template.md)
- [Threat model](threat-model-template.md)
- [Logging standard](logging-standard-template.md)
- [Security events](security-events-template.md)
- [Test strategy](test-strategy-template.md)
- [Solo Kanban board](solo-kanban-board-template.md)

## How to use

1. Choose only the templates needed for the change.
2. Copy to the destination folder and allocate a stable ID where applicable.
3. Fill in metadata and content, replacing all placeholders.
4. Keep canonical relationships in metadata and navigable relative links in the body.
5. Remove author guidance sections; submit for review.
6. Update the affected coverage view.

Templates intentionally contain sample IDs and empty fields. Exclude them from live project ID and coverage validation. Changes to a template affect future copies; review existing records separately rather than silently rewriting them.
