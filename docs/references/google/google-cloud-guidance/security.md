# Google Cloud Well-Architected — Security Analysis

## Source scope

This analysis covers the Security pillar of the Google Cloud Well-Architected Framework and related Google Cloud security architecture guidance.

Google's guidance emphasizes security by design, Zero Trust, least privilege, layered defenses, data protection, continuous validation, privacy, and compliance.

## Extracted concepts

### GCP-SEC-001 — Security is designed, not appended

**Source concept**

Security should be incorporated from the beginning of workload and platform design.

**Disposition:** ADOPT

**IaCognition normalization**

Material security requirements MUST be identified before infrastructure implementation.

Architecture SHOULD define:

- identity assumptions;
- trust boundaries;
- exposure;
- sensitive data;
- privilege requirements;
- security responsibilities.

**Provider neutrality:** High

---

### GCP-SEC-002 — Use explicit identity and authorization

**Source concept**

Google promotes Zero Trust principles that avoid treating network location as sufficient evidence of trust.

**Disposition:** ADAPT

**IaCognition normalization**

Access decisions SHOULD be based on authenticated identity and appropriate authorization context.

Network placement alone SHOULD NOT establish trust for sensitive operations.

**Provider neutrality:** High

---

### GCP-SEC-003 — Apply least privilege

**Source concept**

Users and workloads should have only the permissions required to perform their intended functions.

**Disposition:** ADOPT

**IaCognition normalization**

Human and workload identities SHOULD receive the minimum permissions necessary for their responsibilities.

Standing privilege SHOULD be minimized where temporary or workload-scoped access is practical.

**Provider neutrality:** High

---

### GCP-SEC-004 — Use defense in depth

**Source concept**

No single preventive control should be assumed sufficient.

**Disposition:** ADOPT

**IaCognition normalization**

Material security architectures SHOULD use multiple complementary controls across identity, network, workload, data, and monitoring layers.

**Provider neutrality:** High

---

### GCP-SEC-005 — Limit blast radius

**Source concept**

Architecture should contain the impact of compromised identities, services, or components.

**Disposition:** ADOPT

**IaCognition normalization**

Trust boundaries, privilege scopes, network segmentation, and data boundaries SHOULD limit the effect of individual control failures.

**Provider neutrality:** High

---

### GCP-SEC-006 — Data protection follows sensitivity and lifecycle

**Source concept**

Security controls should account for data sensitivity, location, access, transmission, retention, and destruction.

**Disposition:** ADOPT

**IaCognition normalization**

Workloads handling material data SHOULD classify it sufficiently to determine appropriate:

- access controls;
- encryption;
- retention;
- exposure;
- backup;
- destruction requirements.

**Provider neutrality:** High

---

### GCP-SEC-007 — Security posture requires continuous validation

**Source concept**

Google recommends ongoing assessment, monitoring, vulnerability detection, and policy enforcement.

**Disposition:** ADOPT

**IaCognition normalization**

Security posture SHOULD be continuously validated rather than inferred from original configuration.

Validation SHOULD detect:

- drift;
- vulnerable configurations;
- unexpected exposure;
- privilege expansion;
- control regressions.

**Provider neutrality:** High

---

### GCP-SEC-008 — Supply-chain security is part of infrastructure security

**Source concept**

Google promotes secure software and artifact supply chains, including provenance and integrity controls.

**Disposition:** ADAPT

**IaCognition normalization**

Infrastructure delivery pipelines SHOULD include controls appropriate to the risk of unauthorized, unreviewed, or compromised changes.

**Provider neutrality:** High

---

### GCP-SEC-009 — Privacy and compliance are architecture inputs

**Source concept**

Google includes privacy and regulatory obligations within workload security guidance.

**Disposition:** ADOPT

**IaCognition normalization**

Applicable privacy, regulatory, and compliance requirements SHOULD be identified as architecture constraints before implementation.

**Provider neutrality:** High

---

### GCP-SEC-010 — Secure recovery paths

**Source concept**

Backups, recovery systems, and alternate environments remain part of the workload security boundary.

**Disposition:** ADOPT

**IaCognition normalization**

Backup, replication, failover, and recovery mechanisms MUST NOT become weaker alternate paths around security requirements.

**Provider neutrality:** High

## Cross-pillar considerations

Security controls can affect:

- latency;
- availability;
- cost;
- operational complexity;
- deployment velocity.

Those tradeoffs SHOULD be explicit when material.
