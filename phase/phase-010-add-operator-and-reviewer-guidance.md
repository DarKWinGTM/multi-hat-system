# Phase 010 - Add operator and reviewer guidance

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 010
> **Status:** Implemented - Pending Review
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-010-operator-reviewer-guidance.patch.md](../patch/phase-010-operator-reviewer-guidance.patch.md)

---

## Objective

Add explicit steady-state operator and reviewer guidance so the package can be assessed in live usage without relying on prototype-only review mechanics.

## Why this phase exists

The active package already had strong runtime and handbook depth, but review and adoption decisions were still too implicit. The package needed a governed way to say how to evaluate live usage, what counts as a blocker vs follow-up, and when a prototype-derived idea can be promoted into the active package.

## Design Extraction

- Source requirement: the package should be maintainable from active surfaces alone
- Derived execution work: add explicit operator/reviewer expectations to the active governance model
- Target outcome: live-usage review and future adoption decisions become more legible and repeatable

## Flow Diagram

active package is materially complete
  → identify remaining steady-state review ambiguity
  → define operator/reviewer expectations
  → define blocker vs follow-up posture
  → define when prototype-derived ideas may be promoted
  → package maintenance becomes more deliberate and reviewable

## Reviewer Checklist

- [x] README or design now makes operator/reviewer expectations clearer
- [x] package governance no longer assumes prototype-only review mechanics for important future decisions
- [x] the patch layer captures the before/after guidance change explicitly
- [x] current TODO focus is now the live-usage review itself rather than a vague package re-understanding exercise

## Verification

- the active governance docs now define enough review posture for steady-state maintenance
- future adoption of prototype-derived ideas can be discussed with explicit disposition language
- the package has a clearer operator/reviewer model without creating a second runtime authority surface

## Exit Criteria

- operator and reviewer guidance is explicit enough for the current package state
- remaining review work is now about actual live-usage gaps, not missing governance vocabulary
