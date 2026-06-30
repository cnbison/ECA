# EvolveR: Self-Evolving LLM Agents through an Experience-Driven Lifecycle

**arXiv:** [2510.16079](https://arxiv.org/abs/2510.16079)
**PDF:** [下载](https://arxiv.org/pdf/2510.16079) · 本地: `2510.16079.pdf`
**作者:** Wu, Rong, Wang, Xiaoman, Mei, Jianbiao, Cai, Pinlong, Fu, Daocheng, Yang, Cheng, Wen, Licheng, Yang, Xuemeng, Shen, Yufan, Wang, Yuxin, Shi, Botian
**日期:** 2025/10/17

## Abstract

Current Large Language Model (LLM) agents show strong performance in tool use, but lack the crucial capability to systematically learn from their own experiences. While existing frameworks mainly focus on mitigating external knowledge gaps, they fail to address a more fundamental limitation: the inability to iteratively refine problem-solving strategies. In this work, we introduce EvolveR, a framework designed to enable agent to self-improve through a complete, closed-loop experience lifecycle. This lifecycle comprises two key stages: (1) Offline Self-Distillation, where the agent&#39;s interaction trajectories are synthesized into a structured repository of abstract, reusable strategic principles; (2) Online Interaction, where the agent interacts with tasks and actively retrieves distilled principles to guide its decision-making, accumulating a diverse set of behavioral trajectories. This loop employs a policy reinforcement mechanism to iteratively update the agent based on its performance. We demonstrate the effectiveness of EvolveR on complex multi-hop question-answering benchmarks, where it achieves superior performance over strong agentic baselines. Our work presents a comprehensive blueprint for agents that learn not only from external data but also from the consequences of their own actions, paving the way for more autonomous and continuously improving systems. Code is available at this https URL.

## 文件

- `2510.16079.pdf` — 论文原文
- `meta.json` — 结构化元数据
