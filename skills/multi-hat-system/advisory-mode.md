# Advisory Mode

Use Advisory Mode when the user already has a defined task.

Examples:
- "Build an API for orders"
- "Improve authentication"
- "Design a migration plan"
- "How should I implement X?"

---

## Core Goal

Improve the **same task** from three perspectives and end with **one clear path forward**.

Advisory Mode is not a weak version of comparison mode.
It should not explode into A/B/C branches unless the user explicitly asks for comparison.

---

## Advisory Process

1. Restate the task and intended outcome.
2. Extract constraints, assumptions, and unknowns.
3. Decide whether to proceed or clarify first.
4. Analyze the same task through Developer, Security, and Architect hats.
5. Surface the main tensions, dependencies, blockers, and sequencing needs.
6. Recommend one path.
7. Give practical next steps.

---

## Framing Questions

- What exactly is the user trying to achieve?
- What matters most: speed, safety, scale, cost, maintainability, or reversibility?
- What hidden prerequisites could make the obvious answer wrong?
- What would make this recommendation unsafe or premature?

---

## Strong Advisory Moves

- identify implementation order, not just design preference
- state blocker conditions plainly
- point out where “simple now” becomes “painful later”
- explain why the recommended path is better than the tempting shortcut
- say when prerequisite work should happen first

---

## Good Advisory Output Should Show

- one clear path forward
- concrete hat-specific insights
- explicit assumptions where uncertainty remains
- tensions resolved into one recommendation
- practical next steps rather than generic encouragement

---

## Advisory Anti-Patterns

- generating options by default
- treating one task as three separate subprojects
- giving three parallel sections with no synthesis
- hiding uncertainty under generic “best practice” language
- using comparison machinery when comparison was not requested
