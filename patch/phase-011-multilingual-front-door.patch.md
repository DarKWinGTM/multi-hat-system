# Phase 011 Multilingual Front Door Patch

## 0) Document Control

> **Current Version:** 1.0
> **Status:** In Progress
> **Target Design:** [../design/design.md](../design/design.md) v1.4
> **Target Phase:** [../phase/phase-011-multilingual-front-door.md](../phase/phase-011-multilingual-front-door.md)
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Full history:** [../changelog/changelog.md](../changelog/changelog.md)

---

## 1) Context

This patch captures the front-door before/after surface for improving multilingual interpretation in the active multi-hat package.

Why this matters:
- current front-door routing cues are still mostly English
- the user wants better multilingual interpretation without rewriting the full package into other languages
- the highest-leverage package surfaces are the canonical agent description and the skill front door

---

## 2) Analysis

Risk level: Medium

Dependencies:
- `../design/design.md`
- `../README.md`
- `../TODO.md`
- `../phase/SUMMARY.md`
- `../agents/multi-hat-system.md`
- `../skills/multi-hat-system/SKILL.md`
- `../skills/multi-hat-system/overview.md`
- `../skills/multi-hat-system/validation.md`

Review concern:
- front-door wording must improve multilingual intent interpretation without introducing advisory vs decision confusion or turning the package into duplicated multilingual documentation

---

## 3) Change Items

### Change Item 1
- **Target location:** canonical agent description
- **Change type:** replacement

**Before**
```text
Description is mostly English-only.
```

**After**
```text
Description stays English, but explicitly says mode/package selection should follow user intent rather than exact wording or prompt language.
```

### Change Item 2
- **Target location:** skill front door
- **Change type:** additive

**Before**
```text
SKILL front-door guidance and examples are primarily English-only.
```

**After**
```text
SKILL front-door guidance includes multilingual examples that help map advisory, decision, and clarify-first requests without translating the deeper handbook.
```

### Change Item 3
- **Target location:** validation surface
- **Change type:** additive

**Before**
```text
Validation guidance does not explicitly test multilingual advisory / decision / clarify-first classification.
```

**After**
```text
Validation guidance includes multilingual prompt checks to verify that the front door still preserves one-task / one-answer behavior and correct mode classification.
```

---

## 4) Verification

- [ ] Confirm the canonical agent description now emphasizes intent-based mode/package selection rather than exact wording or prompt language
- [ ] Confirm SKILL front-door examples include multilingual advisory/decision/clarify-first shapes
- [ ] Confirm overview documents the multilingual front-door boundary without turning into a translated handbook
- [ ] Confirm validation now checks multilingual mode classification explicitly
- [ ] Confirm the patch remains focused on front-door surfaces only

---

## 5) Rollback Approach

If the multilingual front-door wording creates new confusion:
- narrow or remove the conflicting wording
- keep the English baseline intact
- preserve this patch as the historical record of the attempted front-door change
