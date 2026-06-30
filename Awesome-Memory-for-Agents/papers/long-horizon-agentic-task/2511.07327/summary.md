# IterResearch: Rethinking Long-Horizon Agents with Interaction Scaling

**arXiv:** [2511.07327](https://arxiv.org/abs/2511.07327)
**PDF:** [下载](https://arxiv.org/pdf/2511.07327) · 本地: `2511.07327.pdf`
**作者:** Chen, Guoxin, Qiao, Zile, Chen, Xuanzhong, Yu, Donglei, Xu, Haotian, Zhao, Wayne Xin, Song, Ruihua, Yin, Wenbiao, Yin, Huifeng, Zhang, Liwen, Li, Kuan, Liao, Minpeng, Jiang, Yong, Xie, Pengjun, Huang, Fei, Zhou, Jingren
**日期:** 2025/11/10

## Abstract

Recent advances in deep-research agents have shown promise for autonomous knowledge construction through dynamic reasoning over external sources. However, existing approaches rely on a mono-contextual paradigm that accumulates all information in a single, expanding context window, leading to context suffocation and noise contamination that limit their effectiveness on long-horizon tasks. We introduce \textbf{IterResearch}, a novel iterative deep-research paradigm that revisits long-horizon research through the lens of Interaction Scaling. Instead of relying on linear context accumulation, we adopt an MDP-inspired architecture with strategic workspace reconstruction. By maintaining an evolving report as memory and periodically synthesizing insights, our approach preserves consistent reasoning capacity across arbitrary exploration depths. To effectively train this paradigm, we employ Efficiency-Aware Policy Optimization (EAPO), a training strategy that adapts geometric reward discounting to incentivize efficient exploration and utilizes adaptive downsampling for stable distributed training. Extensive experiments demonstrate that IterResearch achieves substantial improvements over existing open-source agents with average +14.5pp across six benchmarks and narrows the gap with frontier proprietary systems. Remarkably, our paradigm exhibits unprecedented interaction scaling, extending to 2048 interactions with dramatic performance gains (from 3.5\% to 42.5\%), and serves as an effective prompting strategy, improving frontier models by up to 19.2pp over ReAct on long-horizon tasks. These findings position IterResearch as a versatile solution for long-horizon reasoning, effective both as a trained agent and as a prompting paradigm for frontier models.

## 文件

- `2511.07327.pdf` — 论文原文
- `meta.json` — 结构化元数据
