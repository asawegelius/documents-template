---
id: REQ-IDENTITY-001
title: Register a pending account
status: draft
owner: "Example product owner role"
source: "Illustrative assumption for this template; not a stakeholder-approved requirement"
decisions: []
---

# REQ-IDENTITY-001: Register a pending account

## Purpose and scope

Allow registration using an email address not already associated with an account. This example assumes syntactically valid email and password inputs. Email normalization, credential policy, verification delivery and abuse controls require separate requirements in a real system.

## Requirement

For a valid new registration, create one account with status `pending_verification`. Reject registration using an already registered email without creating or changing an account.

## Acceptance criteria

- AC-1: Given no account for `new.user@example.test`, when valid registration is submitted, exactly one account for that address exists with status `pending_verification`, and the caller receives a success outcome.
- AC-2: Given an account for `existing.user@example.test`, when registration is submitted with that exact address, the caller receives a rejection outcome, account count is unchanged, and the existing account is unchanged.

## Rationale

Illustrate a requirement with both a success and a failure condition that can be independently tested.

## Open questions

Before adopting this example, decide the public response policy for duplicate addresses, including the risk of revealing account existence. This example does not prescribe an HTTP status or message.
