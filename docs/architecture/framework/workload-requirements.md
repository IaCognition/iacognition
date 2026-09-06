# Workload Architecture Requirements

Architecture begins with an explicit workload model.

This document defines the minimum categories of information that SHOULD be considered before selecting implementation technologies.

## 1. Workload identity

Record:

- workload name;
- purpose;
- business owner;
- technical owner;
- environment;
- lifecycle stage;
- business criticality.

## 2. Functional scope

Describe what the workload must do.

Include:

- primary capabilities;
- critical user or system flows;
- external consumers;
- required dependencies;
- major data flows.

## 3. Availability and reliability

Record where applicable:

- availability target;
- critical flows;
- tolerated failure domains;
- degraded-mode expectations;
- dependency availability requirements;
- maintenance tolerance;
- maximum acceptable outage.

## 4. Recovery and data protection

For stateful workloads, record:

- state categories;
- recovery point objective or equivalent;
- recovery time objective or equivalent;
- backup requirements;
- replication requirements;
- restoration method;
- disaster-recovery expectations;
- recovery test expectations.

## 5. Security

Record:

- human identities;
- workload identities;
- privilege model;
- trust boundaries;
- external exposure;
- administrative exposure;
- sensitive data;
- encryption expectations;
- secrets requirements;
- applicable security controls;
- regulatory/compliance constraints.

## 6. Networking

Record:

- ingress requirements;
- egress requirements;
- east-west communication;
- public/private connectivity;
- hybrid connectivity;
- multicloud connectivity;
- DNS requirements;
- address constraints;
- latency/geographic constraints.

## 7. Performance and scale

Record:

- baseline demand;
- peak demand;
- expected growth;
- latency targets;
- throughput targets;
- concurrency;
- processing deadlines;
- workload burst characteristics;
- scaling constraints.

## 8. Operations

Record:

- support hours;
- monitoring requirements;
- alerting expectations;
- incident responsibilities;
- deployment frequency;
- maintenance windows;
- rollback expectations;
- access model;
- auditability;
- automation expectations.

## 9. Cost

Record:

- budget or cost target;
- major cost sensitivity;
- utilization profile;
- predictable vs variable demand;
- acceptable commercial commitments;
- cost allocation requirements;
- nonproduction cost constraints.

## 10. Sustainability

Where material, record:

- sustainability objectives;
- resource-efficiency objectives;
- data-retention constraints;
- geographic constraints;
- measurable sustainability indicators.

## 11. Organizational constraints

Record:

- approved platforms;
- supported technologies;
- team skills;
- ownership boundaries;
- centralized platform dependencies;
- governance requirements;
- policy constraints;
- provider/account/subscription/project constraints.

## 12. Unknowns and assumptions

Unknown material requirements SHOULD be listed explicitly.

An assumption SHOULD include:

- assumed value;
- reason;
- risk if incorrect;
- affected architecture decisions.

## Architecture gate

An agent SHOULD NOT proceed directly to implementation when unresolved requirements could materially change:

- provider/service selection;
- network topology;
- persistence model;
- availability model;
- security boundaries;
- recovery architecture;
- scaling model;
- cost profile.

When work must proceed despite incomplete information, the resulting architecture MUST expose the assumption.
