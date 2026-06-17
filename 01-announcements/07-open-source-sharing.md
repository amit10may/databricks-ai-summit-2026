# Open Source, Open Formats & Open Sharing

The "Choice / no lock-in" pillar. **Highly relevant to your off-platform tools (DuckDB, Splink)** — see `02-impact/04-interop-duckdb-splink.md`.

## OpenSharing (Linux Foundation)
- Announced **June 10, 2026** (newsroom press release); jointly with the Linux Foundation.
- **Next evolution of Delta Sharing** — now a vendor-neutral **Linux Foundation project**.
- First open protocol for securely sharing **AI assets**: **agent skills, ML models, and unstructured data** — across orgs and platforms **without copying files** or relying on proprietary marketplaces.
- Delta Sharing context: pioneered 5 years ago, now the most widely-adopted open zero-copy data-sharing protocol, used by thousands of enterprises.

## Apache Spark Declarative Pipelines
Databricks' core declarative ETL framework donated to **Apache Spark** as **Spark Declarative Pipelines**, on the back of **Spark 4.0** and **2B+ downloads**. (Details in `04-lakeflow-spark.md`.)

## Open table formats — Delta + Iceberg
- **Apache Iceberg v3 — GA**; **Managed Iceberg — GA**; new federation connectors; cross-engine ABAC.
- **External access to managed Delta tables — Public Preview:** external engines (Spark, Flink, and others) can **create and write** Unity Catalog managed Delta tables — not just read.
- **Multimodal FILE type — Beta:** managed Delta + Iceberg tables natively govern unstructured data (PDFs, images, audio, video).
- **Geospatial types in Delta + Iceberg v3 — GA.**
- Unity Catalog positioned as the most comprehensive, open catalog across the Delta Lake + Iceberg ecosystems.

## Open semantics & metrics
- **Metrics** in Unity Catalog are **open source** (in Apache Spark + Unity Catalog OSS) and **Open Semantic Interchange (OSI)-ready** — KPI definitions aren't locked to Databricks.

## Sharing & collaboration ecosystem
- **SecureConnect** — first-of-its-kind secure cross-cloud connectivity with zero-copy sharing.
- **Global Distribution** — automated replication across clouds/regions.
- **Genie Sharing** — cross-org collaboration on Genie Agents.
- **3rd-party apps on Databricks Marketplace.**

## Why this matters strategically
Databricks is doubling down on **openness as a competitive wedge** vs more closed stacks: open formats (Delta + Iceberg), open pipelines (SDP in Spark), open semantics (OSI), open sharing (OpenSharing). For a multi-tool shop like yours, this lowers the cost of keeping DuckDB/Splink/etc. in the mix while still governing everything through Unity Catalog.
