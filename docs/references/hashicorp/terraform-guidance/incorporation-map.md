# HashiCorp Terraform Guidance Incorporation Map

All concepts in this ingestion are **Proposed** until a separate IaCognition incorporation change.

| Area | Normalized concept | Candidate destination |
|---|---|---|
| Style | Canonical formatting and validation | `rules/terraform/`, `validation/` |
| Style | Typed/documented interfaces | `rules/terraform/` |
| Modules | Coherent capability modules | `docs/terraform/`, `rules/terraform/` |
| Modules | Avoid over-modularization / prefer flat composition | `rules/terraform/` |
| Modules | Standard module structure | `rules/terraform/`, `examples/` |
| State | State is a critical managed artifact | `docs/terraform/`, `rules/terraform/` |
| State | Secure remote state and locking | `rules/security/`, `rules/terraform/` |
| State | State boundaries reflect architecture/ownership | `schemas/architecture/`, `docs/architecture/` |
| State | Declarative migration/refactoring | `workflows/` |
| Dependencies | Provider requirements and constraints | `rules/terraform/` |
| Dependencies | Commit root lock files | `rules/terraform/` |
| Dependencies | Upgrades are deliberate | `workflows/`, `validation/` |
| Validation | fmt/validate/tests/plan as distinct layers | `validation/` |
| Validation | Preconditions and postconditions | `rules/terraform/` |
| Validation | Checks are non-blocking | `rules/terraform/`, `validation/` |
| Security | State/plans may contain sensitive data | `rules/security/` |
| Security | `sensitive` redaction is not encryption | `rules/security/` |
| Security | Least-privilege execution identity | `rules/security/` |
| Provider design | Explicit provider source/configuration | `rules/terraform/` |
| Provider design | Managed resource vs observed data ownership | `docs/terraform/`, `rules/terraform/` |
| Adoption | Import before unnecessary recreation | `workflows/` |
| Adoption | Generated configuration requires normalization | `workflows/`, `rules/terraform/` |
| Adoption | Reconcile before modernization | `workflows/`, `validation/` |
| Adoption | Adopt before optimize | `docs/principles/`, `workflows/` |

## Recommended incorporation sequence
```text
Canonical architecture framework
            +
HashiCorp Terraform normalization
            ↓
Terraform implementation model
            ↓
Schemas
            ↓
Stable normative rules
            ↓
Workflows
            ↓
Validation
            ↓
Examples
```

Future rules should retain traceability:

```text
HashiCorp source → HC-* concept → IaCognition normalized principle → IACOG-TF-* rule → implementation → validation evidence
```
