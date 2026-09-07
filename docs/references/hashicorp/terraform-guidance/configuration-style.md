# Terraform Configuration Style Analysis

## Normalized concepts

### HC-STYLE-001 — Canonical formatting
**Disposition:** ADOPT

Generated or modified Terraform SHOULD pass `terraform fmt` before review or delivery.

### HC-STYLE-002 — Static validation before commit
**Disposition:** ADOPT

Terraform SHOULD pass `terraform validate` before it is considered implementation-complete. Passing validation does not prove architectural correctness.

### HC-STYLE-003 — Module files form one configuration document
**Disposition:** ADOPT

Terraform evaluates all top-level configuration files in a module together. IaCognition MUST NOT infer execution semantics from filenames or file ordering.

### HC-STYLE-004 — Inputs and outputs are documented interfaces
**Disposition:** ADOPT

Reusable inputs SHOULD have explicit types and descriptions; outputs SHOULD be described and expose only useful interface values.

### HC-STYLE-005 — Avoid needless abstraction
**Disposition:** ADAPT

IaCognition SHOULD NOT convert every literal into a variable or every expression into a local. Abstraction should express real variability or intent.

### HC-STYLE-006 — Resource labels express purpose
**Disposition:** ADAPT

Terraform labels SHOULD communicate workload or architectural role rather than redundantly repeat provider resource type.

### HC-STYLE-007 — Use `count` and `for_each` deliberately
**Disposition:** ADAPT

Meta-arguments SHOULD improve correctness or maintainability. Address stability must be considered when choosing collection semantics.

### HC-STYLE-008 — Provider configuration is explicit
**Disposition:** ADAPT

Root modules SHOULD make provider requirements and intended configurations explicit. Reusable modules SHOULD avoid embedding environmental credentials.
