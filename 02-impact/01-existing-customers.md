# What DAIS 2026 Means for Existing Databricks Customers

Written for an existing Databricks customer heavily using **Spark, MLflow, Genie Spaces, Lakeflow/DLT pipelines**, who also runs **DuckDB + Splink** off-platform.

## Bottom line
Almost nothing here is disruptive. It's **additive and upgrade-shaped** — most items make tools you already run better. The two things that actually require *decisions* are (1) adopting the agent-governance layer (Unity AI Gateway) before agents proliferate, and (2) curating semantics/ontology to unlock the accuracy gains.

## By the tools you already use

### Genie Spaces → Genie Agents (do this first)
- Your curated Spaces are the on-ramp; they become **autonomous, action-taking, shareable agents** that also reason over unstructured data.
- **Genie Ontology** is a large accuracy lever (84.5% vs 52.4% on Databricks' internal benchmark) — but it rewards curated Glossary/Domains/Metrics.
- New surfaces: Slack, Teams, iOS/Android, MCP. Good way to expand Genie beyond analysts.

### Lakeflow / DLT
- **Rename to watch:** DLT is now **Lakeflow (Spark) Declarative Pipelines**. Update runbooks/IaC/docs; behavior is compatible.
- The engine is now an **open Apache Spark standard (SDP)** → less lock-in, portable patterns.
- New **streaming-table flow syntax** and **Lakeflow Designer** (visual/NL authoring) let analysts self-serve simpler pipelines.
- **Lakeflow Connect auto-captures lineage** into Unity Catalog.

### Spark
- **Spark 4.0** + Declarative Pipelines in OSS. Your Spark skills/code get a cleaner declarative path and an open standard.

### MLflow
- **MLflow 3 for GenAI** is the observability/eval backbone of the agentic stack: adopt **Tracing** + **prompt registry** now; it integrates with Unity AI Gateway and Lakewatch. Works for off-Databricks deployments too.

## Cross-cutting decisions for existing customers

1. **Adopt Unity AI Gateway early.** As soon as agents (Genie Agents, Agent Bricks, MCP tools) appear in your estate, you want one governed control plane for access, cost caps, routing, and tracing. Retrofitting governance later is painful.
2. **Invest in semantics/context.** Glossary + Domains + Metrics in Unity Catalog feed Genie Ontology and every agent. This is the highest-ROI prep work.
3. **Mind release stages.** Many marquee items are **Beta / Public Preview / Private Preview**. Pilot, don't bet production on previews; re-check docs for current stage.
4. **New cost surface.** Agents + tokens are a new spend category. Use Gateway **hard spend caps** and budgets from day one.
5. **Watch for new add-ons/SKUs.** E.g., **Mission Critical add-on** (Managed DR + Enhanced Security/Compliance). Budget impact if you need DR.
6. **Governance got stronger for free-ish.** ABAC GA (row/column), Governed Tags, Data Classification, External Lineage GA, cross-cloud addressability — worth a governance review to adopt.

## Risks / things to verify
- **Preview ≠ GA:** confirm stage before committing.
- **Rename churn:** DLT→Lakeflow, AI/BI Genie→Genie One/Agents — internal docs and onboarding need updating.
- **Region/cloud:** new features roll out unevenly across AWS/Azure/GCP — check your region's release notes.
