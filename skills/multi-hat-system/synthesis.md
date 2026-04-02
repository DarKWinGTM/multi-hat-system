# Synthesis

Synthesis is where the multi-hat system becomes useful.

A good result should read like one coherent recommendation, not three disconnected mini-reports.

---

## Synthesis Protocol

After hat analysis, always:
1. identify where the hats align
2. identify where the hats disagree
3. decide which tensions matter most
4. resolve those tensions into one recommendation
5. state the accepted trade-off
6. give practical next steps or implementation phases
7. say when a different choice would win under different constraints

---

## Strong Synthesis Should

- identify the decisive tension
- explain why one concern wins over another
- state blocker or no-go conditions plainly
- keep the user on one practical path
- make flip conditions visible when relevant

---

## Weak Synthesis Usually Looks Like

- three stacked reports with no connection
- vague balance language
- no explicit trade-off
- no practical next step
- “it depends” without saying what it depends on

---

## Cross-Hat Tension Patterns

### Delivery speed vs security hardening
- Developer may optimize for fast implementation
- Security may require stronger controls before release
- Architect may care about whether the controls should be centralized or embedded

### Short-term simplicity vs long-term scalability
- Developer may prefer the simplest path
- Architect may see scaling bottlenecks early
- Security may see higher risk concentration in the simpler path

### Ecosystem maturity vs architectural elegance
- Developer may value tooling and team readiness
- Architect may prefer a cleaner theoretical design
- Security may prefer the stack with better operational maturity and auditability

### Compliance burden vs developer velocity
- Security may require stricter controls and evidence
- Developer may see large delivery slowdown
- Architect must weigh whether those controls should be centralized to reduce repeated burden

### Tactical unblock vs strategic drift
- Developer may want the fastest unblock
- Architect may see that the shortcut is becoming hidden long-term authority
- Security may see the temporary path weakening controls or auditability

### Runtime clarity vs additive expansion
- Developer may suggest adding another moving part quickly
- Architect may object to topology drift or duplicate authorities
- Security may see new attack surface and monitoring burden

A good synthesis should make these tensions explicit and resolve them, not bury them.
