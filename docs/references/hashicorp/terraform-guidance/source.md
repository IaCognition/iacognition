# HashiCorp Terraform Guidance

## Publisher
HashiCorp

## Source family
Authoritative Terraform language, CLI, module, state, validation, import, provider, and workflow guidance.

## Primary official sources
- https://developer.hashicorp.com/terraform/language/style
- https://developer.hashicorp.com/terraform/language/files
- https://developer.hashicorp.com/terraform/language/modules
- https://developer.hashicorp.com/terraform/language/modules/develop
- https://developer.hashicorp.com/terraform/language/modules/develop/structure
- https://developer.hashicorp.com/terraform/language/providers/requirements
- https://developer.hashicorp.com/terraform/language/files/dependency-lock
- https://developer.hashicorp.com/terraform/language/state
- https://developer.hashicorp.com/terraform/language/state/remote
- https://developer.hashicorp.com/terraform/language/state/backends
- https://developer.hashicorp.com/terraform/language/state/locking
- https://developer.hashicorp.com/terraform/language/state/refactor
- https://developer.hashicorp.com/terraform/language/manage-sensitive-data
- https://developer.hashicorp.com/terraform/language/validate
- https://developer.hashicorp.com/terraform/language/files/tests
- https://developer.hashicorp.com/terraform/language/tests/mocking
- https://developer.hashicorp.com/terraform/language/meta-arguments/lifecycle
- https://developer.hashicorp.com/terraform/language/block/check
- https://developer.hashicorp.com/terraform/language/import
- https://developer.hashicorp.com/terraform/language/import/generating-configuration
- https://developer.hashicorp.com/terraform/language/import/bulk

## Access date
2026-09-06

## Scope
This ingestion covers Terraform implementation concerns that should inform IaCognition after architecture decisions are known: configuration style, module design and structure, state/backends, dependencies and versions, validation/testing, workflow/lifecycle, security/sensitive data, provider/resource semantics, and import/adoption.

## IaCognition relationship
HashiCorp is authoritative for Terraform language and CLI behavior. Its engineering recommendations are strong evidence for IaCognition Terraform guidance, but they do not replace IaCognition's provider-neutral architecture framework.

```text
Architecture requirement
        ↓
Architecture decision
        ↓
Terraform representation
        ↓
Provider implementation
```

This package performs SOURCE → EXTRACT → NORMALIZE. Canonical incorporation into `docs/terraform/`, `schemas/`, `rules/`, `workflows/`, and `validation/` should occur separately.
