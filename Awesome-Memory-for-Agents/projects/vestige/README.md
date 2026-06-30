# Vestige

**收录日期:** 2026-05

**GitHub:** [https://github.com/samvallad33/vestige](https://github.com/samvallad33/vestige)
**Website:** [https://github.com/samvallad33/vestige](https://github.com/samvallad33/vestige)

## 简述

Local-first cognitive memory MCP server for coding agents. Supports FSRS-6 decay, spreading activation, contradiction inspection, active suppression, Receipt Lock, and an inspectable dashboard.

## GitHub README 摘要

> [**⚡ Quick Start**](#-get-it-running-in-60-seconds) · [**🧠 The Idea**](#-why-i-built-this) · [**🔬 The Science**](#-this-is-real-neuroscience-not-a-metaphor) · [**🛠 13 Tools**](#-13-tools-one-brain) · [**📊 Dashboard**](#-watch-your-ai-think-in-3d)

## README 摘录（GitHub）

```markdown
<div align="center">

<h1>Vestige</h1>

### Your bug was born days before it crashed. You just can't remember where.

<em>Vestige is a local-first memory for AI agents that reaches <b>backward through time</b> to find the quiet change that caused today's failure: the cause that looks nothing like the bug. One 23MB Rust binary. No cloud. Your data never leaves your machine.</em>

[![GitHub stars](https://img.shields.io/github/stars/samvallad33/vestige?style=for-the-badge&logo=github&color=8b5cf6)](https://github.com/samvallad33/vestige/stargazers)
[![Release](https://img.shields.io/github/v/release/samvallad33/vestige?style=for-the-badge&color=06b6d4)](https://github.com/samvallad33/vestige/releases/latest)
[![Tests](https://img.shields.io/badge/tests-1550_passing-22c55e?style=for-the-badge)](https://github.com/samvallad33/vestige/actions)
[![License](https://img.shields.io/badge/license-AGPL--3.0-3b82f6?style=for-the-badge)](LICENSE)

[**⚡ Quick Start**](#-get-it-running-in-60-seconds) · [**🧠 The Idea**](#-why-i-built-this) · [**🔬 The Science**](#-this-is-real-neuroscience-not-a-metaphor) · [**🛠 13 Tools**](#-13-tools-one-brain) · [**📊 Dashboard**](#-watch-your-ai-think-in-3d)

</div>

---

## 👋 Why I built this

Hi, I'm [Sam](https://github.com/samvallad33). I built Vestige from a tiny apartment in Chicago because I kept losing days to the same thing, and I bet you have too.

Production breaks. You start hunting. And the cause is almost never *near* the error. It's some quiet change you made days ago that looks **nothing** like the crash it eventually caused. A flipped env var. A swapped service. A config tweak you'd already forgotten.

Here's the part that took me a while to see: **every AI memory tool is built on vector search, and vector search hunts for what *looks like* your problem.** But a root cause never looks like the bug it creates. So they all search the goal line, while the real failure was a quiet midfield turnover fifteen minutes earlier.

I wanted a memory that traces the match *backward.*

So that's what Vestige is. Everyone else built a memory that **remembers**. I tried to build the first one that **realizes**: it gates what's worth keeping, lets the noise fade like your own memory does, and when a failure hits, it reaches back through time to the change that actually caused it.

It's one Rust binary. It runs entirely on your machine. It never phones home. And there's a 60-second start right below.

> 🎙️ **The 60-second version** of this whole story, the one I give in person, lives in [`demo/PITCH-v2-causebench.md`](demo/PITCH-v2-causebench.md). If you've got a minute, read that first. It's the clearest way to *get* why this matters.

---

## ⚡ Get it running in 60 seconds

**Step 1 — install (one binary, no Docker, no API key, no signup):**

```bash
npm install -g vestige-mcp-server@latest
```

**Step 2 — connect it to your agent.** Vestige speaks [MCP](https://modelcontextprotocol.io), so it works with *any* AI agent. The universal config (works everywhere):

```json
{ "mcpServers": { "vestige": { "command": "vestige-mcp" } } }
```

Drop that into your agent's MCP config file. Or use the one-line shortcut for your agent:

```bash
# Cursor / Windsurf / VS Code      → add the JSON above to ~/.cursor/mcp.json (or the editor's MCP settings)
# Claude Code                      → claude mcp add vestige vestige-mcp -s user
# Codex                            → codex mcp add vestige -- vestige-mcp
# Cline / Continue / Zed / Goose   → add the JSON above to that client's MCP config
```

**Step 3 — confirm it's working:**

```bash
vestige-mcp --version     # prints the installed version
vestige stats             # prints your memory count (0 on a fresh install)
```

That's the whole install. Per-agent guides (Cursor, VS Code, Windsurf, JetBrains, Xcode, OpenCode, Codex, Claude Desktop) are [here ↓](#-works-with-every-ai-agent).

Now talk to your agent like it has a memory, because now it does:

```
You:  "Remember: we always disable SimSIMD on release builds, it breaks old x86 CPUs."
        ...days later, fresh session, zero context...
You:  "Should I enable SimSIMD for the release?"
AI:   ⚠️ Hold on, this contradicts a decision you stored: you chose to DISABLE it
        because it breaks old x86 CPUs.
```

That last line isn't me being cute. It's a real status the engine returns, called `claim_contradicts_memory`. Most memory tools would have happily handed you the wrong answer. Vestige tells you when you're about to walk back into a mistake you already learned from.

And the headline feature, the one nothing else does, is one command:

```bash
vestige backfill --contrast
```

When a failure is in your memory, this reaches *backward through time* and finds the quiet earlier change that caused it (the one a vector search ranks poorly because it shares no words with the error). It shows you, side by side, what similarity search returns versus the real cause. [More on the backward reach ↓](#-the-thing-nothing-else-does-memory-with-hindsight)

*(Works with Codex, Cursor, VS Code, Claude Desktop, Windsurf, JetBrains, Zed: anything that speaks MCP. [Full setup is here ↓](#-works-in-every-editor-you-use).)*

---

## 🧠 It's not RAG with a nicer haircut

RAG is a bucket: throw everything in, hope nearest-neighbor finds it later. Vestige behaves more like an actual memory: it decides what's worth keeping, forgets what isn't, and reasons across what's left.

|  | 🪣 RAG / Vector Store | 🧠 Vestige |
|---|---|---|
| **What it stores** | Everything you hand it | Only what's **surprising or new** (the rest gets merged or skipped) |
| **What it forgets** | Nothing; it just bloats | Unused memories **fade** on a real forgetting curve, so your context stays lean |
| **Finding a root cause** | Can't, because the cause isn't *similar* to the bug | **Reaches backward in time** to the change that caused it (the whole point ↓) |
| **Catching contradictions** | Silent; serves the stale answer with a 

... (更多内容请访问上面 GitHub 链接)
```

