# From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs

**arXiv:** [2410.14052](https://arxiv.org/abs/2410.14052)
**PDF:** [下载](https://arxiv.org/pdf/2410.14052) · 本地: `2410.14052.pdf`
**作者:** Rezazadeh, Alireza, Li, Zichao, Wei, Wei, Bao, Yujia
**日期:** 2024/10/17

## Abstract

Recent advancements in large language models have significantly improved their context windows, yet challenges in effective long-term memory management remain. We introduce MemTree, an algorithm that leverages a dynamic, tree-structured memory representation to optimize the organization, retrieval, and integration of information, akin to human cognitive schemas. MemTree organizes memory hierarchically, with each node encapsulating aggregated textual content, corresponding semantic embeddings, and varying abstraction levels across the tree's depths. Our algorithm dynamically adapts this memory structure by computing and comparing semantic embeddings of new and existing information to enrich the model's context-awareness. This approach allows MemTree to handle complex reasoning and extended interactions more effectively than traditional memory augmentation methods, which often rely on flat lookup tables. Evaluations on benchmarks for multi-turn dialogue understanding and document question answering show that MemTree significantly enhances performance in scenarios that demand structured memory management.

## 文件

- `2410.14052.pdf` — 论文原文
- `meta.json` — 结构化元数据
