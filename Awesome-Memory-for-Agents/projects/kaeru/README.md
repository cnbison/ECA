# kaeru

**收录日期:** 2026-06

**GitHub:** [https://github.com/LamantinAI/kaeru](https://github.com/LamantinAI/kaeru)
**Website:** [https://github.com/LamantinAI/kaeru](https://github.com/LamantinAI/kaeru)

## 简述

Local-first cognitive memory for any LLM agent over MCP: a bi-temporal typed knowledge graph (CozoDB / RocksDB) giving cross-session and multi-agent continuity via episodes, provenance chains, and consolidated outcomes — a single Rust binary, with an optional shared cloud tier for teams.

## GitHub README 摘要

> `kaeru` is a **cross-agent cognitive engine** for LLM agents — a typed graph that agents think in, plus a recollection layer for long-term ideas and outcomes. Local-first for each agent, with an optional shared cloud tier so a whole team of agents and people build on one another's memory.

## README 摘录（GitHub）

```markdown
# 蛙 kaeru

`kaeru` is a **cross-agent cognitive engine** for LLM agents — a typed graph that agents think in, plus a recollection layer for long-term ideas and outcomes. Local-first for each agent, with an optional shared cloud tier so a whole team of agents and people build on one another's memory.

Designed for **multi-session, multi-agent continuity**: when an agent opens a project, it has full context of what was being thought about, can follow provenance chains, can consolidate outcomes into stable long-term knowledge, and can pull in what the rest of the team has shared.

Inspired by the LLM-wiki pattern (Karpathy, gist `442a6bf555914893e9891c11519de94f`), the bi-temporal knowledge graph approach of Graphiti / Zep, the curator-driven knowledge engine of Cognee, and the reasoning-based hierarchical-summary navigation pattern from PageIndex. Two-tier design grounded in the hippocampus / cortex split.

Name: 蛙 (*kaeru*, "frog"; homophonic with 帰る "to return" and 変える "to change") — the agent that returns, recalls, and reshapes.

![A kaeru vault rendered as a live knowledge galaxy by kaeru-viz](kaeru-viz/galaxy.gif)

<sub>A kaeru vault rendered by [`kaeru-viz`](kaeru-viz/) — one cluster per initiative, nodes sized by memory layer, with reasoning-chain replay and a time-lapse of how the knowledge grew.</sub>

## Overview

![A kaeru vault rendered as a knowledge galaxy by kaeru-viz](kaeru-viz/screenshot.png)

`kaeru` is built around a typed property graph stored in CozoDB. Two tiers, biological analogy:

- **cognitive (operational / hippocampus)** — high-velocity working graph where the agent actively thinks: episodes, scratch, drafts, hypotheses, experiments, audit events.
- **recollection (archival / cortex)** — settled ideas, outcomes, summaries, references; mostly read.

Every node and edge is **bi-temporal** — the substrate stores assertion / retraction history natively, so time-travel queries are out of the box and conflict resolution is non-destructive (the old version is invalidated, not deleted).

Per-initiative subgraphs through a junction-relation pattern: one substrate, many initiatives, multi-membership. An agent working on project A asks "what was I doing here last time?" and gets an answer scoped to A. The same node can belong to several initiatives at once.

`kaeru` is a **facilitator, not an enforcer**. The curator API exposes ~40 primitives (`awake`, `recall`, `drill`, `claim`, `synthesise`, `at`, `history`, `consolidate_out`, …) as available tools. The agent and user choose when to invoke them; the daemon hints but doesn't block.

## Features

- **Two-tier graph** — operational (cognitive / hippocampus) for active thinking; archival (recollection / cortex) for settled knowledge. `consolidate_out` promotes across the boundary, preserving provenance.
- **Bi-temporal** — native assertion / retraction history. `at` reads a node in full as it is now or as-of any past moment; conflicts are non-destructive (the old version is invalidated, not deleted).
- **Per-initiative scoping + layered re-entry** — one substrate, many projects. `awake` restores a project's working context by memory layer (Core → Hot → Warm); `surface` reaches the archived Cold / Frozen on demand.
- **Cross-agent sharing** — local-first by default; an optional `kaeru-cloud` tier lets a trusted team share settled knowledge through two safety gates (initiative policy + a deterministic secret guard). See [Local & cloud](#local--cloud--sharing-memory-across-a-team).
- **Structural recall** — exact name lookup, typed `walk` / `drill` / `trace`, `between`, FTS fuzzy fallback. Vectors are not the primary mode.
- **Initiative management** — `rename` / `delete` an initiative, locally or team-wide.
- **Markdown export** — Obsidian-friendly snapshot of any initiative.

## Architecture Notes

- **Substrate is CozoDB** with RocksDB backend; bi-temporal `Validity` is native to the substrate, not bolted on.
- **Edges carry operational semantics** — each edge type is something the curator API responds to. `derived_from` powers provenance and explainability; `contradicts` triggers a non-destructive `under_review` flow; `supersedes` retracts the previous version through the bi-temporal substrate. Edges are not just associations.
- **`audit_event` is a first-class node type** — every mutation writes an audit node, so changes to memory themselves become reasoning surface for the agent. Substrate-level history (`Validity`) and operational audit (audit-event nodes) stay separate: the substrate tracks *what was*, the audit nodes track *who did it and why*.
- **Per-initiative scope through junction relations** rather than column filtering — RocksDB prefix-scan gives O(log n + k) on the active initiative.
- **Retrieval is structural-first** — explicit name lookup, typed graph traversal, summary views. Cozo FTS for fuzzy fallback when an exact name is forgotten. Vector embeddings are not the primary mode.
- **Two-tier with explicit `consolidate_out`** — operational drafts get promoted to archival as a deliberate, logged operation. Provenance (`derived_from`) survives the tier boundary.
- **Single binary, embedded substrate** — `kaeru` runs in-process with the agent. No server, no network. Vault on disk under a platform-specific default (Linux `$XDG_DATA_HOME/kaeru`, macOS `~/Library/Application Support/ai.lamantin.kaeru`, Windows `%LOCALAPPDATA%\ai.lamantin.kaeru`); override with `KAERU_VAULT_PATH`.

## Layout

```
kaeru/
├── Cargo.toml                  ← workspace root
├── kaeru-core/                 ← library: substrate, schema, primitives
├── kaeru-mcp/                  ← binary `kaeru-mcp`: Model Context Protocol server (the agent's surface)
├── kaeru-cloud/                ← binary `kaeru-cloud`: shared cloud tier (Axum REST over kaeru-core)
├── kaeru-rig/                  ← library: `rig` Tools that give a rig agent kaeru memory
└── skills/
    └── kaeru-skill/            ← portable agent skill (Claude Code / etc.)
```

`kaeru-r

... (更多内容请访问上面 GitHub 链接)
```

