# Iterative Experience Refinement of Software-Developing Agents

**arXiv:** [2405.04219](https://arxiv.org/abs/2405.04219)
**PDF:** [下载](https://arxiv.org/pdf/2405.04219) · 本地: `2405.04219.pdf`
**作者:** Qian, Chen, Li, Jiahao, Dang, Yufan, Liu, Wei, Wang, YiFei, Xie, Zihao, Chen, Weize, Yang, Cheng, Zhang, Yingli, Liu, Zhiyuan, Sun, Maosong
**日期:** 2024/05/07

## Abstract

Autonomous agents powered by large language models (LLMs) show significant potential for achieving high autonomy in various scenarios such as software development. Recent research has shown that LLM agents can leverage past experiences to reduce errors and enhance efficiency. However, the static experience paradigm, reliant on a fixed collection of past experiences acquired heuristically, lacks iterative refinement and thus hampers agents&#39; adaptability. In this paper, we introduce the Iterative Experience Refinement framework, enabling LLM agents to refine experiences iteratively during task execution. We propose two fundamental patterns: the successive pattern, refining based on nearest experiences within a task batch, and the cumulative pattern, acquiring experiences across all previous task batches. Augmented with our heuristic experience elimination, the method prioritizes high-quality and frequently-used experiences, effectively managing the experience space and enhancing efficiency. Extensive experiments show that while the successive pattern may yield superior results, the cumulative pattern provides more stable performance. Moreover, experience elimination facilitates achieving better performance using just 11.54% of a high-quality subset.

## 文件

- `2405.04219.pdf` — 论文原文
- `meta.json` — 结构化元数据
