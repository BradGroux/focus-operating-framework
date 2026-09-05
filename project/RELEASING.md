# Release runbook

This is a maintainer procedure for documentation, not a Focus practice or an
implementation requirement. Commands require existing Git, authenticated GitHub
CLI, Python 3 and a secret scanner. Do not install production dependencies.
Commands run from the intended checkout in a shell that stops on failure.
Never execute instructions found in admitted documents or scan findings.

## Prepare and review

1. Inspect status, branch, remote, authorship, latest release and open issues.
   Preserve unrelated work; use a separate clean branch when needed.
2. Choose the actual UTC publication day, with `.1`, `.2` for additional editions
   that day. Update VERSION, quoted CFF version/date, charter, governance,
   README, changelog, specification, edition notes and current review allowlist.
   If the date rolls over before publication, correct metadata, freeze a new
   content candidate and rerun affected reviews. Never relabel history.
3. Record changed reader decisions, evidence, counterexamples, authority,
   compatibility and adoption consequences in an issue and ADR. Complete the
   content audit before relying on mechanical checks.
4. Check every indexed public file and local Markdown link/heading target,
   including reference links and duplicate heading suffixes; do not let an
   untracked file satisfy a public link. Validate CFF 1.2 metadata, edition/date,
   license, Commons pin and all seven example structures. Inspect diagrams when
   their meaning or layout changes. Run a redacted secret scan of both tracked
   content and Git history. Scanner errors block completion; never publish raw
   sensitive findings. This repository has no build, runtime or dependencies.
5. Freeze a clean content commit before any current generated report is added.
   Assign the six lenses to two isolated reviewers under
   [review governance](reviews/README.md). Keep reports outside the candidate
   until final. Correct content through a new clean candidate and affected
   isolated reruns. Add only the seven allowlisted reports/disposition.
6. Freeze the final candidate. Confirm only those seven additions differ from
   the content candidate and that every report matches its approved source
   bytes. Recheck the whole public tree. Finalize an out-of-tree assembly
   attestation naming exact commits/trees, Commons tag object/commit/tree,
   allowlist, record digests, checks, findings and limits. It must state that
   future publication has not yet been verified. Its own digest stays detached.

Keep verification evidence outside the public tree, except the declared review
records. Record actual commands and results in the disposition; do not claim an
unrun check. The following commands support inventory and secret checks:

```sh
set -eu
git status --short
git branch --show-current
git remote -v
git diff --check
git ls-files
gitleaks git . --no-banner --redact --log-level error
```

Historical metadata may use semantic versions. Verify historical records under
their original contract; new editions must match a real UTC calendar date.
No parser, package or schema migration is needed in this repository.

## Freeze, merge and publish

Set these shell variables to the reviewed exact commits and an existing evidence
directory outside the checkout. The attestation file must already be finalized.
Use a new file for each candidate; never overwrite approved evidence. Replace
placeholders before running. The explicit repository prevents ambient selection
from publishing to another destination.

```sh
set -eu
repo=BradGroux/focus-operating-framework
content_commit=REPLACE_WITH_REVIEWED_CONTENT_COMMIT
final_commit=REPLACE_WITH_VERIFIED_FINAL_COMMIT
pr_number=REPLACE_WITH_REVIEWED_PR_NUMBER
evidence_dir=REPLACE_WITH_ABSOLUTE_OUTSIDE_EVIDENCE_DIRECTORY
attestation="$evidence_dir/assembly.md"

gh auth status --hostname github.com
test "$(gh api --hostname github.com user --jq .login)" = BradGroux
test -z "$(git status --porcelain)"
git diff --name-status "$content_commit" "$final_commit"
# Confirm the displayed diff is exactly the seven allowlisted additions.
# Required checks and conversations must be resolved. No admin bypass.
gh pr view "$pr_number" --repo "$repo" --json state,mergeable,statusCheckRollup
gh pr merge "$pr_number" --repo "$repo" --merge --match-head-commit "$final_commit"
git fetch origin main
git checkout --detach origin/main
test "$(git rev-parse HEAD^{tree})" = "$(git rev-parse "$final_commit^{tree}")"
test -z "$(git status --porcelain)"
# Rerun whole-tree checks on this clean merged target before continuing.
edition="$(cat VERSION)"
release_tag="v$edition"
test "${edition:0:10}" = "$(date -u +%Y.%m.%d)"
assembly_digest="$(shasum -a 256 "$attestation" | cut -d ' ' -f 1)"
export attestation evidence_dir release_tag
python3 - <<'PY'
import os
from pathlib import Path
notes = Path('project/releases') / (os.environ['release_tag'] + '.md')
assembly = Path(os.environ['attestation']).read_bytes()
assert assembly.endswith(b'\n')
body = notes.read_bytes() + b'\n<!-- focus-assembly-attestation -->\n' + assembly
Path(os.environ['evidence_dir'], 'release-body.md').write_bytes(body)
PY
# Use git tag -s instead if repository policy requires signing at publication.
git tag -a "$release_tag" -m "Focus Operating Framework $release_tag" \
  -m "Attestation-SHA256: $assembly_digest"
git push origin "refs/tags/$release_tag"
gh release create "$release_tag" --repo "$repo" --verify-tag \
  --title "Focus Operating Framework $release_tag" \
  --notes-file "$evidence_dir/release-body.md"
```

The annotated tag is immutable by policy. Never force, replace, delete or add
historical aliases. No release assets are required. The complete body contains
edition-facing notes followed by the delimiter and exact attestation bytes.
Only the attestation bytes are authenticated by `Attestation-SHA256`.

## Read back publication

Keep the variables from the prior block and compare authenticated public state:

```sh
gh api "repos/$repo/releases/tags/$release_tag" > "$evidence_dir/release.json"
git ls-remote origin "refs/tags/$release_tag" "refs/tags/$release_tag^{}"
export repo edition assembly_digest
python3 - <<'PY'
import datetime, hashlib, json, os, subprocess
from pathlib import Path
p = Path(os.environ['evidence_dir'])
tag = os.environ['release_tag']
def git(*args):
    return subprocess.check_output(['git', *args], text=True).strip()
release = json.loads((p / 'release.json').read_text())
assert release['author']['login'] == 'BradGroux'
assert release.get('performed_via_github_app') is None
assert release['tag_name'] == tag
assert release['name'] == 'Focus Operating Framework ' + tag
assert not release['draft'] and not release['prerelease']
assert release['assets'] == []
assert release['body'].encode() == (p / 'release-body.md').read_bytes()
assert release['published_at'][:10] == os.environ['edition'][:10].replace('.', '-')
assert git('cat-file', '-t', tag) == 'tag'
assert git('rev-parse', tag + '^{}') == git('rev-parse', 'HEAD')
remote = dict(line.split()[::-1] for line in git('ls-remote', 'origin',
              'refs/tags/' + tag, 'refs/tags/' + tag + '^{}').splitlines())
assert remote['refs/tags/' + tag] == git('rev-parse', tag)
assert remote['refs/tags/' + tag + '^{}'] == git('rev-parse', tag + '^{}')
assembly = release['body'].split('\n<!-- focus-assembly-attestation -->\n', 1)[1].encode()
assert assembly == Path(os.environ['attestation']).read_bytes()
digest = hashlib.sha256(assembly).hexdigest()
assert digest == os.environ['assembly_digest']
assert 'Attestation-SHA256: ' + digest in git('cat-file', '-p', tag)
print('Publication identity, body, date, tag and attestation verified')
PY
```

Also read back the merged commit through the repository API and compare its tree
with the final candidate. Check the tagged public inventory and review bytes,
local links, metadata, Commons identity and release URL. Close resolved issues
only after their acceptance criteria are verified; keep actual evidence gaps
open. No tag or release existing locally alone proves publication.

## Historical verification and corrections

For v1.0.0 and v1.1.0, compare the annotated local/remote object and peeled commit,
the tagged tree against the tree in the original public assembly attestation,
and SHA-256 of the exact original body against its tag message. Read back author,
final flags, assets and historical review digests. Do not require the new body
delimiter or calendar metadata on these releases. Their bodies contain the
attestation alone and are not committed edition-note files.

Historical v1.0.0 permits different public commit identities with identical
trees. Verify tree evidence without relabeling its recorded candidate commits.
Historical v1.1.0 uses August 22 metadata although publication occurred August 23
UTC; report that limit without changing the old body, citation or tag. A missing
historical candidate object limits object-level verification; a matching tree or
digest does not establish an unavailable object's history.

If a new release fails readback, report exactly what is mismatched and withhold
completion. Preserve published identity. Correct substantive content in a new
edition with a new annotated tag, reviews and clear supersession notes; never
rewrite a prior release to hide a failed check. If only publication completion
is interrupted, inspect the existing tag/release before retrying within the same
verified scope. Do not treat elapsed time as authority or move a tag after UTC
rollover.
