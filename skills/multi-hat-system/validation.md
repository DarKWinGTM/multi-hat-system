# Validation

This file governs evidence strength, recommendation quality, and review readiness.

---

## Evidence and Validation Ladder

Use this when deciding how strongly to phrase conclusions.

### Level 1 — Established best practice
Use when the point is general and widely accepted.

### Level 2 — Strong contextual inference
Use when evidence is indirect but strong enough to guide a recommendation.

### Level 3 — Assumption requiring validation
Use when a recommendation depends on unknown environment details.

### Level 4 — Factual claim requiring verification
Use when a concrete technology, benchmark, security, compliance, or platform claim needs authoritative confirmation.

The system should avoid presenting Level 3 or Level 4 material as if it were Level 1 certainty.

---

## External Validation Lenses

Before making a strong claim, prefer verification through:
- official documentation
- mature standards bodies or guidance
- production-proven patterns
- credible benchmark or case-study evidence
- current project evidence when the claim is local

---

## Final Validation Lenses

Before finalizing a strong recommendation, check whether it still fits:
- technical reality
- business constraints
- team capability
- delivery timeline
- operational environment

---

## Recommendation Scorecard

Before finalizing a recommendation, pressure-test it against this scorecard:

| Lens | Key Question |
|---|---|
| Feasibility | Can the real team build and support this? |
| Security | Are the main risks controlled enough? |
| Architecture | Does it fit and scale cleanly enough? |
| Evidence | Is the confidence level honest? |
| Trade-off | Is the accepted downside explicit? |
| Operability | Can this be monitored, debugged, and rolled back? |

If multiple rows are weak, the recommendation is not ready.

---

## Practical Review Checklist

Before treating a response as good enough, confirm:
- Was the correct mode selected?
- Was the correct depth selected?
- Was the task or decision context restated clearly?
- Were key constraints and assumptions surfaced?
- Did each hat add something unique and useful?
- Were the main tensions identified?
- Did the answer end in one synthesized recommendation?
- Are the next steps practical?
- Is the confidence level honest enough for the claim strength?
- Were no-go or prerequisite conditions stated when warranted?
- Would the same task intent still map to the same mode even if the prompt language changed?
- Do the multilingual examples still preserve one-task / one-answer behavior rather than triggering accidental option sprawl?

---

## Review Disposition Guidance

Use this package-level review vocabulary when assessing live usage or future package changes:

### Severity
- `Blocking` = the package guidance is materially unsafe, misleading, or unusable until fixed
- `Follow-Up` = the package is usable, but a real gap should be recorded and closed later
- `None` = no meaningful gap was found for the checked scope

### Disposition
- `Must Fix Before Approval` = not acceptable to leave as-is
- `May Proceed With Follow-Up` = usable now, but record the gap explicitly
- `Approved As-Is` = no meaningful gap for the checked scope

### Practical blocker examples
- mode confusion that causes the wrong analytical pattern repeatedly
- generic hat filler with no real synthesis
- missing no-go guidance for clearly high-risk recommendations
- prototype-only material still required for current-system correctness

### Practical follow-up examples
- a worked example is missing but the active package still functions correctly
- one handbook section could be clearer, but operator use is still safe
- a deeper review rubric would help future maintenance, but current evaluation is still workable
