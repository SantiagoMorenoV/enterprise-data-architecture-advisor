# Semantic Layer Guidance

## Core Principles

The Semantic Layer must provide a single, trusted, and governed representation of business information.

Dimensions should:

- Be conformed whenever possible.
- Have a single business meaning.
- Avoid duplicate business definitions.
- Support enterprise governance requirements.
- Be understandable by business users.

Metrics should:

- Have a business owner.
- Have a data steward.
- Be traceable to source systems.
- Be auditable.
- Have documented calculation logic.
- Support enterprise reporting standards.

---

## KPI Definition Standard

Every KPI or Metric must include:

### Business Definition

A clear business description written in business language.

### Formula

The official calculation logic.

### Granularity

The level at which the metric is measured.

Examples:

- Transaction
- Customer
- Product
- Store
- Month

### Source System

The system providing the original data.

### System of Record

The authoritative source for the metric.

### Data Owner

The person or business area accountable for the KPI.

### Data Steward

The person responsible for maintaining quality and definitions.

### Refresh Frequency

Examples:

- Real-time
- Hourly
- Daily
- Weekly
- Monthly

### Data Quality Rules

Validation and control rules used to ensure trustworthiness.

### Lineage Dependencies

Upstream systems, transformations and datasets required to calculate the metric.

---

## Semantic Layer Governance Rules

- Business definitions must be documented.
- Duplicate metrics are prohibited.
- Conflicting metric definitions are prohibited.
- Naming conventions must be standardized.
- Metrics must reference approved business glossary terms.
- Every KPI requires ownership and stewardship.
- Every KPI must have a documented lineage.
- Every metric must be reproducible.

---

## Dimensional Modeling Considerations

For every Dimension define:

- Business Meaning
- Grain
- Hierarchies
- Relationships
- Conformance Status

For every Fact define:

- Grain
- Measures
- Additivity
- Related Dimensions
- Calculation Logic

---

## Hierarchy Standards

Hierarchies should:

- Follow business reporting requirements.
- Be clearly documented.
- Avoid ambiguity.
- Support drill-down and roll-up analysis.

Examples:

### Geographic Hierarchy

Country → Region → City → Store

### Product Hierarchy

Category → Subcategory → Product

---

## Data Governance Considerations

Always identify:

- Data Owner
- Data Steward
- Business Owner
- System Owner

Always document:

- Metadata requirements
- Lineage requirements
- Data quality controls
- Audit requirements
- Compliance considerations

---

## Business Glossary Alignment

All semantic objects must align with approved business glossary definitions.

For every semantic object document:

- Business Name
- Business Definition
- Synonyms
- Related Metrics
- Related Dimensions

---

## Anti-Patterns

Avoid:

- Duplicate KPIs.
- Conflicting metric definitions.
- Undefined business ownership.
- Ambiguous dimensions.
- Hidden calculations.
- Metrics without lineage.
- Metrics without stewardship.
- Semantic models without governance.
- Reuse of terms with different meanings.
- Business logic embedded only in reports.

---

## Semantic Layer Quality Checklist

For every KPI verify:

- Business definition exists.
- Formula is documented.
- Owner is assigned.
- Steward is assigned.
- Lineage is documented.
- Source system is known.
- Quality controls are defined.
- Refresh frequency is defined.

For every Dimension verify:

- Business meaning is unique.
- Hierarchies are documented.
- Conformance status is known.
- Ownership is established.

For every Semantic Model verify:

- Naming standards are applied.
- Governance controls are implemented.
- Metadata is documented.
- Auditability is supported.
- Business glossary alignment is verified.