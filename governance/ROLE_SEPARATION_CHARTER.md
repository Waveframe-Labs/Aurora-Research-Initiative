---
title: "Role Separation Charter"
version: "1.1.0"
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
  - "EPISTEMIC_DOCTRINE.md"
anchors:
  - "ARI-ROLE-SEPARATION-CHARTER-v1.1"
---

# Role Separation Charter

This charter defines the **formal separation of roles, authorities, and responsibilities** across the
Aurora ecosystem. It establishes binding boundaries that prevent role bleeding, preserve
accountability, and enable institutional growth without structural rewrites.

This document adopts a **hybrid role model**: a minimal set of active roles with explicitly reserved
future roles defined but inactive.

---

## 1. Purpose

The purpose of this charter is to:

- Define distinct roles across ARI, AWO, CRI-CORE, Waveframe Labs, and Case Studies
- Enforce strict separation of authority
- Prevent governance and execution overlap
- Preserve long-term institutional stability
- Reserve capacity for future governance bodies without retrofitting

This document is binding on all contributors and governed systems.

---

## 2. Active Roles

The following roles are **active** and hold authority today.

### 2.1 ARI Institutional Coordinator (IC)

**Scope:**
- Highest governance authority
- Ratifies governance and policy changes
- Adopts epistemic doctrine and compliance standards
- Oversees constitutional documents
- Ensures role-separation compliance

**Prohibitions:**
- May not act as Method or Tooling Maintainer
- May not approve undocumented changes
- May not influence execution or workflow logic

---

### 2.2 AWO Lead Maintainer

**Scope:**
- Maintains methodological logic
- Oversees workflow architecture
- Ensures compliance with method constraints
- Implements reproducible reasoning and metadata generation

**Prohibitions:**
- May not modify governance or epistemic doctrine
- May not implement enforcement or identity binding
- May not perform scientific adjudication

---

### 2.3 CRI-CORE Lead Maintainer

**Scope:**
- Maintains deterministic execution engine
- Implements integrity verification and identity binding
- Enforces reproducibility guarantees

**Prohibitions:**
- May not interpret workflow meaning
- May not alter method logic
- May not modify governance or doctrine

---

### 2.4 Waveframe Labs Maintainer

**Scope:**
- Develops engineering projects under ARI governance
- Maintains AWO, CRI-CORE, and case study repositories
- Builds tooling, simulators, and demonstrations

**Prohibitions:**
- May not modify governance or epistemic doctrine
- May not override ARI constraints

---

### 2.5 Case Study Maintainers

**Scope:**
- Conduct applied research using AWO and CRI-CORE
- Produce reproducible scientific artifacts
- Maintain domain-specific repositories

**Prohibitions:**
- May not alter governance, method, or tooling rules
- May not modify AWO or CRI-CORE behavior

---

## 3. Reserved Future Roles

The following roles are **defined but inactive**. Their inclusion prevents future ambiguity and
structural rewrites.

### 3.1 ARI Governance Council (Future)
Collective body for governance ratification and oversight.

### 3.2 AWO Method Council (Future)
Advisory body for method evolution proposals.

### 3.3 CRI Integrity Council (Future)
Oversight body for enforcement, attestation, and tooling integrity.

### 3.4 Audit & Compliance Officer (Future)
Independent reviewer for governance and compliance adherence.

### 3.5 External Reviewers (Future)
Read-only observers of governance processes.

---

## 4. Separation of Powers

| Role | Permitted Modifications | Prohibited Modifications |
|------|--------------------------|--------------------------|
| **ARI IC** | Governance, doctrine | Method logic, enforcement |
| **AWO Lead** | Workflow logic | Governance, enforcement |
| **CRI Lead** | Deterministic enforcement | Governance, method |
| **Labs Maintainer** | Tooling, demos | Core governance or method |
| **Case Study Maintainers** | Applied research artifacts | Core system logic |

These boundaries are binding.

---

## 5. Forbidden Role Interactions

The following actions constitute governance violations:

- Self-approval of governance changes
- Cross-role modification without authority
- Silent or undocumented updates
- Method enforcing governance
- Enforcement defining method or doctrine
- Case studies altering upstream systems
- Governance engaging in execution

---

## 6. Authority Ordering

From highest to lowest:

1. ARI Institutional Coordinator
2. (Future) ARI Governance Council
3. AWO Lead Maintainer
4. CRI-CORE Lead Maintainer
5. Waveframe Labs Maintainer
6. Case Study Maintainers

No lower role may override a higher one.

---

## 7. Revisions

Revisions to this charter REQUIRE:

1. Institutional Coordinator approval
2. Architecture Decision Record (if governance-impacting)
3. Governance log entry
4. Semantic version increment
5. Backward traceability preservation

---

This charter defines the authoritative role separation model of the Aurora ecosystem.
