# Terraform Provider and Resource Design Analysis

### HC-PROV-001 — Provider source is explicit
**Disposition:** ADOPT

Modules MUST declare intended provider sources.

### HC-PROV-002 — Reusable modules should not own environment credentials
**Disposition:** ADAPT

Child modules SHOULD receive provider configurations from callers and avoid embedding environment authentication assumptions.

### HC-PROV-003 — Express real dependencies through references
**Disposition:** ADOPT

Prefer expression references that let Terraform infer dependencies. Use explicit `depends_on` only for genuine dependencies Terraform cannot infer.

### HC-PROV-004 — Resources imply lifecycle ownership
**Disposition:** ADOPT

A Terraform `resource` means Terraform is expected to manage the object's lifecycle unless explicit exceptions exist. Do not generate managed resources casually for externally owned infrastructure.

### HC-PROV-005 — Data/query mechanisms imply observation rather than ownership
**Disposition:** ADOPT

Externally managed objects should generally be referenced through data/query mechanisms when Terraform is not intended to own them.

### HC-PROV-006 — Provider behavior is independently versioned
**Disposition:** ADOPT

Provider schemas and resource semantics evolve independently from Terraform CLI and must be treated as external dependencies.

### HC-PROV-007 — Provider configuration should preserve architecture intent
**Disposition:** ADOPT

Terraform should remain traceable to the architecture it implements rather than optimize only for brevity.
