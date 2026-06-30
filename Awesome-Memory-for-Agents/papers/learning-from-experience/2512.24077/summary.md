# LoongFlow: Directed Evolutionary Search via a Cognitive Plan-Execute-Summarize Paradigm

**arXiv:** [2512.24077](https://arxiv.org/abs/2512.24077)
**PDF:** [下载](https://arxiv.org/pdf/2512.24077) · 本地: `2512.24077.pdf`
**作者:** Wan, Chunhui, Dai, Xunan, Wang, Zhuo, Li, Minglei, Wang, Yanpeng, Mao, Yinan, Lan, Yu, Xiao, Zhiwen
**日期:** 2025/12/30

## Abstract

The transition from static Large Language Models (LLMs) to self-improving agents is hindered by the lack of structured reasoning in traditional evolutionary approaches. Existing methods often struggle with premature convergence and inefficient exploration in high-dimensional code spaces. To address these challenges, we introduce LoongFlow, a self-evolving agent framework that achieves state-of-the-art solution quality with significantly reduced computational costs. Unlike "blind" mutation operators, LoongFlow integrates LLMs into a cognitive "Plan-Execute-Summarize" (PES) paradigm, effectively mapping the evolutionary search to a reasoning-heavy process. To sustain long-term architectural coherence, we incorporate a hybrid evolutionary memory system. By synergizing Multi-Island models with MAP-Elites and adaptive Boltzmann selection, this system theoretically balances the exploration-exploitation trade-off, maintaining diverse behavioral niches to prevent optimization stagnation. We instantiate LoongFlow with a General Agent for algorithmic discovery and an ML Agent for pipeline optimization. Extensive evaluations on the AlphaEvolve benchmark and Kaggle competitions demonstrate that LoongFlow outperforms leading baselines (e.g., OpenEvolve, ShinkaEvolve) by up to 60% in evolutionary efficiency while discovering superior solutions. LoongFlow marks a substantial step forward in autonomous scientific discovery, enabling the generation of expert-level solutions with reduced computational overhead.

## 文件

- `2512.24077.pdf` — 论文原文
- `meta.json` — 结构化元数据
