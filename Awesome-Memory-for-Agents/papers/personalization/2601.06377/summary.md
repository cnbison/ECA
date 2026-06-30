# HiMem: Hierarchical Long-Term Memory for LLM Long-Horizon Agents

**arXiv:** [2601.06377](https://arxiv.org/abs/2601.06377)
**PDF:** [下载](https://arxiv.org/pdf/2601.06377) · 本地: `2601.06377.pdf`
**作者:** Zhang, Ningning, Yang, Xingxing, Tan, Zhizhong, Deng, Weiping, Wang, Wenyong
**日期:** 2026/01/10

## Abstract

Although long-term memory systems have made substantial progress in recent years, they still exhibit clear limitations in adaptability, scalability, and self-evolution under continuous interaction settings. Inspired by cognitive theories, we propose HiMem, a hierarchical long-term memory framework for long-horizon dialogues, designed to support memory construction, retrieval, and dynamic updating during sustained interactions. HiMem constructs cognitively consistent Episode Memory via a Topic-Aware Event--Surprise Dual-Channel Segmentation strategy, and builds Note Memory that captures stable knowledge through a multi-stage information extraction pipeline. These two memory types are semantically linked to form a hierarchical structure that bridges concrete interaction events and abstract knowledge, enabling efficient retrieval without sacrificing information fidelity. HiMem supports both hybrid and best-effort retrieval strategies to balance accuracy and efficiency, and incorporates conflict-aware Memory Reconsolidation to revise and supplement stored knowledge based on retrieval feedback. This design enables continual memory self-evolution over long-term use. Experimental results on long-horizon dialogue benchmarks demonstrate that HiMem consistently outperforms representative baselines in accuracy, consistency, and long-term reasoning, while maintaining favorable efficiency. Overall, HiMem provides a principled and scalable design paradigm for building adaptive and self-evolving LLM-based conversational agents. The code is available at this https URL.

## 文件

- `2601.06377.pdf` — 论文原文
- `meta.json` — 结构化元数据
