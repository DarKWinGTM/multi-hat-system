# Phase 007 - Modularize skill handbook

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 007
> **Status:** Completed
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** n/a

---

## Objective

Split the skill handbook into focused support files so the support surface stays modular, maintainable, and easy to evolve section-by-section instead of concentrating all handbook depth into a single file.

## Why this phase exists

The package structure was already correct, but keeping most handbook detail inside one `reference.md` still created unnecessary concentration. This phase exists to restore a more decomposed structure similar in spirit to the prototype while preserving the one-agent / one-skill runtime model.

## Design Extraction

- Source requirement: the live support surface should remain one skill package while allowing its detailed content to be split into maintainable sections
- Derived execution work: keep `SKILL.md` as the skill entrypoint, convert `reference.md` into an index, create focused handbook files by topic, and resync README/design/TODO/changelog/phase docs
- Target outcome: the skill package remains one canonical support surface but its handbook depth is distributed across focused files

## Flow Diagram

single-file-heavy support handbook exists
  → keep `SKILL.md` as entrypoint
  → convert `reference.md` into index/map
  → split detailed content into focused handbook files
  → keep all files inside the same skill package
  → support layer becomes modular and easier to maintain

## Reviewer Checklist

- [x] `SKILL.md` remains the operator bridge and skill entrypoint
- [x] focused handbook files created for major concerns
- [x] support files remain part of one skill package rather than separate skills
- [x] `reference.md` now acts as a handbook index rather than a concentrated handbook blob
- [x] governance docs updated to describe the modular support surface truthfully

## Verification

- focused support files created under `skills/multi-hat-system/`
- `SKILL.md` rewritten to act as navigation surface
- `reference.md` rewritten as modular handbook index
- README/design/TODO/changelog/phase docs updated to reflect the modularized support surface
- runtime authority remains unchanged under `agents/multi-hat-system.md`

## Exit Criteria

- the support surface is modular, easier to evolve, and no longer unnecessarily concentrated in one support file while still remaining a single coherent skill package
