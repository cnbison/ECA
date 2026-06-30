# ML-Agent: Reinforcing LLM Agents for Autonomous Machine Learning Engineering

**arXiv:** [2505.23723](https://arxiv.org/abs/2505.23723)
**PDF:** [下载](https://arxiv.org/pdf/2505.23723) · 本地: `2505.23723.pdf`
**作者:** Liu, Zexi, Chai, Jingyi, Zhu, Xinyu, Tang, Shuo, Ye, Rui, Zhang, Bo, Bai, Lei, Chen, Siheng
**日期:** 2025/05/29

## Abstract

The emergence of large language model (LLM)-based agents has significantly advanced the development of autonomous machine learning (ML) engineering. However, the dominant prompt-based paradigm exhibits limitations: smaller models lack the capacity to learn from execution trajectories for generalization, while large proprietary models incur high computational overhead, restricting accessibility and scalability. Focusing on this, for the first time, we explore the paradigm of learning-based agentic ML, where an LLM agent learns through interactive experimentation on ML tasks using online reinforcement learning (RL). To realize this, we propose a novel agentic ML training framework with three key components: (1) exploration-enriched fine-tuning, which enables LLM agents to generate diverse actions for enhanced RL exploration; (2) step-wise RL, which enables training on a single action step, accelerating experience collection and improving training efficiency; (3) an agentic ML-specific reward module, which unifies varied ML feedback signals into consistent rewards for RL optimization. Leveraging this framework, we train ML-Agent, driven by a 7B-sized Qwen-2.5 LLM for autonomous ML. Despite training on only 9 ML tasks, our 7B-sized ML-Agent achieves comparable performance to agents using much larger proprietary LLMs (e.g., GPT-5) but at significantly lower computational cost, demonstrating strong performance and cross-task generalization.

## 文件

- `2505.23723.pdf` — 论文原文
- `meta.json` — 结构化元数据
