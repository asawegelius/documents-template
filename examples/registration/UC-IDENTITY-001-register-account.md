---
id: UC-IDENTITY-001
title: Register an account
status: draft
owner: "Example product owner role"
requirements: [REQ-IDENTITY-001]
decisions: []
---

# UC-IDENTITY-001: Register an account

## Goal and actors

A visitor wants to create an account.

## Trigger

The visitor submits a registration form.

## Preconditions

Valid email and password inputs are available. The main flow uses an email not already registered.

## Postconditions

- Success: exactly one account exists for the submitted address with status `pending_verification`.
- Failure: duplicate registration creates no account and leaves the existing account unchanged.

## Main flow

1. Visitor enters valid registration data.
2. Visitor submits the form.
3. System creates a pending account.
4. System returns a success outcome.

## Alternative and failure flows

- A1 (step 3): The email already belongs to an account. The system rejects the registration, does not change the existing account and creates no additional account.

## Data notes

Inputs are email and password. Synthetic data only is used in the example tests. Password and email handling controls require separate requirements.

## Related artifacts

[REQ-IDENTITY-001](REQ-IDENTITY-001-register-account.md), criteria AC-1 and AC-2. Test navigation is provided by the [coverage view](coverage.md).

## Open questions

The public duplicate-response policy is unresolved in the linked requirement.
