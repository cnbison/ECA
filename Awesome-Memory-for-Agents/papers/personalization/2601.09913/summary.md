# Continuum Memory Architectures for Long-Horizon LLM Agents

**arXiv:** [2601.09913](https://arxiv.org/abs/2601.09913)
**PDF:** [下载](https://arxiv.org/pdf/2601.09913) · 本地: `2601.09913.pdf`
**作者:** Logan, Joe
**日期:** 2026/01/14

## Abstract

Retrieval-augmented generation (RAG) has become the default strategy for providing large language model (LLM) agents with contextual knowledge. Yet RAG treats memory as a stateless lookup table: information persists indefinitely, retrieval is read-only, and temporal continuity is absent. We define the \textit{Continuum Memory Architecture} (CMA), a class of systems that maintain and update internal state across interactions through persistent storage, selective retention, associative routing, temporal chaining, and consolidation into higher-order abstractions. Rather than disclosing implementation specifics, we specify the architectural requirements CMA imposes and show consistent behavioral advantages on tasks that expose RAG&#39;s structural inability to accumulate, mutate, or disambiguate memory. The empirical probes (knowledge updates, temporal association, associative recall, contextual disambiguation) demonstrate that CMA is a necessary architectural primitive for long-horizon agents while highlighting open challenges around latency, drift, and interpretability.

## 文件

- `2601.09913.pdf` — 论文原文
- `meta.json` — 结构化元数据
