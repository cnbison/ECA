# MemoryBear

**收录日期:** 未知

**GitHub:** [https://github.com/SuanmoSuanyangTechnology/MemoryBear](https://github.com/SuanmoSuanyangTechnology/MemoryBear)
**Website:** [https://www.memorybear.ai/](https://www.memorybear.ai/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> **Next-Generation AI Memory Management System · Perceive · Extract · Associate · Forget**

## README 摘录（GitHub）

```markdown
<img width="2346" height="1310" alt="MemoryBear Hero Banner" src="https://github.com/user-attachments/assets/2c0a3f72-1a14-4017-93c8-a7f490d545b6" />

<div align="center">

# MemoryBear — Empowering AI with Human-Like Memory

**Next-Generation AI Memory Management System · Perceive · Extract · Associate · Forget**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.12+-green?logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-teal?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Neo4j](https://img.shields.io/badge/Neo4j-4.4+-blue?logo=neo4j&logoColor=white)](https://neo4j.com/)
[![Gitee Sync](https://img.shields.io/github/actions/workflow/status/SuanmoSuanyangTechnology/MemoryBear/sync-to-gitee.yml?label=Gitee%20Sync&logo=gitee&logoColor=white)](https://github.com/SuanmoSuanyangTechnology/MemoryBear/actions/workflows/sync-to-gitee.yml)

[中文](./README_CN.md) | English

[Quick Start](#quick-start) · [Installation](#installation) · [Core Features](#core-features) · [Architecture](#architecture) · [Benchmarks](#benchmarks) · [Papers](#papers)

</div>

---

## Overview

MemoryBear is a next-generation AI memory system developed by RedBear AI. Its core breakthrough lies in moving beyond the limitations of traditional "static knowledge storage". Inspired by the cognitive mechanisms of biological brains, MemoryBear builds an intelligent knowledge-processing framework that spans the full lifecycle of **perception → extraction → association → forgetting**.

Unlike traditional memory tools that treat knowledge as static data to be retrieved, MemoryBear emulates the hippocampus's memory encoding, the neocortex's knowledge consolidation, and synaptic pruning-based forgetting — enabling knowledge to dynamically evolve with life-like properties. This shifts the relationship between AI and users from **passive lookup** to **proactive cognitive assistance**.

## Papers

| Paper | Description |
|-------|-------------|
| 📄 [Memory Bear AI: A Breakthrough from Memory to Cognition](https://memorybear.ai/pdf/memoryBear) | MemoryBear core technical report |
| 📄 [Memory Bear AI Memory Science Engine for Multimodal Affective Intelligence](https://arxiv.org/abs/2603.22306) | Technical report on multimodal affective intelligence memory engine |
| 📄 [A-MBER: Affective Memory Benchmark for Emotion Recognition](https://arxiv.org/abs/2604.07017) | Affective memory benchmark dataset |

## Why MemoryBear

### Knowledge Forgetting in Single Models

- **Context window limits**: Mainstream LLMs have 8k–32k token windows. In long conversations, early messages are pushed out, causing responses to lose historical context
- **Static knowledge gap**: Training data is a static snapshot — it cannot absorb personalized information (preferences, history) from live interactions
- **Recency bias**: Transformer self-attention weakens on long-range dependencies, overweighting recent input and ignoring earlier critical information

### Memory Gaps in Multi-Agent Collaboration

- **Data silos**: Different agents (consulting, after-sales, recommendation) maintain isolated memories, forcing users to repeat information
- **Inconsistent dialogue state**: When switching agents, user intent and history labels are not fully passed along, causing service discontinuities
- **Decision conflicts**: Agents with partial memory can produce contradictory responses (e.g., recommending products a user is allergic to)

### Semantic Ambiguity in Reasoning

- Domain jargon, colloquial expressions, and context-dependent references are not accurately encoded, leading to semantic drift in memory interpretation
- Cross-language memory associations fail in multilingual or dialect-rich scenarios

<img width="2294" height="1154" alt="Why MemoryBear" src="https://github.com/user-attachments/assets/5e4192d8-ab76-402a-9e80-50d6ede147b9" />

---

## Core Features

<img width="2294" height="1154" alt="MemoryBear Core Features" src="https://github.com/user-attachments/assets/5ae1e2bf-24be-4487-9065-7209f2a57f65" />

### Memory Extraction Engine

Performs **semantic-level parsing** of unstructured conversations and documents to extract:

- **Core declarative information**: Strips redundant modifiers, preserving subject-action-object logic
- **Structured triples**: Automatically extracts entity relationships (e.g., `MemoryBear → core function → knowledge extraction`) as atomic units for graph storage
- **Temporal anchoring**: Automatically extracts and tags timestamps, enabling time-based knowledge tracing
- **Intelligent summarization**: Customizable length (50–500 words) and focus; generates concise summaries of 10-page documents in under 3 seconds

### Graph Storage (Neo4j)

**Graph-first architecture** integrated with Neo4j, overcoming the weak relational modeling of traditional databases:

- Supports millions of entities and tens of millions of relational edges
- Covers 12 core relationship types: hierarchical, causal, temporal, logical, and more
- Extracted triples sync directly to Neo4j, automatically building the initial knowledge graph
- Interactive graph visualization with "machine-generated + human-optimized" collaborative management

### Hybrid Search

**Keyword retrieval + semantic vector retrieval** dual-engine fusion:

- Keyword search powered by Elasticsearch for millisecond-level exact matching of structured information
- Semantic vector search via BERT embeddings, recognizing synonyms, near-synonyms, and implicit intent
- Semantic retrieval expands the candidate space; keyword retrieval then performs precise filtering
- Retrieval accuracy reaches **92%**, improving **35%** over single-mode retrieval

### Memory Forgetting Engine

Inspired by the brain's **synaptic pruning** mechanism, using a dual-dimension model of memory strength and time decay:

- Each knowledge item is assigned an initial memory st

... (更多内容请访问上面 GitHub 链接)
```

