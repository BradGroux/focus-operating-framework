# ADR 0002: Require explicit authority and provenance

- **Status:** Accepted
- **Date:** 2026-08-04

## Context

Physical sources, digital records, derivatives, projections, and external
systems can disagree. Treating the newest or most convenient copy as truth
would hide provenance, correction, and accountable ownership.

## Decision

Focus does not act as a universal source of truth. The individual designates the
record of authority for each purpose. Physical sources, captured images, literal
derivatives, corrected derivatives, accepted records, projections, and external
destinations retain distinct identities.

Focus preserves provenance, human review, and promotion history. It never
resolves conflicts through silent merge, silent overwrite, or
latest-timestamp-wins.

## Consequences

- Different purposes may use different records of authority.
- A derivative does not become authoritative by existing.
- Promotion requires human approval and a named destination.
- Conflicts remain visible until accountable review resolves them.
- Paper and replaceable digital systems can coexist without obscuring control.
