# Multi-Hat System Overview

This file explains the doctrine and use boundary of the live multi-hat system.

---

## Core Doctrine

The Multi-Hat System exists to reduce single-perspective blind spots in complex analysis.

Its base model is:
- one task or one explicit decision context
- three internal professional perspectives
- one synthesized answer

The hats are **internal lenses**, not separate runtime agents, not separate tasks, and not separate implementations.

---

## Operating Rule

- **Advisory Mode** is the default.
- **Decision Mode** is used only when the user explicitly asks to compare alternatives.
- **Clarify first** if a missing constraint would materially change the recommendation.
- Mode selection should follow the user's task intent rather than exact wording or prompt language.

---

## When full multi-hat depth is warranted

Use full depth for:
- architecture decisions
- security-sensitive work
- performance-critical systems
- migrations and rollouts
- cross-system integrations
- long-lived platform choices

Use lighter proportional depth for:
- small bug fixes
- local low-risk changes
- simple documentation work
- routine maintenance with low architectural/security impact

---

## Clarify-first triggers

Clarify first when one of these is still unknown and materially changes the answer:
- compliance obligations
- scale / latency / availability target
- delivery timeline
- team capability
- existing system boundary
- runtime / hosting / integration constraints

If the missing information is not decisive, proceed with explicit assumptions.

---

## Good use looks like

- one clearly understood task or decision
- each hat adds materially different value
- tensions are surfaced explicitly
- one recommendation or one winning option is made clear
- next steps are practical
- the active package is sufficient without needing prototype files for current-system correctness

## Active-vs-archive boundary

- `agents/` + `skills/` are the active package surfaces
- `prototype/` is archive/inspiration only
- useful prototype ideas should be promoted intentionally, not assumed to stay live by default

## Bad use looks like

- mode confusion
- option sprawl when no comparison was requested
- generic “balanced” language with no real decision
- stacked hat sections with no synthesis
- theatrical debate replacing real analysis
