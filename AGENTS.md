# Repository instructions

## Purpose

This repository contains the Focus Operating Framework: an independent,
documentation-only framework for one individual's attention and continuity
across selected work and personal contexts.

## Authority

Apply this order:

1. Direct current owner instruction for active repository work.
2. [`framework/charter.md`](framework/charter.md).
3. Accepted decisions under [`docs/adr/`](docs/adr/).
4. Canonical documents under [`framework/`](framework/) and [`CONTEXT.md`](CONTEXT.md).
5. [`GOVERNANCE.md`](GOVERNANCE.md) and repository policies.
6. Examples, pilot records, review records, and project history.

Lower-authority material cannot silently redefine higher-authority material.
Brad Groux is the founding steward and release authority.

Focus adopts [Open Framework Commons
v1.1.0](https://github.com/BradGroux/open-framework-commons/tree/v1.1.0) at
commit
[`f25a2b89b4aed95984fd235e2e229efe52c125d8`](https://github.com/BradGroux/open-framework-commons/commit/f25a2b89b4aed95984fd235e2e229efe52c125d8)
by exact reference. If Commons and local guidance appear to conflict, stop and
surface the conflict. Do not silently copy, reinterpret, or change Commons.

## Framework boundaries

- Keep Focus scoped to one individual. The individual may choose work,
  personal, or combined life scope; do not introduce team ownership, shared
  Focus workspaces, assignments, manager views, or organizational workflow.
- Keep the method tool-agnostic and fully usable through paper-only,
  digital-only, unassisted, and AI-assisted paths.
- Treat paper as first-class. Never make digitization, proprietary materials,
  or destruction of a source necessary.
- Require selective admission. Do not add ambient capture, watched libraries,
  bulk ingestion, capture-everything, or whole-life indexing.
- Keep sources, derivatives, proposals, accepted records, projections, and
  records of authority distinct. Never use silent overwrite, silent merge, or
  latest-timestamp-wins.
- Keep AI optional, source-backed, proposal- and draft-only. AI cannot execute
  an external mutation, including after confirmation.
- Keep connectors optional and separately controlled. Permission never equals
  approval of a particular observation, draft, change, send, or deletion.
- Keep Personal Mission Control optional, derived, and non-authoritative. Do not
  turn it into an everything app, team command center, or required dashboard.
- Keep Journal material private and selectively resurfaced. A Transition
  Check-In becomes a Journal Entry only through explicit promotion.
- Preserve defer, release, stop, no action, portable exit, and manual
  continuity as valid outcomes.
- Do not add application code, schemas, provider-specific connector designs,
  automation, CI, runtime behavior, technical conformance, certification, or
  outcome guarantees to a documentation release.

## Documentation

- Write direct, clear Markdown for people and assisting reviewers.
- Use lowercase kebab-case for content filenames, except conventional root and
  directory index files.
- Keep local links relative and portable.
- Use canonical terms exactly as defined in [`CONTEXT.md`](CONTEXT.md).
- Separate principle, requirement, proposal, example, pilot observation,
  review finding, and open question.
- Keep examples fictional and explicitly non-authoritative.
- Use a diagram only when it materially clarifies authority or relationships;
  surrounding prose must remain sufficient.
- Keep private context, personal records, credentials, private paths, source
  history, review tools, model names, and generated-by attribution out of
  public files.
- Do not name external sources, source applications, creators, competitors, or
  frameworks other than the exact adopted Commons release.
- Do not claim that the owner pilot or documentation review proves general
  effectiveness.

## Review records

- Independent reviewers receive only an exact clean content-candidate tree,
  the assigned prompt, and the exact Commons release.
- Generated review records and the disposition must be absent from that clean
  tree.
- Review reports may be added only at the paths predeclared in
  [`project/reviews/README.md`](project/reviews/README.md).
- Any change outside the review-record allowlist creates a new content
  candidate and requires affected independent reviews to rerun without access
  to prior findings.
- Never create a review report, disposition, pilot result, attestation, or
  release claim without the evidence it names.

## Verification

Before reporting completion:

- inspect repository status, diff, branch, remote, and authorship when Git is
  available;
- check every local Markdown link and heading target;
- compare commitments, concerns, moves, authority language, AI boundaries,
  individual scope, and Commons pin across canonical documents;
- confirm all seven examples include their required structure and remain
  illustrative;
- inspect every public file for private history, outside-source references,
  credentials, unsupported claims, and attribution leakage;
- validate citation, license, changelog, version, and release metadata
  consistency;
- run the required independent review suite against an exact content-candidate
  commit; and
- compare the merged tree with the verified final-release-candidate tree before
  release.
