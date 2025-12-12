# Aurora Research Initiative (ARI)
## Metadata Policy v2.0.0

---
title: "Metadata Policy"
policy_version: "ARI-Metadata-2.0.0"
version: "2.0.0"
status: "Active"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
license: "Apache-2.0"
created: "2025-11-27"
updated: "2025-12-13"
ai_assisted: "partial"
ai_assistance_details: "AI-assisted drafting and structural review with full human oversight and final approval."
---

### Status
**Active — Governance Law**

This policy supersedes **ARI Metadata Policy v1.0.0** in its entirety.

This policy defines the **mandatory metadata requirements** for all scientific, methodological, governance, and tooling artifacts published under the authority of the Aurora Research Initiative (ARI).

---

## 1. Purpose

Metadata is not descriptive ornamentation.  
Within ARI, metadata is a **governance primitive**.

This policy establishes the minimum metadata required to:

- Identify intellectual responsibility
- Preserve provenance and auditability
- Enable reproducibility across time, tools, and institutions
- Ensure compliance with the Neurotransparency Doctrine
- Prevent epistemic ambiguity in AI-assisted research

Any artifact lacking required metadata **cannot be considered institutionally valid**, regardless of content quality.

---

## 2. Scope

This policy applies to **all artifacts** produced, published, or archived under ARI authority, including but not limited to:

- Markdown documents
- Specifications
- Governance policies
- Research manuscripts
- Methodology documents
- Case study documentation
- Tooling documentation
- Machine-generated outputs intended for publication
- PDFs generated from Markdown sources

This policy applies **equally** to human-authored and AI-assisted content.

---

## 3. Governance Position

- ARI defines **what metadata is required**.
- ARI does **not** define how metadata is injected, validated, or enforced.
- Tooling that injects or validates metadata operates **downstream** of this policy.

This separation ensures that **governance cannot be altered by tooling convenience**.

---

## 4. Required Metadata Fields

All Markdown-based scientific or governance artifacts **MUST** include a top-level metadata block containing the following fields.

### M.1 — Title
```yaml
title:
```
A human-readable title uniquely identifying the artifact.

---

### M.2 — Version
```yaml
version:
```
A semantic version identifier for the artifact itself.

Versioning is governed by ARI semantic versioning rules and must reflect the epistemic impact of changes.

---

### M.3 — Status
```yaml
status:
```
One of:
- Draft
- Active
- Archived
- Superseded

Status indicates the artifact’s current institutional standing.

---

### M.4 — Required Author Attribution
```yaml
author:
```

All Markdown-based scientific artifacts **MUST** include an explicit `author` field.

This field identifies the **human or organizational entity** responsible for the intellectual content of the artifact.

- The author may be:
  - A named individual
  - A collective entity (e.g., “Waveframe Labs”)
- AI systems **MUST NOT** be listed as authors.
- Absence of this field constitutes a **metadata compliance violation**.

---

### M.5 — Maintainer
```yaml
maintainer:
```
The entity responsible for maintaining the artifact over time.

---

### M.6 — License
```yaml
license:
```
The license governing use, redistribution, and modification of the artifact.

---

### M.7 — Created / Updated Dates
```yaml
created:
updated:
```
ISO-8601 formatted dates indicating initial creation and most recent substantive update.

---

### M.8 — AI Assistance Disclosure
```yaml
ai_assisted:
```

Valid values:
- "true"
- "false"
- "partial"

If `ai_assisted` is `"true"` or `"partial"`, the following field **MUST** be present:

```yaml
ai_assistance_details:
```

This field **MUST NOT** appear when `ai_assisted: "false"`.

The disclosure **does not require** exact model versions or proprietary details. Unknown or custom models may be described descriptively.

This policy governs **disclosure**, not surveillance.

---

## 5. Optional Metadata Fields

```yaml
doi:
orcid:
related_artifacts:
repository:
```

Optional fields **MUST NOT** contradict required fields.

---

## 6. Format Requirements

- Metadata **MUST** appear at the very top of the document.
- YAML is the canonical metadata format.
- Metadata **MUST** be machine-parseable without inference.

---

## 7. Derived Artifacts

When a PDF or other derived artifact is generated from a Markdown source:

- The derived artifact **MUST inherit metadata** from the source file.
- Loss of required metadata constitutes a **tooling failure**, not a policy exception.
- Validation of inheritance lies with the maintainer or designated automation.

The source Markdown remains the canonical record.

---

## 8. Compliance and Violations

Artifacts missing required metadata are **non-compliant** and **MUST NOT** be treated as institutionally valid.

This policy defines **law**, not punishment.

---

## 9. Version Authority

This document is **Metadata Policy v2.0.0**.

- Changes to required fields or compliance conditions **MUST** result in a major version increment.
- Editorial or non-normative clarifications **MAY** be released as minor or patch versions.

---

## 10. Closing Principle

Metadata is the mechanism by which **truth remains attributable, inspectable, and reproducible** over time.

Without metadata, artifacts decay into authority without accountability.
