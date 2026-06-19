# 📝 DAIS 2026 Pack — Update Log (append-only)

How this works: each sync appends a new dated section at the **top** (newest first). New findings
land here first; they're only folded into the main topic files on a "full rebuild" sync. See
`_SYNC-RUNBOOK.md` for the procedure and trigger phrase.

---

## ENTRY TEMPLATE — copy this for each new sync

```
## YYYY-MM-DD — sync run
**Sources checked:** <blog index, newsroom, release notes pages...>
**New official URLs found:** <count> (added to 03-sources.md)

### 🆕 New announcements
- **<Title>** (<stage>, pub <date>) — <what it is + why it matters for Spark/MLflow/Genie/Lakeflow/DuckDB/Splink>. → would update `01-announcements/<file>.md`. Source: <url>

### 🔁 Stage changes (preview → GA, etc.)
- **<Feature>**: <old stage> → <new stage> (as of <date>). → feature-status.md updated. Source: <url>

### 🎤 New sessions / recordings
- **<Talk title>** — <speaker/topic>, <link>.

### ⚠️ Corrections (conflicts with existing pack content — flagged, not silently overwritten)
- <what the pack currently says> vs <new official info>. Recommend: <merge/keep/verify>.

### Summary
<3–5 lines: what changed this run.>
```

---

## 2026-06-19 — sync run
**Sources checked:** databricks.com/blog (Announcements/Platform, newest), newsroom, Lakeflow + AI/BI + platform 2026 release notes, Tech Times Day-2 recap. Summit concluded June 18.
**New official URLs found:** 5 (added to `03-sources.md`).

### 🆕 New announcements
- **Lakeflow: "A new era of agentic data engineering"** (pub Jun 16) — the dedicated Lakeflow keynote blog (fills a baseline gap). Highlights for your stack: **Real-Time Mode (RTM) for Spark Declarative Pipelines — Public Preview** (end-to-end latency as low as **5 ms**, no separate Flink engine, on classic + serverless); **SDP declarative APIs (Append, Auto CDC, Replace Where, Materialized View) now in Databricks SQL (GA)**, coming to serverless Notebooks + Lakeflow Designer; **Genie Code** deeply embedded across Lakeflow authoring; **Lakeflow Connect now 100+ managed connectors** (+ Free Tier: 100 DBUs/day) and **query-based CDC capture (GA)**; **Zerobus Ingest** Kafka-free ingestion (Kafka-compatible APIs Beta, gRPC/REST GA); **Lakeflow Jobs** with 50+ integrations + External Orchestration (can trigger Snowflake jobs, REST, Slack, PagerDuty), data-readiness triggers. → updates `01-announcements/04-lakeflow-spark.md`. Source: https://www.databricks.com/blog/lakeflow-new-era-agentic-data-engineering
- **Genie ZeroOps** (announced Jun 16) — background AI agent that monitors data/AI assets, does root-cause analysis from UC quality metrics/logs/lineage, proposes fixes validated in a sandbox, applied human-in-the-loop. → relevant to your Lakeflow/DLT ops. Source: (linked in Lakeflow blog) https://www.databricks.com/blog/introducing-genie-zeroops
- **What's New in the AI Platform: Agents for ML Engineering, Deep Learning, Real-Time ML** (pub Jun 17) — **fills the MLflow gap.** **Genie Code for ML** (coding agent across the full ML lifecycle, logs every run to **MLflow**, registers to UC, deploys to serving); **AI Runtime — Public Preview** (serverless A10/H100 GPUs, now multinode, MLflow + UC governed); **Real-Time ML**: Declarative Feature Engineering, Streaming Features, **High-QPS Model Serving (300K+ QPS at <10 ms p99)**, Online Feature Serving on Lakebase, Genie ZeroOps for ML. → updates `01-announcements/05-mlflow.md`. Source: https://www.databricks.com/blog/whats-new-ai-platform-agents-ml-engineering-our-deep-learning-platform-and-new-capabilities
- **Platform security & compliance** (DAIS 2026) — **Context-Based Ingress (CBI)**: zero-trust access policies to safely expose Genie, dashboards, Apps, and AI Gateway endpoints to external users. → relevant to governance rollout. Source: https://www.databricks.com/blog/whats-new-databricks-platform-security-and-compliance-data-ai-summit-2026
- **2026 Databricks Global Partner Awards** (65+ awards). Low priority for your stack. Source: https://www.databricks.com/blog/databricks-announces-2026-global-partner-awards

### 🔁 Stage changes (preview → GA, etc.)
- **Lakeflow Designer**: Public Preview → **GA** (as of Jun 16). Every visual Flow runs on a production Spark Declarative Pipeline. → `feature-status.md` updated.
- **RTM for Spark Declarative Pipelines**: new → **Public Preview**. Added to tracker.
- **SDP declarative APIs in Databricks SQL**: → **GA**. Added.
- **AI Runtime**: (March preview) → **Public Preview** w/ multinode training. Added.
- **Databricks Runtime 19 / DBR 19 ML**: **Beta**, ships **Apache Spark 4.2.0** (per June 2026 release notes). Added — relevant to your Spark workloads.

### ⚠️ Corrections (vs existing pack)
- `04-lakeflow-spark.md` hedged "Lakeflow Designer (PuP — confirm current)." **Now confirmed GA.** Fold on next full rebuild.
- Baseline `05-mlflow.md` said MLflow had "no brand-new headline" at DAIS 2026. Partially superseded: MLflow is the backbone of the new **Genie Code for ML** + **AI Runtime** announcements (still not a standalone MLflow release, but more prominent than baseline implied).

### Summary
Post-summit posts landed the two big stack-relevant pieces we were missing: the **Lakeflow** keynote blog (Real-Time Mode for SDP, Designer GA, 100+ connectors, Zerobus, Genie ZeroOps) and the **AI/ML Platform** blog (Genie Code for ML on top of MLflow, AI Runtime GPUs, high-QPS serving). Net for you: your DLT/Spark and MLflow workflows both got concrete upgrades. Still pending: verbatim keynote quotes / recordings for the scoop, and any further GA flips. Recommend a **"full rebuild"** sync to fold these into `04-lakeflow-spark.md` and `05-mlflow.md`.

---

## 2026-06-17 — baseline (initial pack created)
**Sources checked:** newsroom keynote press release; blogs for Unity Catalog, Unity AI Gateway,
Agent Bricks, Genie One/Agents/Ontology, Lakeflow/Spark Declarative Pipelines, Lakebase, MLflow;
Lakeflow + AI/BI 2026 release notes; product pages.
**New official URLs found:** see `03-sources.md` (all baseline sources).

### Summary
Initial briefing pack built mid-summit (event runs June 15–18). Captured the marquee launches:
Unity AI Gateway, Agent Bricks (full agent platform), Genie One / Genie Agents / Genie Ontology,
Lakeflow + Spark Declarative Pipelines, MLflow 3 for GenAI, Lakebase GA, Iceberg v3 GA,
OpenSharing (Linux Foundation). Days 17–18 of the summit and post-summit recap blogs + session
recordings are **not yet captured** — those are the priority for the next sync.

### Known gaps to chase next sync
- Day 3–4 keynote/announcement blogs (June 17–18).
- Post-summit "everything announced" recap post (usually lands the week after).
- Session recordings + detailed talk content on the agenda page.
- Any preview→GA stage flips on Lakeflow, Genie, MLflow, Unity Catalog.
- Explicit DuckDB/Splink interop confirmations (currently inference-based in 02-impact/04).
