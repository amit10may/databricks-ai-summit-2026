# Lakeflow & Apache Spark — the future of your DLT pipelines

**Most relevant to your Spark + DLT workloads.** Two intertwined storylines: (1) DLT has been rebranded and folded into **Lakeflow**; (2) the underlying declarative ETL engine was **open-sourced into Apache Spark** as **Spark Declarative Pipelines (SDP)**.

## Naming: DLT → Lakeflow (Spark) Declarative Pipelines
What you know as **DLT (Delta Live Tables)** is now **Lakeflow Declarative Pipelines / Lakeflow Spark Declarative Pipelines (SDP)** — a declarative framework for batch + streaming pipelines in SQL and Python. Core concepts: **pipelines, flows, streaming tables, materialized views, sinks**, with automatic orchestration and incremental updates. Lakeflow is the umbrella covering:
- **Lakeflow Connect** — managed ingestion connectors (now auto-record source→destination lineage into Unity Catalog).
- **Lakeflow (Spark) Declarative Pipelines** — the DLT successor.
- **Lakeflow Jobs** — orchestration.
- **Lakeflow Designer** — visual/AI-native authoring (below).

## Open-sourced into Apache Spark (the strategic move)
Databricks donated its core declarative ETL framework to the Apache Spark open-source project as **Spark Declarative Pipelines**, riding on **Apache Spark 4.0** and Spark passing **2 billion downloads**. SDP defines pipelines for batch + streaming ETL across any Spark-supported source (cloud storage, message buses, change feeds, external systems) — you declare *what* the pipeline should do and Spark figures out *how*.

**Why it matters:** your declarative pipeline skills/code are now portable to an open standard — less lock-in, broader community, and the same model usable outside Databricks-managed pipelines.

## 2026 authoring & feature updates
- **Lakeflow Designer** — visual, no-code, AI-native experience: design/edit/automate pipelines via **drag-and-drop canvas + natural-language prompts**, aimed at analysts and less-technical users while producing real Lakeflow pipelines under the hood. (Announced Public Preview in 2025; continued updates through 2026 — confirm current stage in docs.)
- **New flow syntax for streaming tables** (2026 release notes) — more direct, declarative way to define streaming pipelines; simplifies authoring and aligns with current patterns.
- Ongoing feature/quality improvements shipped across 2026 releases (see Lakeflow SDP release notes for AWS/Azure/GCP).

## Action items for you
- Track the **DLT → Lakeflow** rename in your runbooks/IaC; behavior is compatible but names/docs have moved.
- Evaluate **Lakeflow Designer** to let analysts self-serve simpler pipelines (offloads your engineers).
- Adopt the **new streaming-table flow syntax** for new streaming pipelines.
- Note that **Lakeflow Connect now auto-captures lineage** into Unity Catalog — useful for your governance/External Lineage story.
- Strategic: because SDP is now in Apache Spark, you can standardize pipeline *patterns* on an open API and reduce platform lock-in for portable workloads.
