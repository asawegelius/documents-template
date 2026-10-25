---
id: TEST-IDENTITY-001
title: New registration creates one pending account
status: draft
owner: "Example test owner role"
verifies: [REQ-IDENTITY-001]
use_cases: [UC-IDENTITY-001]
decisions: []
execution_status: not_run
---

# TEST-IDENTITY-001: New registration creates one pending account

## Purpose and test layer

Component test design for [REQ-IDENTITY-001](REQ-IDENTITY-001-register-account.md), AC-1, through the main flow of [UC-IDENTITY-001](UC-IDENTITY-001-register-account.md).

## Preconditions and test data

An isolated test environment has no account for `new.user@example.test`. Record total account count N. Input password is synthetic and valid under the adopting project's password policy; choose and record the exact fixture when implementing this test.

## Steps

1. Submit registration with that address and the valid test password.
2. Observe the result and query persisted account state.

## Expected results

For AC-1, the result indicates success, total account count is N+1, exactly one account has the submitted email, and its status is `pending_verification`.

## Automation

Not automated. No application or fixture implementation is supplied by this documentation example.

## Latest execution

No execution recorded. Time, executor, source commit, environment, actual results and evidence are unavailable. This case is `not_run`; it proves no implemented behavior.
