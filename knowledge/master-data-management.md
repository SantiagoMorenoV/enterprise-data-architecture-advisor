# Master Data Management (MDM)

## Purpose

MDM creates a trusted and governed source for critical business entities.

## Selection Criteria

Implement MDM when:

- Multiple systems manage the same business entities.
- Customer, Product, Supplier, Employee or Location data is duplicated across systems.
- Inconsistent business definitions exist.
- Enterprise reporting requires standardized dimensions.
- Regulatory compliance requires trusted master records.
- A Golden Record is required.
- Multiple business units consume the same master data.

Prefer MDM when:

- Data quality issues are affecting business operations.
- Customer, Product or Supplier data is fragmented.
- Cross-functional reporting requires consistent master data.
- Data ownership can be assigned and governed.

Avoid implementing MDM when:

- Only one authoritative system exists.
- Business ownership is undefined.
- Governance capabilities are absent.
- The cost of implementation outweighs the business value.
- Master data challenges are isolated and do not impact multiple processes.

Business Commitment Required: Very High

Governance Maturity Required: High

Complexity: High

Organizational Impact: High

## Typical Domains

- Customer
- Product
- Supplier
- Employee
- Location
- Asset

## Core Concepts

### Master Data

Shared business entities used across multiple systems.

### Golden Record

The most trusted representation of a business entity.

Characteristics:

- Unified
- Governed
- Trusted
- Business-approved

### Survivorship Rules

Rules determining which source wins when conflicts occur.

Examples:

- CRM email overrides ERP email.
- Most recently updated address takes precedence.
- Source priority hierarchy determines final value.

### Matching Rules

Rules used to detect duplicates.

Examples:

- Exact Match
- Fuzzy Match
- Probabilistic Match
- Hybrid Match

## MDM Styles

### Registry

Maintains references to source records.

Best For:

- Low complexity environments
- Initial MDM implementations
- Minimal operational impact

### Consolidation

Creates a centralized trusted view.

Best For:

- Enterprise reporting
- Data quality initiatives
- Golden Record creation

### Coexistence

Synchronizes data across systems.

Best For:

- Distributed operational environments
- Shared ownership models

### Transactional

Acts as the primary source of truth.

Best For:

- Enterprise-wide master data control
- Mature governance environments

## Governance Requirements

Define:

- Data Owner
- Data Steward
- Matching Rules
- Survivorship Rules
- Quality Rules

Additional Governance Elements:

- Master Data Policies
- Data Standards
- Metadata Requirements
- Audit Requirements
- Access Controls

## Data Quality Controls

- Completeness
- Accuracy
- Uniqueness
- Consistency
- Timeliness

Additional Controls:

- Validity
- Referential Integrity
- Duplicate Detection
- Standardization Rules

## Architecture Considerations

Every MDM implementation should define:

- System of Record
- System of Reference
- Golden Record Strategy
- Matching Strategy
- Survivorship Strategy
- Stewardship Model
- Integration Model
- Governance Operating Model

## Success Criteria

- Clear ownership
- Approved business definitions
- Stable golden records
- Measurable quality improvements
- Reduced duplicates
- Consistent reporting across systems
- Improved trust in enterprise data

## Risks

- Business ownership conflicts
- Poor stewardship
- Unclear golden record definitions
- Weak governance processes
- Organizational resistance
- Undefined decision rights
- Lack of executive sponsorship

## Common Anti-Patterns

Avoid:

- Implementing MDM without governance.
- Implementing MDM without ownership.
- Creating Golden Records without business approval.
- Defining matching rules without stewardship involvement.
- Treating MDM as only a technology project.
- Ignoring data quality controls.
- Maintaining multiple competing Golden Records.

## MDM Readiness Checklist

Before implementing MDM verify:

- Business ownership exists.
- Stewardship has been assigned.
- Critical domains are identified.
- Data quality issues are documented.
- Governance processes exist.
- Executive sponsorship exists.
- Success metrics are defined.
- Integration requirements are understood.