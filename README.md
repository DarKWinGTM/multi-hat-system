# Multi-Hat System

A governed multi-perspective agent package for analyzing one task through three complementary lenses:
- **Developer Hat**
- **Security Hat**
- **Architect Hat**

The system targets **one canonical main agent only**:
- `agents/multi-hat-system.md`

The current product-hardening focus is making the front door more explicit in live usage so the user can see whether the package is in Advisory, Decision, or Clarify-First mode and why the chosen path fits.

The active package also includes:
- `skills/multi-hat-system/` as the operator bridge plus modular handbook surface
- `.claude-plugin/plugin.json` so the same package can be loaded through a plugin-compatible path without creating a second governed project
- governance artifacts at the package root
- `patch/*.patch.md` as the before/after evidence surface for governed changes

---

## Purpose

The Multi-Hat System exists to reduce single-perspective blind spots in complex technical analysis.

---

## Path notation

- `<repo-root>` = this standalone repo root and the preferred public source-side path for install commands
- `<workspace-root>` = the current local working copy of the same package
- `<user-runtime-agents>` = the user-level Claude Code runtime agent directory
- `<user-runtime-skills>` = the user-level Claude Code runtime skill directory

## Installation and activation

### Recommended public install path
This package now has its own standalone GitHub repo at:
- `https://github.com/DarKWinGTM/multi-hat-system`

Clone once, then run the install from the repo root:

```bash
git clone https://github.com/DarKWinGTM/multi-hat-system.git
cd multi-hat-system
claude plugins marketplace add ./ --scope local
claude plugins install multi-hat-system@multi-hat-system --scope local
```

Optional reload:

```bash
/reload-plugins
```

Check installed state:

```bash
claude plugins list
claude agents
```

Checked local validation from the repo root:
- `claude plugins marketplace add ./ --scope local` succeeds
- `claude plugins install multi-hat-system@multi-hat-system --scope local` succeeds
- `claude agents` shows `multi-hat-system:multi-hat-system`

### Update an installed plugin

If the plugin is already installed, update it by using the installed identifier shape `plugin@marketplace`:

```bash
claude plugins update multi-hat-system@darkwingtm --scope local
```

Why this exact shape matters:
- `claude plugins update multi-hat-system --scope local` may fail because the installed local plugin is keyed by `multi-hat-system@darkwingtm`
- the explicit `plugin@marketplace` form matches the installed identifier shown in `claude plugins list`

### Alternate local source loading

| Path | Current meaning | Status |
|---|---|---|
| `claude --plugin-dir "<repo-root>"` | documented local source loading for development/testing from the standalone repo | verified locally |
| `claude plugins marketplace add ./ --scope local` + `claude plugins install multi-hat-system@multi-hat-system --scope local` | repo-root local marketplace install for the standalone repo | validated locally |

### Local development compatibility note

The same package may still be referenced through the shared local `darkwingtm` marketplace during workspace development, but that route is no longer package authority. The standalone repo is now the intended source of truth, and any remaining shared-workspace usage should be treated as temporary local compatibility only.

What was **not** found in the checked official scope:
- no documented `settings.json` key that clearly persists a local plugin directory across sessions by path

So the package should currently be treated as:
- **standalone repo authority now**
- **validated repo-root local marketplace package now**
- **future broader marketplace/repository distribution candidate later**

It is designed to answer three operator situations:
- **Advisory Mode** — analyze one clearly defined task from 3 perspectives
- **Decision Mode** — compare explicit alternatives from 3 perspectives
- **Clarify First** — stop briefly when a missing high-impact constraint would materially change the answer

**Default behavior:** Advisory Mode

---

## Current Structure

```text
multi-hat-system/
  README.md
  TODO.md
  design/
    design.md
  changelog/
    changelog.md
  phase/
    SUMMARY.md
    phase-001-create-governance-baseline.md
    phase-002-lock-canonical-agent-design.md
    phase-003-review-and-approve-migration-plan.md
    phase-004-implement-canonical-main-agent.md
    phase-005-refactor-to-agents-and-skills.md
    phase-006-complete-substantive-content-migration.md
    phase-007-modularize-skill-handbook.md
    phase-008-establish-patch-model-and-artifact-taxonomy.md
    phase-009-clarify-surface-boundaries.md
    phase-010-add-operator-and-reviewer-guidance.md
    phase-011-multilingual-front-door.md
    phase-012-plugin-compatible-packaging-and-install-cleanup.md
  patch/
    phase-008-patch-model-and-artifact-taxonomy.patch.md
    phase-009-surface-boundary-clarification.patch.md
    phase-010-operator-reviewer-guidance.patch.md
    phase-011-multilingual-front-door.patch.md
    phase-012-plugin-compatible-packaging-and-install-cleanup.patch.md
  .claude-plugin/
    plugin.json
  agents/
    multi-hat-system.md
  skills/
    multi-hat-system/
      SKILL.md
      reference.md
      overview.md
      advisory-mode.md
      decision-mode.md
      developer-hat.md
      security-hat.md
      architect-hat.md
      synthesis.md
      validation.md
      anti-patterns.md
      examples.md
  prototype/
    System.md
    Framework.md
    Developer-Hat.md
    Security-Hat.md
    Architect-Hat.md
    multi-hat-system-framework.md
    multi-hat-advisor.md
    multi-hat-decision.md
```

---

## Canonical Runtime Authority

### `agents/multi-hat-system.md`
This is the active runtime authority for the package.

It owns:
- one-main-agent behavior
- advisory vs decision vs clarify-first routing
- proportional depth selection
- internal 3-hat perspective model
- unified response contract
- blocker / no-go rules
- guardrails against splitting one task into multiple per-hat tasks

---

## Skills Boundary

The `skills/multi-hat-system/` directory is the active **operator bridge + modular handbook** surface for the package.

Current intended contents:
- `SKILL.md` → operator/support entrypoint
- focused handbook files → canonical deep guidance by topic
- `reference.md` → handbook index / map

This support layer should reinforce the canonical main agent, not compete with it.

---

## Mode Model

### Advisory Mode (default)
Use when the user already has a clear task.

Examples:
- "Build an API for orders"
- "Improve authentication"
- "Design a microservice boundary"

Expected behavior:
- one task
- three perspectives
- one unified recommendation
- one short reason showing why this path fits better than the tempting shortcut

### Decision Mode
Use only when the user explicitly asks to compare alternatives.

Examples:
- "REST or GraphQL?"
- "PostgreSQL or MongoDB?"
- "Which is better for this use case?"

Expected behavior:
- explicit options
- three-perspective comparison
- one recommended option
- one short reason showing why the winning option fits better here
- clear trade-off explanation

### Clarify First
Use when a missing constraint would materially change the recommendation.

Examples:
- compliance obligations unknown
- scale target unknown
- team/runtime constraints unknown but decisive

Expected behavior:
- ask a few focused questions
- keep the uncertainty bounded
- continue once the missing constraint is resolved

---

## Package Boundary

The live package is defined by:
- `agents/` as the runtime authority surface
- `skills/` as the active operator bridge + modular handbook surface
- governance docs at the package root
- `patch/` as the governed before/after evidence surface

`prototype/` may remain for archive/inspiration value, but it is not part of the active package contract.

---

## Artifact Roles

| Artifact | Role |
|----------|------|
| `agents/multi-hat-system.md` | Canonical runtime authority |
| `skills/multi-hat-system/SKILL.md` | Operator/support bridge |
| `skills/multi-hat-system/*.md` | Canonical modular handbook |
| `design/design.md` | Target-state governance and architecture authority |
| `changelog/changelog.md` | Authoritative shipped/synchronized history |
| `TODO.md` | Execution tracking only |
| `phase/` | Governed execution planning and review state |
| `patch/*.patch.md` | Before/after change surface for governed deltas |
| `prototype/` | Archive/inspiration only |

### Phase vs patch

- **phase** = execution structure, scope, checklist, verification, review state
- **patch** = before/after delta and evidence surface
- **changelog** = completed or synchronized history only
- **TODO** = unresolved execution work only

---

## Current Status

Implemented so far:
- governance scaffold created
- one-main-agent target model locked
- canonical runtime authority established under `agents/`
- operator bridge and modular handbook established under `skills/`
- active package rewritten to be self-sufficient
- substantive operating playbook migrated into the active package
- skill handbook split into focused support files so it is easier to evolve section-by-section
- patch baseline, artifact taxonomy, surface-boundary clarification, and operator/reviewer guidance are now part of the governed package model
- shared local marketplace scaffolding also exposes this package for checked workspace development, but that is no longer the recommended public install story
- plugin visibility remains intact after `/reload-plugins`
- fresh CLI-process visibility confirms the marketplace-installed package remains available across session restarts

Current review focus:
- validate whether the new governance-hardening wave is sufficient in live usage
- validate whether multilingual front-door wording improves advisory / decision / clarify-first interpretation without creating new mode confusion
- validate `/reload-plugins` only if hot-reload behavior remains operationally important after repo-root local marketplace install is in place
- decide when to retire loser runtime-distribution paths after marketplace-installed usage stays stable
- polish public-repo readiness while keeping `@darkwingtm` as the current shared publisher namespace

Deferred for later:
- archive/reorganization work if needed later
- optional sync workflow into `<user-runtime-agents>/` and `<user-runtime-skills>/`

---

## Prototype Boundary

`prototype/` remains available for archive/inspiration value only.

Current governed disposition model:
- **migrated** → concepts already absorbed into the active package
- **deferred** → ideas worth revisiting later if real usage reveals a need
- **intentionally not migrated** → archive material that should not become active authority by default

Prototype is therefore still useful context, but not current-system authority.

---

## What to review next

1. Does `agents/multi-hat-system.md` remain compact while fully runtime-capable?
2. Does `SKILL.md` still work as a real operator bridge?
3. Does the split handbook under `skills/multi-hat-system/*.md` now provide enough modular depth without forcing prototype fallback?
4. Is the new patch layer sufficient to make governance changes reviewable before they drift into narrative-only history?
5. Are artifact boundaries now explicit enough that active package vs archive package confusion is materially reduced?
