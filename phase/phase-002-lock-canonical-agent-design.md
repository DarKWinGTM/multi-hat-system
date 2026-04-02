# Phase 002 - Lock Canonical Agent Design

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 002
> **Status:** Completed
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** n/a

---

## Objective

Lock the one-main-agent model and the active package boundaries.

## Why this phase exists

The package needs a stable authority model before implementation so the runtime and support surfaces do not drift.

## Design Extraction

- Source requirement: the future system should converge to one canonical main agent file only
- Derived execution work: define the future runtime target, advisory-vs-decision mode model, and file-role classification map
- Target outcome: implementation later can proceed without ambiguity about what belongs in the canonical file

## Flow Diagram

Governance scaffold exists
  → define one future canonical main agent
  → define advisory vs decision as modes
  → classify archive files as inspiration/reference only
  → migration target becomes explicit

## Reviewer Checklist

- [x] one future canonical runtime file is defined
- [x] advisory mode is explicitly default
- [x] decision mode is explicitly conditional
- [x] hats are explicitly internal perspectives, not peer agents
- [x] active package boundaries are defined

## Verification

- future canonical target path defined
- active support/reference boundary defined
- one-main-agent authority model documented

## Exit Criteria

- the future one-main-agent structure is explicit and reviewable
