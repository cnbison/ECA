# MAGMA: A Multi-Graph based Agentic Memory Architecture for AI Agents

**arXiv:** [2601.03236](https://arxiv.org/abs/2601.03236)
**PDF:** [下载](https://arxiv.org/pdf/2601.03236) · 本地: `2601.03236.pdf`
**作者:** Jiang, Dongming, Li, Yi, Li, Guanpeng, Li, Bingzhe
**日期:** 2026/01/06

## Abstract

Memory-Augmented Generation (MAG) extends Large Language Models with external memory to support long-context reasoning, but existing approaches largely rely on semantic similarity over monolithic memory stores, entangling temporal, causal, and entity information. This design limits interpretability and alignment between query intent and retrieved evidence, leading to suboptimal reasoning accuracy. In this paper, we propose MAGMA, a multi-graph agentic memory architecture that represents each memory item across orthogonal semantic, temporal, causal, and entity graphs. MAGMA formulates retrieval as policy-guided traversal over these relational views, enabling query-adaptive selection and structured context construction. By decoupling memory representation from retrieval logic, MAGMA provides transparent reasoning paths and fine-grained control over retrieval. Experiments on LoCoMo and LongMemEval demonstrate that MAGMA consistently outperforms state-of-the-art agentic memory systems in long-horizon reasoning tasks.

## 文件

- `2601.03236.pdf` — 论文原文
- `meta.json` — 结构化元数据
