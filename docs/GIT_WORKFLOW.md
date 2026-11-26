# Git workflow — Git Flow with owner-approved pull requests

Nothing reaches `develop` or `main` without a pull request that the owner reviews and merges.

## Branches

| Branch | Created from | Merges into | Purpose |
|---|---|---|---|
| `main` (or `master`) | — | — | Released, owner-approved state. |
| `develop` | `main` | — | Integration branch; default PR target. |
| `feature/SPEC-XXX-<slug>` | `develop` | `develop` | One spec: Draft, implementation and Outcome. |
| `feature/<slug>` | `develop` | `develop` | Process, documentation or chores without a spec. |
| `release/<version>` | `develop` | `main` and `develop` | Promote a tested set of work (owner request only). |
| `hotfix/<slug>` | `main` | `main` and `develop` | Urgent fix to released state (owner request only). |

## Life of a spec

1. `git switch develop && git pull` then `git switch -c feature/SPEC-XXX-<slug>`.
2. `/create-spec` writes the Draft on that branch. The owner may review it in a draft PR or in conversation.
3. Owner approves; status Ready. `/implement-spec` commits on the same branch.
4. Checks pass and evidence is recorded; push the branch and open a PR to `develop` with the PR template.
5. After owner acceptance, `/close-spec` records Outcome and sets Done on the same branch, so the PR carries the closing documentation.
6. The owner reviews and merges. The merge is the final approval: until then the spec is awaiting merge, not finished.
7. Delete the feature branch only after the merge, and only if the owner wants it deleted.

## Commits

Conventional Commits with the spec reference when there is one:

```
docs(SPEC-005): draft interactive sky experiment
feat(SPEC-005): render gifter name as light-dot text
fix(SPEC-005): ignore intermediate streak events
chore: add pull request template
```

## Rules for AI agents

- Never commit directly to `main` or `develop`. Never merge. Never force-push a shared branch.
- Work on the active spec's feature branch; preserve unrelated changes in the working tree.
- Open the PR only when the change is verified; list every acceptance criterion as Verified, Not verified or Blocked.
- If the project's `CLAUDE.md` is stricter (for example, commit only after the owner tests), follow it.

## One-time repository setup

```bash
git switch -c develop   # from the up-to-date default branch
git push -u origin develop
gh repo edit --default-branch develop
```

Recommended on GitHub: protect `main` and `develop` (require a pull request before merging, block force-push and deletion). Branch protection or rulesets on private repositories may need a paid GitHub plan. GitHub does not let you approve your own PR, so when PRs are opened from the owner's account, requiring an approving review blocks merging; in that case require a PR but zero approvals, and the owner's merge is the approval.
