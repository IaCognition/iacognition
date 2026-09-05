# Workload Definition Schema

The workload definition captures the information an AI agent or engineer should consider before designing infrastructure.

This document defines the conceptual schema. A machine-readable JSON Schema or equivalent may be added later.

## Goals

The workload definition should:

- distinguish requirements from implementation;
- expose unknowns and assumptions;
- provide enough context for architecture decisions;
- remain independent of a specific cloud provider;
- support both lightweight and detailed use.

## Example

```yaml
workload:
  name: example-api
  purpose: Provide an internal HTTP API
  environment: production
  type: service

availability:
  target: high
  failure_domains:
    availability_zone: required
    region: not_required

recovery:
  rto: 60m
  rpo: 15m

networking:
  internet_facing: false
  outbound_internet: required

data:
  persistent: true
  model: relational
  sensitivity: internal

security:
  authentication: required
  encryption_at_rest: required
  encryption_in_transit: required

operations:
  centralized_logging: required
  monitoring: required
  alerting: required

cost:
  priority: balanced

assumptions:
  - Traffic is expected to remain below 100 requests per second during the initial release.

unknowns:
  - Exact database growth rate has not yet been measured.
```

## Sections

### workload

Identifies the system and its purpose.

Suggested fields:

- `name`
- `purpose`
- `environment`
- `type`
- `owners`
- `criticality`

### availability

Describes required service continuity and failure behavior.

Suggested fields:

- `target`
- `failure_domains.availability_zone`
- `failure_domains.region`
- `dependency_expectations`

Avoid translating "high availability" directly into a specific architecture without defining the failure that must be tolerated.

### recovery

Suggested fields:

- `rto`
- `rpo`
- `backup_required`
- `restore_testing_required`
- `data_durability`

### networking

Suggested fields:

- `internet_facing`
- `ingress_sources`
- `outbound_internet`
- `private_connectivity`
- `service_discovery`
- `dns_requirements`

### data

Suggested fields:

- `persistent`
- `model`
- `sensitivity`
- `expected_size`
- `growth_rate`
- `transaction_characteristics`

### security

Suggested fields:

- `authentication`
- `authorization`
- `encryption_at_rest`
- `encryption_in_transit`
- `secrets_required`
- `audit_requirements`
- `compliance_constraints`

### workload_characteristics

Suggested fields:

- `execution_model`
- `expected_concurrency`
- `cpu_profile`
- `memory_profile`
- `storage_profile`
- `network_profile`
- `scaling_pattern`
- `latency_requirements`

### operations

Suggested fields:

- `monitoring`
- `centralized_logging`
- `alerting`
- `support_hours`
- `maintenance_windows`
- `deployment_frequency`
- `operational_owner`

### cost

Suggested fields:

- `priority`
- `budget`
- `optimization_constraints`

A cost priority might be `minimize`, `balanced`, or `performance_first`, but the framework should avoid pretending cost can be optimized without workload information.

### assumptions

Assumptions are explicitly accepted facts used to continue architecture work despite missing information.

Each assumption SHOULD be:

- specific;
- testable where possible;
- revisited when better information becomes available.

### unknowns

Unknowns are unresolved questions that may affect the design.

Agents should distinguish:

- unknowns that block architecture;
- unknowns that can safely use a documented assumption;
- unknowns that can be resolved during validation or operation.

## Architecture gate

Before moving from SPECIFY to ARCHITECT, the agent should determine whether unresolved information could materially affect:

- security;
- availability;
- data loss;
- compliance;
- major cost;
- irreversible architecture choices.

If so, the missing information should normally be resolved before implementation.
