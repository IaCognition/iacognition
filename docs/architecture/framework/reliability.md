# Reliability

Reliability is the ability of a workload to perform its intended function correctly and consistently, tolerate required failure conditions, and recover within defined objectives.

## REL-01 — Define reliability objectives

A material workload SHOULD define reliability objectives based on business and user requirements.

Objectives SHOULD focus on critical workload flows rather than infrastructure uptime alone.

## REL-02 — Identify failure domains

Architecture SHOULD identify which failure domains must be tolerated.

Examples include:

- process;
- host;
- rack;
- zone/facility;
- region;
- network;
- dependency;
- control plane;
- provider;
- human/operator.

## REL-03 — Analyze failure modes

Critical architecture SHOULD identify:

- what can fail;
- effect of the failure;
- detection mechanism;
- containment mechanism;
- recovery mechanism.

## REL-04 — Design redundancy against actual failure boundaries

Replica count alone does not demonstrate resilience.

Redundant components SHOULD avoid unacceptable correlated failure modes.

## REL-05 — Define recovery objectives

Stateful workloads SHOULD define:

- protected state;
- acceptable data loss;
- acceptable recovery time;
- restoration/failover mechanism;
- recovery dependencies.

RPO and RTO MAY be used where appropriate.

## REL-06 — Test recovery

Material recovery mechanisms SHOULD be tested periodically and after significant changes.

A recovery plan SHOULD NOT be treated as validated merely because it is documented.

## REL-07 — Prefer automated recovery for understood failures

Well-understood failure modes SHOULD use automated remediation when automation is safer, bounded, deterministic, and observable.

## REL-08 — Consider graceful degradation

Critical workloads SHOULD consider whether partial functionality can remain available when dependencies or capacity fail.

## REL-09 — Design for capacity and limits

Architecture SHOULD account for:

- expected demand;
- peak demand;
- provider/service limits;
- scaling lag;
- resource exhaustion;
- dependency capacity.

## REL-10 — Minimize reliability complexity

Reliability mechanisms introduce their own failure modes.

Additional redundancy, failover, and orchestration SHOULD be justified by reliability requirements.

## Validation examples

Evidence MAY include:

- fault-injection testing;
- failover testing;
- restore testing;
- capacity testing;
- dependency-failure testing;
- chaos experiments;
- disaster-recovery exercises;
- production service-level telemetry.
