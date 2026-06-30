# Memori

**收录日期:** 未知

**GitHub:** [https://github.com/GibsonAI/Memori](https://github.com/GibsonAI/Memori)
**Website:** [https://memorilabs.ai/](https://memorilabs.ai/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## README 摘录（GitHub）

```markdown
[![Memori Labs](https://images.memorilabs.ai/banner-dark-large.jpg)](https://memorilabs.ai/)

<p align="center">
  <strong>Memory from what agents do, not just what they say.</strong>
</p>

<p align="center">
  <i>Memori plugs into the software and infrastructure you already use. It is LLM, datastore and framework agnostic and seamlessly integrates into the architecture you've already designed.</i>
</p>

<p align="center">
  <strong>→ <a href="https://memorilabs.ai/docs/memori-cloud/">Memori Cloud</a></strong> — Zero config. Get an API key and start building in minutes.
</p>
<p align="center">
  <a href="https://trendshift.io/repositories/15435" target="_blank"><img src="https://trendshift.io/api/badge/repositories/15435" alt="MemoriLabs%2FMemori | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>
</p>

<p align="center">
  <a href="https://badge.fury.io/py/memori">
    <img src="https://badge.fury.io/py/memori.svg" alt="PyPI version">
  </a>
  <a href="https://www.npmjs.com/package/@memorilabs/memori">
    <img src="https://img.shields.io/npm/v/@memorilabs/memori.svg" alt="NPM version">
  </a>
  <a href="https://pepy.tech/projects/memori">
    <img src="https://static.pepy.tech/badge/memori" alt="Downloads">
  </a>
  <a href="https://opensource.org/license/apache-2-0">
    <img src="https://img.shields.io/badge/license-Apache%202.0-blue" alt="License">
  </a>
  <a href="https://discord.gg/abD4eGym6v">
    <img src="https://img.shields.io/discord/1042405378304004156?logo=discord" alt="Discord">
  </a>
</p>

<p align="center">
  <a href="https://github.com/MemoriLabs/Memori/stargazers">
    <img src="https://img.shields.io/badge/⭐%20Give%20a%20Star-Support%20the%20project-orange?style=for-the-badge" alt="Give a Star">
  </a>
</p>

<p align="center">
  <strong>Choose memory that performs</strong>
</p>



[![Memori Labs](https://images.memorilabs.ai/stats.jpg)](https://memorilabs.ai/benchmark)

---

## Getting Started

### Installation

<details open>
<summary><b>TypeScript SDK</b></summary>

```bash
npm install @memorilabs/memori
```
</details>

<details open>
<summary><b>Python SDK</b></summary>

```bash
pip install memori
```
</details>

### Quickstart

Sign up at [app.memorilabs.ai](https://app.memorilabs.ai), get a Memori API key, and start building. Full docs: [memorilabs.ai/docs/memori-cloud/](https://memorilabs.ai/docs/memori-cloud/).

Set `MEMORI_API_KEY` and your LLM API key (e.g. `OPENAI_API_KEY`), then:

<details open>
<summary><b>TypeScript SDK</b></summary>

```typescript
import { OpenAI } from 'openai';
import { Memori } from '@memorilabs/memori';

// Requires MEMORI_API_KEY and OPENAI_API_KEY in your environment
const client = new OpenAI();
const mem = new Memori().llm
  .register(client)
  .attribution('user_123', 'support_agent');

async function main() {
  await client.chat.completions.create({
    model: 'gpt-4o-mini',
    messages: [{ role: 'user', content: 'My favorite color is blue.' }],
  });
  // Conversations are persisted and recalled automatically in the background.

  const response = await client.chat.completions.create({
    model: 'gpt-4o-mini',
    messages: [{ role: 'user', content: "What's my favorite color?" }],
  });
  // Memori recalls that your favorite color is blue.
}
```
</details>

<details open>
<summary><b>Python SDK</b></summary>

```python
from memori import Memori
from openai import OpenAI

# Requires MEMORI_API_KEY and OPENAI_API_KEY in your environment
client = OpenAI()
mem = Memori().llm.register(client)

mem.attribution(entity_id="user_123", process_id="support_agent")

response = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": "My favorite color is blue."}]
)
# Conversations are persisted and recalled automatically.

response = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": "What's my favorite color?"}]
)
# Memori recalls that your favorite color is blue.
```
</details>

## Explore the Memories

Use the [Dashboard](https://app.memorilabs.ai) — Memories, Analytics, Playground, and API Keys.

> [!TIP]
> Want to use your own database? Check out docs for Memori BYODB here:
> [https://memorilabs.ai/docs/memori-byodb/](https://memorilabs.ai/docs/memori-byodb/).
> For disposable BYODB development databases, see the TiDB Zero provisioning
> guide: [docs/memori-byodb/databases/tidb.mdx](docs/memori-byodb/databases/tidb.mdx).

## LoCoMo Benchmark

Memori was evaluated on the LoCoMo benchmark for long-conversation memory and achieved **81.95% overall accuracy** while using an average of **1,294 tokens per query**. That is just **4.97% of the full-context footprint**, showing that structured memory can preserve reasoning quality without forcing large prompts into every request.

Compared with other retrieval-based memory systems, Memori outperformed Zep, LangMem, and Mem0 while reducing prompt size by roughly **67% vs. Zep** and lowering context cost by more than **20x vs. full-context prompting**.

Read the [benchmark overview](docs/memori-cloud/benchmark/overview.mdx), see the [results](docs/memori-cloud/benchmark/results.mdx), or download the [paper](https://arxiv.org/abs/2603.19935).

!["Memori's average accuracy along with the standard deviation"](https://images.memorilabs.ai/docs/memori-locomo-benchmark.webp)

## OpenClaw (Persistent Memory for Your Gateway)

By default, OpenClaw agents forget everything between sessions. The Memori plugin fixes that. It automatically captures structured memory from conversation and agent execution after each turn — including tool calls, decisions, and outcomes — and makes it available for agents to recall on demand.

No changes to your agent code or prompts are required. The plugin hooks into OpenClaw's lifecycle, so you get structured memory, agent-controlled recall, and Advanced Augmentation with a drop-in plugin.

```bash
openclaw plugins install @memorilabs/openclaw-memori
open

... (更多内容请访问上面 GitHub 链接)
```

