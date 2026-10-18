# AI Project Template — SDD Starter

Reusable, technology-neutral foundation for AI-assisted, spec-driven software development.

**Start here:** [Step-by-step guide to the five skills](docs/GETTING_STARTED.md).

## Create a new project
1. On GitHub click **Use this template** (the repository owner must enable the Template repository setting first).
2. Clone your new repository and open it in Claude Code.
3. Run `/initialize-project [brief project idea]`.
4. Review generated `docs/PRODUCT.md`, `docs/ROADMAP.md` and Draft SPEC-001.
5. Use `/review-spec SPEC-001`; approve and set Ready only when satisfied.
6. Run `/implement-spec SPEC-001`, validate, then `/close-spec SPEC-001`.

GitHub CLI alternative (once template status is enabled):
```bash
gh repo create OWNER/NEW_PROJECT --private --template thefakir/ai-project-template --clone
```

## Commands
`/initialize-project` · `/create-spec` · `/review-spec` · `/implement-spec` · `/close-spec`

## Source of truth
- `CLAUDE.md`: AI rules, authority order and approval gates
- `docs/PRODUCT.md`: validated problem, users, hypotheses and scope
- `docs/ROADMAP.md`: active work and nonbinding candidates
- `docs/ARCHITECTURE.md`: accepted/implemented technology only
- `docs/decisions/`: architecture decision records
- `docs/specs/`: bounded specifications and evidence-based outcomes
- `docs/design/SCREENS.md`: optional UI inventory
- `docs/GLOSSARY.md`: domain terminology
- `docs/METHODOLOGY.md`: how to apply the methodology
- `SDD_VERSION` and `CHANGELOG.md`: template baseline and changes

## Ground rules
This repository is a **template**, not a preselected application stack. Specs start Draft, architectural decisions require owner approval, and completion requires evidence. No feature implementation happens just because a roadmap proposes it.

A new repository created from this template is a **copy**, not a live-linked derivative. Later template improvements must be integrated through reviewed changes. Nothing updates older projects automatically.

## Existing projects
Do not overwrite their product-specific documentation or accepted decisions when adopting template improvements. Bring over process updates selectively.

## Status
Generic template ready for project-specific initialization. No application code is included.
