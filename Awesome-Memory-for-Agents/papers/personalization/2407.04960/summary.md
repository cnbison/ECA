# MemoCRS: Memory-enhanced Sequential Conversational Recommender Systems with Large Language Models

**arXiv:** [2407.04960](https://arxiv.org/abs/2407.04960)
**PDF:** [下载](https://arxiv.org/pdf/2407.04960) · 本地: `2407.04960.pdf`
**作者:** Xi, Yunjia, Liu, Weiwen, Lin, Jianghao, Chen, Bo, Tang, Ruiming, Zhang, Weinan, Yu, Yong
**日期:** 2024/07/06

## Abstract

Conversational recommender systems (CRSs) aim to capture user preferences and provide personalized recommendations through multi-round natural language dialogues. However, most existing CRS models mainly focus on dialogue comprehension and preferences mining from the current dialogue session, overlooking user preferences in historical dialogue sessions. The preferences embedded in the user&#39;s historical dialogue sessions and the current session exhibit continuity and sequentiality, and we refer to CRSs with this characteristic as sequential CRSs. In this work, we leverage memory-enhanced LLMs to model the preference continuity, primarily focusing on addressing two key issues: (1) redundancy and noise in historical dialogue sessions, and (2) the cold-start users problem. To this end, we propose a Memory-enhanced Conversational Recommender System Framework with Large Language Models (dubbed MemoCRS) consisting of user-specific memory and general memory. User-specific memory is tailored to each user for their personalized interests and implemented by an entity-based memory bank to refine preferences and retrieve relevant memory, thereby reducing the redundancy and noise of historical sessions. The general memory, encapsulating collaborative knowledge and reasoning guidelines, can provide shared knowledge for users, especially cold-start users. With the two kinds of memory, LLMs are empowered to deliver more precise and tailored recommendations for each user. Extensive experiments on both Chinese and English datasets demonstrate the effectiveness of MemoCRS.

## 文件

- `2407.04960.pdf` — 论文原文
- `meta.json` — 结构化元数据
