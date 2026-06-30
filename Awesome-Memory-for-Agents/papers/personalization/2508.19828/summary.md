# Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning

**arXiv:** [2508.19828](https://arxiv.org/abs/2508.19828)
**PDF:** [下载](https://arxiv.org/pdf/2508.19828) · 本地: `2508.19828.pdf`
**作者:** Yan, Sikuan, Yang, Xiufeng, Huang, Zuchao, Nie, Ercong, Ding, Zifeng, Li, Zonggen, Ma, Xiaowen, Bi, Jinhe, Kersting, Kristian, Pan, Jeff Z., Schütze, Hinrich, Tresp, Volker, Ma, Yunpu
**日期:** 2025/08/27

## Abstract

Large Language Models (LLMs) have demonstrated impressive capabilities across a wide range of NLP tasks, but they remain fundamentally stateless, constrained by limited context windows that hinder long-horizon reasoning. Recent efforts to address this limitation often augment LLMs with an external memory bank, yet most existing pipelines are static and heuristic-driven, lacking a learned mechanism for deciding what to store, update, or retrieve. We present Memory-R1, a reinforcement learning (RL) framework that equips LLMs with the ability to actively manage and utilize external memory through two specialized agents: a Memory Manager that learns structured operations, including ADD, UPDATE, DELETE, and NOOP; and an Answer Agent that pre-selects and reasons over relevant entries. Both agents are fine-tuned with outcome-driven RL (PPO and GRPO), enabling adaptive memory management with minimal supervision. With only 152 training QA pairs, Memory-R1 outperforms strong baselines and generalizes across diverse question types, three benchmarks (LoCoMo, MSC, LongMemEval), and multiple model scales (3B-14B).

## 文件

- `2508.19828.pdf` — 论文原文
- `meta.json` — 结构化元数据
