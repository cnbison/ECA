# WebCoach: Self-Evolving Web Agents with Cross-Session Memory Guidance

**arXiv:** [2511.12997](https://arxiv.org/abs/2511.12997)
**PDF:** [下载](https://arxiv.org/pdf/2511.12997) · 本地: `2511.12997.pdf`
**作者:** Liu, Genglin, Geng, Shijie, Li, Sha, Cui, Hejie, Zhang, Sarah, Liu, Xin, Liu, Tianyi
**日期:** 2025/11/17

## Abstract

Multimodal LLM-powered agents have recently demonstrated impressive capabilities in web navigation, enabling agents to complete complex browsing tasks across diverse domains. However, current agents struggle with repetitive errors and lack the ability to learn from past experiences across sessions, limiting their long-term robustness and sample efficiency. We introduce WebCoach, a model-agnostic self-evolving framework that equips web browsing agents with persistent cross-session memory, enabling improved long-term planning, reflection, and continual learning without retraining. WebCoach consists of three key components: (1) a WebCondenser, which standardizes raw navigation logs into concise summaries; (2) an External Memory Store, which organizes complete trajectories as episodic experiences; and (3) a Coach, which retrieves relevant experiences based on similarity and recency, and decides whether to inject task-specific advice into the agent via runtime hooks. This design empowers web agents to access long-term memory beyond their native context window, improving robustness in complex browsing tasks. Moreover, WebCoach achieves self-evolution by continuously curating episodic memory from new navigation trajectories, enabling agents to improve over time without retraining. Evaluations on the WebVoyager benchmark demonstrate that WebCoach consistently improves the performance of browser-use agents across three different LLM backbones. With a 38B model, it increases task success rates from 47% to 61% while reducing or maintaining the average number of steps. Notably, smaller base models with WebCoach achieve performance comparable to the same web agent using GPT-4o.

## 文件

- `2511.12997.pdf` — 论文原文
- `meta.json` — 结构化元数据
