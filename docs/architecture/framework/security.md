# Security

Security architecture protects identities, systems, data, and assets while preserving confidentiality, integrity, availability, privacy, and compliance requirements.

## SEC-01 — Define identity explicitly

Architecture SHOULD identify:

- human identities;
- workload identities;
- administrative identities;
- identity providers;
- trust relationships.

## SEC-02 — Enforce least privilege

Access SHOULD use the minimum privileges necessary for the intended responsibility.

Standing privileged access SHOULD be minimized when temporary or scoped access is practical.

## SEC-03 — Do not infer trust from network location

Network placement alone SHOULD NOT establish trust.

Sensitive operations SHOULD use explicit authentication and authorization appropriate to the risk.

## SEC-04 — Define trust boundaries

Architecture SHOULD identify trust boundaries and how information, identities, and requests cross them.

## SEC-05 — Limit blast radius

Security architecture SHOULD limit the effect of compromised components or identities using mechanisms such as:

- privilege boundaries;
- segmentation;
- isolation;
- account/subscription/project boundaries;
- data boundaries;
- workload separation.

## SEC-06 — Apply defense in depth

Material workloads SHOULD assume individual controls can fail.

Multiple complementary controls SHOULD protect important assets where justified.

## SEC-07 — Classify and protect data

Data SHOULD be classified sufficiently to determine:

- access;
- encryption;
- retention;
- replication;
- backup;
- exposure;
- destruction.

## SEC-08 — Protect secrets and credentials

Long-lived embedded credentials SHOULD be avoided where managed identity, temporary credentials, or secure secret-delivery mechanisms are practical.

Secrets MUST NOT be committed to source control.

## SEC-09 — Protect the delivery chain

Infrastructure delivery SHOULD use controls appropriate to its risk, which MAY include:

- protected branches;
- code review;
- dependency scanning;
- policy validation;
- trusted artifacts;
- provenance;
- signing;
- controlled deployment identities.

## SEC-10 — Secure recovery paths

Backup, replication, disaster recovery, and administrative recovery mechanisms MUST NOT become weaker alternate paths around security requirements.

## SEC-11 — Continuously validate posture

Security SHOULD be validated over time for:

- drift;
- exposure;
- privilege expansion;
- vulnerable configuration;
- control regressions;
- changed threats.

## SEC-12 — Include compliance and privacy constraints

Applicable regulatory, privacy, residency, and compliance requirements SHOULD be explicit architecture inputs.

## Validation examples

Evidence MAY include:

- threat modeling;
- access review;
- policy-as-code;
- configuration scanning;
- vulnerability scanning;
- secret scanning;
- network-path analysis;
- audit-log validation;
- recovery-access review.
