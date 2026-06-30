# Alita-G: Self-Evolving Generative Agent for Agent Generation

**arXiv:** [2510.23601](https://arxiv.org/abs/2510.23601)
**PDF:** [下载](https://arxiv.org/pdf/2510.23601) · 本地: `2510.23601.pdf`
**作者:** Qiu, Jiahao, Qi, Xuan, Wang, Hongru, Juan, Xinzhe, Wang, Yimin, Zhao, Zelin, Geng, Jiayi, Guo, Jiacheng, Li, Peihang, Shi, Jingzhe, Liu, Shilong, Wang, Mengdi
**日期:** 2025/10/27

## Abstract

Large language models (LLMs) have been shown to perform better when scaffolded into agents with memory, tools, and feedback. Beyond this, self-evolving agents have emerged, but current work largely limits adaptation to prompt rewriting or failure retries. Therefore, we present ALITA-G, a self-evolution framework that transforms a general-purpose agent into a domain expert by systematically generating, abstracting, and curating Model Context Protocol (MCP) tools. In this framework, a generalist agent executes a curated suite of target-domain tasks and synthesizes candidate MCPs from successful trajectories. These are then abstracted to parameterized primitives and consolidated into an MCP Box. At inference time, ALITA-G performs retrieval-augmented MCP selection with the help of each tool&#39;s descriptions and use cases, before executing an agent equipped with the MCP Executor. Across several benchmarks GAIA, PathVQA, and Humanity&#39;s Last Exam, ALITA-G attains strong gains while reducing computation costs. On GAIA validation, it achieves 83.03% pass@1 and 89.09% pass@3, establishing a new state-of-the-art result while reducing mean tokens per example by approximately 15% relative to a strong baseline agent. ALITA-G thus provides a principled pathway from generalist capability to reusable, domain-specific competence, improving both accuracy and efficiency on complex reasoning tasks.

## 文件

- `2510.23601.pdf` — 论文原文
- `meta.json` — 结构化元数据
