# Contributing to IaCognition

IaCognition is intended to become a rigorous, machine-consumable infrastructure-engineering framework. Contributions should improve the quality of both human and AI infrastructure decisions.

## Ways to contribute

Useful contributions include:

- engineering principles;
- architecture guidance;
- normative infrastructure rules;
- Terraform patterns and anti-patterns;
- reference architectures;
- validation techniques;
- workload and architecture schemas;
- agent workflows;
- corrections and clarifications;
- executable examples.

## Contribution principles

Contributions should follow these rules:

1. **Architecture should precede implementation.** Avoid adding code examples that imply an architectural choice without explaining the choice.
2. **Separate knowledge from rules.** Explanatory material belongs under `docs/`; normative requirements belong under `rules/`.
3. **Avoid agent lock-in.** Canonical knowledge must not depend on a specific AI product. Agent-specific integrations belong under `agents/`.
4. **Prefer explicit assumptions.** If guidance depends on workload type, availability goals, security posture, scale, or cost priorities, state those dependencies.
5. **Avoid universal claims without justification.** Infrastructure engineering is contextual. Use MUST only for rules the framework deliberately treats as mandatory.
6. **Make examples production-conscious.** Examples should account for security, observability, lifecycle, and failure behavior when relevant.
7. **Prefer verifiable outcomes.** Wherever possible, define how a recommendation or implementation can be validated.

## Normative language

IaCognition uses the following terms deliberately:

- **MUST / MUST NOT** — mandatory framework requirement.
- **SHOULD / SHOULD NOT** — expected default; deviation requires a reason.
- **MAY** — acceptable optional behavior.

Do not use these terms casually in explanatory prose.

## Pull requests

A good pull request should:

- describe the problem being addressed;
- identify the affected framework area;
- explain important architectural reasoning;
- identify new assumptions or dependencies;
- include or update validation where appropriate;
- avoid unrelated changes.

For significant changes to the lifecycle, schemas, or core principles, open an issue first so the architecture can be discussed before implementation.

## Terraform contributions

Terraform examples should eventually pass the repository's automated checks, including formatting and validation. Do not include credentials, account identifiers, private endpoints, secrets, or organization-specific infrastructure details.

## AI-generated contributions

AI-assisted contributions are welcome, but the contributor remains responsible for correctness.

AI-generated material must be reviewed for:

- fabricated resource behavior;
- incorrect cloud-provider assumptions;
- security regressions;
- hidden availability assumptions;
- obsolete Terraform syntax;
- unnecessary complexity;
- unsupported cost or reliability claims.

The fact that an AI agent produced a change is never evidence that the change is correct.

## Licensing

By contributing, you agree that your contribution will be licensed under the Apache License 2.0 used by this repository.
