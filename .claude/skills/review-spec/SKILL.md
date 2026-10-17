---
name: review-spec
description: Check a draft specification's completeness, feasibility and testability.
argument-hint: "SPEC-XXX"
disable-model-invocation: true
---
# Review specification
Find the exact SPEC and read applicable source-of-truth documents.
Check bounded goal, testable criteria, error cases, data rules, scope, dependencies and accepted architecture constraints.
Highlight uncertainty around privacy, cost, provider API and concurrency when applicable. Recommend Ready or Not Ready with specific blockers.
The owner alone approves promotion to Ready. Do not self-approve, implement, commit or push.
