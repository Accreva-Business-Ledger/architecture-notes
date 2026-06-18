# ADR 0002: Audited financial mutations

- Status: Accepted
- Date: 2026-06-18

## Context

Financial systems need a record of who changed data, which record changed, and which operation caused the change.

## Decision

Application services write an audit record for each financial mutation. The server supplies actor identity and timestamps from the authenticated request context.

## Consequences

Reviews and investigations can trace application changes. Mutation workflows must fail when they cannot preserve the required audit record.
