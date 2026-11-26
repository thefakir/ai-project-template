# Git workflow — Git Flow with owner-approved pull requests

Nothing reaches `develop` or `main` without a pull request that the owner reviews and merges.

## Branches

| Branch | Created from | Merges into | Purpose |
|---|---|---|---|
| `main` (or `master`) | — | — | Released, owner-approved state. |
| `develop` | `main` | — | Integration branch; default PR target. |
| `feature/SPEC-XXX-spec` | `develop` | `develop` | The spec document only: Draft until the owner approves it, merged once Ready. |
| `feature/SPEC-XXX-impl` | `develop` | `develop` | Implementation of a Ready spec, its evidence and Outcome. |
| `feature/<slug>` | `develop` | `develop` | Process, documentation or chores without a spec. |
| `release/<version>` | `develop` | `main` and `develop` | Promote a tested set of work (owner request only). |
| `hotfix/<slug>` | `main` | `main` and `develop` | Urgent fix to released state (owner request only). |

## Life of a spec

A spec travels in two pull requests: first the document, then the implementation.

**Spec PR**
1. From an up-to-date `develop`, create `feature/SPEC-XXX-spec`. The Draft is written there (with `/create-spec` or drafted in conversation with the owner, sketches included).
2. Open the PR to `develop` (it can stay a draft PR while questions are open).
3. The owner approves the spec explicitly; its status changes to Ready on the same branch.
4. The owner merges. From now on the Ready spec is in `develop`.

**Implementation PR**
5. The agent updates `develop` (`git switch develop && git pull`) and receives the spec number from the owner (`/implement-spec SPEC-XXX`). It verifies the spec is Ready in `develop`; a Draft, or a spec that only exists on an unmerged branch, is not implemented.
6. It creates `feature/SPEC-XXX-impl` from `develop`, sets the status to In progress and implements.
7. When verified, it pushes the branch and opens a PR to `develop` with the PR template. After owner acceptance, `/close-spec` records Outcome and Done on that branch.
8. The owner reviews and merges. Until then the spec is awaiting merge, not finished. If the implementation was merged with manual checks still pending, they are closed later on `feature/SPEC-XXX-close`.
9. Delete branches only after their merge, and only if the owner wants them deleted.

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
