# SimpleMem: Efficient Lifelong Memory for LLM Agents

**arXiv:** [2601.02553](https://arxiv.org/abs/2601.02553)
**PDF:** [下载](https://arxiv.org/pdf/2601.02553) · 本地: `2601.02553.pdf`
**作者:** Liu, Jiaqi, Su, Yaofeng, Xia, Peng, Han, Siwei, Zheng, Zeyu, Xie, Cihang, Ding, Mingyu, Yao, Huaxiu
**日期:** 2026/01/05

## Abstract

To support long-term interaction in complex environments, LLM agents require memory systems that manage historical experiences. Existing approaches either retain full interaction histories via passive context extension, leading to substantial redundancy, or rely on iterative reasoning to filter noise, incurring high token costs. To address this challenge, we introduce SimpleMem, an efficient memory framework based on semantic lossless compression. We propose a three-stage pipeline designed to maximize information density and token utilization: (1) Semantic Structured Compression, which distills unstructured interactions into compact, multi-view indexed memory units; (2) Online Semantic Synthesis, an intra-session process that instantly integrates related context into unified abstract representations to eliminate redundancy; and (3) Intent-Aware Retrieval Planning, which infers search intent to dynamically determine retrieval scope and construct precise context efficiently. Experiments on benchmark datasets show that our method consistently outperforms baseline approaches in accuracy, retrieval efficiency, and inference cost, achieving an average F1 improvement of 26.4% in LoCoMo while reducing inference-time token consumption by up to 30-fold, demonstrating a superior balance between performance and efficiency. Code is available at this https URL.

## 文件

- `2601.02553.pdf` — 论文原文
- `meta.json` — 结构化元数据
