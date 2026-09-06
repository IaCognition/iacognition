# Google Cloud Guidance Incorporation Map

This document tracks the proposed disposition and future IaCognition destination of concepts extracted from the Google Cloud Well-Architected Framework and Google Cloud Architecture Center.

## Status meaning

- **Proposed** — extracted and normalized but not yet incorporated into canonical IaCognition guidance.
- **Incorporated** — represented in canonical IaCognition artifacts.
- **Rejected** — reviewed and deliberately not incorporated.
- **Superseded** — replaced by a later normalized concept or stronger source synthesis.

At the time of this ingestion, all concepts below are **Proposed**.

## Cross-cutting concepts

| Concept | Disposition | Candidate IaCognition destination | Status |
|---|---|---|---|
| Workload requirements drive architecture | ADOPT | `docs/principles/`, `schemas/workload/`, `rules/architecture/` | Proposed |
| Reliability should reflect workload outcomes | ADAPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Architecture requires explicit tradeoffs | ADOPT | `schemas/architecture/`, `docs/architecture/` | Proposed |
| Observability is part of architecture | ADOPT | `schemas/architecture/`, `rules/operations/` | Proposed |
| Operational evidence should evolve architecture | ADOPT | `docs/workflows/`, `rules/operations/` | Proposed |
| Simplicity is preferable to speculative complexity | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |
| Automation should reduce deterministic toil | ADAPT | `rules/operations/`, `validation/` | Proposed |
| Deployment topology is an architecture decision | ADOPT | `schemas/architecture/`, `docs/patterns/` | Proposed |
| Hybrid and multicloud are valid architecture contexts | ADOPT | `schemas/workload/`, `docs/architecture/` | Proposed |

## Operational Excellence concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Operational readiness precedes production | ADOPT | `schemas/review/`, `rules/operations/` | Proposed |
| Production ownership must be explicit | ADOPT | `schemas/architecture/`, `rules/operations/` | Proposed |
| Service objectives should be measurable | ADAPT | `schemas/workload/`, `rules/operations/` | Proposed |
| Incident management is an engineering capability | ADOPT | `docs/workflows/`, `rules/operations/` | Proposed |
| Changes should be controlled and reversible | ADOPT | `validation/`, `rules/operations/` | Proposed |
| Operational toil should be reduced | ADOPT | `rules/operations/` | Proposed |

## Security concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Security is an architecture input | ADOPT | `schemas/workload/`, `rules/security/` | Proposed |
| Use explicit identity and authorization | ADAPT | `rules/security/` | Proposed |
| Least privilege | ADOPT | `rules/security/` | Proposed |
| Defense in depth | ADOPT | `rules/security/`, `docs/architecture/security/` | Proposed |
| Limit blast radius | ADOPT | `rules/security/`, `schemas/architecture/` | Proposed |
| Data controls derive from sensitivity | ADOPT | `schemas/workload/`, `rules/security/` | Proposed |
| Security posture requires continuous validation | ADOPT | `validation/`, `rules/security/` | Proposed |
| Supply-chain security affects IaC delivery | ADAPT | `validation/`, `rules/security/` | Proposed |

## Reliability concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Reliability objectives should be user-focused | ADAPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Reliability targets should be realistic | ADOPT | `schemas/workload/` | Proposed |
| Failure domains should drive topology | ADOPT | `schemas/architecture/`, `rules/reliability/` | Proposed |
| Replica count alone does not prove resilience | ADOPT | `rules/reliability/`, `validation/` | Proposed |
| Graceful degradation can preserve workload value | ADOPT | `docs/patterns/`, `rules/reliability/` | Proposed |
| Stateful workloads require recovery objectives | ADOPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Recovery requires testing | ADOPT | `validation/`, `rules/reliability/` | Proposed |

## Cost concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Cost aligns with business value | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |
| Cost is an architecture input | ADOPT | `schemas/workload/` | Proposed |
| Cost drivers should be explicit | ADOPT | `schemas/workload/`, `validation/` | Proposed |
| Capacity should be right-sized | ADOPT | `rules/architecture/` | Proposed |
| Elasticity can reduce waste | ADOPT | `docs/patterns/`, `rules/architecture/` | Proposed |
| Cost optimization is continuous | ADOPT | `rules/operations/`, `validation/` | Proposed |

## Performance concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Performance objectives derive from workload needs | ADOPT | `schemas/workload/` | Proposed |
| Performance targets need load context | ADOPT | `schemas/workload/` | Proposed |
| Capacity planning precedes implementation | ADOPT | `schemas/architecture/` | Proposed |
| Elasticity follows workload behavior | ADAPT | `rules/architecture/`, `docs/patterns/` | Proposed |
| Performance requires representative testing | ADOPT | `validation/` | Proposed |
| Optimization should be evidence-driven | ADOPT | `validation/`, `rules/operations/` | Proposed |

## Sustainability concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Sustainability can be an architecture requirement | ADOPT | `schemas/workload/`, `docs/architecture/` | Proposed |
| Avoid unnecessary resource consumption | ADOPT | `rules/architecture/` | Proposed |
| Match resources to demand | ADOPT | `rules/architecture/`, `docs/patterns/` | Proposed |
| Data lifecycle affects sustainability | ADOPT | `rules/architecture/` | Proposed |
| Application efficiency can affect infrastructure demand | ADOPT | `docs/architecture/`, `rules/architecture/` | Proposed |
| Sustainability requires measurable outcomes | ADOPT | `validation/` | Proposed |

## Architecture Center concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Deployment topology is requirement-driven | ADOPT | `schemas/architecture/`, `docs/architecture/` | Proposed |
| Deployment archetypes encode tradeoffs | ADOPT | `docs/patterns/` | Proposed |
| Reference architectures require context matching | ADOPT | `examples/`, `rules/architecture/` | Proposed |
| Architecture should be documented | ADOPT | `docs/principles/`, `schemas/architecture/` | Proposed |
| Decoupling should create justified independence | ADAPT | `docs/patterns/`, `rules/architecture/` | Proposed |
| Prefer simplicity over premature complexity | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |
| Hybrid and multicloud are valid contexts | ADOPT | `schemas/workload/`, `docs/architecture/` | Proposed |

## Recommended next step

Do not promote Google concepts into canonical IaCognition rules in isolation.

The next step SHOULD compare Google guidance against the corresponding AWS and Microsoft extractions:

```text
AWS Operational Excellence
Microsoft Operational Excellence
Google Operational Excellence
                ↓
       CROSS-PROVIDER NORMALIZATION

AWS Security
Microsoft Security
Google Security
                ↓
       CROSS-PROVIDER NORMALIZATION

AWS Reliability
Microsoft Reliability
Google Reliability
                ↓
       CROSS-PROVIDER NORMALIZATION

AWS Cost Optimization
Microsoft Cost Optimization
Google Cost Optimization
                ↓
       CROSS-PROVIDER NORMALIZATION

AWS Performance Efficiency
Microsoft Performance Efficiency
Google Performance Optimization
                ↓
       CROSS-PROVIDER NORMALIZATION
```

Sustainability should compare AWS and Google directly while also considering Microsoft's separate sustainability guidance before IaCognition decides whether sustainability becomes a first-class provider-neutral quality attribute.

The goal of the next phase is not to merge vendor terminology. It is to identify independent infrastructure-engineering principles that remain valid across providers.
