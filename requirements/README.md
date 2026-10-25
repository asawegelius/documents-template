# Requirements

Record required outcomes and constraints here. Each file contains one independently verifiable requirement, including measurable quality requirements.

## Create a requirement

1. Copy [requirements-template.md](../templates/requirements-template.md).
2. Name it `REQ-<DOMAIN>-<NNN>-<short-name>.md`.
3. Fill in identity, owner, source, scope, required behavior and observable acceptance criteria.
4. Request review before treating proposed behavior as agreed scope.

Use [CONVENTIONS.md](../CONVENTIONS.md) for statuses and relationships. Record uncertain behavior as an open question or explicit assumption. Avoid quality statements such as "fast" or "secure" without measurable criteria.

## Review checklist

- Is the requirement necessary, unambiguous and testable?
- Is its source or assumption explicit?
- Are relevant boundary conditions and failure behavior specified?
- Can tests prove each acceptance criterion?
- Does the [coverage matrix](../traceability/README.md) expose missing tests or evidence?

Use cases reference requirements through `requirements`; tests reference them through `verifies`. Requirements do not maintain duplicate reverse lists. See the [worked example](../examples/README.md). This folder initially contains guidance only.
