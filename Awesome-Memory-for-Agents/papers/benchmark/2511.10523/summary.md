# Convomem Benchmark: Why Your First 150 Conversations Don't Need RAG

**arXiv:** [2511.10523](https://arxiv.org/abs/2511.10523)
**PDF:** [下载](https://arxiv.org/pdf/2511.10523) · 本地: `2511.10523.pdf`
**作者:** Pakhomov, Egor, Nijkamp, Erik, Xiong, Caiming
**日期:** 2025/11
**GitHub:** [SalesforceAIResearch/ConvoMem](https://github.com/SalesforceAIResearch/ConvoMem)
**名称:** ConvoMem

## Abstract

We introduce a comprehensive benchmark for conversational memory evaluation containing 75,336 question-answer pairs across diverse categories including user facts, assistant recall, abstention, preferences, temporal changes, and implicit connections. While existing benchmarks have advanced the field, our work addresses fundamental challenges in statistical power, data generation consistency, and evaluation flexibility that limit current memory evaluation frameworks. We examine the relationship between conversational memory and retrieval-augmented generation (RAG). While these systems share fundamental architectural patterns--temporal reasoning, implicit extraction, knowledge updates, and graph representations--memory systems have a unique characteristic: they start from zero and grow progressively with each conversation. This characteristic enables naive approaches that would be impractical for traditional RAG. Consistent with recent findings on long context effectiveness, we observe that simple full-context approaches achieve 70-82% accuracy even on our most challenging multi-message evidence cases, while sophisticated RAG-based memory systems like Mem0 achieve only 30-45% when operating on conversation histories under 150 interactions. Our analysis reveals practical transition points: long context excels for the first 30 conversations, remains viable with manageable trade-offs up to 150 conversations, and typically requires hybrid or RAG approaches beyond that point as costs and latencies become prohibitive. These patterns indicate that the small-corpus advantage of conversational memory--where exhaustive search and complete reranking are feasible--deserves dedicated research attention rather than simply applying general RAG solutions to conversation histories.

## 文件

- `2511.10523.pdf` — 论文原文
- `meta.json` — 结构化元数据
