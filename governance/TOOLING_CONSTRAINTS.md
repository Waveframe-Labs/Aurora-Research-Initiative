---
title: "Tooling Constraints"
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
  - "EPISTEMIC_DOCTRINE.md"
  - "METADATA_POLICY.md"
anchors:
  - "ARI-TOOLING-CONSTRAINTS-v1.1.0"
---

# Tooling Constraints

This document defines the **binding constraints and required capabilities** governing the CRI-CORE
tooling layer. It specifies what CRI-CORE **must do**, **may do**, and **must not do** under the
authority of the Aurora Research Initiative (ARI).

CRI-CORE is the deterministic enforcement and execution engine of the Aurora ecosystem. Its role is
strictly mechanical: enforcing integrity, provenance, and determinism **without interpretive or
epistemic authority**.

---

## 1. Purpose

The purpose of this document is to:

- Define strict limitations on CRI-CORE authority
- Ensure CRI-CORE performs only mechanical, deterministic enforcement
- Prevent semantic, epistemic, or methodological interpretation
- Guarantee independence from AWO and ARI decision-making
- Provide enforceable guardrails for all future tooling development

This document is binding for all implementations and versions of CRI-CORE.

---

## 2. Required Capabilities of CRI-CORE

### 2.1 Deterministic Execution

CRI-CORE MUST:

- Execute workflows deterministically
- Eliminate nondeterministic behavior where possible
- Produce reproducible outputs given identical inputs and environments
- Enforce consistency across execution environments

Determinism is an enforcement guarantee, not a methodological choice.

---

### 2.2 Identity and Attestation Enforcement

CRI-CORE MUST:

- Perform identity binding for execution contexts
- Enforce attestation independence
- Prevent actors from approving their own changes
- Validate signatures, checksums, or attestations required by ARI

---

### 2.3 Integrity and Provenance Validation

CRI-CORE MUST:

- Compute and validate cryptographic integrity hashes
- Detect tampering or unapproved modifications
- **Halt execution immediately** when integrity or provenance validation fails
- Ensure artifacts remain unaltered across executions

CRI-CORE has veto authority only in the form of execution halting on validation failure.

---

### 2.4 Metadata Enforcement and Equivalence

CRI-CORE MUST:

- Validate presence and schema compliance of metadata produced by AWO
- Enforce metadata completeness prior to artifact acceptance
- Verify metadata equivalence across derived artifacts (e.g., Markdown → PDF)
- Inject or map metadata into derived artifacts when required to preserve equivalence

CRI-CORE MUST NOT generate, infer, or correct metadata content. It enforces compliance, not authorship.

---

### 2.5 Execution Environment Capture

CRI-CORE MUST:

- Capture execution environment details deterministically
- Record runtime conditions as provenance metadata
- Expose environment records for audit and reconstruction
- Avoid reliance on implicit or untracked environmental state

---

## 3. Explicit Prohibitions

### 3.1 Epistemic Prohibitions

CRI-CORE MUST NOT:

- Interpret workflow meaning or intent
- Evaluate scientific or logical correctness
- Perform reasoning or inference of any kind

CRI-CORE is not an epistemic actor.

---

### 3.2 Method Prohibitions

CRI-CORE MUST NOT:

- Implement or modify method logic
- Validate methodological correctness
- Embed procedural reasoning
- Override logic defined by AWO

CRI enforces execution; it does not define method.

---

### 3.3 Structural Prohibitions

CRI-CORE MUST NOT:

- Analyze or infer workflow structure beyond required validation
- Detect or correct logical errors
- Conditionally alter execution paths
- Modify workflow structure at runtime

---

### 3.4 Governance Prohibitions

CRI-CORE MUST NOT:

- Modify ARI governance artifacts
- Approve governance or policy changes
- Override ARI or AWO constraints
- Assume any governance authority

---

### 3.5 Provenance Prohibitions

CRI-CORE MUST NOT:

- Generate metadata content
- Infer missing metadata
- Correct metadata violations
- Silence or bypass validation failures

---

## 4. Cross-Layer Boundaries

### 4.1 CRI-CORE → ARI

CRI-CORE MUST operate under ARI governance authority.
CRI-CORE MUST NOT reinterpret, modify, or influence governance rules.

---

### 4.2 CRI-CORE → AWO

CRI-CORE MUST execute workflows mechanically as provided by AWO.
CRI-CORE MUST NOT question, refine, or reinterpret workflow instructions.

---

### 4.3 CRI-CORE → Waveframe Labs

Waveframe Labs MAY implement CRI-CORE, but MAY NOT grant CRI-CORE interpretive,
methodological, or governance authority beyond this document.

---

### 4.4 CRI-CORE → Case Studies

Case studies MAY execute workflows via CRI-CORE.
They MUST NOT extend or modify CRI-CORE behavior.

---

## 5. Forbidden Cross-Layer Interactions

The following actions constitute governance failures:

- Tooling interpreting workflow semantics
- Tooling inferring structure or intent
- Tooling evaluating correctness or truth
- Tooling generating or correcting metadata
- Tooling bypassing validation failures
- Tooling modifying workflow structure
- Tooling making autonomous decisions

These prohibitions preserve CRI-CORE neutrality.

---

## 6. Revisions

Revisions to this document REQUIRE:

1. Institutional Coordinator approval
2. Architecture Decision Record (if governance-impacting)
3. Governance log entry
4. Semantic version increment
5. Backward traceability preservation

---

This document defines the authoritative tooling constraints governing CRI-CORE.
