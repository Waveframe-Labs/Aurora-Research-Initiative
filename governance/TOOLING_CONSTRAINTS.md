---
title: "Tooling Constraints"
version: "1.1.1"
status: "Active"
created: "2025-11-27"
updated: "2025-12-12"
type: "governance"
doi: "10.5281/zenodo.17743096"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
license: "Apache-2.0"
ai_assisted: "partial"
ai_assistance_details: "AI-assisted structural review and risk analysis under full human oversight."
policy_version: "ARI-Metadata-2.0.0"
dependencies:
  - "ARI_BOUNDARIES_AND_RESPONSIBILITIES.md"
  - "EPISTEMIC_DOCTRINE.md"
  - "METADATA_POLICY.md"
anchors:
  - "ARI-TOOLING-CONSTRAINTS-v1.1.1"
---

# Tooling Constraints (v1.1.1)

This document establishes the binding constitutional constraints governing the CRI-CORE tooling layer. It defines the legal, epistemic, and operational boundaries under which CRI-CORE must function. These constraints ensure that CRI-CORE remains a purely mechanistic execution and enforcement engine with no authority to interpret, infer, or influence epistemic or methodological logic.

---

## 1. Purpose

The purpose of this document is to:

- define the strict limitations of CRI-CORE
- ensure CRI-CORE performs only mechanical, deterministic enforcement
- prevent semantic or epistemic influence from tooling
- guarantee reproducibility within declared technical limits
- provide enforceable guardrails for all future CRI development

This document is binding for all implementations and versions of CRI-CORE.

---

## 2. Required Capabilities of CRI-CORE

### 2.1 Deterministic Execution (Declared Scope)

CRI-CORE must:

- enforce **deterministic intent**, not universal bitwise determinism
- ensure *semantic determinism* where bitwise determinism is technically infeasible
- document and pin execution environments, libraries, and hardware targets
- declare known nondeterministic domains (e.g., GPU floating-point operations)

**Definition:**  
*Semantic determinism* means that repeated executions produce functionally equivalent results within documented tolerance bounds, even if low-level floating-point representations differ.

Bitwise determinism MAY be required only where explicitly declared by a case study or method contract.

---

### 2.2 Identity and Attestation Enforcement

CRI-CORE must:

- perform identity-binding for execution contexts
- enforce attestation independence
- ensure no actor approves their own changes
- validate cryptographic signatures and checksums as required

---

### 2.3 Integrity Validation

CRI-CORE must:

- compute and validate cryptographic integrity hashes
- detect unauthorized modification of artifacts or logs
- **halt execution immediately** upon integrity failure
- distinguish between declared nondeterminism and tampering

Integrity checks MUST respect the determinism scope defined in Section 2.1.

---

### 2.4 Execution Environment Capture

CRI-CORE must:

- capture runtime environment details deterministically
- record versions of compilers, libraries, hardware, and drivers
- expose environment records for audit and replay
- avoid implicit or untracked environmental dependencies

---

### 2.5 Metadata Transport and Injection

CRI-CORE must:

- transport metadata from governed sources into derived artifacts
- inject metadata *verbatim* into outputs (e.g., PDFs, archives)
- preserve field values exactly as provided
- validate metadata equivalence across representations

CRI-CORE must **not**:

- generate missing metadata
- infer metadata values
- correct or synthesize metadata fields

Injection is strictly a **transport operation**, not a creative or interpretive act.

---

## 3. Explicit Prohibitions

CRI-CORE is explicitly forbidden from:

- interpreting scientific or logical meaning
- evaluating correctness beyond integrity checks
- inferring workflow intent or structure
- modifying method logic
- altering metadata content
- resolving epistemic ambiguity
- making discretionary decisions

CRI-CORE enforces constraints; it does not reason.

---

## 4. Cross-Layer Boundaries

CRI-CORE:

- obeys ARI governance without reinterpretation
- executes AWO instructions mechanically
- may halt execution on validation failure
- may not override, refine, or reinterpret upstream logic

---

## 5. Revision Rules

All revisions require:

1. ARI Institutional approval
2. Governance log entry
3. Semantic version increment
4. Backward linkage
5. Documented rationale

No silent modifications permitted.
