# Multi-Hat System - TODO

> **Last Updated:** 2026-04-03

---

## ✅ Completed

- [x] Create governance baseline for `multi-hat-system` with `design`, `changelog`, `TODO`, and `phase` before any runtime rewrite.
- [x] Create the first canonical runtime authority for the package.
- [x] Polish and enrich the canonical main agent with sharper mode behavior, compact high-value hat checkpoints, and stronger synthesis guardrails.
- [x] Rewrite the active package surface so `agents/` and `skills/` are self-sufficient and no longer depend on prototype paths for current-system correctness.
- [x] Complete the substantive content migration so the active package carries real advisory/decision mechanics, richer per-hat depth, stronger synthesis discipline, and a deeper support handbook.
- [x] Split the skill handbook into focused support files so the support surface is modular, easier to evolve, and closer to the original prototype decomposition style.
- [x] Add the governed patch baseline and artifact taxonomy for steady-state governance.
- [x] Clarify active surface vs archive/prototype boundaries and formalize prototype disposition.
- [x] Add explicit operator/reviewer guidance for live-usage review and future adoption decisions.

---

## 📋 Tasks To Do

### Current Governance Execution
- [x] Review the governance-hardening wave across README/design/changelog/TODO/phase/patch and identify only remaining real gaps from live usage.
- [x] Harden the front-door output contract so Advisory / Decision / Clarify-First mode behavior is more explicit and more decision-useful in live usage.
- [ ] Implement the multilingual front-door routing wave so the active package can better interpret advisory / decision / clarify-first prompts across prompt languages without translating the full handbook.
- [x] Validate persistent plugin install and local-scope visibility from this same package through a shared local marketplace.
- [x] Record the exact local marketplace-installed cache path and settings persistence model for this package.
- [x] Validate `/reload-plugins` visibility from the marketplace-installed path.
- [x] Validate restart-time visibility from the marketplace-installed path.
- [ ] Apply the winning-path cleanup plan so only one active runtime distribution remains.
- [ ] Complete separate-repo cutover and retire shared-workspace authority once the standalone repo becomes the source of truth.

### Deferred / Later Decisions
- [ ] Decide when to archive, trim, or reorganize the `prototype/` corpus after the active package is stable in use.
- [ ] Decide when to sync the finalized package into `<user-runtime-agents>/` and `<user-runtime-skills>/` again.
- [ ] Decide whether to distribute this same workspace through a marketplace-style plugin path once metadata and release posture are ready.

---

## 📜 History

| Date | Changes |
|------|---------|
| 2026-04-03 | Hardened the front-door output contract across the runtime agent and support skill, clarified why-this-path / why-this-winner expectations in live usage, and bumped the plugin/marketplace package versions for installed update visibility. |
| 2026-04-03 | Normalized public install docs to the standalone repo root, validated `claude plugins marketplace add ./ --scope local` plus `claude plugins install multi-hat-system@multi-hat-system --scope local` from the repo root in an isolated HOME, and kept the shared `darkwingtm` path scoped as checked local workspace-development context. |
| 2026-04-02 | Added the shared local marketplace scaffold, validated local-scope plugin install for `multi-hat-system`, recorded the persisted local settings entry plus plugin-cache path model, and resynchronized README/design/changelog/TODO/phase/patch to match the new activation truth. |
| 2026-03-30 | Added the governed `patch/*.patch.md` baseline, defined the explicit artifact taxonomy, clarified active vs archive/prototype boundaries, formalized prototype disposition, and added operator/reviewer guidance for steady-state package governance. |
| 2026-03-28 | Split the skill support layer into focused handbook files (`overview.md`, `advisory-mode.md`, `decision-mode.md`, per-hat files, `synthesis.md`, `validation.md`, `anti-patterns.md`, `examples.md`) so the active package can evolve section-by-section instead of concentrating all support depth into one `reference.md`, and resynchronized README/design/TODO to describe the modular skill surface truthfully. |
| 2026-03-28 | Completed the substantive content migration into the active package: rewrote `agents/multi-hat-system.md` to carry clearer runtime-critical behavior, upgraded `skills/multi-hat-system/SKILL.md` into a stronger operator bridge, expanded `skills/multi-hat-system/reference.md` into a deeper handbook with evaluation frameworks / scorecards / anti-patterns / worked shapes, and resynchronized README/design/TODO/phase governance so the package is described as substantively complete rather than only structurally correct. |
| 2026-03-28 | Completed the earlier substantive migration wave: expanded `skills/multi-hat-system/reference.md` into a real operating playbook, upgraded `SKILL.md` into an operator/support guide, strengthened the canonical agent with runtime-critical mechanics, and updated governance docs so the package can be understood and used without relying on the prototype corpus for current-system correctness. |
| 2026-03-28 | Rewrote the active package surface so `agents/` and `skills/` are self-sufficient: removed prototype-driven dependency language from the canonical agent, support skill, reference guide, README, design, TODO, changelog, and phase docs while keeping `prototype/` only as archive/inspiration material. |
| 2026-03-28 | Refactored the package model to mirror the Claude runtime layout more explicitly: moved the canonical runtime authority to `agents/multi-hat-system.md`, added `skills/multi-hat-system/` as the active support/reference surface, and updated design/README/TODO/changelog/phase tracking to match. |
| 2026-03-28 | Added `README.md` for the governed `multi-hat-system` package so the canonical runtime authority, mode model, prototype boundary, governance files, and next review questions are visible from one overview document. |
| 2026-03-28 | Polished and enriched `multi-hat-system.md` with sharper advisory-vs-decision behavior, compact high-value Developer/Security/Architect checkpoints, and stronger synthesis guardrails while keeping the one-main-agent model and leaving `prototype/` untouched. |
| 2026-03-28 | Created `multi-hat-system.md` as the first canonical runtime authority for `<workspace-root>/`; preserved `prototype/` unchanged as source/reference material; and added `phase/phase-004-implement-canonical-main-agent.md` to record the first implementation wave. |
| 2026-03-28 | Created the governance-first scaffold for `<workspace-root>/`: added `design/design.md`, `changelog/changelog.md`, `TODO.md`, and `phase/` planning files; defined the target as one canonical future main agent only; and classified current `prototype/` files into future roles before implementation. |
