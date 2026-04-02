# Phase 004 - Implement Canonical Main Agent

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 004
> **Status:** Completed
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** n/a

---

## Objective

Create the first canonical runtime authority for the multi-hat system.

## Why this phase exists

The governance baseline already defines the one-main-agent target. This phase materializes that target as a self-sufficient canonical agent and support surface.

## Design Extraction

- Source requirement: the future system should converge to one canonical main agent file only inside `agents/`, with support/reference material under `skills/`
- Derived execution work: create `agents/multi-hat-system.md`, create `skills/multi-hat-system/`, and keep `prototype/` untouched
- Target outcome: one active runtime authority and one support/reference surface now exist for the system

## Flow Diagram

Governance baseline approved
  → create canonical main agent under `agents/`
  → create support/reference surface under `skills/`
  → write the active system as a self-sufficient canonical package
  → keep archive corpus untouched as archive/inspiration only
  → canonical runtime authority and support structure exist

## Reviewer Checklist

- [x] canonical main agent file created under `agents/`
- [x] support/reference surface created under `skills/`
- [x] advisory mode remains default
- [x] decision mode remains conditional
- [x] hats remain internal perspectives, not peer agents
- [x] `prototype/` remains untouched in this wave

## Verification

- `agents/multi-hat-system.md` created
- `skills/multi-hat-system/SKILL.md` and `skills/multi-hat-system/reference.md` created
- implementation aligned to `design/design.md`
- canonical file enriched with sharper mode behavior and compact high-value hat checkpoints
- no prototype files changed

## Exit Criteria

- one canonical main agent file exists under `agents/` and the support/reference surface exists under `skills/` without reintroducing peer-agent ambiguity
