# AtomMem : Learnable Dynamic Agentic Memory with Atomic Memory Operation

**arXiv:** [2601.08323](https://arxiv.org/abs/2601.08323)
**PDF:** [下载](https://arxiv.org/pdf/2601.08323) · 本地: `2601.08323.pdf`
**作者:** Huo, Yupeng, Lu, Yaxi, Zhang, Zhong, Chen, Haotian, Lin, Yankai
**日期:** 2026/01/13

## Abstract

Equipping agents with memory is essential for solving real-world long-horizon problems. However, most existing agent memory mechanisms rely on static and hand-crafted workflows. This limits the performance and generalization ability of these memory designs, which highlights the need for a more flexible, learning-based memory framework. In this paper, we propose AtomMem, which reframes memory management as a dynamic decision-making problem. We deconstruct high-level memory processes into fundamental atomic CRUD (Create, Read, Update, Delete) operations, transforming the memory workflow into a learnable decision process. By combining supervised fine-tuning with reinforcement learning, AtomMem learns an autonomous, task-aligned policy to orchestrate memory behaviors tailored to specific task demands. Experimental results across 3 long-context benchmarks demonstrate that the trained AtomMem-8B consistently outperforms prior static-workflow memory methods. Further analysis of training dynamics shows that our learning-based formulation enables the agent to discover structured, task-aligned memory management strategies, highlighting a key advantage over predefined routines.

## 文件

- `2601.08323.pdf` — 论文原文
- `meta.json` — 结构化元数据
