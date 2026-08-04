# Contributing

Contributions are welcome when they improve the Focus Operating Framework
without weakening individual authority, selective admission, privacy,
provenance, tool replaceability, or the framework's documentation-only scope.

Read the [charter](framework/charter.md), [canonical language](CONTEXT.md), and
[governance](GOVERNANCE.md) before proposing a change.

## Before opening a proposal

Check that the change:

- serves one individual's Focus practice rather than a team or business
  workflow;
- preserves complete paper-only and unassisted paths;
- keeps AI advisory and external mutations separately human-controlled;
- does not require comprehensive capture, one authoritative tool, or a fixed
  lifecycle;
- distinguishes sources, derivatives, proposals, accepted records,
  projections, and records of authority;
- keeps Personal Mission Control optional and derived;
- uses canonical language consistently; and
- belongs in framework doctrine rather than an example implementation.

## Proposal types

### Editorial correction

Use for spelling, grammar, broken links, clearer phrasing, and other changes
that preserve meaning. Keep the change small and identify why it is
non-material.

### Material framework change

Use for a change to purpose, audience, commitments, concerns, moves, authority,
AI boundaries, physical-digital practice, Journal, Mission Control, evidence,
or governance. A material proposal must state:

1. the problem;
2. the affected canonical statements;
3. evidence and its limits;
4. alternatives considered;
5. consequences and migration implications;
6. privacy, authority, accessibility, and misuse risks;
7. compatibility with the adopted Commons release; and
8. unresolved questions or dissent.

A material change follows the full review and release path in
[governance](GOVERNANCE.md).

### Example or guidance change

Examples must be original, fictional, tool-neutral, and clearly illustrative.
They must identify purpose, life scope, assumptions, provenance, limits,
concerns, moves, authority decisions, boundaries, outcome, and lessons. They
cannot create requirements or claim effectiveness.

## Preparing a change

- Use direct Markdown and relative repository links.
- Use lowercase kebab-case content filenames.
- Update every affected canonical document rather than leaving contradictions.
- Add or update an ADR when the decision changes a durable boundary.
- Update the changelog for a material change.
- Do not add application code, schemas, provider-specific designs, automation,
  CI, runtime behavior, or conformance machinery to the documentation release.
- Do not include private context, personal records, confidential work,
  credentials, source-inspiration history, or review-tool attribution.
- Do not fabricate pilot episodes, review findings, approvals, dates, commits,
  trees, tags, receipts, or release evidence.

## Review expectations

Every change receives review proportionate to its risk. Material framework
changes require an exact-candidate practical, adversarial, coherence,
accessibility, public-hygiene, and release-integrity review, followed by a
documented disposition. A correction after review may require a new content
candidate and reruns.

The contributor should verify local links and headings, canonical terminology,
publication hygiene, metadata consistency, and the absence of unsupported
claims before requesting review.

## Privacy and security

Use fictional or fully abstracted examples. Never post personal Journal
material, private Check-Ins, credentials, confidential work, or identifying
third-party information in a public issue or pull request. Follow
[security guidance](SECURITY.md) for sensitive reports.

## License

Contributions accepted into this repository are licensed under the repository's
[MIT License](LICENSE). Do not submit material you do not have the right to
license under those terms.
