# CAMELoT: Towards Large Language Models with Training-Free Consolidated Associative Memory

**arXiv:** [2402.13449](https://arxiv.org/abs/2402.13449)
**PDF:** [下载](https://arxiv.org/pdf/2402.13449) · 本地: `2402.13449.pdf`
**作者:** He, Zexue, Karlinsky, Leonid, Kim, Donghyun, McAuley, Julian, Krotov, Dmitry, Feris, Rogerio
**日期:** 2024/02/21

## Abstract

Large Language Models (LLMs) struggle to handle long input sequences due to high memory and runtime costs. Memory-augmented models have emerged as a promising solution to this problem, but current methods are hindered by limited memory capacity and require costly re-training to integrate with a new LLM. In this work, we introduce an associative memory module which can be coupled to any pre-trained (frozen) attention-based LLM without re-training, enabling it to handle arbitrarily long input sequences. Unlike previous methods, our associative memory module consolidates representations of individual tokens into a non-parametric distribution model, dynamically managed by properly balancing the novelty and recency of the incoming data. By retrieving information from this consolidated associative memory, the base LLM can achieve significant (up to 29.7% on Arxiv) perplexity reduction in long-context modeling compared to other baselines evaluated on standard benchmarks. This architecture, which we call CAMELoT (Consolidated Associative Memory Enhanced Long Transformer), demonstrates superior performance even with a tiny context window of 128 tokens, and also enables improved in-context learning with a much larger set of demonstrations.

## 文件

- `2402.13449.pdf` — 论文原文
- `meta.json` — 结构化元数据
