# Sustainability

Sustainability is the ability to meet workload requirements while reducing unjustified resource consumption and environmental impact where sustainability is a material objective.

## Context

AWS and Google Cloud expose sustainability as top-level Well-Architected pillars.

Microsoft Azure currently treats sustainability as an additional design concern rather than one of the five core Azure Well-Architected pillars.

IaCognition therefore treats sustainability as a first-class architecture quality attribute while recognizing that its priority depends on workload and organizational requirements.

## SUS-01 — Define sustainability objectives where material

A workload SHOULD record material sustainability requirements explicitly.

## SUS-02 — Avoid unnecessary resource consumption

Persistent compute, storage, data transfer, replication, and processing SHOULD be justified by workload requirements.

## SUS-03 — Align capacity with demand

Variable workloads SHOULD consider mechanisms that reduce unnecessary idle consumption when reliability and performance objectives remain satisfied.

## SUS-04 — Consider data lifecycle

Data retention, replication, movement, and processing SHOULD be justified by functional, reliability, analytical, security, or compliance requirements.

## SUS-05 — Consider software-driven infrastructure demand

Architecture review SHOULD consider whether application inefficiency is driving unnecessary infrastructure consumption.

Allocating additional resources SHOULD NOT automatically substitute for addressing avoidable software inefficiency.

## SUS-06 — Evaluate managed/shared platforms contextually

Managed or shared platforms MAY reduce resource and operational inefficiency.

They SHOULD still be evaluated for:

- control;
- portability;
- security;
- reliability;
- cost;
- organizational constraints.

## SUS-07 — Measure where sustainability matters

Material sustainability objectives SHOULD have measurable indicators where practical.

## SUS-08 — Make sustainability tradeoffs explicit

Sustainability optimizations MUST NOT silently violate:

- reliability;
- security;
- performance;
- recovery;
- compliance;
- data-residency requirements.

## Validation examples

Evidence MAY include:

- utilization data;
- idle-resource analysis;
- data-retention analysis;
- capacity efficiency;
- architecture comparison;
- provider sustainability metrics where available.
