# Phase 008 Patch Model and Artifact Taxonomy Patch

## 0) Document Control

> **Current Version:** 1.0
> **Status:** Implemented
> **Target Design:** [../design/design.md](../design/design.md) v1.4
> **Target Phase:** [../phase/phase-008-establish-patch-model-and-artifact-taxonomy.md](../phase/phase-008-establish-patch-model-and-artifact-taxonomy.md)
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Full history:** [../changelog/changelog.md](../changelog/changelog.md)

---

## 1) Context

This patch captures the package transition from governance-without-patch-evidence to governance-with-an-explicit patch baseline.

Target artifacts:
- `../design/design.md`
- `../README.md`
- `../phase/SUMMARY.md`
- `../TODO.md`

Why this change mattered:
- the package already had strong governance structure
- but a reviewer still had to reconstruct large deltas from changelog prose alone
- the package needed an explicit before/after evidence layer

---

## 2) Analysis

Risk level: Low

Dependencies:
- `../design/design.md`
- `../phase/phase-008-establish-patch-model-and-artifact-taxonomy.md`
- `../changelog/changelog.md`

Review concern:
- patch should clarify the package model without collapsing phase/changelog/TODO roles together

---

## 3) Change Items

### Change Item 1
- **Target location:** package artifact taxonomy
- **Change type:** additive

**Before**
```text
The package described runtime authority, support/reference, governance, and archive, but did not define a governed patch surface.
```

**After**
```text
The package now defines:
- agents/ = runtime authority
- skills/ = operator bridge + modular handbook
- design/changelog/TODO/phase = governance surfaces
- patch/ = governed before/after evidence surface
- prototype/ = archive/inspiration only
```

### Change Item 2
- **Target location:** phase-to-patch linkage model
- **Change type:** additive

**Before**
```text
The package had no explicit rule connecting current governance-hardening phases to patch artifacts.
```

**After**
```text
The current hardening phases now link their governing patch artifacts explicitly, and the patch artifacts name their governing phases.
```

### Change Item 3
- **Target location:** package reviewability
- **Change type:** additive

**Before**
```text
Large governance deltas were primarily understandable from changelog prose.
```

**After**
```text
Governance deltas can now be reviewed through an explicit before/after patch surface.
```

---

## 4) Verification

- [ ] Confirm `patch/` exists in the package root
- [ ] Confirm design and README describe patch as a real governed surface
- [ ] Confirm phase 008 links this patch explicitly
- [ ] Confirm patch clarifies rather than duplicates changelog/phase roles

---

## 5) Rollback Approach

If this patch overcomplicates the package model:
- keep the artifact taxonomy clarification
- simplify the wording of patch-role guidance
- preserve explicit patch linkage for the current hardening wave once introduced
