# Use cases

Describe how an actor achieves a goal, including alternative and failure paths. Keep implementation details in design documents unless a requirement explicitly constrains implementation.

## Create a use case

1. Copy [use-case-template.md](../templates/use-case-template.md).
2. Name it `UC-<DOMAIN>-<NNN>-<short-name>.md`.
3. Fill in actors, trigger, preconditions, success and failure postconditions, main flow and alternatives.
4. Put existing requirement IDs in `requirements`, and add navigable links in the body.

## Review checklist

- Does the flow have a clear actor goal and trigger?
- Do alternatives identify the step or condition where they diverge?
- Are outputs, state changes and failure outcomes explicit?
- Are linked requirements actually illustrated by this flow?
- Are important paths covered by tests in the [coverage view](../traceability/README.md)?

Follow [CONVENTIONS.md](../CONVENTIONS.md). Quality constraints may be tested directly without a use case. The illustrative registration use case lives under [examples/](../examples/README.md); this folder is reserved for live project records.
