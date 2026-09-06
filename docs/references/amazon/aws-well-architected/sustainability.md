# AWS Well-Architected — Sustainability Analysis

## Source scope

This analysis covers the Sustainability pillar of the AWS Well-Architected Framework. AWS's pillar is focused primarily on environmental sustainability, especially resource and energy efficiency.

## AWS focus areas

AWS guidance covers:

- region selection;
- alignment to demand;
- software and architecture;
- data management;
- hardware and services;
- process and culture;
- continuous improvement and measurement.

## Extracted concepts

### AWS-SUS-001 — Treat sustainability as a non-functional requirement

**Disposition:** ADAPT

**Normalized concept:** Where sustainability is material to organizational or workload goals, the workload SHOULD define measurable sustainability objectives as architecture inputs rather than treating resource efficiency as an accidental by-product.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, future sustainability rules

### AWS-SUS-002 — Measure impact relative to useful work

**Disposition:** ADAPT

**Normalized concept:** Resource-efficiency metrics SHOULD relate consumption to useful workload output where practical, rather than relying only on absolute resource consumption.

**Provider neutrality:** High

**Candidate destinations:** future sustainability validation

### AWS-SUS-003 — Minimize unnecessary resource consumption

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD avoid persistent idle, redundant, or over-provisioned resources that do not materially contribute to required performance, resilience, security, or business outcomes.

**Provider neutrality:** High

**Candidate destinations:** `rules/architecture/`, future sustainability rules

### AWS-SUS-004 — Align capacity with demand

**Disposition:** ADOPT

**Normalized concept:** Resource consumption SHOULD scale with workload demand where doing so does not violate required reliability, latency, or recovery objectives.

**Provider neutrality:** High

**Candidate destinations:** `rules/architecture/`

### AWS-SUS-005 — Consider data lifecycle and movement

**Disposition:** ADOPT

**Normalized concept:** Architecture SHOULD evaluate whether retained, replicated, transferred, or backed-up data provides required value relative to its storage, processing, network, cost, and recovery implications.

**Provider neutrality:** High

**Candidate destinations:** `docs/architecture/data/`, future sustainability rules

### AWS-SUS-006 — Prefer efficient execution mechanisms when requirements permit

**Disposition:** ADAPT

AWS includes guidance on hardware choices, accelerators, managed services, and efficient platforms. IaCognition should express this as a workload-driven efficiency decision rather than a provider-specific recommendation.

**Normalized concept:** Compute mechanisms SHOULD be selected using required performance, utilization, energy/resource efficiency, operational complexity, cost, and portability as explicit tradeoffs.

**Provider neutrality:** High at the decision level.

**Candidate destinations:** `schemas/architecture/`, future sustainability guidance

### AWS-SUS-007 — Include lifecycle effects

**Disposition:** ADAPT

**Normalized concept:** Sustainability and resource-efficiency analysis SHOULD consider build, test, production, data retention, backup, and retirement behavior when those lifecycle stages materially affect consumption.

**Provider neutrality:** High

**Candidate destinations:** `docs/principles/`, future sustainability guidance

### AWS-SUS-008 — Improve incrementally using measurement

**Disposition:** ADOPT

**Normalized concept:** Sustainability improvements SHOULD be prioritized, tested, measured, and iterated rather than based solely on assumptions about which changes reduce resource impact.

**Provider neutrality:** High

**Candidate destinations:** `docs/workflows/`, future sustainability validation

## IaCognition implications

The sustainability pillar exposes an important overlap among performance, cost, and resource utilization. IaCognition should avoid creating independent optimizers that recommend contradictory choices. Resource efficiency should be evaluated together with reliability, security, performance, cost, and business requirements.
