# MemGen: Weaving Generative Latent Memory for Self-Evolving Agents

**arXiv:** [2509.24704](https://arxiv.org/abs/2509.24704)
**PDF:** [下载](https://arxiv.org/pdf/2509.24704) · 本地: `2509.24704.pdf`
**作者:** Zhang, Guibin, Fu, Muxin, Yan, Shuicheng
**日期:** 2025/09/29

## Abstract

Agent memory shapes how Large Language Model (LLM)-powered agents, akin to the human brain, progressively refine themselves through environment interactions. Existing paradigms remain constrained: parametric memory forcibly adjusts model parameters, and retrieval-based memory externalizes experience into structured databases, yet neither captures the fluid interweaving of reasoning and memory that underlies human cognition. To address this gap, we propose MemGen, a dynamic generative memory framework that equips agents with a human-esque cognitive faculty. It consists of a \textit{memory trigger}, which monitors the agent&#39;s reasoning state to decide explicit memory invocation, and a \textit{memory weaver}, which takes the agent&#39;s current state as stimulus to construct a latent token sequence as machine-native memory to enrich its reasoning. In this way, MemGen enables agents to recall and augment latent memory throughout reasoning, producing a tightly interwoven cycle of memory and cognition. Extensive experiments across eight benchmarks show that MemGen surpasses leading external memory systems such as ExpeL and AWM by up to $38.22\%$, exceeds GRPO by up to $13.44\%$, and exhibits strong cross-domain generalization ability. More importantly, we find that without explicit supervision, MemGen spontaneously evolves distinct human-like memory faculties, including planning memory, procedural memory, and working memory, suggesting an emergent trajectory toward more naturalistic forms of machine cognition.

## 文件

- `2509.24704.pdf` — 论文原文
- `meta.json` — 结构化元数据
