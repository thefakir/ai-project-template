# Spec-driven development methodology

This repository is a reusable development-process template, not an application architecture.

## Lifecycle
Idea -> discovery -> Draft SPEC -> owner review -> Ready -> implement -> verify -> owner acceptance -> Done.

## New project
Create a repository using GitHub's template feature, then run `/initialize-project [idea]` in Claude Code.
Review product documentation and the first Draft SPEC before implementing.

## Skills
- `/initialize-project`: bootstrap source of truth from an idea.
- `/create-spec`: define one bounded spec.
- `/review-spec`: assess readiness without self-approval.
- `/implement-spec`: execute one approved spec.
- `/close-spec`: confirm evidence and close after human acceptance.

## Authority and architecture
Use the hierarchy in CLAUDE.md. An active spec limits implementation scope. An ADR only becomes Accepted with explicit owner approval. Roadmap ideas are not commitments.

## Repeatability
`SDD_VERSION` records the baseline copied into each project. A GitHub template is a snapshot; it does not update older projects automatically. Future improvements should be versioned here and propagated via reviewed changes, not automatic overwrites.

## Safety
Never commit secrets, personal data or test customer images. Do not assume external-service claims are verified without testing.
