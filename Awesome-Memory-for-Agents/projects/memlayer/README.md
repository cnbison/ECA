# Memlayer

**收录日期:** 未知

**GitHub:** [https://github.com/divagr18/memlayer](https://github.com/divagr18/memlayer)
**Website:** [https://divagr18.github.io/memlayer/](https://divagr18.github.io/memlayer/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> **The plug-and-play memory layer for smart, contextual agents**

## README 摘录（GitHub）

```markdown
<div align="center">

# Memlayer

**The plug-and-play memory layer for smart, contextual agents**

Memlayer adds persistent, intelligent memory to any LLM in just 3 lines of code, enabling agents that recall context across conversations, extract structured knowledge, and surface relevant information when it matters.

**<100ms Fast Search • Noise-Aware Memory Gate • Multi-Tier Retrieval Modes • 100% Local • Zero Config**


[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PyPI version](https://img.shields.io/pypi/v/memlayer.svg)](https://pypi.org/project/memlayer/)

[Quick Start](#quick-start) • [Documentation](https://divagr18.github.io/memlayer/) • [Examples](https://github.com/divagr18/memlayer/tree/main/examples) • [Twitter](https://x.com/getmemlayer)




</div>

<br/>

<p align="center">
  <img src="./memlayer.png" alt="Memlayer Overview" width="700">
</p>

<br/>

## Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [Key Concepts](#key-concepts)
- [Memory Modes](#memory-modes)
- [Search Tiers](#search-tiers)
- [Providers](#providers)
- [Advanced Features](#advanced-features)
- [Examples](#examples)
- [Performance](#performance)
- [Documentation](#documentation)
- [Contributing](#contributing)

##  Features

- **Universal LLM Support**: Works with OpenAI, Claude, Gemini, Ollama models
- **Plug-and-play**: Install with `pip install memlayer` and get started in minutes — minimal setup required.
- **Intelligent Memory Filtering**: Three operation modes (LOCAL/ONLINE/LIGHTWEIGHT) automatically filter important information
- **Hybrid Search**: Combines vector similarity + knowledge graph traversal for accurate retrieval
- **Three Search Tiers**: Fast (<100ms), Balanced (<500ms), Deep (<2s) optimized for different use cases
- **Knowledge Graph**: Automatically extracts entities, relationships, and facts from conversations
- **Proactive Reminders**: Schedule tasks and get automatic reminders when they're due
- **Built-in Observability**: Trace every search operation with detailed performance metrics
- **Flexible Storage**: ChromaDB (vector) + NetworkX (graph) or graph-only mode
- **Production Ready**: Serverless-friendly with fast cold starts using online mode

##  Quick Start

### Installation

```bash
pip install memlayer
```

### Basic Usage

```python
from memlayer import OpenAI

# Initialize with memory capabilities
client = OpenAI(
    model="gpt-4.1-mini",
    storage_path="./memories",
    user_id="user_123"
)

# Store information automatically
client.chat([
    {"role": "user", "content": "My name is Alice and I work at TechCorp"}
])

# Retrieve information automatically (no manual prompting needed!)
response = client.chat([
    {"role": "user", "content": "Where do I work?"}
])
# Response: "You work at TechCorp."
```

That's it! Memlayer automatically:
1. ✅ Filters salient information using ML-based classification
2. ✅ Extracts structured facts, entities, and relationships
3. ✅ Stores memories in hybrid vector + graph storage
4. ✅ Retrieves relevant context for each query
5. ✅ Injects memories seamlessly into LLM context

##  Key Concepts

### Salience Filtering
Not all conversation content is worth storing. Memlayer uses **salience gates** to intelligently filter:
- ✅ **Save**: Facts, preferences, user info, decisions, relationships
- ❌ **Skip**: Greetings, acknowledgments, filler words, meta-conversation

### Hybrid Storage
Memories are stored in two complementary systems:
- **Vector Store (ChromaDB)**: Semantic similarity search for facts
- **Knowledge Graph (NetworkX)**: Entity relationships and structured knowledge

### Automatic Consolidation
After each conversation, background threads:
1. Extract facts, entities, and relationships using LLM
2. Store facts in vector database with embeddings
3. Build knowledge graph with entities and relationships
4. Index everything for fast retrieval

##  Memory Modes

Memlayer offers three modes that control both **memory filtering (salience)** and **storage**:

### 1. LOCAL Mode (Default)
```python
client = Ollama(operation_mode="local")
```
- **Filtering**: Sentence-transformers ML model (high accuracy)
- **Storage**: ChromaDB (vector) + NetworkX (graph)
- **Startup**: ~10s (model loading)
- **Best for**: High-volume production, offline apps
- **Cost**: Free (no API calls)

### 2. ONLINE Mode (Default)
```python
client = OpenAI(operation_mode="online")
```
- **Filtering**: OpenAI embeddings API (high accuracy)
- **Storage**: ChromaDB (vector) + NetworkX (graph)
- **Startup**: ~2s (no model loading!)
- **Best for**: Serverless, cloud functions, fast cold starts
- **Cost**: ~$0.0001 per operation

### 3. LIGHTWEIGHT Mode
```python
client = OpenAI(operation_mode="lightweight")
```
- **Filtering**: Keyword-based (medium accuracy)
- **Storage**: NetworkX only (no vector storage!)
- **Startup**: <1s (instant)
- **Best for**: Prototyping, testing, low-resource environments
- **Cost**: Free (no embeddings at all)

**Performance Comparison:**
```
Mode          Startup Time    Accuracy    API Cost    Storage
──────────────────────────────────────────────────────────────
LOCAL         ~10s            High        Free        Vector+Graph
ONLINE        ~2s             High        $0.0001/op  Vector+Graph  
LIGHTWEIGHT   <1s             Medium      Free        Graph-only
```

##  Search Tiers

Memlayer provides three search tiers optimized for different latency requirements:

### Fast Tier (<100ms)
```python
# Automatic - LLM chooses based on query complexity
response = client.chat([{"role": "user", "content": "What's my name?"}])
```
- 2 vector search results
- No graph traversal
- Perfect for: Real-time chat, simple factual recall

### Balanced Tier (<500ms)  DEFAULT
```python
# Automatic - handles most queries well
response = client.chat([{"role": "user", "content": "Tell me about my projects"}])
`

... (更多内容请访问上面 GitHub 链接)
```

