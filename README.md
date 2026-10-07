# [Project Name]

[One sentence: what this project is.]

## Current status

[One or two lines. Keep it current.]

## Source of truth

The repository is the source of truth for product, architecture, specs, and implementation decisions.

- `docs/PRODUCT.md`: problem, hypotheses, users, scope, principles, open questions
- `docs/ARCHITECTURE.md`: current and explicitly accepted technical truth
- `docs/ROADMAP.md`: active work plus likely next and later candidates
- `docs/decisions/`: accepted architecture decision records (ADRs)
- `docs/specs/`: bounded specs, each with acceptance criteria
- `docs/design/SCREENS.md`: designed screens, flows, and role visibility
- `docs/GLOSSARY.md`: domain terms and open naming decisions
- `CLAUDE.md`: rules for AI-assisted development in this repository

Design workspace: [link to the design file, if any]

Chat conversations are useful for discovery, challenge, and review. Decisions that affect implementation must be reflected in the repository before they become authoritative.

## Using this template for a new project

1. Create a new repository from this template, or copy its files into an empty repository.
2. Search for `[` in all files and fill in every placeholder. Delete sections that do not apply.
3. In `CLAUDE.md`, set the language policy and, once a project exists, the commands.
4. Write `docs/PRODUCT.md` first: problem, target user, and hypotheses. Mark everything unvalidated as a hypothesis.
5. Add a design link and fill `docs/design/SCREENS.md` only if the project has a UI. Otherwise delete it and its references.
6. Write the first spec from `docs/specs/_TEMPLATE.md` and set it as the active work in `docs/ROADMAP.md`.
7. Record architecture choices as ADRs only after a human has accepted them.

## How the documents relate

When sources conflict, the authority order in `CLAUDE.md` decides. In short: the current instruction from the human, then the active spec, then accepted ADRs and architecture, then product documentation, then the roadmap, then the existing implementation.

Each document has one job. Do not turn any of them into a project diary.
