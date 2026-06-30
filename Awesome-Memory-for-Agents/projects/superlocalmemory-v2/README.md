# SuperLocalMemory V2

**收录日期:** 2026-02

**GitHub:** [https://github.com/varun369/SuperLocalMemoryV2](https://github.com/varun369/SuperLocalMemoryV2)
**Website:** [https://varun369.github.io/SuperLocalMemoryV2/](https://varun369.github.io/SuperLocalMemoryV2/)

## 简述

Universal local-first memory infrastructure for AI agents with dual MCP + A2A protocol support

## GitHub README 摘要

> Proxy: <code>slm wrap claude</code> &nbsp;·&nbsp; MCP: add <code>slm_compress</code> to your config &nbsp;·&nbsp; Skill: zero-config</p>

## README 摘录（GitHub）

```markdown
<p align="center">
  <img src="https://superlocalmemory.com/assets/logo-mark.png" alt="SuperLocalMemory" width="200"/>
</p>

<h1 align="center">SuperLocalMemory V3.6.18</h1>
<p align="center"><strong>Cache. Compress. Remember. Three surfaces — proxy, MCP tools, or skill. Every setup covered.</strong><br/>
<em>To the best of our knowledge, the only zero-cloud agent memory that beats Mem0's zero-LLM score on LoCoMo. Mode A: 74.8% vs Mem0 64.2% — no GPU, no API key, on CPU.</em></p>
<p align="center"><code>v3.6.18</code> — <strong>Plugin-native. Profile-aware. Distributed-ready.</strong><br/>
Proxy: <code>slm wrap claude</code> &nbsp;·&nbsp; MCP: add <code>slm_compress</code> to your config &nbsp;·&nbsp; Skill: zero-config</p>
<p align="center"><strong>3 published research papers</strong> (arXiv preprints + Zenodo-archived) · <a href="https://arxiv.org/abs/2603.02240">arXiv:2603.02240</a> · <a href="https://arxiv.org/abs/2603.14588">arXiv:2603.14588</a> · <a href="https://arxiv.org/abs/2604.04514">arXiv:2604.04514</a></p>

<p align="center">
  <a href="https://arxiv.org/abs/2603.14588"><img src="https://img.shields.io/badge/arXiv-2603.14588-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" alt="arXiv Paper"/></a>
  <a href="#three-surfaces-proxy--mcp-tools--skill"><img src="https://img.shields.io/badge/Proxy_|_MCP_|_Skill-22c55e?style=for-the-badge" alt="Three Surfaces: Proxy, MCP Tools, Skill"/></a>
  <a href="https://pypi.org/project/superlocalmemory/"><img src="https://img.shields.io/pypi/v/superlocalmemory?style=for-the-badge&logo=pypi&logoColor=white" alt="PyPI"/></a>
  <a href="https://www.npmjs.com/package/superlocalmemory"><img src="https://img.shields.io/npm/v/superlocalmemory?style=for-the-badge&logo=npm&logoColor=white" alt="npm"/></a>
  <a href="https://www.gnu.org/licenses/agpl-3.0"><img src="https://img.shields.io/badge/License-AGPL_v3-blue.svg?style=for-the-badge" alt="AGPL v3"/></a>
  <a href="#eu-ai-act-compliance"><img src="https://img.shields.io/badge/EU_AI_Act-Design_Compliant-brightgreen?style=for-the-badge" alt="EU AI Act Design Compliant"/></a>
  <a href="https://superlocalmemory.com"><img src="https://img.shields.io/badge/Web-superlocalmemory.com-ff6b35?style=for-the-badge" alt="Website"/></a>
  <a href="#dual-interface-mcp--cli"><img src="https://img.shields.io/badge/MCP-Native-blue?style=for-the-badge" alt="MCP Native"/></a>
  <a href="#dual-interface-mcp--cli"><img src="https://img.shields.io/badge/CLI-Agent--Native-green?style=for-the-badge" alt="CLI Agent-Native"/></a>
  <a href="#multilingual-embedding-support"><img src="https://img.shields.io/badge/Multilingual-30%2B_Languages-ff69b4?style=for-the-badge" alt="Multilingual 30+ Languages"/></a>
</p>

---

## Why SuperLocalMemory?

Every hosted AI memory platform — Mem0 Cloud, Zep Cloud, Letta Cloud, EverMemOS Cloud — sends your data to cloud LLMs by default. Self-hosted variants exist but require Docker, a separate graph DB, or Ollama config, and most default to OpenAI until you flip env vars. After **August 2, 2026**, any of those cloud paths becomes a compliance question under the EU AI Act.

SuperLocalMemory V3 uses **mathematics instead of cloud compute** — differential geometry, algebraic topology, and stochastic analysis replace the work other systems need LLMs to do. Local-first out of the box. No Docker. No graph DB. No API keys. CPU-only.

**Benchmark results** (evaluated on [LoCoMo](https://arxiv.org/abs/2402.09714), the standard long-conversation memory benchmark, published April 2026):

| System | Score | Config | Cloud LLM required? | Open Source | Source |
|:-------|:-----:|:-------|:-------------------:|:-----------:|:-------|
| EverMemOS | 93.05% | Cloud (proprietary) | Yes | Core only | [evermind.ai](https://evermind.ai/) (Feb 2026) |
| Hindsight (LoComo10) | 92.0% | Cloud | Yes | No | [benchmarks.hindsight.vectorize.io](https://benchmarks.hindsight.vectorize.io) (Apr 2026) |
| Mem0 (token-efficient) | 91.6% | Hybrid (Cohere/OpenAI) | Yes | Partial | [mem0.ai blog](https://mem0.ai/blog/mem0-the-token-efficient-memory-algorithm) (Apr 16 2026) |
| **SLM V3 Mode C** | **87.7%** | Local + optional LLM | Optional (Ollama OK) | **Yes (AGPL-3.0)** | In-house, [arXiv:2603.14588](https://arxiv.org/abs/2603.14588) |
| Zep v3 Cloud | 85.2% | Cloud | Yes | Community deprecated | [getzep.com](https://www.getzep.com/) |
| **SLM V3 Mode A** | **74.8%** | **Local, CPU-only, zero-LLM** | **No** | **Yes (AGPL-3.0)** | In-house, [arXiv:2603.14588](https://arxiv.org/abs/2603.14588) |
| Mem0 (zero-retrieval-LLM) | 64.2% | Local baseline | No | Partial | Mem0 paper, zero-LLM row |

> **How to read this table.** Scores from different papers use different LoCoMo splits, judge models, and prompt variants. We do NOT claim these numbers are apples-to-apples across rows. Rows marked "In-house" were run by us; cited rows link to the vendor's public source and date. The only apples-to-apples comparison is **Mode A 74.8% vs Mem0 zero-retrieval-LLM 64.2%** (+10.6pp) — both are zero-LLM configurations. Mem0's 91.6% and EverMemOS's 93.05% use cloud LLMs; Mode C uses a local LLM (Ollama).

**What Mode A is:** CPU-only, SQLite-only, zero-LLM retrieval on published LoCoMo questions. To the best of our knowledge it is the only publicly-released local-first memory that clears Mem0's zero-LLM baseline on this benchmark. If another fully-local system hits similar numbers, please open an issue so we can update this table.

Mathematical layers contribute **+12.7 percentage points** average across 6 conversations (n=832 questions), with up to **+19.9pp on the most challenging dialogues**.

---

## Quick Start

```bash
# npm (recommended)
npm install -g superlocalmemory
slm setup       # Choose mode (A/B/C)
slm doctor      # Verify everything is working
```

```bash
# pip
pip install superlocalmemory
slm setup
slm doctor
```

```bash
# First use
slm remember "Alice works at Google as a Staff Engineer"
slm recall "What does Alice do?"


... (更多内容请访问上面 GitHub 链接)
```

