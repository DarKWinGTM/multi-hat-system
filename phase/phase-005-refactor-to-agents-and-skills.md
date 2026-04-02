# Phase 005 - Refactor to agents and skills

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 005
> **Status:** Completed
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** n/a

---

## Objective

Patch the governance/docs model first, then refactor the package so it mirrors the Claude runtime layout more directly through `agents/` and `skills/`.

## Why this phase exists

The package initially implemented a root-level canonical file, but the desired long-term model is clearer if the source workspace mirrors `~/.claude/agents/` and `~/.claude/skills/` directly.

## Design Extraction

- Source requirement: runtime authority should live under `agents/` and support/reference material should live under `skills/`
- Derived execution work: patch docs, move the canonical agent into `agents/`, create `skills/multi-hat-system/`, and preserve `prototype/`
- Target outcome: the governed package structure now mirrors the Claude runtime mental model more closely

## Flow Diagram

Root-level canonical file exists
  → patch design and governance docs first
  → create `agents/` and `skills/`
  → move canonical agent into `agents/`
  → create support/reference files under `skills/`
  → preserve `prototype/` untouched
  → package structure now mirrors runtime layout

## Reviewer Checklist

- [x] docs patched before structure move
- [x] canonical runtime authority now lives under `agents/`
- [x] support/reference surface now lives under `skills/`
- [x] `prototype/` remains untouched as frozen source material
- [x] README, TODO, changelog, and phase tracking reflect the new structure

## Verification

- `agents/multi-hat-system.md` exists
- `skills/multi-hat-system/SKILL.md` exists
- `skills/multi-hat-system/reference.md` exists
- package docs reflect `agents/` + `skills/`
- no prototype files changed

## Exit Criteria

- the package structure mirrors the Claude runtime model without reintroducing peer-agent ambiguity or collapsing support/reference material back into runtime authority
