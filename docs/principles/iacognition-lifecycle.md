# The IaCognition Lifecycle

IaCognition defines an architecture-driven lifecycle for AI-assisted infrastructure engineering.

```text
INTENT
  ↓
SPECIFY
  ↓
ARCHITECT
  ↓
IMPLEMENT
  ↓
VALIDATE
  ↓
REVIEW
  ↓
OPERATE
  ↺
```

The stages are deliberately ordered. Implementation begins only after enough information exists to make defensible architecture decisions.

## 1. INTENT

Understand what the infrastructure is intended to accomplish.

Inputs may include:

- business objective;
- application or service purpose;
- environment;
- users or dependent systems;
- expected operating model;
- known constraints.

The output is a concise statement of workload intent.

## 2. SPECIFY

Convert intent into material infrastructure requirements.

Relevant areas can include:

- availability;
- recovery;
- networking;
- security;
- workload characteristics;
- data persistence;
- scale;
- operations;
- compliance;
- cost.

The specification should distinguish known requirements from assumptions.

The IaCognition workload schema provides a structured starting point.

## 3. ARCHITECT

Turn requirements into explicit infrastructure decisions.

Examples:

- failure-domain strategy;
- public versus private placement;
- compute model;
- persistence model;
- load-balancing strategy;
- identity boundaries;
- scaling approach;
- backup and recovery architecture.

Architecture decisions should describe reasoning and tradeoffs, not merely list resources.

## 4. IMPLEMENT

Translate the approved architecture into Infrastructure as Code.

Implementation includes:

- resource declarations;
- modules;
- variables and outputs;
- dependency relationships;
- provider configuration;
- environment-specific configuration.

Terraform is IaCognition's initial implementation focus.

Implementation MUST remain traceable to the architecture it realizes.

## 5. VALIDATE

Use deterministic tools wherever possible to test implementation quality.

Validation may include:

- formatting;
- syntax validation;
- provider validation;
- linting;
- policy checks;
- security scanning;
- tests;
- plan analysis;
- schema validation;
- cross-reference validation.

AI review does not replace deterministic validation.

## 6. REVIEW

Evaluate the result as an infrastructure system rather than only as code.

Review should consider:

- architecture;
- security;
- reliability;
- recoverability;
- operability;
- maintainability;
- cost;
- consistency with stated requirements.

A technically valid Terraform plan can still fail review.

## 7. OPERATE

Deployment creates evidence.

Operational information can include:

- incidents;
- alerts;
- scaling behavior;
- observed utilization;
- cost;
- failure behavior;
- drift;
- deployment problems;
- recovery exercises.

That evidence should feed back into requirements, architecture, rules, and reference patterns.

This feedback loop is why the lifecycle is cyclic rather than linear.

## Lifecycle invariants

Across all stages:

1. Assumptions should be explicit.
2. Material decisions should be traceable.
3. Deterministic evidence is preferred over model confidence.
4. Provider-specific implementation should not silently become provider-neutral principle.
5. Validation should test the architecture's intended behavior whenever practical.
6. Operational evidence may invalidate earlier assumptions.

## Lightweight use

IaCognition does not require bureaucracy for simple infrastructure.

A small non-production workload may move through INTENT, SPECIFY, and ARCHITECT in a few paragraphs.

The lifecycle exists to ensure that reasoning occurs—not to require unnecessary documentation.
