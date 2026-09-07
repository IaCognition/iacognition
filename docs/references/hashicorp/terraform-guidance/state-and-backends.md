# Terraform State and Backends Analysis

### HC-STATE-001 — State is a critical managed artifact
**Disposition:** ADOPT

Terraform state MUST be treated as production data for material infrastructure. State architecture should be deliberate.

### HC-STATE-002 — Shared/production usage should normally use remote state
**Disposition:** ADOPT

Collaborative or production Terraform SHOULD use a suitably secured remote state mechanism unless a documented exception exists.

### HC-STATE-003 — State requires security controls
**Disposition:** ADOPT

State storage SHOULD provide access control, encryption, protected transport, and auditability where appropriate. State MUST NOT be committed to ordinary source control.

### HC-STATE-004 — Prefer effective locking or serialized execution
**Disposition:** ADOPT

Collaborative state SHOULD use locking or an equivalent mechanism that prevents concurrent writers.

### HC-STATE-005 — State boundaries are architecture boundaries
**Disposition:** ADAPT

State partitioning SHOULD reflect meaningful boundaries such as ownership, lifecycle, blast radius, privilege, environment, or deployment cadence.

### HC-STATE-006 — Avoid direct state manipulation
**Disposition:** ADOPT

IaCognition SHOULD prefer supported declarative refactoring and import/removal workflows over manual state editing or forceful state push.

### HC-STATE-007 — Preserve declarative migration history
**Disposition:** ADOPT

For new migrations, declarative constructs such as `removed` and `import` SHOULD be preferred when they preserve intent and history.

### HC-STATE-008 — Resource addresses have lifecycle significance
**Disposition:** ADOPT

Refactors MUST distinguish code movement from infrastructure replacement intent. `moved` blocks are preferred where applicable.
