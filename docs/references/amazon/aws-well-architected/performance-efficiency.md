# AWS Well-Architected — Performance Efficiency Analysis

## Source scope

This analysis covers the Performance Efficiency pillar of the AWS Well-Architected Framework.

## AWS focus areas

AWS organizes performance efficiency around:

- architecture selection;
- compute and hardware;
- data management;
- networking and content delivery;
- process and culture.

The pillar emphasizes data-driven architecture choices, access patterns, benchmarking, right-sizing, elasticity, performance telemetry, load testing, and periodic re-evaluation as technology evolves.

## Extracted concepts

### AWS-PERF-001 — Define performance requirements explicitly

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD define measurable performance requirements for user-visible and system-critical operations before architecture selection.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `validation/`

### AWS-PERF-002 — Select architecture using evidence

**Disposition:** ADOPT

**Normalized concept:** Material performance-sensitive architecture choices SHOULD be informed by workload characteristics, representative measurements, benchmarks, tests, or validated reference patterns rather than intuition alone.

**Provider neutrality:** High

**Candidate destinations:** `schemas/architecture/`, `validation/`

### AWS-PERF-003 — Match resource type to workload characteristics

**Disposition:** ADOPT

**Normalized concept:** Compute, storage, database, and network choices SHOULD be selected according to workload access patterns, concurrency, latency, throughput, consistency, durability, and scaling needs.

**Provider neutrality:** High

**Candidate destinations:** `docs/architecture/`, `schemas/architecture/`

### AWS-PERF-004 — Right-size and dynamically adjust capacity

**Disposition:** ADAPT

**Normalized concept:** Workloads SHOULD avoid both chronic over-provisioning and capacity starvation by using measured demand to size resources and, where appropriate, adjust capacity dynamically.

**Provider neutrality:** High

**Candidate destinations:** `rules/architecture/`, future performance rules

### AWS-PERF-005 — Treat network behavior as an architectural concern

**Disposition:** ADOPT

**Normalized concept:** Performance-sensitive architectures SHOULD account for network topology, protocol behavior, locality, content distribution, connection patterns, and measurable network constraints.

**Provider neutrality:** High

**Candidate destinations:** `docs/architecture/networking/`, `schemas/architecture/`

### AWS-PERF-006 — Load test material workload paths

**Disposition:** ADOPT

**Normalized concept:** Workloads with material performance or scalability requirements SHOULD be tested using representative load and failure conditions before those requirements are considered validated.

**Provider neutrality:** High

**Candidate destinations:** `validation/`

### AWS-PERF-007 — Re-evaluate architecture as technology and demand change

**Disposition:** ADOPT

**Normalized concept:** Performance architecture SHOULD be periodically re-evaluated when workload demand, access patterns, platform capabilities, or economic constraints materially change.

**Provider neutrality:** High

**Candidate destinations:** `docs/workflows/`, `schemas/review/`

### AWS-PERF-008 — Evaluate managed and serverless capabilities by tradeoff

**Disposition:** ADAPT

AWS highlights managed and serverless technologies as ways to gain capabilities and reduce undifferentiated work. IaCognition should retain the tradeoff analysis rather than treating either model as universally superior.

**Normalized concept:** Managed or serverless capabilities SHOULD be evaluated against performance, scaling, operational burden, cost, control, portability, and lifecycle requirements.

**Provider neutrality:** High at the decision level.

**Candidate destinations:** `docs/architecture/`, `schemas/architecture/`

## IaCognition implications

Performance cannot be inferred from Terraform syntax or nominal resource specifications. IaCognition should connect performance requirements to architecture decisions and then to measurable validation evidence.
