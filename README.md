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

- **Principles** explain the engineering philosophy behind the framework.
- **Rules** define normative behavior using MUST, MUST NOT, SHOULD, SHOULD NOT, and MAY.
- **Schemas** define structured inputs and outputs used by agents and humans.
- **Workflows** describe repeatable infrastructure-engineering processes.
- **Validation** defines how implementations and decisions are checked.

Terraform and AWS are the first implementation focus, but IaCognition is intended to remain conceptually independent of any single cloud provider, IaC language, or AI agent.

## Initial scope

The initial IaCognition releases focus on:

- infrastructure requirements and workload classification;
- architecture-first AI workflows;
- Terraform design and implementation;
- AWS reference architectures;
- security, reliability, operability, and cost reasoning;
- automated and human review of infrastructure changes;
- validation of Terraform examples and framework artifacts.

## Repository structure

```text
docs/         Engineering knowledge, principles, architecture, and workflows
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

## Status

IaCognition is in early development. The initial repository establishes the framework, lifecycle, vocabulary, schemas, and contribution model before expanding into detailed Terraform and AWS guidance.

Early contributions, criticism, architecture discussions, and reference implementations are welcome.

## License

IaCognition is licensed under the [Apache License 2.0](LICENSE).
