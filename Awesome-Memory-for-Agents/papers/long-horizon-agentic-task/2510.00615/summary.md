# ACON: Optimizing Context Compression for Long-horizon LLM Agents

**arXiv:** [2510.00615](https://arxiv.org/abs/2510.00615)
**PDF:** [下载](https://arxiv.org/pdf/2510.00615) · 本地: `2510.00615.pdf`
**作者:** Kang, Minki, Chen, Wei-Ning, Han, Dongge, Inan, Huseyin A., Wutschitz, Lukas, Chen, Yanzhi, Sim, Robert, Rajmohan, Saravan
**日期:** 2025/10/01

## Abstract

Large language models (LLMs) are increasingly deployed as agents in dynamic real-world environments, where success depends on maintaining precise records of actions and observations. However, the resulting unbounded context growth in long-horizon agentic tasks makes two critical bottlenecks: prohibitive inference memory costs and reasoning degradation due to irrelevant information. Existing compression methods fail to fully address this, often relying on brittle heuristics or requiring parameter updates impractical for proprietary or large-scale LLMs. We introduce Agent Context Optimization (ACON), a unified framework that optimally compresses both observations and history into concise, informative representations. Distinct from prior works, ACON employs an optimization in natural language space: it iteratively refines compression guidelines based on failure analysis of the agent, ensuring critical state information is preserved without model fine-tuning. To further minimize computational overhead, we distill the optimized compressor into smaller models. Experiments on AppWorld, OfficeBench, and Multi-objective QA demonstrate that ACON reduces peak token usage by 26-54% while improving task success over existing compression baselines. Notably, it enables smaller LMs to function effectively as long-horizon agents, achieving up to 46% performance improvement by mitigating context distraction. Our code is available at https://github.com/microsoft/acon.

## 文件

- `2510.00615.pdf` — 论文原文
- `meta.json` — 结构化元数据
