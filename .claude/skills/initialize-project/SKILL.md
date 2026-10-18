---
name: initialize-project
description: Explore and validate a new software product idea, then initialize the repository's SDD source of truth and one draft experiment.
argument-hint: "[project idea]"
disable-model-invocation: true
---

# Initialize project — discovery before implementation

Read `CLAUDE.md`, `README.md`, `docs/METHODOLOGY.md` and relevant templates. Inspect repository state first. If the project has already been initialized, do not overwrite established facts or existing SPECs: propose focused amendments instead.

## Phase 1 — Understand the idea
From the owner's description identify:
- Who faces the problem and in which real-world workflow.
- Current workaround and its friction, frequency and consequences.
- Customer, user, buyer and operator (these may be different people).
- Proposed value, earliest realistic audience and assumptions.
- What success would look like and what is not yet known.

Ask a few high-leverage questions only when missing answers materially affect the initial direction. Prefer an iterative conversation over a long questionnaire. Never invent validation evidence.

## Phase 2 — Lightweight business validation
Before defining a build plan, assess three dimensions with clear separation of **known facts**, **hypotheses** and **unknowns**:
1. **Problem:** Is the pain recurring, material and observable? What evidence would validate it?
2. **Market:** Who might pay, what alternatives/workarounds exist, and what evidence of willingness to pay is available?
3. **Feasibility:** What technical, platform, legal, operational or adoption dependency is most likely to block the idea?

Use available research tools when current outside facts are important; cite sources and verify time-sensitive claims. Do not treat market guesses or search results as customer interviews.

## Phase 3 — Choose the smallest next validation
Recommend the highest-risk assumption to test first. Prefer a short interview, operational trial, manual prototype or technical proof of concept over a full MVP when that yields faster evidence.
Describe an independently checkable outcome and success/failure criteria. If the owner prefers a different first slice, record that decision and the trade-off.

## Phase 4 — Initialize project documents
After enough discovery to define the first experiment:
1. Adapt `README.md` and `docs/PRODUCT.md`, including problem, first customer, workflow, MVP hypothesis, validation evidence and out-of-scope features.
2. Update `docs/ROADMAP.md` with the initial experiment and clearly labeled noncommittal candidates.
3. Update `docs/ARCHITECTURE.md` with only implemented or expressly owner-approved technology; leave unresolved choices open.
4. Tailor `CLAUDE.md` with known project language, user locale, design links and actual build/test commands without guessing.
5. Create one bounded `docs/specs/SPEC-001-<slug>.md` from the template, status **Draft**, with acceptance criteria, exclusions, open questions and evidence expected.
6. Preserve reusable template files, skills, `SDD_VERSION` and changelog. Do not copy product-specific decisions from another project.

## Handoff
Summarize the hypothesis, greatest risk, first proposed experiment, files changed and decisions still requiring owner review. The owner must explicitly approve promotion to Ready. Do not implement application code, accept ADRs, change unrelated files, commit or push without an explicit request.

## Guardrails
- Keep discovery proportional: no elaborate market study unless needed.
- Do not assume every idea is a viable business.
- Do not silently substitute your own business strategy or technology choice.
- When essential facts are unavailable, label assumptions and proceed only as far as evidence permits.
