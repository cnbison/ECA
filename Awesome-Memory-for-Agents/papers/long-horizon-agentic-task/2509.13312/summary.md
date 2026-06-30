# WebWeaver: Structuring Web-Scale Evidence with Dynamic Outlines for Open-Ended Deep Research

**arXiv:** [2509.13312](https://arxiv.org/abs/2509.13312)
**PDF:** [下载](https://arxiv.org/pdf/2509.13312) · 本地: `2509.13312.pdf`
**作者:** Li, Zijian, Guan, Xin, Zhang, Bo, Huang, Shen, Zhou, Houquan, Lai, Shaopeng, Yan, Ming, Jiang, Yong, Xie, Pengjun, Huang, Fei, Zhang, Jun, Zhou, Jingren
**日期:** 2025/09/16

## Abstract

This paper tackles \textbf{open-ended deep research (OEDR)}, a complex challenge where AI agents must synthesize vast web-scale information into insightful reports. Current approaches are plagued by dual-fold limitations: static research pipelines that decouple planning from evidence acquisition and monolithic generation paradigms that include redundant, irrelevant evidence, suffering from hallucination issues and low citation accuracy. To address these challenges, we introduce \textbf{WebWeaver}, a novel dual-agent framework that emulates the human research process. The planner operates in a dynamic cycle, iteratively interleaving evidence acquisition with outline optimization to produce a comprehensive, citation-grounded outline linking to a memory bank of evidence. The writer then executes a hierarchical retrieval and writing process, composing the report section by section. By performing targeted retrieval of only the necessary evidence from the memory bank via citations for each part, it effectively mitigates long-context issues and citation hallucinations. Our framework establishes a new state-of-the-art across major OEDR benchmarks, including DeepResearch Bench, DeepConsult, and DeepResearchGym. These results validate our human-centric, iterative methodology, demonstrating that adaptive planning and focused synthesis are crucial for producing comprehensive, trusted, and well-structured reports.

## 文件

- `2509.13312.pdf` — 论文原文
- `meta.json` — 结构化元数据
