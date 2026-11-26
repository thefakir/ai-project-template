---
name: close-spec
description: Close a spec only after verifying evidence and obtaining owner acceptance.
argument-hint: "SPEC-XXX"
disable-model-invocation: true
---
# Close SPEC
Read CLAUDE.md, target SPEC and validation evidence.
Evaluate every acceptance criterion and note actual test results, unresolved limitations and manual checks.
If any required criterion remains unverified, leave it In progress and explain the blocker.
After explicit owner acceptance, fill Outcome with evidence and move to Done. Update roadmap and factual documentation as necessary.
Record Outcome and Done on the spec's feature branch so they travel in its PR to `develop`; report the spec as awaiting merge until the owner merges it (if it was already merged, use a follow-up feature branch and PR). Do not make ADR decisions, merge, or commit to `main`/`develop`.
