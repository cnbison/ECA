# CAM: A Constructivist View of Agentic Memory for LLM-Based Reading Comprehension

**arXiv:** [2510.05520](https://arxiv.org/abs/2510.05520)
**PDF:** [下载](https://arxiv.org/pdf/2510.05520) · 本地: `2510.05520.pdf`
**作者:** Li, Rui, Zhang, Zeyu, Bo, Xiaohe, Tian, Zihang, Chen, Xu, Dai, Quanyu, Dong, Zhenhua, Tang, Ruiming
**日期:** 2025/10/07

## Abstract

Current Large Language Models (LLMs) are confronted with overwhelming information volume when comprehending long-form documents. This challenge raises the imperative of a cohesive memory module, which can elevate vanilla LLMs into autonomous reading agents. Despite the emergence of some heuristic approaches, a systematic design principle remains absent. To fill this void, we draw inspiration from Jean Piaget's Constructivist Theory, illuminating three traits of the agentic memory -- structured schemata, flexible assimilation, and dynamic accommodation. This blueprint forges a clear path toward a more robust and efficient memory system for LLM-based reading comprehension. To this end, we develop CAM, a prototype implementation of Constructivist Agentic Memory that simultaneously embodies the structurality, flexibility, and dynamicity. At its core, CAM is endowed with an incremental overlapping clustering algorithm for structured memory development, supporting both coherent hierarchical summarization and online batch integration. During inference, CAM adaptively explores the memory structure to activate query-relevant information for contextual response, akin to the human associative process. Compared to existing approaches, our design demonstrates dual advantages in both performance and efficiency across diverse long-text reading comprehension tasks, including question answering, query-based summarization, and claim verification.

## 文件

- `2510.05520.pdf` — 论文原文
- `meta.json` — 结构化元数据
