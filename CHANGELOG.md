# Changelog

## 1.3.0 — 2026-11-26
- Each spec now travels in two PRs to `develop`: `feature/SPEC-XXX-spec` (the document, merged once the owner approves it as Ready) and `feature/SPEC-XXX-impl` (the implementation, created from the updated `develop`).
- `/implement-spec` updates `develop` first and refuses specs that are not Ready there; `/close-spec` closes on the implementation branch or on `feature/SPEC-XXX-close`.

## 1.2.0 — 2026-11-25
- Added Git Flow workflow with owner-approved pull requests (`docs/GIT_WORKFLOW.md`).
- Added `.github/pull_request_template.md` mapping PRs to spec acceptance criteria.
- `/create-spec`, `/implement-spec` and `/close-spec` now work on `feature/SPEC-XXX-<slug>` branches and target `develop`; agents never merge or commit to `main`/`develop`.
- A spec is Done only after its PR is merged by the owner.

## 1.1.0 — 2026-10-17
- Expanded `/initialize-project` with lightweight problem, market and feasibility validation.
- Added explicit separation of evidence, hypotheses and unknowns.
- Prioritize testing the riskiest assumption before committing to a full MVP.
- Preserve proportional discovery, owner approval and Draft SPEC gating.

## 1.0.0 — 2026-10-17
- Generalized reusable SDD workflow based on lessons from Easy TJournal and LiveSalesAutomation.
- Added initialize, create, review, implement and close SPEC skills.
- Added template version tracking and methodology documentation.
- Preserved product, architecture, design, glossary and ADR scaffolding.
