# Beyond Dialogue Time: Temporal Semantic Memory for Personalized LLM Agents

**arXiv:** [2601.07468](https://arxiv.org/abs/2601.07468)
**PDF:** [下载](https://arxiv.org/pdf/2601.07468) · 本地: `2601.07468.pdf`
**作者:** Su, Miao, Guo, Yucan, Hou, Zhongni, Bai, Long, Li, Zixuan, Zhang, Yufei, Yin, Guojun, Lin, Wei, Jin, Xiaolong, Guo, Jiafeng, Cheng, Xueqi
**日期:** 2026/01/12

## Abstract

Memory enables Large Language Model (LLM) agents to perceive, store, and use information from past dialogues, which is essential for personalization. However, existing methods fail to properly model the temporal dimension of memory in two aspects: 1) Temporal inaccuracy: memories are organized by dialogue time rather than their actual occurrence time; 2) Temporal fragmentation: existing methods focus on point-wise memory, losing durative information that captures persistent states and evolving patterns. To address these limitations, we propose Temporal Semantic Memory (TSM), a memory framework that models semantic time for point-wise memory and supports the construction and utilization of durative memory. During memory construction, it first builds a semantic timeline rather than a dialogue one. Then, it consolidates temporally continuous and semantically related information into a durative memory. During memory utilization, it incorporates the query&#39;s temporal intent on the semantic timeline, enabling the retrieval of temporally appropriate durative memories and providing time-valid, duration-consistent context to support response generation. Experiments on LongMemEval and LoCoMo show that TSM consistently outperforms existing methods and achieves up to 12.2% absolute improvement in accuracy, demonstrating the effectiveness of the proposed method.

## 文件

- `2601.07468.pdf` — 论文原文
- `meta.json` — 结构化元数据
