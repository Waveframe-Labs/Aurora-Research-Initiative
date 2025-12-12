# ADR-0001: Metadata Enforcement, Authorship, and Schema Canonicalization

## Status
Accepted

## Context

The Aurora Research Initiative (ARI) governs institutional correctness for all research artifacts produced under the Aurora ecosystem. As ARI matured from an initial governance concept into an operational institution, limitations were identified in the original metadata policy (v1.0.0).

Specifically:
- Author attribution was not explicitly required at the policy level.
- Metadata validation rules were partially implicit and tool-dependent.
- Derived artifacts (e.g., rendered PDFs) could lose or omit authoritative metadata.
- The distinction between governance policy and enforcement mechanisms was not formally recorded.

These gaps resulted in artifacts that were structurally valid but institutionally ambiguous, undermining provenance guarantees and auditability expectations.

## Decision

ARI formally adopts Metadata Policy v2.0.0 as binding institutional law, with the following architectural decisions:

1. **Mandatory Author Attribution**  
   All scientific artifacts must declare a responsible human or organizational author in top-level metadata.

2. **Non-Authorship of AI Systems**  
   AI systems may assist in artifact production but cannot be listed as authors or intellectual owners.

3. **Explicit AI-Assistance Disclosure**  
   AI involvement must be disclosed using a structured, non-proprietary schema that supports partial, unknown, or custom model usage.

4. **Schema Canonicalization**  
   The JSON Schema associated with the metadata policy is designated as the canonical machine-enforceable specification. Human-readable policy text governs meaning; schemas govern validation.

5. **Policy–Enforcement Separation**  
   ARI defines rules and constraints. Enforcement mechanisms are external and may evolve independently, provided they conform to the policy and schema.

6. **Derived Artifact Inheritance**  
   All derived artifacts must inherit authoritative metadata from their source artifact. Loss of metadata constitutes non-compliance.

7. **Governance-Level Versioning**  
   Changes to required metadata fields constitute major version increments, treated as legal changes rather than editorial updates.

## Rationale

These decisions ensure that institutional authority resides in declared policy rather than tooling, individuals, or execution environments. By mandating authorship and formalizing disclosure without over-specifying implementation details, ARI preserves both accountability and adaptability.

Separating governance from enforcement prevents conflicts of interest, where tooling might implicitly define correctness. Canonical schemas provide deterministic validation while remaining subordinate to institutional law.

## Consequences

- Artifacts lacking required metadata are institutionally invalid.
- Existing repositories must be revised to achieve compliance with Metadata Policy v2.0.0.
- Tooling may flag, reject, or annotate non-compliant artifacts but must not silently modify authoritative content.
- Future governance changes must be recorded through ADRs prior to enforcement.

## Alternatives Considered

- **Tool-defined metadata rules**: Rejected due to governance capture risk.
- **Optional author attribution**: Rejected due to accountability failure.
- **Full AI provenance requirements**: Rejected due to infeasibility and privacy constraints.
- **Backward compatibility exemptions**: Rejected to avoid permanent ambiguity.

## Notes on Enforcement Boundary

This ADR intentionally does not prescribe specific enforcement tools or workflows. Validation, reporting, and remediation mechanisms are implementation concerns governed by downstream systems, provided they do not alter, override, or redefine ARI policy.

This decision establishes the precedent for all future governance changes within ARI.
