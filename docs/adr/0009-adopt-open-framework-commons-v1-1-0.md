# ADR 0009: Adopt Open Framework Commons v1.1.0

- **Status:** Accepted
- **Date:** 2026-08-22
- **Focus release:** v1.1.0
- **Public proposal:** [Commons v1.1.0 adoption proposal (Issue 6)](https://github.com/BradGroux/focus-operating-framework/issues/6)

## Context

Focus v1.0.0 adopted Open Framework Commons v1.0.0 while remaining independent
and explicitly deferring any Commons recognition to a separate Commons change.
Open Framework Commons v1.1.0 now recognizes Focus as the fifth independent
ecosystem product.

Focus governance requires a local compatibility review, explicit decision,
complete pin update, and Focus release before a newer Commons release has local
authority.

The exact upstream release is:

- annotated tag: `v1.1.0`;
- tag object: `79e5f06dab46f262cad1d1daf7840e683ffc3880`;
- peeled commit: `f25a2b89b4aed95984fd235e2e229efe52c125d8`; and
- tree: `3216f7dc5dc0172df163bf50c13f57013a9125ff`.

## Compatibility review

The tagged v1.0.0-to-v1.1.0 Commons diff leaves the shared principles and
research-and-review expectations unchanged. The shared boundary changes add
Focus to the complete product list and shared-applicability test. The upstream
recognition decision preserves Focus control of its purpose, audience, method,
terminology, evidence, releases, licensing, and implementations.

The release therefore conflicts with no Focus commitment, concern, move,
authority boundary, selective-admission rule, paper path, AI boundary, privacy
rule, or portable-exit requirement. No deviation from a Commons statement is
required.

## Decision

Adopt Open Framework Commons v1.1.0 by exact reference in Focus v1.1.0.
Recognize the upstream decision as an ecosystem relationship, not as a transfer
or inheritance of product authority.

Classify this as a backward-compatible minor Focus change because it updates an
external adoption boundary and current release metadata without changing Focus
practice meaning.

## Consequences

- Current Focus adoption surfaces pin Commons v1.1.0 and its peeled commit.
- Focus may truthfully state that Commons recognizes it as an independent
  ecosystem product.
- Focus v1.0.0 and its Commons v1.0.0 adoption record remain immutable.
- Later Commons changes still have no automatic authority in Focus.
- A later Commons adoption still requires a new Focus-local decision and
  release.

## Alternatives considered

- **Remain on Commons v1.0.0:** compatible but would leave current Focus
  documentation behind the release that recognizes Focus.
- **Treat recognition as automatic adoption:** rejected because it would violate
  both repositories' independence and local-decision boundaries.
- **Copy Commons statements into Focus:** rejected because exact adoption is a
  reference relationship, not inheritance or duplicated doctrine.
