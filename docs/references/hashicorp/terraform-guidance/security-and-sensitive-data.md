# Terraform Security and Sensitive Data Analysis

### HC-SEC-001 — State and plans may contain sensitive data
**Disposition:** ADOPT

Terraform state and saved plans SHOULD be treated as sensitive artifacts.

### HC-SEC-002 — `sensitive` redaction is not encryption
**Disposition:** ADOPT

IaCognition MUST NOT claim `sensitive = true` secures a value at rest; it primarily controls presentation while values can remain in state.

### HC-SEC-003 — Do not hard-code secrets
**Disposition:** ADOPT

Secrets SHOULD NOT be embedded in Terraform source. Credentials should be supplied through secure execution mechanisms.

### HC-SEC-004 — Secure remote state
**Disposition:** ADOPT

Production/shared state SHOULD use secure storage with least-privilege access, encryption, and appropriate auditing.

### HC-SEC-005 — State access is privileged infrastructure access
**Disposition:** ADOPT

State may reveal topology, identifiers, metadata, and secrets; access should be tightly controlled.

### HC-SEC-006 — Plan artifacts require protection
**Disposition:** ADOPT

Saved plans and CI artifacts SHOULD be protected in proportion to the information they contain.

### HC-SEC-007 — Terraform execution identity should be least privilege
**Disposition:** ADAPT

Terraform SHOULD run with identities scoped to the infrastructure responsibilities being managed rather than assuming broad administrator credentials.

### HC-SEC-008 — Protect the IaC delivery path
**Disposition:** ADOPT

Appropriate controls can include protected branches, PR review, secret scanning, dependency review, policy validation, and controlled deployment credentials.
