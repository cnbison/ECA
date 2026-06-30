# MAPLE: Multi-Agent Adaptive Planning with Long-Term Memory for Table Reasoning

**arXiv:** [2506.05813](https://arxiv.org/abs/2506.05813)
**PDF:** [下载](https://arxiv.org/pdf/2506.05813) · 本地: `2506.05813.pdf`
**作者:** Bai, Ye, Wang, Minghan, Vu, Thuy-Trang
**日期:** 2025/06/06

## Abstract

Table-based question answering requires complex reasoning capabilities that current LLMs struggle to achieve with single-pass inference. Existing approaches, such as Chain-of-Thought reasoning and question decomposition, lack error detection mechanisms and discard problem-solving experiences, contrasting sharply with how humans tackle such problems. In this paper, we propose MAPLE (Multi-agent Adaptive Planning with Long-term mEmory), a novel framework that mimics human problem-solving through specialized cognitive agents working in a feedback-driven loop. MAPLE integrates 4 key components: (1) a Solver using the ReAct paradigm for reasoning, (2) a Checker for answer verification, (3) a Reflector for error diagnosis and strategy correction, and (4) an Archiver managing long-term memory for experience reuse and evolution. Experiments on WiKiTQ and TabFact demonstrate significant improvements over existing methods, achieving state-of-the-art performance across multiple LLM backbones.

## 文件

- `2506.05813.pdf` — 论文原文
- `meta.json` — 结构化元数据
