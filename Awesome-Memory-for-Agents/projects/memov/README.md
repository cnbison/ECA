# MemoV

**收录日期:** 未知

**GitHub:** [https://github.com/memovai/memov](https://github.com/memovai/memov)
**Website:** [https://www.memov.ai/](https://www.memov.ai/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> MemoV is a memory layer for AI coding agents that provides **traceable**, **Git-powered** version control for prompts, context, and code diffs. It enables **VibeGit** - automatic versioning of AI coding sessions with branch exploration, rollback capabilities, and **zero pollution** to the standard .

## README 摘录（GitHub）

```markdown
<p align="center">
  <a href="https://github.com/memovai/memov">
    <img src="docs/images/memov-banner.png" width="800px" alt="MemoV - The Memory Layer for AI Coding Agents">
  </a>
</p>

<p align="center">
  <b>English</b> | <a href="docs/readme/README_DE.md">Deutsch</a> | <a href="docs/readme/README_ES.md">Español</a> | <a href="docs/readme/README_FR.md">Français</a> | <a href="docs/readme/README_JA.md">日本語</a> | <a href="docs/readme/README_KO.md">한국어</a> | <a href="docs/readme/README_PT.md">Português</a> | <a href="docs/readme/README_RU.md">Русский</a> | <a href="docs/readme/README_CN.md">中文</a>
</p>

<h4 align="center">VibeGit🤌: Auto-trace your prompts, context & code diffs.</h4>

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-7289da?logo=discord&logoColor=white)](https://discord.gg/un54aD7Hug)
[![DeepWiki](https://img.shields.io/badge/DeepWiki-memovai%2Fmemov-blue.svg?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIj48cGF0aCBkPSJNNCAxOWguNmMuNC0uMi44LS41IDEuMi0uOCAyLjItMS42IDMuNy0zLjggNC4yLTYuMyIvPjxwYXRoIGQ9Ik0xNC42IDEyLjFjLjYtLjkgMS4zLTEuOCAyLjEtMi42IDEuMS0xLjEgMi40LTEuOCAzLjgtMi4yIDEuMS0uMyAyLjItLjQgMy4zLS4zIi8+PHBhdGggZD0iTTE5LjQgNS4yYy0uOC4xLTEuNi4zLTIuMy41LS41LjItLjkuNC0xLjQuNy0uNC4zLS44LjYtMS4xIDEiLz48cGF0aCBkPSJNNiAxOGMtMS44IDAtMy0xLjUtMy0zIDAtMi4yIDEuOS0zLjUgMi44LTUgLjUtLjggMS45LTIuNyAyLjMtMy43LjYtMS4yIDEuMi0yLjQgMS42LTMuNi4xLS40LjUtLjkuOS0uOS43IDAgLjggMS4yLjggMS4zIDAgMS40LS4zIDIuOC0uNyA0LjEtLjQgMS41LTEuMSAyLjktMS44IDQuMyIvPjwvc3ZnPg==)](https://deepwiki.com/memovai/memov)
[![Twitter Follow](https://img.shields.io/twitter/follow/ssslvky?style=social)](https://x.com/ssslvky)

</div>

MemoV is a memory layer for AI coding agents that provides **traceable**, **Git-powered** version control for prompts, context, and code diffs. It enables **VibeGit** - automatic versioning of AI coding sessions with branch exploration, rollback capabilities, and **zero pollution** to the standard .git repository.

<div align="center">

| MemoV | Checkpoints |
|-------|-------------|
| Branch exploration | Linear timeline |
| Cross-session | Session-bound |
| Rollback preserves all | Rollback erases history |
| Every jump tracked | No trajectory |

</div>

<!-- <p align="center">
  <img src="docs/images/readme.gif" alt="MemoV Demo" width="800px">
</p> -->


![MemoV Time](docs/images/ALL.png)
- 💬 [Join our Discord](https://discord.gg/un54aD7Hug) and dive into smarter vibe engineering

<!-- <div align="center">

[![Add to VS Code](https://img.shields.io/badge/Add%20to%20VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://memov.ai/set-mcp)
[![Add to Cursor](https://img.shields.io/badge/Add%20to%20CURSOR-000000?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://memov.ai/set-mcp)

</div> -->

## Features

- **One-click MCP**: Works with any AI coding agent
- **VibeGit for Agents**: Auto-trace prompts, context, and code diffs before git commits
- **Version Control**: Branch, rollback, replay any interaction
- **Keep Git Clean**: Shadow `.mem` timeline, files as context, zero pollution on `.git` 
- **Visual UI**: Say "mem ui" in chat, and view at http://localhost:38888
- **Private-first** — Local, no database, no overhead. Use .memignore to exclude

![MemoV Time](docs/images/one.png)

## Quick Start (MCP Installation)

### Prerequisites

Install `uv` first:

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Install Git (if not installed)
winget install --id Git.Git -e --source winget
```

### Claude Code

Run in your project root directory:

```bash
claude mcp add mem-mcp --scope project -- uvx --from git+https://github.com/memovai/memov.git mem-mcp-launcher stdio $(pwd)
```

### Codex

Run in your project root directory:

```bash
codex mcp add mem-mcp -- uvx --from git+https://github.com/memovai/memov.git mem-mcp-launcher stdio $(pwd)
```

<details>
<summary><b>VS Code</b></summary>

Create `.vscode/mcp.json` in your project root:

```json
{
  "servers": {
    "mem-mcp": {
      "type": "stdio",
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/memovai/memov.git",
        "mem-mcp-launcher",
        "stdio",
        "${workspaceFolder}"
      ]
    }
  }
}
```

</details>

<details>
<summary><b>Cursor</b></summary>

Go to **Files > Preferences > Cursor Settings > MCP**, then add:

```json
{
  "mcpServers": {
    "mem-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/memovai/memov.git",
        "mem-mcp-launcher",
        "stdio",
        "${workspaceFolder}"
      ]
    }
  }
}
```

</details>

<details>
<summary><b>Antigravity</b></summary>

> **Note:** Antigravity does not support `"${workspaceFolder}"` variable. Please manually enter the absolute path to your project directory.

Go to **Settings > MCP**, then add:

```json
{
  "mcpServers": {
    "mem-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/memovai/memov.git",
        "mem-mcp-launcher",
        "stdio",
        "/absolute/path/to/your/project"
      ]
    }
  }
}
```

Replace `/absolute/path/to/your/project` with the actual absolute path to your project directory (e.g., `/Users/username/projects/my-project` on macOS/Linux or `C:\\Users\\username\\projects\\my-project` on Windows).

</details>

<details>
<summary><b>With VectorDB (RAG mode)</b> 🚧 WIP</summary>

To enable semantic search, validation, and debugging tools, install with `[rag]` extras:

**Claude Code:**
```bash
claud

... (更多内容请访问上面 GitHub 链接)
```

