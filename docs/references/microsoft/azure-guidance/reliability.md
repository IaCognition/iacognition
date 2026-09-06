# Microsoft Azure Well-Architected — Reliability Analysis

## Source scope

This analysis covers the Reliability pillar of the Microsoft Azure Well-Architected Framework and related Azure reliability guidance.

Microsoft frames reliability around the ability of a workload to resist malfunction, remain useful when failures occur, and recover to an acceptable operating state.

## Extracted concepts

### AZ-REL-001 — Reliability begins with business requirements

**Source concept**

Availability and recoverability targets should be derived from workload and business requirements rather than selected arbitrarily.

**Disposition:** ADOPT

**IaCognition normalization**

A workload SHOULD define explicit reliability objectives before architecture selection.

Reliability requirements SHOULD identify measurable availability and recovery expectations for critical workload flows.

**Provider neutrality:** High

**Candidate destinations**

- `schemas/workload/`
- `rules/reliability/`
- `docs/architecture/reliability/`

---

### AZ-REL-002 — Critical flows require explicit reliability targets

**Source concept**

Microsoft recommends identifying important workload flows and setting measurable reliability targets for them.

**Disposition:** ADAPT

**IaCognition normalization**

Reliability requirements SHOULD be associated with business-critical workload flows rather than expressed only as a single system-wide availability percentage.

Architecture reasoning SHOULD identify which flows require stronger availability, durability, or recovery guarantees.

**Provider neutrality:** High

---

### AZ-REL-003 — Failure modes should be analyzed explicitly

**Source concept**

Reliability design includes identifying dependencies, potential failures, their effects, and mitigation strategies.

**Disposition:** ADOPT

**IaCognition normalization**

Material infrastructure architectures SHOULD include failure-mode analysis for critical components, dependencies, and flows.

The analysis SHOULD identify:

- what can fail;
- the scope of impact;
- how failure is detected;
- how service is preserved or degraded;
- how recovery occurs.

**Provider neutrality:** High

---

### AZ-REL-004 — Design for resilience

**Source concept**

Systems should tolerate faults and continue delivering acceptable functionality when components malfunction.

**Disposition:** ADOPT

**IaCognition normalization**

Architecture SHOULD define the failure domains that the workload must tolerate.

Resilience mechanisms SHOULD be selected according to workload criticality rather than added automatically.

**Provider neutrality:** High

---

### AZ-REL-005 — Design for recovery

**Source concept**

A reliable workload must recover from failures, including severe failures, in a manner consistent with business objectives.

**Disposition:** ADOPT

**IaCognition normalization**

Stateful workloads MUST identify recovery objectives and a recovery strategy before implementation.

Recovery architecture SHOULD define:

- protected state;
- recovery point expectations;
- recovery time expectations;
- restoration or failover mechanisms;
- recovery dependencies;
- validation procedures.

**Provider neutrality:** High

---

### AZ-REL-006 — Redundancy should follow failure boundaries

**Source concept**

Microsoft recommends redundancy where required to satisfy reliability targets and warns that redundancy choices introduce cost and operational consequences.

**Disposition:** ADAPT

**IaCognition normalization**

Redundancy SHOULD be designed against explicit failure domains.

Additional replicas or deployment locations SHOULD NOT be treated as inherently sufficient evidence of resilience.

**Provider neutrality:** High

---

### AZ-REL-007 — Self-healing is preferable where practical

**Source concept**

Workloads should detect and automatically recover from routine or expected failure conditions when doing so is safe.

**Disposition:** ADOPT

**IaCognition normalization**

Recoverable, well-understood failure modes SHOULD use automated remediation when the automation is deterministic, observable, bounded, and safer than manual intervention.

**Provider neutrality:** High

---

### AZ-REL-008 — Recovery must be tested

**Source concept**

Recovery plans should be validated through testing and operational drills.

**Disposition:** ADOPT

**IaCognition normalization**

A documented recovery strategy SHOULD NOT be considered validated solely because it exists.

Recovery mechanisms for material workloads SHOULD be tested periodically and after significant architecture changes.

**Provider neutrality:** High

---

### AZ-REL-009 — Reliability includes operations and observability

**Source concept**

Reliable systems need sufficient monitoring, alerting, telemetry, and operational practices to detect faults and support recovery.

**Disposition:** ADOPT

**IaCognition normalization**

Reliability architecture MUST include detection and operational response considerations, not only redundancy.

A workload SHOULD expose sufficient signals to determine whether critical flows are meeting reliability objectives.

**Provider neutrality:** High

---

### AZ-REL-010 — Simplicity improves reliability

**Source concept**

Microsoft identifies simplicity as a reliability design principle because unnecessary components and complexity create additional failure modes and operational burden.

**Disposition:** ADOPT

**IaCognition normalization**

Architectures SHOULD avoid components, dependencies, and mechanisms that do not materially support workload requirements.

Complexity SHOULD be treated as a reliability and operability cost.

**Provider neutrality:** High

## Cross-pillar considerations

Reliability can increase:

- infrastructure cost;
- architectural complexity;
- operational burden;
- security surface area;
- deployment complexity.

IaCognition SHOULD therefore require reliability mechanisms to be justified by workload requirements and explicit tradeoffs.
