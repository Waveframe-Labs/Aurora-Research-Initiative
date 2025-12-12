---
title: "Change Control and Versioning Policy"
version: "1.1.1"
status: "Active"
created: "2025-11-27"
updated: "2025-12-12"
type: "governance"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
license: "Apache-2.0"
doi: "10.5281/zenodo.17743096"
ai_assisted: "partial"
ai_assistance_details: "AI-assisted structural review and consistency checking under full human oversight and final approval."
policy_version: "ARI-Metadata-2.0.0"
dependencies:
  - "ARI_BOUNDARIES_AND_RESPONSIBILITIES.md"
  - "METHOD_CONSTRAINTS.md"
  - "TOOLING_CONSTRAINTS.md"
  - "ROLE_SEPARATION_CHARTER.md"
  - "Neurotransparency_Doctrine.md"
anchors:
  - "ARI-CHANGE-CONTROL-v1.1.1"
---

# Change Control and Versioning Policy

## Purpose

This policy defines the **binding governance rules** for versioning, release control, and institutional
change management across the Aurora Research Initiative (ARI), Aurora Workflow Orchestration (AWO),
CRI-CORE, Waveframe Labs, and all affiliated case studies.

It establishes a **dual versioning model** and mandates **global ecosystem release tagging** to ensure
reproducibility, auditability, and long-term institutional stability, while preserving scalability
and minimizing unnecessary release noise.

---

## 1. Scope and Authority

This policy is authoritative under ARI governance.

All governed subsystems MUST comply with the rules defined herein. No subsystem may redefine,
override, or bypass these requirements through local practice or tooling behavior.

---

## 2. Dual Versioning Model

The Aurora ecosystem uses **independent semantic versioning per subsystem**, combined with a required
**global ecosystem release tag** for qualifying releases.

### 2.1 Subsystem Versions

Each subsystem maintains its own semantic version:

- ARI
- AWO
- CRI-CORE
- Waveframe Labs (optional, non-governance)
- Case Studies (per project)

All versions MUST follow `MAJOR.MINOR.PATCH` semantics.

---

### 2.2 Global Ecosystem Release Tag (Scoped)

Every **qualifying release** MUST produce a unified global release tag in the format:

```
ARI-x.y.z_AWO-a.b.c_CRI-d.e.f_LABS-l.m.n_CSNAME-u.v.w
```

The global tag applies to:
- the **core ecosystem** (ARI, AWO, CRI-CORE, optional Labs), and
- **at most one case study**, corresponding to the release context.

Case studies not included in the tag are considered out of scope for that release and are tracked
via their own independent versions and logs.

The global tag is the **canonical provenance anchor** for the ecosystem state represented by the
release.

---

## 3. Version Change Triggers

### 3.1 ARI Version Changes

MAJOR or MINOR increments are required for:
- Governance policy changes
- Role definitions or authority boundaries
- Metadata, provenance, or schema rules
- Institutional constraints

PATCH increments are permitted only for non-normative clarifications.

---

### 3.2 AWO Version Changes

MAJOR or MINOR increments are required for:
- Workflow logic or structure changes
- Reasoning-chain architecture modifications
- Metadata handling behavior

PATCH increments are permitted for documentation corrections and non-functional bug fixes that do not
alter the reasoning chain structure or governance guarantees.

---

### 3.3 CRI-CORE Version Changes

MAJOR or MINOR increments are required for:
- Deterministic execution logic
- Identity, attestation, or integrity mechanisms
- Execution environment capture

PATCH increments are permitted for non-executable changes.

---

### 3.4 Waveframe Labs Version Changes

Applied to:
- Demonstrations
- Infrastructure utilities
- Non-governance tooling

May not alter upstream subsystem versions.

---

### 3.5 Case Study Version Changes

Each case study is versioned independently. Case study versions are included in the global ecosystem
release tag only when explicitly in scope for that release.

---

## 4. Change Classes

### 4.1 Governance-Impacting Change

A change is considered governance-impacting if it alters:
- Metadata requirements
- Role permissions or authority boundaries
- Provenance or attestation guarantees
- Enforcement scope defined by ARI

Governance-impacting changes REQUIRE an ADR.

---

### 4.2 Breaking Change

A change that:
- Invalidates prior assumptions
- Alters subsystem guarantees
- Impacts reproducibility or determinism

Requires:
- MAJOR version increment
- ADR (if governance-impacting)
- Governance log entry
- Global ecosystem release tag

---

### 4.3 Non-Breaking Change

Adds functionality without violating existing constraints.

Requires:
- MINOR version increment
- Governance log entry
- Global ecosystem release tag

---

### 4.4 Clarification Change

Documentation-only changes and non-functional corrections with no behavioral impact.

Requires:
- PATCH version increment
- Governance log entry

Clarification changes do **not** require a new global ecosystem release tag unless they are
governance-impacting or explicitly bundled into a milestone release.

---

### 4.5 Deprecation or Retirement

Subsystems or artifacts may be deprecated but MUST remain accessible and traceable.

Requires:
- Version increment (MAJOR or MINOR as appropriate)
- Deprecation notice
- Governance log entry

---

## 5. Approval Requirements

All version changes REQUIRE:

1. Institutional Coordinator approval
2. Architecture Decision Record (if governance-impacting)
3. Governance log entry
4. Provenance verification
5. Metadata normalization

Global ecosystem release tags are required only for qualifying releases as defined above.

No subsystem may approve its own version changes.

---

## 6. Release Preconditions

Prior to any qualifying release, the following MUST be satisfied:

- Metadata validity
- Provenance verification
- Deterministic execution validation (CRI-CORE changes)
- Auditability validation (AWO changes)
- Integrity hash regeneration
- Changelog updates

Silent or partial releases are prohibited.

---

## 7. Cross-Layer Constraints

- ARI changes require re-anchoring of all subsystems at the next qualifying release
- AWO may not trigger ARI version changes
- CRI-CORE may not alter ARI or AWO versioning rules
- Case studies may not redefine governance constraints
- Circular version dependencies are prohibited

Re-anchoring requirements apply to **release actions**, not to internal synchronization steps, to
avoid recursive versioning loops.

---

## 8. Amendments and Revision Rules

Revisions to this policy REQUIRE:

1. Institutional Coordinator approval
2. ADR documentation
3. Governance log entry
4. Semantic version increment
5. Backward traceability preservation

---

This policy defines the authoritative change control and versioning rules of the Aurora ecosystem.
