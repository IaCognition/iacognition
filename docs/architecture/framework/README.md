# IaCognition Architecture Framework

> Architect before you code.

The IaCognition Architecture Framework is a provider-neutral model for reasoning about infrastructure architecture before Infrastructure as Code implementation.

It is derived from cross-provider normalization of authoritative architecture guidance from:

- Amazon Web Services Well-Architected Framework;
- Microsoft Azure Well-Architected Framework and Azure Architecture Center;
- Google Cloud Well-Architected Framework and Google Cloud Architecture Center.

The framework does not reproduce any provider framework. It identifies infrastructure-engineering concepts that remain useful after provider terminology, services, and implementation details are removed.

## Purpose

The framework gives humans and AI agents a consistent way to move from workload intent to architecture decisions before selecting cloud services or generating Terraform.

It is designed to answer questions such as:

- What requirements must be known before implementation?
- Which quality attributes materially affect this workload?
- What failure domains must the architecture tolerate?
- What security boundaries and identities exist?
- What performance objectives must be met?
- What cost constraints matter?
- What operational capabilities are required?
- What sustainability objectives apply?
- What tradeoffs are being made?
- How will the resulting architecture be validated?

## Architecture lifecycle

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

This framework primarily governs `SPECIFY`, `ARCHITECT`, `VALIDATE`, and `REVIEW`, while informing all lifecycle stages.

## Framework model

IaCognition treats workload architecture as the result of four interacting elements:

```text
WORKLOAD INTENT
      │
      ▼
REQUIREMENTS + CONSTRAINTS
      │
      ▼
ARCHITECTURE DECISIONS
      │
      ├───────────────┐
      ▼               ▼
QUALITY ATTRIBUTES   TRADEOFFS
      │               │
      └───────┬───────┘
              ▼
       VALIDATED DESIGN
              │
              ▼
      IaC IMPLEMENTATION
```

## Quality attributes

IaCognition currently recognizes six first-class architecture quality attributes:

1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

The first five are strongly convergent across AWS, Microsoft Azure, and Google Cloud architecture guidance.

Sustainability is explicitly represented as a top-level pillar by AWS and Google Cloud. Microsoft treats sustainability as an additional architecture design concern rather than one of the five core Azure Well-Architected pillars.

Quality attributes are not independent. Architecture decisions frequently improve one while increasing cost, complexity, latency, operational burden, or another quality attribute.

## Foundational invariants

The framework establishes the following invariants:

1. Architecture decisions MUST be grounded in explicit requirements or explicit assumptions.
2. Provider services SHOULD be selected after architectural intent is known.
3. Material tradeoffs SHOULD be recorded.
4. Quality objectives SHOULD be measurable where practical.
5. Failure and recovery behavior SHOULD be designed before production deployment.
6. Security boundaries and identity assumptions SHOULD be explicit.
7. Operational readiness is part of architecture readiness.
8. Cost is an architecture input, not only a post-deployment optimization task.
9. Architecture SHOULD be validated using evidence rather than inferred from configuration presence.
10. Reference architectures and patterns MUST be evaluated against workload context before reuse.
11. Architecture SHOULD remain traceable to implementation.
12. Operational evidence MAY invalidate prior architecture assumptions and trigger redesign.

## Files in this framework

- `core-principles.md` — provider-neutral foundational principles.
- `quality-attributes.md` — quality-attribute model and interactions.
- `workload-requirements.md` — minimum architecture input model.
- `architecture-decision-model.md` — how architecture decisions are formed and recorded.
- `operational-excellence.md` — provider-neutral operational quality model.
- `security.md` — provider-neutral security architecture model.
- `reliability.md` — provider-neutral reliability architecture model.
- `performance-efficiency.md` — provider-neutral performance architecture model.
- `cost-optimization.md` — provider-neutral cost architecture model.
- `sustainability.md` — provider-neutral sustainability model.
- `validation-and-review.md` — architecture validation and review model.
- `provider-traceability.md` — provenance and cross-provider normalization map.

## Relationship to canonical IaCognition artifacts

These documents define architecture guidance.

Normative machine-consumable requirements SHOULD be promoted separately into:

```text
rules/
schemas/
validation/
```

Executable provider implementations SHOULD belong in:

```text
examples/
```

Provider-specific implementation guidance SHOULD remain distinct from this provider-neutral framework.

## Source provenance

The normalized source analyses are maintained under:

```text
docs/references/amazon/aws-well-architected/
docs/references/microsoft/azure-guidance/
docs/references/google/google-cloud-guidance/
```

Those directories are evidence and provenance. This directory is canonical IaCognition architecture guidance.
