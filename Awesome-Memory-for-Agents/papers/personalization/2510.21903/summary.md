# TOM-SWE: User Mental Modeling For Software Engineering Agents

**arXiv:** [2510.21903](https://arxiv.org/abs/2510.21903)
**PDF:** [下载](https://arxiv.org/pdf/2510.21903) · 本地: `2510.21903.pdf`
**作者:** Zhou, Xuhui, Chen, Valerie, Wang, Zora Zhiruo, Neubig, Graham, Sap, Maarten, Wang, Xingyao
**日期:** 2025/10/24

## Abstract

Recent advances in coding agents have made them capable of planning, editing, running, and testing complex code bases. Despite their growing ability in coding tasks, these systems still struggle to infer and track user intent, especially when instructions are underspecified or context-dependent. To bridge this gap, we introduce ToM-SWE, a dual-agent architecture that pairs a primary software-engineering (SWE) agent with a lightweight theory-of-mind (ToM) partner agent dedicated to modeling the user&#39;s mental state. The ToM agent infers user goals, constraints, and preferences from instructions and interaction history, maintains a \textbf{persistent memory} of the user, and provides user-related suggestions to the SWE agent. In two software engineering benchmarks (ambiguous SWE-bench and stateful SWE-bench), ToM-SWE improves task success rates and user satisfaction. Notably, on the stateful SWE benchmark, a newly introduced evaluation that provides agents with a user simulator along with previous interaction histories, ToM-SWE achieves a substantially higher task success rate of 59.7\% compared to 18.1\% for OpenHands, a state-of-the-art SWE agent. Furthermore, in a three-week study with professional developers using ToM-SWE in their daily work, participants found it useful 86\% of the time, underscoring the value of stateful user modeling for practical coding agents.

## 文件

- `2510.21903.pdf` — 论文原文
- `meta.json` — 结构化元数据
