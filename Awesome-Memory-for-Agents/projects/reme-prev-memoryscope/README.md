# ReMe (prev. MemoryScope)

**收录日期:** 2025-12

**GitHub:** [https://github.com/modelscope/ReMe](https://github.com/modelscope/ReMe)
**Website:** [https://modelscope.github.io/ReMe/](https://modelscope.github.io/ReMe/)
**Paper:** [https://arxiv.org/abs/2512.10696](https://arxiv.org/abs/2512.10696)

## 简述

Remember Me, Refine Me: A Dynamic Procedural Memory Framework for Experience-Driven Agent Evolution

## GitHub README 摘要

> > Previous versions: [0.3.x](https://github.com/agentscope-ai/ReMe/tree/reme_v3) ·

## README 摘录（GitHub）

```markdown
<p align="center">
 <img src="docs/figure/reme_logo.png" alt="ReMe Logo" width="50%">
</p>

<p align="center">
  <a href="https://pypi.org/project/reme-ai/"><img src="https://img.shields.io/badge/python-3.11+-blue" alt="Python Version"></a>
  <a href="https://pypi.org/project/reme-ai/"><img src="https://img.shields.io/pypi/v/reme-ai.svg?logo=pypi" alt="PyPI Version"></a>
  <a href="https://pepy.tech/project/reme-ai/"><img src="https://img.shields.io/pypi/dm/reme-ai" alt="PyPI Downloads"></a>
  <a href="https://github.com/agentscope-ai/ReMe"><img src="https://img.shields.io/github/commit-activity/m/agentscope-ai/ReMe?style=flat-square" alt="GitHub commit activity"></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-Apache--2.0-black" alt="License"></a>
  <a href="./README.md"><img src="https://img.shields.io/badge/English-Click-yellow" alt="English"></a>
  <a href="./README_ZH.md"><img src="https://img.shields.io/badge/简体中文-点击查看-orange" alt="简体中文"></a>
  <a href="https://github.com/agentscope-ai/ReMe"><img src="https://img.shields.io/github/stars/agentscope-ai/ReMe?style=social" alt="GitHub Stars"></a>
  <a href="https://deepwiki.com/agentscope-ai/ReMe"><img src="https://img.shields.io/badge/DeepWiki-Ask_Devin-navy.svg" alt="DeepWiki"></a>
</p>

<p align="center">
<a href="https://trendshift.io/repositories/20528" target="_blank"><img src="https://trendshift.io/api/badge/repositories/20528" alt="agentscope-ai%2FReMe | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>
</p>

<p align="center">
  <strong>A memory management toolkit for AI agents — Remember Me, Refine Me.</strong><br>
</p>

> Previous versions: [0.3.x](https://github.com/agentscope-ai/ReMe/tree/reme_v3) ·
> [0.2.x](https://github.com/agentscope-ai/ReMe/tree/v0.2.0.6) ·
> [MemoryScope](https://github.com/agentscope-ai/ReMe/tree/memoryscope_branch)

🧠 ReMe is a memory management toolkit for **AI agents**. It turns conversations and resources into readable, editable,
and searchable file-based long-term memory.

## ✨ Core Ideas

- **Memory as File**: Markdown files with frontmatter and wikilinks serve as memory nodes that both users and agents can
  read and write directly.
- **Self-evolving knowledge base**: Auto Memory, Auto Resource, and Auto Dream progressively transform conversations and
  resources into long-term memories, while automatically building wikilink relationships.
- **Progressive hybrid search**: ReMe combines wikilinks, BM25, and embeddings for hybrid retrieval across keyword
  matching, semantic recall, and relationship expansion.
- **Agent-friendly integration**: SKILL.md + CLI integration makes it easy for different agents to read, write,
  maintain, and reuse memory.

<p align="center">
  <img src="docs/figure/design-philosophy.svg" alt="ReMe Design Philosophy" width="92%">
</p>

<details>
<summary><b>Use Cases</b></summary>

<br>

- **Personal assistants**: Provide long-term memory for agents such
  as [QwenPaw](https://github.com/agentscope-ai/QwenPaw).
- **Coding assistants**: Preserve coding style, project background, and workflow experience across sessions.
- **Knowledge QA**: Progressively transform resources and conversations into a searchable, traceable, and linked
  Markdown knowledge base.
- **Task automation**: Reuse successful paths, lessons from failures, and operating procedures from past tasks.

</details>

## 📰 News

- Our paper [Remember Me, Refine Me: A Dynamic Procedural Memory Framework for Experience-Driven Agent Evolution](https://aclanthology.org/2026.findings-acl.829/) has been accepted to Findings of ACL 2026.

## 🚀 Quick Start

### Installation

ReMe requires Python 3.11+.

Install from pip:

```bash
pip install "reme-ai[core]"
```

Install from source:

```bash
git clone https://github.com/agentscope-ai/ReMe.git
cd ReMe
pip install -e ".[core]"
```

### Environment Variables

Configure environment variables:

```bash
cat > .env <<'EOF'
EMBEDDING_API_KEY=sk-xxx
EMBEDDING_BASE_URL=https://dashscope.aliyuncs.com/compatible-mode/v1
LLM_API_KEY=sk-xxx
LLM_BASE_URL=https://dashscope.aliyuncs.com/compatible-mode/v1
EOF
```

### Start the Service

```bash
reme start
```

The default service address is `127.0.0.1:2333`. If the port is occupied, specify another port:

```bash
reme start service.port=8181
# reme start workspace_dir=/tmp/reme-demo service.port=8181
```

After startup, check the service status. If you use a custom port, replace `2333` in the URL below with that port.

```bash
reme version
curl -s http://127.0.0.1:2333/version -H 'Content-Type: application/json' -d '{}'
```

### Agent Integration

ReMe runs as a service and exposes memory through CLI / MCP jobs. Agents can adopt it in whichever way fits them: deep
SDK integration, plugin integration, or a lightweight Skill + CLI integration. They can wire `auto_memory` / `proactive`
into their lifecycle so conversations are consolidated into memory and surfaced at the right time. Indexing (
`auto_index`) and resource processing (`auto_resource`) run automatically through file watching, and `auto_dream`
consolidates daily memories into long-term digests on a schedule.

<p align="center"><b>QwenPaw Auto Memory / Auto Dream demo</b></p>

<table>
  <tr>
    <td width="50%" align="center"><b>Auto Memory</b></td>
    <td width="50%" align="center"><b>Auto Dream</b></td>
  </tr>
  <tr>
    <td width="50%">
      <img src="docs/figure/qwenpaw-auto-memory.gif" alt="QwenPaw Auto Memory demo" width="100%">
    </td>
    <td width="50%">
      <img src="docs/figure/qwenpaw-auto-dream.gif" alt="QwenPaw Auto Dream demo" width="100%">
    </td>
  </tr>
</table>

Integration status across agents:

| Agent                                               | Status      | How it integrates                                                                                                                                                                                                                        

... (更多内容请访问上面 GitHub 链接)
```

