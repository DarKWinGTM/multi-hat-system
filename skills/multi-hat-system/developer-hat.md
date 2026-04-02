# Developer Hat

The Developer Hat protects implementation reality.

Its job is to test whether the recommendation is actually buildable, operable, debuggable, and maintainable by the real team in the real environment.

---

## Focus Areas

- implementation feasibility
- complexity and effort
- maintainability and testability
- debugging and observability needs
- timeline and team-readiness impact
- performance implications
- dependency and tooling burden

---

## Detailed Review Questions

- Can the current team realistically build this?
- What new dependencies or skills are required?
- What are the likely blockers?
- How testable will this be?
- What debugging or monitoring support will be needed?
- How much technical debt does this create or reduce?
- What is the likely timeline including testing and integration?
- What breaks first if the implementation is rushed?

---

## Feasibility Checklist

- stack fit is credible
- dependency burden is acceptable
- local development path is clear
- testing path is practical
- failure modes are understandable
- rollout and support burden are reasonable

---

## Performance and Delivery Lenses

- CPU / memory / IO cost
- latency sensitivity
- concurrency model
- caching opportunities
- failure recovery behavior
- instrumentation needed to troubleshoot production issues

---

## Strong-Solution Signals

- implementation path is clear
- effort is proportional to value
- testability is practical
- operational debugging is possible
- maintenance burden stays reasonable
- team fit is credible

## Weak-Solution Signals

- hidden complexity
- unrealistic delivery assumptions
- opaque failure modes
- fragile implementation path
- hard-to-test behavior
- avoidable technical debt
- a lot of “we’ll clean it up later” language

---

## Best-Practice Prompts

- profile before optimizing
- prefer simple, understandable designs first
- document important implementation constraints
- plan observability with the implementation, not after it
- flag blockers explicitly instead of smoothing them into optimism
- use phased delivery when the full target is too risky to land at once

---

## Common Anti-Patterns

- over-engineering
- under-engineering
- ignoring team capability constraints
- skipping tests
- poor error handling
- hard-coding values or assumptions
- shipping opaque code paths with no monitoring

---

## Worked Evaluation Shape

- Implementation shape
- Complexity / effort
- Hidden blockers
- Testing / observability needs
- Delivery risk
- Maintainability implication
