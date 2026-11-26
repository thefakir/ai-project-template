---
name: create-spec
description: Draft a bounded specification or experiment with testable acceptance criteria.
argument-hint: "[feature or experiment]"
disable-model-invocation: true
---
# Create specification
Read CLAUDE.md and relevant product, roadmap, architecture and accepted ADRs. Pick the next unused SPEC ID.
Use docs/specs/_TEMPLATE.md. Write the Draft on a new `feature/SPEC-XXX-<slug>` branch from `develop` (docs/GIT_WORKFLOW.md). Set status Draft. Document goal, observable behavior, data/rules, failure cases, tests, exclusions, constraints and open decisions.
Do not invent provider capabilities or pre-approve technologies. Report risks and questions before status Ready. No implementation; no commit, push or PR without explicit instruction, and never to `main`/`develop`.
