---
id: REQ-DOMAIN-000
title: "Replace with the required quality or constraint"
type: non_functional
category: "Choose an agreed category"
status: draft
owner: "Unassigned — identify the accountable human before approval"
source: "Identify a source reference or explicitly label an assumption"
decisions: []
---

# REQ-DOMAIN-000: Required quality or constraint

## Need and consequence

Who depends on this quality? Explain the practical consequence of missing it and the rationale for the target. Link to the source where possible.

## Scope

- Applies to: specific operations, components, interfaces or system boundary.
- Exclusions: explicit boundaries; a system-wide claim must be justified.

## Requirement

Under the defined operating conditions, state the quality level or constraint the system must satisfy. Keep proposed targets visibly provisional until a human agrees to them.

## Operating scenario and measurement conditions

Describe enough context for another person or agent to repeat the assessment. Complete relevant fields and explain any that do not apply.

| Condition | Definition |
|:----------|:-----------|
| Trigger or event | Request, sustained load, dependency failure, recovery event or change scenario |
| Workload and traffic mix | Arrival rate or concurrency, operation mix, burst pattern and relevant user behavior |
| Data | Dataset size, distribution, growth assumptions and fixture version |
| Environment and resource envelope | Relevant topology, runtime configuration and allowed resources or cost |
| Dependencies | Expected behavior, latency or simulated failures of external systems |
| Duration and preparation | Measurement window, warm-up policy, cache state and repetition where relevant |
| Measurement boundary | Exact start/end points, included work, instrumentation and units |

## Acceptance criteria

| Criterion | Observable measure or constraint | Acceptance threshold | Conditions |
|:----------|:---------------------------------|:---------------------|:-----------|
| AC-1 | Define the quality measure, such as a latency percentile or recovery time | Human-agreed limit or objectively checkable condition | Identify the scenario above |
| AC-2 | Add a complementary measure when needed, such as error rate or allowed data loss | Human-agreed limit | Identify the relevant scenario |

Define pass/fail precisely. For latency, state percentile and units, which requests are counted and how errors are handled. For recovery, define both restored service and allowable data loss. For non-numeric constraints, define an objective inspection or test procedure. Do not use "fast", "scalable" or "easy to maintain" without a verifiable meaning.

## Verification plan

- Method: benchmark, load test, failure experiment, inspection, analysis or another specified method.
- Early investigation: which architecture-critical assumption needs testing before a dependent design decision, and what result will inform that decision?
- Implementation verification: how the implemented system will be checked under representative conditions.
- Recheck triggers: relevant code, configuration, dependency, data-volume or workload changes.
- Evidence required: source commit, environment, configuration/fixtures, actual conditions, results and report or execution record.

Concrete tests declare their requirement links in `verifies`. Approval of this requirement and completion of an early prototype do not prove implemented compliance.

## Architecture considerations and tradeoffs

Identify decisions that could make this target hard to meet, interactions with other requirements and options worth investigating. Record approved design choices in ADRs and add their IDs to `decisions`. Do not turn a tentative solution into a mandatory design by implication.

## Assumptions and open questions

| Assumption or question | Consequence if wrong or unresolved | Human owner | Resolve before |
|:-----------------------|:-----------------------------------|:------------|:---------------|
| Unknown workload, target or dependency behavior; replace or state None | Architectural or acceptance impact | Responsible person or role | Specific decision or milestone |

An unknown that prevents agreement on acceptance must be resolved before approval, or isolated in a separate draft requirement. Agents may suggest investigations and candidate targets; humans decide binding thresholds and tradeoffs.

## Review record

- Agent review: Not requested. Replace with a link to findings and the reviewed revision when available.
- Human disposition: Pending. Record decisions on proposed targets and material findings.
- Human approval: Not approved. Record approver and approval reference before setting `status: approved`.

## Author guidance — remove after copying

Use the [requirements guidance](../requirements/README.md). Select a category from the agreed list. Keep only applicable conditions and criteria, with explicit reasons for omissions. Keep IDs and criterion labels stable. The human authors, adapts and approves the requirement; the agent reviews and proposes. The review record refers to the current material revision and must be refreshed after substantive changes.
