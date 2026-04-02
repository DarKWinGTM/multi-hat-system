# Phase 012 - Plugin-compatible packaging and install cleanup

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 012
> **Status:** Implemented - Pending Review
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-012-plugin-compatible-packaging-and-install-cleanup.patch.md](../patch/phase-012-plugin-compatible-packaging-and-install-cleanup.patch.md)

---

## Objective

Keep plugin-compatible packaging and install-cleanup planning inside the main `multi-hat-system` workspace so the package does not split into duplicate governed projects.

## Why this phase exists

The duplicate plugin-pilot workspace created unnecessary authority drift. The package needs one governed workspace that owns runtime surfaces, plugin-compatible packaging, validation tracking, and install cleanup planning together.

## Action points / execution checklist

- [x] Add `.claude-plugin/plugin.json` to the main workspace
- [x] Make the main skill surface plugin-compatible
- [x] Move plugin-compatible packaging language into the main README/design/TODO/changelog/phase surfaces
- [x] Create one main-workspace patch surface for plugin-compatible packaging and install cleanup
- [x] Record the checked official activation/distribution model for local source plugins vs marketplace install
- [x] Validate persistent local-scope install from a shared local marketplace for this same workspace
- [x] Record the exact installed plugin cache path and local settings persistence model
- [ ] Validate `/reload-plugins` and restart-time visibility from this same workspace if hot-reload behavior still matters operationally
- [ ] Apply the winner/loser cleanup plan

## Observed official activation/distribution facts

- checked official docs document local source plugin loading through `claude --plugin-dir /path/to/plugin`
- checked official docs document distributed plugin installation through marketplace install
- checked official scope did not show a documented settings-based local plugin-path activation method across sessions

## Verification

- one main governed workspace remains authoritative
- plugin-compatible packaging is described from the main package, not a duplicate project
- cleanup planning remains attached to the same package authority
- local source vs marketplace distribution boundaries are explicit

## Exit criteria

- duplicate project is retired
- one workspace remains authoritative
- remaining validation work is tracked only from the main workspace
