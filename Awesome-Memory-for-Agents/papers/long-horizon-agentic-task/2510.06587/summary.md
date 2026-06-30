# WebDART: Dynamic Decomposition and Re-planning for Complex Web Tasks

**arXiv:** [2510.06587](https://arxiv.org/abs/2510.06587)
**PDF:** [下载](https://arxiv.org/pdf/2510.06587) · 本地: `2510.06587.pdf`
**作者:** Yang, Jingbo, Hou, Bairu, Wei, Wei, Chang, Shiyu, Bao, Yujia
**日期:** 2025/10/08

## Abstract

Large language model (LLM) agents are becoming competent at straightforward web tasks, such as opening an item page or submitting a form, but still struggle with objectives that require long horizon navigation, large scale information extraction, and reasoning under constraints. We present WebDART, a general framework that enables a single LLM to handle such complex chores. WebDART (i) dynamically decomposes each objective into three focused subtasks: navigation, information extraction, and execution, so the model concentrates on one skill at a time, and (ii) continuously replans the decomposition as new webpages are revealed, taking advantage of newly discovered filters or shortcuts and avoiding redundant exploration. Evaluated on WebChoreArena, WebDART lifts success rates by up to 13.7 percentage points over previous SOTA agents, while matching their performance on the easier WebArena suite and completing tasks with up to 14.7 fewer navigation steps.

## 文件

- `2510.06587.pdf` — 论文原文
- `meta.json` — 结构化元数据
