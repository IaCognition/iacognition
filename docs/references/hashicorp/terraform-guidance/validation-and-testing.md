# Terraform Validation and Testing Analysis

HashiCorp provides several distinct validation mechanisms. IaCognition SHOULD preserve their different semantics.

### HC-VAL-001 — Formatting baseline
**Disposition:** ADOPT

Generated Terraform SHOULD pass `terraform fmt -check`.

### HC-VAL-002 — Static validation baseline
**Disposition:** ADOPT

`terraform validate` SHOULD be required, but success MUST NOT be interpreted as architectural, provider, security, reliability, or production-readiness proof.

### HC-VAL-003 — Plan evaluates proposed change
**Disposition:** ADOPT

Material changes SHOULD be evaluated with a plan against appropriate inputs and state. Review should detect unintended replacement, destruction, topology, privilege, exposure, and state-address changes.

### HC-VAL-004 — Validate inputs early
**Disposition:** ADOPT

Module variables SHOULD use deterministic validation where invalid input can be identified usefully.

### HC-VAL-005 — Preconditions encode assumptions
**Disposition:** ADOPT

Architecturally material assumptions that Terraform can verify SHOULD be candidates for preconditions.

### HC-VAL-006 — Postconditions encode guarantees
**Disposition:** ADOPT

Guarantees on which downstream infrastructure relies SHOULD be candidates for postconditions.

### HC-VAL-007 — Checks are non-blocking
**Disposition:** ADAPT

IaCognition MUST distinguish blocking safety requirements from `check` assertions, which report warnings rather than block operations.

### HC-VAL-008 — Terraform tests validate behavior
**Disposition:** ADOPT

Reusable modules SHOULD include Terraform tests for material behavioral contracts where practical.

### HC-VAL-009 — Mocking supplements integration testing
**Disposition:** ADAPT

Mock providers can validate logic cheaply but SHOULD NOT replace real-provider testing when behavior depends on provider APIs.

### HC-VAL-010 — Validation is layered
**Disposition:** ADOPT

```text
fmt → validate → lint/policy → tests → plan review → integration/provider evidence → architecture validation
```

Prefer deterministic evidence over model confidence.
