# Hierarchical Memory for High-Efficiency Long-Term Reasoning in LLM Agents

**arXiv:** [2507.22925](https://arxiv.org/abs/2507.22925)
**PDF:** [下载](https://arxiv.org/pdf/2507.22925) · 本地: `2507.22925.pdf`
**作者:** Sun, Haoran, Zeng, Shaoning
**日期:** 2025/07/23

## Abstract

Long-term memory is one of the key factors influencing the reasoning capabilities of Large Language Model Agents (LLM Agents). Incorporating a memory mechanism that effectively integrates past interactions can significantly enhance decision-making and contextual coherence of LLM Agents. While recent works have made progress in memory storage and retrieval, such as encoding memory into dense vectors for similarity-based search or organizing knowledge in the form of graph, these approaches often fall short in structured memory organization and efficient retrieval. To address these limitations, we propose a Hierarchical Memory (H-MEM) architecture for LLM Agents that organizes and updates memory in a multi-level fashion based on the degree of semantic abstraction. Each memory vector is embedded with a positional index encoding pointing to its semantically related sub-memories in the next layer. During the reasoning phase, an index-based routing mechanism enables efficient, layer-by-layer retrieval without performing exhaustive similarity computations. We evaluate our method on five task settings from the LoCoMo dataset. Experimental results show that our approach consistently outperforms five baseline methods, demonstrating its effectiveness in long-term dialogue scenarios.

## 文件

- `2507.22925.pdf` — 论文原文
- `meta.json` — 结构化元数据
