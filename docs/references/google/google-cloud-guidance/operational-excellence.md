# Google Cloud Well-Architected — Operational Excellence Analysis

## Source scope

This analysis covers the Operational Excellence pillar of the Google Cloud Well-Architected Framework and related Google Cloud operational guidance.

Google emphasizes operational readiness, incident management, change management, automation, resource optimization, observability, and continuous improvement.

## Extracted concepts

### GCP-OPS-001 — Operational readiness precedes production

**Source concept**

A workload should be operationally ready before it is treated as production-ready.

**Disposition:** ADOPT

**IaCognition normalization**

Production readiness SHOULD include explicit operational criteria in addition to successful deployment.

Criteria MAY include:

- monitoring and alerting;
- incident ownership;
- recovery procedures;
- deployment and rollback procedures;
- maintenance processes;
- capacity expectations;
- escalation paths.

**Provider neutrality:** High

---

### GCP-OPS-002 — Operations require explicit ownership

**Source concept**

Operational responsibilities should be known and actionable.

**Disposition:** ADOPT

**IaCognition normalization**

Production infrastructure SHOULD identify ownership for:

- routine operation;
- changes;
- incidents;
- maintenance;
- lifecycle decisions.

**Provider neutrality:** High

---

### GCP-OPS-003 — Define service objectives

**Source concept**

Google's SRE-oriented guidance emphasizes measurable service objectives and operating expectations.

**Disposition:** ADAPT

**IaCognition normalization**

Material workloads SHOULD define measurable service objectives where availability, latency, throughput, or correctness materially affect business outcomes.

Operational review SHOULD compare observed behavior against those objectives.

**Provider neutrality:** High

---

### GCP-OPS-004 — Observability is foundational

**Source concept**

Monitoring and telemetry are required to understand workload behavior, failures, and user impact.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture SHOULD define the telemetry required to determine:

- workload health;
- critical-flow status;
- failure conditions;
- performance behavior;
- operational state.

Observability SHOULD be designed before deployment rather than added only after incidents.

**Provider neutrality:** High

---

### GCP-OPS-005 — Incident management is an engineering capability

**Source concept**

Google treats incident detection, coordination, mitigation, communication, and learning as part of operational excellence.

**Disposition:** ADOPT

**IaCognition normalization**

Production workloads SHOULD define incident-response expectations proportional to their criticality.

**Provider neutrality:** High

---

### GCP-OPS-006 — Changes should be controlled and reversible

**Source concept**

Change management should reduce production risk through testing, review, staged rollout, and rollback capabilities.

**Disposition:** ADOPT

**IaCognition normalization**

Material infrastructure changes SHOULD be reviewable before production application.

High-risk changes SHOULD support rollback, replacement, or another controlled recovery mechanism where practical.

**Provider neutrality:** High

---

### GCP-OPS-007 — Automate repeatable operations

**Source concept**

Automation reduces inconsistency and operational toil.

**Disposition:** ADOPT

**IaCognition normalization**

Repeatable deterministic operations SHOULD be automated when doing so improves consistency, safety, scalability, or recovery.

Automation SHOULD be observable and appropriately controlled.

**Provider neutrality:** High

---

### GCP-OPS-008 — Reduce operational toil

**Source concept**

Google SRE practices distinguish engineering work from repetitive manual operational effort.

**Disposition:** ADOPT

**IaCognition normalization**

Recurring manual infrastructure work SHOULD be evaluated as potential operational debt.

Where practical, toil SHOULD be removed through simplification, automation, or architectural change.

**Provider neutrality:** High

---

### GCP-OPS-009 — Learn from incidents and operations

**Source concept**

Post-incident analysis and production telemetry should feed continuous improvement.

**Disposition:** ADOPT

**IaCognition normalization**

Material incidents SHOULD produce candidate improvements to architecture, automation, validation, documentation, or operating procedures.

Operational evidence SHOULD be allowed to invalidate earlier architecture assumptions.

**Provider neutrality:** High

## Cross-pillar considerations

Operational excellence supports reliability, security, cost, performance, and sustainability by making infrastructure behavior measurable and manageable.

IaCognition SHOULD treat operations as an architecture concern rather than a post-deployment activity.
