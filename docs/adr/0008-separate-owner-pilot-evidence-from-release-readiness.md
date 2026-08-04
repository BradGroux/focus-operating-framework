# ADR 0008: Separate owner-pilot evidence from release readiness

- **Status:** Accepted
- **Date:** 2026-08-04

## Context

Focus v1.0.0 is a documentation framework, not an application or an efficacy
claim. Its release can establish the method, boundaries, examples, and review
process without claiming that the method has already produced real-world
outcomes.

Requiring a three-week owner pilot before the initial documentation release
would conflate two different questions: whether the public framework is
complete and reviewable, and what one individual later observes while using
it. It would also make an intentionally empty evidence protocol a release
failure even when the repository makes no effectiveness claim.

## Decision

Focus v1.0.0 includes a bounded owner-pilot protocol, but completion of that
pilot is not a prerequisite for the v1.0.0 content candidate or release.

The pilot may begin before or after publication. Any result must come from
actual use, remain sanitized, and retain its single-practitioner evidence
limit. A planned, not-started, incomplete, reshaped, or stopped pilot is valid
when labeled truthfully and cannot be presented as evidence of effectiveness.

Completed pilot results and any framework changes they support enter a later
version through normal governance and review. Fabricated pilot evidence,
unsupported outcome claims, or a release that misstates pilot status remains a
release blocker.

## Consequences

- v1.0.0 can publish the complete agnostic framework without waiting three
  calendar weeks.
- Release reviews assess the pilot protocol, status accuracy, privacy boundary,
  and evidence claims; they do not require a completed result.
- The owner pilot remains a meaningful evidence track with its original
  coverage, pass, reshape, and stop criteria.
- A later pilot result may support correction or refinement, but cannot prove
  general effectiveness, safety, clinical value, or suitability for everyone.
