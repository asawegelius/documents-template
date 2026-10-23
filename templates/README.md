# Templates

This folder contains the canonical reusable templates for this repository.

These templates are meant to support two goals:

1. Make new documents easier to start consistently.
2. Act as the seed for a future standalone documentation template project.

## Available Templates

- [requirements-template.md](requirements-template.md)
- [use-case-template.md](use-case-template.md)
- [traceability-matrix-template.md](traceability-matrix-template.md)
- [security-events-template.md](security-events-template.md)
- [adr-template.md](adr-template.md)
- [service-overview-template.md](service-overview-template.md)
- [api-contract-template.md](api-contract-template.md)
- [database-design-review-template.md](database-design-review-template.md)
- [logging-standard-template.md](logging-standard-template.md)
- [state-model-template.md](state-model-template.md)
- [test-case-template.md](test-case-template.md)
- [test-strategy-template.md](test-strategy-template.md)
- [threat-model-template.md](threat-model-template.md)
- [solo-kanban-board-template.md](solo-kanban-board-template.md)

## How to Use

1. Copy the template you need.
2. Rename it to match the module or decision you are documenting.
3. Remove guidance text that is no longer needed.
4. Link the document to requirements, use cases, and tests where relevant.

## Naming Guidance

- Requirements: `domain-requirements.md`
- Use cases: `UC-DOMAIN-001-short-name.md`
- ADRs: `ADR-001-short-title.md`
- State models: `entity-state-model.md`
- Threat models: `module-threat-model.md`

## Note

Some older template files still exist in their original folders as compatibility pointers.
Use the files in this folder as the canonical source from now on.
