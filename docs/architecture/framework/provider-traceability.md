# Provider Traceability and Cross-Provider Normalization

This document records the evidence basis for the IaCognition Architecture Framework.

It does not make provider documentation canonical IaCognition guidance.

## Source families

### Amazon

```text
docs/references/amazon/aws-well-architected/
```

Primary source family:

- AWS Well-Architected Framework
- six pillars:
  - Operational Excellence
  - Security
  - Reliability
  - Performance Efficiency
  - Cost Optimization
  - Sustainability

### Microsoft

```text
docs/references/microsoft/azure-guidance/
```

Primary source family:

- Azure Well-Architected Framework
- Azure Architecture Center

Core Azure pillars:

- Reliability
- Security
- Cost Optimization
- Operational Excellence
- Performance Efficiency

Microsoft also recognizes additional design concerns such as sustainability outside the five core pillars.

### Google

```text
docs/references/google/google-cloud-guidance/
```

Primary source family:

- Google Cloud Well-Architected Framework
- Google Cloud Architecture Center

Current pillars:

- Operational Excellence
- Security
- Reliability
- Cost Optimization
- Performance Optimization
- Sustainability

## Normalized quality mapping

| IaCognition | AWS | Microsoft Azure | Google Cloud |
|---|---|---|---|
| Operational Excellence | Operational Excellence | Operational Excellence | Operational Excellence |
| Security | Security | Security | Security |
| Reliability | Reliability | Reliability | Reliability |
| Performance Efficiency | Performance Efficiency | Performance Efficiency | Performance Optimization |
| Cost Optimization | Cost Optimization | Cost Optimization | Cost Optimization |
| Sustainability | Sustainability | Additional design concern | Sustainability |

## High-confidence convergence

The following concepts independently recur across all three provider source families and are therefore strong candidates for provider-neutral guidance:

### Requirements drive architecture

All three frameworks relate architectural quality to workload or business requirements.

### Tradeoffs are inherent

All three frameworks acknowledge that quality attributes interact and that architecture involves tradeoffs.

### Reliability requires more than redundancy

Reliability guidance converges on failure tolerance, recovery, testing, monitoring, and operational processes.

### Security is continuous

Security guidance converges on identity, least privilege, data protection, layered controls, monitoring, and ongoing improvement.

### Operations are part of design

All three providers treat observability, automation, controlled change, incident response, and continuous improvement as architecture-quality concerns.

### Performance requires measurement

All three providers emphasize workload-specific performance objectives, capacity planning, testing, and ongoing measurement.

### Cost requires continuous optimization

All three providers treat cost as an ongoing architecture and operational concern rather than simple resource-price minimization.

### Architecture should be contextual

AWS workload tradeoffs, Azure Architecture Center guidance, and Google reference architectures all support context-driven rather than universal architecture prescriptions.

## Sustainability normalization

Sustainability has explicit top-level framework status in AWS and Google Cloud.

Microsoft currently does not expose it as one of the five Azure Well-Architected pillars, but Azure architecture guidance allows organizations to apply additional principles such as sustainability.

IaCognition therefore includes sustainability as a quality attribute but does not assume it has equal priority for every workload.

## Provider-specific concepts intentionally not normalized

The framework intentionally avoids making provider-specific mechanisms canonical, including:

- AWS Availability Zones as a universal term;
- Azure resource groups/subscriptions as a universal hierarchy;
- Google Cloud projects/folders as a universal hierarchy;
- provider-specific IAM products;
- provider-specific load balancers;
- provider-specific databases;
- provider-specific monitoring platforms;
- provider-specific pricing instruments.

Those belong in provider implementation guidance.

## Normalization rule

A provider recommendation SHOULD become provider-neutral IaCognition guidance only when at least one of the following is true:

1. the underlying principle is independently supported across multiple credible sources;
2. the concept is clearly independent of provider implementation;
3. it follows directly from an IaCognition foundational principle;
4. IaCognition explicitly adopts it as an opinionated engineering rule with documented rationale.

Provider popularity alone is insufficient.

## Source update behavior

Provider frameworks evolve.

Changes to source material SHOULD trigger reevaluation of affected normalized concepts, but SHOULD NOT automatically overwrite canonical IaCognition guidance.

Canonical changes require explicit review.
