# IaCognition Agent Instructions

This repository is an infrastructure-engineering knowledge framework. AI agents working in this repository MUST preserve the separation between architecture reasoning, normative rules, schemas, workflows, validation, and implementation examples.

## Primary operating principle

**Architect before you code.**

Before generating or materially changing infrastructure code, determine whether the workload requirements and architecture decisions needed to justify that change are known.

Read:

- `docs/principles/architecture-before-code.md`
- `docs/principles/iacognition-lifecycle.md`
- `schemas/workload/workload-definition.md`

## Repository semantics

- `docs/` contains explanatory engineering knowledge.
- `rules/` contains normative requirements.
- `schemas/` contains structured definitions used to describe workloads, decisions, and reviews.
- `validation/` defines verification requirements.
- `examples/` contains concrete implementations and reference architectures.
- `agents/` contains product-specific adapters. Do not make agent-specific files the canonical source of framework knowledge.

## Agent behavior

When designing infrastructure:

1. Establish workload intent.
2. Identify missing material requirements.
3. State assumptions explicitly.
4. Classify the workload.
5. Make architecture decisions before choosing IaC resources.
6. Explain material tradeoffs.
7. Implement the chosen architecture.
8. Validate the implementation.
9. Review security, reliability, operability, maintainability, and cost.
10. Revisit assumptions when validation contradicts the design.

Do not begin by generating Terraform solely because Terraform was requested.

## Changes to this repository

When modifying IaCognition itself:

- preserve terminology used by the framework;
- prefer links to canonical documents over duplicated guidance;
- place normative requirements under `rules/`;
- place explanatory content under `docs/`;
- do not introduce provider-specific assumptions into provider-neutral principles;
- do not claim a recommendation is universal when it depends on workload context;
- update cross-references when moving or renaming files.

## Infrastructure safety

Never include real credentials, secrets, private keys, production account identifiers, proprietary endpoints, or organization-specific confidential values in examples.

Infrastructure examples should default toward safe deployment patterns and should clearly identify intentionally simplified behavior.
