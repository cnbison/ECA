# Structured Belief State and the First Precision-Aware Benchmark for LLM Memory Retrieval

**arXiv:** [2605.11325](https://arxiv.org/abs/2605.11325)
**PDF:** [下载](https://arxiv.org/pdf/2605.11325) · 本地: `2605.11325.pdf`
**作者:** Flynt, Jeffrey
**日期:** 2026/05
**GitHub:** [tenurehq/precisionMemBench](https://github.com/tenurehq/precisionMemBench)
**名称:** PrecisionMemBench

## Abstract

Every major benchmark for LLM memory systems, LoCoMo foremost, measures whether a model answered correctly, not whether the memory system retrieved correctly. A system returning its entire belief store achieves recall of 1.0 and passes answer-quality evaluation. This is the difference between a unit test and an integration test: retrieval quality must be measured in isolation from the generative model it feeds into, and no existing benchmark does this. We demonstrate that this failure persists even when entity extraction is entirely faithful. Memory baselines achieve mean retrieval precision of just 0.05 to 0.08 on cases referencing their own extractions. The failure is structural: cosine similarity over a domain-specific corpus cannot discriminate relevant beliefs from semantically proximate ones, an invariance confirmed across a 20x range in embedding model scale. Multi-turn evaluation surfaces a compounding failure; after topic drift, comparison systems allow semantic mass to bleed across turns, yielding high drift scores on re-entry. Single-turn metrics conceal this cost: Hindsight reports sub-700ms single-turn latency but exceeds 2,700ms mean per session turn, with p95 above 6,000ms. Under LLM-as-a-Judge evaluation, these failures remain invisible. We present two contributions: PrecisionMemBench, an 89-case benchmark measuring retrieval precision independently of generative models across diverse scope, mutation, and isolation assertions; and Tenure, a local-first structured belief store using multi-path BM25 with analyzer asymmetry, differential boosting, and hard scope isolation. Tenure passes 89/89 cases with mean precision 1.0 and sub-15ms retrieval latency. Comparison providers perform worse than the raw vector baseline they are built on, with zero active retrieval passes and ingestion costs of 98 to 897 seconds, failures that answer-quality benchmarks cannot detect.

## 文件

- `2605.11325.pdf` — 论文原文
- `meta.json` — 结构化元数据
