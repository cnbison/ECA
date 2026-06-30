# To Retrieve or To Think? An Agentic Approach for Context Evolution

**arXiv:** [2601.08747](https://arxiv.org/abs/2601.08747)
**PDF:** [下载](https://arxiv.org/pdf/2601.08747) · 本地: `2601.08747.pdf`
**作者:** Chen, Rubing, Wang, Jian, Li, Wenjie, Wei, Xiao-Yong, Li, Qing
**日期:** 2026/01/13

## Abstract

Current context augmentation methods, such as retrieval-augmented generation, are essential for solving knowledge-intensive reasoning tasks. However, they typically adhere to a rigid, brute-force strategy that executes retrieval at every step. This indiscriminate approach not only incurs unnecessary computational costs but also degrades performance by saturating the context with irrelevant noise. To address these limitations, we introduce Agentic Context Evolution (ACE), a framework inspired by human metacognition that dynamically determines whether to seek new evidence or reason with existing knowledge. ACE employs a central orchestrator agent to make decisions strategically via majority voting. It aims to alternate between activating a retriever agent for external retrieval and a reasoner agent for internal analysis and refinement. By eliminating redundant retrieval steps, ACE maintains a concise and evolved context. Extensive experiments on challenging multi-hop QA benchmarks demonstrate that ACE significantly outperforms competitive baselines in accuracy while achieving efficient token consumption. Our work provides valuable insights into advancing context-evolved generation for complex, knowledge-intensive tasks.

## 文件

- `2601.08747.pdf` — 论文原文
- `meta.json` — 结构化元数据
