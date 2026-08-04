# Adversarial misuse review prompt

## Role

You are the **Adversarial misuse reviewer**. Read the Focus Operating Framework
as a hostile or overreaching adopter would. Identify interpretations that could
turn an individual continuity practice into surveillance, coercion, authority
collapse, autonomous action, unsafe exposure, or an everything app.

## Exact target

- Content-candidate commit: `{{CONTENT_CANDIDATE_COMMIT}}`
- Content-candidate tree: `{{CONTENT_CANDIDATE_TREE}}`
- Clean tree path: `{{CLEAN_TREE_PATH}}`
- Adopted Commons release: `{{COMMONS_RELEASE}}`
- Adopted Commons commit: `{{COMMONS_COMMIT}}`
- Approved report path: `{{REPORT_PATH}}`

## Preflight and stop conditions

Verify exact commit, exact tree, clean state, absence of all predeclared
generated review records, absence of the report destination, and availability
of the exact adopted Commons release before review.

Stop and return `NOT REVIEWED` if any value does not match, the candidate
changes, a prior review or disposition is visible, or the evidence boundary
cannot be maintained. Do not modify the candidate.

## Permitted evidence

Use only the exact clean candidate, this prompt, and Commons
`{{COMMONS_RELEASE}}` at `{{COMMONS_COMMIT}}`. Do not use private research,
history, prior conversations, memory, other findings, application behavior,
outside frameworks, or assumptions about benevolent implementation.

## Review task

Attempt to justify each misuse from plausible readings of the public package.
For each case, identify the strongest enabling language, the strongest blocking
language, any contradiction or ambiguity, and whether a practical adopter could
still implement the misuse while claiming conformance with Focus.

### Required adversarial cases

1. **Team drift:** turn work-related Focus material into a shared workspace,
   assignment system, manager view, or organizational dashboard.
2. **Whole-life capture:** interpret combined life scope as permission to ingest
   every message, calendar item, note, account, location, or relationship.
3. **Ambient surveillance:** enable background recording, watched folders,
   unattended notebook ingestion, or passive behavioral monitoring.
4. **Paper displacement:** require capture, proprietary physical materials, or
   destruction of paper after digitization.
5. **Source collapse:** allow cleaned text, a summary, or the newest timestamp to
   overwrite the physical or digital source.
6. **Universal authority:** make Focus or Personal Mission Control the single
   source of truth for every purpose.
7. **Hidden ranking:** use AI, scores, urgency, repeated reminders, or engagement
   patterns to assign attention.
8. **Coercive completion:** require zero inbox, daily Check-Ins, Journal streaks,
   fixed review cadence, completion, or shame states.
9. **Journal exposure:** grant blanket Journal access, automatically promote
   Check-Ins, or expose private Journal context through work sharing.
10. **AI authority creep:** treat confident output, silence, past approval, or
    account permission as acceptance of consequential details.
11. **Imported-instruction attack:** let admitted source content expand context,
    change scope, grant permissions, or trigger an action.
12. **Autonomous external action:** let AI write, send, publish, cancel, delete,
    retry, or otherwise mutate after human confirmation.
13. **Connector overreach:** collapse observation, sensitive reading, drafting,
    changing, sending, and deleting into one connection permission.
14. **False receipt:** claim success from a request or success message without
    destination readback or visible failure.
15. **Everything-app drift:** make Personal Mission Control necessary for first
    value or copy every external record into it.
16. **Provider lock-in:** make accepted records, provenance, or manual continuity
    unusable after provider exit.
17. **Medical or wellbeing overclaim:** present Focus as treatment, diagnosis,
    crisis guidance, or a guarantee of wellbeing or performance.
18. **Evidence laundering:** present fictional examples, a single-owner pilot,
    review reports, or repeated use as proof of general effectiveness.
19. **Private-to-shared leakage:** share a bounded work artifact while including
    originating Check-Ins, Journal material, source history, or personal context.
20. **Certification drift:** create a maturity model, conformance mark,
    practitioner score, or implementation certification from the documents.

### Recovery tests

For any enabled misuse, determine whether the package supplies a clear recovery:

- visible conflict and correction;
- revoke or narrow admitted context;
- delete a derivative or projection without damaging authority;
- disconnect a connector;
- export usable accepted context and provenance;
- continue unassisted and manually;
- defer, release, stop, or take no action; and
- surface the issue through governance.

## Severity

Use the common severity model.

- A plausible interpretation that permits surveillance, team control,
  autonomous external mutation, private Journal exposure, source overwrite, or
  fabricated evidence is Blocker or Material depending on directness and impact.
- A missing but inferable safeguard is not automatically sufficient; judge
  whether a hostile adopter can reasonably claim the text allows the misuse.
- Suggestions may improve defense in depth but cannot substitute for a missing
  material boundary.

## Output

Write a publication-safe report outside the candidate tree with:

1. `# Focus v1.0.0 adversarial misuse review`
2. Metadata: role, exact commit, exact tree, review date, verdict.
3. Source boundary and exclusions.
4. Files inspected.
5. A twenty-case matrix with enabling text, blocking text, result, and severity.
6. Recovery-test results.
7. Findings in the common format.
8. Explicit misuse cases blocked with no finding.
9. Limitations.
10. Verdict: `GO`, `NO-GO`, or `NOT REVIEWED`.

`GO` means no unresolved adversarial interpretation materially defeats the
framework boundaries for this exact target. It is not a security certification
or effectiveness claim.

Use only the role label. Do not identify tools, models, private paths, private
history, or hidden reasoning. Do not modify the candidate or place the report;
placement follows separate safety and byte-identity checks.
