# Google Cloud Well-Architected — Cost Optimization Analysis

## Source scope

This analysis covers the Cost Optimization pillar of the Google Cloud Well-Architected Framework.

Google frames cost optimization around maximizing business value, building cost awareness, optimizing resources, and continuously improving cost efficiency.

## Extracted concepts

### GCP-COST-001 — Cost should align with business value

**Source concept**

Cloud spend should be evaluated according to the value delivered by the workload.

**Disposition:** ADOPT

**IaCognition normalization**

Cost decisions SHOULD be evaluated against workload value and architecture requirements rather than optimized independently.

**Provider neutrality:** High

---

### GCP-COST-002 — Cost is an architecture input

**Source concept**

Cost implications should be considered during design rather than after deployment.

**Disposition:** ADOPT

**IaCognition normalization**

Material workloads SHOULD define cost constraints, budgets, or optimization objectives before architecture selection.

**Provider neutrality:** High

---

### GCP-COST-003 — Build cost awareness

**Source concept**

Teams should understand the financial effects of architecture and operational choices.

**Disposition:** ADOPT

**IaCognition normalization**

Architectures SHOULD expose enough cost attribution information to identify significant cost drivers and responsible workloads.

**Provider neutrality:** High

---

### GCP-COST-004 — Identify cost drivers

**Source concept**

Optimization requires understanding which resources, services, traffic patterns, or usage characteristics primarily determine cost.

**Disposition:** ADOPT

**IaCognition normalization**

Cost-sensitive workloads SHOULD identify major cost drivers and how they scale with usage or growth.

**Provider neutrality:** High

---

### GCP-COST-005 — Right-size resources

**Source concept**

Resources should be matched to workload requirements rather than persistently overprovisioned.

**Disposition:** ADOPT

**IaCognition normalization**

Provisioned capacity SHOULD be justified by observed demand, forecast requirements, reliability headroom, or recovery constraints.

**Provider neutrality:** High

---

### GCP-COST-006 — Elasticity can reduce waste

**Source concept**

Variable workloads can benefit from capacity that changes with demand.

**Disposition:** ADOPT

**IaCognition normalization**

Variable-demand workloads SHOULD consider elastic capacity mechanisms when those mechanisms preserve reliability and performance requirements.

**Provider neutrality:** High

---

### GCP-COST-007 — Optimize rates separately from usage

**Source concept**

Commercial commitments and pricing models can reduce cost when demand is predictable.

**Disposition:** ADAPT

**IaCognition normalization**

Cost analysis SHOULD distinguish:

- consumption optimization;
- unit-rate optimization.

Commitments SHOULD be justified by forecast confidence and operational constraints.

**Provider neutrality:** High

---

### GCP-COST-008 — Avoid unnecessary complexity

**Source concept**

Overengineered architectures can increase both resource cost and operational cost.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture SHOULD NOT introduce components or redundancy without a requirement or measurable benefit that justifies their lifecycle cost.

**Provider neutrality:** High

---

### GCP-COST-009 — Cost optimization is continuous

**Source concept**

Workload behavior, provider pricing, architecture, and business priorities change over time.

**Disposition:** ADOPT

**IaCognition normalization**

Material cost assumptions SHOULD be reviewed periodically and when workload behavior or architecture changes significantly.

**Provider neutrality:** High

## Cross-pillar considerations

Cost decisions can affect:

- reliability;
- security;
- performance;
- operability;
- sustainability.

IaCognition SHOULD model these tradeoffs explicitly.
