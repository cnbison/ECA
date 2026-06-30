# AccInt

**收录日期:** 2026-06

**GitHub:** [https://github.com/maxbaluev/accreted-intelligence](https://github.com/maxbaluev/accreted-intelligence)
**Website:** [https://accint.xyz/](https://accint.xyz/)

## 简述

Local-first Work Model for AI agents: records commitments, actions, approval gates, outcomes, and reusable runtimes, then uses outcome-scored memory to predict and replay verified paths across Claude Code, Codex, OpenCode, and Cursor via MCP.

## GitHub README 摘要

> > Make your AI work compound. Offload the task. Never the learning.

## README 摘录（GitHub）

```markdown
# Accreted Intelligence

[![Stars](https://img.shields.io/github/stars/maxbaluev/accreted-intelligence?style=flat&logo=github&color=f5c518)](https://github.com/maxbaluev/accreted-intelligence/stargazers)
[![License](https://img.shields.io/badge/license-Apache--2.0%20(repo%20glue)-blue)](LICENSE)
[![MCP](https://img.shields.io/badge/MCP-server-1f6feb)](https://modelcontextprotocol.io)
[![Official MCP Registry](https://img.shields.io/badge/MCP%20Registry-io.github.maxbaluev%2Faccint-1f6feb)](https://registry.modelcontextprotocol.io/v0.1/servers/io.github.maxbaluev%2Faccint/versions/latest)
[![Works with](https://img.shields.io/badge/works%20with-Claude%20Code%20·%20OpenCode%20·%20Codex%20·%20Cursor-7c3aed)](#install)
[![Platform](https://img.shields.io/badge/platform-Linux%20·%20macOS%20·%20Windows-555)](#install)
[![Live](https://img.shields.io/badge/live-accint.xyz-3fb950)](https://accint.xyz/?ref=github-readme&utm_source=github&utm_campaign=readme)

> Make your AI work compound. Offload the task. Never the learning.

AI agents are powerful but amnesiac: every run burns your tokens on real work, ships an output, then forgets. You **rent** capability — you never build it. `acc` changes the unit from a task that evaporates to an **investment that compounds**. Hand work to the agents you already run (Claude Code, Codex, OpenCode, Cursor), and **two things** compound into one owned asset — a **Work Model** of your business: your **intellect** (what you decide, what good looks like, what you'll never allow) and your **agents' tokens** (every verified path distilled into a runtime that replays instead of re-reasoning). It learns what actually worked, checked against your own results, and **predicts the better path before the next run starts**. It acts in your real accounts with a receipt for every step, holds anything that leaves your machine for your OK, and lets reality settle it. So the same job gets cheaper, faster, and genuinely better every time it runs. The learning is yours: **swap the model, keep the company veteran.** Your work turns into capital you own, on a machine you control.

```
predict the better path  →  act in your accounts, receipted  →  reality settles it  →  the Work Model sharpens
```

> **See it live: [accint.xyz](https://accint.xyz/?ref=github-readme&utm_source=github&utm_campaign=readme).** The commitments ledger settles in real time there, alongside the full story and a measured readout that updates as the system runs. The engine source is private; the binary installs in one line (below) and the building blocks are open. We say what's proven and what's young.

---

## Why this exists

A model that scores 90% on a benchmark today scores 90% tomorrow. It doesn't learn from deployment, doesn't track which of its outputs led to good outcomes, and doesn't remember last week's mistake. It generates intelligence and throws it away. You keep paying — in time and tokens — to rediscover what already worked.

Accreted Intelligence is a bet that this is temporary. The idea is to move learning out of model weights and into scored external state, where judgment compounds from contact with reality and the model becomes a replaceable processor rather than the place intelligence lives. **The reasoning engine is the part you can swap; the judgment it earned in your world is the part you keep.**

There's a gap in how the existing tools are positioned, and it's where `acc` sits. Memory remembers context. Observability shows traces. Automation runs playbooks. `acc` closes the learning loop: commitment, action, approval, outcome, reusable path — scored by results, audited on a ledger, and running fully on your hardware. And it does the one thing memory can't: it **predicts** the path most likely to work from everything that worked in your world before, then watches its own error.

`acc` is a working kernel for that thesis. It's a Recursive Language Model over a late-interaction scored-token memory: two verbs over one memory. Credit defaults to a weak prior, and only reality earns full weight.

---

## One universal workflow for everything

There is no separate mode for technical and non-technical work. The loop is identical whether you're shipping code or chasing invoices. Only the content of what's retrieved and acted on differs. You talk to your agent in plain words, and the domain lives in the content rather than the architecture.

| Job | Run 1 | What `acc` now predicts and replays |
|---|---|---|
| Ship a feature | reasons every step, runs the tests | the test that catches this class of bug, the path that passed |
| Source candidates | reads your ATS, ranks, drafts first-touches | the sourcing angle that got replies |
| Chase invoices | reads the ledger, drafts the nudge | which reminder cadence actually moves receivables |
| Monday client briefs | gathers, drafts, files | the brief shape each client reads |

*(Illustrative. The measured counts live at [accint.xyz](https://accint.xyz/?ref=github-readme&utm_source=github&utm_campaign=readme). These rows show the shape, not a benchmark.)*

Four different jobs, one set of primitives: **commitment → action → `HELD → your OK` → outcome → credited lesson.** The authority gate (`HELD → your OK`) is structural in every flow that touches the outside world. That gate is what makes the same loop safe for consequential work and not only for code.

Run it again next week and verified steps replay instead of re-reasoning. Most AI re-reasons every task from scratch, so you pay full price forever. `acc` predicts the path that worked and replays the verified steps, so the same job costs less every run and keeps dropping as it learns.

---

## Install

`acc` installs in one line. It runs the installer for your OS, which sets `acc` up on your machine:

```bash
curl -fsSL https://raw.githubusercontent.com/maxbaluev/accreted-intelligence/main/bootstrap/install | ACC_INSTALL_REF=github-readme ACC_INSTALL_SOURCE='ref=github-readme&utm_source=github&utm_ca

... (更多内容请访问上面 GitHub 链接)
```

