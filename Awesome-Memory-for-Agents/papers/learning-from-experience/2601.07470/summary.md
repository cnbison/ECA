# Learning How to Remember: A Meta-Cognitive Management Method for Structured and Transferable Agent Memory

**arXiv:** [2601.07470](https://arxiv.org/abs/2601.07470)
**PDF:** [下载](https://arxiv.org/pdf/2601.07470) · 本地: `2601.07470.pdf`
**作者:** Liang, Sirui, Cao, Pengfei, Zhao, Jian, Teng, Wenhao, Liao, Xiangwen, Zhao, Jun, Liu, Kang
**日期:** 2026/01/12

## Abstract

Large language model (LLM) agents increasingly rely on accumulated memory to solve long-horizon decision-making tasks. However, most existing approaches store memory in fixed representations and reuse it at a single or implicit level of abstraction, which limits generalization and often leads to negative transfer when distribution shift. This paper proposes the Meta-Cognitive Memory Abstraction method (MCMA), which treats memory abstraction as a learnable cognitive skill rather than a fixed design choice. MCMA decouples task execution from memory management by combining a frozen task model with a learned memory copilot. The memory copilot is trained using direct preference optimization, it determines how memories should be structured, abstracted, and reused. Memories are further organized into a hierarchy of abstraction levels, enabling selective reuse based on task similarity. When no memory is transferable, MCMA transfers the ability to abstract and manage memory by transferring the memory copilot. Experiments on ALFWorld, ScienceWorld, and BabyAI demonstrate substantial improvements in performance, out-of-distribution generalization, and cross-task transfer over several baselines.

## 文件

- `2601.07470.pdf` — 论文原文
- `meta.json` — 结构化元数据
