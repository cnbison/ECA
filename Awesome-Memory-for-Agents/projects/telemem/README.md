# TeleMem

**收录日期:** 2026-06

**GitHub:** [https://github.com/TeleAI-UAGI/telemem](https://github.com/TeleAI-UAGI/telemem)
**Website:** [https://teleai-uagi.github.io/telemem/](https://teleai-uagi.github.io/telemem/)
**Paper:** [https://arxiv.org/abs/2601.06037](https://arxiv.org/abs/2601.06037)

## 简述

Long-term and multimodal memory for agentic AI — a drop-in replacement for Mem0 with character-isolated memory profiles, LLM-based semantic deduplication, video memory with ReAct-style QA, an MCP server, and a fully local option (FAISS + Ollama/Qwen).

## README 摘录（GitHub）

```markdown
<p align="center">
  <a href="https://github.com/TeleAI-UAGI/telemem">
    <img src="./assets/TeleMem.png" width="40%" />
  </a>
</p>

<h1 align="center"> TeleMem: Building Long-Term and Multimodal Memory for Agentic AI </h1>

<p align="center">
  <a href="https://arxiv.org/abs/2601.06037">
    <img src="https://img.shields.io/badge/arXiv-Paper-red" alt="arXiv">
  </a>
  <a href="https://github.com/TeleAI-UAGI/telemem/actions/workflows/ci.yml">
    <img src="https://github.com/TeleAI-UAGI/telemem/actions/workflows/ci.yml/badge.svg" alt="CI">
  </a>
  <a href="https://pypi.org/project/telemem/">
    <img src="https://img.shields.io/pypi/v/telemem?color=blue" alt="PyPI">
  </a>
  <a href="https://github.com/TeleAI-UAGI/telemem">
    <img src="https://img.shields.io/github/stars/TeleAI-UAGI/TeleMem?style=social" alt="GitHub Stars">
  </a>
  <a href="https://github.com/TeleAI-UAGI/TeleMem/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-Apache%20License%202.0-blue" alt="License: Apache 2.0">
  </a>
  <img src="https://img.shields.io/github/last-commit/TeleAI-UAGI/TeleMem?color=blue" alt="Last Commit">
  <img src="https://img.shields.io/badge/PRs-Welcome-red" alt="PRs Welcome">
</p>

<div align="center">
  
**If you find this project helpful, please give us a ⭐️ on GitHub for the latest update.**

_🤝 Contributions welcome! Feel free to open an issue or submit a pull request._

</div>

---

<div align="center">
  <p>
      <a href="README.md">English</a> | <a href="README-ZH.md">简体中文</a>
  </p>
  <p>
      <a href="https://github.com/TeleAI-UAGI/Awesome-Agent-Memory"> <strong>📄 Awesome-Agent-Memory →</strong></a>
  </p>
</div>

TeleMem is an agent memory management layer that can be used as <mark>**a high-performance drop-in replacement for [Mem0](https://mem0.ai/)** with one line of code (`import telemem as mem0`)</mark>, deeply optimized for complex scenarios involving **multi-turn dialogues**, **character modeling**, **long-term information storage**, and **semantic retrieval**.

Through its unique **context-aware enhancement mechanism**, TeleMem provides conversational AI with core infrastructure offering **higher accuracy**, **faster performance**, and **stronger character memory capabilities**.

Building upon this foundation, TeleMem implements **video understanding, multimodal reasoning, and visual question answering** capabilities. Through a complete pipeline of video frame extraction, caption generation, and vector database construction, AI Agents can effortlessly **store, retrieve, and reason over video content** just like handling text memories.

The ultimate goal of the TeleMem project is to _use an agent's hindsight to improve its foresight_. 

**TeleMem, where memory lives on and intelligence grows strong.**

### Why TeleMem?

- 🎭 **Character memory done right** — the only open-source memory layer that automatically builds **isolated, per-character memory profiles**, built for role-play, companion AI, NPCs, and multi-persona assistants.
- 🎬 **Memory for video, not just text** — a full video → frames → captions → vector DB pipeline with **ReAct-style multi-step video QA**.
- 🏠 **Fully local by default** — runs end-to-end on your hardware (Qwen + FAISS); no cloud service, no paid tier, no data leaving your machine.
- 🔌 **mem0-compatible API** — `add()` / `search()` accept the same arguments and return the same `{"results": [...]}` shapes, so existing Mem0 code keeps working.

---

## 📢 Latest Updates
- **[2026-06-12] 🎉 TeleMem [v1.7.1](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.7.1) is live on the [official MCP registry](https://registry.modelcontextprotocol.io) — run the memory server with zero install: `uvx telemem`! Also new: [evaluation principles](https://teleai-uagi.github.io/telemem/evaluation/) and a LongMemEval harness with built-in baselines.**
- **[2026-06-12] 🎉 TeleMem is now on PyPI: `pip install telemem`! [v1.6.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.6.0) adds Ollama/DeepSeek/Kimi configs, LangChain & LlamaIndex examples, and a [documentation site](https://teleai-uagi.github.io/telemem/).**
- **[2026-06-12] 🎉 TeleMem [v1.5.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.5.0) has been released: true mem0 drop-in API, lightweight core install, and CI!**
- **[2026-06-11] 🎉 TeleMem [v1.4.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.4.0) has been released with [MCP support](docs/MCP.md)!**
- **[2026-01-28] 🎉 TeleMem [v1.3.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.3.0) has been released!**
- **[2026-01-22] 🎉 TeleMem [Tech Report](https://arxiv.org/abs/2601.06037) has been updated to its 4th version!**
- **[2026-01-13] 🎉 TeleMem [Tech Report](https://arxiv.org/abs/2601.06037) has been released on arXiv!**
- **[2026-01-09] 🎉 TeleMem [v1.2.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.2.0) has been released!**
- **[2025-12-31] 🎉 TeleMem [v1.1.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.1.0) has been released!**
- **[2025-12-05] 🎉 TeleMem [v1.0.0](https://github.com/TeleAI-UAGI/telemem/releases/tag/v1.0.0) has been released!**

---

## 🔥 Research Highlights

* **Significantly improved memory accuracy**: Achieved **86.33%** accuracy on the ZH-4O Chinese multi-character long-dialogue benchmark, **19% higher** than Mem0.
* **Doubled speed performance**: Millisecond-level semantic retrieval enabled by efficient buffering and batch writing.
* **Greatly reduced token cost**: Optimized token usage delivers the same performance with significantly lower LLM overhead.
* **Precise character memory preservation**: Automatically builds independent memory profiles for each character, eliminating confusion.
* **Automated Video Processing Pipeline**: From raw video → frame extraction → caption generation → vector database, fully automated
* **ReAct-Style Video QA**: Multi-step reasoning + tool calling for precise video content understanding

---

## 📌 Table of Contents

* [Proje

... (更多内容请访问上面 GitHub 链接)
```

