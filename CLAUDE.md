# AI-assisted development rules

This repository is the source of truth, not previous conversations.

## Authority
Resolve conflicts in this order: current explicit owner instruction; active SPEC; accepted ADRs; accepted/current architecture; product; roadmap; implementation; prior chat. Surface material contradictions.

## Working method
Read the active SPEC and only relevant context for the requested work. For meaningful changes inspect the code, consider failure cases, create a proportionate plan, implement approved scope, run relevant tests and review the diff.

## Human approval
Do not promote a Draft SPEC to Ready without explicit owner approval. Do not silently accept significant architecture decisions or ADRs. Roadmap candidates are not commitments. If there is no approved active SPEC, pursue discovery and drafting rather than feature implementation.

## SPEC lifecycle
Draft -> Ready -> In progress -> Done (or Superseded). Use `docs/specs/_TEMPLATE.md`. Before Done record Outcome with verification evidence, limitations and owner acceptance. Manual-only tests must not be reported as passed without execution.

## Skills
- `/initialize-project` — turn an idea into project documents and Draft SPEC-001.
- `/create-spec` — draft another bounded spec.
- `/review-spec` — assess readiness.
- `/implement-spec` — implement one approved spec.
- `/close-spec` — verify outcome and complete after owner acceptance.

Read `docs/METHODOLOGY.md` for lifecycle and reuse guidance.

## Guardrails
Choose simple solutions. Avoid speculative abstractions, dependencies and infrastructure. Do not change unrelated code. Never commit secrets or user data. Do not deploy, commit, push, merge or open PRs without explicit instruction. Confirm external provider behavior before claiming real-world integration success.

## Document ownership
PRODUCT: people/problem/scope/evidence. ROADMAP: prioritized possibilities. ARCHITECTURE: implemented or explicitly accepted technical truth. ADR: accepted significant decisions and rationale. SPEC: bounded behavior, validation and outcome. SCREENS: UI exploration and role visibility. GLOSSARY: terms.

## Project-specific settings
During `/initialize-project`, set development language, end-user language/locale, design link (if any), and actual build/test commands when known. Do not invent them. Keep optional docs only if useful.

## Definition of done
Every criterion verified with evidence; relevant validation passed; diff reviewed; meaningful limitations reported; documentation reflects approved changes.
