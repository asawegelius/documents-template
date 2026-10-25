# Documentation conventions

These rules apply to project records created from the templates. Markdown holds readable content; YAML front matter holds identity, status and canonical relationships. Templates are instructions and examples are illustrative: exclude both from live coverage and ID validation.

## Identity and location

| Artifact | ID pattern | Destination |
|:---------|:-----------|:------------|
| Requirement | `REQ-<DOMAIN>-<NNN>` | `requirements/<ID>-<short-name>.md` |
| Use case | `UC-<DOMAIN>-<NNN>` | `use-cases/<ID>-<short-name>.md` |
| Test case | `TEST-<DOMAIN>-<NNN>` | `test-cases/<ID>-<short-name>.md` |
| Architecture decision | `ADR-<NNN>` | `decisions/<ID>-<short-name>.md` |

Use an uppercase alphabetic domain, such as `IDENTITY`, and a number of at least three digits. IDs are unique across live project records, stable after creation and never reused. Filenames may change without changing the ID. Check existing IDs and open pull requests before assigning an ID; resolve collisions before merging.

Use one requirement per file so it can be reviewed and linked independently. Each independently verifiable quality constraint also gets a requirement ID. Split requirements with unrelated acceptance conditions.

## Required metadata

Core records use these fields:

```yaml
---
id: REQ-IDENTITY-001
title: Register an account
status: draft
owner: "Project role or person responsible for this record"
---
```

`status` describes document review: `draft`, `in_review`, `approved`, or `deprecated`. Move a draft to review when ready; an accountable reviewer approves through the project's review process. Record review in a pull request or equivalent review record. Material changes to approved content return it to `in_review`. Deprecation preserves the record and explains its replacement or reason. Review authority follows project roles and the user's authorization.

An owner is accountable for content, not necessarily its author. Keep unresolved owners and unknown facts explicit. Do not invent a person, decision or approval to complete a field.

## Canonical relationships

| Record | Field | Meaning |
|:-------|:------|:--------|
| Requirement | `source` (string) | Stakeholder statement, work item, parent requirement or other origin; identify assumptions explicitly |
| Use case | `requirements` (list of IDs) | Requirements illustrated by this flow |
| Test case | `verifies` (list of IDs) | Requirements whose acceptance criteria this test actually checks |
| Test case | `use_cases` (list of IDs) | Use cases exercised; may be empty for direct requirement tests |
| Requirement, use case or test | `decisions` (list of IDs) | Relevant ADRs; may be empty |
| ADR | `related` (list of IDs) | Artifacts affected by the decision; may be empty |

An empty list is `[]`. Nonempty lists contain exact existing IDs, never `TBD`. Missing coverage is a gap, not a fictional link. Every use case needs at least one requirement; every test needs at least one requirement it verifies. Not every requirement needs a use case or ADR. A requirement may have multiple tests; a test may verify multiple requirements only when its expected results explicitly address each one.

Store each relationship in its canonical field above. Use relative Markdown links in the body for navigation. Reverse links and matrices are derived views: review them against canonical fields rather than maintaining competing relationship lists. Coverage matrices are currently maintained manually.

## Verification and evidence

Test document status and execution result are independent. Test cases have `execution_status`: `not_run`, `passed`, `failed`, or `blocked`. `passed` requires evidence from a real execution, not a predicted outcome. In the execution section record:

- Execution time in ISO 8601 with timezone, executor or automation identity, and exact source commit.
- Environment and relevant configuration or fixture version.
- Actual result and a link to a CI run, report or committed manual execution record.

The execution section summarizes the latest relevant run; retain historical evidence in CI/report storage or versioned execution records. If no run exists, use `not_run` and say so. When behavior, acceptance criteria, test code or relevant configuration changes, reset the affected case to `not_run` until rerun. Old results remain evidence for their original commit and environment only. An unrelated edit need not invalidate evidence; explain relevance during review.

## Coverage and change control

Start coverage from **all in-scope requirements**, including quality requirements with no use case. Distinguish missing test design, tests not run, failing tests and current passing evidence. A test definition alone is not verification.

For each change, review affected requirements, use cases, decisions, tests, implementation and evidence. Update affected records together. Record unresolved questions, owners and follow-up work explicitly. Deprecating a record also requires reviewing incoming references.

A change is ready when its acceptance criteria are satisfied, required checks have run, evidence identifies the tested revision, and unresolved gaps are resolved or explicitly accepted by the responsible reviewer with rationale. Project-specific release criteria may be stricter.

## Validation to automate after adoption

This is a proposed validation contract; no validator or CI enforcement is included yet:

1. Unique IDs; valid metadata, ID patterns and enumerated status values.
2. Existing relative links and correctly typed relationship targets.
3. Requirements for each use case and test; no dangling references.
4. Requirement-first coverage, including gaps and direct tests of quality constraints.
5. Evidence fields for executed tests, especially `passed`; evidence relevance to the target revision remains a review responsibility.

Separate structural checks from semantic review. A script can establish that a link resolves; a reviewer must establish that the test proves the requirement.
