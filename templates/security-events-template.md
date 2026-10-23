# Security Events Template

## Purpose

Describe which security-relevant events must be logged for this module or service.

## Logging Standard

Each event should be traceable in logs, tests, and monitoring.

Expected fields:

- `event_id`
- `error_code` when the event is linked to a failed operation
- `trace_id` or `correlation_id` when available
- `actor_type`
- `actor_id`
- `source`
- `outcome`
- `timestamp`
- `metadata`

## Event Table

| Event ID | Description | Logged By | Mandatory | Notes |
|:---------|:------------|:----------|:----------|:------|
| SEC-TEMPLATE-001 | Example security event | Example Service | Yes | Add the triggering condition |

## Review Questions

- Is the event useful for incident investigation?
- Does it reveal too much sensitive data?
- Is it linked to test cases and alerting where needed?
- Can the event be correlated with the failing request or flow?
