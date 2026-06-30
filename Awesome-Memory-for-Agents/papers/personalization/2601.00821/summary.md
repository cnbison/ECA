# Verbatim Chunks Beat Extracted Artifacts: A Controlled Ablation of Memory Representations for Long LLM Conversations

**arXiv:** [2601.00821](https://arxiv.org/abs/2601.00821)
**PDF:** [下载](https://arxiv.org/pdf/2601.00821) · 本地: `2601.00821.pdf`
**作者:** An, Tao
**日期:** 2025/12/23

## Abstract

A growing class of conversational-memory systems compresses dialogue history into structured artifacts -- extracted facts, decisions, or events -- on the premise that distilled structure retrieves better than raw text. We test this premise with a controlled ablation: within one fixed retrieval-rerank-reasoning pipeline, we swap only the stored representation -- LLM-extracted typed artifacts versus verbatim conversation chunks -- holding the model, retriever, reranker, and judge constant. Verbatim chunks win by 15.9 points on LoCoMo (43.9% vs. 28.0%) and 22.0 points on LongMemEval-S (67.4% vs. 45.4%); a 1-hop semantic graph does not recover the gap, and five confound controls reproduce the effect. The mechanism is lossy distillation: extraction discards verbatim detail that chunks retain for free, and the extracted-artifact pipeline never beats naive RAG in overall accuracy. Concurrent positive results with near-verbatim, provenance-preserving units fit the same account: retrieval accuracy tracks how far the representation departs from the source. For the extraction designs we test, structured memory should augment verbatim text rather than replace it: a chunks $\cup$ artifacts union store matches chunks on both benchmarks while artifacts alone forfeit the gap. Code and data: this https URL

## 文件

- `2601.00821.pdf` — 论文原文
- `meta.json` — 结构化元数据
