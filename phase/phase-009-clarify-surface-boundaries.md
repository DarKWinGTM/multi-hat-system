# Phase 009 - Clarify surface boundaries

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 009
> **Status:** Implemented - Pending Review
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-009-surface-boundary-clarification.patch.md](../patch/phase-009-surface-boundary-clarification.patch.md)

---

## Objective

Clarify the difference between the active package surfaces and the archive/prototype surface, and formalize prototype disposition rules.

## Why this phase exists

The package already described `prototype/` as archive/inspiration only, but it still lacked a governed disposition model that said which ideas were migrated, deferred, or intentionally not migrated. That left avoidable ambiguity for maintainers.

## Design Extraction

- Source requirement: active package surfaces should be self-sufficient and archive should not compete for authority
- Derived execution work: define prototype disposition categories and update README/design/TODO/phase/changelog wording accordingly
- Target outcome: active vs archive boundaries become explicit enough for steady-state maintenance

## Flow Diagram

active package is self-sufficient
  → clarify prototype is archive only
  → add migrated / deferred / intentionally-not-migrated categories
  → update governance surfaces to use the same language
  → archive remains useful without competing for authority

## Reviewer Checklist

- [x] active package surfaces remain the only current-system authority
- [x] prototype disposition categories are explicit
- [x] README and design use the same active-vs-archive language
- [x] changelog and TODO no longer leave the boundary implicit

## Verification

- design defines prototype disposition categories explicitly
- README explains prototype as archive/inspiration with governed disposition semantics
- the package can still be understood without consulting prototype for current-system correctness

## Exit Criteria

- archive boundary is clearer
- maintainers can reason about prototype ideas without mistaking them for active authority
