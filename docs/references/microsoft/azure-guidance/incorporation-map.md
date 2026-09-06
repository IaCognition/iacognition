# Microsoft Azure Guidance Incorporation Map

This document tracks the proposed disposition and future IaCognition destination of concepts extracted from the Microsoft Azure Well-Architected Framework and Azure Architecture Center.

## Status meaning

- **Proposed** — extracted and normalized but not yet incorporated into canonical IaCognition guidance.
- **Incorporated** — represented in canonical IaCognition artifacts.
- **Rejected** — reviewed and deliberately not incorporated.
- **Superseded** — replaced by a later normalized concept or stronger source synthesis.

At the time of this ingestion, the concepts below are **Proposed**.

## Cross-cutting concepts

| Concept | Disposition | Candidate IaCognition destination | Status |
|---|---|---|---|
| Workload requirements drive architecture | ADOPT | `docs/principles/`, `schemas/workload/`, `rules/architecture/` | Proposed |
| Quality attributes are workload-specific | ADOPT | `schemas/workload/`, `docs/architecture/` | Proposed |
| Architecture requires explicit tradeoffs | ADOPT | `schemas/architecture/`, `docs/architecture/` | Proposed |
| Architecture quality should be measurable | ADOPT | `validation/`, `schemas/review/` | Proposed |
| Architecture evolves from operational evidence | ADOPT | `docs/workflows/`, `rules/operations/` | Proposed |
| Simplicity is an architecture quality | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |
| Automation should be deterministic and governed | ADAPT | `rules/operations/`, `validation/` | Proposed |
| Reference architectures are contextual | ADOPT | `examples/`, `docs/architecture/` | Proposed |
| Technology selection follows architecture | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |

## Reliability concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Reliability objectives derive from business requirements | ADOPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Critical flows require reliability targets | ADAPT | `schemas/workload/` | Proposed |
| Failure modes should be analyzed explicitly | ADOPT | `schemas/architecture/`, `rules/reliability/` | Proposed |
| Failure domains should drive resilience design | ADOPT | `rules/reliability/`, `docs/architecture/reliability/` | Proposed |
| Stateful workloads require recovery strategy | ADOPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Recovery mechanisms require testing | ADOPT | `validation/`, `rules/reliability/` | Proposed |
| Simplicity improves reliability | ADOPT | `rules/reliability/`, `docs/principles/` | Proposed |

## Security concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Security is an architecture input | ADOPT | `schemas/workload/`, `rules/security/` | Proposed |
| Verify explicitly | ADAPT | `rules/security/` | Proposed |
| Least privilege | ADOPT | `rules/security/` | Proposed |
| Assume individual controls can fail | ADAPT | `rules/security/`, `docs/architecture/security/` | Proposed |
| Trust boundaries must be explicit | ADOPT | `schemas/architecture/`, `rules/security/` | Proposed |
| Data protection derives from classification | ADOPT | `schemas/workload/`, `rules/security/` | Proposed |
| Recovery systems require equivalent security | ADOPT | `rules/security/`, `rules/reliability/` | Proposed |
| Security posture requires continuous validation | ADOPT | `validation/`, `rules/security/` | Proposed |

## Cost concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Cost is an architecture constraint | ADOPT | `schemas/workload/`, `rules/architecture/` | Proposed |
| Cost optimization is value optimization | ADOPT | `docs/principles/`, `rules/architecture/` | Proposed |
| Model lifecycle cost, not only resource price | ADOPT | `schemas/architecture/`, `rules/architecture/` | Proposed |
| Identify workload cost drivers | ADOPT | `schemas/workload/`, `validation/` | Proposed |
| Avoid unjustified overengineering | ADOPT | `rules/architecture/` | Proposed |
| Nonproduction may use different cost profiles | ADOPT | `rules/architecture/`, `examples/` | Proposed |
| Separate usage and rate optimization | ADAPT | `docs/architecture/cost/` | Proposed |
| Cost assumptions need ongoing validation | ADOPT | `validation/`, `rules/operations/` | Proposed |

## Operational Excellence concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Operational requirements are architecture inputs | ADOPT | `schemas/workload/`, `rules/operations/` | Proposed |
| Production ownership must be explicit | ADOPT | `schemas/architecture/`, `rules/operations/` | Proposed |
| Standardize repeatable processes | ADOPT | `docs/workflows/`, `rules/operations/` | Proposed |
| Observability is designed, not appended | ADOPT | `schemas/architecture/`, `rules/operations/` | Proposed |
| Deterministic operations should be automated | ADOPT | `rules/operations/` | Proposed |
| Deployment safety is part of architecture | ADOPT | `rules/operations/`, `validation/` | Proposed |
| Operational evidence should drive improvements | ADOPT | `docs/workflows/`, `rules/operations/` | Proposed |
| Organizational constraints are architecture inputs | ADOPT | `schemas/workload/`, `schemas/architecture/` | Proposed |

## Performance Efficiency concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Define measurable performance objectives | ADOPT | `schemas/workload/`, `rules/architecture/` | Proposed |
| Performance targets require load context | ADOPT | `schemas/workload/` | Proposed |
| Capacity planning precedes implementation | ADOPT | `schemas/architecture/` | Proposed |
| Scaling strategy follows workload behavior | ADAPT | `rules/architecture/`, `docs/patterns/` | Proposed |
| Performance requires representative testing | ADOPT | `validation/` | Proposed |
| Production telemetry validates performance assumptions | ADOPT | `rules/operations/`, `validation/` | Proposed |
| Avoid speculative optimization | ADOPT | `rules/architecture/` | Proposed |

## Architecture Center concepts

| Concept | Disposition | Candidate destination | Status |
|---|---|---|---|
| Architecture styles impose deliberate constraints | ADOPT | `docs/architecture/` | Proposed |
| Style selection must be requirement-driven | ADOPT | `rules/architecture/` | Proposed |
| Patterns encode reusable architecture reasoning | ADOPT | `docs/patterns/` | Proposed |
| Patterns have cross-pillar consequences | ADOPT | `docs/patterns/`, `schemas/review/` | Proposed |
| Reference architectures require context matching | ADOPT | `examples/`, `rules/architecture/` | Proposed |
| Provider implementation must remain separate from provider-neutral pattern | ADOPT | `docs/patterns/`, `examples/` | Proposed |

## Recommended next step

Do not immediately promote the Microsoft concepts into canonical IaCognition rules in isolation.

The next normalization step SHOULD compare these concepts against the corresponding AWS Well-Architected extraction, particularly:

```text
AWS Reliability              ↔ Azure Reliability
AWS Security                 ↔ Azure Security
AWS Cost Optimization        ↔ Azure Cost Optimization
AWS Operational Excellence   ↔ Azure Operational Excellence
AWS Performance Efficiency   ↔ Azure Performance Efficiency
```

The resulting provider-neutral synthesis can then determine which concepts become canonical IaCognition principles, rules, schemas, workflows, patterns, and validation requirements.

AWS Sustainability has no direct Azure Well-Architected pillar equivalent and should therefore be evaluated separately rather than forced into a one-to-one mapping.
