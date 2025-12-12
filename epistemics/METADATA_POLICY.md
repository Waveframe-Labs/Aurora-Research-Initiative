---
title: "Metadata Policy"
filetype: "documentation"
type: "governance"
version: "2.0.0"
status: "Active"
created: "2025-11-27"
updated: "2025-12-12"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
contact: "swright@waveframelabs.org"
license: "Apache-2.0"
ai_assisted: "partial"
ai_assistance_details: "AI-assisted drafting and structural review with full human oversight and final approval."
policy_version: "ARI-Metadata-2.0.0"
---

# Aurora Research Initiative (ARI)

# Metadata Policy v2.0.0

**Status:** Active — Governance Law  
**Supersedes:** ARI Metadata Policy v1.0.0 (in full)

---

## 1. Purpose

This policy defines the mandatory metadata requirements for all **Markdown-based scientific artifacts** and governance documents published under the Aurora ecosystem. Its goal is to ensure that each artifact is **traceable, attributable, auditable, and reconstructible**.

Artifacts lacking required metadata are **not institutionally valid** and MUST NOT be treated as compliant outputs.

---

## 2. Scope

This policy applies to:

- Governance documents within ARI
- Method specifications and documentation within AWO
- Enforcement and tooling documentation within CRI-CORE
- Published scientific artifacts, reports, and case-study documents produced under the Aurora hierarchy

This policy governs **metadata blocks** included in Markdown files. It does not define PDF metadata fields, but **derived artifacts MUST preserve equivalent metadata** (see Section 7).

---

## 3. Governance and Enforcement Separation

This policy defines institutional law. Enforcement is implemented by external tooling (e.g., validators, CI checks, Doc Guard, Stamp) that MUST conform to this policy.

Tooling MAY flag, block, or report violations; however, the policy itself is the authoritative reference, not any specific tool implementation.

---

## 4. Required Metadata Block

Every governed Markdown file MUST begin with a **top-of-file YAML metadata block** delimited by `---` lines.

Example:

```yaml
---
title: "Example Artifact"
filetype: "documentation"
type: "specification"
version: "1.0.0"
status: "Draft"
created: "2025-12-01"
updated: "2025-12-10"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
license: "CC-BY-4.0"
ai_assisted: "true"
ai_assistance_details: "Drafted with AI assistance; reviewed and approved by maintainer."
---
```

---

## 5. Required Fields

The following fields are REQUIRED unless explicitly exempted by this policy:

### M.1 — Title

- `title` MUST be present.
- `title` MUST be a human-readable string.

### M.2 — Version

- `version` MUST be present.
- `version` MUST follow semantic versioning: `MAJOR.MINOR.PATCH`.

### M.3 — Status

- `status` MUST be present.
- `status` MUST be one of: `Draft`, `Active`, `Archived`, `Superseded`.

### M.4 — Required Author Attribution

- `author` MUST be present.
- `author` MUST identify the responsible **human or organizational entity** for intellectual content.
- Anonymous authorship is not permitted under standard ARI governance.
- AI systems MUST NOT be listed as `author`.

### M.5 — Dates

- `created` MUST be present.
- `updated` MUST be present.
- Both MUST use ISO-8601 date format: `YYYY-MM-DD`.

### M.6 — License

- `license` MUST be present.
- `license` MUST be an SPDX identifier when available (e.g., `Apache-2.0`, `CC-BY-4.0`, `CC-BY-NC-SA-4.0`).

### M.7 — AI Assistance Disclosure

- `ai_assisted` MUST be present.
- `ai_assisted` MUST be one of: `"true"`, `"false"`, `"partial"` (string enum).
- If `ai_assisted` is `"true"` or `"partial"`, `ai_assistance_details` MUST be present.
- If `ai_assisted` is `"false"`, `ai_assistance_details` MUST NOT appear.

Disclosure MUST be accurate. The goal is accountability without requiring proprietary details.

---

## 6. Optional Fields

The following fields are OPTIONAL unless required by a repo-level policy:

- `maintainer`
- `contact`
- `type`
- `filetype`
- `dependencies`
- `anchors`
- `policy_version` (recommended for policies)

Optional fields MUST NOT conflict with required fields and MUST be valid YAML.

---

## 7. Derived Artifacts

If a governed artifact is rendered or exported (e.g., Markdown → PDF), the derived artifact MUST preserve **equivalent metadata**, including at minimum:

- Title
- Version
- Status
- Author attribution
- License
- AI assistance disclosure (when applicable)

Maintainers or designated automation are responsible for validating that derived artifacts retain metadata equivalence.

---

## 8. Institutional Validity

Any governed artifact that:

- lacks a required field,
- contains an invalid field value,
- violates an explicit prohibition in this policy,

is **noncompliant**.

Noncompliant artifacts MUST NOT be treated as ARI-valid institutional outputs, and MUST NOT be used as authoritative references for downstream governance, tooling, or research claims.

---

## 9. Policy Versioning

Changes to this policy MUST follow semantic versioning:

- MAJOR: changes to required fields, field meanings, allowed enums, or compliance rules
- MINOR: additions that do not change compliance requirements
- PATCH: formatting, clarifications, and non-normative wording changes that do not change enforcement logic

Policy version increments are governance actions and MUST be logged and released according to ARI release practice.

---

## 10. Ratification

This policy is ratified upon publication in the ARI repository and is binding across the Aurora ecosystem from that point forward.
