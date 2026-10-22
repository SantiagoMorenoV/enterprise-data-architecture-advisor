<div align="center">
  <img src="https://lens.usercontent.google.com/banana?agsi=CmdnbG9iYWw6OjAwMDA1NWNmZWM3MDAyNmQ6MDAwMDAwZWI6MTo4NjVhNjkwODgwYTk0MDJkOjAwMDA1NWNmZWM3MDAyNmQ6MDAwMDAzNjRiYzYwMzM2ODowMDA2NWU2NzYyYjhhZTdmEAIYASIKaW1hZ2UvanBlZw==" alt="Enterprise Data Architecture Advisor" width="800">
  <br>
  <sub><em> Nanobanana generated this immage. That's cool!</em> 🍌</sub>
</div>

# Enterprise Data Architecture Advisor

An advanced AI skill designed to act as a **Principal Enterprise Data Architect**. Based on the principles of DAMA-DMBOK2, TOGAF, and the Zachman Framework, this skill helps conceptualize, design, document, and govern data architectures at an enterprise level.

## What does this Skill do?

- **Architectural Design:** Recommends modern architecture patterns (Data Mesh, Data Fabric, Lakehouse, Data Vault 2.0, Kimball) based on business requirements, governance maturity, and technical constraints.
- **Documentation Generation (Architecture as Code):** Creates standardized documents ready for review:
  * High-Level Design (HLD)
  * Low-Level Design (LLD)
  * Architecture Decision Records (ADR)
- **Visualization:** Generates logical topologies, conceptual diagrams, and integration flows using **Mermaid** syntax.
- **Data Governance & MDM:** Advises on Master Data Management strategies, metadata management, data lineage, and semantic modeling.

## Caveats and Limitations

- **Context Dependency:** The skill is strictly instructed **not to invent** business entities, source systems, or KPIs. If the prompt is vague, the resulting architecture will be generic. It requires explicit business context.
- **Does not replace human judgment:** The design recommendations, trade-offs, and risk assessments generated must always be reviewed and validated by an Architecture Review Board (ARB) or responsible engineers.
- **Cloud Environments:** Although it supports Azure, GCP, and AWS, detailed infrastructure designs (e.g., specific network configurations, precise IAM roles) require validation against your organization's internal security policies.

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
```

### 🤖 How to use this Skill (Gemini, Claude, ChatGPT)

#### For Google Gemini (Native Support)

To install it:

1. Click the green "Code" button at the top right of this repository and select "Download ZIP".
2. Open your Gemini interface and navigate to the Skill Creator or import menu.
3. Upload the downloaded `.zip` file. Gemini will automatically extract and map the `SKILL.md` instructions along with all the auxiliary folders (`/knowledge`, `/templates`, `/examples`).

#### For Claude (Projects)

Claude makes this process incredibly seamless:

1. Create a new Project in Claude.
2. Simply provide the link to this GitHub repository, or connect it directly via Claude's GitHub integration. Claude will ingest the `SKILL.md` instructions and all the contextual folders automatically.
3. Add your customized `business-context.md` file to the project so Claude understands your specific enterprise environment.

#### For ChatGPT Plus (Custom GPTs)

1. **Instructions:** Open the `SKILL.md` file, copy everything from `# ROLE` downwards, and paste it into the "Instructions" box of your Custom GPT.
2. **Knowledge Base:** Download the markdown files inside the `/knowledge`, `/templates`, and `/examples` folders and upload them directly to the GPT's knowledge base.
3. **Context:** Upload your adapted `business-context.md` file.

### 📁 Repository Structure

- `SKILL.md`: Main instructions (system prompt) and AI behavior.
- `/knowledge/`: Business rules, architecture principles, and frameworks (e.g., DAMA, modeling patterns).
- `/templates/`: Markdown templates to ensure outputs (HLDs, ADRs) have a standardized format.
- `/examples/`: Solved use cases to calibrate the AI's behavior.

### ✒️ Credits and Attribution

This skill and its base architecture were created by **Santiago Moreno**.

Feel free to use, fork, or adapt this project for your own developments. The only thing I ask is that you keep the original attribution by linking back to this repository and mentioning the authorship.

### 📄 License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.
