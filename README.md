# ACCREVA architecture notes

This repository explains selected design decisions without publishing product source code, deployment details, or customer information.

ACCREVA develops accounting and business operations software with a layered application architecture. The web client calls an API. Domain services enforce business rules. Repositories own database queries. Agent tooling uses approved application interfaces instead of direct database access.

## Published notes

- [Service boundaries](docs/service-boundaries.md)
- [Accounting integrity](docs/accounting-integrity.md)
- [Decision record process](docs/decision-records.md)
- [ADR 0001: API ownership of database writes](decisions/0001-api-owns-database-writes.md)
- [ADR 0002: Audited financial mutations](decisions/0002-audited-financial-mutations.md)

These notes describe design principles. They do not publish a production API contract or security certification.
