# Databricks Data + AI Summit 2026 — Briefing Pack

**The agentic era, distilled.**  
A curated, source-backed guide to what Databricks announced at DAIS 2026 — organized so you can skim the headlines, dive deep on what matters to your stack, or trace every claim back to official docs.

> **Event:** Data + AI Summit 2026 · Moscone Center, San Francisco · **June 15–18, 2026**  
> **Compiled:** June 17, 2026 (mid-summit) · **Sources:** [official Databricks newsroom, blogs & docs only](03-sources.md)

---

## 🚀 Drive this with Claude — and keep it fresh

This isn't a static report. It's a small repo you **run with Claude**: ask it questions, and
refresh it with new announcements as the summit and its recap posts keep rolling out.

**Ask it anything** — point Claude at this folder and try:
> *"Read `dais-2026/00-START-HERE.md` and get oriented."*
> *"What changed for our Lakeflow/DLT pipelines?"*
> *"Summarize the Genie announcements for a non-technical exec."*

**Keep it current — just say the magic words** ✨

> ### 🔄 "Sync the Databricks Summit pack"

Claude reads [`_SYNC-RUNBOOK.md`](_SYNC-RUNBOOK.md), hunts official Databricks sources, dedups
against what's already captured, and appends new findings to [`UPDATES.md`](UPDATES.md) +
[`feature-status.md`](feature-status.md) — **without** clobbering your existing files.

| Say this | And Claude will |
|---|---|
| **"Sync the Databricks Summit pack"** | Find new official content, append to the changelog (safe, additive) |
| *…add* **"full rebuild"** | Also fold updates into the main topic files |
| *…add* **"just status"** | Only refresh the preview→GA status tracker |
| *…add* **"since June 18"** | Only look for content after that date |

Then check **[`UPDATES.md`](UPDATES.md)** (dated changelog) and **[`feature-status.md`](feature-status.md)**
(GA vs Preview at a glance) to see what moved. The runbook is self-contained, so even a brand-new
Claude session can run a sync correctly.

---

## Why this repo exists

DAIS 2026 wasn't a scattershot product dump. It had a spine:

> **Agents are now first-class actors on enterprise data** — and Databricks rebuilt the platform so they get **Choice** (any model, format, cloud), **Context** (governed business meaning), and **Control** (governance over what agents *do*, not just what they access).

This pack turns 800+ sessions and a week of announcements into something you can actually use: **what shipped, what stage it's in, and what it means** — whether you're an existing Spark/MLflow/Genie shop, evaluating Databricks for the first time, or wiring DuckDB and Splink into a governed lakehouse.

No hype. No third-party hot takes as gospel. Every note ties back to [documented sources](03-sources.md).

---

## Start here

| If you want to… | Go to |
|---|---|
| **Get oriented in 5 minutes** | [00-START-HERE.md](00-START-HERE.md) |
| **See the marquee launches at a glance** | [01-headline-launches.md](01-announcements/01-headline-launches.md) |
| **Understand the event themes & keynotes** | [00-overview.md](01-announcements/00-overview.md) |
| **Verify links & release stages** | [03-sources.md](03-sources.md) |
| **Have some fun — flexes, subtweets & memes** 🍿 | [the-scoop-zingers-and-memes.md](the-scoop-zingers-and-memes.md) |

---

## The three themes that organize everything

Databricks framed the whole summit around governing and building for **agents**. These three lenses show up in Unity Catalog, Agent Bricks, and Genie alike:

| Theme | What it means | Where to read more |
|---|---|---|
| **Control** | Govern what agents *do*, not just what they can access | [Unity Catalog & AI Gateway](01-announcements/02-unity-catalog-governance.md) |
| **Context** | Give agents governed business meaning so they stop guessing | [Genie One, Agents & Ontology](01-announcements/03-genie.md) |
| **Choice** | No lock-in on model, format, cloud, or region | [Open formats & OpenSharing](01-announcements/07-open-source-sharing.md) |

---

## What's inside

```
dais-2026/
├── README.md                         ← you are here (overview + how to drive it with Claude)
├── 00-START-HERE.md                  ← your entry point for the content
├── _SYNC-RUNBOOK.md                  ← how Claude refreshes the pack + the magic words
├── UPDATES.md                        ← append-only changelog of every sync
├── feature-status.md                 ← preview → GA status tracker
├── the-scoop-zingers-and-memes.md    ← 🍿 the fun file: flexes, subtweets, meme bait
├── 01-announcements/
│   ├── 00-overview.md                ← event facts, keynotes, themes
│   ├── 01-headline-launches.md       ← marquee items at a glance
│   ├── 02-unity-catalog-governance.md
│   ├── 03-genie.md                   ← Genie One / Agents / Ontology
│   ├── 04-lakeflow-spark.md          ← DLT → Lakeflow + Spark Declarative Pipelines
│   ├── 05-mlflow.md                  ← MLflow 3 for GenAI
│   ├── 06-agent-bricks-ai.md         ← Agent Bricks, models, Lakebase memory
│   └── 07-open-source-sharing.md     ← Iceberg v3, OpenSharing, open formats
├── 02-impact/
│   ├── 01-existing-customers.md      ← additive upgrades for current users
│   ├── 02-new-customers.md           ← what to evaluate first
│   └── 04-interop-duckdb-splink.md   ← off-platform tools + governed tables
└── 03-sources.md                     ← every link + the dedup ledger for syncs
```

---

## Headline launches (the 30-second version)

| Area | Launch | Why it matters |
|---|---|---|
| AI Governance | **Unity AI Gateway** | One runtime layer to govern every model, MCP, tool, and agent |
| Business AI | **Genie One & Genie Agents** | Genie Spaces evolve into shareable, autonomous, action-taking agents |
| Context | **Genie Ontology** | Auto-learned context graph — big accuracy jump on governed semantics |
| Agent dev | **Agent Bricks** | Full agent platform: any model, governed memory, sandboxes |
| Open formats | **Iceberg v3 GA** + external write to managed Delta | Deepest open interop; external engines can read *and write* UC tables |
| Open sharing | **OpenSharing** → Linux Foundation | Vendor-neutral sharing of AI assets without copy or lock-in |
| Data eng | **Spark Declarative Pipelines** | DLT becomes an open Apache Spark standard + AI-native authoring |
| ML/GenAI | **MLflow 3 for GenAI** | Tracing, eval, and observability for agents — even off Databricks |

Full table with release stages (GA / Preview / Beta): [headline launches](01-announcements/01-headline-launches.md)

---

## Pick your reading path

### Already on Databricks (Spark, MLflow, Genie, Lakeflow)

You're in luck — almost nothing here is disruptive. It's **additive and upgrade-shaped**. Start with:

1. [Genie → Genie Agents](01-announcements/03-genie.md) — your Spaces are the on-ramp
2. [Lakeflow / Spark Declarative Pipelines](01-announcements/04-lakeflow-spark.md) — the future of your DLT pipelines
3. [MLflow 3 for GenAI](01-announcements/05-mlflow.md) — tracing & eval for agents
4. [Impact for existing customers](02-impact/01-existing-customers.md) — decisions worth making now

### Evaluating Databricks for the first time

Focus on the platform bet, not the buzzwords:

1. [Event overview & themes](01-announcements/00-overview.md)
2. [Unity Catalog + AI Gateway](01-announcements/02-unity-catalog-governance.md)
3. [Agent Bricks](01-announcements/06-agent-bricks-ai.md)
4. [Impact for new customers](02-impact/02-new-customers.md)

### Running DuckDB, Splink, or other engines off-platform

The open-format story is the bridge:

1. [Open formats & OpenSharing](01-announcements/07-open-source-sharing.md)
2. [DuckDB / Splink interop analysis](02-impact/04-interop-duckdb-splink.md)

---

## A note on scope & freshness

- **Official sources only** — databricks.com newsroom, blog, and docs. Third-party links in [03-sources.md](03-sources.md) are context, not authority.
- **2026 content** — where a feature launched earlier and was only *re-stated* at DAIS 2026, that's flagged in the notes.
- **Release stages move fast** — GA, Public Preview, Beta, and Private Preview are quoted as Databricks stated them in mid-June 2026. **Re-confirm in docs before you build.**

---

## Official sources (live)

| What | Where |
|---|---|
| Keynote livestream & replays | [databricks.com/dataaisummit](https://www.databricks.com/dataaisummit) |
| Product announcement blogs | [databricks.com/blog](https://www.databricks.com/blog) |
| Feature status & how-to | [docs.databricks.com](https://docs.databricks.com) release notes |
| Session catalog (800+ breakouts) | [Summit agenda](https://www.databricks.com/dataaisummit/agenda) |

Full annotated link list: **[03-sources.md](03-sources.md)**

---

## Contributing

This is a personal briefing pack, not an official Databricks resource. If you spot a stale release stage or a broken link, open an issue or PR — especially on [03-sources.md](03-sources.md).

---

*Built for people who missed the keynotes, sat through them and forgot half of it, or need to explain DAIS 2026 to their team on Monday morning.*
