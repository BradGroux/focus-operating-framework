# Governance

- **Status:** Accepted governance for v2026.09.05
- **Founding steward and release authority:** Brad Groux
- **Effective date:** 2026-08-04
- **Last amended:** 2026-09-05

## Purpose

This document governs how the Focus Operating Framework changes while remaining
individual, independent, tool-agnostic, and accountable to its
[charter](framework/charter.md) and adopted [Open Framework Commons
v2026.09.05](https://github.com/BradGroux/open-framework-commons/tree/v2026.09.05).

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
8. explicit steward approval in an identifiable documentation edition.

### Charter or governance change

A charter amendment follows the charter's amendment rule. A material governance
change follows the material path and states who gains or loses authority,
transition conditions, effective date, compatibility implications, and dissent.

### Example, pilot, or review record

These records require truthful status, exact target or scope, limitations,
privacy, and publication-safety review. They cannot claim general effectiveness
or silently amend canonical guidance.

## Commons adoption

Focus adopts Open Framework Commons v2026.09.05 exactly. The adopted annotated tag
peels to
[`8868a248457dd7b663563beb243c5ebcbb8ac360`](https://github.com/BradGroux/open-framework-commons/commit/8868a248457dd7b663563beb243c5ebcbb8ac360).

Focus owns its local purpose, method, terminology, examples, governance, and
releases. Commons owns its own shared statements and release decisions. Neither
repository changes the other automatically.

Adopting a newer Commons release requires a Focus-local issue, compatibility
review, explicit decision, updates to every pin and compatibility statement,
and a Focus release. If Focus must deviate from an adopted shared statement,
the release must identify the exact statement, rationale, consequences, and
steward decision.

The [calendar and adoption decision](docs/adr/0010-calendar-editions-and-commons-adoption.md)
records provenance, compatibility and authority. Historical v1.0.0 and v1.1.0
adoptions remain unchanged. No shared tooling, repository layout or review quota
is imported. Focus applies its own review and publication process.

When adopted guidance appears to conflict, pause the disputed action only,
identify both statements and the exact adopted tag and commit, and record the
question through the local issue process. The steward decides Focus meaning;
only Commons authority decides Commons meaning. Record rationale, uncertainty,
dissent and any deviation or deferral with an owner and revisit trigger. Resume
only within the recorded decision and existing authority. Silence is not approval.

## Evidence and compatibility decisions

Material decisions distinguish chosen values, textual interpretation, actual
observation and effect claims. Record supporting context, limits, the strongest
counterexample, alternatives, rationale and dissent in the issue or ADR. Defer
unsupported empirical claims with an owner and evidence-based revisit trigger.
No volume of fictional scenarios replaces practitioner or specialist evidence.
Help, accommodation and feedback need not be earned through contribution.

## Review authority and evidence

Calendar editions use two reviewers independent of content preparation to cover
all six lenses and produce six scoped reports, as defined in the review process.
Independence is from preparation and the other reviewer; three reports from one
reviewer are not three independent opinions. This prospective assignment changes
no historical evidence and transfers no release authority. It reduces reviewer
coordination while retaining coverage, exact targets and correction reruns.

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

New documentation editions use `YYYY.MM.DD` and annotated tags `vYYYY.MM.DD`,
based on the actual UTC publication date. Additional editions that day use `.1`,
then `.2`. Compare date components chronologically and correction suffixes
numerically; do not sort suffixes lexically. The first dated edition follows
v1.1.0. Historical tags, releases, citations, decisions and review records keep
their original identities; never add dated aliases or move a published tag.

The date does not promise compatibility, quality or effectiveness. Release
notes separately identify the predecessor, changed reader decisions, authority,
responsibilities, optional paths, adoption consequences and evidence limits.
A spelling fix is editorial only if choices stay unchanged. A clarification
that changes what someone may or must do is substantive even if the diff is
small. Required new behavior or transferred authority is potentially
incompatible and requires explicit steward disposition.

Every edition independently identifies its Commons pin. Implementations retain
their own package, runtime and schema versions; no such surfaces exist here.
See the [release runbook](project/RELEASING.md) for runnable publication and
readback steps, same-day corrections and historical verification limits.

## Amendments

This governance document may be amended only through its applicable change
class. The amendment must be reviewable, identify consequences, preserve
material dissent, receive explicit steward approval, and appear in an
identifiable release. No example, pilot result, implementation, repeated
practice, or review report may amend governance silently.
