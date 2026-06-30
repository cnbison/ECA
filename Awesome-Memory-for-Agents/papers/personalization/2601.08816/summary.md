# MemRec: Collaborative Memory-Augmented Agentic Recommender System

**arXiv:** [2601.08816](https://arxiv.org/abs/2601.08816)
**PDF:** [下载](https://arxiv.org/pdf/2601.08816) · 本地: `2601.08816.pdf`
**作者:** Chen, Weixin, Zhao, Yuhan, Huang, Jingyuan, Ye, Zihe, Ju, Clark Mingxuan, Zhao, Tong, Shah, Neil, Chen, Li, Zhang, Yongfeng
**日期:** 2026/01/13

## Abstract

The evolution of recommender systems has shifted from traditional collaborative filtering to LLM-based agentic systems, which rely on semantic user and item memories to make predictions. However, existing agents maintain these memories in isolation. This overlooks crucial collaborative signals, such as user-item co-engagements and peer relationships across the community, which significantly limits their ability to uncover hidden preferences and accurately infer user needs, particularly for data-sparse users. To bridge this gap, we introduce collaborative memory, a paradigm that connects isolated semantics to enable the sharing of relational insights. Yet, naively utilizing collaborative memory causes severe context overload and introduces noise to downstream LLMs, alongside prohibitive computational costs. To resolve this, we propose MemRec, a framework that architecturally decouples memory management from reasoning. MemRec introduces a dedicated, lightweight language model (LM_Mem) to efficiently manage and synthesize a dynamic collaborative memory graph in the background. It provides only distilled, high-signal contexts to a downstream, heavyweight large language model (LLM_Rec) for the final recommendation. Extensive experiments on four benchmarks demonstrate that MemRec achieves state-of-the-art performance. Code: this https URL and Homepage: this https URL

## 文件

- `2601.08816.pdf` — 论文原文
- `meta.json` — 结构化元数据
