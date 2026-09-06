# IaCognition

**Architecture-driven AI for Infrastructure as Code.**

> Architect before you code.

IaCognition is an open-source framework for applying AI agents to infrastructure engineering—from workload intent and architecture decisions through Infrastructure as Code (IaC) implementation, validation, review, and operational readiness.

IaCognition is built around a simple premise:

**An AI agent should reason about infrastructure before it writes infrastructure code.**

Modern AI coding assistants can generate syntactically valid Terraform quickly. That is useful, but syntax is not architecture. Production infrastructure also requires decisions about availability, failure domains, security boundaries, networking, data persistence, operability, cost, lifecycle, and organizational constraints.

IaCognition provides a structured way to make those decisions explicit and machine-consumable.

## The IaCognition lifecycle

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

The lifecycle intentionally places architecture before implementation. Infrastructure code should be the implementation of an architectural decision, not the mechanism by which the architecture is accidentally discovered.

## What IaCognition provides

IaCognition is organized around five kinds of artifacts:

* **Principles** explain the engineering philosophy behind the framework.
* **Rules** define normative behavior using MUST, MUST NOT, SHOULD, SHOULD NOT, and MAY.
* **Schemas** define structured inputs and outputs used by agents and humans.
* **Workflows** describe repeatable infrastructure-engineering processes.
* **Validation** defines how implementations and decisions are checked.

Terraform and AWS are the first implementation focus, but IaCognition is intended to remain conceptually independent of any single cloud provider, IaC language, or AI agent.

## Initial scope

The initial IaCognition releases focus on:

* infrastructure requirements and workload classification;
* architecture-first AI workflows;
* Terraform design and implementation;
* AWS reference architectures;
* security, reliability, operability, and cost reasoning;
* automated and human review of infrastructure changes;
* validation of Terraform examples and framework artifacts.

## Repository structure

```text
docs/         Engineering knowledge, principles, architecture, workflows,
              and source references
rules/        Normative machine-consumable rules
schemas/      Structured workload, architecture, and review definitions
validation/   Validation requirements and tooling guidance
examples/     Reference architectures and executable examples
agents/       Thin integrations for specific AI coding agents
```

The canonical IaCognition knowledge belongs in the framework directories above. Agent-specific files should act as adapters into that knowledge rather than duplicate it.

## Core principles

IaCognition starts with several foundational principles:

1. **Architect before you code.**
2. **Treat infrastructure requirements as explicit engineering inputs.**
3. **Separate architecture decisions from implementation details.**
4. **Prefer verifiable decisions over plausible AI output.**
5. **Validate security, reliability, operability, and cost—not only syntax.**
6. **Use AI to augment engineering judgment, not conceal missing requirements.**
7. **Make assumptions explicit.**
8. **Treat infrastructure knowledge as versioned engineering material.**

See [Architecture Before Code](docs/principles/architecture-before-code.md) and the [IaCognition Lifecycle](docs/principles/iacognition-lifecycle.md).

## Knowledge sources and incorporation

IaCognition incorporates engineering knowledge from authoritative public sources while maintaining its own independent, structured body of infrastructure-engineering guidance.

Public sources are treated as **evidence and inputs**, not as the canonical IaCognition knowledge base.

Source material follows a controlled incorporation process:

```text
SOURCE
  ↓
EXTRACT
  ↓
NORMALIZE
  ↓
INCORPORATE
```

### Source

Identify the authoritative source, its publisher, applicable version or publication date, access date, scope, and relevance to IaCognition.

Primary sources are preferred wherever practical, including cloud-provider documentation, Infrastructure as Code documentation, standards bodies, security frameworks, and authoritative engineering guidance.

### Extract

Identify the engineering principles, requirements, patterns, constraints, and practices that are materially relevant to infrastructure engineering.

Extraction focuses on engineering meaning rather than reproducing source material.

### Normalize

Translate useful concepts into IaCognition's architecture-first vocabulary and determine their appropriate scope.

During normalization, source concepts are classified as:

* **ADOPT** — the concept is consistent with IaCognition and can be incorporated substantially as expressed.
* **ADAPT** — the underlying concept is useful but should be generalized, narrowed, clarified, or expressed differently within IaCognition.
* **REJECT** — the concept is intentionally not incorporated because it is inappropriate for the framework, overly provider-specific, insufficiently justified, or inconsistent with IaCognition principles.

Provider-specific recommendations must not silently become provider-neutral principles.

Conflicting guidance from multiple sources should be reconciled explicitly rather than blended without explanation.

### Incorporate

Accepted concepts are incorporated into the appropriate canonical IaCognition artifacts:

```text
Source knowledge
      ↓
Principles
Rules
Schemas
Workflows
Patterns
Anti-patterns
Validation
Examples
```

Each incorporated concept should remain traceable to its source while the resulting IaCognition guidance stands on its own.

Source references and incorporation records belong under `docs/references/`. Canonical engineering guidance belongs in the appropriate framework directories and should not be duplicated inside agent-specific integrations.

Detailed source-ingestion conventions are defined in [`docs/references/README.md`](docs/references/README.md).

## Status

IaCognition is in early development. The initial repository establishes the framework, lifecycle, vocabulary, schemas, and contribution model before expanding into detailed Terraform and AWS guidance.

Early contributions, criticism, architecture discussions, and reference implementations are welcome.

## License

IaCognition is licensed under the [Apache License 2.0](LICENSE).
