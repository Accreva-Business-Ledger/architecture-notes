# Accounting integrity

Accreva treats accounting rules as application and database invariants.

## Journal entries

- Total debits must equal total credits before posting.
- A line contains a debit or a credit, not both.
- The server assigns identifiers and entry numbers.
- Posted entries remain immutable. Corrections use reversals.

## Approval

The server records approval actors and timestamps. Clients cannot supply approval identities or mark records approved without an authorized transition.

## Tenant scope

Queries and mutations use the active company identifier. Services verify that referenced accounts and business records belong to the same company.

## Audit records

Each financial mutation records the actor, action, target, and change context. Audit records support review and investigation. They do not replace source documents or legal retention duties.
