# Architecture Decision Model

IaCognition treats architecture as a series of explicit, traceable decisions.

## Decision sequence

A typical decision sequence is:

```text
Requirement
    ↓
Constraint
    ↓
Quality objective
    ↓
Architecture options
    ↓
Tradeoff analysis
    ↓
Decision
    ↓
Validation criterion
    ↓
Provider implementation
    ↓
IaC implementation
```

Provider resource selection SHOULD occur after the provider-neutral decision where practical.

## Architecture decision record

A material decision SHOULD capture:

### Decision

What is being decided?

### Drivers

Which requirements or constraints make the decision necessary?

### Options considered

What credible alternatives were considered?

### Selected approach

What approach was selected?

### Rationale

Why does the selected approach best satisfy the drivers?

### Tradeoffs

What disadvantages, costs, complexity, or limitations are accepted?

### Quality attributes affected

Which quality attributes are materially affected?

### Assumptions

Which assumptions influence the decision?

### Validation

How will the architecture decision be shown to work?

### Provider implementation

How is the provider-neutral decision implemented on the selected platform?

## Decision quality

A decision is weak when its rationale is primarily:

- "this is the default";
- "this is common";
- "the AI recommended it";
- "the Terraform module already does it";
- "the provider makes it easy";
- "this is best practice"

without connecting the recommendation to workload requirements.

A decision is stronger when it is traceable:

```text
Requirement
  ↓
Architecture reasoning
  ↓
Decision
  ↓
Implementation
  ↓
Evidence
```

## Reversibility

Architecture decisions SHOULD identify reversibility where material.

A decision that is expensive or risky to reverse deserves stronger evidence and review than an easily reversible decision.

## Provider selection

IaCognition SHOULD distinguish:

1. architecture requirement;
2. provider capability;
3. service selection;
4. implementation configuration.

Example:

```text
Requirement:
Survive loss of a single infrastructure location.

Architecture decision:
Deploy active workload capacity across independent failure domains.

AWS implementation:
Multiple Availability Zones.

Azure implementation:
Multiple Availability Zones.

Google Cloud implementation:
Multiple zones within an appropriate regional topology.
```

The requirement and decision remain canonical. Provider implementation belongs in provider-specific guidance or examples.
