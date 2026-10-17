---
name: implement-spec
description: Implement one owner-approved SPEC with scope and verification discipline.
argument-hint: "SPEC-XXX"
disable-model-invocation: true
---
# Implement approved SPEC
Resolve exactly one spec in docs/specs and read CLAUDE.md plus relevant context.
Require Ready or In progress. If Draft, stop for approval.
Inspect working tree, existing implementation and tests. Preserve unrelated changes.
Plan meaningful work against acceptance criteria. Flag consequential architecture decisions for owner approval.
Implement smallest approved scope, adding focused tests for edge and failure cases.
Run applicable checks, inspect diff and check secrets. For every criterion report Verified, Not verified or Blocked with evidence.
Never claim live third-party verification without performing it. Do not mark Done until human-only verification is accepted.
No deployment, destructive change, commit, push, PR or merge unless expressly instructed.
