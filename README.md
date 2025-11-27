---
title: "Aurora Research Initiative (ARI) — Repository Overview"
version: "1.0.0"
status: "Active"
created: "2025-11-27"
updated: "2025-11-27"
type: "documentation"
author: "Aurora Research Initiative (ARI)"
dependencies:
  - "ARI_BOUNDARIES_AND_RESPONSIBILITIES.md"
  - "GOVERNANCE_MODEL.md"
  - "EPISTEMIC_DOCTRINE.md"
anchors:
  - "ARI-README-v1.0"
---

# Aurora Research Initiative (ARI)  
[![DOI](https://zenodo.org/badge/1105021427.svg)](https://doi.org/10.5281/zenodo.17743096)

The **Aurora Research Initiative (ARI)** is the governance and epistemic foundation of the Aurora ecosystem.  
ARI defines the institutional rules, constraints, doctrines, metadata models, and change-control structures that govern:

- **AWO** — the Aurora Workflow Orchestration method  
- **CRI-CORE** — the deterministic execution and enforcement engine  
- **Waveframe Systems** — engineering, tooling, and applied research  
- **Case Studies** — scientific models developed under ARI governance  

ARI is not an engineering repo. It contains **no code**, **no workflows**, and **no tooling logic**.  
Its role is to define institutional correctness, epistemic rigor, and governance invariants.

---

## Purpose

ARI establishes:

- **Epistemic doctrine** — how knowledge is defined, validated, and governed  
- **Institutional governance** — separation of roles, powers, and responsibilities  
- **Method constraints** — what the AWO method must uphold  
- **Tooling constraints** — what CRI is allowed and forbidden to enforce  
- **Organizational hierarchy** — the relationship between ARI, Waveframe Labs, and Waveframe Systems  
- **Versioning & release policy** — how the ecosystem evolves  
- **Metadata policy** — the schema required for all artifacts  

ARI provides the rules.  
Waveframe Systems builds the tools.  
Waveframe Labs operates the ecosystem.

---

## Position in the Ecosystem

The Aurora ecosystem follows a strict institutional hierarchy:
```
Waveframe Labs (organization)
│
├── Aurora Research Initiative (ARI)
│ Governance • Epistemics • Doctrine • Constraints
│
└── Waveframe Systems
Engineering • Tooling • Method Execution
│
├── AWO — Workflow Methodology
├── CRI-CORE — Deterministic Execution Engine
└── Case Studies (Waveframe v4.0, Societal Health Simulator, etc.)
```

### ARI governs method + tooling + engineering  
but  
### does not implement method or tooling.

This separation is foundational to Aurora's integrity and reproducibility guarantees.

---

## Repository Structure
```
architecture/ High-level institutional architecture for ARI
epistemics/ Epistemic doctrine and metadata policy
governance/ Constitutional documents and operating rules
logs/ Governance and initialization logs
roadmap/ High-level development and institutional roadmap
LICENSE Apache 2.0 license
CITATION.cff Citation metadata
README.md This document
```

---

## Constitutional Documents

Located under `/governance/`:

- **ARI_BOUNDARIES_AND_RESPONSIBILITIES.md**  
- **METHOD_CONSTRAINTS.md**  
- **TOOLING_CONSTRAINTS.md**  
- **ROLE_SEPARATION_CHARTER.md**  
- **CHANGE_CONTROL_AND_VERSIONING_POLICY.md**  
- **GOVERNANCE_MODEL.md**  
- **GOVERNANCE_LOG.md**

These define ARI’s authority, responsibilities, and institutional guarantees.

---

## Epistemic Foundations

Located under `/epistemics/`:

- **EPISTEMIC_DOCTRINE.md**  
- **METADATA_POLICY.md**

These documents define Aurora’s epistemic worldview:  
how knowledge is represented, constrained, validated, and archived.

---

## Architecture

Located under `/architecture/`:

- **ARI_ARCHITECTURE.md**  
  High-level structural model of ARI and its governance layers.

---

## Logs

Located under `/logs/`:

- **INIT_LOG.md**  
- **GOVERNANCE_LOG.md**

These record institutional events, releases, approvals, and governance actions.

---

## Roadmap

Located under `/roadmap/`:

- **ROADMAP.md**  
  High-level guidance for future ARI development and institutional evolution.

---

## Licensing

This repository is licensed under the **Apache License 2.0**, enabling:

- open scientific use  
- reproducibility  
- modification  
- redistribution  

with proper attribution.

---

## Citation  

To cite ARI:

```bibtex
@software{
  title        = {Aurora Research Initiative (ARI)},
  author       = {Wright, Shawn C.},
  year         = {2025},
  doi          = {10.5281/zenodo.17743097},  
  url          = {https://github.com/Waveframe-Labs/Aurora-Research-Initiative},
}
```
## Status

Version: 1.0.0
```  
Role: Institutional Governance Layer
Scope: Full governance, epistemics, constraints, and constitutional structure
Release: v1.0.0
DOI: 10.5281/zenodo.17743097     
```  
## Identity & Contact

**Organization:** Waveframe Labs  
**Initiative:** Aurora Research Initiative (ARI)  
**Primary Contact:** swright@waveframelabs.org  
**ORCID:** https://orcid.org/0009-0006-6043-9295  
**Repository:** https://github.com/Waveframe-Labs/Aurora-Research-Initiative  
**Website:** https://waveframelabs.org  

For questions about governance, epistemic standards, or the Aurora ecosystem,  
contact the ARI Institutional Coordinator at the email above.
