# Phase 011 - Multilingual front door

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 011
> **Status:** In Progress
> **Session:** a0fe4e7f-e9e7-41ac-a473-3fcdbbf39ba2
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-011-multilingual-front-door.patch.md](../patch/phase-011-multilingual-front-door.patch.md)

---

## Objective

Improve multilingual prompt interpretation at the package front door without translating the deep handbook into other languages.

## Why this phase exists

The package already has a strong active boundary and front-door model, but current routing cues are still mostly English. The cleanest evidence-backed improvement is to add intent-oriented multilingual examples and wording where mode/package selection is actually decided.

## Entry conditions / prerequisites

- The package already has a governed patch baseline
- Artifact taxonomy and active/archive boundaries are already explicit
- Operator/reviewer guidance already exists for steady-state package review

## Action points / execution checklist

- [x] Add the multilingual-front-door wave to `TODO.md`
- [x] Add phase 011 to `phase/SUMMARY.md`
- [ ] Update package design and README to document multilingual support as a front-door routing layer only
- [ ] Add intent-oriented wording to `agents/multi-hat-system.md`
- [ ] Add multilingual examples to `skills/multi-hat-system/SKILL.md`
- [ ] Add a brief multilingual intent-mapping note to `skills/multi-hat-system/overview.md`
- [ ] Add multilingual advisory / decision / clarify-first checks to `skills/multi-hat-system/validation.md`
- [ ] Record the before/after front-door surface in patch form
- [ ] Update changelog after implementation is complete
- [ ] Sync changed active files to `~/.claude/agents/` and `~/.claude/skills/`

## Out of scope

- Full handbook translation
- Deep edits to hat-specific handbook files unless front-door changes prove insufficient
- Central RULES changes

## Affected artifacts

- `../README.md`
- `../design/design.md`
- `../TODO.md`
- `../phase/SUMMARY.md`
- `../patch/phase-011-multilingual-front-door.patch.md`
- `../agents/multi-hat-system.md`
- `../skills/multi-hat-system/SKILL.md`
- `../skills/multi-hat-system/overview.md`
- `../skills/multi-hat-system/validation.md`
- installed copies under `~/.claude/agents/` and `~/.claude/skills/`

## TODO coordination

This phase turns multilingual front-door support into explicit execution work rather than leaving it as an implicit future refinement.

## Changelog coordination

Changelog should record the multilingual front-door change only after the package surfaces and installed copies are updated.

## Verification

Success should mean:
- prompts for analysis/recommendation/comparison are easier to map at the front door across prompt languages
- advisory vs decision vs clarify-first remains explicit
- the package still produces one unified answer rather than per-hat roleplay
- deeper handbook content remains English and unchanged unless strictly necessary

## Exit criteria

- phase 011 artifacts exist
- front-door surfaces contain multilingual intent guidance
- design/README explain the new boundary cleanly
- patch captures the before/after front-door surface
- installed copies are synced
- validation notes are recorded honestly

## Risks / rollback notes

- Do not bloat the front-door wording until it becomes noisy
- Do not push multilingual examples so deep that the handbook becomes partially duplicated
- If a wording change causes advisory/decision confusion, narrow the wording rather than broadening the whole package

## Next possible phases

- a later narrow validation follow-up if multilingual advisory/decision classification still drifts materially after front-door tuning
