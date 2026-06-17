# Agent Bricks & the AI Stack (incl. Lakebase)

Source: "Agent Bricks: Data + AI Summit 2026" (Databricks Blog, June 16, 2026). Since the 2025 launch: **100k+ agents built**, **1+ quadrillion tokens/year** processed; customers incl. AstraZeneca, 7-Eleven, Fox, Block.

## The thesis: the missing 99%
The core agent loop is ~1% of the work; the other **99%** is hidden technical debt — token capacity, deployment, security, evaluation, monitoring, context, sharing. Agent Bricks becomes a **developer agent platform** that handles that infrastructure. Built on three pillars: **Choice, Context, Control**.

## Choice — models & harnesses
- **Models:** all frontier proprietary + open-source models in one platform, inside Databricks' security boundary. Added **Kimi**; existing OpenAI, Anthropic, Gemini, Qwen. New **partnership with SpaceX** to make **Grok** models natively available.
- **Custom models:** prompt optimization, fine-tuning, RL via **AI Runtime** (serverless NVIDIA GPUs). A Databricks custom RL data agent is competitive with Opus/Sonnet on Genie tasks at much lower cost/query. Customers: Merck, First American.
- **Harnesses:** any framework — LangGraph, Agno, CrewAI, Claude Code SDK, OpenAI Agent SDK. Deploy to **Databricks Apps** with horizontal autoscaling. Managed version of open-source meta-harness **Omnigent** to orchestrate across harnesses.

## Context — grounding agents
- **MCP support in Unity Catalog** — agents securely connect to Google Drive, Jira, Slack, GitHub, etc.
- **Genie Ontology** — continuously-learned business context (see `03-genie.md`).
- **Databricks Agent Tools** — built-in, governed (in UC) tools; document-search subagent now **3× faster** at higher quality.
- **Agent memory service** — managed memory **powered by Lakebase**; agents persist context/session history across sessions (and eventually across agents).
- **Document Intelligence (GA)** — SQL functions `ai_parse_document`, `ai_extract`, `ai_classify` for SOTA PDF/document parsing & analysis.
- **Databricks Sandbox** — secure VMs with downscoped UC access for code interpreters, subagents, harnesses, safe experimentation.

## Control — governance
- **Unity AI Gateway** (see `02-unity-catalog-governance.md`): catalog of all agents/models/MCPs/skills, fine-grained access control, per-user/group budgets, intelligent routing.
- **Agent Traces & Monitoring** — reasoning traces/memory/generations governed in the Lakehouse (not a separate vendor); integrated with **Lakewatch** for PII alerts, audit, incident response.
- **Contextual Policies** — stateful, context-aware security policies for tools/agents in SQL (Python soon). Example: if an agent touches PII, block publishing to a public site but allow emailing a coworker; Salesforce updates require human approval.
- **UC Registry for agents/tools/models** — govern AI assets alongside data; one control plane.

## Lakebase (operational Postgres) — context
Source: "Databricks Lakebase is now Generally Available" + Lakebase launch press releases.
- **Serverless Postgres**, **GA earlier in 2026**; separates compute/storage; auto-scales; **instant data branching** for safe dev/test.
- **Postgres 17** support (and 16), incl. **pgvector** for AI search.
- Built for **AI agents' operational state** (low-latency transactional read/write), not just historical queries. Adoption growing **2× faster** than the data-warehousing product; thousands of production customers. Framed under Databricks' **LTAP** ("Lake Transactional/Analytical Processing") architecture.
- **Powers Agent Bricks' agent memory service.**

## Action items for you
- If you build agents, evaluate **Agent Bricks** to avoid hand-building the "99%" infra; start with **Document Intelligence** functions (easy SQL win for your document workflows).
- Consider **Lakebase** where agents/apps need transactional state or vector search alongside lakehouse data.
- Use **Omnigent** if you're juggling multiple agent frameworks.
