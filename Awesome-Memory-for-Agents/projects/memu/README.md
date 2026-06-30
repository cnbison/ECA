# MemU

**收录日期:** 未知

**GitHub:** [https://github.com/NevaMind-AI/memU](https://github.com/NevaMind-AI/memU)
**Website:** [https://memu.pro/](https://memu.pro/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> **Fast retrieval. Higher accuracy. Lower cost.**

## README 摘录（GitHub）

```markdown
![MemU Banner](assets/banner.png)

<div align="center">

# memU

### Personal memory, stored as files

**Fast retrieval. Higher accuracy. Lower cost.**

[![PyPI version](https://badge.fury.io/py/memu-py.svg)](https://badge.fury.io/py/memu-py)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.13+](https://img.shields.io/badge/python-3.13+-blue.svg)](https://www.python.org/downloads/)
[![Discord](https://img.shields.io/badge/Discord-Join%20Chat-5865F2?logo=discord&logoColor=white)](https://discord.com/invite/hQZntfGsbJ)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?logo=x&logoColor=white)](https://x.com/memU_ai)

<a href="https://trendshift.io/repositories/17374" target="_blank"><img src="https://trendshift.io/api/badge/repositories/17374" alt="NevaMind-AI%2FmemU | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

**[English](readme/README_en.md) | [中文](readme/README_zh.md) | [日本語](readme/README_ja.md) | [한국어](readme/README_ko.md) | [Español](readme/README_es.md) | [Français](readme/README_fr.md)**

</div>

---

memU compiles conversations, documents, code, images, audio, video, URLs, and tool traces into human-readable Markdown files (`INDEX.md`, `MEMORY.md`, `SKILL.md`). Agents traverse the tree and load only what the moment needs — instead of rescanning everything or stuffing long histories into every prompt.


```python
await service.memorize(resource_url="workspace/meeting-notes.md", modality="document")

context = await service.retrieve(
    queries=[{"role": "user", "content": {"text": "What should I know about this user's launch preferences?"}}],
    where={"user_id": "123"},
)
```

That's it. Instead of one giant prompt about a person or their workspace, your agent gets three durable layers it can traverse:

```txt
workspace/
├── INDEX.md              ← Index: a map of everything — categories, files, and summaries
├── MEMORY.md             ← Memory: profile, preferences, goals, facts, and key events
└── skill/
    ├── {skill_name}/
    │   └── SKILL.md       ← Skill: a learned tool pattern, workflow, or mistake to avoid
    └── {another_skill}/
        └── SKILL.md
```

- **Index (`INDEX.md`)** — a map of your memories: what exists, where it came from, and where to look first
- **Memory (`MEMORY.md`)** — personal facts, preferences, goals, events, and decisions extracted from source data
- **Skill (`SKILL.md`)** — **auto-extracted from tool traces and refined on every `memorize()`** so the agent improves at recurring tasks

Three things make it different from stuffing everything into the prompt:

- **Fast retrieval** — walk to the right folder and rank the right files instead of scanning everything every time.
- **Higher accuracy** — scope by user, task, or session, and trace every item back to the exact conversation, document, image, or log it came from.
- **Lower cost** — retrieve compact, scoped context instead of reinjecting long histories, documents, logs, and media-derived text into every prompt.
- **Yours to inspect** — a human-readable file tree you can audit, edit, scope, and route through your own storage (`inmemory`, `sqlite`, `postgres`) and LLM providers.


---

## ⭐️ Star the repository

<img width="100%" src="https://github.com/NevaMind-AI/memU/blob/main/assets/star.gif" />

If you find memU useful or interesting, a GitHub Star ⭐️ would be greatly appreciated.

---

## ✨ Core Features

| Capability | Description |
|------------|-------------|
| 🗂️ **Multimodal Ingestion** | Write conversations, documents, images, video, audio, URLs, logs, and local files into memory |
| 📁 **Compiled Memory Workspace** | Persist the Index, Skill, and Memory layers — folders (categories), files (items), source artifacts, links, summaries, and embeddings |
| 🧠 **Typed Memory Extraction** | Extract profile, event, knowledge, behavior, skill, and tool memories from raw sources |
| 🛠️ **Self-Evolving Skills** | Auto-extract reusable tool patterns and workflows from tool traces, then merge and refine them on every `memorize()` instead of relearning |
| 🧭 **Self-Organizing Folders** | Auto-build categories, links, summaries, and embeddings without manual tagging |
| 🤖 **Agent-Ready Retrieval** | Find the right files quickly — scoped, ranked context for any agent workflow |
| 🧱 **Pluggable Storage** | Use in-memory, SQLite, or Postgres backends with the same repository contracts |
| 🔀 **Profile-Based LLM Routing** | Route chat, embedding, vision, and transcription work through configurable LLM profiles |

---

## 🎯 Use Cases

### 1. **Personal Memory**
*Turn chat logs and workspace notes into user preferences, goals, events, decisions, and relationship context.*

```python
await service.memorize(
    resource_url="examples/resources/conversations/conv1.json",
    modality="conversation",
    user={"user_id": "123"},
)

context = await service.retrieve(
    queries=[{"role": "user", "content": {"text": "What should I remember about this user?"}}],
    where={"user_id": "123"},
)
```

### 2. **Workspace Context for Coding Agents**
*Convert docs, PR notes, logs, and design decisions into reusable project memory.*

```python
await service.memorize(resource_url="docs/architecture.md", modality="document")
await service.memorize(resource_url="examples/resources/logs/log1.txt", modality="document")

context = await service.retrieve(
    queries=[{"role": "user", "content": {"text": "How should I structure this module?"}}],
)
```

### 3. **Multimodal Knowledge Layer**
*Extract searchable facts from documents, screenshots, images, videos, and audio notes.*

```python
await service.memorize(resource_url="examples/resources/docs/doc1.txt", modality="document")
# Rich documents (PDF/Word/PowerPoint/Excel/HTML) are converted to Markdown via
# MarkItDown — install the extra with: pip install 'memu-py[document]'
await service.memorize(resource_url="reports/q3-summary.pdf"

... (更多内容请访问上面 GitHub 链接)
```

