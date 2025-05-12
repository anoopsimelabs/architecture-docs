# ADR-001: Database Schema Refactoring for Normalization, Consistency, and Integrity

## Status

Proposed - 13/05/2025

## Context

The current schema works fine as per the functionality, however there are many issues which could lead to trechnical debt and maintainability issues in a long term. Key observations include redundant and denormalized fields. Expecially, the people_user table conatins 50+ fields which could be normalized.

## Decision

- Normalize or restructure large tables.
- Naming convetions should be followed.
- Revisit default datatypes like varying(255)
- Maintain up to date ER diagram

## Consequences

### Pros

- Improved data integrity and query performance.
- Easier to maintain.

### Cons

- Requires significant refactoring throughout the application.
- Migration scripts need to be written to convert existing data to this structure.

## Alternatives Considered

- Instead of refcatoring the database, we can inlcude this as part of [ADR-002](./migrate-to-springboot.md) (This would be the **better solution**, to build that module from scratch)
- Concentrate only on the tables which has more than 10 fields. (This could make a mix of normalized and denormalized tables)

## Related

[Tables with field count](../others/tables-and-field-counts.md)
