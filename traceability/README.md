# Traceability

Make coverage and gaps visible for every in-scope requirement. A matrix is a view of project records, not a second source of relationships.

## Create a coverage view

1. Copy [traceability-matrix-template.md](../templates/traceability-matrix-template.md) to a named scope such as `identity-coverage.md`.
2. State the scope and revision being assessed.
3. Start with every requirement in scope, including quality requirements without a use case.
4. Read canonical `requirements`, `verifies`, `use_cases` and `decisions` fields to populate the view.
5. Check execution summaries and evidence before describing a requirement as verified.

Use additional rows when a requirement has multiple test cases. Use `—` for a relationship that does not apply; describe missing coverage explicitly in the gap column. Expected results determine what a case covers; an ID relationship alone does not prove full acceptance coverage.

## Review checklist

- Are any in-scope requirements omitted?
- Do artifacts exist and agree with their canonical fields?
- Are missing tests distinguishable from tests that have not run?
- Are failing or blocked results visible?
- Is passing evidence relevant to the revision being assessed?

See [CONVENTIONS.md](../CONVENTIONS.md) and the [illustrative matrix](../examples/registration/coverage.md). Matrices are maintained manually for now; generated coverage and CI checks can follow once the convention is stable. This folder initially contains guidance only.
