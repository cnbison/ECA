# Beyond Static Summarization: Proactive Memory Extraction for LLM Agents

**arXiv:** [2601.04463](https://arxiv.org/abs/2601.04463)
**PDF:** [下载](https://arxiv.org/pdf/2601.04463) · 本地: `2601.04463.pdf`
**作者:** Yang, Chengyuan, Sun, Zequn, Wei, Wei, Hu, Wei
**日期:** 2026/01/08

## Abstract

Memory management is vital for LLM agents to handle long-term interaction and personalization. Most research focuses on how to organize and use memory summary, but often overlooks the initial memory extraction stage. In this paper, we argue that existing summary-based methods have two major limitations based on the recurrent processing theory. First, summarization is &#34;ahead-of-time&#34;, acting as a blind &#34;feed-forward&#34; process that misses important details because it doesn&#39;t know future tasks. Second, extraction is usually &#34;one-off&#34;, lacking a feedback loop to verify facts, which leads to the accumulation of information loss. To address these issues, we propose proactive memory extraction (namely ProMem). Unlike static summarization, ProMem treats extraction as an iterative cognitive process. We introduce a recurrent feedback loop where the agent uses self-questioning to actively probe the dialogue history. This mechanism allows the agent to recover missing information and correct errors. Our ProMem significantly improves the completeness of the extracted memory and QA accuracy. It also achieves a superior trade-off between extraction quality and token cost.

## 文件

- `2601.04463.pdf` — 论文原文
- `meta.json` — 结构化元数据
