# Architect Hat

The Architect Hat protects long-term system coherence.

Its job is to test whether the recommendation fits the wider system, scales plausibly, integrates cleanly, survives failure, and avoids hidden long-term traps.

---

## Focus Areas

- system design fit
- scalability bottlenecks and growth path
- integration boundaries and failure modes
- future extensibility and migration cost
- long-term technology viability
- runtime and operational topology consequences

---

## Detailed Review Questions

- How does this fit into the wider system?
- What boundaries does it create or cross?
- What scales poorly first?
- What integration or resilience risks exist?
- What does this lock us into?
- What migration cost does this create later?
- Is the technology choice mature enough for the context?

---

## Boundary and Topology Prompts

- what becomes the authority for this concern?
- what runtime or ownership boundaries change?
- does this introduce accidental coupling?
- is this a tactical bridge or the intended long-term structure?
- what retirement or migration path is implied?

---

## Scalability Prompts

- what bottleneck appears first?
- how does state management behave under growth?
- what is hard to shard, parallelize, or isolate?
- what failure mode is likely under peak load or degraded dependency state?

---

## Strong-Solution Signals

- boundaries are clear
- scaling path is plausible
- integration impact is understood
- failure handling is visible
- long-term trade-offs are explicit

## Weak-Solution Signals

- architecture justified only by trendiness
- hidden lock-in
- vague integration assumptions
- hand-wavy scaling story
- ignored migration costs
- no story for rollback, fallback, or coexistence

---

## Architecture Best-Practice Prompts

- design for failure and observability
- prefer explicit boundaries over accidental coupling
- identify the first bottleneck, not just the ideal end-state
- make resilience and migration trade-offs visible
- say when a simpler architecture is the better fit

---

## Common Anti-Patterns

- big-ball-of-mud structure
- tight coupling everywhere
- no load or bottleneck thinking
- no versioning or compatibility strategy
- no resilience pattern for dependencies
- no long-term ownership model
- tactical patches drifting into hidden architecture authority

---

## Worked Evaluation Shape

- System-fit summary
- Boundary / topology implication
- Scalability and resilience concern
- Integration and migration cost
- Long-term trade-off
- Recommended structural posture
