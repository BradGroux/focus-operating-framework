# ADR 0007: Keep the public framework self-contained

- **Status:** Accepted
- **Date:** 2026-08-04

## Context

Public documentation should be evaluated from its own claims. Naming outside
origins, inspiration history, or local workflow would make the framework
dependent on unavailable context and weaken clean review of the framework's own
claims.

## Decision

The public Focus repository contains original, self-contained framework material
and fictional examples without naming research sources, source applications,
source creators, competitors, private paths, private handoffs, or inspiration
history.

Open Framework Commons is the sole permitted external framework reference
because Focus explicitly adopts an exact Commons release. Public review records
remain sanitized, tool-neutral, and tied to exact candidate commits. Source and
inspiration history does not enter the public package.

## Consequences

- Public readers can evaluate Focus from the repository itself.
- Review prompts exclude private research and prior conversations.
- Examples remain original, fictional, and non-authoritative.
- Public records preserve decisions and evidence without naming assisting tools
  or private source history.
