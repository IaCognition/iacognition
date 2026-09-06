# Google Cloud Architecture Center Analysis

## Source scope

This analysis covers the Google Cloud Architecture Center as a complementary source to the Google Cloud Well-Architected Framework.

The Architecture Center contains reference architectures, design guides, deployment archetypes, enterprise foundation guidance, migration guidance, and workload-specific architectural patterns.

## Extracted concepts

### GCP-ARC-001 — Architecture begins with requirements and constraints

**Source concept**

Google's architecture guidance selects deployment and service approaches according to workload requirements, scale, geography, availability, and organizational constraints.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture style and topology SHOULD be selected from explicit requirements and constraints before implementation technologies are chosen.

**Provider neutrality:** High

---

### GCP-ARC-002 — Deployment topology is an architecture decision

**Source concept**

Google describes deployment archetypes such as zonal, regional, multi-regional, global, hybrid, and multicloud.

**Disposition:** ADAPT

**IaCognition normalization**

Deployment topology SHOULD be selected according to:

- failure-domain requirements;
- user geography;
- latency;
- regulatory constraints;
- data locality;
- recovery requirements;
- cost;
- operational complexity.

Topology SHOULD NOT be inferred solely from what a cloud provider makes easy to provision.

**Provider neutrality:** High

---

### GCP-ARC-003 — Architecture archetypes encode tradeoffs

**Source concept**

Google compares deployment archetypes according to availability, cost, complexity, and other design goals.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition architecture patterns SHOULD explicitly document:

- applicability;
- advantages;
- disadvantages;
- assumptions;
- failure behavior;
- cost implications;
- operational implications.

**Provider neutrality:** High

---

### GCP-ARC-004 — Reference architectures are contextual examples

**Source concept**

Google reference architectures demonstrate solutions for specific workload contexts.

**Disposition:** ADOPT

**IaCognition normalization**

Reference architectures SHOULD be treated as contextual implementations rather than universal templates.

Agents MUST compare reference assumptions with target workload requirements before adapting them.

**Provider neutrality:** High

---

### GCP-ARC-005 — Architecture should be documented

**Source concept**

Google guidance emphasizes documenting architecture and major changes.

**Disposition:** ADOPT

**IaCognition normalization**

Material architecture decisions SHOULD be recorded as versioned engineering artifacts.

Infrastructure code SHOULD remain traceable to those decisions.

**Provider neutrality:** High

---

### GCP-ARC-006 — Decoupling can create independent failure and scaling boundaries

**Source concept**

Google architecture guidance frequently recommends separating components that have different scaling, reliability, security, or lifecycle needs.

**Disposition:** ADAPT

**IaCognition normalization**

Components SHOULD be decoupled when doing so creates justified independence in:

- scaling;
- failure isolation;
- deployment;
- security;
- ownership.

Decoupling SHOULD NOT be introduced without a clear architectural benefit.

**Provider neutrality:** High

---

### GCP-ARC-007 — Simplicity should be preferred over premature complexity

**Source concept**

Google architecture guidance recommends starting simple and avoiding unnecessary overengineering.

**Disposition:** ADOPT

**IaCognition normalization**

The simplest architecture that satisfies known requirements SHOULD generally be preferred.

Speculative complexity SHOULD be treated as architectural cost.

**Provider neutrality:** High

---

### GCP-ARC-008 — Managed services are architectural choices, not defaults

**Source concept**

Google often recommends managed services to reduce operational burden.

**Disposition:** ADAPT

**IaCognition normalization**

Managed services SHOULD be evaluated where they materially reduce operational responsibility, but selection MUST still account for:

- portability;
- control;
- availability;
- cost;
- security;
- lifecycle;
- organizational constraints.

**Provider neutrality:** High

---

### GCP-ARC-009 — Hybrid and multicloud are valid architecture contexts

**Source concept**

Google explicitly states that its Well-Architected recommendations apply to hybrid and multicloud environments.

**Disposition:** ADOPT

**IaCognition normalization**

IaCognition SHOULD model provider boundaries and hybrid dependencies as architecture constraints rather than assume a single-cloud topology.

**Provider neutrality:** High

## Implications for IaCognition

Google's Architecture Center strongly reinforces the need for IaCognition artifacts representing:

- architecture styles;
- deployment archetypes;
- patterns;
- tradeoffs;
- reference architectures;
- topology decisions;
- assumptions;
- provider-specific implementations.

It also reinforces the repository principle that Terraform is an implementation of architecture, not a substitute for architecture reasoning.
