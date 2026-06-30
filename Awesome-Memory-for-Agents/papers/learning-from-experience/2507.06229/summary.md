# Agent KB: Leveraging Cross-Domain Experience for Agentic Problem Solving

**arXiv:** [2507.06229](https://arxiv.org/abs/2507.06229)
**PDF:** [下载](https://arxiv.org/pdf/2507.06229) · 本地: `2507.06229.pdf`
**作者:** Tang, Xiangru, Qin, Tianrui, Peng, Tianhao, Zhou, Ziyang, Shao, Daniel, Du, Tingting, Wei, Xinming, Xia, Peng, Wu, Fang, Zhu, He, Zhang, Ge, Liu, Jiaheng, Wang, Xingyao, Hong, Sirui, Wu, Chenglin, Cheng, Hao, Wang, Chi, Zhou, Wangchunshu
**日期:** 2025/07/08

## Abstract

AI agent frameworks operate in isolation, forcing agents to rediscover solutions and repeat mistakes across different systems. Despite valuable problem-solving experiences accumulated by frameworks like smolagents, OpenHands, and OWL, this knowledge remains trapped within individual systems, preventing the emergence of collective intelligence. Current memory systems focus on individual agents or framework-specific demonstrations, failing to enable cross-architecture knowledge transfer. We introduce AGENT KB, a universal memory infrastructure enabling seamless experience sharing across heterogeneous agent frameworks without retraining. AGENT KB aggregates trajectories into a structured knowledge base and serves lightweight APIs. At inference time, hybrid retrieval operates through two stages: planning seeds agents with cross-domain workflows, while feedback applies targeted diagnostic fixes. A disagreement gate ensures retrieved knowledge enhances rather than disrupts reasoning, addressing knowledge interference in cross-framework transfer. We validate AGENT KB across major frameworks on GAIA, Humanity&#39;s Last Exam, GPQA, and SWE-bench. Results show substantial improvements across diverse model families: compared to baseline pass@1, smolagents with AGENT KB achieve up to 18.7pp gains at pass@3 (55.2% -&gt; 73.9%), while OpenHands improves 4.0pp on SWE-bench pass@1 (24.3% -&gt; 28.3%). Similar improvements are observed across all base model families. Ablations confirm that hybrid retrieval and feedback stages are essential, with automatically generated experiences matching manual curation. This establishes the foundation for collective agent intelligence through shared memory infrastructures.

## 文件

- `2507.06229.pdf` — 论文原文
- `meta.json` — 结构化元数据
