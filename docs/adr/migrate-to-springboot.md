# ADR-001: Migrate Authentication from Python to Spring Boot service

## Status

Proposed - 13/05/2025

## Context

The current authentication system is built using a Python service, but it's a resourcing bottleneck and hard to maintain. It also handles token validation for other spring boot services, creating unnecessary coupling and latency.

## Decision

We will migrate the authentication to Spring Boot services, so the resource could be easily mananged technology wise.

## Consequences

- Resourcing would be easy as all other services are written in Java
- Centralized user, role, and token management
- Improved maintainability and scalability
- Short-term migration effort required

## Alternatives Considered

- Using Keycloak to handle all authentication and user management. (This would be hard in our scenerio as it includes employees)
- Using Auth0 or Cognito (involves recurring costs)
