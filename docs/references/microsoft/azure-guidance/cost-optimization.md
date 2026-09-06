# Microsoft Azure Well-Architected — Cost Optimization Analysis

## Source scope

This analysis covers the Cost Optimization pillar of the Microsoft Azure Well-Architected Framework.

Microsoft frames cost optimization as maximizing workload value and return on investment, not simply minimizing cloud spend.

## Extracted concepts

### AZ-COST-001 — Cost is an architecture constraint

**Source concept**

Architecture decisions are driven by business goals, ROI, budgets, and financial constraints.

**Disposition:** ADOPT

**IaCognition normalization**

Material workloads SHOULD define cost constraints or objectives before architecture selection.

Cost SHOULD be treated as an architecture input rather than a post-deployment optimization task.

**Provider neutrality:** High

---

### AZ-COST-002 — Lowest cost is not necessarily optimal

**Source concept**

A cost-optimized workload is not necessarily the least expensive workload.

**Disposition:** ADOPT

**IaCognition normalization**

Cost decisions SHOULD maximize workload value while preserving required functional and nonfunctional outcomes.

An architecture SHOULD NOT reduce cost by silently violating reliability, security, performance, or operational requirements.

**Provider neutrality:** High

---

### AZ-COST-003 — Model total cost, not only resource price

**Source concept**

Microsoft recommends considering infrastructure, support, implementation, licensing, training, personnel, automation, and operational costs.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture cost analysis SHOULD consider material direct and indirect lifecycle costs.

Resource unit price alone SHOULD NOT be treated as sufficient evidence that one architecture is less expensive than another.

**Provider neutrality:** High

---

### AZ-COST-004 — Identify cost drivers

**Source concept**

A workload should understand which architectural and usage factors primarily determine spend.

**Disposition:** ADOPT

**IaCognition normalization**

Cost-sensitive workloads SHOULD identify major cost drivers and how those drivers scale with workload growth or usage.

**Provider neutrality:** High

---

### AZ-COST-005 — Avoid unnecessary overengineering

**Source concept**

Microsoft warns against designing beyond expected requirements and growth because doing so can reduce ROI.

**Disposition:** ADOPT

**IaCognition normalization**

Architectures SHOULD NOT provision resilience, scale, isolation, or platform capabilities beyond justified requirements without recording the tradeoff.

**Provider neutrality:** High

---

### AZ-COST-006 — Environments can have different cost profiles

**Source concept**

Development, test, staging, and production environments need not use identical capacity or features when requirements differ.

**Disposition:** ADOPT

**IaCognition normalization**

Nonproduction environments MAY use different availability, capacity, observability, retention, and service tiers when those differences do not invalidate their purpose.

Differences from production SHOULD be explicit when they can affect test validity or deployment risk.

**Provider neutrality:** High

---

### AZ-COST-007 — Match capacity to demand

**Source concept**

Dynamic scaling and right-sizing can reduce waste while maintaining workload outcomes.

**Disposition:** ADOPT

**IaCognition normalization**

Variable-demand workloads SHOULD consider mechanisms that align provisioned capacity with observed or anticipated demand.

Scaling strategies MUST still satisfy reliability and performance constraints.

**Provider neutrality:** High

---

### AZ-COST-008 — Optimize rate separately from usage

**Source concept**

Microsoft distinguishes consuming fewer resources from paying a more favorable rate for resources whose demand is understood.

**Disposition:** ADAPT

**IaCognition normalization**

Cost reasoning SHOULD distinguish:

- quantity or usage optimization;
- unit-rate or commercial optimization.

Commitment-based pricing SHOULD only be selected when forecast confidence and operational constraints justify it.

**Provider neutrality:** High

---

### AZ-COST-009 — Cost requires ongoing measurement

**Source concept**

Cost optimization is continuous because architectures, demand, business priorities, and commercial models change.

**Disposition:** ADOPT

**IaCognition normalization**

Cost-sensitive workloads SHOULD expose sufficient allocation and usage data to evaluate actual spending against architecture assumptions.

Material cost assumptions SHOULD be reviewed as workload behavior changes.

**Provider neutrality:** High

---

### AZ-COST-010 — Cost guardrails can prevent unintended spend

**Source concept**

Microsoft recommends budgets, alerts, governance, and architecture controls that reduce accidental or unapproved expenditure.

**Disposition:** ADOPT

**IaCognition normalization**

Organizations MAY define automated cost guardrails where unbounded resource creation or scaling could create material financial risk.

Guardrails SHOULD NOT silently prevent required reliability or recovery operations.

**Provider neutrality:** High

## Cross-pillar considerations

Cost optimization frequently trades against:

- reliability;
- security;
- performance;
- operational simplicity.

IaCognition SHOULD require those tradeoffs to be visible rather than treating cost reduction as an independent objective.
