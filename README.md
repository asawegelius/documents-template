# Documents template

A shared documentation structure for people and development agents. Connect project intent, decisions, behavior and verification in Git.

## Start here

1. Read the [documentation conventions](CONVENTIONS.md).
2. Follow the [registration example](examples/README.md) from requirement to test design and evidence.
3. Copy the necessary [templates](templates/README.md) into the destination folders below.
4. Review documentation and implementation together in a pull request.

Agents also read [AGENTS.md](AGENTS.md). People and agents use the same artifact definitions and acceptance criteria.

## Structure

| Location | Responsibility |
|:---------|:---------------|
| [requirements/](requirements/README.md) | Required outcomes, constraints and measurable acceptance criteria |
| [use-cases/](use-cases/README.md) | Actor goals, flows and exceptions |
| [test-cases/](test-cases/README.md) | Repeatable verification scenarios and evidence references |
| [decisions/](decisions/README.md) | Significant design decisions and their consequences |
| [traceability/](traceability/README.md) | Requirement coverage and visible gaps |
| [glossary/](glossary/README.md) | Shared meaning of domain terms |
| [git-strategy/](git-strategy/README.md) | Branching, review and release guidance |
| [templates/](templates/README.md) | Reusable starting documents |
| [examples/](examples/README.md) | Illustrative records, excluded from live project coverage |

## Smallest useful workflow

1. Write a testable requirement and identify its owner and source.
2. Add a use case when an actor interaction needs explanation. Quality constraints can be tested directly.
3. Design tests with explicit inputs, expected results and requirement IDs.
4. Implement within the agreed scope; link the work item and pull request to the affected IDs.
5. Run relevant checks. Record the tested commit, environment, result and evidence location.
6. Refresh coverage and review the changes. An approved document or an existing test case does not prove working software.

Use additional architecture, API, state, security and operational templates when needed. Choose and document their destination folders before using them; not every template is needed for every change.

## Adopting this template

- Replace this introduction with the project's purpose, scope and entry points.
- Choose domain prefixes, document owners, reviewers and the project's Definition of Done.
- Keep illustrative records in `examples/` or remove that folder; never count them as project evidence.
- Choose a branching and release model. The supplied `develop` / `test` / `main` model is an option.
- Configure actual validation commands and required checks. No CI or branch protections are installed by this template.
- Choose a license before distributing the template for reuse; no license is currently supplied.

## Current maturity

This is a documentation starter. Relationships and status values are defined in `CONVENTIONS.md`; automated schema validation, generated coverage and CI enforcement are future work. The versioning and CI/CD chapters in `git-strategy/` are currently empty placeholders.
