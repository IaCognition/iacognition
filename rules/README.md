# IaCognition Rules

This directory contains IaCognition's normative, machine-consumable engineering rules.

Explanatory guidance belongs under `docs/`. Rules should be concise enough that both humans and AI agents can determine whether an architecture or implementation complies.

## Normative terms

Rules use:

- **MUST**
- **MUST NOT**
- **SHOULD**
- **SHOULD NOT**
- **MAY**

A rule should not use mandatory language unless IaCognition deliberately intends to establish a requirement.

## Intended organization

```text
rules/
├── architecture/
├── security/
├── reliability/
├── terraform/
└── operations/
```

As the framework evolves, rules should receive stable identifiers so validation and review results can reference them without relying solely on filenames or headings.

Example:

```text
IACOG-SEC-001
```

## Rule design

A useful rule should identify:

- the requirement;
- when it applies;
- allowed exceptions or conditions;
- the rationale or canonical documentation reference;
- how compliance can be verified when practical.

Rules should not merely restate cloud-provider documentation.
