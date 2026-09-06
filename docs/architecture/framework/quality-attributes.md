# Architecture Quality Attributes

IaCognition uses quality attributes to organize nonfunctional architecture requirements and evaluate tradeoffs.

## Core quality attributes

### Operational Excellence

The ability to deploy, operate, observe, change, recover, and continuously improve a workload effectively.

### Security

The ability to protect systems, identities, data, and assets while preserving required confidentiality, integrity, availability, privacy, and compliance outcomes.

### Reliability

The ability of a workload to perform its intended function correctly and consistently, tolerate required failure conditions, and recover within defined objectives.

### Performance Efficiency

The ability to meet workload performance objectives efficiently as demand and technology change.

### Cost Optimization

The ability to deliver required workload outcomes at a justified lifecycle cost and maximize value from consumed resources.

### Sustainability

The ability to meet workload requirements while reducing unjustified resource consumption and environmental impact where sustainability is a material objective.

## Quality attributes are not scores to maximize

IaCognition does not assume every workload should maximize every quality attribute.

For example:

- a development workload may accept reduced availability to control cost;
- a safety-critical workload may accept significant cost and complexity for stronger reliability;
- a high-throughput workload may accept additional cost for lower latency;
- a regulated workload may accept operational complexity for stronger isolation.

The architecture objective is appropriate quality for the workload, not theoretical maximum quality.

## Cross-attribute interactions

| Decision | Likely benefit | Possible cost |
|---|---|---|
| Multi-site deployment | Reliability | Cost, operations, complexity |
| Strong segmentation | Security | Complexity, latency, operations |
| Aggressive caching | Performance | Consistency, complexity |
| Autoscaling | Cost/performance | Operational complexity, failure modes |
| Extensive telemetry | Operations/security | Cost, data handling |
| Long retention | Recovery/compliance | Cost, sustainability |
| Managed services | Operations/reliability | Portability, control, cost |
| Geographic replication | Reliability | Cost, latency, data governance |
| Reduced redundancy | Cost/sustainability | Reliability |

Architecture review SHOULD examine these interactions explicitly.

## Priority

A workload SHOULD identify which quality attributes materially influence architecture.

Priority MAY be expressed using:

- mandatory constraints;
- target objectives;
- relative priority;
- risk classification;
- business criticality.

IaCognition SHOULD avoid generic statements such as "security is high priority" when measurable or actionable requirements can be stated instead.

## Quality-attribute completeness

An architecture review SHOULD determine whether each quality attribute is:

- materially applicable;
- explicitly not applicable;
- insufficiently specified.

Silence SHOULD NOT automatically mean that a quality attribute is irrelevant.
