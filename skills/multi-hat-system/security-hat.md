# Security Hat

The Security Hat protects the system from unsafe optimism.

Its job is to identify threats, control requirements, compliance implications, data-protection needs, and the conditions under which the answer should become a no-go.

---

## Focus Areas

- threat model and attack surface
- vulnerability exposure
- control requirements
- data protection and logging
- compliance and audit implications
- abuse resistance and failure containment

---

## Detailed Review Questions

- What could go wrong from a security perspective?
- What are the highest-risk failure modes?
- What are the critical controls required before this is acceptable?
- What data protection requirements apply?
- What logging and auditability are necessary?
- What compliance or policy constraints matter?
- What risk level would justify a no-go recommendation?

---

## Threat-Model Prompts

Use structured prompts such as:
- spoofing / identity abuse
- tampering / integrity risk
- repudiation / auditability gap
- information disclosure
- denial of service / resource exhaustion
- privilege escalation

---

## Control Classes

### Preventive controls
- authn/authz
- validation and input handling
- encryption and secret handling
- least privilege
- segmentation and isolation

### Detective controls
- audit logs
- anomaly detection
- security event visibility
- monitoring and alerting

### Corrective controls
- incident response hooks
- rollback / key rotation / revocation
- containment and recovery playbooks

---

## Strong-Solution Signals

- critical risks are identified early
- controls are concrete
- logging and auditability are explicit
- sensitive data paths are clear
- compliance impact is not hand-waved

## Weak-Solution Signals

- “secure it later” language
- no concrete controls
- no logging or audit plan
- hidden compliance assumptions
- vague treatment of sensitive data
- lack of abuse-rate or misuse thinking

---

## Security Best-Practice Prompts

- define the top threat actors and attack surfaces
- map the minimum preventive, detective, and corrective controls
- name high-risk no-go conditions explicitly
- make compliance obligations concrete, not generic
- state what evidence would be needed for stronger certainty

---

## Common Anti-Patterns

- client-side-only authorization logic
- hard-coded secrets
- weak or absent encryption strategy
- unbounded sensitive data retention
- no monitoring of security-relevant events
- treating auditability as optional
- confusing “works” with “safe enough to operate”

---

## Worked Evaluation Shape

- Top threats
- Essential controls
- Compliance / policy burden
- Sensitive data path concerns
- Logging / audit requirements
- Explicit no-go conditions
