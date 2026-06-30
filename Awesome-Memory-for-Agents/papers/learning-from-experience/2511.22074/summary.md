# Real-Time Procedural Learning From Experience for AI Agents

**arXiv:** [2511.22074](https://arxiv.org/abs/2511.22074)
**PDF:** [下载](https://arxiv.org/pdf/2511.22074) · 本地: `2511.22074.pdf`
**作者:** Bi, Dasheng, Hu, Yubin, Nasir, Mohammed N.
**日期:** 2025/11/27

## Abstract

Learning how to do things from trial and error in real time is a hallmark of biological intelligence, yet most LLM-based agents lack mechanisms to acquire procedural knowledge after deployment. We propose Procedural Recall for Agents with eXperiences Indexed by State (PRAXIS), a lightweight post-training learning mechanism that stores the consequences of actions and retrieves them by jointly matching environmental and internal states of past episodes to the current state. PRAXIS augments agentic action selection with retrieved state-action-result exemplars that are generated in real time. When evaluated on the REAL web browsing benchmark, PRAXIS improves task completion accuracy, reliability, and cost efficiency across different foundation model backbones, and shows preliminary generalization to unseen tasks in similar environments. These results demonstrate that PRAXIS enables the practical adoption of AI agents in fast-evolving stateful environments by helping them learn new procedures effectively.

## 文件

- `2511.22074.pdf` — 论文原文
- `meta.json` — 结构化元数据
