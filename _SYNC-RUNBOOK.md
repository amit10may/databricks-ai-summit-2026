# 🔄 DAIS 2026 Pack — Sync Runbook

This file tells any Claude session how to refresh this briefing pack with new official
Databricks content from Data + AI Summit 2026. It is self-contained: a fresh session with
no memory of the original work can follow it.

---

## ✨ MAGIC WORDS (say any of these to trigger a sync)

> **"Sync the Databricks Summit pack"**

Also accepted (all mean the same thing):
- "Run the DAIS 2026 sync"
- "Update the Databricks summit pack"
- "Sync DAIS"

Optional modifiers you can add:
- `...full rebuild` → also fold the changelog into the main files (heavier; see Step 6).
- `...just status` → only refresh `feature-status.md` (preview→GA changes), skip new-blog hunt.
- `...since <date>` → only look for content published after that date.

---

## 📂 What this pack is

Location: `dais-2026/` (this folder).
- `00-START-HERE.md` — index / exec summary
- `01-announcements/` — 8 topic files (overview, headline launches, UC, Genie, Lakeflow, MLflow, Agent Bricks, open source)
- `02-impact/` — existing customers, new customers, DuckDB+Splink interop
- `03-sources.md` — **the ledger of already-processed URLs** (dedup source of truth)
- `feature-status.md` — preview→GA tracking table
- `UPDATES.md` — **append-only changelog; new findings land here first**
- `_SYNC-RUNBOOK.md` — this file

User context (keep tailoring to this): existing Databricks customer using **Spark, MLflow,
Genie Spaces, Lakeflow/DLT pipelines**; also runs **DuckDB + Splink** (entity resolution) off-platform.

---

## ✅ Scope rules (non-negotiable)

1. **Official Databricks sources only**: databricks.com (newsroom, blog, product pages) and
   docs.databricks.com. Third-party (analysts, news, aggregators) may be read for *leads* but
   never quoted as fact and never merged into the pack.
2. **2026 / DAIS 2026 only.** Ignore older summit content unless it's needed as context and
   clearly labeled as such.
3. **Dedup against the ledger.** Before adding anything, check `03-sources.md`. If the URL is
   already listed, skip it. Only act on genuinely new official posts.
4. **Append, don't rewrite** (default mode). New material goes into `UPDATES.md` as a dated
   entry. Do NOT silently rewrite the 8 topic files on a normal sync.
5. **Flag contradictions, don't overwrite.** If new info conflicts with existing pack content,
   note it explicitly in `UPDATES.md` under a "⚠️ Corrections" subhead rather than quietly editing.
6. **Stages change** — always record the stage (GA/Public Preview/Beta/Private Preview) exactly
   as stated, with the date observed.

---

## 🪜 The procedure

### Step 1 — Read state
Read `03-sources.md` (processed URLs), `feature-status.md`, and the latest entry in `UPDATES.md`
to learn what's already covered and when the last sync ran.

### Step 2 — Hunt for new official content
Search + fetch from official sources. Good queries / pages to check each run:
- `site:databricks.com/blog "Data + AI Summit 2026"` (and `dais-2026`)
- databricks.com/blog (Announcements / Platform categories) — newest posts
- databricks.com/company/newsroom — press releases
- Product release notes (2026) for the user's stack:
  - Lakeflow Spark Declarative Pipelines: docs.databricks.com/aws/en/release-notes/dlt/2026
  - AI/BI & Genie: docs.databricks.com/aws/en/ai-bi/release-notes/2026
  - Platform release notes 2026 (monthly pages)
  - MLflow 3 / GenAI docs
- Session catalog: databricks.com/dataaisummit/agenda (for new talk details / recordings)

Compare every candidate URL against the ledger; keep only new ones.

### Step 3 — Extract what matters
For each new official item, pull: title, URL, publish date, the concrete announcement(s),
release stage, and **why it matters for this user's stack** (Spark / MLflow / Genie / Lakeflow,
plus DuckDB/Splink interop). Keep it tight and factual.

### Step 4 — Write to UPDATES.md (append-only)
Add one dated section per sync. Use the template at the top of `UPDATES.md`. Group by:
new announcements, stage changes, new sessions/recordings, ⚠️ corrections. Cross-reference which
topic file each item *would eventually* update (e.g., "→ 01-announcements/03-genie.md").

### Step 5 — Update the ledger + status table
- Append every newly-processed URL to `03-sources.md` (so the next sync dedups correctly).
- Update `feature-status.md` rows whose stage changed; add new rows for new features.

### Step 6 — (Only on "full rebuild") Fold changelog into main files
Merge accumulated `UPDATES.md` entries into the relevant topic + impact files, then mark those
changelog entries as "folded in (date)". Re-run a light verification pass. Do this sparingly —
at natural checkpoints (e.g., end of summit, or once a month), not every sync.

### Step 7 — Verify before finishing
- Re-confirm dates/stages against the official page (don't trust headlines).
- Watch for known traps: DLT↔Lakeflow renames, AI/BI Genie↔Genie One/Agents renames, and
  date errors (event is **June 15–18, 2026**; reject sources saying otherwise).
- End with a 3–5 line summary of what changed this run, and present `UPDATES.md`.

---

## 🧭 Quick rules of thumb
- When unsure whether something is "new": if its URL isn't in `03-sources.md`, it's new.
- When unsure whether to merge vs append: **append**. Merging is opt-in via "full rebuild".
- When unsure if a source is trustworthy: if it isn't on databricks.com / docs.databricks.com,
  it's a lead, not a fact.
