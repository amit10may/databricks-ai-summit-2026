# Genie One, Genie Agents & Genie Ontology

Source: "Introducing Genie One, Genie Agents, and Genie Ontology" (Databricks Blog, June 16, 2026). **Most directly relevant to you — you already run Genie Spaces.**

## The headline for you: Genie Spaces → Genie Agents
Databricks reports customers have created **1M+ Genie Spaces** (curated, governed, topic-scoped chat experiences with verified logic and benchmarks). At DAIS 2026, **Genie Spaces is evolving into Genie Agents**:

- **Take autonomous action** — same toolset as Genie One: MCP connections, scheduled tasks, document/artifact generation, and **writes to external systems** — completing multi-step workflows without oversight.
- **Reason over unstructured data, not just tables/views** — grounded in documents, files, and knowledge sources alongside structured data.
- **Created from a single prompt** — spin up a Genie Agent in Genie One or Genie Code, scope it, benchmark it, share it for teammates to use/customize. Turns domain expertise into reusable "coworkers."

> Net: your existing curated Genie Spaces are the on-ramp. They don't go away — they become more capable (actions + unstructured data + sharing). Expect to revisit benchmarks/verified logic as you promote Spaces to Agents.

## Genie One — the data-smart AI coworker
The next step beyond conversational analytics in AI/BI:

- **Across all apps & data** — native connectors + **Lakehouse Federation** + **Lakeflow Connect** + two-way integrations (Gmail, Slack, Teams) to extract insight and orchestrate actions.
- **Full cowork capabilities** — schedules, alerts, monitoring, document creation, custom skills, custom MCP support. (E.g., daily customer-meeting brief from calendar + email + Lakehouse; auto-update a business review doc from inventory + meeting transcripts.)
- **Everywhere work happens** — embedded in **Slack** and **Microsoft Teams** (@mention Genie in channels/threads, governed per-user permissions); new **iOS and Android apps**; and a **Genie MCP App** so existing/3rd-party agents can use Genie without changing workflows.

## Genie Ontology — the accuracy engine
An **automatic context layer**: continuously extracts knowledge snippets from tables, queries, dashboards, pipelines, and connected apps, and organizes them into a living graph of how the company works and what data actually means (metric definitions, business terms, unique calcs, relationships).

- **Authority via PageRank-style weighting** — weighs source, author authority, usage frequency, ties to certified/widely-used assets, and freshness; answers from highest-weight sources. Enforces source permissions (shows only what you're allowed to see) — solving context **without** hand-curation or a separate permissions system.
- **Benchmark (internal, June 2026, 28-question real-world suite):** Genie answered **84.5%** correctly on first attempt vs **52.4%** for the strongest general-purpose coding agent (weakest 25%), and ~**2× faster** than the strongest coding agent.
- Fed by Unity Catalog Semantics (Glossary/Domains/Metrics) + signals like Column-level Popularity.

## Governed & secure by design
Permissions enforced on every answer via source-native ACLs or Unity Catalog; MCP, tools, and costs governed by **Unity AI Gateway**; full admin governance suite for org-wide rollout.

## Action items for you
- Inventory your current Genie Spaces; identify the 3–5 highest-value ones to promote to **Genie Agents** (where autonomous actions/writes add value).
- Stand up **Genie Ontology** by curating Glossary/Domains/Metrics in Unity Catalog — this is the single biggest accuracy lever.
- Pilot Genie in **Slack/Teams** for a business team to test the "AI coworker" pattern.
- Confirm Unity AI Gateway governs Genie's MCP/tool/cost usage before broad rollout.
