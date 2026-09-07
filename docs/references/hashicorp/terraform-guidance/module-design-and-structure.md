# Terraform Module Design Analysis

### HC-MOD-001 — Modules represent coherent capabilities
**Disposition:** ADOPT

A module SHOULD represent a coherent infrastructure capability, architectural unit, or reusable responsibility rather than exist merely to wrap resources.

### HC-MOD-002 — Repetition and standardization justify modules
**Disposition:** ADOPT

Repeated patterns are strong module candidates when reuse improves consistency, policy enforcement, maintainability, or delivery speed.

### HC-MOD-003 — Avoid over-modularization
**Disposition:** ADOPT

HashiCorp explicitly warns that excessive modularization can reduce understandability and maintainability. IaCognition SHOULD require a real abstraction benefit.

### HC-MOD-004 — Prefer relatively flat composition
**Disposition:** ADOPT

Module composition SHOULD generally prefer visible root-level orchestration to deep nested call chains.

### HC-MOD-005 — Inputs and outputs form the module contract
**Disposition:** ADOPT

Reusable modules SHOULD expose the smallest practical interface that expresses architectural intent while hiding unnecessary implementation detail.

### HC-MOD-006 — Root and reusable modules differ
**Disposition:** ADOPT

Root modules assemble workload-specific infrastructure; reusable modules encode repeatable infrastructure capability.

### HC-MOD-007 — Modules can preserve architecture language
**Disposition:** ADOPT

IaCognition SHOULD prefer module abstractions that communicate architectural purpose instead of merely mirroring physical provider objects.

---

# Standard Module Structure

### HC-MSTRUCT-001 — Use recognizable structure
**Disposition:** ADOPT

Reusable modules SHOULD normally follow Terraform conventions such as `README.md`, `main.tf`, `variables.tf`, and `outputs.tf`.

### HC-MSTRUCT-002 — Root module is the primary entry point
**Disposition:** ADOPT

A reusable-module repository SHOULD expose a coherent root-module experience.

### HC-MSTRUCT-003 — Nested modules under `modules/`
**Disposition:** ADOPT

Secondary modules SHOULD follow standard Terraform layout and remain limited and justified.

### HC-MSTRUCT-004 — Examples under `examples/`
**Disposition:** ADOPT

Reusable modules SHOULD include representative examples when usage is not trivial.

### HC-MSTRUCT-005 — Documentation is part of module quality
**Disposition:** ADOPT

Reusable modules SHOULD document purpose, assumptions, inputs, outputs, provider requirements, important behavior, examples, and limitations.

### HC-MSTRUCT-006 — File boundaries do not create Terraform boundaries
**Disposition:** ADOPT

Semantic files such as `network.tf` or `identity.tf` MAY improve comprehension, but Terraform treats the module's top-level files as one configuration.
