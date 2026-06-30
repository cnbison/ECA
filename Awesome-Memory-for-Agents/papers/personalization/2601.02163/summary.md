# EverMemOS: A Self-Organizing Memory Operating System for Structured Long-Horizon Reasoning

**arXiv:** [2601.02163](https://arxiv.org/abs/2601.02163)
**PDF:** [下载](https://arxiv.org/pdf/2601.02163) · 本地: `2601.02163.pdf`
**作者:** Hu, Chuanrui, Gao, Xingze, Zhou, Zuyi, Xu, Dannong, Bai, Yi, Li, Xintong, Zhang, Hui, Li, Tong, Zhang, Chong, Bing, Lidong, Deng, Yafeng
**日期:** 2026/01/05

## Abstract

Large Language Models (LLMs) are increasingly deployed as long-term interactive agents, yet their limited context windows make it difficult to sustain coherent behavior over extended interactions. Existing memory systems often store isolated records and retrieve fragments, limiting their ability to consolidate evolving user states and resolve conflicts. We introduce EverMemOS, a self-organizing memory operating system that implements an engram-inspired lifecycle for computational memory. Episodic Trace Formation converts dialogue streams into MemCells that capture episodic traces, atomic facts, and time-bounded Foresight signals. Semantic Consolidation organizes MemCells into thematic MemScenes, distilling stable semantic structures and updating user profiles. Reconstructive Recollection performs MemScene-guided agentic retrieval to compose the necessary and sufficient context for downstream reasoning. Experiments on LoCoMo and LongMemEval show that EverMemOS achieves state-of-the-art performance on memory-augmented reasoning tasks. We further report a profile study on PersonaMem v2 and qualitative case studies illustrating chat-oriented capabilities such as user profiling and Foresight. Code is available at this https URL.

## 文件

- `2601.02163.pdf` — 论文原文
- `meta.json` — 结构化元数据
