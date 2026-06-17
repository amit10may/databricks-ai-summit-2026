# MLflow 3 for GenAI

**Relevant to your MLflow usage.** Caveat: the *category-defining* MLflow 3 launch happened at DAIS 2025 and reached GA / further releases through 2026. At DAIS 2026, MLflow shows up mainly as the **observability/eval backbone for agents** (Agent Bricks, Unity AI Gateway, training sessions), rather than a brand-new headline. Treat this as "where MLflow sits in the 2026 agentic stack."

## What MLflow 3 is now
MLflow 3 was rebuilt for Generative AI — an open platform unifying **tracking, evaluation, and observability** for GenAI apps and agents across the dev → production lifecycle.

- **MLflow Tracing** — end-to-end observability: records inputs, outputs, intermediate steps, and metadata for a complete picture of app/agent behavior. Native **agent tracing** + **multi-turn conversation tracking**.
- **Monitor agents deployed anywhere** — including outside Databricks (AWS, GCP, on-prem).
- **Prompt registry** — register, version, test, deploy LLM prompts for agent systems.
- **Evaluation** — built-in eval for GenAI quality.
- **AI Gateway support** — integrates with the Unity AI Gateway governance layer.

## How it connects at DAIS 2026
- **Agent Bricks** uses MLflow's `ResponsesAgent` framework + MLflow tracing for deploying and monitoring agents; agent traces land in the Lakehouse and feed Lakewatch for security/PII analysis.
- **Unity AI Gateway** captures model + MCP activity as governed traces — conceptually the same observability surface, now governed centrally.
- DAIS 2026 training covers MLflow tracing best practices: capture metrics, analyze responses, detect anomalies in production.

## Action items for you
- Standardize **MLflow Tracing** across your agent and GenAI workloads now — it's the common observability layer everything else (Agent Bricks, Gateway, Lakewatch) builds on.
- Adopt the **prompt registry** to version prompts the same way you version models.
- If you deploy models/agents **off-Databricks**, note MLflow 3 can still monitor them — useful for hybrid setups.
- Plan to route MLflow agent traces into Unity Catalog / Lakewatch for governance + debugging.
