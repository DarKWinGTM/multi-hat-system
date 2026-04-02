# Phase 008 - Establish patch model and artifact taxonomy

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 008
> **Status:** Implemented - Pending Review
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-008-patch-model-and-artifact-taxonomy.patch.md](../patch/phase-008-patch-model-and-artifact-taxonomy.patch.md)

---

## Objective

Add a governed patch layer and formal artifact taxonomy so steady-state package changes are reviewable as explicit deltas rather than only narrative history.

## Why this phase exists

The package already had strong design, changelog, TODO, and phase structure, but it still lacked an explicit patch/evidence surface. That made large governance deltas harder to review after the fact.

## Design Extraction

- Source requirement: the package should distinguish runtime, support, governance, archive, and patch roles explicitly
- Derived execution work: add `patch/`, define artifact taxonomy in design/README, and wire phase-to-patch linkage into the new hardening wave
- Target outcome: the package becomes easier to audit through before/after artifacts

## Flow Diagram

no explicit patch layer exists
  → define artifact taxonomy
  → create `patch/`
  → add first governance-hardening patch artifact
  → update README / design / summary to recognize patch role
  → package deltas become explicitly reviewable

## Reviewer Checklist

- [x] `patch/` exists as a governed surface
- [x] design defines explicit artifact taxonomy
- [x] README describes patch as part of the active governance model
- [x] the phase links its patch artifact explicitly
- [x] changelog is not misused as the only place to understand the delta

## Verification

- `patch/` exists
- the package defines artifact roles clearly enough to separate runtime authority, operator bridge, handbook, governance, archive, and patch evidence
- the current hardening wave links phase and patch explicitly

## Exit Criteria

- governed patch baseline exists
- package artifact taxonomy is explicit
- future governance deltas no longer need to be reconstructed only from changelog prose
