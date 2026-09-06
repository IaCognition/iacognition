# Performance Efficiency

Performance Efficiency is the ability to meet workload performance objectives efficiently as demand and technology change.

## PERF-01 — Define measurable targets

Performance-sensitive workloads SHOULD define measurable objectives such as:

- latency;
- throughput;
- concurrency;
- processing duration;
- freshness;
- queue depth.

## PERF-02 — Include load context

Performance targets SHOULD identify the workload conditions under which they apply.

A target without demand context is incomplete when scale materially affects the outcome.

## PERF-03 — Plan capacity

Architecture SHOULD identify:

- baseline demand;
- peak demand;
- burst behavior;
- expected growth;
- scaling constraints.

## PERF-04 — Match scaling strategy to workload behavior

Scaling mechanisms SHOULD account for:

- state model;
- demand shape;
- startup time;
- scaling lag;
- latency objectives;
- cost;
- reliability.

Automatic scaling SHOULD NOT be assumed appropriate for every workload.

## PERF-05 — Select resources from requirements

Compute, storage, network, database, and platform choices SHOULD follow workload performance requirements.

## PERF-06 — Test representative workloads

Material performance objectives SHOULD have a validation method using representative demand and data where practical.

## PERF-07 — Observe production performance

Performance-sensitive workloads SHOULD expose telemetry sufficient to compare actual behavior with objectives and architecture assumptions.

## PERF-08 — Optimize from evidence

Architecture SHOULD avoid speculative optimization.

Optimization SHOULD be driven by:

- measured bottlenecks;
- justified forecasts;
- explicit requirements.

## PERF-09 — Performance efficiency is not maximum performance

Architecture SHOULD seek sufficient performance without unjustified resource consumption.

Excess capacity SHOULD be justified by another requirement such as reliability headroom, recovery behavior, or forecast growth.

## Validation examples

Evidence MAY include:

- load tests;
- stress tests;
- latency distributions;
- saturation metrics;
- capacity models;
- production telemetry;
- benchmark results.
