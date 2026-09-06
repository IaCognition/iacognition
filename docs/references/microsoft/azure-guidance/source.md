# Microsoft Azure Architecture Guidance

## Publisher

Microsoft

## Source family

Microsoft Azure architecture guidance

## Primary sources

This source family is based on current official Microsoft Learn material, primarily:

- Azure Well-Architected Framework
- Azure Well-Architected Framework pillar guidance
- Azure Architecture Center
- Azure Application Architecture Fundamentals
- Azure Architecture Center architecture styles and cloud design patterns

## Official source locations

- https://learn.microsoft.com/en-us/azure/well-architected/
- https://learn.microsoft.com/en-us/azure/well-architected/what-is-well-architected-framework
- https://learn.microsoft.com/en-us/azure/well-architected/pillars
- https://learn.microsoft.com/en-us/azure/architecture/
- https://learn.microsoft.com/en-us/azure/architecture/guide/
- https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/

## Access date

2026-09-06

## Source type

Cloud architecture framework, architecture design guidance, reference architectures, patterns, and operational guidance.

## Scope

Microsoft's Azure Well-Architected Framework organizes workload quality around five pillars:

- Reliability
- Security
- Cost Optimization
- Operational Excellence
- Performance Efficiency

Microsoft describes a Well-Architected workload as one whose functional and nonfunctional requirements are defined and prioritized, whose architecture uses intentional design patterns and tradeoffs, whose implementation and operations conform to its purpose, and whose effectiveness is measured and adapted over time.

The Azure Architecture Center complements the Well-Architected Framework with architecture styles, design patterns, technology guidance, reference architectures, and implementation examples.

## IaCognition relevance

This source family provides input into:

- workload and nonfunctional-requirement modeling;
- architecture decision and tradeoff reasoning;
- reliability and recoverability requirements;
- security architecture and Zero Trust principles;
- cost modeling and FinOps-aware design;
- observability, automation, deployment, and operational readiness;
- performance targets, capacity planning, scaling, and continuous optimization;
- architectural styles, constraints, patterns, and reference architecture reasoning.

Microsoft guidance is treated as source evidence, not as canonical IaCognition guidance.

## Ingestion approach

This ingestion performs:

```text
SOURCE
  ↓
EXTRACT
  ↓
NORMALIZE
```

It does not automatically promote Microsoft recommendations into IaCognition requirements.

Extracted concepts are assigned one of the following dispositions:

- `ADOPT`
- `ADAPT`
- `REJECT`

Canonical incorporation into IaCognition principles, rules, schemas, workflows, validation, or examples requires a separate incorporation change.

## Provider-neutrality

Microsoft often expresses broadly applicable architecture concepts through Azure terminology and Azure service examples.

IaCognition separates:

1. the underlying architecture principle;
2. the architectural decision or constraint;
3. the Azure-specific implementation mechanism.

Azure-specific recommendations MUST NOT automatically become provider-neutral IaCognition requirements.

## Notes

Microsoft's framework explicitly encourages workload-specific tradeoffs. A well-architected workload is not expected to maximize every quality attribute without regard to business value, cost, complexity, or other constraints.

This aligns strongly with IaCognition's architecture-first model: functional and nonfunctional requirements should drive architecture decisions before Infrastructure as Code implementation begins.
