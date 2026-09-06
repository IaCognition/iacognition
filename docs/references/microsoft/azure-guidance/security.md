# Microsoft Azure Well-Architected — Security Analysis

## Source scope

This analysis covers the Security pillar of the Microsoft Azure Well-Architected Framework.

Microsoft explicitly anchors the pillar in Zero Trust and the confidentiality, integrity, and availability properties of workload assets.

## Extracted concepts

### AZ-SEC-001 — Security is an architectural requirement

**Source concept**

Security must be considered in architecture, design choices, development, and operations rather than applied only after deployment.

**Disposition:** ADOPT

**IaCognition normalization**

Material security requirements MUST be identified before infrastructure implementation.

Architecture SHOULD establish trust boundaries, identity assumptions, data sensitivity, exposure, and security responsibilities before resources are selected.

**Provider neutrality:** High

---

### AZ-SEC-002 — Verify explicitly

**Source concept**

Microsoft Zero Trust guidance emphasizes explicit verification of identities and access context.

**Disposition:** ADAPT

**IaCognition normalization**

Access decisions SHOULD be based on authenticated identity and appropriate authorization context rather than implicit network location or assumed trust.

**Provider neutrality:** High

---

### AZ-SEC-003 — Enforce least privilege

**Source concept**

Permissions should be limited by identity, scope, duration, and asset.

**Disposition:** ADOPT

**IaCognition normalization**

Human and workload access SHOULD use the minimum permissions and duration necessary to perform the intended operation.

Standing privileged access SHOULD be avoided when temporary or workload-scoped mechanisms are practical.

**Provider neutrality:** High

---

### AZ-SEC-004 — Assume controls can fail

**Source concept**

Microsoft's Zero Trust model includes an assume-breach posture and recommends controls that limit blast radius when a primary defense fails.

**Disposition:** ADAPT

**IaCognition normalization**

Security architecture SHOULD assume individual preventive controls can fail.

Architectures SHOULD use segmentation, isolation, bounded privilege, monitoring, and compensating controls to limit impact.

**Provider neutrality:** High

---

### AZ-SEC-005 — Security boundaries should follow risk and business requirements

**Source concept**

Microsoft recommends segmentation of workload environments, processes, data, and team responsibilities according to criticality and business requirements.

**Disposition:** ADOPT

**IaCognition normalization**

Trust and security boundaries SHOULD be explicit architectural artifacts.

Boundary strength SHOULD reflect workload criticality, data sensitivity, regulatory requirements, and blast-radius objectives.

**Provider neutrality:** High

---

### AZ-SEC-006 — Data protection depends on classification

**Source concept**

Data should be classified and protected according to sensitivity and risk throughout its lifecycle.

**Disposition:** ADOPT

**IaCognition normalization**

Workloads that process or store material data SHOULD classify that data sufficiently to determine appropriate access controls, encryption, retention, and exposure constraints.

**Provider neutrality:** High

---

### AZ-SEC-007 — Protect confidentiality, integrity, and availability

**Source concept**

Microsoft frames workload security around confidentiality, integrity, and availability.

**Disposition:** ADOPT

**IaCognition normalization**

Security analysis SHOULD consider:

- unauthorized disclosure;
- unauthorized or accidental modification;
- loss or degradation of legitimate availability.

Controls SHOULD be evaluated for their effect across all three properties.

**Provider neutrality:** High

---

### AZ-SEC-008 — Protect the software and infrastructure supply chain

**Source concept**

Microsoft calls for continuous protection and vulnerability detection across infrastructure, build systems, dependencies, code, and runtime assets.

**Disposition:** ADOPT

**IaCognition normalization**

Infrastructure delivery pipelines SHOULD include controls appropriate to the risk of unauthorized or vulnerable changes.

Relevant controls MAY include:

- dependency and vulnerability scanning;
- artifact provenance;
- code review;
- protected branches;
- policy validation;
- trusted build processes;
- signing and attestation.

**Provider neutrality:** High

---

### AZ-SEC-009 — Recovery assets require equivalent security

**Source concept**

Recovery systems and backups should receive security rigor comparable to primary systems.

**Disposition:** ADOPT

**IaCognition normalization**

Backup, replication, failover, and recovery infrastructure MUST NOT become weaker alternate paths around workload security requirements.

**Provider neutrality:** High

---

### AZ-SEC-010 — Security posture requires continuous validation

**Source concept**

Microsoft recommends ongoing measurement, threat modeling, vulnerability assessment, testing, policy enforcement, incident learning, and security improvement.

**Disposition:** ADOPT

**IaCognition normalization**

Security posture SHOULD be continuously validated rather than inferred from initial architecture intent.

Validation SHOULD identify drift, vulnerabilities, control regressions, and changes in assumptions or threat exposure.

**Provider neutrality:** High

---

### AZ-SEC-011 — Incident response is part of architecture readiness

**Source concept**

Workloads should have defined incident-response processes and responsibilities.

**Disposition:** ADOPT

**IaCognition normalization**

Production workloads SHOULD identify incident detection, escalation, containment, recovery, and responsibility expectations as part of operational readiness.

**Provider neutrality:** High

## Cross-pillar considerations

Security controls can affect:

- availability;
- latency;
- cost;
- operational complexity;
- deployment velocity.

Security tradeoffs MUST be explicit when they materially affect another architecture objective.
