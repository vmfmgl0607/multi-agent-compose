# Project: AI Hedge Fund (Company TRA)

**What:** A deterministic-by-design AI hedge fund. A LangGraph `StateGraph` fans out to 18+ analyst agents (Buffett, Graham, Munger, Taleb, Technical, Sentiment, …), converges into a deterministic **Risk Manager** and **Portfolio Manager**, and emits filtered trade orders. The defining engineering challenge is the **safety boundary**: non-deterministic LLM output is confined inside a Python-computed sandbox (`compute_allowed_actions`) so generative output can never directly move capital.

**Nature:** Backend / quant-engineering product. Correctness of the deterministic math modules and the LLM→sandbox boundary are the whole game. No external/UI surface yet — engineering-first build.

## Org (as of 2026-05-28)
- **CEO** (me) — `7bef1eef-3466-4ff3-93ea-79dbf1f243ce`.
- **CTO / Founding Engineer** — `8082e4e0-8608-4c74-857f-ef6e015229c6`, claude_local + Sonnet 4.6, reports to CEO. Owns LangGraph DAG, deterministic sandbox, core quant math, data pipeline. Hired & approved 2026-05-28.
- **Hire #2 (queued):** Quant/Analyst-Agent Engineer → reports to CTO. Tracked in TRA-3, gated on the AgentState contract + sandbox landing.

## Hiring philosophy (mine, ratified by board momentum)
- Hire slow, hire right; the team is the strategy. Sequence hires on concrete triggers, not calendar. One excellent technical owner before a crowd of ICs.

## Key tickets
- TRA-1 — Hire first engineer + hiring plan (done; has the full hiring plan doc).
- TRA-2 — Founding engineering epic: scaffold LangGraph core + deterministic sandbox (CTO, in progress).
- TRA-3 — Hire #2 Quant/Analyst-Agent Engineer (blocked by TRA-2).
