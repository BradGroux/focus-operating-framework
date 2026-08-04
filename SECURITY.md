# Security and privacy

The Focus Operating Framework is documentation, not deployed software. Security
reports for this repository concern the public documentation, repository
configuration, release process, and accidental disclosure of sensitive
material. Implementations require their own security design, threat model,
testing, and reporting process.

## Report privately

Use the repository's private vulnerability-reporting form:

<https://github.com/BradGroux/focus-operating-framework/security/advisories/new>

Use that private form for:

- exposed credentials, tokens, keys, or private links;
- personal, confidential, or third-party information committed by mistake;
- unsafe release or repository permissions;
- a documentation pattern that would predictably cause unauthorized access,
  disclosure, overwrite, deletion, or external action; or
- a vulnerability in any future repository-owned validation surface.

Do not place sensitive details in a public issue, pull request, example, pilot
record, or review report. Share only the minimum information needed to reproduce
and understand the concern.

If the private form is unavailable, do not publish the sensitive material. Open
a minimal public issue stating only that the private reporting path is
unavailable and asking the steward to restore it. The public issue is not a
private report and must contain no sensitive detail.

## Framework security boundaries

Focus requires implementations and practices to preserve these boundaries:

- selective admission rather than ambient or comprehensive capture;
- explicit purpose, authority, retention, and provider exposure;
- separation of sources, derivatives, proposals, accepted records, and
  projections;
- visible freshness and unresolved conflicts;
- explicit promotion into named records of authority;
- separate connector authority for observation, sensitive reading, drafting,
  changing, sending, and deleting;
- exact human preview and confirmation before an external mutation;
- Action Receipts with destination readback or visible failure;
- imported content treated as data, never as authority to act;
- private Journal material resurfaced only through deliberate selection;
- disconnect, deletion, usable export, and manual continuity; and
- no autonomous external mutation by AI assistance.

These are framework requirements, not a claim that any implementation is
secure.

## Response

The steward will confirm receipt through the private channel, assess scope and
severity, preserve necessary evidence, and coordinate a proportionate fix. A
public notice should disclose only what practitioners need to understand the
risk and remedy. Credentials and personal information must never be repeated in
the public notice.

## Out of scope

General product suggestions, framework disagreements, and non-sensitive
documentation corrections belong in the normal contribution process. Medical,
therapeutic, legal, employment, crisis, and personal-safety guidance is outside
the framework's scope.
