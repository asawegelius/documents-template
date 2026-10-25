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

# Requirement templates

This README describes the two requirement templates. When integrating it into a broader template repository, merge this guidance into the existing template index and retain its other template links.

## Available templates

| Template | Purpose |
|:---------|:--------|
| [functional-requirement-template.md](functional-requirement-template.md) | Define required behavior, business rules, success and failure outcomes |
| [non-functional-requirement-template.md](non-functional-requirement-template.md) | Define quality targets or constraints under explicit operating and measurement conditions |

See [requirements guidance](../requirements/README.md) for classification, IDs, categories, ownership, review and traceability.

## How to use

1. A human selects a template based on the requirement's content.
2. Copy it into `requirements/` and name it `REQ-<DOMAIN>-<NNN>-<short-name>.md`.
3. Allocate a stable ID and fill in the human owner and source. Keep the filename, metadata and heading consistent.
4. Write the requirement and acceptance criteria. Replace prompts and remove the author-guidance section. Use an explicit reason when a section is not applicable.
5. Keep uncertain facts and proposed targets visible. Do not present example values or agent suggestions as agreed requirements.
6. Request agent review, resolve findings and obtain human approval through the project's review process.
7. Update the affected requirement coverage view and related records.

## Shared metadata

- `id`: stable requirement identifier.
- `title`: short descriptive title.
- `type`: `functional` or `non_functional`.
- `status`: `draft`, `in_review`, `approved` or `deprecated`.
- `owner`: accountable human or human role; resolve the role to a person through project ownership rules.
- `source`: stakeholder, work item, parent requirement or explicitly labeled assumption.
- `decisions`: list of applicable ADR IDs, or `[]`.
- `category`: non-functional classification; used only in the non-functional template.

Templates contain intentional placeholders. Exclude `templates/` from live ID, coverage and completeness checks. Copies become project records and must satisfy the project's conventions.

## Human and agent responsibilities

The human writes, adds, adapts and approves requirements. The agent reviews and proposes improvements, questions and investigations. It must not approve requirements, invent sources, silently change scope or choose binding quality thresholds. Agent-review completion and human approval are separate facts recorded in the review process.

## Migration from a shared requirement template

Use the two new templates for new requirements. Preserve existing IDs. Classify existing records and improve them through review rather than blindly rewriting them. Replace old template links; if a compatibility pointer is retained, clearly direct authors to the two canonical templates.
