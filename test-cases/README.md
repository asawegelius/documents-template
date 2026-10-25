# Test cases

Define repeatable checks of requirement acceptance criteria. A case explains what to test; execution evidence records what actually happened.

## Create a test case

1. Copy [test-case-template.md](../templates/test-case-template.md).
2. Name it `TEST-<DOMAIN>-<NNN>-<short-name>.md`.
3. Set `verifies` to existing requirement IDs and `use_cases` to exercised use cases, or `[]` for a direct requirement test.
4. Describe test layer, preconditions, fixtures, steps and observable expected results.
5. Link automation when it exists. After execution, record source commit, environment, time, result and evidence.

## Review checklist

- Do expected results check linked acceptance criteria, including important failure paths?
- Can another person or agent repeat the check?
- Does automation map to a concrete test file or selector?
- Does any `passed` claim have relevant execution evidence?
- Have changed behavior or fixtures invalidated an earlier result?

Follow [CONVENTIONS.md](../CONVENTIONS.md). Keep `status` (document review) separate from `execution_status` (test run). Use `not_run` until executed. Use the [coverage view](../traceability/README.md) to expose gaps; see the [worked example](../examples/README.md). This folder initially contains guidance only.
