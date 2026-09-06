# AWS Well-Architected Framework — Source Record

## Publisher

Amazon Web Services (AWS)

## Source family

AWS Well-Architected Framework

## Source type

Cloud architecture framework and pillar guidance.

## Access date

2026-09-06

## Primary source locations

- AWS Well-Architected Framework: https://docs.aws.amazon.com/wellarchitected/latest/framework/
- AWS Well-Architected Tool user guide overview: https://docs.aws.amazon.com/wellarchitected/latest/userguide/waf.html
- Operational Excellence Pillar: https://docs.aws.amazon.com/wellarchitected/latest/operational-excellence-pillar/
- Security Pillar: https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/
- Reliability Pillar: https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/
- Performance Efficiency Pillar: https://docs.aws.amazon.com/wellarchitected/latest/performance-efficiency-pillar/
- Cost Optimization Pillar: https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/
- Sustainability Pillar: https://docs.aws.amazon.com/wellarchitected/latest/sustainability-pillar/

## Framework scope

AWS Well-Architected provides a structured approach for evaluating and improving cloud workloads. The framework is organized around six pillars:

1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

AWS also provides general design principles, workload and architecture definitions, a review process, pillar-specific design principles, questions, best practices, and supporting implementation guidance.

## IaCognition relevance

AWS Well-Architected is a foundational input for IaCognition because it addresses many of the architectural quality attributes that an infrastructure agent must reason about before generating Infrastructure as Code.

The source is especially relevant to:

- workload definition and classification;
- architecture tradeoffs;
- operational readiness;
- identity and security boundaries;
- failure domains and recovery objectives;
- performance requirements and evidence;
- cost awareness and resource efficiency;
- sustainability and resource utilization;
- continuous architecture review and improvement.

## Ingestion boundary

This directory does not reproduce the AWS Well-Architected Framework. It records IaCognition's analysis and normalization of the engineering concepts contained in the source.

AWS-specific service recommendations remain provider-specific. Concepts are promoted into provider-neutral IaCognition guidance only when the underlying engineering principle is valid independently of AWS terminology and services.

## Source handling notes

The AWS documentation uses `latest` URLs that may change over time. The access date above establishes the point-in-time basis for this extraction. Future changes to AWS guidance should be evaluated through the same SOURCE → EXTRACT → NORMALIZE → INCORPORATE process rather than automatically replacing IaCognition guidance.
