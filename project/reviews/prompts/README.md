# Review prompts

These prompts are reusable, tool-neutral instructions for an exact Focus
release process. They are written to be copied into a clean reviewing task
after replacing every placeholder.

## Prompt inventory

### Independent reviews

1. [Practical application](practical-application.md)
2. [Adversarial misuse](adversarial-misuse.md)
3. [Canonical coherence](canonical-coherence.md)
4. [Accessibility and plain language](accessibility-and-plain-language.md)
5. [Public hygiene](public-hygiene.md)
6. [Release integrity](release-integrity.md)

### Synthesis and release verification

7. [Review disposition](review-disposition.md)
8. [Release-assembly verification](release-assembly-verification.md)
9. [Post-merge verification](post-merge-verification.md)

The first six are isolated independent reviews. The disposition begins only
after all six are complete. Release-assembly and post-merge work are verification
passes, not independent framework reviews.

## Required placeholders

Replace every applicable placeholder before giving a prompt to a reviewer:

| Placeholder | Value |
| --- | --- |
| `{{FOCUS_RELEASE}}` | Exact target Focus tag, such as `v1.1.0` |
| `{{CONTENT_CANDIDATE_COMMIT}}` | Full commit identifier for the clean content candidate |
| `{{CONTENT_CANDIDATE_TREE}}` | Full tree identifier for the clean content candidate |
| `{{CLEAN_TREE_PATH}}` | Read-only or detached path containing exactly that tree |
| `{{COMMONS_RELEASE}}` | Exact Commons tag adopted by the target Focus release |
| `{{COMMONS_COMMIT}}` | Full peeled commit for that Commons tag |
| `{{REPORT_PATH}}` | Exact predeclared output path for the assigned review |
| `{{CORRECTION_LEDGER_PATH}}` | Out-of-tree publication-safe ledger of findings, corrections, and reruns, or `NONE` |
| `{{SUPERSEDED_REPORT_SOURCE_DIRECTORY}}` | Out-of-tree publication-safe superseded report bytes, or `NONE` |
| `{{FINAL_CANDIDATE_COMMIT}}` | Full final-release-candidate commit identifier |
| `{{FINAL_CANDIDATE_TREE}}` | Full final-release-candidate tree identifier |
| `{{FINAL_CANDIDATE_PATH}}` | Read-only path containing exactly the final candidate |
| `{{APPROVED_REPORT_SOURCE_DIRECTORY}}` | Out-of-tree directory containing approved report bytes |
| `{{ALLOWLIST_MANIFEST_PATH}}` | Exact seven-path review-record allowlist manifest |
| `{{MERGED_COMMIT}}` | Full merged commit identifier |
| `{{MERGED_TREE}}` | Full merged tree identifier |
| `{{TAG_OBJECT}}` | Full annotated tag-object identifier |
| `{{ATTESTATION_PATH}}` | Publication-safe out-of-tree attestation path |
| `{{ATTESTATION_SHA256}}` | Detached SHA-256 of finalized attestation bytes |
| `{{PUBLIC_RELEASE_IDENTIFIER}}` | Public release record identifier for readback |

Do not leave a placeholder unresolved. If an input does not yet exist, the
review cannot begin.

## Clean-task setup

For each independent review:

1. Create a clean reviewing task with no prior project conversation, memory,
   private research, or other review report.
2. Provide only the populated assigned prompt, the exact clean content-candidate
   tree, and the exact adopted Commons release.
3. Ensure all target-release generated review-record paths are absent from the
   tree. Historical records from immutable earlier releases may remain.
4. Require the reviewer to verify commit, tree, cleanliness, source boundary,
   and report-path absence before reading content.
5. Have the reviewer write the report outside the candidate tree first.
6. Inspect the report for publication safety before placing it at the allowlisted
   destination.

Independent reviews should run without access to one another's current-release
work. Do not ask one reviewer to reconcile another current-release reviewer's
findings.

## Common severity model

- **Blocker:** unsafe or invalid review target, material harm, fabricated
  evidence, invalid release identity, or loss of authority. Stop and return
  `NO-GO` or `NOT REVIEWED` as applicable.
- **Material:** wrong, missing, contradictory, or meaningfully unsafe framework
  requirement or release condition. Correction and affected rerun required.
- **Minor:** bounded clarity, navigation, accessibility, or consistency defect.
  Correct before release or accept explicitly with rationale.
- **Suggestion:** non-required improvement that preserves meaning and may be
  deferred.

## Common finding format

Every finding uses:

1. `ID`
2. `Severity`
3. `Location`
4. `Evidence`
5. `Requirement or risk`
6. `Impact`
7. `Smallest acceptable correction`
8. `Rerun required`

## Public report rules

- Use the role label specified by the prompt.
- Name the exact commit, tree, scope, and permitted evidence.
- Include files inspected, tests performed, limitations, findings, and verdict.
- Keep tool, model, provider, environment, private-path, and hidden-reasoning
  details out of the report.
- Do not name private research, prior conversations, source inspiration, or
  personal pilot content.
- Do not claim general effectiveness.
- Do not modify the candidate tree.
- Do not place a report if its predeclared destination already exists.

## Report placement

The predeclared allowlist and complete workflow are in the
[reviews README](../README.md). Placement is an evidence-only step after the
report has been approved and checked for byte identity. Any change outside the
allowlist creates a new content candidate and requires affected independent
reviews to rerun.
