# Headline Launches — At a Glance

The marquee DAIS 2026 announcements, with release stage as stated by Databricks. **Re-verify stages in docs before building** — they move quickly.

| Area | Launch | Stage (as announced) | One-line significance |
|---|---|---|---|
| AI Governance | **Unity AI Gateway** | Live / expanding | One runtime governance layer for every model, MCP, tool, agent — on or off Databricks. |
| AI Governance | **Contextual Service Policies** | Beta | Govern what an agent can *do* in a given interaction (allow/deny/require-approval), with built-in PII / prompt-injection guardrails. |
| AI Governance | **Governance Hub** | Private Preview | Single command center for data stewards across data, AI, cost, performance. |
| Governance | **ABAC Grant Policies (models)** | Beta | Attribute-based EXECUTE grants across all matching models; more securables coming. |
| Governance | **Role-Based Access Control (RBAC)** | Public Preview (soon) | Groups-as-roles for data isolation / privileged tasks. |
| Governance | **Cross-cloud, cross-region addressability** | Live | Four-level namespace `metastore.catalog.schema.table` — one address, one policy set, one audit trail across your whole estate. |
| Governance | **Managed Disaster Recovery** | Live (Mission Critical add-on) | Replicate + fail over a deployment to a secondary region in minutes. |
| Context | **Unity Catalog Semantics: Glossary, Domains, Metrics** | Mixed (Domains PuP; Glossary preview soon; Metrics materialization PuP) | Governed business meaning agents and BI tools share. |
| Context | **Genie Ontology** | Live | Auto-learned context graph; 84.5% first-attempt accuracy on internal benchmark vs 52.4% for strongest coding agent. |
| Business AI | **Genie One** | Live | Genie becomes a "data-smart AI coworker" across Slack/Teams/mobile/MCP with actions, schedules, doc creation. |
| Business AI | **Genie Agents** | Live | Genie Spaces evolve into shareable, autonomous, multi-step agents over structured + unstructured data. |
| Agent dev | **Agent Bricks → full agent platform** | Expanding | Any model, any harness, governed memory (Lakebase), sandboxes, Document Intelligence (GA). |
| Agent dev | **Omnigent** (open-source meta-harness) | Open source + managed | Orchestrate across LangGraph/CrewAI/Claude Code SDK/OpenAI Agent SDK. |
| Open formats | **Iceberg v3 GA, Managed Iceberg GA** | GA | Deepest open Delta + Iceberg interop in the market. |
| Open formats | **External access to managed Delta tables** | Public Preview | External engines (Spark, Flink, …) can **create and write** UC-managed Delta tables. |
| Open formats | **Multimodal FILE type** | Beta | Govern PDFs/images/audio/video natively in managed Delta + Iceberg. |
| Open formats | **Geospatial types (Delta + Iceberg v3)** | GA | Native geo for routing, fleet, geofencing. |
| Open sharing | **OpenSharing** (donated to Linux Foundation, June 10) | Open protocol | Vendor-neutral sharing of AI assets (agent skills, models, unstructured data) — no copy, no proprietary marketplace. |
| Data eng | **Lakeflow / Spark Declarative Pipelines** | Evolving (SDP open-sourced into Apache Spark) | Your DLT framework is now an open Apache Spark standard + AI-native authoring (Lakeflow Designer). |
| Operational DB | **Lakebase** (serverless Postgres) | GA (earlier in 2026) | Postgres 17, instant branching; powers agent memory; adoption growing 2× faster than the DW product. |
| ML/GenAI | **MLflow 3 for GenAI** | GA (2026) | Tracing, eval, observability, prompt registry for agents deployed anywhere. |
| Security | **Lakewatch** | — | Lakehouse-native SIEM; ingests Unity AI Gateway agent traces for PII/audit/incident response. |

> **Newest categories worth a mention:** Lakewatch (open agentic SIEM), CustomerLake (agentic CDP embedded in Databricks), and LTAP ("Lake Transactional/Analytical Processing") as the architecture story behind Lakebase.
