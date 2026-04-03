# Multi-Hat System

## 0) Document Control

> **Parent Scope:** Multi-Hat System Design
> **Current Version:** 1.6
> **Session:** dd0bf4af-a66b-4b07-bb9d-a90a0e57b54e (2026-04-02)

---

## 1) Path notation

- `<repo-root>` = this standalone repo root and the preferred public source-side path for install commands
- `<workspace-root>` = the current local working copy of the same package
- `<user-runtime-agents>` = the user-level Claude Code runtime agent directory
- `<user-runtime-skills>` = the user-level Claude Code runtime skill directory

## 2) Goal

Provide a governed design baseline for `<repo-root>/` as the standalone source of truth, so the live package can operate as **one canonical main agent file plus one canonical modular support surface** without depending on archive material for current-system correctness.

This design establishes the live package structure by defining:
- one canonical main agent only
- advisory mode as the default operating mode
- decision/comparison behavior as a mode inside the same main agent rather than a peer agent
- hats as internal analytical perspectives, not separate active agents
- one canonical support/reference surface under `skills/`
- one governed patch surface for before/after evidence
- a governance model that keeps the live package self-sufficient and split into maintainable sections

---

## 2) Current-State Inventory

The live package now consists of:
- `agents/multi-hat-system.md`
- `skills/multi-hat-system/SKILL.md`
- `skills/multi-hat-system/reference.md`
- focused skill support files under `skills/multi-hat-system/*.md`
- `README.md`
- `design/design.md`
- `changelog/changelog.md`
- `TODO.md`
- `phase/`
- `patch/`

An archive/inspiration corpus still exists under `prototype/`.

Current-state observations:
- the live package structure exists and mirrors the Claude runtime model directly
- the live package now carries substantive operating mechanics rather than only a thin structural shell
- the skill support surface is now split into focused support files instead of concentrating everything in one handbook file
- deeper future refinements should extend the active package itself rather than reintroducing archive files as active dependencies
- the governance model now needs an explicit patch/evidence layer and clearer surface taxonomy for steady-state maintenance

---

## 3) Target Repository Model

### 3.1 Canonical runtime artifact

The runtime authority should converge to **one canonical main agent file only**.

Canonical runtime path:
- `agents/multi-hat-system.md`

This file exists as the active canonical runtime authority.

### 3.2 Modes, not peer agents

The target system supports two operating modes inside the same canonical main agent:
- **Advisory Mode** — default, for a single defined task
- **Decision Mode** — only when the user explicitly asks for comparison between alternatives

The target model explicitly rejects:
- separate peer agents for advisory vs decision
- separate peer agents for each hat

### 3.3 Hat model

The three hats remain mandatory analytical perspectives for complex work:
- Developer Hat
- Security Hat
- Architect Hat

In the target model, these are internal reasoning lenses, not separate active agent artifacts.

### 3.4 Active package boundary

The intended live boundary is:
- `agents/multi-hat-system.md` = active runtime authority
- `skills/multi-hat-system/SKILL.md` = operator/support bridge and entrypoint
- `skills/multi-hat-system/*.md` = focused support/reference files inside the same skill package
- `.claude-plugin/plugin.json` = plugin-compatible packaging metadata for the same governed package
- `design/changelog/TODO/phase` = governance authority for the package
- `patch/*.patch.md` = governed before/after evidence artifacts
- `prototype/` = archive/inspiration material only

---

## 4) Canonical Main Agent Contract

The canonical main agent should own:
- identity and mission of the multi-hat system
- advisory-vs-decision mode detection
- clarify-first gate for materially missing context
- proportional depth selection
- the rule that one task is analyzed through three perspectives rather than split into three tasks
- per-hat minimum deliverables
- synthesis protocol
- evidence/confidence discipline
- blocker / no-go behavior
- concise response contracts for advisory mode, decision mode, and clarify-first handling
- front-door output guidance that makes the active mode and chosen path legible in live usage
- guardrails against misuse, scope drift, and accidental peer-agent behavior

The canonical main agent should not directly embed every long explanatory, example-heavy, or checklist-heavy document in full.

It should remain a self-sufficient runtime contract, with deeper explanation and operating detail kept in the active support/reference surface under `skills/`.

---

## 5) Active Package Model

The package should be maintainable from its active surfaces alone:
- `agents/multi-hat-system.md`
- `skills/multi-hat-system/SKILL.md`
- focused support files under `skills/multi-hat-system/`

### 5.1 `agents/multi-hat-system.md`
Should stay compact but fully operational.

It owns:
- runtime-critical behavior
- mode detection
- depth selection
- per-hat deliverable minimums
- synthesis rules
- no-go / blocker logic
- final response contract

### 5.2 `skills/multi-hat-system/SKILL.md`
Should act as the operator and maintainer bridge.

It owns:
- quick mode selection guidance
- depth-selection guidance
- practical quality gates
- maintainer boundary rules
- navigation into the modular handbook

### 5.3 Focused support files under `skills/multi-hat-system/`
Should act as the deep canonical handbook, split by concern.

Recommended role split:
- `overview.md` — doctrine and use boundaries
- `advisory-mode.md` — detailed default single-task method
- `decision-mode.md` — detailed explicit comparison method
- `developer-hat.md` — Developer framework
- `security-hat.md` — Security framework
- `architect-hat.md` — Architect framework
- `synthesis.md` — cross-hat resolution rules
- `validation.md` — evidence ladder, scorecards, and review checklist
- `anti-patterns.md` — failure modes to avoid
- `examples.md` — worked shapes
- `reference.md` — modular index / handbook map

The archive corpus may remain available for historical context, but it is not part of the active package contract.

---

## 6) Artifact Taxonomy and Patch Model

### 6.1 Artifact taxonomy

| Surface | Role |
|---------|------|
| `agents/` | active runtime authority |
| `skills/` | active operator bridge + modular handbook |
| `design/` | target-state governance authority |
| `changelog/` | shipped/synchronized package history |
| `TODO.md` | unresolved execution work |
| `phase/` | governed execution plan and review state |
| `patch/` | before/after evidence for governed deltas |
| `prototype/` | archive/inspiration only |

### 6.2 Patch role

Patch artifacts exist to show:
- what changed
- where it changed
- what the previous state was
- what the target state became after the change
- what was intentionally preserved, excluded, or deferred when that distinction matters

Patch artifacts should be used when:
- a governance change materially affects package boundaries or policy
- a phase introduces a meaningful structural or operational delta worth explicit review
- operator/reviewer guidance changes need a clear before/after surface

### 6.3 Phase-to-patch linkage rule

When patch is in scope:
- `phase/SUMMARY.md` should link the relevant patch artifact explicitly
- the child phase file should name the patch in `Patch References`
- the patch should name its governing phase

### 6.4 Artifact boundary rule

- **phase** = why the work exists, what it does, how it is reviewed, and when it is done
- **patch** = the explicit before/after delta
- **changelog** = completed or synchronized history only
- **TODO** = unresolved execution work only

### 6.5 Multilingual front-door rule

Multilingual prompt support should be implemented at the front door through intent-oriented wording, not by translating the full package or depending on hard-coded language-specific trigger lists.

The intended model is:
- keep the canonical runtime and handbook bodies in English
- make mode selection and package selection follow task intent rather than exact wording or prompt language
- add multilingual examples only where they materially improve front-door understanding or validation

### 6.6 Single-workspace plugin-compatible packaging rule

Plugin-compatible packaging for `multi-hat-system` should live inside the same governed workspace, not in a second duplicate project.

The intended model is:
- one governed package at `<workspace-root>`
- one runtime authority under `agents/`
- one support surface under `skills/`
- one plugin manifest under `.claude-plugin/plugin.json`
- one cleanup plan for installed runtime paths

This avoids duplicate governance chains for the same package and keeps plugin-path validation attached to the real package authority.

### 6.7 Official activation/distribution model

From the checked official Claude Code plugin docs:
- local source plugin testing is documented through `claude --plugin-dir /path/to/plugin`
- standard distributed plugin installation is documented through marketplace install
- local marketplaces are documented, so this same package can be added from the standalone repo root through `claude plugins marketplace add ./ --scope local` without creating a duplicate workspace

Checked local validation now shows:
- local marketplace declaration persists through project-local Claude settings
- local marketplace install surfaces the packaged agent in normal `claude agents` discovery
- the installed package materializes as a cached plugin copy under the Claude plugin cache for the declared marketplace and package version

Not found in the checked official scope:
- no documented settings-based local directory activation method that clearly persists a local plugin path across sessions

So the strategic distribution target should be:
- treat `<repo-root>` as the package authority now
- keep this package usable as a local source plugin now
- use repo-root local marketplace install as the public local install/distribution path now
- treat the shared `darkwingtm` route only as temporary checked local compatibility context, not source authority
- keep the same package ready for broader marketplace-style distribution later
- do not invent a second local project just to simulate plugin packaging

---

## 7) Prototype Disposition Model

The active package should no longer treat `prototype/` as a shadow source of authority.

Instead, prototype content should be interpreted through one of three dispositions:
- **migrated** — active package already absorbed the useful concept
- **deferred** — worth revisiting later if live usage reveals a real need
- **intentionally not migrated** — archive value remains, but the concept should not become active authority by default

This keeps prototype usable as inspiration without making it responsible for current-system correctness.

---

## 8) Substantive Completion Standard

The package is **structurally complete** when the active file-role split is correct.

The package is **substantively complete** only when the active files carry the important operating mechanics of the original system, including:
- real advisory-mode discipline
- real decision-mode comparison discipline
- real per-hat evaluation depth
- real synthesis and tension-resolution behavior
- explicit evidence and confidence discipline
- practical operator/maintainer guidance
- modular handbook depth that can be developed section-by-section without crowding one file
- enough active-surface depth that the package can be used without opening archive files

---

## 9) Phase Strategy

### Phase 001
Create governance baseline.

### Phase 002
Lock canonical agent design.

### Phase 003
Review and approve the migration plan before any runtime rewrite starts.

### Phase 004
Implement the canonical main agent.

### Phase 005
Refactor the package to the `agents/` + `skills/` layout and mirror the live Claude structure more explicitly.

### Phase 006
Complete the substantive content migration so the active package carries the real multi-hat operating playbook rather than only a thin shell.

### Phase 007
Split the skill handbook into focused support files so the support surface stays modular, maintainable, and closer to the prototype's sectioned structure without reintroducing peer-skill drift.

### Phase 008
Establish the governed patch model and explicit artifact taxonomy for steady-state maintenance.

### Phase 009
Clarify active surface vs archive surface boundaries and formalize prototype disposition.

### Phase 010
Add explicit operator/reviewer guidance for live usage, review disposition, and future adoption decisions.

### Phase 011
Improve multilingual prompt interpretation at the package front door without translating the deep handbook into other languages.

### Phase 012
Keep plugin-compatible packaging and install-cleanup planning inside the same governed workspace, then validate persistent local marketplace install for that same package.

---

## 10) Deferred Work

Deferred from the current wave:
- moving, deleting, or archiving `prototype/` files
- trimming or de-duplicating the archive corpus after the active package is stable
- later sync workflow into `<user-runtime-agents>/` and `<user-runtime-skills>/`
- future refinements driven by real usage observations

The package structure now mirrors the live Claude layout directly:
- `agents/` as the runtime-agent surface
- `skills/` as the modular support/reference surface
- `patch/` as the governed before/after evidence surface
- `prototype/` as archive/inspiration material only

---

## 11) Acceptance Criteria

This package is considered substantially complete only when:
- `agents/multi-hat-system.md` is the canonical runtime authority
- advisory mode is explicitly default
- decision mode is explicitly conditional
- clarify-first handling exists for materially missing context
- hats are internal analytical perspectives, not peer agents
- `skills/multi-hat-system/` acts as a real modular support/reference surface rather than a thin stub or a single crowded handbook file
- the active package carries the substantive operating mechanisms of the original system, not just the structural shell
- design, changelog, TODO, README, phase, and patch artifacts all exist and cross-link cleanly
- archive material is not required for current-system correctness
- prototype disposition is explicit enough that archive and active package are not confused

---

## 12) Related Documents

- [../changelog/changelog.md](../changelog/changelog.md)
- [../TODO.md](../TODO.md)
- [../phase/SUMMARY.md](../phase/SUMMARY.md)
- [../agents/multi-hat-system.md](../agents/multi-hat-system.md)
- [../skills/multi-hat-system/SKILL.md](../skills/multi-hat-system/SKILL.md)
- [../skills/multi-hat-system/reference.md](../skills/multi-hat-system/reference.md)

---

> Full history: [../changelog/changelog.md](../changelog/changelog.md)
