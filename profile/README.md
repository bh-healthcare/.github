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

## Projects

- **bh-audit-schema**  
  Canonical audit event schema for behavioral healthcare systems.

- **bh-fastapi-audit**  
  A FastAPI middleware implementation that emits audit events conforming to the bh-audit-schema standard.

- **bh-data-lake-reference**  
  Reference architectures for storing, retaining, and querying healthcare audit events.

## Status

Projects are actively developed and used in real-world behavioral healthcare systems. All repositories are open-source and welcome engineering-focused contributions.