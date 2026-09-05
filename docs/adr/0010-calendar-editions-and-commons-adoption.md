# ADR 0010: Calendar editions and exact Commons adoption

- **Status:** Accepted for edition 2026.09.05
- **Date:** 2026-09-05
- **Authority:** Brad Groux, founding steward and release authority
- **Proposal:** [Issue 9](https://github.com/BradGroux/focus-operating-framework/issues/9)

## Decision and provenance

Prospectively use UTC calendar documentation editions and retain compatibility
as a separate content judgment. Adopt Open Framework Commons v2026.09.05:

- repository: [Open Framework Commons](https://github.com/BradGroux/open-framework-commons/tree/v2026.09.05);
- annotated tag object: `67914a6e305768206f1ead83dfcbc4325b951168`;
- peeled commit: `8868a248457dd7b663563beb243c5ebcbb8ac360`;
- tree: `c139b847583e9550440ce6ac138b01cc8c710e89`.

Authenticated repository metadata and Git objects agree on these identities.
The upstream tag is annotated and unsigned. Focus has no required signing
policy; existing branch protection is retained. Publication authority for this
edition is the founding steward's explicit instruction to audit, remediate,
merge and publish the next calendar edition.

## Applicability and compatibility

The adopted principles clarify chosen commitments: contribution earns no claim
on others, asking for help needs no prior contribution, privacy limits openness,
and continuity does not override disengagement. These support Focus's personal
capacity, private Journal and stopping boundaries. They supply no empirical
claim that Focus improves performance or wellbeing.

Commons governance now specifies a bounded conflict pause, discoverable exact
adoption and honest exceptions; research guidance calls for reasoned evidence
and counterexamples. Focus applies these to its own decisions and six review
lenses. Upstream Decision 0002, adverse cases, audit disposition and release
procedure were considered. Commons's validation software, CI, dependencies and
repository controls are local stewardship, not shared adoption requirements.
No exception to shared principles or boundaries is needed. No shared-guidance
item is deferred. Product-local tooling and processes remain independently
chosen, not omitted obligations.

Affected active surfaces are AGENTS.md, charter, governance, README, citation,
VERSION, release specification, release notes and review instructions. The
practice changes are assessed in [ADR 0011](0011-minimum-practice-and-receipt-evidence.md).
The date identifies this edition, not compatibility with the previous one.

## Alternatives and limits

Retaining Commons v1.1.0 was legitimate but would omit compatible human-boundary
clarifications and the new explicit conflict guidance. Automatic adoption or
copying shared statements was rejected. Requiring Focus to orchestrate work,
relationship stewardship or contribution would cross its individual scope;
those purposes remain independent, and no product requires Focus or its view.

Historical v1.0.0 and v1.1.0 identities and evidence remain unchanged. No runtime,
package, schema or machine consumer requiring semantic versions exists in this
tracked repository. External consumers may need to accept a calendar string;
they must pin an exact edition and assess meaning separately. No external
consumer migration or other product adoption is claimed.

No material dissent is recorded at decision preparation. Preserve review dissent
in the edition disposition. The steward revisits adoption if a specific shared
statement conflicts with actual local guidance; disputed action pauses while
unrelated authorized work continues.
