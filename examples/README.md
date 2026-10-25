# Worked examples

These are illustrative design records, not approved product requirements or proof of implemented behavior. Exclude this folder from live project IDs and coverage calculations.

## Registration

1. [Requirement](registration/REQ-IDENTITY-001-register-account.md): observable behavior and acceptance criteria.
2. [Use case](registration/UC-IDENTITY-001-register-account.md): actor interaction, including duplicate registration.
3. [Success test](registration/TEST-IDENTITY-001-register-new-account.md): verifies AC-1.
4. [Duplicate test](registration/TEST-IDENTITY-002-reject-duplicate-account.md): verifies AC-2.
5. [Coverage](registration/coverage.md): both criteria have test designs; neither test has been run.

The previous `use-cases/example-use-case.md` has been replaced by this connected example. Its references to undefined requirements have been replaced with an explicit illustrative requirement.

Real registration would need additional requirements and tests for validation, password handling, email delivery, verification, abuse prevention and privacy. Those behaviors are outside this example's scope.
