# Phase 012 Plugin-Compatible Packaging and Install Cleanup Patch

## 0) Document Control

> **Current Version:** 1.1
> **Status:** Implemented - Pending Review
> **Target Design:** [../design/design.md](../design/design.md) v1.5
> **Target Phase:** [../phase/phase-012-plugin-compatible-packaging-and-install-cleanup.md](../phase/phase-012-plugin-compatible-packaging-and-install-cleanup.md)
> **Session:** dd0bf4af-a66b-4b07-bb9d-a90a0e57b54e
> **Full history:** [../changelog/changelog.md](../changelog/changelog.md)

---

## 1) Context

This patch captures the consolidation of plugin-compatible packaging and install-cleanup planning back into the main `multi-hat-system` workspace, plus the extension into a validated shared local marketplace install path.

## 2) Analysis

Risk level: Medium

The duplicate plugin-pilot workspace created unnecessary authority drift for the same package. Plugin-compatible packaging, validation tracking, and install cleanup need to stay attached to the real package authority instead of living in a second governed project.

---

## 3) Change Items

### Change Item 1
- **Target location:** main package runtime structure
- **Change type:** additive

**Before**
```text
The main package had runtime and skill surfaces but no plugin manifest inside the same governed workspace.
```

**After**
```text
The main package now includes `.claude-plugin/plugin.json` so plugin-compatible loading belongs to the same governed workspace.
```

### Change Item 2
- **Target location:** package governance surfaces
- **Change type:** replacement

**Before**
```text
Plugin packaging and install-cleanup planning had drifted into a second duplicate governed project.
```

**After**
```text
Plugin-compatible packaging, validation tracking, and install-cleanup planning now live in the main `multi-hat-system` governance chain.
```

### Change Item 3
- **Target location:** duplicate project topology
- **Change type:** deletion

**Before**
```text
A second workspace `multi-hat-system-plugin-pilot` existed beside the main package, duplicating runtime surfaces and governance artifacts.
```

**After**
```text
The duplicate workspace is removed so one governed package remains authoritative.
```

### Change Item 4
- **Target location:** shared local marketplace root, local Claude settings persistence, and plugin cache path
- **Change type:** additive

**Before**
```text
The package could be tested through `claude --plugin-dir <workspace-root>`, but there was no validated marketplace-style local install path attached to the same governed workspace.
```

**After**
```text
A shared marketplace manifest at `<marketplace-root>/.claude-plugin/marketplace.json` exposes `multi-hat-system`, local marketplace declaration persists through `.claude/settings.local.json`, and local install materializes a cached plugin copy at `~/.claude/plugins/cache/darkwingtm/multi-hat-system/1.0.0/`.
```

---

## 4) Verification

- [x] `.claude-plugin/plugin.json` exists in the main workspace
- [x] main workspace docs describe plugin-compatible packaging directly
- [x] duplicate `multi-hat-system-plugin-pilot` workspace has been removed
- [x] plugin install-cleanup planning is now tracked from the main workspace
- [x] shared local marketplace manifest validates
- [x] `claude plugins marketplace add <marketplace-root> --scope local` succeeds
- [x] `claude plugins install multi-hat-system@darkwingtm --scope local` succeeds
- [x] `claude agents` shows `multi-hat-system:multi-hat-system` after local marketplace install
- [x] `multi-hat-system:multi-hat-system` remains visible after `/reload-plugins`

---

## 5) Rollback Approach

If this consolidation proves wrong, restore plugin validation tracking inside the main package rather than recreating a second duplicate governance project. The rollback-safe principle is one package authority, not parallel package copies.
