# Threat Model Template

## Scope

What component, service, or flow is being analyzed?

## Assets

- Sensitive data
- Credentials
- Tokens
- Business-critical operations

## Actors

- Legitimate users
- Administrators
- Internal services
- Attackers

## Trust Boundaries

- Client to public API
- Public API to internal services
- Service to database

## Abuse Cases

| Threat | Impact | Likelihood | Current Mitigation | Needed Follow-Up |
|:-------|:-------|:-----------|:-------------------|:-----------------|
| Example threat | Medium | Medium | Existing control | Additional work |

## Controls

- Authentication controls
- Authorization controls
- Logging and monitoring
- Rate limiting
- Data protection

## Open Risks

- Risk 1
- Risk 2
