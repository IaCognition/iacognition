# Extracted Principles — Google Cloud Guidance

This document identifies cross-cutting infrastructure-engineering principles derived from analysis of the Google Cloud Well-Architected Framework and Google Cloud Architecture Center.

Detailed analysis is maintained in the individual guidance files.

## GCP-X001 — Workload requirements drive architecture

Google consistently relates architecture decisions to workload, user, business, geographic, regulatory, operational, and technical requirements.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture decisions MUST be grounded in explicit workload requirements or explicit assumptions.

This directly supports:

- Architect before you code.
- Treat infrastructure requirements as explicit engineering inputs.
- Make assumptions explicit.

---

## GCP-X002 — Reliability should be measured from the workload perspective

Google's SRE-oriented guidance emphasizes service behavior and user-visible outcomes rather than infrastructure component uptime alone.

**Disposition:** ADAPT

**IaCognition normalization**

Reliability objectives SHOULD represent meaningful workload outcomes.

Infrastructure metrics SHOULD support those objectives rather than replace them.

---

## GCP-X003 — Architecture requires explicit tradeoffs

Google's framework repeatedly balances reliability, security, performance, cost, sustainability, and operational complexity.

**Disposition:** ADOPT

**IaCognition normalization**

Material architecture decisions SHOULD identify the quality attributes improved, degraded, or constrained by the decision.

---

## GCP-X004 — Observability is part of architecture

Google's Well-Architected and SRE guidance treats telemetry as foundational to reliability, performance, operations, security, and continuous improvement.

**Disposition:** ADOPT

**IaCognition normalization**

Production architectures SHOULD define the telemetry needed to determine health, failure, performance, and relevant operational state.

---

## GCP-X005 — Architecture evolves through operational evidence

Incident learning, production telemetry, performance data, and cost information are expected to drive continuous improvement.

**Disposition:** ADOPT

**IaCognition normalization**

Infrastructure architecture SHOULD be treated as a versioned engineering artifact that evolves through operation and review.

---

## GCP-X006 — Simplicity is preferable to speculative complexity

Google's design guidance encourages simple architectures and incremental evolution rather than premature overengineering.

**Disposition:** ADOPT

**IaCognition normalization**

Unnecessary infrastructure complexity SHOULD be treated as architectural debt.

---

## GCP-X007 — Automation should remove repeatable toil

Google SRE and operations guidance strongly favors automation for repeatable operational processes.

**Disposition:** ADAPT

**IaCognition normalization**

Deterministic repeatable infrastructure operations SHOULD be automated where automation improves safety, consistency, scalability, or efficiency.

Automation SHOULD remain observable and reviewable.

---

## GCP-X008 — Failure behavior should be designed explicitly

Reliability guidance emphasizes realistic targets, failure isolation, graceful degradation, recovery, and testing.

**Disposition:** ADOPT

**IaCognition normalization**

Production architectures SHOULD define expected behavior under material failure scenarios before implementation.

---

## GCP-X009 — Security requires explicit identity and trust boundaries

Google emphasizes Zero Trust, least privilege, layered defenses, data protection, and continuous validation.

**Disposition:** ADOPT

**IaCognition normalization**

Security architecture SHOULD explicitly define identity, trust boundaries, sensitive data, exposure, privilege, and validation expectations.

---

## GCP-X010 — Cost optimization is value optimization

Google frames cost optimization around business value rather than minimum expenditure.

**Disposition:** ADOPT

**IaCognition normalization**

Cost SHOULD be evaluated against workload value and architecture requirements rather than optimized independently.

---

## GCP-X011 — Performance requires measurable objectives and evidence

Google's performance guidance emphasizes workload-specific objectives, representative testing, capacity planning, elasticity, and ongoing measurement.

**Disposition:** ADOPT

**IaCognition normalization**

Performance-sensitive architectures SHOULD define measurable targets and validation methods.

---

## GCP-X012 — Sustainability can be a first-class architecture quality

Google now treats sustainability as a full Well-Architected pillar.

**Disposition:** ADOPT

**IaCognition normalization**

Where material, sustainability SHOULD be modeled as an explicit quality attribute with measurable objectives and documented tradeoffs.

---

## GCP-X013 — Deployment topology is an architectural decision

Google's deployment archetypes explicitly relate topology to availability, geography, latency, cost, complexity, and regulation.

**Disposition:** ADOPT

**IaCognition normalization**

Deployment topology SHOULD be selected from workload requirements rather than implicitly determined by implementation defaults.

---

## GCP-X014 — Reference architectures are contextual

Google's Architecture Center demonstrates specific ways to implement architecture goals for defined scenarios.

**Disposition:** ADOPT

**IaCognition normalization**

Reference architectures SHOULD declare assumptions and applicability constraints.

Agents MUST NOT copy them without comparing those assumptions to the target workload.

---

## GCP-X015 — Hybrid and multicloud are legitimate architecture contexts

Google explicitly applies its framework to hybrid and multicloud workloads.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD support provider-neutral architecture reasoning across cloud, hybrid, and multicloud boundaries.

## Overall assessment

Google Cloud guidance strongly aligns with IaCognition's architecture-first model.

The highest-value provider-neutral concepts are:

1. requirement-driven architecture;
2. measurable service and reliability objectives;
3. explicit tradeoffs;
4. observability as architecture;
5. operational learning and continuous improvement;
6. failure-domain and recovery reasoning;
7. Zero Trust and least privilege;
8. cost/value optimization;
9. workload-specific performance engineering;
10. sustainability as a quality attribute;
11. deployment topology as a deliberate architecture choice;
12. contextual patterns and reference architectures.

These concepts are candidates for cross-normalization with the existing AWS and Microsoft guidance before promotion into canonical IaCognition rules.
