# MemGPT: Towards LLMs as Operating Systems

**arXiv:** [2310.08560](https://arxiv.org/abs/2310.08560)
**PDF:** [下载](https://arxiv.org/pdf/2310.08560) · 本地: `2310.08560.pdf`
**作者:** Packer, Charles, Wooders, Sarah, Lin, Kevin, Fang, Vivian, Patil, Shishir G., Stoica, Ion, Gonzalez, Joseph E.
**日期:** 2023/10/12

## Abstract

Large language models (LLMs) have revolutionized AI, but are constrained by limited context windows, hindering their utility in tasks like extended conversations and document analysis. To enable using context beyond limited context windows, we propose virtual context management, a technique drawing inspiration from hierarchical memory systems in traditional operating systems that provide the appearance of large memory resources through data movement between fast and slow memory. Using this technique, we introduce MemGPT (Memory-GPT), a system that intelligently manages different memory tiers in order to effectively provide extended context within the LLM&#39;s limited context window, and utilizes interrupts to manage control flow between itself and the user. We evaluate our OS-inspired design in two domains where the limited context windows of modern LLMs severely handicaps their performance: document analysis, where MemGPT is able to analyze large documents that far exceed the underlying LLM&#39;s context window, and multi-session chat, where MemGPT can create conversational agents that remember, reflect, and evolve dynamically through long-term interactions with their users. We release MemGPT code and data for our experiments at this https URL.

## 文件

- `2310.08560.pdf` — 论文原文
- `meta.json` — 结构化元数据
