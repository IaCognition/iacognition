# Security Policy

IaCognition contains infrastructure guidance, rules, schemas, workflows, and executable examples. Defects in this material can have security consequences when adopted by downstream users.

## Reporting a security issue

Please do not open a public issue for a vulnerability that could cause users to deploy insecure infrastructure.

Use GitHub's private vulnerability reporting feature for this repository when available. If private reporting is not available, contact the project maintainers through the organization contact information rather than publishing exploit details.

A useful report includes:

- the affected file, rule, workflow, or example;
- the security impact;
- the conditions required for the issue to occur;
- a suggested correction, when known;
- whether the issue affects a specific cloud provider, Terraform version, or workload type.

## Scope

Security reports may include:

- IaCognition guidance that recommends an insecure architecture;
- Terraform examples that create unsafe defaults;
- validation logic that fails to detect a documented security requirement;
- workflows that could expose credentials or sensitive values;
- agent instructions that encourage unsafe infrastructure changes;
- dependency or automation vulnerabilities in repository tooling.

## Security philosophy

IaCognition treats security as an architectural concern, not merely a post-generation scan.

Security considerations should be incorporated during specification and architecture, validated during implementation, and reviewed again before operation.
