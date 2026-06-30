# Hindsight

**收录日期:** 2025-12

**GitHub:** [https://github.com/vectorize-io/hindsight](https://github.com/vectorize-io/hindsight)
**Website:** [https://hindsight.vectorize.io/](https://hindsight.vectorize.io/)
**Paper:** [https://arxiv.org/abs/2512.12818](https://arxiv.org/abs/2512.12818)

## 简述

Hindsight is 20/20: Building Agent Memory that Retains, Recalls, and Reflects

## GitHub README 摘要

> [Documentation](https://hindsight.vectorize.io) • [Paper](https://arxiv.org/abs/2512.12818) • [Cookbook](https://hindsight.vectorize.io/cookbook) • [Hindsight Cloud](https://ui.hindsight.vectorize.io/signup)

## README 摘录（GitHub）

```markdown
<div align="center">

![Hindsight Banner](./hindsight-docs/static/img/hindsight-github-banner.png)

[Documentation](https://hindsight.vectorize.io) • [Paper](https://arxiv.org/abs/2512.12818) • [Cookbook](https://hindsight.vectorize.io/cookbook) • [Hindsight Cloud](https://ui.hindsight.vectorize.io/signup)

[![CI](https://github.com/vectorize-io/hindsight/actions/workflows/release.yml/badge.svg)](https://github.com/vectorize-io/hindsight/actions/workflows/release.yml)
[![Slack Community](https://img.shields.io/badge/Slack-Join%20Community-4A154B?logo=slack)](https://join.slack.com/t/hindsight-space/shared_invite/zt-3nhbm4w29-LeSJ5Ixi6j8PdiYOCPlOgg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![PyPI - Downloads](https://img.shields.io/pypi/dm/hindsight-api?label=PyPI)
![NPM Downloads](https://img.shields.io/npm/dm/%40vectorize-io%2Fhindsight-client?logoColor=orange&label=NPM&color=blue&link=https%3A%2F%2Fwww.npmjs.com%2Fpackage%2F%40vectorize-io%2Fhindsight-client)
<br/>

<a href="https://trendshift.io/repositories/15603" target="_blank"><img src="https://trendshift.io/api/badge/repositories/15603" alt="vectorize-io%2Fhindsight | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>
</div>

---

## What is Hindsight?

Hindsight™ is an agent memory system built to create smarter agents that learn over time. Most agent memory systems focus on recalling conversation history. Hindsight is focused on making agents that learn, not just remember.


<video src="https://github.com/user-attachments/assets/923b798d-3581-4897-bb62-9cfa5a931682" controls></video>

It eliminates the shortcomings of alternative techniques such as RAG and knowledge graph and delivers state-of-the-art performance on long term memory tasks.

## Memory Performance & Accuracy

Hindsight is the most accurate agent memory system ever tested according to benchmark performance. It has achieved state-of-the-art performance on the LongMemEval benchmark, widely used to assess memory system performance across a variety of conversational AI scenarios. The current reported performance of Hindsight and other agent memory solutions as of January 2026 is shown here:

![Overview](./hindsight-docs/static/img/hindsight-benchmarks.png)

The benchmark performance data for Hindsight has been independently reproduced by research collaborators at the Virginia Tech [Sanghani Center for Artificial Intelligence and Data Analytics](https://sanghani.cs.vt.edu/) and The Washington Post. Other scores are self-reported by software vendors.

Hindsight is being used in production at Fortune 500 enterprises and by a growing number of AI startups. 

## Adding Hindsight to Your AI Agents

The easiest way to use Hindsight with an existing agent is with the LLM Wrapper. You can add memory to your agent with 2 lines of code. That will swap your current LLM client out with the Hindsight wrapper. After that, memories will be stored and retrieved automatically as you make LLM calls.

If you need more control over how and when your agent stores and recalls memories, there's also a simple API you can integrate with using the SDKs or directly via HTTP.

![Hindsight Banner](./hindsight-docs/static/img/migration-code.png)

---

> 🤖 **Using a coding agent?** Install the Hindsight documentation skill for instant access to docs while you code:
> ```bash
> npx skills add https://github.com/vectorize-io/hindsight --skill hindsight-docs
> ```
> Works with Claude Code, Cursor, and other AI coding assistants.

---


## Quick Start

### Docker (recommended)

```bash
export OPENAI_API_KEY=sk-xxx

docker run -it --pull always --name hindsight --restart unless-stopped -p 8888:8888 -p 9999:9999 \
  -e HINDSIGHT_API_LLM_API_KEY=$OPENAI_API_KEY \
  -v hindsight-data:/home/hindsight/.pg0 \
  ghcr.io/vectorize-io/hindsight:latest
```

>API: http://localhost:8888
>UI: http://localhost:9999

You can modify the LLM provider by setting `HINDSIGHT_API_LLM_PROVIDER`. Valid options are `openai`, `anthropic`, `gemini`, `groq`, `ollama`, `lmstudio`, `minimax`, and `atlas` ([Atlas Cloud](https://www.atlascloud.ai/?utm_source=github&utm_medium=link&utm_campaign=hindsight)). The documentation provides more details on [supported models](https://hindsight.vectorize.io/developer/models).



### Docker (external PostgreSQL)

```bash
export OPENAI_API_KEY=sk-xxx
export HINDSIGHT_DB_PASSWORD=choose-a-password
cd docker/docker-compose
docker compose up 
```

> Oracle AI Database is also supported for enterprise deployments with full feature parity. See the [storage documentation](https://hindsight.vectorize.io/developer/storage) for details.


>API: http://localhost:8888
>UI: http://localhost:9999

### Client

```bash
pip install hindsight-client -U
# or
npm install @vectorize-io/hindsight-client
```

#### Python

```python
from hindsight_client import Hindsight

client = Hindsight(base_url="http://localhost:8888")

# Retain: Store information
client.retain(bank_id="my-bank", content="Alice works at Google as a software engineer")

# Recall: Search memories
client.recall(bank_id="my-bank", query="What does Alice do?")

# Reflect: Generate disposition-aware response
client.reflect(bank_id="my-bank", query="Tell me about Alice")
```

#### Node.js / TypeScript

```bash
npm install @vectorize-io/hindsight-client
```

```javascript
const { HindsightClient } = require('@vectorize-io/hindsight-client');

const main = async () => {
  const client = new HindsightClient({ baseUrl: 'http://localhost:8888' });

  await client.retain('my-bank', 'Alice loves hiking in Yosemite');

  const results = await client.recall('my-bank', 'What does Alice like?');
  console.log(results);
}

main();
```


### Python Embedded (no server required)

```bash
pip install hindsight-all -U
```

On Intel (x86_64) Macs, install `hindsight-all-slim` instead — see [Supported Platforms](#supported-platforms).

```python
import os
from hindsight import Hi

... (更多内容请访问上面 GitHub 链接)
```

