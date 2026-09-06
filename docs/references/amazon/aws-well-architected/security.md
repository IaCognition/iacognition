# AWS Well-Architected — Security Analysis

## Source scope

This analysis covers the Security pillar of the AWS Well-Architected Framework.

## AWS focus areas

AWS security guidance spans:

- security foundations;
- identity and access management;
- detection;
- infrastructure protection;
- data protection;
- incident response;
- application security.

## Extracted concepts

### AWS-SEC-001 — Establish a strong identity foundation

**Disposition:** ADAPT

**Normalized concept:** Infrastructure architecture MUST define an identity and authorization model before implementation. Least privilege, separation of duties, and centralized or otherwise consistently governed identity SHOULD be applied where appropriate. Long-lived static credentials SHOULD be avoided when safer temporary or workload-identity mechanisms are available.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `schemas/architecture/`

### AWS-SEC-002 — Maintain traceability

**Disposition:** ADOPT

**Normalized concept:** Security-relevant actions and material infrastructure changes SHOULD produce durable, attributable audit evidence sufficient for detection, investigation, and accountability.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `validation/`

### AWS-SEC-003 — Apply security at multiple layers

**Disposition:** ADOPT

**Normalized concept:** Workloads SHOULD use layered security controls so that failure or bypass of a single control does not automatically expose a protected asset.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `docs/architecture/security/`

### AWS-SEC-004 — Automate security controls and verification

**Disposition:** ADOPT

**Normalized concept:** Repeatable security controls, policy checks, configuration validation, and remediation SHOULD be automated when deterministic automation can reduce drift and human error without introducing unacceptable operational risk.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `validation/`

### AWS-SEC-005 — Protect data according to sensitivity and lifecycle

**Disposition:** ADAPT

**Normalized concept:** Workloads SHOULD classify material data and define required protections for data at rest, in transit, in use where applicable, during backup, and during deletion or retirement.

**Provider neutrality:** High

**Candidate destinations:** `schemas/workload/`, `rules/security/`

### AWS-SEC-006 — Minimize direct human access to sensitive data

**Disposition:** ADOPT

**Normalized concept:** Administrative workflows SHOULD minimize unnecessary direct access to sensitive production data and SHOULD prefer controlled, audited, purpose-specific mechanisms.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `docs/standards/`

### AWS-SEC-007 — Prepare and test incident response

**Disposition:** ADOPT

**Normalized concept:** Security incident response capabilities SHOULD be prepared before an incident, including access, tooling, evidence preservation, playbooks, communications, and periodic exercises appropriate to workload risk.

**Provider neutrality:** High

**Candidate destinations:** `rules/security/`, `validation/`, `docs/workflows/`

### AWS-SEC-008 — Embed security throughout delivery

**Disposition:** ADOPT

**Normalized concept:** Infrastructure and application delivery pipelines SHOULD perform security validation throughout design, implementation, review, and deployment rather than relying only on post-deployment inspection.

**Provider neutrality:** High

**Candidate destinations:** `validation/`, `rules/security/`

## IaCognition implications

Security is not a post-generation Terraform scan. IaCognition should require security requirements, identities, trust boundaries, data sensitivity, exposure, auditability, and incident-readiness decisions before infrastructure implementation, then validate that the IaC satisfies those decisions.
