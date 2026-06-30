# OpenMemory

**收录日期:** 未知

**GitHub:** [https://github.com/CaviraOSS/OpenMemory](https://github.com/CaviraOSS/OpenMemory)
**Website:** [https://openmemory.cavira.app/](https://openmemory.cavira.app/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> Expect breaking changes and potential bugs.

## README 摘录（GitHub）

```markdown
# 🚧 This project is currently being rewritten.

Expect breaking changes and potential bugs.
### Contributers needed
To contribute, visit https://github.com/CaviraOSS/OpenMemory/tree/rewrite branch.
If you find an issue, please open a GitHub issue with details so it can be tracked and resolved.
## OpenMemory

> **Real long-term memory for AI agents. Not RAG. Not a vector DB. Self-hosted, Python + Node.**

[![VS Code Extension](https://img.shields.io/badge/VS%20Code-Extension-007ACC?logo=visualstudiocode)](https://marketplace.visualstudio.com/items?itemName=Nullure.openmemory-vscode)
[![Discord](https://img.shields.io/discord/1300368230320697404?label=Discord)](https://discord.gg/93M9XSuEj6)
[![PyPI](https://img.shields.io/pypi/v/openmemory-py.svg)](https://pypi.org/project/openmemory-py/)
[![npm](https://img.shields.io/npm/v/openmemory-js.svg)](https://www.npmjs.com/package/openmemory-js)
[![License](https://img.shields.io/github/license/CaviraOSS/OpenMemory)](LICENSE)

![OpenMemory demo](.github/openmemory.gif)

OpenMemory is a **cognitive memory engine** for LLMs and agents.

- 🧠 Real long-term memory (not just embeddings in a table)
- 💾 Self-hosted, local-first (SQLite / Postgres)
- 🐍 Python + 🟦 Node SDKs
- 🧩 Integrations: LangChain, CrewAI, AutoGen, Streamlit, MCP, VS Code
- 📥 Sources: GitHub, Notion, Google Drive, OneDrive, Web Crawler
- 🔍 Explainable traces (see *why* something was recalled)

Your model stays stateless. **Your app stops being amnesiac.**

---

## 1. TL;DR – Use It in 10 Seconds

### 🐍 Python (local-first)

Install:

```bash
pip install openmemory-py
```

Use:

```python
from openmemory.client import Memory

mem = Memory()
mem.add("user prefers dark mode", user_id="u1")
results = mem.search("preferences", user_id="u1")
await mem.delete("memory_id")
```

> Note: `add`, `search`, `get`, `delete` are async. Use `await` in async contexts.

#### 🔗 OpenAI

```python
mem = Memory()
client = mem.openai.register(OpenAI(), user_id="u1")
resp = client.chat.completions.create(...)
```

#### 🧱 LangChain

```python
from openmemory.integrations.langchain import OpenMemoryChatMessageHistory

history = OpenMemoryChatMessageHistory(memory=mem, user_id="u1")
```

#### 🤝 CrewAI / AutoGen / Streamlit

OpenMemory is designed to sit behind **agent frameworks and UIs**:

- Crew-style agents: use `Memory` as a shared long-term store
- AutoGen-style orchestrations: store dialog + tool calls as episodic memory
- Streamlit apps: give each user a persistent memory by `user_id`

See the integrations section in the docs for concrete patterns.

---

### 🟦 Node / JavaScript (local-first)

Install:

```bash
npm install openmemory-js
```

Use:

```ts
import { Memory } from "openmemory-js"

const mem = new Memory()
await mem.add("user likes spicy food", { user_id: "u1" })
const results = await mem.search("food?", { user_id: "u1" })
await mem.delete("memory_id")
```

Drop this into:

- Node backends
- CLIs
- local tools
- anything that needs durable memory without running a separate service.

---

### 📥 Connectors

Ingest data from external sources directly into memory:

```python
# python
github = mem.source("github")
await github.connect(token="ghp_...")
await github.ingest_all(repo="owner/repo")
```

```ts
// javascript
const github = await mem.source("github")
await github.connect({ token: "ghp_..." })
await github.ingest_all({ repo: "owner/repo" })
```

Available connectors: `github`, `notion`, `google_drive`, `google_sheets`, `google_slides`, `onedrive`, `web_crawler`

---

## 2. Modes: SDKs, Server, MCP

OpenMemory can run **inside your app** or as a **central service**.

### 2.1 Python SDK

- ✅ Local SQLite by default
- ✅ Supports external DBs (via config)
- ✅ Great fit for LangChain / LangGraph / CrewAI / notebooks

Docs: https://openmemory.cavira.app/docs/sdks/python

---

### 2.2 Node SDK

- Same cognitive model as Python
- Ideal for JS/TS applications
- Can either run fully local or talk to a central backend

Docs: https://openmemory.cavira.app/docs/sdks/javascript

---

### 2.3 Backend server (multi-user + dashboard + MCP)

Use when you want:

- org‑wide memory
- HTTP API
- dashboard
- MCP server for Claude / Cursor / Windsurf

Run from source:

```bash
git clone https://github.com/CaviraOSS/OpenMemory.git
cd OpenMemory
cp .env.example .env

cd packages/openmemory-js
npm install
npm run dev   # default :8080
```

Or with Docker (API + MCP):

```bash
docker compose up --build -d
```

Optional: include the dashboard service profile:

```bash
docker compose --profile ui up --build -d
```

Using Doppler-managed config (recommended for hosted dashboard/API URLs):

```bash
cd OpenMemory
tools/ops/compose_with_doppler.sh up -d --build
```

Check service status:

```bash
docker compose ps
curl -f http://localhost:8080/health
```

The backend exposes:

- `/api/memory/*` – memory operations
- `/api/temporal/*` – temporal knowledge graph
- `/mcp` – MCP server
- dashboard UI (when `ui` profile is enabled)

---

## 3. Why OpenMemory (vs RAG, vs “just vectors”)

LLMs forget everything between messages.  
Most “memory” solutions are really just **RAG pipelines**:

- text is chunked
- embedded into a vector store
- retrieved by similarity

They don’t understand:

- whether something is a **fact**, **event**, **preference**, or **feeling**
- how **recent / important** it is
- how it links to other memories
- what was true at a specific **time**

Cloud memory APIs add:

- vendor lock‑in
- latency
- opaque behavior
- privacy problems

**OpenMemory gives you an actual memory system:**

- 🧠 Multi‑sector memory (episodic, semantic, procedural, emotional, reflective)
- ⏱ Temporal reasoning (what was true *when*)
- 📉 Decay & reinforcement instead of dumb TTLs
- 🕸 Waypoint graph (associative, traversable links)
- 🔍 Explainable traces (see which nodes were recalled and why)
- 🏠 Self‑hosted, local‑first, you own the DB
- 🔌 SDKs + server + VS Code + MCP

It behaves like a memory module, not a “vector DB with marketing

... (更多内容请访问上面 GitHub 链接)
```

