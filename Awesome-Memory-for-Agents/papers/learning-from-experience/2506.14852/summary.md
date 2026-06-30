# Agentic Plan Caching: Test-Time Memory for Fast and Cost-Efficient LLM Agents

**arXiv:** [2506.14852](https://arxiv.org/abs/2506.14852)
**PDF:** [下载](https://arxiv.org/pdf/2506.14852) · 本地: `2506.14852.pdf`
**作者:** Zhang, Qizheng, Wornow, Michael, Wan, Gerry, Olukotun, Kunle
**日期:** 2025/06/17

## Abstract

LLM-based agent applications have shown increasingly remarkable capabilities in complex workflows but incur substantial costs and latency due to extensive planning and reasoning requirements. Existing LLM caching techniques (like context caching and semantic caching), primarily designed for serving chatbots, are insufficient for agent applications where outputs depend on external data and environmental contexts. We propose Agentic Plan Caching (APC), a novel test-time memory that extracts, stores, adapts, and reuses structured plan templates from planning stages of agent applications across semantically similar tasks to reduce the cost and latency of serving. Unlike traditional semantic caching, our system extracts plan templates from completed agent executions at test-time, employs keyword extraction to match new requests against cached plans, and utilizes lightweight models to adapt these templates to task-specific plans with contexts. Evaluation across multiple real-world agent applications shows that our system can reduce costs by 50.31% and latency by 27.28% on average while maintaining performance, offering a more efficient solution for serving LLM-based agents that complements existing LLM serving infrastructures.

## 文件

- `2506.14852.pdf` — 论文原文
- `meta.json` — 结构化元数据
