# Databricks Data + AI Summit 2026 — Briefing Pack

**Event:** Data + AI Summit 2026 (DAIS 2026) · Moscone Center, San Francisco · **June 15–18, 2026**
**Compiled:** June 17, 2026 (mid-summit; based on official Databricks newsroom + blog posts dated June 10–16, 2026)
**Audience:** VCreaTek — existing Databricks customer (Spark, MLflow, Genie Spaces, Lakeflow/DLT) also running DuckDB + Splink off-platform.

> Scope note: This pack sticks to **official Databricks sources only** (databricks.com newsroom, blog, docs) and to **2026** content. Where a feature launched earlier and was only *re-stated* at DAIS 2026, that is flagged. Release stages (GA / Public Preview / Beta / Private Preview) are quoted as Databricks stated them — these change fast, so re-confirm in docs before you build.

---

## The one-paragraph version

DAIS 2026 is an **"agentic era"** summit. The throughline across every announcement is the same: agents are now first-class actors on enterprise data, and Databricks is rebuilding its platform so those agents have **choice** (any model/format/cloud), **context** (governed business meaning), and **control** (governance over what agents *do*, not just what they access). The flagship launches are **Unity AI Gateway** (govern every model, MCP, tool, and agent), **Agent Bricks as a full developer agent platform**, **Genie One / Genie Agents / Genie Ontology** (Genie Spaces evolves into autonomous agents), and a wave of **open-format + open-sharing** moves (Iceberg v3 GA, external write access to managed Delta tables, **OpenSharing** donated to the Linux Foundation). For an existing Spark/MLflow/Genie/Lakeflow shop, almost none of this is disruptive — it's additive, and several items directly upgrade tools you already run.

---

## What to catch up on first (priority order for your stack)

1. **Genie One / Genie Agents / Genie Ontology** — your Genie Spaces are being promoted into shareable autonomous agents; Ontology is a big accuracy upgrade. → `01-announcements/03-genie.md`
2. **Lakeflow / Spark Declarative Pipelines** — the future of your DLT pipelines; now an open Apache Spark standard + AI-native authoring. → `01-announcements/04-lakeflow-spark.md`
3. **MLflow 3 for GenAI** — tracing/observability/eval for agents, works even off-Databricks. → `01-announcements/05-mlflow.md`
4. **Unity Catalog + Unity AI Gateway** — the governance layer everything else plugs into; also the key to DuckDB/Splink interop. → `01-announcements/02-unity-catalog-governance.md`
5. **Open formats & OpenSharing** — how DuckDB/Splink read and write the same governed tables. → `01-announcements/07-open-source-sharing.md` and `02-impact/04-interop-duckdb-splink.md`

---

## Where to get the source content (official)

| What | Where |
|---|---|
| Keynote livestream + replays | databricks.com/dataaisummit (Virtual Experience) |
| Product announcement blogs | databricks.com/blog (category: Announcements / Platform) |
| Keynote lineup & programming | Newsroom press release, June 15, 2026 |
| Feature status & how-to | docs.databricks.com release notes (AWS/Azure/GCP, 2026) |
| Session catalog (800+ breakouts) | databricks.com/dataaisummit/agenda |

Full link list: `03-sources.md`

---

## Folder map

```
dais-2026/
├── 00-START-HERE.md                  ← you are here
├── 01-announcements/
│   ├── 00-overview.md                ← event facts, keynotes, themes
│   ├── 01-headline-launches.md       ← the marquee items at a glance
│   ├── 02-unity-catalog-governance.md
│   ├── 03-genie.md                   ← Genie One / Agents / Ontology
│   ├── 04-lakeflow-spark.md          ← DLT → Lakeflow + Spark Declarative Pipelines
│   ├── 05-mlflow.md                  ← MLflow 3 for GenAI
│   ├── 06-agent-bricks-ai.md         ← Agent Bricks platform, models, Lakebase memory
│   └── 07-open-source-sharing.md     ← Iceberg v3, OpenSharing, open formats
├── 02-impact/
│   ├── 01-existing-customers.md
│   ├── 02-new-customers.md
│   └── 04-interop-duckdb-splink.md   ← your off-platform tools
└── 03-sources.md
```
