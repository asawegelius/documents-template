# State Model Template

## Entity

Entity name

## Purpose

Why this state model exists.

## States

| State | Meaning | Terminal |
|:------|:--------|:---------|
| STATE_A | Explain the state | No |
| STATE_B | Explain the state | Yes |

## Transitions

| From | To | Trigger | Rules |
|:-----|:---|:--------|:------|
| STATE_A | STATE_B | Event or action | Business rule |

## Invariants

- Invariant 1
- Invariant 2

## Time-Based Rules

- Expiration
- Retry window
- Lockout period

## Audit and Security Notes

- Which transitions are audit-sensitive?
- Which transitions should produce security events?
