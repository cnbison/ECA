# Memorization and Knowledge Injection in Gated LLMs

**arXiv:** [2504.21239](https://arxiv.org/abs/2504.21239)
**PDF:** [下载](https://arxiv.org/pdf/2504.21239) · 本地: `2504.21239.pdf`
**作者:** Pan, Xu, Hahami, Ely, Zhang, Zechen, Sompolinsky, Haim
**日期:** 2025/04/30

## Abstract

Large Language Models (LLMs) currently struggle to sequentially add new memories and integrate new knowledge. These limitations contrast with the human ability to continuously learn from new experiences and acquire knowledge throughout life. Most existing approaches add memories either through large context windows or external memory buffers (e.g., Retrieval-Augmented Generation), and studies on knowledge injection rarely test scenarios resembling everyday life events. In this work, we introduce a continual learning framework, Memory Embedded in Gated LLMs (MEGa), which injects event memories directly into the weights of LLMs. Each memory is stored in a dedicated set of gated low-rank weights. During inference, a gating mechanism activates relevant memory weights by matching query embeddings to stored memory embeddings. This enables the model to both recall entire memories and answer related questions. On two datasets - fictional characters and Wikipedia events - MEGa outperforms baseline approaches in mitigating catastrophic forgetting. Our model draws inspiration from the complementary memory system of the human brain.

## 文件

- `2504.21239.pdf` — 论文原文
- `meta.json` — 结构化元数据
