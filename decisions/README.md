# Architecture decisions

Record significant design choices, their context, alternatives and consequences. Use an ADR when future contributors will need to understand why a choice was made.

## Create a decision record

1. Copy [adr-template.md](../templates/adr-template.md).
2. Name it `ADR-<NNN>-<short-name>.md`.
3. Identify owner, relevant artifacts, constraints, alternatives and resulting decision.
4. Review the proposal with the responsible decision maker.

Follow [CONVENTIONS.md](../CONVENTIONS.md) for metadata and review status. Requirements, use cases and tests link to ADRs using `decisions`. The ADR's `related` field identifies affected artifacts; it does not imply test coverage.

## Review checklist

- Is the problem and decision scope clear?
- Are alternatives and negative consequences recorded?
- Does the choice conflict with an accepted requirement?
- Is follow-up work explicit?

When replacing an approved decision, preserve its rationale, mark the old record deprecated with a link to the replacement, and review incoming references. This folder initially contains guidance only.
