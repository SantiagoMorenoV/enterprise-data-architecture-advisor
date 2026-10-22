# Medallion Architecture

## Purpose

The Medallion Architecture organizes data into progressive quality layers.

## Selection Criteria

Choose Medallion Architecture when:

- Multiple data sources must be integrated.
- Data quality improvements are required before business consumption.
- Lakehouse architectures are being implemented.
- Data lineage and traceability are important.
- Analytics, reporting and machine learning workloads share the same platform.
- A layered data engineering approach is desired.
- Microsoft Fabric, Databricks or similar modern platforms are being used.

Prefer Medallion Architecture when:

- Raw data must be preserved.
- Data transformations must be auditable.
- Governance requirements exist across multiple stages of data processing.
- Business-ready datasets must be separated from ingestion processes.

Avoid when:

- The solution is extremely simple.
- Only a single curated dataset exists.
- Data complexity does not justify multiple layers.
- The organization lacks operational maturity to manage multiple layers.

Complexity: Medium

Governance Maturity Required: Medium

Scalability: High

Auditability: High

Lineage Support: High

## Bronze Layer

Purpose:

- Raw data ingestion
- Minimal transformation

Characteristics:

- Source-centric
- Immutable when possible
- Historical retention

Typical Activities:

- Landing source extracts
- Initial ingestion
- Basic metadata capture
- Source preservation

## Silver Layer

Purpose:

- Data cleansing
- Standardization
- Integration

Characteristics:

- Business-ready structures
- Quality controls
- Common business entities

Typical Activities:

- Data quality validation
- Standardization
- Conforming business entities
- Data enrichment
- Deduplication

## Gold Layer

Purpose:

- Analytics consumption
- Reporting
- Machine Learning

Characteristics:

- Aggregated datasets
- Data products
- KPI-ready datasets

Typical Activities:

- Business aggregations
- Semantic model preparation
- KPI generation
- Data product creation
- Reporting optimization

## Advantages

- Clear separation of concerns
- Incremental quality improvement
- Governance support
- Improved auditability
- Better lineage visibility
- Flexible support for analytics and AI

## Risks

- Layer proliferation
- Storage growth
- Duplication if poorly governed
- Increased operational complexity
- Additional processing costs

## Architecture Considerations

Data quality should improve progressively:

Bronze → Silver → Gold

Each layer should define:

- Ownership
- Stewardship
- Quality controls
- Metadata requirements
- Lineage requirements

Avoid bypassing layers unless justified and documented.

## Fabric Mapping

### Bronze

- OneLake Raw Zone
- Data Factory Ingestion
- Event Streams

### Silver

- Curated Lakehouse
- Data Engineering Workloads
- Data Transformations

### Gold

- Semantic Models
- Data Warehouse
- Power BI
- Data Products

## Common Anti-Patterns

Avoid:

- Reporting directly from Bronze.
- Mixing raw and curated data in the same layer.
- Implementing Gold datasets without governance.
- Skipping quality controls in Silver.
- Building KPIs directly on raw ingestion data.
- Creating duplicate business entities across layers.