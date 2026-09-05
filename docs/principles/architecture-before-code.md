# Architecture Before Code

## Principle

**Infrastructure code should implement an architecture. It should not be the mechanism by which the architecture is accidentally discovered.**

AI coding agents make it inexpensive to generate large amounts of syntactically plausible Infrastructure as Code. That changes the cost of implementation, but it does not remove the need for architecture.

IaCognition therefore requires infrastructure reasoning to begin with workload intent and material requirements rather than resource declarations.

## The failure mode

A common AI-assisted workflow looks like this:

```text
User request
    ↓
Resource selection
    ↓
Terraform generation
    ↓
Syntax validation
```

This can produce correct Terraform for the wrong architecture.

A valid configuration can still be:

- insecure;
- unnecessarily expensive;
- unable to survive required failures;
- operationally difficult;
- inconsistent with recovery objectives;
- incorrectly exposed to the network;
- poorly matched to workload scale;
- difficult to maintain or migrate.

Syntax is only one dimension of infrastructure correctness.

## The IaCognition approach

```text
Workload intent
      ↓
Material requirements
      ↓
Explicit assumptions
      ↓
Architecture decisions
      ↓
Infrastructure design
      ↓
IaC implementation
      ↓
Validation and review
```

The agent should know *why* a resource exists before deciding *how* to declare it.

## Material architecture dimensions

Before implementation, an infrastructure design should consider the dimensions that materially affect the workload. These commonly include:

### Availability

- production or non-production;
- acceptable outage duration;
- required failure domains;
- single-AZ or multi-AZ behavior;
- regional failure expectations;
- dependency availability.

### Recovery

- recovery time objective (RTO);
- recovery point objective (RPO);
- backup requirements;
- restore testing;
- data durability.

### Networking

- public versus private exposure;
- ingress sources;
- egress requirements;
- service-to-service communication;
- DNS and service discovery;
- connectivity to external systems.

### Security

- data sensitivity;
- authentication and authorization;
- least privilege;
- encryption;
- credential management;
- audit requirements.

### Workload behavior

- request-driven, event-driven, batch, scheduled, or continuous;
- stateful or stateless;
- expected concurrency;
- CPU, memory, storage, and network characteristics;
- scaling behavior.

### Operations

- monitoring;
- logging;
- alerting;
- deployment strategy;
- maintenance expectations;
- ownership and support model.

### Cost

- cost sensitivity;
- utilization pattern;
- elasticity;
- managed-service tradeoffs;
- availability-cost tradeoffs.

Not every workload requires exhaustive analysis of every dimension. The objective is to identify the dimensions capable of changing the architecture.

## Assumptions are engineering artifacts

When requirements are incomplete, agents MAY proceed using explicit assumptions when doing so is appropriate and reversible.

An assumption should be visible:

> Assumption: this is an internal non-production service and does not require multi-AZ availability.

This is preferable to silently designing a single-AZ system.

If an assumption could cause significant security, availability, data-loss, compliance, or cost consequences, the agent SHOULD obtain clarification rather than invent a default.

## Architecture decisions should be explainable

Material decisions should be traceable to requirements.

For example:

```text
Requirement:
The API must remain available after loss of one availability zone.

Decision:
Run application capacity across at least two AZs and avoid single-AZ
dependencies in the synchronous request path.

Implementation:
Create private application subnets in multiple AZs and distribute
compute through a multi-AZ load-balancing and scaling design.
```

This separates *requirement*, *decision*, and *implementation*.

That separation allows implementations to change without losing the reasoning that produced them.

## AI does not eliminate engineering judgment

IaCognition uses AI to make infrastructure reasoning faster, more consistent, and more accessible.

It does not assume that an AI agent can infer every organizational constraint, business requirement, or operational consequence from a short request.

Agents should expose uncertainty rather than hide it behind generated code.

## Practical rule

When a user asks for infrastructure code, the first question is not:

> Which Terraform resources should I create?

The first question is:

> What infrastructure behavior must this workload have?

That is the foundation of IaCognition.
