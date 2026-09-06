# Architecture Validation and Review

IaCognition separates architecture intent from evidence that the architecture actually satisfies that intent.

## Review layers

Architecture review SHOULD consider at least four layers:

```text
REQUIREMENTS
    ↓
ARCHITECTURE
    ↓
IMPLEMENTATION
    ↓
EVIDENCE
```

## 1. Requirements review

Determine whether:

- functional scope is understood;
- quality objectives are identified;
- material constraints are explicit;
- assumptions are visible;
- unknowns have been acknowledged.

## 2. Architecture review

Determine whether:

- decisions trace to requirements;
- failure domains are understood;
- security boundaries are explicit;
- data lifecycle is defined;
- operational model is credible;
- cost model is plausible;
- performance model is credible;
- material tradeoffs are documented.

## 3. Implementation review

Determine whether implementation conforms to the architecture.

For Terraform this may include:

- resource topology;
- network placement;
- identity configuration;
- encryption;
- persistence;
- redundancy;
- monitoring;
- backup;
- provider configuration;
- state handling.

## 4. Evidence review

Determine whether the architecture objectives have been demonstrated.

Examples:

### Operational Excellence

- deploy/rollback tests;
- alerts;
- dashboards;
- runbooks;
- incident exercise.

### Security

- policy validation;
- threat model;
- access review;
- vulnerability scan;
- secret scan.

### Reliability

- restore test;
- failover test;
- failure injection;
- dependency failure test.

### Performance Efficiency

- load test;
- stress test;
- capacity analysis;
- production telemetry.

### Cost Optimization

- cost model;
- utilization evidence;
- budget controls;
- forecast.

### Sustainability

- utilization analysis;
- idle-resource analysis;
- retention analysis.

## Review severity

Findings MAY be classified as:

- `BLOCKER` — architecture or implementation cannot safely proceed.
- `MAJOR` — material risk or requirement gap that SHOULD be resolved.
- `MINOR` — improvement with limited immediate risk.
- `ADVISORY` — contextual recommendation or future consideration.

## Architecture confidence

AI-generated architecture SHOULD NOT be marked valid based on model confidence.

Confidence is not evidence.

Prefer:

- deterministic validation;
- provider data;
- tests;
- explicit calculations;
- reviewable reasoning.

## Review output

An architecture review SHOULD produce:

1. requirements assessed;
2. architecture decisions assessed;
3. findings;
4. tradeoffs;
5. unresolved assumptions;
6. required actions;
7. evidence reviewed;
8. residual risks.
