# Online Adaptation of Language Models with a Memory of Amortized Contexts

**arXiv:** [2403.04317](https://arxiv.org/abs/2403.04317)
**PDF:** [下载](https://arxiv.org/pdf/2403.04317) · 本地: `2403.04317.pdf`
**作者:** Tack, Jihoon, Kim, Jaehyung, Mitchell, Eric, Shin, Jinwoo, Teh, Yee Whye, Schwarz, Jonathan Richard
**日期:** 2024/03/07

## Abstract

Due to the rapid generation and dissemination of information, large language models (LLMs) quickly run out of date despite enormous development costs. To address the crucial need to keep models updated, online learning has emerged as a critical tool when utilizing LLMs for real-world applications. However, given the ever-expanding corpus of unseen documents and the large parameter space of modern LLMs, efficient adaptation is essential. To address these challenges, we propose Memory of Amortized Contexts (MAC), an efficient and effective online adaptation framework for LLMs with strong knowledge retention. We propose a feature extraction and memory-augmentation approach to compress and extract information from new documents into compact modulations stored in a memory bank. When answering questions, our model attends to and extracts relevant knowledge from this memory bank. To learn informative modulations in an efficient manner, we utilize amortization-based meta-learning, which substitutes an otherwise required optimization process with a single forward pass of the encoder. Subsequently, we learn to choose from and aggregate selected documents into a single modulation by conditioning on the question, allowing us to adapt a frozen language model during test time without requiring further gradient updates. Our experiment demonstrates the superiority of MAC in multiple aspects, including online adaptation performance, time, and memory efficiency. In addition, we show how MAC can be combined with and improve the performance of popular alternatives such as retrieval augmented generations (RAGs). Code is available at: this https URL.

## 文件

- `2403.04317.pdf` — 论文原文
- `meta.json` — 结构化元数据
