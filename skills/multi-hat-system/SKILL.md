---
name: Multi-Hat System Support Skill
description: This skill should be used when the user needs deeper operator guidance for the multi-hat-system package, including mode selection, hat expectations, synthesis review, package maintenance, or plugin-compatible usage of the same package.
version: 1.0.0
---

# Multi-Hat System Support Skill

This skill is the **active operator and support surface** for the governed `multi-hat-system` package.

It complements the canonical runtime authority at:
- `../../agents/multi-hat-system.md`

This skill exists to help a maintainer or operator:
- choose the correct operating mode
- choose the right depth for the task
- understand what the three hats must contribute
- review whether a response is complete enough
- navigate the deeper modular handbook
- extend the package without reintroducing peer-agent drift

---

## When to use this skill

Use this support skill when you need to:
- deepen the analysis method behind the canonical agent
- review whether advisory, decision, or clarify-first handling was chosen correctly
- inspect what each hat should contribute in more detail
- pressure-test synthesis quality
- review anti-patterns, examples, and quality criteria
- maintain or extend the package without bloating the runtime file

---

## Quick mode selector

| Situation | Mode | Why |
|---|---|---|
| User already has a defined task | Advisory | Improve the same task from 3 perspectives |
| User explicitly asks to compare alternatives | Decision | Compare explicit options and recommend one |
| Missing constraint would materially change the answer | Clarify first | Avoid giving a misleadingly strong recommendation |

### Advisory examples
- "Build an API for orders"
- "Improve authentication"
- "Design a migration plan"
- "How should I implement a queue worker?"
- "ช่วยวิเคราะห์แนวทางทำระบบนี้"

### Decision examples
- "REST or GraphQL?"
- "PostgreSQL or MongoDB?"
- "Monolith or microservices?"
- "ควรเลือกแบบไหนดีระหว่าง A กับ B"

### Clarify-first examples
- request is too vague to assess responsibly
- compliance, scale, or runtime constraints are unknown and would flip the recommendation
- team capability or delivery constraints are unknown but decisive
- "ช่วยออกแบบระบบนี้" แต่ยังไม่รู้ scale / compliance / runtime constraints ที่เปลี่ยนคำแนะนำอย่างมีนัยสำคัญ

---

## Depth selector

| Task shape | Suggested depth | Typical behavior |
|---|---|---|
| small local change | Light | concise multi-hat check without heavy ceremony |
| normal engineering task | Standard | full hat coverage with compact synthesis |
| high-risk or long-lived decision | Full | strong hat detail, explicit tensions, stronger validation discipline |

Use more depth when:
- security exposure is meaningful
- architecture consequences are long-lived
- rollout/migration risk matters
- the user explicitly wants deep analysis

---

## Standard workflow

1. Normalize the task or decision.
2. Choose the correct mode.
3. Choose proportional depth.
4. Extract constraints, assumptions, and unknowns.
5. Ask focused clarifying questions only if the missing context is materially decisive.
6. Run all three hats on the same task or explicit option set.
7. Surface the main tensions.
8. Synthesize one recommendation or one winning option.
9. Make the front-door shape explicit so the user can tell why this path won.
10. Check whether the answer is practical, evidence-aware, and non-generic.

---

## What each hat must add

### Developer Hat
Must contribute something concrete about:
- implementation shape
- complexity or delivery effort
- maintainability, testing, or observability
- blockers, hidden complexity, or team fit

### Security Hat
Must contribute something concrete about:
- top threat or failure mode
- required controls
- sensitive-data, auth, logging, or compliance impact
- explicit no-go conditions when relevant

### Architect Hat
Must contribute something concrete about:
- system-boundary fit
- scalability or resilience
- integration or migration impact
- long-term trade-off or lock-in

If a hat adds only generic filler, the output is not ready.

---

## Handbook map

### Core system
- [overview.md](overview.md)
- [advisory-mode.md](advisory-mode.md)
- [decision-mode.md](decision-mode.md)

### Hat frameworks
- [developer-hat.md](developer-hat.md)
- [security-hat.md](security-hat.md)
- [architect-hat.md](architect-hat.md)

### Cross-hat quality layers
- [synthesis.md](synthesis.md)
- [validation.md](validation.md)
- [anti-patterns.md](anti-patterns.md)
- [examples.md](examples.md)

### Index
- [reference.md](reference.md) — modular handbook index

---

## Maintainer guidance

When extending the package:
- keep `agents/multi-hat-system.md` compact and runtime-critical
- keep `SKILL.md` as the operator bridge and map
- split heavy handbook content into focused support files
- do not reintroduce prototype files as active dependencies
- do not create peer runtime agents for hats or modes

### Artifact taxonomy
- `agents/` = runtime authority
- `skills/` = operator bridge + modular handbook
- `design/changelog/TODO/phase/patch` = governance surfaces
- `prototype/` = archive/inspiration only

### Live-usage review loop
When reviewing the package in real usage, check:
- mode selection quality
- depth calibration quality
- whether each hat adds concrete value
- whether synthesis resolves the main tensions cleanly
- whether blocker vs follow-up judgment was explicit enough
- whether any missing active-package guidance should be added to the active package rather than pushed back into prototype dependency

### Future idea adoption rule
If a prototype-derived idea looks useful later, classify it before adoption as:
- migrated
- deferred
- intentionally not migrated

Do not promote prototype material directly into active authority without making that decision explicit.

---

## Front-door output guide

### Advisory output should make visible
- Task Summary
- the three hats on the same task
- one synthesized recommendation
- one short `Why this path` reason
- practical next steps

### Decision output should make visible
- Decision Context
- a small real option set
- cross-hat comparison
- one recommendation
- one short `Why this winner` reason
- what would flip the winner

### Clarify-first output should make visible
- current task understanding
- the exact missing high-impact constraint
- why it changes the answer
- focused clarifying questions
- bounded partial guidance if any is still safe

## Quality gate

Before accepting a response as good enough, confirm:
- correct mode selected
- proportional depth selected
- no task splitting into per-hat deliverables
- each hat contributed something concrete
- synthesis resolved the main tensions
- the response shape makes the active mode obvious
- the answer includes why this path or winner fits
- confidence level matches the certainty of the claims
- next steps are practical
- blocker/no-go language is used when warranted

---

## Boundary

- runtime authority lives in `../../agents/multi-hat-system.md`
- this skill is the active support surface
- this skill is not a competing runtime authority
- this skill should deepen and explain the active system, not replace it
- the linked markdown files in this directory are support files inside the same skill package, not separate skills
