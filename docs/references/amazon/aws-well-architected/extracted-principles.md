# AWS Well-Architected — Cross-Cutting Extracted Principles

This document synthesizes cross-cutting infrastructure-engineering concepts extracted from the AWS Well-Architected Framework. Detailed pillar-specific analysis is maintained in the individual pillar files in this directory.

These concepts are inputs to IaCognition. They are not canonical IaCognition requirements until separately incorporated into the appropriate framework artifacts.

## AWS-WAF-X001 — Workload requirements drive architecture

**Disposition:** ADOPT

AWS treats architecture as a set of decisions made in the context of a workload's business purpose, requirements, and operating environment. IaCognition should preserve this relationship: architecture must be derived from explicit workload intent rather than inferred from the IaC implementation.

**Normalized concept:** Infrastructure architecture SHOULD be derived from explicit workload requirements, constraints, quality attributes, and business priorities before implementation choices are made.

**Candidate destinations:**

- `schemas/workload/`
- `docs/principles/`
- `docs/architecture/`

## AWS-WAF-X002 — Architecture requires explicit tradeoffs

**Disposition:** ADOPT

AWS explicitly recognizes tradeoffs among quality attributes such as reliability, performance, and cost. IaCognition should require material tradeoffs to be visible rather than embedded implicitly in resource choices.

**Normalized concept:** Material architectural tradeoffs SHOULD identify the competing qualities, decision rationale, accepted risk, and conditions that would cause the decision to be revisited.

**Candidate destinations:**

- `schemas/architecture/`
- `docs/architecture/`
- `rules/architecture/`

## AWS-WAF-X003 — Architecture should be continuously reviewed

**Disposition:** ADOPT

AWS presents architecture review as a lightweight, repeatable activity rather than a one-time audit. This aligns with IaCognition's REVIEW and OPERATE lifecycle stages.

**Normalized concept:** Architecture SHOULD be re-evaluated when workload requirements, scale, dependencies, risks, or operating conditions materially change.

**Candidate destinations:**

- `docs/workflows/`
- `validation/`
- `schemas/review/`

## AWS-WAF-X004 — Automation is an architectural capability

**Disposition:** ADOPT

Automation appears across operations, security, recovery, performance, cost, and sustainability guidance. It is not merely an implementation convenience.

**Normalized concept:** Repetitive, failure-sensitive, or scale-sensitive infrastructure operations SHOULD be candidates for deterministic automation, with controls appropriate to the risk of the operation.

**Candidate destinations:**

- `rules/operations/`
- `rules/reliability/`
- `rules/security/`
- `docs/principles/`

## AWS-WAF-X005 — Measure business-relevant outcomes

**Disposition:** ADAPT

AWS frequently connects metrics to business outcomes and workload health rather than relying only on low-level resource telemetry.

**Normalized concept:** Workloads SHOULD define measurable indicators that connect infrastructure behavior to user-visible or business-relevant outcomes, supplemented by component-level telemetry needed for diagnosis.

**Candidate destinations:**

- `schemas/workload/`
- `docs/architecture/observability/`
- `validation/`

## AWS-WAF-X006 — Design for change and evolution

**Disposition:** ADOPT

AWS repeatedly emphasizes small reversible changes, evolving services, changing demand, changing technologies, and iterative improvement.

**Normalized concept:** Infrastructure architectures SHOULD be designed for controlled evolution, including safe change mechanisms, observable outcomes, and the ability to reverse or remediate harmful changes.

**Candidate destinations:**

- `docs/principles/`
- `rules/operations/`
- `validation/`

## AWS-WAF-X007 — Failure must be assumed, bounded, and tested

**Disposition:** ADOPT

Failure anticipation, fault isolation, automated recovery, recovery testing, game days, and disaster recovery appear across Reliability and Operational Excellence.

**Normalized concept:** Workloads MUST identify material failure scenarios and required recovery outcomes before architecture is considered production-ready. Recovery mechanisms SHOULD be tested rather than assumed.

**Candidate destinations:**

- `schemas/workload/`
- `rules/reliability/`
- `validation/`

## AWS-WAF-X008 — Organizational ownership is part of architecture

**Disposition:** ADAPT

AWS treats ownership, governance, operational capability, security responsibility, and cost management as architectural enablers. IaCognition should capture ownership without prescribing AWS's preferred organizational model.

**Normalized concept:** Material infrastructure capabilities SHOULD have explicit ownership for design, operation, security, cost, and lifecycle responsibilities.

**Candidate destinations:**

- `schemas/workload/`
- `schemas/architecture/`
- `docs/standards/`

## AWS-WAF-X009 — Prefer evidence over intuition

**Disposition:** ADOPT

Benchmarking, load testing, recovery exercises, monitoring, cost measurement, and review evidence are recurring themes.

**Normalized concept:** Architecture decisions SHOULD be supported by observable or testable evidence when evidence can reasonably be obtained.

**Candidate destinations:**

- `docs/principles/`
- `validation/`
- `schemas/review/`

## AWS-WAF-X010 — Optimize the whole lifecycle, not only initial deployment

**Disposition:** ADOPT

AWS guidance considers design, implementation, operation, incident response, maintenance, review, and improvement. IaCognition should likewise avoid treating a successful Terraform apply as completion.

**Normalized concept:** Infrastructure quality MUST be evaluated across implementation, operation, change, failure, recovery, and retirement—not only at provisioning time.

**Candidate destinations:**

- `docs/principles/iacognition-lifecycle.md`
- `validation/`
- `docs/workflows/`

## AWS-WAF-X011 — Provider capabilities are implementation choices, not universal principles

**Disposition:** ADAPT

AWS often recommends AWS managed services or AWS-specific mechanisms. The underlying reasons—reducing undifferentiated operational work, increasing automation, improving scaling, or reducing risk—can be provider-neutral even when the implementation is not.

**Normalized concept:** IaCognition SHOULD separate an architectural objective from a provider-specific mechanism used to satisfy it.

**Candidate destinations:**

- `docs/principles/`
- `docs/architecture/`
- provider-specific reference guidance

## AWS-WAF-X012 — Resource efficiency spans cost, performance, and sustainability

**Disposition:** ADOPT

AWS's cost, performance, and sustainability guidance overlap around right-sizing, demand alignment, utilization, and avoiding waste.

**Normalized concept:** Capacity and resource choices SHOULD be evaluated jointly for required performance, resilience, cost, and resource efficiency rather than optimized independently.

**Candidate destinations:**

- `schemas/architecture/`
- `rules/architecture/`
- `rules/reliability/`
- future cost and sustainability rules

## Cross-pillar implication for IaCognition

AWS Well-Architected supports IaCognition's core premise that infrastructure code is downstream of architecture. The strongest provider-neutral contribution is not any individual AWS best practice; it is the repeated requirement to reason about workload intent, tradeoffs, failure, security, operations, measurement, cost, and evolution as a coherent system before and after infrastructure is provisioned.
