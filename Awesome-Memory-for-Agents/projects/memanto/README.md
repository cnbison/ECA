# Memanto

**收录日期:** 2026-04

**GitHub:** [https://github.com/moorcheh-ai/memanto](https://github.com/moorcheh-ai/memanto)
**Website:** [https://memanto.ai/](https://memanto.ai/)
**Paper:** [https://arxiv.org/abs/2604.22085](https://arxiv.org/abs/2604.22085)

## 简述

Memanto: Typed Semantic Memory with Information-Theoretic Retrieval for Long-Horizon Agents

## GitHub README 摘要

> Persistent memory for Claude Code, Cursor, Codex, and 14+ other agents, built on the world's first information-theoretic search engine. 100% free, open source, and runs entirely on your machine - no API keys, no vector database, no backend to babysit.

## README 摘录（GitHub）

```markdown
<p align="center">
    <a href="https://www.memanto.ai/">
    <img alt="MEMANTO Logo" src="https://github.com/moorcheh-ai/memanto/raw/main/assets/memanto-logo.svg" width="500">
    </a>
</p>

<div align="center">
  <h1>Memory that AI Agents Love!</h1>
</div>

<h2 align="center">
  <em>A companion memory agent that lets your agents focus and improve while you keep ownership of everything they learn.</em>
</h2>

<p align="center">
  Persistent memory for Claude Code, Cursor, Codex, and 14+ other agents, built on the world's first information-theoretic search engine. 100% free, open source, and runs entirely on your machine - no API keys, no vector database, no backend to babysit.
</p>

<p align="center">
  <a href="https://memanto.ai/discord">
    <img src="https://img.shields.io/badge/Join-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Join Discord">
  </a>
  <a href="https://www.youtube.com/watch?v=vEtOaoweIG4">
    <img src="https://img.shields.io/badge/Setup-Video-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Setup Video">
  </a>
  <a href="https://docs.memanto.ai">
    <img src="https://img.shields.io/badge/Docs-memanto.ai-000000?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Docs">
  </a>
</p>

<p align="center">
    <a href="https://pepy.tech/projects/memanto"><img alt="PyPI - Total Downloads" src="https://static.pepy.tech/personalized-badge/memanto?period=total&units=INTERNATIONAL_SYSTEM&left_color=BLACK&right_color=GREEN&left_text=downloads"></a>
    <a href="https://deepwiki.com/moorcheh-ai/memanto"><img alt="Ask DeepWiki" src="https://deepwiki.com/badge.svg"></a>
    <a href="https://opensource.org/licenses/MIT"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg"></a>
    <a href="https://pypi.org/project/memanto/"><img alt="PyPI Version" src="https://img.shields.io/pypi/v/memanto.svg?color=%2334D058"></a>
    <a href="https://x.com/moorcheh_ai" target="_blank"><img src="https://img.shields.io/twitter/url/https/twitter.com/langchain.svg?style=social&label=Follow%20%40Moorcheh.ai" alt="Twitter / X"></a>
</p>


<p align="center"><a href="https://trendshift.io/repositories/27378" target="_blank"><img src="https://trendshift.io/api/badge/repositories/27378" alt="moorcheh-ai%2Fmemanto | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a></p>

<p align="center">
  <a href="https://www.star-history.com/?repos=moorcheh-ai%2Fmemanto&type=date&legend=top-left">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=moorcheh-ai/memanto&type=date&theme=dark&legend=top-left" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=moorcheh-ai/memanto&type=date&legend=top-left" />
    <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=moorcheh-ai/memanto&type=date&legend=top-left" />
  </picture>
  </a>
</p>



---
## What Is MEMANTO?

**MEMANTO is a memory agent. It remembers, recalls, and answers — so your agents can achieve long-term goals and avoid confusion.**

Most memory tools today are passive infrastructure: agents have to query them, parse the results, and figure out what to do next. MEMANTO is built differently. It's an active memory agent designed from the gaps agents themselves named when asked about their memory — three operations (`remember`, `recall`, `answer`) that give your agents persistent context across sessions, with state-of-the-art retrieval and zero ingestion latency.

<div align="center">
  <h1>Memanto in action</h1>
  <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 20px 0;">
    <div style="text-align: center;">
      <h2 style="margin-top: 8px;">Without Memanto</strong></h2>
      <img src="https://github.com/moorcheh-ai/memanto/raw/main/assets/Before.gif" alt="Before" width="1100" style="border-radius: 8px;">
    </div>
    <div style="text-align: center;">
        <h2 style="margin-top: 8px;">With Memanto Connected</strong></h2>
        <img src="https://github.com/moorcheh-ai/memanto/raw/main/assets/After.gif" alt="After" width="1100" style="border-radius: 8px;">
    </div>
  </div>
</div>

## Get started in 2 minutes

Works on macOS, Linux, and Windows.

**Option A — Fully local (no account, no API key):**
```bash
pip install memanto
memanto           # choose "On-Prem" — guides through Docker + Ollama setup
```
Requires Docker. Everything runs and stays on your machine.

**Option B — Free cloud (no card, ~60 seconds):**
```bash
pip install memanto
memanto           # choose "Cloud" — paste your free Moorcheh API key
```
Get your free API from : https://console.moorcheh.ai/api-keys

Switch between local and cloud at any time with `memanto config backend`.

---

## What you get

- **No more re-explaining your codebase** after every context reset. Memanto persists across sessions, your agent picks up where it left off.
- **Fewer tokens burned on repeated context.** Memories are retrieved only when relevant, so context windows go further.
- **Memories searchable the instant they're stored.** Zero indexing wait, no LLM extraction tax at write time.
- **One `pip install`.** No vector DB to provision, no schema, no rerankers, no backend service to babysit.
- **Flexible deployment.** Choose between running the backend fully local, using it as a cloud SaaS, hosting in your own VPC, or switching between any of these options anytime you want.

---

## Integrations

Works with Claude Code, Cursor, Codex, Windsurf, Cline, Continue, Goose, GitHub Copilot, and more. See the [full list →](https://docs.memanto.ai/integrations/overview)

```bash
memanto connect <integration-tool-id> # integrates in one command
#eg: memanto connect claude-code    
```

---

## The Six Gaps

Most memory tools are passive infrastructure — agents have to query them, parse the results, and figure out what to do. Memanto is an active

... (更多内容请访问上面 GitHub 链接)
```

