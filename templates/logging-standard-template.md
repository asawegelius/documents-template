# Logging Standard Template

## Purpose

Explain what this logging standard covers and why it exists.

## Logging Categories

- Application
- Security
- Audit

## Required Structured Fields

- `timestamp`
- `level`
- `service`
- `event_id`
- `outcome`
- `error_code`
- `trace_id` or `correlation_id`

## Event Taxonomy

Describe the event ID namespace and ownership rules.

## Sensitive Data Rules

Describe what must never be logged and what should be minimized.

## Error Logging Rules

Describe how business failures, validation failures, and unexpected exceptions should differ.

## Review Questions

- Are the important events actually logged?
- Are the logs machine-friendly?
- Are error codes and event IDs stable and documented?
- Is sensitive data handled correctly?
