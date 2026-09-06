# AWS Well-Architected — Incorporation Map

This document tracks candidate IaCognition concepts derived from the AWS Well-Architected Framework.

**Status rule:** Extraction and normalization do not imply incorporation. Items remain `Proposed` until canonical IaCognition artifacts are created or updated in a separate incorporation change.

| Concept | Source area | Disposition | Candidate IaCognition destination | Status |
|---|---|---|---|---|
| Workload requirements drive architecture | Framework / review model | ADOPT | `schemas/workload/`, `docs/principles/` | Proposed |
| Explicit architectural tradeoffs | Framework | ADOPT | `schemas/architecture/`, `rules/architecture/` | Proposed |
| Continuous architecture review | Review process | ADOPT | `docs/workflows/`, `schemas/review/`, `validation/` | Proposed |
| Operations as code | Operational Excellence | ADOPT | `rules/operations/`, `docs/principles/` | Proposed |
| Small, reversible changes | Operational Excellence | ADOPT | `rules/operations/`, `validation/` | Proposed |
| Operational readiness before production | Operational Excellence | ADOPT | `schemas/review/`, `validation/` | Proposed |
| Explicit ownership and operating model | Operational Excellence | ADAPT | `schemas/workload/`, `docs/standards/` | Proposed |
| Strong identity foundation | Security | ADAPT | `rules/security/`, `schemas/architecture/` | Proposed |
| Traceability and security telemetry | Security | ADOPT | `rules/security/`, `validation/` | Proposed |
| Defense in depth | Security | ADOPT | `rules/security/`, `docs/architecture/security/` | Proposed |
| Security automation | Security | ADOPT | `rules/security/`, `validation/` | Proposed |
| Data classification and protection | Security | ADAPT | `schemas/workload/`, `rules/security/` | Proposed |
| Incident readiness and tested response | Security | ADOPT | `rules/security/`, `validation/` | Proposed |
| Define availability and recovery objectives | Reliability | ADOPT | `schemas/workload/`, `rules/reliability/` | Proposed |
| Design for failure isolation | Reliability | ADOPT | `rules/reliability/`, `docs/architecture/reliability/` | Proposed |
| Automate recovery | Reliability | ADOPT | `rules/reliability/`, `validation/` | Proposed |
| Test recovery procedures | Reliability | ADOPT | `validation/`, `docs/workflows/` | Proposed |
| Manage quotas and hard constraints | Reliability | ADAPT | `schemas/architecture/`, provider-specific rules | Proposed |
| Data-driven architecture selection | Performance Efficiency | ADOPT | `schemas/architecture/`, `validation/` | Proposed |
| Explicit performance requirements and KPIs | Performance Efficiency | ADOPT | `schemas/workload/`, `validation/` | Proposed |
| Benchmark and load test material choices | Performance Efficiency | ADOPT | `validation/` | Proposed |
| Dynamic scaling to demand | Performance Efficiency | ADAPT | `rules/architecture/`, provider-specific guidance | Proposed |
| Financial ownership and cost awareness | Cost Optimization | ADAPT | future cost rules / schemas | Proposed |
| Measure and attribute cloud expenditure | Cost Optimization | ADAPT | future cost validation | Proposed |
| Align supply with demand | Cost Optimization | ADOPT | `rules/architecture/`, future cost rules | Proposed |
| Review cost efficiency over time | Cost Optimization | ADOPT | `docs/workflows/`, validation | Proposed |
| Sustainability as a non-functional requirement | Sustainability | ADAPT | `schemas/workload/`, future sustainability rules | Proposed |
| Measure impact relative to useful work | Sustainability | ADAPT | future sustainability validation | Proposed |
| Minimize idle or unnecessary resource consumption | Sustainability | ADOPT | `rules/architecture/`, future sustainability rules | Proposed |
| Include lifecycle effects in optimization | Sustainability | ADAPT | `docs/principles/`, future sustainability guidance | Proposed |

## Deferred provider-specific material

The following classes of guidance are useful but SHOULD remain AWS-specific unless separately normalized:

- particular AWS Regions, Availability Zones, or service capabilities;
- AWS IAM, AWS Organizations, AWS Control Tower, CloudWatch, CloudTrail, Config, or Security Hub implementation details;
- EC2, Lambda, ECS, EKS, RDS, DynamoDB, S3, or other AWS service-specific recommendations;
- AWS pricing constructs and purchasing mechanisms;
- AWS-specific quota, account, and control-plane behavior;
- AWS-specific sustainability implementation recommendations.

These may later support provider-specific IaCognition implementation guidance and Terraform examples.
