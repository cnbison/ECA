# MemoChat: Tuning LLMs to Use Memos for Consistent Long-Range Open-Domain Conversation

**arXiv:** [2308.08239](https://arxiv.org/abs/2308.08239)
**PDF:** [下载](https://arxiv.org/pdf/2308.08239) · 本地: `2308.08239.pdf`
**作者:** Lu, Junru, An, Siyu, Lin, Mingbao, Pergola, Gabriele, He, Yulan, Yin, Di, Sun, Xing, Wu, Yunsheng
**日期:** 2023/08/16

## Abstract

We propose MemoChat, a pipeline for refining instructions that enables large language models (LLMs) to effectively employ self-composed memos for maintaining consistent long-range open-domain conversations. We demonstrate a long-range open-domain conversation through iterative &#34;memorization-retrieval-response&#34; cycles. This requires us to carefully design tailored tuning instructions for each distinct stage. The instructions are reconstructed from a collection of public datasets to teach the LLMs to memorize and retrieve past dialogues with structured memos, leading to enhanced consistency when participating in future conversations. We invite experts to manually annotate a test set designed to evaluate the consistency of long-range conversations questions. Experiments on three testing scenarios involving both open-source and API-accessible chatbots at scale verify the efficacy of MemoChat, which outperforms strong baselines. Our codes, data and models are available here: this https URL.

## 文件

- `2308.08239.pdf` — 论文原文
- `meta.json` — 结构化元数据
