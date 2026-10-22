# Data Vault 2.0

## Purpose

Data Vault 2.0 is an enterprise data modeling methodology designed to support scalability, auditability, historical tracking and agility.

## Best For

- Enterprise Data Warehouses
- Multi-source integrations
- Regulatory environments
- Audit requirements
- Frequent source system changes

## Selection Criteria

Choose Data Vault when:

- Multiple source systems must be integrated into a unified enterprise data platform.
- Full historical traceability is required.
- Regulatory compliance and auditability are important.
- Source systems change frequently.
- Business requirements evolve rapidly.
- Enterprise-scale integration is required.
- Long-term maintainability is a priority.

Prefer Data Vault over traditional dimensional models when:

- Enterprise integration is more important than reporting.
- Data must be preserved with minimal business transformation.
- Regulatory requirements mandate historical reconstruction.

Avoid Data Vault when:

- Dashboard delivery is the primary objective.
- The solution scope is small.
- Business reporting is the only requirement.
- The organization lacks Data Vault expertise.
- Simplicity and rapid implementation are more important than auditability.

Complexity: High

Governance Maturity Required: Medium-High

Scalability: Very High

Time to Business Reporting: Medium-High

Auditability: Very High

## Core Components

### Hub

Stores unique business keys.

Examples:

- Customer
- Product
- Supplier
- Employee

Characteristics:

- Immutable
- Business-centric
- No descriptive attributes

### Link

Stores relationships between business entities.

Examples:

- Customer purchases Product
- Employee works in Department

Characteristics:

- Defines associations
- Supports many-to-many relationships

### Satellite

Stores descriptive context.

Examples:

- Customer Name
- Customer Address
- Customer Status

Characteristics:

- Historical tracking
- Time-variant
- Audit-friendly

## Advantages

- Full historical traceability
- High scalability
- Flexible ingestion
- Strong auditability

## Risks

- Increased modeling complexity
- Requires specialized knowledge
- Additional layers for reporting

## Recommended Usage

Use Data Vault as the enterprise integration layer.

Prefer Kimball-style dimensional models or Semantic Models for business consumption.

## Architecture Considerations

Data Vault is typically most effective when combined with:

- Data Lake architectures
- Lakehouse architectures
- Enterprise Data Warehouses
- Semantic Layers
- Kimball Dimensional Models for reporting

Typical flow:

Source Systems → Data Vault → Business Vault (Optional) → Dimensional Models / Semantic Layer → Reports & Analytics

## Common Anti-Patterns

Avoid:

- Exposing raw Data Vault structures directly to business users.
- Building dashboards directly on Hubs, Links and Satellites.
- Loading descriptive attributes into Hubs.
- Using Links to store descriptive business data.
- Skipping business key definition and governance.
- Implementing Data Vault without lineage and metadata management.