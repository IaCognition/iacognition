# IaCognition Validation

IaCognition distinguishes AI reasoning from deterministic validation.

An AI agent may explain why an implementation appears correct. Validation should provide evidence that can be checked independently.

## Validation layers

IaCognition validation is expected to evolve across several layers.

### Framework validation

Checks the IaCognition repository itself:

- Markdown quality;
- broken links;
- schema correctness;
- duplicate rule identifiers;
- invalid cross-references;
- inconsistent metadata.

### IaC validation

Checks Infrastructure as Code:

- formatting;
- initialization;
- syntax and provider validation;
- linting;
- policy checks;
- security scanning;
- tests.

For Terraform, a baseline may include:

```text
terraform fmt -check
terraform init -backend=false
terraform validate
tflint
```

Additional security and policy tooling may be added as the framework matures.

### Plan validation

A valid configuration does not guarantee a safe change.

Terraform plan analysis should identify:

- unexpected resource replacement;
- destructive changes;
- privilege expansion;
- public exposure;
- topology changes;
- persistence changes;
- significant cost-impacting changes.

### Architecture validation

Architecture validation asks whether the implementation satisfies the declared requirements and decisions.

Examples:

- Does a workload that requires AZ-failure tolerance actually avoid single-AZ dependencies?
- Is a workload declared private exposed through a public endpoint?
- Does the recovery architecture support the stated RPO?
- Does the implementation contradict an explicit architecture decision?

## Principle

**Prefer deterministic evidence over model confidence.**

AI review is useful for reasoning about architecture and tradeoffs, but deterministic tools should be used wherever the question can be answered mechanically.
