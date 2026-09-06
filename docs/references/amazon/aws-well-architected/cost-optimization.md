# AWS Well-Architected — Cost Optimization Analysis

## Source scope

This analysis covers the Cost Optimization pillar of the AWS Well-Architected Framework.

## AWS focus areas

AWS guidance includes:

- Cloud Financial Management;
- expenditure and usage awareness;
- cost-effective resources;
- managing demand and supply;
- optimization over time.

The pillar treats cost as an engineering and organizational responsibility tied to business value rather than as a one-time procurement exercise.

## Extracted concepts

### AWS-COST-001 — Establish cost ownership

**Disposition:** ADAPT

**Normalized concept:** Material workloads SHOULD have explicit ownership for understanding, reviewing, and acting on infrastructure cost relative to delivered business value.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, future cost rules

### AWS-COST-002 — Make cost visible and attributable

**Disposition:** ADAPT

**Normalized concept:** Infrastructure expenditure SHOULD be measurable and attributable at a level that permits meaningful engineering and business decisions.

**Provider neutrality:** High

**Candidate destinations:** future cost validation and standards

### AWS-COST-003 — Align resource supply with actual demand

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD provision capacity according to required demand, resilience, and performance rather than static maximum assumptions when more adaptive approaches are practical.

**Provider neutrality:** High

**Candidate destinations:** `rules/architecture/`, future cost rules

### AWS-COST-004 — Evaluate total architectural cost, not only unit price

**Disposition:** ADAPT

**Normalized concept:** Architecture decisions SHOULD consider infrastructure charges together with operational effort, reliability implications, performance, licensing, data movement, and lifecycle costs relevant to the decision.

**Provider neutrality:** High

**Candidate destinations:** `schemas/architecture/`, `docs/architecture/`

### AWS-COST-005 — Use economic constraints as architecture inputs

**Disposition:** ADOPT

**Normalized concept:** Cost objectives and material budget constraints SHOULD be explicit workload inputs rather than discovered only after implementation.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`

### AWS-COST-006 — Review cost efficiency continuously

**Disposition:** ADOPT

**Normalized concept:** Cost efficiency SHOULD be re-evaluated as utilization, pricing, workload requirements, and platform capabilities change.

**Provider neutrality:** High

**Candidate destinations:** `docs/workflows/`, `schemas/review/`

### AWS-COST-007 — Consider the cost of engineering effort

**Disposition:** ADOPT

**Normalized concept:** Optimization work SHOULD consider both expected infrastructure savings and the engineering effort, operational complexity, and risk required to realize and maintain those savings.

**Provider neutrality:** High

**Candidate destinations:** future cost guidance

### AWS-COST-008 — Automate recurring cost controls where practical

**Disposition:** ADOPT

**Normalized concept:** Repetitive cost-management actions such as scheduling, cleanup, scaling, anomaly detection, or policy enforcement SHOULD be automated when doing so is reliable and proportionate to workload risk.

**Provider neutrality:** High

**Candidate destinations:** future cost rules, `rules/operations/`

## IaCognition implications

Cost belongs in SPECIFY and ARCHITECT, not only REVIEW. An agent choosing infrastructure without cost objectives, expected usage patterns, and business constraints is making an architectural decision with missing inputs.
