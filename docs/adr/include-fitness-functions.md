# ADR-005: Include Fitness Functions for Architecture Validation

## Status

Draft - 19/05/2025

## Context

As our system evolves, architectural integrity can degrade over time — leading to issues such as increased coupling, performance bottlenecks, and security gaps. We want to ensure that the architecture of our Spring Boot services remains aligned with our intended principles such as modularity, resilience, performance, and security.

To address this proactively, we propose incorporating **Fitness Functions** — automated checks that continuously validate architectural characteristics.

## Decision

We will incorporate fitness functions into the project to validate architectural characteristics such as:

- **Modular boundaries**: Using `ArchUnit` to ensure correct package and layer interactions.
- **Response time thresholds**: Using integration tests and/or observability tools to ensure SLAs are met.
- **Security enforcement**: Ensuring public APIs are secured via Spring Security (token-based).
- **Naming and package consistency**: Enforcing naming conventions and dependencies using `ArchUnit`.

These fitness functions will be:

- Implemented as part of the test suite using **ArchUnit** for structural rules.
- Optionally extended via **JUnit tests**, **Postman/Newman**, or **integration test frameworks** to validate runtime characteristics.
- Integrated into the CI/CD pipeline to fail builds if key architectural rules are violated.

## Consequences

### Positive

- Ensures continuous architectural compliance and visibility into architectural drift.
- Empowers developers to catch violations early in development.
- Simplifies governance and onboarding by documenting expected architecture.

### Negative

- Adds a small initial overhead to set up and maintain tests.
- May require tuning as the system evolves (e.g., response time thresholds).

## Alternatives Considered

- **Manual architectural reviews**: Less effective and scalable.
- **Tooling-only approaches without tests**: Miss the enforcement aspect and are harder to automate.

## Related Decisions

- Introduced ArchUnit for architectural rules validation.
- CI/CD pipeline includes architecture test stage.
