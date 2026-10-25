# Requirements

This folder contains the project's functional and non-functional requirements. Each file defines one independently reviewable requirement with observable acceptance criteria.

A human owns the requirements: people write, add, adapt and approve them. A requirements-review agent helps identify weaknesses and proposes improvements. Agent review does not authorize new scope or approve a requirement.

## Functional and non-functional requirements

| Type | Question answered | Example |
|:-----|:------------------|:--------|
| Functional | What behavior must the system provide? | A visitor can register a pending account. |
| Non-functional | What quality level or constraint must the system satisfy under defined conditions? | Order creation meets an agreed latency target at a specified load and data volume. |

Classify by content, not topic. Account lockout after failed login attempts is functional behavior even though it concerns security. A recovery-time objective is a non-functional requirement. When one statement mixes behavior with an independently verifiable quality target, split it into linked requirements.

## Organization and identity

Keep both types in this folder. Type is explicit in metadata; it is not encoded in the ID or a mandatory subfolder.

- Filename: `REQ-<DOMAIN>-<NNN>-<short-name>.md`.
- ID: `REQ-<DOMAIN>-<NNN>`, such as `REQ-ORDERS-001`.
- Domain: an agreed uppercase alphabetic name; use `SYSTEM` for genuinely system-wide requirements.
- Number: at least three digits, unique within the domain across both types.
- Preserve IDs after creation and never reuse them. Reclassification does not change identity.
- Check existing records and open work before allocating an ID.

Examples: `REQ-ORDERS-001-create-order.md` and `REQ-ORDERS-002-order-creation-latency.md`.

## Choose a template

| Template | Use for |
|:---------|:--------|
| [Functional requirement](../templates/functional-requirement-template.md) | Required behavior, rules and observable outcomes |
| [Non-functional requirement](../templates/non-functional-requirement-template.md) | Measurable quality targets and explicit system constraints |

Both use `id`, `title`, `type`, `status`, `owner`, `source` and `decisions`. Non-functional requirements additionally use `category`.

Allowed types are `functional` and `non_functional`. Review statuses are `draft`, `in_review`, `approved` and `deprecated`. These describe the document's agreement state, not implementation progress or test results.

Start with these non-functional categories: `performance`, `capacity`, `availability`, `recoverability`, `reliability`, `security`, `privacy`, `accessibility`, `maintainability`, `operability` and `compatibility`. Agree and document extensions when needed. Category does not replace measurable criteria.

## Writing a functional requirement

Describe the trigger, necessary starting conditions, required behavior and observable outcome. Include important failure and boundary conditions. Separate a user's need from a proposed implementation unless the implementation itself is a justified constraint.

Give acceptance criteria local labels such as `AC-1` and `AC-2`. A test can then state precisely which criteria it checks. Labels remain stable; add new ones instead of renumbering existing criteria.

## Writing a non-functional requirement

Begin with the need and the consequence of missing it. Describe:

1. The operations or components to which the requirement applies.
2. The operating scenario: load, data volume, duration, dependencies and relevant environment.
3. The observed response or quality attribute and its measurement boundary.
4. The acceptance threshold and how to verify it.
5. Any uncertain assumptions that could change architecture or feasibility.

For performance, identify workload and traffic mix, dataset size, measurement boundary, latency distribution, acceptable errors and resource envelope where relevant. A latency target without those conditions is not reproducible. Recovery targets need a failure scenario and an explicit definition of restored service and allowable data loss.

Do not invent a number to complete the template. A provisional target must be labeled as a proposal and confirmed by the human owner. Record unknowns with an owner, impact and resolution point. If an unknown prevents agreement on a criterion, keep that criterion's requirement unapproved or split the unresolved concern into a separate draft requirement.

Not every quality constraint needs a numeric threshold. For example, an explicit compatibility matrix can be checked by inspection and tests. Acceptance must still be objective and its verification method explicit.

## Review and approval

1. The human author drafts the requirement and identifies its source and accountable human owner.
2. The agent reviews clarity, necessity, scope, consistency, testability and relevant quality risks. It identifies missing information and proposes wording without silently replacing the original intent.
3. The human resolves findings, chooses targets and accepts, modifies or rejects suggestions. Uncertain technical questions may become time-boxed investigations.
4. An accountable human approver records approval in a pull request or equivalent review record. Author and approver may be the same person where project policy allows.
5. Material changes return approved requirements to `in_review` and trigger review of affected use cases, decisions, implementation and tests.

Agent findings should state the observation, consequence, suggested improvement and human decision or investigation needed. Record review against the reviewed revision. Keep agent-review completion separate from approval; a clean agent report does not make a requirement approved.

## Address architecture risks early

Before committing to a significant architecture decision, identify affected quality requirements and high-impact assumptions. Use a focused prototype, benchmark, failure experiment or analysis when uncertainty could make the design expensive to change.

Early investigation reduces uncertainty. Final verification still needs representative conditions and evidence for the implemented system. A prototype result alone does not prove that the production system meets the requirement.

Record a decision's rationale in an ADR and reference it through the requirement's `decisions` field. If constraints conflict, the human owner decides the tradeoff and records the resulting requirement changes; an agent must not quietly weaken a target.

## Traceability and verification

- Use cases declare requirement IDs in `requirements`.
- Test cases declare requirement IDs in `verifies` and identify the acceptance criteria checked.
- Tests may verify non-functional requirements directly without a use case.
- Requirements declare applicable ADR IDs in `decisions`; use `[]` when none apply.
- Use relative Markdown links for navigation. Canonical relationships remain in metadata; avoid competing reverse lists.
- Include every in-scope requirement in coverage views, regardless of type.
- Distinguish no test design, tests not run, failing or blocked tests, and passing execution evidence.

Approval means the requirement is agreed. Verification requires evidence: tested commit, environment, conditions, actual results and a report or execution record. Reassess evidence when relevant requirements, implementation or configuration change.

## Checklist before approval

- Is the source explicit and the human owner identified?
- Is one clear obligation described, with explicit scope?
- Are acceptance criteria objective, complete enough and mutually consistent?
- Are important failure and boundary conditions covered?
- For quality targets, are operating and measurement conditions sufficiently defined?
- Is verification feasible, and are architecture-critical assumptions addressed before dependent decisions?
- Have agent findings received a human disposition where they affect acceptance?
- Is approval recorded independently of agent-review completion?

These are documentation conventions. This package does not install an automated validator or enforce a review workflow.
