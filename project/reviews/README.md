# Reviews

Focus uses exact-candidate reviews to test practical usefulness, misuse
resistance, canonical coherence, accessibility, publication hygiene, and
release integrity before publication. Review records are evidence about one
exact tree. They do not define the framework or prove general effectiveness.

## Clean content-candidate state

Generated records for the target release are absent from its clean content
candidate by design. They appear only in the final release tree at seven
predeclared allowlisted paths after valid exact-candidate reviews. Their absence
in that candidate is not missing documentation; their presence there would
violate reviewer isolation.

Review records from an earlier immutable release remain in later content
candidates as public project history. They do not approve the new target and
must not be treated as another current-release reviewer's findings.

The reusable [review prompts](prompts/README.md) are part of the content package.

## Required independent reviews

Six independent reviews are required:

1. Practical application.
2. Adversarial misuse.
3. Canonical coherence.
4. Accessibility and plain language.
5. Public hygiene.
6. Release integrity.

The disposition is produced only after all six reports are final. It is not an
independent review.

## Predeclared review-record allowlist

The v1.0.0 generated records remain historical release evidence at these paths:

- `project/reviews/v1.0.0-practical-application-review.md`
- `project/reviews/v1.0.0-adversarial-misuse-review.md`
- `project/reviews/v1.0.0-canonical-coherence-review.md`
- `project/reviews/v1.0.0-accessibility-and-plain-language-review.md`
- `project/reviews/v1.0.0-public-hygiene-review.md`
- `project/reviews/v1.0.0-release-integrity-review.md`
- `project/reviews/v1.0.0-review-disposition.md`

Only these v1.1.0 generated records may be added after the v1.1.0 clean content
candidate is reviewed:

- `project/reviews/v1.1.0-practical-application-review.md`
- `project/reviews/v1.1.0-adversarial-misuse-review.md`
- `project/reviews/v1.1.0-canonical-coherence-review.md`
- `project/reviews/v1.1.0-accessibility-and-plain-language-review.md`
- `project/reviews/v1.1.0-public-hygiene-review.md`
- `project/reviews/v1.1.0-release-integrity-review.md`
- `project/reviews/v1.1.0-review-disposition.md`

This README and every file under `project/reviews/prompts/` are content files,
not generated review records. They are excluded from the allowlist and must be
present in the clean content candidate.

Release-assembly verification and post-merge verification do not create in-tree
records. Their attestations remain outside the repository tree as described
below.

## Reviewer isolation

Each independent reviewer receives only:

- a clean checkout of the exact content-candidate commit and tree, with all
  target-release allowlisted generated review records absent;
- the assigned prompt; and
- the exact Commons release and commit adopted by the target release.

The reviewer must not receive or use:

- private research or source-inspiration history;
- prior conversations or memory;
- working branches or uncommitted changes;
- another current-release reviewer's findings or report;
- a disposition draft;
- pilot source content beyond the sanitized record in the candidate; or
- repository history outside the exact target unless the assigned prompt
  explicitly requires comparison with a named candidate.

If the exact commit or tree does not match, a target-release report already
exists in the review tree, required evidence is missing, or the source boundary
cannot be maintained, the reviewer stops with `NOT REVIEWED`.

## Review sequence

### 1. Complete content and pilot protocol

Complete all intended target-release content, including truthful status for any
pilot record. A planned, not-started, incomplete, reshaped, or stopped pilot is
valid when labeled accurately and supports no outcome claim. Pilot completion
is not required before the content candidate is prepared.

### 2. Finalize publication metadata

Before freezing the content candidate, replace phase-bound working-copy language
with publication-valid, phase-neutral metadata. The changelog identifies
target-release content without claiming that a branch is published. The
charter and citation metadata identify the target version. Citation metadata
may omit a release date until it is fixed; if included, that date must match the
planned publication. No content file may permanently claim that no review, tag,
or release exists.

Any later change to those content paths creates a new content candidate and
requires affected independent reviews to rerun.

### 3. Freeze the clean content candidate

Create an exact commit containing all release content except the seven
allowlisted generated review records. Record its commit and tree identifiers.
Confirm the working tree is clean.

### 4. Run six independent reviews

Give each reviewer a clean copy of that exact tree and only the assigned prompt.
Reviewers write their report outside the candidate tree first. Each report must
be publication-safe and name the exact commit, tree, scope, exclusions,
limitations, findings, and verdict.

### 5. Add evidence-only reports

After a report is approved for public placement, add it only at its predeclared
allowlisted path. Preserve byte identity with the approved source. Evidence-only
commits must not change any other path.

### 6. Correct through a new content candidate

If a finding requires any change outside the allowlist:

1. correct the content;
2. create a new clean content-candidate commit with generated records absent;
3. retain the superseded report and a publication-safe correction ledger outside
   the candidate so the final disposition can preserve review history;
4. rerun every affected independent review without access to superseded
   current-release findings; and
5. add only the final reports for the new target.

Do not let an old report approve a changed tree or expose it to an isolated
rerun reviewer. Superseded reports remain out of tree; after all final reviews
finish, the disposition owner may use their publication-safe bytes and the
correction ledger to account for findings, resolutions, and reruns.

### 7. Produce the disposition

After all six final reports are present for the same content candidate, use the
[disposition prompt](prompts/review-disposition.md). Account for every finding,
correction, rerun, limitation, and material dissent using the final reports,
publication-safe superseded reports, and complete correction ledger. Add the
final disposition only at its allowlisted path. Superseded reports and the
ledger do not enter the repository tree separately.

### 8. Freeze and verify release assembly

Freeze an exact final-release-candidate commit containing the reviewed content,
six reports, and disposition. Release-assembly verification may inspect the
accumulated tree because it is a verification pass, not an independent review.

It must verify that:

- only allowlisted records differ from the reviewed content candidate;
- every report is publication-safe and byte-identical to its approved source;
- links, metadata, license, Commons pin, required files, and release contents
  are consistent;
- all reports target the correct clean candidate and do not claim to review
  themselves; and
- the disposition does not conceal unresolved material findings.

The verifier cannot modify the candidate or add an in-tree artifact. It creates
a finalized publication-safe attestation outside the repository tree. After the
attestation bytes are final, compute a detached SHA-256 digest; do not embed that
digest inside the attestation it authenticates.

### 9. Merge, tag, release, and read back

The merged tree must exactly match the verified final-release-candidate tree.
The annotated immutable target-version tag message carries the detached
attestation digest. The public release metadata carries the byte-identical
complete attestation. Post-merge verification reads back the merged tree, tag,
release, authorship, links, file inventory, review-record bytes, attestation,
and digest.

## Severity model

| Severity | Meaning | Release effect |
| --- | --- | --- |
| Blocker | The target cannot be reviewed safely or would create material harm, false evidence, invalid release identity, or loss of authority | Stop; NO-GO |
| Material | A requirement, boundary, example, or release claim is wrong, missing, contradictory, or meaningfully unsafe | Correct and rerun affected review |
| Minor | A bounded clarity, navigation, accessibility, or consistency defect that does not invert the framework | Correct before release or accept explicitly with rationale |
| Suggestion | A non-required improvement that preserves current meaning | May defer with rationale |

A reviewer does not lower severity merely to produce a GO. Uncertainty should
be stated and paired with what evidence would resolve it.

## Finding format

Each finding includes:

- stable finding identifier;
- severity;
- exact repository-relative file and line or heading;
- evidence from the permitted source boundary;
- violated requirement or risk;
- practical impact;
- smallest acceptable correction; and
- whether a rerun is required.

Reports must also list the files inspected, limitations, and explicit tests that
found no issue. Absence of findings is not enough without stated coverage.

## Publication safety

Review records use role labels such as `Practical application reviewer`. They
must not name review tools, models, private paths, private prompts, source
history, personal pilot content, or generated-by provenance. Do not publish raw
logs, credentials, environment details, or hidden reasoning.

The exact target, evidence, finding, limitation, and disposition are the useful
public provenance.
