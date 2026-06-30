# Memobase

**收录日期:** 未知

**GitHub:** [https://github.com/memodb-io/memobase](https://github.com/memodb-io/memobase)
**Website:** [https://www.memobase.io/](https://www.memobase.io/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## README 摘录（GitHub）

```markdown
<div align="center">
    <a href="https://memobase.io">
    <picture>
      <img alt="Memobase logo" src="./assets/images/logo.png" width="80%">
    </picture>
  </a>
  <h1>Memobase</h1>
  <p>
    <a href="https://pypi.org/project/memobase/">
      <img src="https://img.shields.io/pypi/v/memobase.svg">
    </a>
    <a href="https://www.npmjs.com/package/@memobase/memobase">
      <img src="https://img.shields.io/npm/v/@memobase/memobase.svg?logo=npm&logoColor=fff&style=flat&labelColor=2C2C2C&color=28CF8D">
    </a>
    <a href="https://jsr.io/@memobase/memobase">
      <img src="https://img.shields.io/jsr/v/@memobase/memobase.svg?logo=jsr&logoColor=fff&style=flat&labelColor=2C2C2C&color=28CF8D" />
    </a>
    <a href="https://pkg.go.dev/github.com/memodb-io/memobase/src/client/memobase-go">
      <img src="https://img.shields.io/badge/go-reference-blue?logo=go&logoColor=fff&style=flat&labelColor=2C2C2C&color=28CF8D" />
    </a>
    <a href="./src/mcp">
       <img src="https://img.shields.io/badge/MCP-Memobase-green">
    </a>
  </p>
  <p>
    <a href="https://github.com/memodb-io/memobase/actions/workflows/publish.yaml">
      <img src="https://github.com/memodb-io/memobase/actions/workflows/publish.yaml/badge.svg">
    </a>
        <a href="https://github.com/orgs/memodb-io/packages?repo_name=memobase">
    <img src="https://img.shields.io/github/v/tag/memodb-io/memobase">
    </a>
  </p>
  <p>
    <a href="https://app.memobase.io/playground">
       <img src="https://img.shields.io/badge/Memobase-Playground-blue">
    </a>
    <a href="https://discord.gg/YdgwU4d9NB">
      <img src="https://dcbadge.limes.pink/api/server/YdgwU4d9NB?style=flat">
    </a>
  </p>
</div>



## News

- 🚀 Meet [Acontext](https://github.com/memodb-io/Acontext), Context Data Platform that Improves your Agent with Experiences.





Memobase is a **user profile-based memory system** designed to bring long-term user memory to your LLM applications. Whether you're building virtual companions, educational tools, or personalized assistants, Memobase empowers your AI to **remember**,  **understand**, and **evolve** with your users.



Memobase offers the perfect balance for your product among various memory solutions. At Memobase, we focus on three key metrics simultaneously:

- **Performance**: Although Memobase is not specifically designed for RAG/search tasks, it still achieves top-tier search performance in the LOCOMO benchmark.
- **LLM Cost**: Memobase includes a built-in buffer for each user to batch-process their chats, allowing the overhead to be distributed efficiently. Additionally, we carefully design our prompts and workflows, ensuring there are no "agents" in the system that could lead to excessive costs.
- **Latency**: Memobase works similarly to the memory system behind ChatGPT: for each user, there is always a user profile and event timeline available. This allows you to access the most important memories of a user without any pre-processing, but only few SQL operations, keeping online latency under 100ms.



Check out the profile [result](./docs/experiments/900-chats/readme.md) (compared with [mem0](https://github.com/mem0ai/mem0)) from a 900-turns real-world chatting:

<details>
<summary>Partial Profile Output</summary>



```python
{
  "basic_info": {
    "language_spoken": ["English", "Korean"],
    "name": "오*영"
  },
  "demographics": {
    "marital_status": "married"
  },
  "education": {
    "notes": "Had an English teacher who emphasized capitalization rules during school days",
    "major": "국어국문학과 (Korean Language and Literature)"
  },
  "interest": {
    "games": "User is interested in Cyberpunk 2077 and wants to create a game better than it",
    "youtube_channels": "Kurzgesagt",
    ...
  },
  "psychological": {...},
  "work": {"working_industry": ..., "title": ..., },
  ...
}
```

</details>

## 🎉 Recent Updates
- `0.0.40`: we updated the internal workflows in Memobase, reducing the number of LLM calls in a single run from approximately 3-10 times to a fixed 3 times, which reduces token costs by approximately 40-50%. (Consider updating your Memobase version!)
- `0.0.37`: we added fine-grained event gist, enabling the detailed search on users' timeline. [Re-ran the LOCOMO benchmark](./docs/experiments/locomo-benchmark) and we're SOTA!
- `0.0.36`: we updated the search of `context` api, making the search take between 500~1000ms (depending on the embedding API you're using). Also, you can [pass a prompt template](https://docs.memobase.io/api-reference/prompt/get_context#parameter-customize-context-prompt) to the `context` api to pack memories directly into prompt.



## 📖 Table of Contents

- [Table of Contents](#table-of-contents)
- [Core Features](#core-features)
- [Get Started](#get-started)
- [Step-by-step breakdown](#step-by-step-breakdown)
  - [1. Make sure you're connected](#1-make-sure-youre-connected)
  - [2. Manage Users](#2-manage-users)
  - [3. Insert Data](#3-insert-data)
  - [4. Get your Memory](#4-get-your-memory)
  - [5. Integrate memory into your prompt](#5-integrate-memory-into-your-prompt)
- [What's next?](#whats-next)
- [Why/Where should I use Memobase?](#whywhere-should-i-use-memobase)
  - [Remember the users](#remember-the-users)
  - [User analysis and tracking](#user-analysis-and-tracking)
  - [Sell something to your customers.](#sell-something-to-your-customers)
- [Documentation](#documentation)
- [Stay Updated](#stay-updated)
- [Support](#support)
- [Contribute](#contribute)
- [License](#license)

## Core Features

**🎯 Memory for User, not Agent**

Define and control exactly what user information your AI captures. 

📈 **SOTA**

Check out performance on [public benchmark](./docs/experiments/locomo-benchmark) against mem0, langmem, zep...

📅 **Time-aware Memory**

Memobase has more than user profiles, it also records [user event](https://docs.memobase.io/features/event/event). User event is essential to answer time-related question, see how we can [improve temporal m

... (更多内容请访问上面 GitHub 链接)
```

