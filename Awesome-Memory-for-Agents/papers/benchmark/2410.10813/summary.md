# LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory

**arXiv:** [2410.10813](https://arxiv.org/abs/2410.10813)
**PDF:** [下载](https://arxiv.org/pdf/2410.10813) · 本地: `2410.10813.pdf`
**作者:** Wu, Di, Wang, Hongwei, Yu, Wenhao, Zhang, Yuwei, Chang, Kai-Wei, Yu, Dong
**日期:** 2024/10
**GitHub:** [xiaowu0162/LongMemEval](https://github.com/xiaowu0162/LongMemEval)
**名称:** LongMemEval

## Abstract

Recent large language model (LLM)-driven chat assistant systems have integrated memory components to track user-assistant chat histories, enabling more accurate and personalized responses. However, their long-term memory capabilities in sustained interactions remain underexplored. We introduce LongMemEval, a comprehensive benchmark designed to evaluate five core long-term memory abilities of chat assistants: information extraction, multi-session reasoning, temporal reasoning, knowledge updates, and abstention. With 500 meticulously curated questions embedded within freely scalable user-assistant chat histories, LongMemEval presents a significant challenge to existing long-term memory systems, with commercial chat assistants and long-context LLMs showing a 30% accuracy drop on memorizing information across sustained interactions. We then present a unified framework that breaks down the long-term memory design into three stages: indexing, retrieval, and reading. Built upon key experimental insights, we propose several memory design optimizations including session decomposition for value granularity, fact-augmented key expansion for indexing, and time-aware query expansion for refining the search scope. Extensive experiments show that these optimizations greatly improve both memory recall and downstream question answering on LongMemEval. Overall, our study provides valuable resources and guidance for advancing the long-term memory capabilities of LLM-based chat assistants, paving the way toward more personalized and reliable conversational AI. Our benchmark and code are publicly available at https://github.com/xiaowu0162/LongMemEval.

## 文件

- `2410.10813.pdf` — 论文原文
- `meta.json` — 结构化元数据
