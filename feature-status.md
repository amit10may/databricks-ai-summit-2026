# 📊 DAIS 2026 — Feature Status Tracker

Tracks release stages so the slow preview→GA changes have a clean home (separate from prose).
Update the **Stage** and **As of** columns on each sync; add rows for new features.
Stages quoted as Databricks stated them — always re-confirm in docs before building.

Legend: GA = Generally Available · PuP = Public Preview · Beta · PrPr = Private Preview

| Feature | Area | Stage (as of 2026-06-17) | As of | Notes / source |
|---|---|---|---|---|
| Unity AI Gateway | Governance | Live / expanding | 2026-06-16 | Govern models/MCPs/tools/agents |
| Contextual Service Policies | Governance | Beta | 2026-06-16 | Govern what an agent can *do* |
| Governance Hub | Governance | PrPr | 2026-06-16 | Steward command center |
| ABAC Grant Policies (models) | Governance | Beta | 2026-06-16 | Expanding to more securables |
| ABAC row-filter / column-mask | Governance | GA | 2026-06-16 | + Governed Tags, Data Classification |
| Identity Attributes | Governance | Preview soon | 2026-06-16 | IdP-synced attributes |
| Context Attributes | Governance | Preview soon | 2026-06-16 | Agent/app/workspace context |
| Tag propagation | Governance | PrPr (now) | 2026-06-16 | Source→downstream tags |
| Role-Based Access Control (RBAC) | Governance | PuP coming soon | 2026-06-16 | Groups-as-roles |
| Cross-cloud/region addressability | Governance | Live | 2026-06-16 | 4-level namespace |
| Managed Disaster Recovery | Platform | Live (Mission Critical add-on) | 2026-06-16 | Region failover in minutes |
| UC Domains | Context | PuP | 2026-06-16 | Business-aligned asset grouping |
| UC Glossary | Context | Preview soon | 2026-06-16 | Authoritative terms |
| UC Metrics — Materialization | Context | PuP | 2026-06-16 | Faster metric queries |
| UC Metrics — import from PBI/Tableau | Context | Beta | 2026-06-16 | |
| External Lineage | Context | GA | 2026-06-16 | Non-Databricks assets |
| Genie Ontology | Genie | Live | 2026-06-16 | 84.5% internal benchmark |
| Genie One | Genie | Live | 2026-06-16 | Slack/Teams/mobile/MCP |
| Genie Agents (from Genie Spaces) | Genie | Live | 2026-06-16 | Autonomous, shareable |
| Iceberg v3 / Managed Iceberg | Open formats | GA | 2026-06-16 | |
| External access to managed Delta tables | Open formats | PuP | 2026-06-16 | Spark/Flink write; check DuckDB |
| Multimodal FILE type | Open formats | Beta | 2026-06-16 | PDFs/images/audio/video |
| Geospatial types (Delta + Iceberg v3) | Open formats | GA | 2026-06-16 | |
| OpenSharing | Open sharing | Open protocol (Linux Foundation) | 2026-06-10 | Successor to Delta Sharing |
| Document Intelligence (`ai_parse_document` etc.) | Agent Bricks | GA | 2026-06-16 | SQL doc parsing |
| Agent Bricks (agent platform) | Agent dev | Expanding | 2026-06-16 | Any model/harness |
| Omnigent (meta-harness) | Agent dev | Open source + managed | 2026-06-16 | |
| Lakebase (serverless Postgres) | Operational DB | GA | early 2026 | Postgres 17, branching |
| MLflow 3 for GenAI | ML/GenAI | GA | 2026 | Tracing, eval, prompt registry |
| Lakeflow Spark Declarative Pipelines | Data eng | Evolving (SDP in Apache Spark) | 2026-06 | DLT successor; OSS standard |
| Lakeflow Designer | Data eng | PuP (confirm current) | 2026-06 | Visual/NL pipeline authoring |

> ⬜ = stage to watch. Next sync: re-check anything marked "soon", "Beta", "PuP", or "PrPr" for GA flips.
