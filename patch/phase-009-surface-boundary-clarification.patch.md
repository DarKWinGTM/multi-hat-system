# Phase 009 Surface Boundary Clarification Patch

## 0) Document Control

> **Current Version:** 1.0
> **Status:** Implemented
> **Target Design:** [../design/design.md](../design/design.md) v1.4
> **Target Phase:** [../phase/phase-009-clarify-surface-boundaries.md](../phase/phase-009-clarify-surface-boundaries.md)
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Full history:** [../changelog/changelog.md](../changelog/changelog.md)

---

## 1) Context

This patch captures the clarification of active package surfaces versus archive/prototype surfaces.

Why this change mattered:
- prototype was already described as archive/inspiration only
- but maintainers still lacked a governed disposition model for prototype ideas
- the package needed explicit language for what was migrated, deferred, or intentionally left out

---

## 2) Analysis

Risk level: Low

Dependencies:
- `../design/design.md`
- `../README.md`
- `../phase/phase-009-clarify-surface-boundaries.md`

Review concern:
- the new boundary language should reduce ambiguity without making prototype unusable as historical context

---

## 3) Change Items

### Change Item 1
- **Target location:** prototype boundary model
- **Change type:** replacement

**Before**
```text
prototype/ was described broadly as archive/inspiration only.
```

**After**
```text
prototype/ is still archive/inspiration only, but the package now uses explicit disposition categories:
- migrated
- deferred
- intentionally not migrated
```

### Change Item 2
- **Target location:** maintainer interpretation of archive material
- **Change type:** additive

**Before**
```text
The package did not clearly explain how a maintainer should reason about prototype ideas after active-package completion.
```

**After**
```text
Prototype remains useful as historical inspiration, but active package surfaces alone remain current-system authority.
```

---

## 4) Verification

- [ ] Confirm design defines the disposition categories explicitly
- [ ] Confirm README reflects the same active-vs-archive language
- [ ] Confirm this patch keeps prototype available as inspiration without restoring active dependency status

---

## 5) Rollback Approach

If this patch introduces too much category language:
- keep the active-vs-archive distinction explicit
- collapse wording only if necessary
- avoid returning to ambiguous archive semantics
