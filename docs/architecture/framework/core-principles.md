# Core Architecture Principles

These principles represent cross-provider concepts that remain valid after AWS, Microsoft Azure, and Google Cloud terminology and service implementations are removed.

## IACOG-ARCH-P01 — Architect before implementation

Infrastructure code SHOULD implement an architecture decision.

Infrastructure code SHOULD NOT be the mechanism by which foundational architecture decisions are accidentally discovered.

Before implementation begins, material requirements, assumptions, constraints, and quality objectives SHOULD be identified.

## IACOG-ARCH-P02 — Requirements drive architecture

Architecture MUST be grounded in:

- functional requirements;
- nonfunctional requirements;
- business objectives;
- organizational constraints;
- regulatory constraints;
- workload characteristics;
- explicit assumptions where requirements remain unknown.

Architecture SHOULD NOT be justified solely by provider defaults or tool convenience.

## IACOG-ARCH-P03 — Make assumptions explicit

Unknown requirements MUST NOT be silently converted into architecture decisions.

When required information is unavailable, an agent or engineer SHOULD:

1. record the unknown;
2. make an explicit assumption if work must continue;
3. describe the consequence of that assumption;
4. identify what would change if the assumption proves false.

## IACOG-ARCH-P04 — Treat architecture as a tradeoff process

There is rarely one architecture that maximizes all quality attributes simultaneously.

Material decisions SHOULD identify:

- intended benefit;
- affected quality attributes;
- introduced cost;
- introduced complexity;
- constraints;
- known disadvantages;
- alternatives considered where material.

## IACOG-ARCH-P05 — Prefer measurable objectives

Architecture objectives SHOULD be measurable when practical.

Examples include:

- availability objective;
- recovery point objective;
- recovery time objective;
- latency target;
- throughput target;
- expected concurrency;
- budget threshold;
- capacity threshold;
- incident detection target;
- deployment recovery target.

Configuration presence alone SHOULD NOT be treated as evidence that an objective is satisfied.

## IACOG-ARCH-P06 — Design for failure

Production architecture SHOULD identify material failure modes.

Architecture reasoning SHOULD consider:

- component failure;
- dependency failure;
- zone or facility failure;
- regional failure where relevant;
- network partition;
- capacity exhaustion;
- configuration error;
- credential or identity failure;
- data corruption;
- operator error;
- provider or third-party dependency failure.

## IACOG-ARCH-P07 — Minimize unnecessary complexity

Every component, dependency, boundary, replica, platform, and automation mechanism introduces lifecycle cost.

The simplest architecture that satisfies known requirements SHOULD generally be preferred.

Speculative flexibility and premature scaling SHOULD NOT justify complexity without a credible requirement.

## IACOG-ARCH-P08 — Design security boundaries explicitly

Identity, privilege, trust boundaries, sensitive data, and exposure SHOULD be explicit architecture elements.

Network location alone SHOULD NOT be assumed to establish trust.

## IACOG-ARCH-P09 — Treat operations as architecture

A design that cannot be safely deployed, observed, maintained, recovered, and supported is incomplete.

Operational requirements SHOULD be considered before production implementation.

## IACOG-ARCH-P10 — Treat cost as an input

Cost SHOULD influence architecture during design rather than only after deployment.

Cost optimization SHOULD preserve required security, reliability, performance, and operational outcomes.

## IACOG-ARCH-P11 — Validate architecture with evidence

Architecture quality SHOULD be demonstrated through appropriate evidence.

Evidence MAY include:

- automated policy validation;
- tests;
- failure exercises;
- recovery tests;
- performance tests;
- security assessment;
- cost analysis;
- production telemetry;
- plan review;
- architecture review.

Prefer deterministic evidence over model confidence.

## IACOG-ARCH-P12 — Contextualize patterns and reference architectures

Patterns and reference architectures are reusable knowledge, not universal templates.

Before reuse, an engineer or agent MUST compare the pattern's assumptions and constraints against the target workload.

## IACOG-ARCH-P13 — Separate provider-neutral intent from provider implementation

The architecture requirement:

> tolerate loss of one infrastructure failure domain

is provider-neutral.

The implementation:

> deploy across three AWS Availability Zones

is provider-specific.

Canonical architecture guidance SHOULD preserve that separation.

## IACOG-ARCH-P14 — Allow operations to revise architecture

Architecture is a versioned engineering artifact.

Production evidence, incidents, growth, platform changes, security findings, cost behavior, and changed business requirements MAY invalidate earlier decisions.

Architecture SHOULD therefore be reviewed and evolved over time.
