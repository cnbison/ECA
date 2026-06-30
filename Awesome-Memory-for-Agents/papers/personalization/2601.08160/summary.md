# SwiftMem: Fast Agentic Memory via Query-aware Indexing

**arXiv:** [2601.08160](https://arxiv.org/abs/2601.08160)
**PDF:** [下载](https://arxiv.org/pdf/2601.08160) · 本地: `2601.08160.pdf`
**作者:** Tian, Anxin, Li, Yiming, Li, Xing, Zhen, Hui-Ling, Chen, Lei, Yu, Xianzhi, Dong, Zhenhua, Yuan, Mingxuan
**日期:** 2026/01/13

## Abstract

Agentic memory systems have become critical for enabling LLM agents to maintain long-term context and retrieve relevant information efficiently. However, existing memory frameworks suffer from a fundamental limitation: they perform exhaustive retrieval across the entire storage layer regardless of query characteristics. This brute-force approach creates severe latency bottlenecks as memory grows, hindering real-time agent interactions. We propose SwiftMem, a query-aware agentic memory system that achieves sub-linear retrieval through specialized indexing over temporal and semantic dimensions. Our temporal index enables logarithmic-time range queries for time-sensitive retrieval, while the semantic DAG-Tag index maps queries to relevant topics through hierarchical tag structures. To address memory fragmentation during growth, we introduce an embedding-tag co-consolidation mechanism that reorganizes storage based on semantic clusters to improve cache locality. Experiments on LoCoMo and LongMemEval benchmarks demonstrate that SwiftMem achieves 47$\times$ faster search compared to state-of-the-art baselines while maintaining competitive accuracy, enabling practical deployment of memory-augmented LLM agents.

## 文件

- `2601.08160.pdf` — 论文原文
- `meta.json` — 结构化元数据
