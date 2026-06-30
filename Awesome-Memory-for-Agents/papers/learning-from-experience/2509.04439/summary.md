# ArcMemo: Abstract Reasoning Composition with Lifelong LLM Memory

**arXiv:** [2509.04439](https://arxiv.org/abs/2509.04439)
**PDF:** [下载](https://arxiv.org/pdf/2509.04439) · 本地: `2509.04439.pdf`
**作者:** Ho, Matthew, Si, Chen, Feng, Zhaoxiang, Yu, Fangxu, Yang, Yichi, Liu, Zhijian, Hu, Zhiting, Qin, Lianhui
**日期:** 2025/09/04

## Abstract

While inference-time scaling enables LLMs to carry out increasingly long and capable reasoning traces, the patterns and insights uncovered during these traces are immediately discarded once the context window is reset for a new query. External memory is a natural way to persist these discoveries, and recent work has shown clear benefits for reasoning-intensive tasks. We see an opportunity to make such memories more broadly reusable and scalable by moving beyond instance-based memory entries (e.g. exact query/response pairs, or summaries tightly coupled with the original problem context) toward concept-level memory: reusable, modular abstractions distilled from solution traces and stored in natural language. For future queries, relevant concepts are selectively retrieved and integrated into the prompt, enabling test-time continual learning without weight updates. Our design introduces new strategies for abstracting takeaways from rollouts and retrieving entries for new queries, promoting reuse and allowing memory to expand with additional experiences. We evaluate on ARC-AGI, a benchmark that stresses compositional generalization and abstract reasoning, making it a natural fit for concept memory. Our method yields a 7.5% relative gain over a strong no-memory baseline with performance continuing to scale with inference compute. We find abstract concepts to be the most consistent memory design, outscoring the baseline at all tested inference compute scales. Moreover, dynamically updating memory during test-time outperforms fixed settings, supporting the hypothesis that accumulating and abstracting patterns enables further solutions in a form of self-improvement. Code is available at this https URL.

## 文件

- `2509.04439.pdf` — 论文原文
- `meta.json` — 结构化元数据
