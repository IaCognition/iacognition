# Terraform Dependency and Version Management Analysis

### HC-DEP-001 — Declare provider requirements explicitly
**Disposition:** ADOPT

Each module MUST declare required provider sources and SHOULD declare compatible provider versions.

### HC-DEP-002 — Version constraints express compatibility
**Disposition:** ADOPT

Constraints SHOULD represent tested compatibility rather than merely freeze whatever version is currently installed.

### HC-DEP-003 — Lock files capture selected provider versions
**Disposition:** ADOPT

Root configurations SHOULD normally commit `.terraform.lock.hcl` so provider selection is reproducible and changes are reviewable.

### HC-DEP-004 — Constraints and locks are different controls
**Disposition:** ADOPT

IaCognition MUST distinguish acceptable-version constraints from the concrete provider versions selected in the lock file.

### HC-DEP-005 — Provider and module dependency locking differ
**Disposition:** ADOPT

Terraform's dependency lock file records provider selections, not remote module selections. Module versions should therefore be explicitly constrained when reproducibility matters.

### HC-DEP-006 — Upgrades are deliberate changes
**Disposition:** ADOPT

Provider/module upgrades SHOULD receive code review, plan review, and suitable validation.

### HC-DEP-007 — Terraform CLI compatibility is explicit
**Disposition:** ADOPT

Projects SHOULD declare a `required_version` constraint appropriate to the language features they depend on.
