---
name: initialize-project
description: Initialize a new product project using the SDD template, with no invented commitments.
argument-hint: "[project idea]"
disable-model-invocation: true
---
# Initialize project
Read CLAUDE.md, README.md and relevant docs templates. Check whether the repo is already initialized; never overwrite existing project facts.
Gather the problem, first users, existing workflow, hypothesis, success signal and first key uncertainty. Ask about essential ambiguities; mark unknowns as open.
Tailor README.md, docs/PRODUCT.md, docs/ROADMAP.md, docs/ARCHITECTURE.md and the language/commands sections in CLAUDE.md. Keep technology undecided unless approved.
Create one small Draft SPEC-001 from the template with verifiable criteria, exclusions and evidence requirements.
Summarize decisions that need owner review. Do not self-approve SPECs/ADRs, implement, commit or push without explicit instruction.
