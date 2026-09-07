# Extracted Principles — HashiCorp Terraform Guidance

### HC-X001 — Terraform implements architecture; it does not replace architecture
**Disposition:** ADOPT

### HC-X002 — State is a first-class infrastructure control artifact
**Disposition:** ADOPT

State affects ownership, blast radius, lifecycle, collaboration, security, and recovery.

### HC-X003 — Declarative history is preferable to opaque state surgery
**Disposition:** ADOPT

### HC-X004 — Modules should express coherent reusable capabilities
**Disposition:** ADOPT

### HC-X005 — Prefer composition over deep nesting
**Disposition:** ADOPT

### HC-X006 — Reproducibility requires explicit dependency management
**Disposition:** ADOPT

Provider requirements, constraints, lock files, and deliberate upgrades are complementary controls.

### HC-X007 — Validation is layered
**Disposition:** ADOPT

Formatting, static validation, tests, plan review, provider evidence, and architecture validation answer different questions.

### HC-X008 — Sensitive Terraform artifacts require protection
**Disposition:** ADOPT

### HC-X009 — Resource addresses are operationally significant
**Disposition:** ADOPT

### HC-X010 — Imported infrastructure should be reconciled before optimization
**Disposition:** ADOPT

### HC-X011 — Generated configuration is evidence, not final design
**Disposition:** ADOPT

### HC-X012 — Root modules and reusable modules have different responsibilities
**Disposition:** ADOPT

### HC-X013 — Lifecycle controls encode change semantics
**Disposition:** ADOPT

### HC-X014 — Terraform provider behavior is independently versioned
**Disposition:** ADOPT

### HC-X015 — Deterministic evidence should supersede AI confidence
**Disposition:** ADOPT

## Overall assessment
The strongest incorporation targets are Terraform module rules, state architecture rules, dependency/version rules, the validation pipeline, sensitive-data rules, import/adoption workflow, state-safe refactoring, and provider/resource ownership semantics.
