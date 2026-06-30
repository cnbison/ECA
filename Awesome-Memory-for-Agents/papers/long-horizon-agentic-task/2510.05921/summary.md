# Prompt reinforcing for long-term planning of large language models

**arXiv:** [2510.05921](https://arxiv.org/abs/2510.05921)
**PDF:** [下载](https://arxiv.org/pdf/2510.05921) · 本地: `2510.05921.pdf`
**作者:** Lin, Hsien-Chin, Ruppik, Benjamin Matthias, van Niekerk, Carel, Shen, Chia-Hao, Heck, Michael, Lubis, Nurul, Vukovic, Renato, Feng, Shutong, Gašić, Milica
**日期:** 2025/10/07

## Abstract

Large language models (LLMs) have achieved remarkable success in a wide range of natural language processing tasks and can be adapted through prompting. However, they remain suboptimal in multi-turn interactions, often relying on incorrect early assumptions and failing to track user goals over time, which makes such tasks particularly challenging. Prior works in dialogue systems have shown that long-term planning is essential for handling interactive tasks. In this work, we propose a prompt optimisation framework inspired by reinforcement learning, which enables such planning to take place by only modifying the task instruction prompt of the LLM-based agent. By generating turn-by-turn feedback and leveraging experience replay for prompt rewriting, our proposed method shows significant improvement in multi-turn tasks such as text-to-SQL and task-oriented dialogue. Moreover, it generalises across different LLM-based agents and can leverage diverse LLMs as meta-prompting agents. This warrants future research in reinforcement learning-inspired parameter-free optimisation methods.

## 文件

- `2510.05921.pdf` — 论文原文
- `meta.json` — 结构化元数据
