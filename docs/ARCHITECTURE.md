# Architecture

## Purpose

This document describes the architecture that is currently implemented or explicitly accepted.

It should not become a wishlist of technologies we may use later.

Historical reasoning for significant accepted decisions belongs in `docs/decisions/`.

## Architecture goals

1. Keep early experiments small and understandable.
2. Avoid premature infrastructure and abstraction.
3. Make decisions when requirements create a real need for them.
4. Preserve the ability to evolve without pretending future architecture is already known.

[Add or replace goals that are specific to this project.]

## Current architecture

No production architecture exists yet.

[When something is implemented or accepted, describe it here in plain terms.]

## Accepted decisions

[One entry per accepted decision, linking to its ADR. Example:]

### [Decision area]

[What was decided, in one line.]

See: `docs/decisions/ADR-001-[slug].md`

## Not yet decided

The following are plausible future choices but are not architecture commitments:

- [Area, for example: backend, database, authentication, deployment.]

Technologies that were only discussed must not be treated as approved architecture until the relevant work requires a decision.

## Decision rule

A technology or architectural pattern becomes authoritative only when:

1. A concrete requirement or active spec creates the need.
2. Relevant alternatives have been considered at an appropriate depth.
3. A human explicitly accepts the decision.
4. Significant decisions are captured in an ADR when useful.

Do not introduce infrastructure simply to prepare for hypothetical scale.
