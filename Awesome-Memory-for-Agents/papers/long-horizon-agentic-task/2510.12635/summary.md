# Memory as Action: Autonomous Context Curation for Long-Horizon Agentic Tasks

**arXiv:** [2510.12635](https://arxiv.org/abs/2510.12635)
**PDF:** [下载](https://arxiv.org/pdf/2510.12635) · 本地: `2510.12635.pdf`
**作者:** Zhang, Yuxiang, Shu, Jiangming, Ma, Ye, Lin, Xueyuan, Wu, Shangxi, Sang, Jitao
**日期:** 2025/10/14

## Abstract

Long-context Large Language Models, despite their expanded capacity, require careful working memory management to mitigate attention dilution during long-horizon tasks. Yet existing approaches rely on external mechanisms that lack awareness of the agent's reasoning state, leading to suboptimal decisions. We propose Memory-as-Action (MemAct), a framework that treats working memory management as learnable policy actions. By formulating context management as in-place editing operations (deletion, insertion), MemAct enables joint optimization of information retention and task performance through end-to-end reinforcement learning. To address the computational challenges of dynamic context updates, we introduce Dynamic Context Policy Optimization, which restores training efficiency without compromising reasoning integrity. Experiments show that MemAct-RL-14B matches the accuracy of models $16\times$ larger while reducing average context length by 51\%, with learned strategies that adapt to model capabilities and generalize across task complexities.

## 文件

- `2510.12635.pdf` — 论文原文
- `meta.json` — 结构化元数据
