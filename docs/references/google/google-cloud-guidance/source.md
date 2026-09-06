# Google Cloud Architecture Guidance

## Publisher

Google

## Source family

Google Cloud architecture guidance

## Primary sources

This source family is based on current official Google Cloud documentation, primarily:

- Google Cloud Well-Architected Framework
- Google Cloud Well-Architected Framework pillar guidance
- Google Cloud Architecture Center
- Google Cloud architecture design guides and deployment archetypes
- Google Cloud reliability and operational guidance

## Official source locations

- https://docs.cloud.google.com/docs/get-started/well-architected-framework
- https://docs.cloud.google.com/architecture/framework
- https://docs.cloud.google.com/architecture
- https://docs.cloud.google.com/architecture/deployment-archetypes
- https://docs.cloud.google.com/architecture/reliability

## Access date

2026-09-06

## Source type

Cloud architecture framework, architecture design guidance, reference architectures, deployment patterns, reliability guidance, and operational guidance.

## Scope

The Google Cloud Well-Architected Framework organizes recommendations under six pillars:

- Operational excellence
- Security
- Reliability
- Cost optimization
- Performance optimization
- Sustainability

The framework also defines cross-pillar perspectives for selected domains and industries.

Google states that the framework applies to cloud-first workloads as well as migrated, hybrid, and multicloud environments.

The Google Cloud Architecture Center complements the framework with:

- reference architectures;
- deployment archetypes;
- design guides;
- architecture patterns;
- landing-zone guidance;
- migration guidance;
- enterprise foundation guidance;
- workload-specific solution architectures.

## IaCognition relevance

This source family provides input into:

- architecture-first workload reasoning;
- reliability objectives and failure-domain design;
- operational readiness and SRE-informed practices;
- Zero Trust and defense-in-depth security;
- workload-focused performance and capacity planning;
- cost/value optimization;
- sustainability requirements;
- architecture styles and deployment archetypes;
- patterns and reference architectures;
- hybrid and multicloud design reasoning;
- observability, automation, incident management, and continuous improvement.

Google guidance is treated as source evidence, not as canonical IaCognition guidance.

## Ingestion approach

This ingestion performs:

```text
SOURCE
  ↓
EXTRACT
  ↓
NORMALIZE
```

It does not automatically promote Google recommendations into IaCognition requirements.

Extracted concepts are assigned one of:

- `ADOPT`
- `ADAPT`
- `REJECT`

Canonical incorporation into IaCognition principles, rules, schemas, workflows, validation, or examples requires a separate incorporation change.

## Provider-neutrality

Google frequently expresses broadly applicable architecture concepts through Google Cloud terminology, products, and SRE practices.

IaCognition separates:

1. the underlying architecture principle;
2. the architecture decision or constraint;
3. the Google Cloud implementation mechanism.

Google-specific recommendations MUST NOT automatically become provider-neutral IaCognition requirements.

## Notes

Google's framework is particularly relevant to IaCognition because it explicitly connects architecture guidance with operational practices such as SRE, incident management, observability, performance engineering, cost awareness, and continuous improvement.

The framework also emphasizes that recommendations should be applied according to workload requirements rather than as universal prescriptions.

This aligns directly with IaCognition's principle:

> Architect before you code.
