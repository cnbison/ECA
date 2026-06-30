# MemSearcher: Training LLMs to Reason, Search and Manage Memory via End-to-End Reinforcement Learning

**arXiv:** [2511.02805](https://arxiv.org/abs/2511.02805)
**PDF:** [下载](https://arxiv.org/pdf/2511.02805) · 本地: `2511.02805.pdf`
**作者:** Yuan, Qianhao, Lou, Jie, Li, Zichao, Chen, Jiawei, Lu, Yaojie, Lin, Hongyu, Sun, Le, Zhang, Debing, Han, Xianpei
**日期:** 2025/11/04

## Abstract

LLM-based search agents often concatenate the full interaction history into the context, producing long and noisy inputs, and increasing compute cost and GPU memory overhead. To address this issue, we propose MemSearcher, an agent framework that maintains a compact memory during multi-turn interactions, retaining only question-relevant information and thereby keeping the context length stable across turns. Training MemSearcher is challenging because each trajectory spans multiple turns under different LLM contexts, making each turn an independent optimization target in reinforcement learning. We introduce multi-context GRPO, which propagates trajectory-level advantages to all turns for end-to-end optimization. Experiments demonstrate that MemSearcher outperforms strong history-concatenation (ReAct-style) baselines on a range of public datasets while maintaining nearly constant token counts across multi-turn interactions. The code and models will be publicly available at https://github.com/icip-cas/MemSearcher

## 文件

- `2511.02805.pdf` — 论文原文
- `meta.json` — 结构化元数据
