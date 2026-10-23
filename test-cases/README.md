# Test Cases

This folder contains concrete test scenarios for platform and product behavior.

Test cases should be used together with:

- requirements
- use cases
- ADRs
- traceability matrices
- test strategy documents

## Purpose

Use test case documents to make important behavior explicit before or during implementation.

They help answer:

- what should be tested
- why the test matters
- which artifacts define the expected behavior
- which outcomes prove the behavior is correct


## Naming Guidance

- Test case files: `TEST-DOMAIN-001-short-name.md`
- Example: `TEST-IDN-001-register-user-creates-pending-account.md`

## Relationship to Traceability

Each important use case should eventually point to one or more test case IDs in the relevant traceability matrix.

Use the traceability matrix to see:

- which use cases already have test coverage defined
- which behaviors still need test cases
- which work items or ADRs affect the test design
