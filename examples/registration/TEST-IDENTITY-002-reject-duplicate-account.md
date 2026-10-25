---
id: TEST-IDENTITY-002
title: Duplicate registration leaves account state unchanged
status: draft
owner: "Example test owner role"
verifies: [REQ-IDENTITY-001]
use_cases: [UC-IDENTITY-001]
decisions: []
execution_status: not_run
---

# TEST-IDENTITY-002: Duplicate registration leaves account state unchanged

## Purpose and test layer

Component test design for [REQ-IDENTITY-001](REQ-IDENTITY-001-register-account.md), AC-2, through alternative A1 of [UC-IDENTITY-001](UC-IDENTITY-001-register-account.md).

## Preconditions and test data

An isolated environment contains an account for `existing.user@example.test`. Capture its persisted state and total account count N. Choose and record a synthetic password valid under the adopting project's policy when implementing the test.

## Steps

1. Submit registration using the exact existing email and a valid synthetic password.
2. Observe the outcome, total account count and persisted state of the existing account.

## Expected results

For AC-2, registration is rejected, total account count stays N, and persisted state of the existing account matches its starting state. The specific public response is subject to the open question in the requirement.

## Automation

Not automated. No application or fixture implementation is supplied by this documentation example.

## Latest execution

No execution recorded. Time, executor, source commit, environment, actual results and evidence are unavailable. This case is `not_run`; it proves no implemented behavior.
