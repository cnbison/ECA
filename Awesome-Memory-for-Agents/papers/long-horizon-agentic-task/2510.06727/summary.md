# Scaling LLM Multi-turn RL with End-to-end Summarization-based Context Management

**arXiv:** [2510.06727](https://arxiv.org/abs/2510.06727)
**PDF:** [下载](https://arxiv.org/pdf/2510.06727) · 本地: `2510.06727.pdf`
**作者:** Lu, Miao, Sun, Weiwei, Du, Weihua, Ling, Zhan, Yao, Xuesong, Liu, Kang, Chen, Jiecao
**日期:** 2025/10/08

## Abstract

We study reinforcement learning (RL) fine-tuning of large language model (LLM) agents for long-horizon multi-turn tool use, where context length quickly becomes a fundamental bottleneck. Existing RL pipelines can suffer from degraded instruction following, excessive rollout costs, and most importantly, strict context limits. To address these challenges, we introduce summarization-based context management to training. In specific, it periodically compresses the tool using history by LLM-generated summaries that retain task-relevant information to keep a compact context while enabling the agent to scale beyond the fixed context window. Building on this formulation, we derive a policy gradient representation that seamlessly enables standard LLM RL infrastructures to optimize both tool-use behaviors as well as summarization strategies in an end-to-end fashion. We instantiate this framework with \underline{SU}mmarization augmented \underline{P}olicy \underline{O}ptimization (\texttt{SUPO}), an LLM RL algorithm that enables long-horizon training beyond a fixed context limit. Experiments on interactive function calling and searching tasks demonstrate that \texttt{SUPO} significantly improves the success rate while maintaining the same or even lower working context length compared to baselines. We also demonstrate that for complex searching tasks, \texttt{SUPO} can further improve the evaluation performance when scaling test-time maximum round of summarization beyond that of training time. Our results establish summarization-based context management as a principled and scalable approach for training RL agents beyond a fixed context length limit.

## 文件

- `2510.06727.pdf` — 论文原文
- `meta.json` — 结构化元数据
