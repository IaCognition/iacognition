# AWS Well-Architected — Operational Excellence Analysis

## Source scope

This analysis covers the Operational Excellence pillar of the AWS Well-Architected Framework, including organization, preparation, operation, evolution, and design-for-operations guidance.

## AWS focus areas

AWS organizes Operational Excellence around four broad areas:

- Organization
- Prepare
- Operate
- Evolve

The pillar emphasizes operations as an engineering discipline, explicit priorities and ownership, operational readiness, automation, observable workloads, small reversible changes, learning from events, and continuous improvement.

## Extracted concepts

### AWS-OE-001 — Treat operations as code

**Disposition:** ADOPT

**Normalized concept:** Repeatable infrastructure and operational procedures SHOULD be represented in versioned, testable, automatable forms where practical. Human-only procedures SHOULD be reserved for decisions or activities that cannot be safely automated.

**Provider neutrality:** High

**Candidate destinations:** `rules/operations/`, `docs/principles/`

### AWS-OE-002 — Make changes small and reversible

**Disposition:** ADOPT

**Normalized concept:** Infrastructure change mechanisms SHOULD minimize blast radius and provide a defined reversal, rollback, or forward-remediation strategy appropriate to the risk of the change.

**Provider neutrality:** High

**Candidate destinations:** `rules/operations/`, `validation/`

### AWS-OE-003 — Validate operational readiness before production

**Disposition:** ADOPT

**Normalized concept:** Production readiness MUST include evaluation of operational risks, monitoring, support procedures, ownership, recovery procedures, and known unresolved risks—not only successful deployment.

**Provider neutrality:** High

**Candidate destinations:** `schemas/review/`, `validation/`, `docs/workflows/`

### AWS-OE-004 — Define ownership and decision responsibility

**Disposition:** ADAPT

AWS includes organizational operating-model guidance. IaCognition should preserve the requirement for clear ownership without prescribing a specific centralized or decentralized structure.

**Normalized concept:** Workloads SHOULD identify accountable ownership for architecture, operation, security, cost, and incident response responsibilities.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `docs/standards/`

### AWS-OE-005 — Anticipate operational failure

**Disposition:** ADOPT

**Normalized concept:** Teams SHOULD identify credible operational failure scenarios before production and verify that procedures, automation, telemetry, and personnel can respond effectively.

**Provider neutrality:** High

**Candidate destinations:** `rules/reliability/`, `validation/`

### AWS-OE-006 — Use business and operational telemetry as a feedback loop

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD emit telemetry sufficient to understand both technical condition and whether the workload is meeting intended outcomes.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `docs/architecture/observability/`

### AWS-OE-007 — Continuously improve procedures and architecture

**Disposition:** ADOPT

**Normalized concept:** Operational procedures and infrastructure architecture SHOULD be revised using evidence from incidents, metrics, changes, and operational experience.

**Provider neutrality:** High

**Candidate destinations:** `docs/workflows/`, `schemas/review/`

### AWS-OE-008 — Use managed capabilities to reduce undifferentiated operations

**Disposition:** ADAPT

AWS recommends managed services where appropriate. IaCognition should capture the tradeoff rather than universally prefer managed services.

**Normalized concept:** Architecture decisions SHOULD evaluate whether a managed capability reduces operational risk and effort enough to justify its cost, constraints, portability implications, and provider dependency.

**Provider neutrality:** High at the decision level; implementation is provider-specific.

**Candidate destinations:** `docs/architecture/`, `schemas/architecture/`

## IaCognition implications

Operational Excellence strongly reinforces IaCognition's OPERATE feedback loop. Infrastructure generation should not be considered complete until the design includes ownership, telemetry, safe change mechanisms, operational readiness, failure response, and a path for continuous improvement.
