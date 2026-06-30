# TeleMem: Building Long-Term and Multimodal Memory for Agentic AI

**arXiv:** [2601.06037](https://arxiv.org/abs/2601.06037)
**PDF:** [下载](https://arxiv.org/pdf/2601.06037) · 本地: `2601.06037.pdf`
**作者:** Chen, Chunliang, Guan, Ming, Lin, Xiao, Li, Jiaxu, Lin, Luxi, Wang, Qiyi, Chen, Xiangyu, Luo, Jixiang, Sun, Changzhi, Zhang, Dell, Li, Xuelong
**日期:** 2025/12/12

## Abstract

Large language models (LLMs) excel at many NLP tasks but struggle to sustain long-term interactions due to limited attention over extended dialogue histories. Retrieval-augmented generation (RAG) mitigates this issue but lacks reliable mechanisms for updating or refining stored memories, leading to schema-driven hallucinations, inefficient write operations, and minimal support for multimodal this http URL address these challenges, we propose TeleMem, a unified long-term and multimodal memory system that maintains coherent user profiles through narrative dynamic extraction, ensuring that only dialogue-grounded information is preserved. TeleMem further introduces a structured writing pipeline that batches, retrieves, clusters, and consolidates memory entries, substantially improving storage efficiency, reducing token usage, and accelerating memory operations. Additionally, a multimodal memory module combined with ReAct-style reasoning equips the system with a closed-loop observe, think, and act process that enables accurate understanding of complex video content in long-term contexts. Experimental results show that TeleMem surpasses the state-of-the-art Mem0 baseline with 19% higher accuracy, 43% fewer tokens, and a 2.1x speedup on the ZH-4O long-term role-play gaming benchmark.

## 文件

- `2601.06037.pdf` — 论文原文
- `meta.json` — 结构化元数据
