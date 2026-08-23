# Behavioral Healthcare Infrastructure & Standards

This organization publishes open-source infrastructure, standards, and tooling for secure, privacy-preserving behavioral healthcare systems.

Behavioral healthcare systems handle some of the most sensitive categories of regulated data, including therapy notes, substance use records, and crisis-related information. The projects in this organization focus on defining practical, engineering-first primitives that help organizations build compliant, auditable, and clinically effective systems without requiring large compliance or governance teams.

While designed with behavioral healthcare as the primary use case, these standards and tooling are applicable to healthcare platforms more broadly.

## Scope

Projects in this organization focus on:

- Standardized, versioned audit event schemas for regulated healthcare systems, including AI agent attribution
- PHI-safe, compliance-aligned audit logging primitives
- Attribution-enforcing emission for MCP servers and other agent-mediated workflows
- Clinical safety signal detection for unstructured text
- Reference architectures for secure data storage, retention, and access review
- Engineering mappings to common healthcare compliance control objectives

## Philosophy

The goal is not to provide legal compliance guarantees, but to publish reusable engineering foundations that make secure, compliant, and clinically informed system design the default rather than an afterthought.

## Founding Principles

### 1. Infrastructure Over Applications
This organization focuses on primitives, standards, and reference implementations, not end-user applications. Projects should be reusable across organizations and deployment environments.

### 2. Schema First
Stable, versioned schemas are treated as public contracts. Implementations must conform to published schemas rather than inventing ad-hoc structures.

### 3. PHI Safety by Default
Systems handling regulated healthcare data must minimize exposure by default. Audit artifacts must never require logging raw PHI to be useful. Clinical text processing must be stateless and ephemeral.

### 4. Engineering Mappings, Not Legal Claims
Projects provide engineering mappings to common compliance objectives (e.g., auditability, traceability, retention), but do not claim legal compliance or provide legal advice.

### 5. Cloud-Native, Vendor-Neutral
Reference implementations should support modern cloud architectures while avoiding hard dependencies on proprietary platforms wherever possible.

### 6. Practical Adoption
Design decisions favor simplicity, clarity, and operational usability over theoretical completeness.

### 7. Public Benefit
All projects are developed with the goal of reducing barriers for small and mid-sized healthcare organizations to adopt secure, compliant system designs.

## Projects

### Audit Infrastructure

- **[bh-audit-schema](https://github.com/bh-healthcare/bh-audit-schema)**
  Canonical, versioned audit event schema for behavioral healthcare systems. v2.0 adds AI agent attribution and a human-agent delegation chain, with HIPAA/SOC 2/42 CFR Part 2 compliance mappings.

- **[bh-audit-logger](https://github.com/bh-healthcare/bh-audit-logger)**
  Cloud and framework-agnostic Python library for emitting privacy-preserving audit events conforming to bh-audit-schema. Zero runtime dependencies.

- **[bh-fastapi-audit](https://github.com/bh-healthcare/bh-fastapi-audit)**
  FastAPI middleware that automatically emits audit events for every HTTP request with HIPAA-safe defaults.

- **[bh-audit-logger-examples](https://github.com/bh-healthcare/bh-audit-logger-examples)**
  Examples and integration tests for bh-audit-logger covering every public API surface. Framework-agnostic.

- **[bh-fastapi-examples](https://github.com/bh-healthcare/bh-fastapi-examples)**
  Minimal applications demonstrating bh-fastapi-audit with production-hardened, HIPAA-safe defaults.

### Agent Attribution

- **[bh-mcp-attribution](https://github.com/bh-healthcare/bh-mcp-attribution)**
  Attribution-enforcing audit emission for MCP servers and gateways. Reference implementation of the enforced emission tier from bh-audit-schema v2. Prototype; not a production control.

### Clinical Tooling

- **[bh-sentinel](https://github.com/bh-healthcare/bh-sentinel)**
  Multi-layer NLP pipeline for clinical safety signal detection in behavioral health text. Detects self-harm/suicidal ideation, harm to others, medication non-adherence, substance use, clinical deterioration, and protective factors. Designed for HIPAA-safe, stateless deployment with clinician-in-the-loop review. FDA CDS-aligned.

- **[bh-sentinel-examples](https://github.com/bh-healthcare/bh-sentinel-examples)**
  Reproducible local integrations for bh-sentinel (core and ml). Hands-on companion for running Layer 1 pattern matching and Layer 2 zero-shot detection on checked-in corpora.

### Reference Architecture

- **[bh-data-lake-reference](https://github.com/bh-healthcare/bh-data-lake-reference)**
  Reference architectures for storing, retaining, and querying healthcare audit events.

## Status

Projects are actively developed and used in real-world behavioral healthcare systems. Public repositories are open-source and welcome engineering-focused contributions.
