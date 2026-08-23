# Governance

- **Status:** Accepted governance for v1.1.0
- **Founding steward and release authority:** Brad Groux
- **Effective date:** 2026-08-04
- **Last amended:** 2026-08-22

## Purpose

This document governs how the Focus Operating Framework changes while remaining
individual, independent, tool-agnostic, and accountable to its
[charter](framework/charter.md) and adopted [Open Framework Commons
v1.1.0](https://github.com/BradGroux/open-framework-commons/tree/v1.1.0).

## Public authority

For active repository work, apply this order:

1. Direct current owner instruction.
2. The [charter](framework/charter.md).
3. Accepted decisions under [`docs/adr/`](docs/adr/).
4. Canonical framework documents and [`CONTEXT.md`](CONTEXT.md).
5. This governance document and accepted repository policies.
6. Examples, pilot records, review records, and project history.

Lower-authority material cannot silently redefine higher-authority material.
Examples show possibilities; pilot records show bounded owner experience;
reviews show findings against an exact target. None becomes doctrine without a
separate governed change.

The founding steward decides material framework changes and release baselines.
Contributors and reviewers may identify needs, gather bounded evidence, draft,
challenge, and review. That work grants no implicit authority over framework
meaning, accepted records, or external actions.

## Change classes

### Editorial change

An editorial change corrects or clarifies without changing meaning. It requires
a focused public change, proportionate review, local-link validation, canonical
language checks, and publication-hygiene review.

### Material framework change

A change is material when it affects the definition, mission, audience, first
job, commitments, concerns, moves, authority boundaries, selective admission,
physical-digital practice, Journal, AI assistance, connectors, Personal Mission
Control, evidence requirements, or governance.

A material change requires:

1. a public issue stating the problem, evidence, alternatives, consequences,
   and unresolved questions;
2. classification against the charter, accepted ADRs, and adopted Commons
   release;
3. a reviewable pull request updating every affected canonical surface;
4. an exact clean content-candidate commit;
5. independent practical, adversarial, canonical-coherence, accessibility,
   public-hygiene, and release-integrity reviews;
6. a disposition of every finding, rerun, limitation, and material dissent;
7. release-assembly verification of the final candidate; and
8. explicit steward approval in an identifiable semantic release.

### Charter or governance change

A charter amendment follows the charter's amendment rule. A material governance
change follows the material path and states who gains or loses authority,
transition conditions, effective date, compatibility implications, and dissent.

### Example, pilot, or review record

These records require truthful status, exact target or scope, limitations,
privacy, and publication-safety review. They cannot claim general effectiveness
or silently amend canonical guidance.

## Commons adoption

Focus adopts Open Framework Commons v1.1.0 exactly. The adopted annotated tag
peels to
[`f25a2b89b4aed95984fd235e2e229efe52c125d8`](https://github.com/BradGroux/open-framework-commons/commit/f25a2b89b4aed95984fd235e2e229efe52c125d8).

Focus owns its local purpose, method, terminology, examples, governance, and
releases. Commons owns its own shared statements and release decisions. Neither
repository changes the other automatically.

Adopting a newer Commons release requires a Focus-local issue, compatibility
review, explicit decision, updates to every pin and compatibility statement,
and a Focus release. If Focus must deviate from an adopted shared statement,
the release must identify the exact statement, rationale, consequences, and
steward decision.

Commons v1.1.0 recognizes Focus as an independent ecosystem product. The
recognition does not transfer product authority or alter Focus v1.0.0. The
v1.0.0 Focus tag and release remain immutable, and this repository adopts the
newer Commons release only through the v1.1.0 decision and release.

## Review authority and evidence

The review process is defined in
[`project/reviews/README.md`](project/reviews/README.md). Independent review
reports must name the exact content-candidate commit and tree. Reviewers receive
only the clean candidate, assigned prompt, and exact Commons release.

Generated review records may be added only at predeclared allowlisted paths.
Any non-review-file correction creates a new content candidate and requires the
affected independent reviews to rerun without access to prior reports.

The final disposition must account for every finding and material dissent. A
GO is a release recommendation against that exact target; it is not proof of
real-world effectiveness and does not replace steward approval.

## Release authority and sequence

The founding steward is the only release authority. Every Focus release
requires:

1. a complete documentation package;
2. a truthful owner-pilot protocol and status that make no unsupported evidence
   claim;
3. phase-neutral publication metadata finalized before review;
4. an exact content candidate and all required independent reviews;
5. a documented GO disposition that preserves findings, corrections, reruns,
   limitations, and material dissent;
6. a frozen final-release-candidate commit;
7. out-of-tree release-assembly verification and detached attestation digest;
8. a merged tree identical to the verified candidate;
9. an annotated immutable tag whose message includes the attestation digest;
10. release metadata containing the byte-identical attestation; and
11. post-merge public readback of authorship, tree, tag, release, links, and
    review records.

The owner pilot is an evidence track, not a release prerequisite. Its
completion, findings, and any resulting framework changes enter a later version
through this governance. A false pilot status or unsupported outcome claim
blocks release.

A material unresolved finding blocks release unless the final disposition
explicitly records a reasoned steward decision that the framework permits. No
record may conceal dissent or claim to review itself.

## Versioning

- **Patch:** clarification or correction without a change to meaning.
- **Minor:** backward-compatible guidance, examples, or optional patterns.
- **Major:** change to the charter, commitments, concerns, moves, authority
  boundaries, or other adoption-significant meaning.

Every release identifies the exact Commons release it adopts. Published tags
are immutable.

## Amendments

This governance document may be amended only through its applicable change
class. The amendment must be reviewable, identify consequences, preserve
material dissent, receive explicit steward approval, and appear in an
identifiable release. No example, pilot result, implementation, repeated
practice, or review report may amend governance silently.
