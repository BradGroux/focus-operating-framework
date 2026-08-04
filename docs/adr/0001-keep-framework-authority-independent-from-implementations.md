# ADR 0001: Keep framework authority independent from implementations

- **Status:** Accepted
- **Date:** 2026-08-04

## Context

Focus may eventually be demonstrated through an application. If that
application becomes the framework's authority, its screens, providers, storage,
and commercial constraints could silently redefine Focus and make a tool
necessary for adoption.

## Decision

The Focus Operating Framework begins as an independent, tool-agnostic
documentation framework. Any application is a non-authoritative example
implementation that pins an exact framework release and cannot redefine the
framework.

Focus may define Personal Mission Control as an optional, stack-agnostic derived
pattern. No dashboard or application is required, and Mission Control never
becomes a record of authority.

## Consequences

- The framework remains usable through paper and ordinary digital surfaces.
- Implementations may vary without changing canonical meaning.
- Application architecture, schemas, providers, and screens remain deferred.
- An implementation must identify the exact Focus release it applies.
