# Interop: Your Off-Platform Tools (DuckDB + Splink)

You run **DuckDB** and **Splink** (entity resolution) *outside* Databricks. There were **no DAIS 2026 announcements naming DuckDB or Splink** (none expected — they're third-party OSS). But several 2026 announcements **directly improve how these tools interoperate** with your governed Databricks estate. This section is **analysis/inference**, clearly labeled, built on the official open-format announcements.

## The interop-relevant announcements
1. **External access to managed Delta tables — Public Preview:** external engines (Spark, Flink, "and others") can now **create and write** Unity Catalog-managed Delta tables, not just read.
2. **Iceberg v3 GA + Managed Iceberg GA** + new federation connectors + cross-engine ABAC.
3. **Multimodal FILE type (Beta)** in managed Delta/Iceberg.
4. **OpenSharing** (Linux Foundation) — vendor-neutral sharing of data + AI assets, zero-copy.
5. **Open Metrics / OSI-ready semantics.**

## What this means for DuckDB
DuckDB reads Delta and Iceberg via its `delta`/`iceberg` extensions and can talk to catalogs.
- **Read path (solid today):** DuckDB can query your governed Delta/Iceberg tables; Iceberg v3 GA + UC's open Iceberg REST catalog support make DuckDB a clean lightweight local/edge query engine over the *same* tables Databricks manages.
- **Write path (improving):** "External access to managed Delta tables (PuP)" is the direction of travel for letting non-Databricks engines write managed tables. Verify whether DuckDB specifically is supported in your region/version — the announcement names Spark and Flink explicitly; DuckDB support depends on its Delta/UC connector maturity, so **test before relying on it**.
- **Governance:** by pointing DuckDB at Unity Catalog (vs raw files), you inherit lineage and (increasingly) ABAC/policy enforcement instead of ungoverned file access.
- **Pattern:** keep DuckDB for fast local/ad-hoc/embedded analytics; treat UC-governed Delta/Iceberg as the shared source of truth so DuckDB and Databricks see consistent data.

## What this means for Splink (entity resolution)
Splink runs ER on a backend (DuckDB, Spark, or Athena). It's not a Databricks product, so nothing was announced — but:
- **Splink-on-Spark already runs inside Databricks.** If you want governed ER, you can run Splink with the **Spark backend on Databricks** so inputs/outputs are UC-governed Delta tables (lineage, ABAC, sharing all apply).
- **Splink-on-DuckDB off-platform** can read the same governed tables (see DuckDB read path above) and write results back to a landing zone that Lakeflow ingests — keeping the lakehouse as the system of record.
- **Geospatial types (GA)** may help if any of your ER blocking/matching uses location.
- **Consider where ER belongs long-term:** Databricks is pushing AI-native matching (e.g., `ai_*` SQL functions, custom models, agentic search). Worth a periodic evaluation of Splink vs Databricks-native approaches — but no need to migrate; Splink remains a strong, transparent, probabilistic ER tool.

## Recommended interop architecture (suggestion)
- **System of record:** Unity Catalog-governed Delta/Iceberg tables.
- **Heavy/streaming pipelines:** Lakeflow (Spark) Declarative Pipelines.
- **Entity resolution:** Splink — on **Spark backend in Databricks** for governed/production ER; on **DuckDB** for local/dev or cost-sensitive batch, reading governed tables and writing back via a Lakeflow-ingested zone.
- **Ad-hoc / local analytics:** DuckDB over the same Delta/Iceberg tables.
- **Governance:** route any agent/model use of these outputs through **Unity AI Gateway**; track lineage end-to-end via **External Lineage (GA)**.

## To verify before relying on it
- Whether your DuckDB version + Delta/UC connector supports **writing** managed Delta tables (the PuP feature explicitly lists Spark/Flink).
- Current UC Iceberg REST catalog auth/config for DuckDB in your cloud/region.
- Whether external-engine writes honor ABAC/row-column policies (governance parity is the goal but confirm current behavior in docs).
