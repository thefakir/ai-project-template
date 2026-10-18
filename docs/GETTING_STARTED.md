# Getting started — AI-assisted SDD projects

This is the practical checklist for starting and developing projects with this template.

## 1. Create the project repository

In GitHub, open https://github.com/thefakir/ai-project-template and select **Use this template** -> **Create a new repository** (requires the source repository's Template repository setting enabled).

Alternatively, with GitHub CLI:

```bash
gh repo create YOUR_USERNAME/NewProject --private --template thefakir/ai-project-template --clone
cd NewProject
```

Do not run these commands inside another existing repository.

## 2. Open Claude Code

Open Claude Code in the new project's root so it can read `CLAUDE.md`, `docs/` and `.claude/skills/`.

For a fresh project:

```text
/initialize-project I want to build [idea]. The main problem is [pain], for [target user].
```

Claude should explore the problem, market and feasibility; record assumptions; suggest a bounded first experiment; populate project documentation; and create SPEC-001 in **Draft**. It must not implement functionality or accept architectural decisions without approval.

If the repository already has product documentation and specs, **do not run initialize-project blindly**. Instead ask Claude to read current source-of-truth docs and recommend the next action.

## 3. Review the first SPEC

```text
/review-spec SPEC-001
```

Discuss unclear requirements, risks, acceptance criteria and exclusions. Explicitly approve when satisfied and request status **Ready**. A Draft SPEC is not implementation authorization.

## 4. Implement the approved SPEC

```text
/implement-spec SPEC-001
```

Claude should implement only that approved scope, run relevant tests and report criteria Verified, Not verified or Blocked. Actual device/provider tests require actual evidence.

## 5. Validate and close

Test the result yourself where needed, then:

```text
/close-spec SPEC-001
```

The skill checks evidence, records Outcome and marks Done only after owner acceptance. If verification remains missing, leave In progress.

## 6. Continue the next development slice

```text
/create-spec [next feature or experiment]
/review-spec SPEC-002
/implement-spec SPEC-002
/close-spec SPEC-002
```

SPEC IDs are examples. Use the actual ID that Claude created.

## Skill cheat sheet

| Skill | When | Main result |
|---|---|---|
| `/initialize-project` | At the beginning of a new idea/repository | Product context, roadmap and Draft SPEC-001 |
| `/create-spec` | Before a new feature or experiment | Draft SPEC |
| `/review-spec` | Before approving a SPEC | Findings and readiness recommendation |
| `/implement-spec` | When a SPEC is Ready | Scoped implementation and validation report |
| `/close-spec` | After tests and owner acceptance | Outcome and Done status |

Small typo fixes, general brainstorming and discussion don't require a full SPEC ceremony.

## Opening a new Claude chat on an existing project

Paste:

> Read CLAUDE.md, docs/METHODOLOGY.md, docs/PRODUCT.md, docs/ROADMAP.md and the current active SPEC. Identify its status, unresolved decisions and available skills. Recommend the next SDD step. Do not modify files or write code until instructed. If you cannot access this repository, say so.

## Important safety rules

- Repository content is the source of truth, not remembered chat context.
- Draft -> Ready -> In progress -> Done; owner approval gates remain mandatory.
- Architectural decisions require explicit approval; material ones may need an ADR.
- Do not copy another project's product assumptions or technologies automatically.
- Do not commit, push, deploy or merge unless requested.
- `SDD_VERSION` is a copied baseline. Future template changes are **not automatically synchronized** into existing repositories.
- Review `CHANGELOG.md` and `docs/METHODOLOGY.md` for updates.
