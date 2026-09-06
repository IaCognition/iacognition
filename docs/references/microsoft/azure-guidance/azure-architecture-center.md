# Microsoft Azure Architecture Center Analysis

## Source scope

This analysis covers the Azure Architecture Center and Azure Application Architecture Fundamentals as complementary sources to the Azure Well-Architected Framework.

The Well-Architected Framework describes quality attributes and decision principles. The Architecture Center provides architecture styles, patterns, technology-selection guidance, reference architectures, and implementation examples.

## Extracted concepts

### AZ-ARC-001 — Architecture style constrains design

**Source concept**

Microsoft describes an architecture style as a family of architectures with shared characteristics and constraints.

**Disposition:** ADOPT

**IaCognition normalization**

An architecture style SHOULD be treated as a set of deliberate structural constraints, not merely as a label.

When an architecture style is selected, agents SHOULD understand the constraints and tradeoffs implied by that choice.

**Provider neutrality:** High

---

### AZ-ARC-002 — Architecture styles should be selected intentionally

**Source concept**

Architecture styles have different strengths, weaknesses, constraints, and operational consequences.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture style selection SHOULD be justified by workload requirements and quality attributes.

An AI agent SHOULD NOT select an architectural style solely because it is common or fashionable.

**Provider neutrality:** High

---

### AZ-ARC-003 — Patterns encode reusable architectural knowledge

**Source concept**

Microsoft uses cloud design patterns to address recurring architecture problems and their tradeoffs.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD represent recurring architecture solutions as patterns that include:

- problem context;
- forces and constraints;
- architecture intent;
- benefits;
- risks;
- tradeoffs;
- applicability;
- implementation considerations.

**Provider neutrality:** High

---

### AZ-ARC-004 — Patterns can span multiple quality attributes

**Source concept**

Microsoft explicitly maps design patterns to multiple Well-Architected pillars.

**Disposition:** ADOPT

**IaCognition normalization**

A pattern SHOULD NOT be classified as benefiting only one quality attribute when it materially affects others.

Pattern documentation SHOULD identify positive and negative cross-cutting effects.

**Provider neutrality:** High

---

### AZ-ARC-005 — Reference architecture is not universal architecture

**Source concept**

Azure reference architectures demonstrate prescriptive ways of applying principles and patterns in particular contexts.

**Disposition:** ADOPT

**IaCognition normalization**

Reference architectures SHOULD be treated as validated examples for defined contexts rather than universally correct templates.

Agents MUST compare a reference architecture's assumptions with the target workload before adapting it.

**Provider neutrality:** High

---

### AZ-ARC-006 — Technology selection follows architecture

**Source concept**

Microsoft Architecture Center guidance connects workload requirements and architecture styles to technology choices.

**Disposition:** ADOPT

**IaCognition normalization**

Technology and service selection SHOULD follow architecture requirements and constraints.

IaC implementation SHOULD NOT be the mechanism by which foundational architecture choices are accidentally made.

**Provider neutrality:** High

This directly reinforces IaCognition's core principle:

> Architect before you code.

---

### AZ-ARC-007 — Tradeoffs are part of architecture selection

**Source concept**

Microsoft Architecture Center guidance repeatedly describes benefits, challenges, and tradeoffs of styles and patterns.

**Disposition:** ADOPT

**IaCognition normalization**

Material architecture decisions SHOULD record both the expected benefit and the significant downside or constraint introduced by the decision.

**Provider neutrality:** High

---

### AZ-ARC-008 — Vendor-specific implementations can demonstrate vendor-neutral patterns

**Source concept**

Architecture Center patterns frequently describe broadly applicable architectural ideas and then show Azure-specific implementations.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD separate:

```text
Architecture pattern
        ↓
Provider implementation
        ↓
IaC implementation
```

The provider implementation MUST NOT redefine the underlying provider-neutral pattern.

**Provider neutrality:** High

## Implications for IaCognition

The Azure Architecture Center strongly supports the decision to maintain separate IaCognition artifact categories for:

- principles;
- architecture guidance;
- patterns;
- anti-patterns;
- examples;
- implementation guidance.

It also reinforces the repository invariant that executable Terraform examples are implementations of architecture decisions, not substitutes for those decisions.
