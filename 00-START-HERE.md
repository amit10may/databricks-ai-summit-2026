# Databricks Data + AI Summit 2026 — Briefing Pack

**Event:** Data + AI Summit 2026 (DAIS 2026) · Moscone Center, San Francisco · **June 15–18, 2026**
**Compiled:** June 17, 2026 (mid-summit; based on official Databricks newsroom + blog posts dated June 10–16, 2026)
**Audience:** Teams already on Databricks (Spark, MLflow, Genie Spaces, Lakeflow/DLT) who also run off-platform tools like DuckDB + Splink.

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

🍿 **Need a break from release stages?** [`the-scoop-zingers-and-memes.md`](the-scoop-zingers-and-memes.md) has the summit's best flexes, competitor subtweets, and meme-able lines — all sourced.

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

## 🚀 Take this for a spin yourself (with Claude)

This pack is a living "repo," not a one-time report. Here's how to drive it with Claude:

1. **Point Claude at this folder.** Open Cowork with the `databricks/` folder connected and start with: *"Read `dais-2026/00-START-HERE.md` and get oriented."*
2. **Ask it anything about the summit.** e.g. *"What changed for our Lakeflow/DLT pipelines?"* or *"Summarize the Genie announcements for a non-technical exec."* Claude answers from the topic files and cites `03-sources.md`.
3. **Keep it current — the updates angle.** The summit is still running and recap posts/recordings land afterward. When you want fresh content pulled in, just say the magic words:

   > **"Sync the Databricks Summit pack"**

   Claude reads `_SYNC-RUNBOOK.md`, hunts official Databricks sources, dedups against what's already captured, and appends new findings to `UPDATES.md` + the status tracker — **without** clobbering your existing files. Add **"...full rebuild"** to fold those updates into the main topic files, or **"...just status"** to only refresh preview→GA changes.

4. **Check what's moved.** `feature-status.md` is the at-a-glance tracker for which features are GA vs Preview; `UPDATES.md` is the dated changelog of every sync.

Everything is plain Markdown — portable, diff-able, and yours. The runbook is self-contained, so even a brand-new Claude session (no memory of how this was built) can run a sync correctly.

## Folder map

```
dais-2026/
├── 00-START-HERE.md                  ← you are here (orientation + how to drive it with Claude)
├── _SYNC-RUNBOOK.md                  ← how Claude refreshes this pack + the magic words
├── UPDATES.md                        ← append-only changelog of every sync
├── feature-status.md                 ← preview → GA status tracker
├── the-scoop-zingers-and-memes.md    ← 🍿 flexes, competitor subtweets & meme bait (for fun)
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
└── 03-sources.md                     ← link list + the dedup ledger for syncs
```
