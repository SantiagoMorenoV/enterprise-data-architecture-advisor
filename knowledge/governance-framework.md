# Governance Framework

## Governance Principles

- Data is an enterprise asset.
- Data ownership must be explicitly assigned.
- Data quality is a shared responsibility.
- Metadata is mandatory.
- Governance must be embedded into business processes.

---

## Governance Roles

### Data Owner

Accountable for business decisions regarding data.

Responsibilities:

- Approve definitions.
- Approve quality thresholds.
- Approve access requirements.
- Resolve business conflicts.

### Data Steward

Responsible for operational governance and data quality.

Responsibilities:

- Maintain definitions.
- Monitor quality issues.
- Coordinate remediation activities.
- Maintain business glossary terms.

### Data Custodian

Responsible for technical implementation and operational support.

Responsibilities:

- Implement controls.
- Manage platforms.
- Implement security measures.
- Support data lifecycle management.

### Governance Council

Responsible for strategic governance decisions.

Responsibilities:

- Approve policies.
- Define governance standards.
- Prioritize governance initiatives.
- Resolve cross-domain conflicts.

---

## Governance Policies

### Data Quality

Controls:

- Completeness
- Accuracy
- Consistency
- Timeliness
- Validity
- Uniqueness

### Data Security

Controls:

- RBAC
- Least Privilege
- Encryption at Rest
- Encryption in Transit
- Audit Logging

### Data Retention

Controls:

- Retention periods
- Archival processes
- Disposal processes
- Compliance requirements

### Compliance

Examples:

- GDPR
- LGPD
- HIPAA
- Industry-specific regulations

---

## Required Governance Artifacts

Every critical data domain should define:

- Data Owner
- Data Steward
- Source Systems
- System of Record
- Business Glossary Terms
- Quality Rules
- Metadata Standards
- Lineage Requirements

---

## Governance Decision Matrix

| Area | Owner | Steward | Custodian |
|--------|--------|--------|--------|
| Business Definitions | ✅ | ✅ | |
| Data Quality | ✅ | ✅ | ✅ |
| Security Controls | | | ✅ |
| Metadata Management | | ✅ | ✅ |
| Platform Operations | | | ✅ |

---

## Governance Review Checklist

Verify:

- Ownership is defined.
- Stewardship is assigned.
- Quality rules exist.
- Metadata is documented.
- Glossary terms exist.
- Security requirements are documented.
- Compliance requirements are documented.
- Lineage is documented.

---

## Governance Anti-Patterns

Avoid:

- Data without ownership.
- Shared ownership without accountability.
- Missing stewardship.
- Duplicate definitions.
- Undefined quality rules.
- Missing metadata.
- Missing lineage.
- Governance managed only by technology teams.