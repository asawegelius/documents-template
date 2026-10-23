# API Contract Template

## Endpoint

`METHOD /path`

## Purpose

What this endpoint is for and who should call it.

## Authentication and Authorization

- Who may call it?
- What token, client, or trust assumptions exist?

## Request

### Headers

- `Content-Type`
- `Authorization`

### Body

```json
{
  "example": "value"
}
```

## Response

### Success

Status:

```json
{
  "example": "value"
}
```

### Errors

| Status | Code | Meaning |
|:-------|:-----|:--------|
| 400 | ERR-TEMPLATE-BAD-REQUEST | Invalid request |
| 401 | ERR-TEMPLATE-UNAUTHORIZED | Missing or invalid authentication |
| 403 | ERR-TEMPLATE-FORBIDDEN | Authenticated but not allowed |
| 409 | ERR-TEMPLATE-CONFLICT | Conflict with current state |

## Side Effects

- State changes
- Audit events
- Security events

## Notes

- Idempotency:
- Rate limits:
- Versioning:
