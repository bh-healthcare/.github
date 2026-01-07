# Behavioral Healthcare Infrastructure & Standards

This organization publishes open-source infrastructure, standards, and reference implementations for secure, privacy-preserving behavioral healthcare systems.

Behavioral healthcare systems handle some of the most sensitive categories of regulated data, including therapy notes, substance use records, and crisis-related information. The projects in this organization focus on defining practical, engineering-first primitives that help organizations build compliant, auditable systems without requiring large compliance or governance teams.

While designed with behavioral healthcare as the primary use case, these standards and reference implementations are applicable to healthcare platforms more broadly.

## Scope

Projects in this organization focus on:

- Standardized audit event schemas for regulated healthcare systems  
- PHI-safe, compliance-aligned audit logging primitives  
- Reference architectures for secure data storage, retention, and access review  
- Engineering mappings to common healthcare compliance control objectives  

This organization intentionally avoids application-specific code, proprietary integrations, or domain-specific business logic.

## Philosophy

The goal is not to provide legal compliance guarantees, but to publish reusable engineering foundations that make secure and compliant system design the default rather than an afterthought.

## Founding Principles

### 1. Infrastructure Over Applications
This organization focuses on primitives, standards, and reference implementations and the not end-user applications. Projects should be reusable across organizations and deployment environments.

### 2. Schema First
Stable, versioned schemas are treated as public contracts. Implementations must conform to published schemas rather than inventing ad-hoc structures.

### 3. PHI Safety by Default
Systems handling regulated healthcare data must minimize exposure by default. Audit artifacts must never require logging raw PHI to be useful.

### 4. Engineering Mappings, Not Legal Claims
Projects provide engineering mappings to common compliance objectives (e.g., auditability, traceability, retention), but do not claim legal compliance or provide legal advice.

### 5. Cloud-Native, Vendor-Neutral
Reference implementations should support modern cloud architectures while avoiding hard dependencies on proprietary platforms wherever possible.

### 6. Practical Adoption
Design decisions favor simplicity, clarity, and operational usability over theoretical completeness.

### 7. Public Benefit
All projects are developed with the goal of reducing barriers for small and mid-sized healthcare organizations to adopt secure, compliant system designs.

## Projects

- **bh-audit-schema**  
  Canonical audit event schema for behavioral healthcare systems.

- **bh-fastapi-audit**  
  A FastAPI middleware implementation that emits audit events conforming to the bh-audit-schema standard.

- **bh-data-lake-reference**  
  Reference architectures for storing, retaining, and querying healthcare audit events.

## Status

Projects are actively developed and used in real-world behavioral healthcare systems. All repositories are open-source and welcome engineering-focused contributions.

