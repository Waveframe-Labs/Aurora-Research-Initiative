---
title: "Metadata Policy"
version: "1.0.0"
status: "Draft — Metadata Requirements"
created: "2025-11-26"
type: "epistemics"
---

# Aurora Research Initiative — Metadata Policy (v1.0.0)

This policy defines the **required metadata structure** for all documents, artifacts, workflows,
and research products within the Aurora ecosystem. Metadata provides the backbone of provenance,
traceability, reproducibility, and institutional accountability.

This document translates ARI’s epistemic doctrine into concrete, enforceable metadata rules.

---

# 1. Purpose of Metadata

Metadata in the Aurora ecosystem ensures:

- reproducibility of artifacts  
- transparent provenance  
- identity binding  
- version consistency  
- auditability of reasoning  
- governance traceability  
- independence of validation  

Every artifact—textual, computational, scientific—must include a metadata block unless explicitly exempted.

---

# 2. Required Metadata Block Format

All documents must begin with a YAML front matter block enclosed in `---` delimiters:

```yaml
---
title: "Document Title"
version: "X.Y.Z"
status: "Draft | Active | Archived | Deprecated"
created: "YYYY-MM-DD"
updated: "YYYY-MM-DD"
type: "governance | epistemics | architecture | log | roadmap | research | tooling | documentation"
author: "Name or Role"
dependencies:
  - "OtherDoc.md"
anchors:
  - "ANCHOR-ID"
---
```

---

# 3. Mandatory Fields

### 3.1 Required
- title
- version
- status
- created
- type
- author

### 3.2 Optional
- updated
- dependencies
- anchors

---

# 4. Metadata for Code & Tooling Artifacts

Scripts and tooling artifacts must include:
- runner
- integrity hashes
- type: tooling

---

# 5. Enforcement Model

Enforced via:
- Doc Guard
- metadata normalization workflow
- CRI-CORE (future)

---

# 6. Metadata Compliance Rules

- All files must include metadata except images, binaries, raw data
- Updates must preserve metadata
- Deletions require log entries

---

# 7. Metadata Exceptions

- images
- binaries
- raw data
- generated outputs
- LICENSE files

---

# 8. Directory-Level Metadata Requirements

Each directory must include a descriptor.

---

# 9. Provenance & Artifact Identity

All artifacts must be identity-bound, versioned, timestamped, and traceable.

---

# 10. Revision & Amendment

Requires:
- IC approval
- log entry
- version bump
- rationale
