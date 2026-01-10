---
title: "ARI Metadata Policy"
filetype: "documentation"
type: "normative"
domain: "governance"
version: "3.0.1"
doi: "10.5281/zenodo.17743096"
status: "Active"
created: "2025-11-27"
updated: "2026-01-09"

author:
  name: "Shawn C. Wright"
  email: "swright@waveframelabs.org"
  orcid: "https://orcid.org/0009-0006-6043-9295"

maintainer:
  name: "Waveframe Labs"
  url: "https://waveframelabs.org"

license: "Apache-2.0"

copyright:
  holder: "Waveframe Labs"
  year: "2026"

ai_assisted: "partial"
ai_assistance_details: "AI-assisted revision under human oversight; aligned with AWO v2.0.0 metadata normalization."

anchors:
  - "ARI-METADATA-POLICY-v3.0.1"
---

# Aurora Research Initiative (ARI)
# Metadata Policy v3.0.1

## 1. Purpose

This policy defines the **mandatory metadata schema** for all governed artifacts in the Aurora ecosystem. It exists to guarantee:

- traceability  
- attribution  
- reproducibility  
- auditability  
- machine validation  

Any artifact lacking required metadata **is noncompliant** and MUST NOT be treated as authoritative.

---

## 2. Scope

This policy applies to every governed artifact in:

- ARI (governance)
- AWO (methodology)
- CRI-CORE (enforcement)
- dependent ecosystems and case studies

This policy governs **YAML metadata blocks** in Markdown files and defines the fields required for automated validation by Stamp and CRI-CORE.

---

## 3. Required Metadata Schema

Every governed Markdown file MUST begin with a `---` fenced YAML block containing ALL of the following fields:

```
title
filetype
type
domain
version
doi
status
created
updated
author (object)
maintainer (object)
license
copyright (object)
ai_assisted
ai_assistance_details
dependencies (array)
anchors (array)
```

All fields listed above are **mandatory** unless otherwise specified by a system-level override.

---

## 4. Field Requirements

### 4.1 Title
- MUST be included
- MUST be a human-readable string

---

### 4.2 Filetype
Defines the structural nature of the file.  
MUST be one of:

- documentation
- specification
- operational
- adr
- log
- schema

---

### 4.3 Type (Authority Level)
Defines the **normative authority** of the document.  
MUST be one of:

- normative
- non-normative
- guidance
- specification

This field determines how CRI-CORE, Stamp, and related tooling interpret document authority.

---

### 4.3A Domain (Conceptual Layer)
**New in v3.0.1**

The `domain` field defines the **conceptual layer** in the Aurora ecosystem to which the document belongs.

MUST be one of:

- governance
- methodology
- enforcement
- documentation
- case-study

`domain` disambiguates document category from normative authority (`type`) and is required for validation, classification, and contract mapping.

---

### 4.4 Version
- MUST follow semantic versioning (`MAJOR.MINOR.PATCH`)

---

### 4.5 DOI
- MUST be present
- README and concept-level documents MUST use concept DOI
- Version-level artifacts MUST use version DOI or placeholder format:
  ```
  doi: "TBD-2.0.0"
  ```

---

### 4.6 Status
MUST be one of:

- Draft
- Active
- Archived
- Deprecated

---

### 4.7 Dates
- `created` MUST NOT change once set
- `updated` MUST reflect real modification date
- MUST follow ISO-8601 (`YYYY-MM-DD`)

---

## 5. Attribution Requirements

### 5.1 Author

```
author:
  name:
  email:
  orcid:
```

- MUST identify a human originator
- AI MUST NOT be listed as author

---

### 5.2 Maintainer

```
maintainer:
  name:
  url:
```

- MUST identify the organizational entity responsible for stewardship

---

### 5.3 Copyright

```
copyright:
  holder:
  year:
```

- MUST reflect intellectual ownership and publication year

---

## 6. AI Assistance Disclosure

### 6.1 ai_assisted
MUST be one of:

- none
- partial
- extensive

### 6.2 ai_assistance_details
- MUST be present for `"partial"` or `"extensive"`
- MUST NOT appear for `"none"`
- MUST describe the nature of AI contribution accurately

---

## 7. Dependencies

- MUST be a list of relative paths
- MUST resolve to actual files
- MUST NOT form circular graphs
- SHOULD include all referenced or upstream documents

---

## 8. Anchors

- MUST be a list
- MUST follow format:
  ```
  <SYSTEM>-<DOCNAME>-v<MAJOR.MINOR.PATCH>
  ```
- MUST be unique across the repository

---

## 9. Derived Artifacts

Generated outputs **MUST preserve metadata equivalence**, including:

- title
- version
- DOIs
- authorship
- AI provenance
- license

Stamp and CRI-CORE MAY enforce this automatically.

---

## 10. Compliance Rules

An artifact is **noncompliant** if:

- any required field is missing  
- fields use invalid or disallowed values  
- metadata format is malformed  
- AI attribution is incorrect  
- DOIs are missing or mismatched  
- dependencies cannot resolve  

Noncompliant artifacts MUST NOT be treated as authoritative.

---

## 11. Policy Versioning

This policy increments according to:

- **MAJOR** — breaking changes to field set or semantics  
- **MINOR** — additive, non-breaking enhancements  
- **PATCH** — clarifications, structural corrections, or metadata-level fixes  

v3.0.1 is a **PATCH** revision introducing explicit domain-field requirements and aligning metadata semantics.

---

## 12. Ratification

This policy becomes binding upon publication in the ARI repository and governs all subsequent metadata across Aurora systems.

---

<p align="center">
  <sub>© 2026 Waveframe Labs · <a href="https://waveframelabs.org">waveframelabs.org</a></sub>
</p>  
