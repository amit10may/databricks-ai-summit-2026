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
