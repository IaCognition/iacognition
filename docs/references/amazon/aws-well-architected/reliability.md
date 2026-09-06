# AWS Well-Architected — Reliability Analysis

## Source scope

This analysis covers the Reliability pillar of the AWS Well-Architected Framework, including foundations, workload architecture, change management, failure management, availability, and disaster recovery.

## AWS focus areas

AWS groups reliability guidance into:

- Foundations
- Workload architecture
- Change management
- Failure management

The pillar emphasizes explicit availability needs, service constraints, failure isolation, elasticity, automated recovery, recovery objectives, backup, recovery testing, and continuous reliability validation.

## Extracted concepts

### AWS-REL-001 — Define reliability objectives before architecture selection

**Disposition:** ADOPT

**Normalized concept:** Workloads MUST define required availability and recovery outcomes, including acceptable downtime and data-loss objectives where applicable, before a production architecture is selected.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `rules/reliability/`

### AWS-REL-002 — Identify platform constraints and quotas

**Disposition:** ADAPT

**Normalized concept:** Architecture MUST identify hard platform limits, quotas, capacity constraints, and dependency limits that can prevent normal operation, scaling, or recovery.

**Provider neutrality:** High; specific limits are provider-specific.

**Candidate destinations:** `schemas/architecture/`, provider-specific validation

### AWS-REL-003 — Isolate failures and limit blast radius

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD identify meaningful failure domains and use isolation boundaries appropriate to the required availability and cost profile.

**Provider neutrality:** High

**Candidate destinations:** `rules/reliability/`, `docs/architecture/reliability/`

### AWS-REL-004 — Design distributed interactions for failure

**Disposition:** ADOPT

**Normalized concept:** Distributed components SHOULD define behavior for dependency latency, unavailability, overload, retry, timeout, duplicate processing, and partial failure when those conditions are material to workload correctness.

**Provider neutrality:** High

**Candidate destinations:** `docs/architecture/reliability/`, `rules/reliability/`

### AWS-REL-005 — Scale capacity with demand

**Disposition:** ADAPT

**Normalized concept:** Workloads with variable demand SHOULD define how capacity changes with load and how overload is bounded when scaling cannot occur quickly enough.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `rules/reliability/`

### AWS-REL-006 — Automate recovery where safe and effective

**Disposition:** ADOPT

**Normalized concept:** Recovery actions that are well-understood, repeatable, and safely detectable SHOULD be automated to reduce recovery time and dependence on manual intervention.

**Provider neutrality:** High

**Candidate destinations:** `rules/reliability/`, `validation/`

### AWS-REL-007 — Test recovery procedures

**Disposition:** ADOPT

**Normalized concept:** Recovery mechanisms MUST be validated at a frequency and scope appropriate to workload criticality. A backup, failover path, or disaster-recovery design SHOULD NOT be considered effective solely because it is configured.

**Provider neutrality:** High

**Candidate destinations:** `validation/`, `docs/workflows/`

### AWS-REL-008 — Protect backup and recovery state from drift

**Disposition:** ADOPT

**Normalized concept:** Recovery environments, configuration, and backup data SHOULD be checked for integrity, recoverability, security, and configuration drift sufficient to meet stated recovery objectives.

**Provider neutrality:** High

**Candidate destinations:** `rules/reliability/`, `validation/`

## IaCognition implications

Reliability is one of the clearest examples of why architecture must precede Terraform. Multi-zone deployment, backup configuration, scaling, health checks, retries, and disaster-recovery resources cannot be evaluated as "correct" unless the workload's failure assumptions and required recovery outcomes are already explicit.
