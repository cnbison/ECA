# Human-inspired Episodic Memory for Infinite Context LLMs

**arXiv:** [2407.09450](https://arxiv.org/abs/2407.09450)
**PDF:** [下载](https://arxiv.org/pdf/2407.09450) · 本地: `2407.09450.pdf`
**作者:** Fountas, Zafeirios, Benfeghoul, Martin A, Oomerjee, Adnan, Christopoulou, Fenia, Lampouras, Gerasimos, Bou-Ammar, Haitham, Wang, Jun
**日期:** 2024/07/12

## Abstract

Large language models (LLMs) have shown remarkable capabilities, but still struggle with processing extensive contexts, limiting their ability to maintain coherence and accuracy over long sequences. In contrast, the human brain excels at organising and retrieving episodic experiences across vast temporal scales, spanning a lifetime. In this work, we introduce EM-LLM, a novel approach that integrates key aspects of human episodic memory and event cognition into LLMs with no fine-tuning, enabling them to handle practically infinite context lengths while maintaining computational efficiency. EM-LLM organises sequences of tokens into coherent episodic events using a combination of Bayesian surprise and graph-theoretic boundary refinement in an online fashion. When needed, these events are retrieved through a two-stage memory process, combining similarity-based and temporally contiguous retrieval for efficient, human-inspired access to relevant information. Experiments on the LongBench and $\infty$-Bench benchmarks demonstrate EM-LLM's superior performance, consistently outperforming the state-of-the-art retrieval model InfLLM across various baseline LLMs. In addition, EM-LLM outperforms its popular counterpart, RAG, in a wide range of tasks, while requiring similar resources. Notably, EM-LLM's performance even surpasses full-context models in most tasks, while successfully performing retrieval across 10 million tokens -- a scale computationally infeasible for such models. Finally, our analysis reveals strong correlations between EM-LLM's event segmentation and human-perceived events, suggesting parallels between this artificial system and its biological counterpart, thereby offering a novel computational framework for exploring human memory mechanisms.

## 文件

- `2407.09450.pdf` — 论文原文
- `meta.json` — 结构化元数据
