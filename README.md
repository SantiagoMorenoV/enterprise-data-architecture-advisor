# Enterprise Data Architecture Adviso

An advanced AI skill designed to act as a **Principal Enterprise Data Architect**. Based on the principles of DAMA-DMBOK2, TOGAF, and the Zachman Framework, this skill helps conceptualize, design, document, and govern data architectures at an enterprise level.

## What does this Skill do?

* **Architectural Design:** Recommends modern architecture patterns (Data Mesh, Data Fabric, Lakehouse, Data Vault 2.0, Kimball) based on business requirements, governance maturity, and technical constraints.
* **Documentation Generation (Architecture as Code):** Creates standardized documents ready for review:
  * High-Level Design (HLD)
  * Low-Level Design (LLD)
  * Architecture Decision Records (ADR)
* **Visualization:** Generates logical topologies, conceptual diagrams, and integration flows using **Mermaid** syntax.
* **Data Governance & MDM:** Advises on Master Data Management strategies, metadata management, data lineage, and semantic modeling.

## Caveats and Limitations

* **Context Dependency:** The skill is strictly instructed **not to invent** business entities, source systems, or KPIs. If the prompt is vague, the resulting architecture will be generic. It requires explicit business context.
* **Does not replace human judgment:** The design recommendations, trade-offs, and risk assessments generated must always be reviewed and validated by an Architecture Review Board (ARB) or responsible engineers.
* **Cloud Environments:** Although it supports Azure, GCP, and AWS, detailed infrastructure designs (e.g., specific network configurations, precise IAM roles) require validation against your organization's internal security policies.

## How to adapt this Skill to your organization

This skill is completely modular. If you download or copy it, you can (and should) inject your specific business context so the responses align with your real ecosystem. 

To do this, modify or add files within the `/knowledge` directory.

### Base Knowledge Template (`knowledge/business-context.md`)
Create a file with this structure so the skill understands your enterprise environment before designing:

```text
# Enterprise Architecture Context - [Your Company, Organization, or Project Name]

## 1. Technology Profile (Tech Stack)
- Primary Cloud: [e.g., Azure / AWS / GCP / Multi-cloud]
- Core Tools: [e.g., Databricks, Snowflake, Microsoft Fabric, dbt]
- BI Tools: [e.g., Power BI, Tableau]

## 2. Internal Architecture Principles
- [e.g., "We prefer PaaS and SaaS over IaaS"]
- [e.g., "Every design must be event-driven by default"]
- [e.g., "The core analytical model must follow Data Vault 2.0"]

## 3. Main Data Domains
- Domain A: [e.g., Customers / CRM]
- Domain B: [e.g., Logistics and Supply Chain]
- Domain C: [e.g., Finance and ERP]

## 4. Governance and Security Rules
- PII and Sensitive Data: [Masking rules, data residency]
- Naming Conventions: [Naming standards for databases, pipelines, and resources]