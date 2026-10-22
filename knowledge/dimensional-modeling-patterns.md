# Dimensional Modeling Patterns

## Purpose

Dimensional Modeling supports business analytics and reporting.

## Selection Criteria

Choose Dimensional Modeling when:

- Business reporting is the primary objective.
- Self-service analytics is required.
- Business users are the primary consumers.
- Fast query performance is important.
- Power BI, Tableau, Looker or similar BI tools are the primary consumption layer.
- Metrics and KPIs require a business-friendly structure.
- Data consumption is more important than enterprise integration.

Prefer Dimensional Modeling when:

- Executive dashboards are required.
- Enterprise reporting standards must be enforced.
- Business users need intuitive datasets.
- Analytics adoption is a strategic objective.

Avoid when:

- Enterprise-wide integration is the primary goal.
- Full historical lineage is the highest priority.
- Frequent structural changes occur in source systems.
- Regulatory traceability is more important than reporting simplicity.

Complexity: Medium

Governance Maturity Required: Medium

Scalability: Medium-High

Business User Adoption: Very High

Reporting Performance: Very High

## Core Components

### Fact Table

Stores measurable events.

Examples:

- Sales
- Orders
- Claims
- Transactions

Characteristics:

- Numeric measures
- Foreign keys to dimensions

### Dimension Table

Provides business context.

Examples:

- Customer
- Product
- Store
- Date

Characteristics:

- Descriptive attributes
- Hierarchies
- Filtering and grouping

## Grain Definition

Every fact table must define its grain.

Examples:

- One row per transaction
- One row per order line
- One row per customer visit

Why Grain Matters:

- Determines measurement precision.
- Impacts aggregation behavior.
- Drives reporting consistency.
- Prevents double counting.

## Star Schema

Characteristics:

- Central fact table
- Multiple dimensions

Advantages:

- High performance
- Simple for business users
- Easy semantic layer implementation
- Optimized for reporting

Selection Criteria:

Choose Star Schema when:

- Reporting performance is critical.
- Business simplicity is important.
- Self-service analytics is a priority.
- Data redundancy is acceptable.

Avoid when:

- Dimension normalization is required.
- Storage optimization is the primary goal.

## Snowflake Schema

Characteristics:

- Normalized dimensions

Advantages:

- Reduced redundancy
- Better normalization
- Easier maintenance of large dimensions

Risks:

- Increased query complexity
- Reduced usability for business users

Selection Criteria:

Choose Snowflake Schema when:

- Dimensions contain significant redundancy.
- Governance requires stronger normalization.
- Storage optimization is important.

Avoid when:

- Simplicity for analysts is the priority.
- Query performance is more important than normalization.

## Conformed Dimensions

Dimensions reused across multiple processes.

Examples:

- Customer
- Product
- Calendar

Benefits:

- Consistent reporting
- Shared business definitions
- Enterprise KPI alignment

Selection Criteria:

Implement Conformed Dimensions when:

- Multiple fact tables exist.
- Cross-functional reporting is required.
- Enterprise-wide metrics must remain consistent.

Avoid:

- Duplicating dimensions across domains without governance.
- Introducing multiple definitions for the same business entity.

## Slowly Changing Dimensions

### Type 1

Overwrite values.

Use When:

- Historical tracking is not required.

Examples:

- Correcting spelling mistakes.

### Type 2

Preserve history.

Use When:

- Historical reporting is required.
- Regulatory requirements exist.
- Customer or product history matters.

Examples:

- Customer address history
- Organizational hierarchy changes

### Type 3

Store limited history.

Use When:

- Comparison of current versus previous value is sufficient.

Examples:

- Previous territory assignment
- Previous customer segment

## Best Practices

- Define grain first.
- Build dimensions before facts.
- Use surrogate keys.
- Prefer conformed dimensions.
- Separate business logic from reporting tools.
- Document metric definitions.
- Align dimensions with business glossary terms.

## Common Anti-Patterns

Avoid:

- Facts without a documented grain.
- Duplicate dimensions with different meanings.
- Metrics defined in reports instead of the semantic layer.
- Excessive snowflaking without a clear business justification.
- Using natural keys as primary analytical keys.
- Dimensions without ownership or stewardship.

## Architecture Considerations

Dimensional Modeling is typically used in:

- Data Warehouses
- Lakehouse Gold Layers
- Semantic Layers
- Power BI Semantic Models
- Enterprise Reporting Platforms

Typical Flow:

Source Systems → Integration Layer → Dimensional Model → Semantic Layer → Dashboards & Analytics