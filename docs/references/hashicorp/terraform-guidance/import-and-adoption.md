# Terraform Import and Adoption Analysis

This area directly supports IaCognition's modernization principle: **Adopt before you optimize.**

### HC-IMP-001 — Existing infrastructure can be adopted without recreation
**Disposition:** ADOPT

IaCognition SHOULD prefer import/adoption over unnecessary replacement when existing infrastructure is to become Terraform-managed.

### HC-IMP-002 — Import requires identity plus desired configuration
**Disposition:** ADOPT

Successful adoption requires inventory, resource identity, Terraform configuration, state association, plan reconciliation, and validation.

### HC-IMP-003 — Generated configuration is a starting point
**Disposition:** ADOPT

HashiCorp describes generated HCL as a best-guess template. It MUST be reviewed and normalized before becoming canonical module design.

### HC-IMP-004 — Reconcile to no unintended change
**Disposition:** ADAPT

IaCognition SHOULD iterate imported configuration until the plan contains no unintended changes before modernization begins.

### HC-IMP-005 — Separate adoption from optimization
**Disposition:** ADOPT

```text
Phase 1 — Capture / Adopt
Phase 2 — Modernize / Optimize
```

Combining these phases increases risk.

### HC-IMP-006 — Bulk import capability is version/provider dependent
**Disposition:** ADAPT

Current Terraform can query and generate configuration for supported resources, but workflows MUST verify Terraform-version and provider support.

### HC-IMP-007 — Preserve migration history
**Disposition:** ADOPT

Version-controlled import/removal/refactoring records SHOULD be preserved where supported.

### HC-IMP-008 — Stateful resources require extra caution
**Disposition:** ADOPT

Migration workflows MUST classify statefulness and data-loss risk before choosing recreate, import, move, backup/restore, or replacement.

## Candidate IaCognition workflow
```text
DISCOVER → INVENTORY → CAPTURE → GENERATE/WRITE → IMPORT → RECONCILE → NO UNINTENDED CHANGE → ARCHITECTURE ASSESSMENT → MODERNIZATION ROADMAP → STAGED OPTIMIZATION
```
