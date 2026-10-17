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
Do not make ADR decisions or commit/push without explicit instruction.
