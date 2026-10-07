# CLAUDE.md

## Purpose

This repository is developed with AI assistance, but the repository remains the source of truth.

The goal is disciplined AI-assisted software engineering, not unrestricted vibe coding.

## Required context

Before proposing or implementing meaningful changes:

1. Read `docs/ROADMAP.md` to identify the active work.
2. Read the active spec under `docs/specs/`.
3. Read `docs/PRODUCT.md` when product intent or scope matters.
4. Read `docs/ARCHITECTURE.md` when technical structure or technology choices matter.
5. Read relevant ADRs under `docs/decisions/`.

Do not assume every document must be read in full for every tiny change. Read the context relevant to the work.

## Authority order

When sources conflict, use this order:

1. Explicit current user instruction.
2. Active spec.
3. Accepted ADRs and current architecture documentation.
4. Product documentation.
5. Roadmap.
6. Existing implementation.
7. Chat history or assumptions.

Call out meaningful conflicts instead of silently choosing a direction.

If a user instruction changes the scope of the active spec, propose the spec update instead of silently deviating from it.

## Core rules

1. Do not implement features outside the active spec.
2. Prefer the simplest solution that satisfies the acceptance criteria.
3. Do not introduce a dependency without a concrete current need.
4. Do not silently change product scope.
5. Do not treat planned or discussed technologies as approved architecture.
6. Keep changes focused; avoid unrelated refactors during feature work.
7. Do not add abstractions solely for hypothetical future scale.
8. Run relevant build, lint, tests, or manual validation before declaring work complete.
9. Review the final diff for accidental or unrelated changes.
10. Do not commit or push unless explicitly requested.

## Architecture decision rule

AI may identify architectural concerns and recommend decisions.

AI must not make a significant architecture choice authoritative merely by:

- implementing it,
- editing `docs/ARCHITECTURE.md`,
- or creating an ADR that marks its own choice as accepted.

When a significant architecture decision is required:

1. Explain the decision that is needed.
2. Present relevant trade-offs or alternatives.
3. Obtain explicit human acceptance when the choice materially affects architecture.
4. Then document the accepted decision when appropriate.

Routine implementation choices that do not materially affect architecture do not require an ADR.

## Standard workflow

For each feature or experiment:

1. Identify the active spec from `docs/ROADMAP.md`.
2. Read the active spec and relevant context.
3. Inspect the existing code that is relevant.
4. Identify ambiguities, missing information, or conflicts.
5. For significant work, produce an implementation plan before modifying code.
6. Implement only the active scope.
7. Run relevant validation.
8. Review the diff.
9. Report:
   - What changed.
   - Which acceptance criteria are satisfied.
   - Validation performed.
   - Any remaining risks, limitations, or follow-up candidates.

## Ambiguity rule

Do not invent product behavior or architecture to fill an important gap.

If an ambiguity materially changes scope, behavior, data design, security, architecture, or user experience, surface it before implementation when practical.

For small implementation details that do not materially change the agreed behavior, use reasonable engineering judgment.

## Documentation responsibilities

Use documentation by responsibility:

- `PRODUCT.md`: problem, hypotheses, users, scope, principles, open questions.
- `ARCHITECTURE.md`: current and explicitly accepted technical truth.
- ADRs: significant accepted architecture decisions and their reasoning.
- Specs: one bounded piece of behavior or work and its acceptance criteria.
- `ROADMAP.md`: active work plus likely next and later candidates.
- `GLOSSARY.md`: domain terms and open naming decisions.
- `CLAUDE.md`: how AI should work in this repository.

Do not turn any single document into a project diary.

## Documentation change rule

Implementation may reveal that documentation is outdated or incomplete.

Do not silently rewrite product or architecture truth to match an implementation choice.

Instead:

- update routine factual documentation when the change is already within approved scope;
- surface product-scope changes for human decision;
- surface significant architecture changes for human decision;
- create or update ADRs only after the underlying decision is accepted.

## Design source

[Delete this section if the project has no UI.]

[Design tool] is the visual design workspace (link in `README.md`). `docs/design/SCREENS.md` maps screens to flows and roles.

- When implementing UI, read the relevant design screens and `docs/design/SCREENS.md`.
- Screens marked Draft are exploration, not approved requirements.
- The design defines how something looks. The active spec defines behavior and acceptance criteria. If they conflict, call it out.

## Language

[Fill in for each project. Example:]

- Everything related to development is in [language]: code, identifiers, comments, documentation, specs, ADRs, and commit messages.
- Everything users see in the product is in [language and locale]: screen text, labels, messages, and errors.
- [Regional formats that matter: currency, dates, numbers.]

## Spec lifecycle

Spec status moves through: Draft, Ready, In progress, Done, Superseded.

Before marking a spec Done, fill its Outcome section: criteria verified, limitations discovered, and follow-up candidates.

Use `docs/specs/_TEMPLATE.md` for new specs and `docs/decisions/_TEMPLATE.md` for new ADRs.

## Commands

Build, lint, test, and run commands are not defined yet. Add them here when the first project exists, and keep them current.

## Definition of done

A change is done only when:

- Active spec acceptance criteria are met.
- Relevant validation has passed.
- The final diff contains no unrelated changes.
- Important discovered limitations are reported.
- Documentation reflects approved changes when needed.
