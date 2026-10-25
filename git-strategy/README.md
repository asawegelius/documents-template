# Git strategy

This section describes an optional `develop` / `test` / `main` promotion model. Adapt the model to the project; documentation traceability also works with simpler branching.

## Reading order

1. [Overview](01-overview.md)
2. [Branching model](02-branching-model.md)
3. [Feature development](03-feature-development.md)
4. [Bugfix handling](04-bugfix-handling.md)
5. [Versioning and tagging](05-versioning-and-tagging.md) — currently an empty placeholder
6. [CI/CD flow](06-ci-cd-flow.md) — currently an empty placeholder

Diagrams are in `diagrams/`. The text explains the workflow without requiring an image reader.

## Applying the guidance

- Confirm which branches exist and what protections apply before following commands.
- Use a task branch and pull request. Direct merge/push commands in the chapters are examples, not authorization or a substitute for required checks.
- Use the project's work-item system; Jira is an example. Link requirement, use case and test IDs in the pull request independently of branch names.
- Record evidence for the actual tested revision and rerun affected checks after integration changes.
- Define release owners, checks, tagging policy and promotion approvals before using the unfinished release chapters.

## Review checklist

- Does the model fit the release cadence and contributors?
- Can a change be traced from requirement to evidence and pull request?
- Are fixes propagated to every affected supported line?
- Are release permissions explicit for both people and agents?

See [CONVENTIONS.md](../CONVENTIONS.md) and [AGENTS.md](../AGENTS.md). No CI workflows or branch protection settings are installed by these documents.
