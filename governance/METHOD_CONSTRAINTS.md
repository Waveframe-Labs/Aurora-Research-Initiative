---
title: "Method Constraints"
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
  - "EPISTEMIC_DOCTRINE.md"
  - "METADATA_POLICY.md"
anchors:
  - "ARI-METHOD-CONSTRAINTS-v1.1.1"
---

# Method Constraints

This document defines the **binding constraints and required capabilities** governing the Aurora
Workflow Orchestration (AWO) framework. It specifies what AWO **must do**, **may do**, and **must not
do** under the authority of the Aurora Research Initiative (ARI).

These constraints preserve governance separation, enable deterministic enforcement by CRI-CORE, and
ensure long-term reproducibility and epistemic integrity.

---

## 1. Purpose

The purpose of this document is to:

- Define mandatory method-level capabilities
- Prevent method-layer overreach into governance or enforcement
- Ensure compliance with ARI epistemic and governance doctrine
- Provide a stable contract for contributors and implementers
- Guarantee reproducibility, traceability, and auditability
- Enable enforcement by CRI-CORE without ambiguity

This document is binding for all implementations and versions of AWO.

---

## 2. Required Capabilities of AWO

### 2.1 Metadata Generation

AWO MUST:

- Generate ARI-compliant metadata for all workflow artifacts
- Propagate metadata across workflow steps and outputs
- Validate metadata presence and structure prior to step transitions
- Surface metadata in a **human-reviewable or human-renderable form**

**Reviewability Requirement:**  
Metadata and intermediate representations MUST be reviewable **on demand**. Native storage MAY be
binary or optimized, provided it can be deterministically rendered into a human-readable form for
audit, debugging, or dispute resolution purposes.

Final enforcement of metadata completeness is performed by CRI-CORE.

---

### 2.2 Reasoning Traceability

AWO MUST:

- Expose all **orchestration-level reasoning decisions**
- Preserve step-level interpretability of workflow control flow
- Avoid hidden or implicit transitions at the orchestration layer
- Record intermediate states in a reviewable or renderable format

**Opaque Dependency Clarification:**  
Internal logic of external libraries, runtimes, or hardware kernels (e.g., numerical solvers,
ML frameworks, CUDA kernels) is considered opaque. Such components MUST be:
- Explicitly invoked
- Version-pinned
- Treated as black-box operations within the reasoning chain

AWO is not required to expose internal logic of opaque dependencies but MUST expose when and why
they are invoked.

---

### 2.3 Reproducibility Intent

AWO MUST:

- Structure workflows to support re-execution under equivalent conditions
- Document runtime dependencies and configuration
- Avoid reliance on transient or undocumented external state
- Preserve deterministic intent pending CRI-CORE enforcement

AWO expresses intent; CRI-CORE enforces determinism.

---

### 2.4 Logging and Auditability

AWO MUST:

- Log all workflow steps and control-flow decisions
- Capture inputs, outputs, and state transitions
- Produce audit trails that are human-reviewable or human-renderable on demand
- Prohibit silent branches or undocumented behavior

High-throughput workflows MAY implement tiered logging or debug levels, provided audit completeness
can be reconstructed post hoc.

---

### 2.5 CRI-CORE Compatibility

AWO MUST:

- Emit workflows in a form compatible with CRI-CORE enforcement
- Expose structure, metadata, and dependencies required for validation
- Avoid embedding logic that conflicts with engine-level constraints

---

### 2.6 Epistemic Compliance

AWO MUST:

- Comply with the ARI Epistemic Doctrine
- Support falsifiability via explicit reasoning chains
- Avoid unfalsifiable or non-auditable processes
- Ensure all outputs are traceable to documented steps

---

## 3. Explicit Prohibitions

### 3.1 Epistemic Overreach

AWO MUST NOT:

- Define, modify, or reinterpret epistemic doctrine
- Adjudicate scientific truth or correctness
- Override epistemic constraints defined by ARI

AWO implements procedures; it does not define knowledge.

---

### 3.2 Governance Overreach

AWO MUST NOT:

- Modify ARI governance artifacts
- Approve or ratify its own changes
- Bypass governance logs or metadata obligations
- Collapse governance, method, and execution roles

---

### 3.3 Enforcement or Determinism

AWO MUST NOT:

- Embed deterministic execution logic
- Perform attestation or identity binding
- Override or intercept CRI-CORE enforcement behavior

Deterministic enforcement is exclusively the responsibility of CRI-CORE.

---

### 3.4 Method–Engine Collapse

AWO MUST NOT:

- Perform engine-level validation
- Enforce workflow correctness
- Embed execution engine capabilities
- Self-modify during execution

---

### 3.5 Provenance Violations

AWO MUST NOT:

- Produce artifacts lacking required metadata
- Bypass provenance or traceability requirements
- Silently alter workflow structure or logic

---

## 4. Cross-Layer Boundaries

### 4.1 AWO → ARI

AWO MUST operate under ARI governance and epistemic authority.
AWO MUST NOT modify, override, or conditionally reinterpret ARI rules.

---

### 4.2 AWO → CRI-CORE

AWO MUST produce workflows compatible with CRI-CORE enforcement.
AWO MUST NOT embed deterministic behavior, identity logic, or enforcement rules.

---

### 4.3 AWO → Waveframe Labs

Waveframe Labs MAY extend or adapt AWO only within the constraints defined here and under ARI
governance. Engineering convenience does not override method constraints.

---

### 4.4 AWO → Case Studies

Case studies MUST use AWO as provided.
They MUST NOT embed, fork, or modify AWO logic in ways that violate these constraints.

---

## 5. Revisions

Revisions to this document REQUIRE:

1. Institutional Coordinator approval
2. Architecture Decision Record (if governance-impacting)
3. Governance log entry
4. Semantic version increment
5. Backward traceability preservation

---

This document defines the authoritative method constraints governing Aurora Workflow Orchestration.
