# Evaluating Very Long-Term Conversational Memory of LLM Agents

**arXiv:** [2402.17753](https://arxiv.org/abs/2402.17753)
**PDF:** [下载](https://arxiv.org/pdf/2402.17753) · 本地: `2402.17753.pdf`
**作者:** Maharana, Adyasha, Lee, Dong-Ho, Tulyakov, Sergey, Bansal, Mohit, Barbieri, Francesco, Fang, Yuwei
**日期:** 2024/02
**GitHub:** [snap-research/locomo](https://github.com/snap-research/locomo)
**名称:** LoCoMo

## Abstract

Existing works on long-term open-domain dialogues focus on evaluating model responses within contexts spanning no more than five chat sessions. Despite advancements in long-context large language models (LLMs) and retrieval augmented generation (RAG) techniques, their efficacy in very long-term dialogues remains unexplored. To address this research gap, we introduce a machine-human pipeline to generate high-quality, very long-term dialogues by leveraging LLM-based agent architectures and grounding their dialogues on personas and temporal event graphs. Moreover, we equip each agent with the capability of sharing and reacting to images. The generated conversations are verified and edited by human annotators for long-range consistency and grounding to the event graphs. Using this pipeline, we collect LoCoMo, a dataset of very long-term conversations, each encompassing 300 turns and 9K tokens on avg., over up to 35 sessions. Based on LoCoMo, we present a comprehensive evaluation benchmark to measure long-term memory in models, encompassing question answering, event summarization, and multi-modal dialogue generation tasks. Our experimental results indicate that LLMs exhibit challenges in understanding lengthy conversations and comprehending long-range temporal and causal dynamics within dialogues. Employing strategies like long-context LLMs or RAG can offer improvements but these models still substantially lag behind human performance.

## 文件

- `2402.17753.pdf` — 论文原文
- `meta.json` — 结构化元数据
