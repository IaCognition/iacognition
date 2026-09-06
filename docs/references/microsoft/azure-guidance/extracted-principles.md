# Extracted Principles — Microsoft Azure Guidance

This document identifies cross-cutting infrastructure-engineering principles derived from analysis of Microsoft's Azure Well-Architected Framework and Azure Architecture Center.

Detailed analysis is maintained in the individual guidance files.

## AZ-X001 — Workload requirements drive architecture

Microsoft repeatedly grounds architecture decisions in functional requirements, nonfunctional requirements, business value, and workload purpose.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture decisions MUST be grounded in explicit workload requirements or explicit assumptions.

This directly supports:

- Architect before you code.
- Treat infrastructure requirements as explicit engineering inputs.
- Make assumptions explicit.

---

## AZ-X002 — Quality attributes are workload-specific

Reliability, security, cost, operational excellence, and performance requirements vary according to workload purpose and business constraints.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD NOT prescribe maximum reliability, security controls, performance, or operational complexity without reference to workload requirements.

---

## AZ-X003 — Architecture is a tradeoff process

Microsoft explicitly treats architecture choices as tradeoffs across pillars.

**Disposition:** ADOPT

**IaCognition normalization**

Material architecture decisions SHOULD identify the quality attributes improved, degraded, or constrained by the decision.

---

## AZ-X004 — Measure outcomes rather than infer quality from configuration

The Azure framework repeatedly connects architecture quality to measurable targets, telemetry, assessments, and observed behavior.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture quality SHOULD be validated using objective evidence where practical.

Configuration presence alone SHOULD NOT be treated as proof that an architecture objective is satisfied.

---

## AZ-X005 — Architecture and operations are continuous

Microsoft treats workload design as something that evolves from production evidence, changes in requirements, platform evolution, incidents, and measured outcomes.

**Disposition:** ADOPT

**IaCognition normalization**

Infrastructure architecture SHOULD be treated as a versioned engineering artifact that evolves through operation and review.

---

## AZ-X006 — Simplicity is an architecture quality

Microsoft explicitly identifies simplicity as a reliability principle and implicitly reinforces it through operational and cost guidance.

**Disposition:** ADOPT

**IaCognition normalization**

Unnecessary infrastructure complexity SHOULD be treated as architectural debt.

Additional components SHOULD be justified by requirements or measurable benefits.

---

## AZ-X007 — Automation improves repeatability but requires governance

Microsoft recommends automation across operations, security, scaling, and delivery.

**Disposition:** ADAPT

**IaCognition normalization**

Deterministic, repeatable infrastructure operations SHOULD be automated where doing so improves consistency, safety, or efficiency.

Automation MUST still be reviewable, observable, and appropriately controlled.

---

## AZ-X008 — Architecture must define failure and recovery behavior

Reliability guidance emphasizes resilience, recovery objectives, testing, and failure analysis.

**Disposition:** ADOPT

**IaCognition normalization**

Production architectures SHOULD define expected behavior under material failure scenarios before implementation.

---

## AZ-X009 — Security requires explicit trust boundaries and continuous validation

Microsoft's Zero Trust guidance, data-classification model, least-privilege model, and continuous security posture all treat security as an ongoing architectural system.

**Disposition:** ADOPT

**IaCognition normalization**

Security architecture SHOULD explicitly define identity, trust boundaries, data sensitivity, exposure, privilege, and validation expectations.

---

## AZ-X010 — Cost is about value, not minimum spend

Microsoft repeatedly frames cost optimization as maximizing investment value while preserving workload requirements.

**Disposition:** ADOPT

**IaCognition normalization**

Cost decisions SHOULD be evaluated against business value and architecture requirements rather than optimized independently.

---

## AZ-X011 — Performance requires measurable targets and representative testing

Microsoft frames performance efficiency as meeting defined performance objectives with appropriate capacity and scaling.

**Disposition:** ADOPT

**IaCognition normalization**

Performance-sensitive architectures SHOULD specify measurable targets and a method for validating them.

---

## AZ-X012 — Observability is part of architecture

Microsoft treats observability as foundational to operations, reliability, performance, security, and continuous improvement.

**Disposition:** ADOPT

**IaCognition normalization**

Production architecture SHOULD define how health, failures, security events, performance, and relevant operational state are observed.

---

## AZ-X013 — Architecture patterns are reusable reasoning artifacts

The Azure Architecture Center models recurring cloud design problems using patterns that include context, constraints, benefits, and tradeoffs.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD represent reusable architecture knowledge as patterns and anti-patterns rather than only as provider-specific examples.

---

## AZ-X014 — Reference architectures are contextual, not universal

Microsoft reference architectures are examples of applying architectural principles to particular solution contexts.

**Disposition:** ADOPT

**IaCognition normalization**

Reference architectures SHOULD declare assumptions and applicability constraints.

Agents MUST NOT copy a reference architecture without checking those assumptions against the target workload.

---

## AZ-X015 — Technology selection follows architectural intent

Microsoft Architecture Center guidance uses architecture needs and styles to narrow technology choices.

**Disposition:** ADOPT

**IaCognition normalization**

Infrastructure technology and resource selection SHOULD implement prior architecture decisions.

This directly reinforces:

> Architect before you code.

## Overall assessment

Microsoft Azure guidance is strongly aligned with IaCognition's foundational model.

The highest-value provider-neutral concepts are:

1. requirement-driven architecture;
2. explicit quality attributes;
3. architecture tradeoffs;
4. measurable outcomes;
5. failure-mode and recovery reasoning;
6. Zero Trust and explicit security boundaries;
7. lifecycle cost/value modeling;
8. observability and operational readiness;
9. evidence-driven performance and capacity planning;
10. patterns and reference architectures as contextual reasoning tools.

These concepts are candidates for cross-normalization with the AWS Well-Architected ingestion before they become canonical IaCognition requirements.
