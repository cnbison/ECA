# M+: Extending MemoryLLM with Scalable Long-Term Memory

**arXiv:** [2502.00592](https://arxiv.org/abs/2502.00592)
**PDF:** [下载](https://arxiv.org/pdf/2502.00592) · 本地: `2502.00592.pdf`
**作者:** Wang, Yu, Krotov, Dmitry, Hu, Yuanzhe, Gao, Yifan, Zhou, Wangchunshu, McAuley, Julian, Gutfreund, Dan, Feris, Rogerio, He, Zexue
**日期:** 2025/02/01

## Abstract

Equipping large language models (LLMs) with latent-space memory has attracted increasing attention as they can extend the context window of existing language models. However, retaining information from the distant past remains a challenge. For example, MemoryLLM (Wang et al., 2024a), as a representative work with latent-space memory, compresses past information into hidden states across all layers, forming a memory pool of 1B parameters. While effective for sequence lengths up to 16k tokens, it struggles to retain knowledge beyond 20k tokens. In this work, we address this limitation by introducing M+, a memory-augmented model based on MemoryLLM that significantly enhances long-term information retention. M+ integrates a long-term memory mechanism with a co-trained retriever, dynamically retrieving relevant information during text generation. We evaluate M+ on diverse benchmarks, including long-context understanding and knowledge retention tasks. Experimental results show that M+ significantly outperforms MemoryLLM and recent strong baselines, extending knowledge retention from under 20k to over 160k tokens with similar GPU memory overhead. We open-source our code at this https URL

## 文件

- `2502.00592.pdf` — 论文原文
- `meta.json` — 结构化元数据
