# Terraform Workflow and Lifecycle Analysis

### HC-WF-001 — Plan before apply
**Disposition:** ADOPT

Material infrastructure changes SHOULD produce a reviewable plan before execution.

### HC-WF-002 — Apply should execute reviewed intent
**Disposition:** ADOPT

Production apply SHOULD correspond to reviewed configuration and, where workflow permits, a reviewed plan.

### HC-WF-003 — Lifecycle meta-arguments are change controls
**Disposition:** ADOPT

`create_before_destroy`, `prevent_destroy`, `ignore_changes`, `replace_triggered_by`, preconditions, and postconditions affect infrastructure lifecycle and deserve review.

### HC-WF-004 — `ignore_changes` creates an ownership exception
**Disposition:** ADAPT

Material use SHOULD have a documented reason because it can legitimately divide ownership or conceal drift.

### HC-WF-005 — `prevent_destroy` is not a complete safety system
**Disposition:** ADAPT

It can protect sensitive resources but is not a substitute for backups, access control, recovery design, and review.

### HC-WF-006 — Refactoring should preserve infrastructure intent
**Disposition:** ADOPT

Use supported migration/refactoring constructs to prevent unintentional recreation.

### HC-WF-007 — Workflow safety depends on state and concurrency
**Disposition:** ADOPT

Plan/apply reasoning SHOULD account for state freshness, locking, concurrent changes, dependency versions, and environment inputs.
