# Unity Catalog & Governance (incl. Unity AI Gateway)

Source: "What's new with Unity Catalog at Data + AI Summit 2026" + "AI governance at Data + AI Summit 2026: What's new with Unity AI Gateway" (Databricks Blog, June 16, 2026). 14,000+ orgs now govern on Unity Catalog.

Databricks organizes the UC story as **Control, Context, Choice**.

## Control — govern what agents *do*

### Unity AI Gateway
The governance solution for enterprise AI, built on Unity Catalog. Extends governance beyond data/AI *assets* to the runtime *interactions* between models, agents, MCPs, skills, and tools.

- **Govern every AI asset in one place** — register and govern Databricks-hosted and external models, MCP services, agents, and skills with the same access controls, discovery, lineage, and auditing you use for data. Databricks ships foundation model services plus managed MCP services for Google Drive, Jira, Slack, GitHub.
- **Enforce what AI can do at runtime** — **Contextual Service Policies (Beta)** extend governance from "who can access" to "what it can do in this interaction." Admins allow / deny / require-approval for actions (e.g., write to a sensitive folder, push code). Built-in guardrails for PII exposure, prompt injection, unsafe content. Policies are written in SQL (Python coming) and can hold state / react to context.
- **Control AI spend across providers** — Gateway budgets now cover external providers incl. bring-your-own-key. **Hard spend caps stop requests** when a budget is hit (not just alert after the fact). Smart routing balances quality vs cost.
- **Monitor & investigate** — unified agent tracing captures model + MCP activity in one governed telemetry layer; traces analyzable in **Lakewatch** (lakehouse-native SIEM).

### Governance Hub (Private Preview)
Centralized command center for stewards/admins: monitor posture, identify risks, prioritize remediation, scale governance across data, AI, cost, and performance.

### Access control upgrades
- **ABAC Grant Policies — Beta for models:** define attribute-based access once → auto-grant EXECUTE across all matching models; expanding to MCP services, agents, tables, volumes. (Builds on the recent **GA of ABAC row-filtering/column-masking + Governed Tags + Data Classification**.)
- **Identity Attributes (Preview soon):** rules from live IdP properties (department, region, clearance).
- **Context Attributes (Preview soon):** rules based on whether access comes from an agent, app, or workspace.
- **Tag propagation (Private Preview now):** governed tags carry automatically from source columns to downstream tables/views.
- **Role-Based Access Control / RBAC (Public Preview soon):** groups behaving like roles; users *assume* a role and are authorized as that role. Enables exclusive-access / data-isolation use cases (clinical trials, country-specific data, privileged debugging). Switch roles in UI or via OAuth flow.

## Context — open, adaptive enterprise meaning

**Unity Catalog Semantics** = one shared source of meaning for humans and agents; defined once, accessible via SQL/APIs/MCPs.

- **Glossary (preview soon):** authoritative concepts, terms, taxonomies (or import existing). Genie Code drafts/refines pages and flags definition drift; team curates collaboratively.
- **Domains (Public Preview):** organize data + AI assets into business-aligned categories so agents get scoped, relevant context (not the whole catalog). Internal marketplace with certification/stewardship signals; AI-driven domain suggestions coming.
- **Metrics:** define KPIs once as governed objects, query from SQL/BI/APIs/agents. New: multi-fact relationships (PuP in Dashboards), level-of-detail calcs, parameterized metrics, window measures; agentic + UI authoring; **Materialization (Public Preview)** for faster queries; **import from Power BI / Tableau (Beta)**. Open-source, in Apache Spark + Unity Catalog OSS, Open Semantic Interchange (OSI)-ready.
- **External lineage (GA):** lineage extends to non-Databricks assets (upstream sources, downstream BI). Lakeflow Connect ingestion auto-records source→destination lineage.
- **Table Insights — Column-level Popularity:** see which columns are most-queried; feeds Genie Ontology.

This user-defined semantic layer feeds the **Genie Ontology** (see `03-genie.md`).

## Choice — open infrastructure, no lock-in

- **Cross-cloud, cross-region addressability:** UC now spans accounts, regions, clouds. New **four-level namespace** `metastore.catalog.schema.table` gives every asset one address across the estate → unified discovery, one policy set, one audit trail, column-level lineage end-to-end. Run workloads wherever GPUs/capacity/data proximity dictate; governance stays consistent.
- **Managed Disaster Recovery:** replicate critical deployment parts to a secondary region, fail over in minutes. Requires the new **Mission Critical add-on** (also unlocks Enhanced Security & Compliance).
- **Cross-format / cross-platform interop:** Iceberg v3 **GA**, Managed Iceberg **GA**, new federation connectors, cross-engine ABAC. Plus at DAIS:
  - **External access to managed Delta tables (Public Preview):** external engines like Spark and Flink can **create and write** UC-managed Delta tables.
  - **Multimodal data in open formats (Beta):** new **FILE type** governs PDFs/images/audio/video natively in managed Delta + Iceberg.
  - **Geospatial types in Delta + Iceberg v3 (GA).**
- **Open sharing:** **OpenSharing** (next evolution of Delta Sharing) — now a Linux Foundation project; first open, vendor-neutral protocol for sharing AI assets (Agent Skills, models, unstructured data). Plus **SecureConnect** (cross-cloud zero-copy connectivity), **Global Distribution** (auto replication across clouds/regions), **Genie Sharing** (cross-org collaboration on Genie Agents), and **3rd-party apps on Databricks Marketplace**.

## Why it's the foundation
Everything else at the summit (Agent Bricks, Genie, agent memory, MLflow tracing) plugs into Unity Catalog + Unity AI Gateway. AI governance is being deliberately fused with data governance: one control plane, one audit trail.
