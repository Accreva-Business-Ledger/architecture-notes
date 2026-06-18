# ADR 0001: API owns database writes

- Status: Accepted
- Date: 2026-06-18

## Context

Web clients and agent components need one enforcement point for authorization, tenant scope, accounting rules, and audit records.

## Decision

The API owns database writes. Web clients call the API. Agent components use approved tools that route changes through application services. Repositories perform ORM queries under the active tenant scope.

## Consequences

One service enforces mutation rules. Clients cannot bypass domain checks through direct database access. API availability becomes a dependency for write operations.
