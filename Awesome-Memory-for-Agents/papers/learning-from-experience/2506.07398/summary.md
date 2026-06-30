# G-Memory: Tracing Hierarchical Memory for Multi-Agent Systems

**arXiv:** [2506.07398](https://arxiv.org/abs/2506.07398)
**PDF:** [下载](https://arxiv.org/pdf/2506.07398) · 本地: `2506.07398.pdf`
**作者:** Zhang, Guibin, Fu, Muxin, Wan, Guancheng, Yu, Miao, Wang, Kun, Yan, Shuicheng
**日期:** 2025/06/09

## Abstract

Large language model (LLM)-powered multi-agent systems (MAS) have demonstrated cognitive and execution capabilities that far exceed those of single LLM agents, yet their capacity for self-evolution remains hampered by underdeveloped memory architectures. Upon close inspection, we are alarmed to discover that prevailing MAS memory mechanisms (1) are overly simplistic, completely disregarding the nuanced inter-agent collaboration trajectories, and (2) lack cross-trial and agent-specific customization, in stark contrast to the expressive memory developed for single agents. To bridge this gap, we introduce G-Memory, a hierarchical, agentic memory system for MAS inspired by organizational memory theory, which manages the lengthy MAS interaction via a three-tier graph hierarchy: insight, query, and interaction graphs. Upon receiving a new user query, G-Memory performs bi-directional memory traversal to retrieve both $\textit{high-level, generalizable insights}$ that enable the system to leverage cross-trial knowledge, and $\textit{fine-grained, condensed interaction trajectories}$ that compactly encode prior collaboration experiences. Upon task execution, the entire hierarchy evolves by assimilating new collaborative trajectories, nurturing the progressive evolution of agent teams. Extensive experiments across five benchmarks, three LLM backbones, and three popular MAS frameworks demonstrate that G-Memory improves success rates in embodied action and accuracy in knowledge QA by up to $20.89\%$ and $10.12\%$, respectively, without any modifications to the original frameworks. Our codes are available at this https URL.

## 文件

- `2506.07398.pdf` — 论文原文
- `meta.json` — 结构化元数据
