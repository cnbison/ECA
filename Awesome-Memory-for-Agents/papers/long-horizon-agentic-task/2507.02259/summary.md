# MemAgent: Reshaping Long-Context LLM with Multi-Conv RL-based Memory Agent

**arXiv:** [2507.02259](https://arxiv.org/abs/2507.02259)
**PDF:** [下载](https://arxiv.org/pdf/2507.02259) · 本地: `2507.02259.pdf`
**作者:** Yu, Hongli, Chen, Tinghong, Feng, Jiangtao, Chen, Jiangjie, Dai, Weinan, Yu, Qiying, Zhang, Ya-Qin, Ma, Wei-Ying, Liu, Jingjing, Wang, Mingxuan, Zhou, Hao
**日期:** 2025/07/03

## Abstract

Despite improvements by length extrapolation, efficient attention and memory modules, handling infinitely long documents with linear complexity without performance degradation during extrapolation remains the ultimate challenge in long-text processing. We directly optimize for long-text tasks in an end-to-end fashion and introduce a novel agent workflow, MemAgent, which reads text in segments and updates the memory using an overwrite strategy. We extend the DAPO algorithm to facilitate training via independent-context multi-conversation generation. MemAgent has demonstrated superb long-context capabilities, being able to extrapolate from an 8K context trained on 32K text to a 3.5M QA task with performance loss < 5% and achieves 95%+ in 512K RULER test.

## 文件

- `2507.02259.pdf` — 论文原文
- `meta.json` — 结构化元数据
