# Sculptor: Empowering LLMs with Cognitive Agency via Active Context Management

**arXiv:** [2508.04664](https://arxiv.org/abs/2508.04664)
**PDF:** [下载](https://arxiv.org/pdf/2508.04664) · 本地: `2508.04664.pdf`
**作者:** Li, Mo, Xu, L. H., Tan, Qitai, Ma, Long, Cao, Ting, Liu, Yunxin
**日期:** 2025/08/06

## Abstract

Large Language Models (LLMs) suffer from significant performance degradation when processing long contexts due to proactive interference, where irrelevant information in earlier parts of the context disrupts reasoning and memory recall. While most research focuses on external memory systems to augment LLMs' capabilities, we propose a complementary approach: empowering LLMs with Active Context Management (ACM) tools to actively sculpt their internal working memory. We introduce Sculptor, a framework that equips LLMs with three categories of tools: (1) context fragmentation, (2) summary, hide, and restore, and (3) precise search. Our approach enables LLMs to proactively manage their attention and working memory, analogous to how humans selectively focus on relevant information while filtering out distractions. Experimental evaluation on diverse long-context benchmarks demonstrates that Sculptor significantly improves performance even without specific training, leveraging LLMs' inherent tool-calling and instruction-following capabilities. To further optimize these strategies, we introduce a novel dynamic context-aware reinforcement learning (RL) approach, advancing the training of an agent that actively modifies its own conversational history. By enabling Active Context Management, Sculptor not only mitigates proactive interference but also provides a cognitive foundation for more reliable reasoning across diverse long-context tasks-highlighting that explicit context-control strategies, rather than merely larger token windows, are key to robustness at scale.

## 文件

- `2508.04664.pdf` — 论文原文
- `meta.json` — 结构化元数据
