# Live-SWE-agent: Can Software Engineering Agents Self-Evolve on the Fly?

**arXiv:** [2511.13646](https://arxiv.org/abs/2511.13646)
**PDF:** [下载](https://arxiv.org/pdf/2511.13646) · 本地: `2511.13646.pdf`
**作者:** Xia, Chunqiu Steven, Wang, Zhe, Yang, Yan, Wei, Yuxiang, Zhang, Lingming
**日期:** 2025/11/17

## Abstract

Large Language Models (LLMs) are reshaping almost all industries, including software engineering. In recent years, a number of LLM agents have been proposed to solve real-world software problems. Such software agents are typically equipped with a suite of coding tools and can autonomously decide the next actions to form complete trajectories to solve end-to-end software tasks. While promising, they typically require dedicated design and may still be suboptimal, since it can be extremely challenging and costly to exhaust the entire agent scaffold design space. Recognizing that software agents are inherently software themselves that can be further refined/modified, researchers have proposed a number of self-improving software agents recently, including the Darwin-Gödel Machine (DGM). Meanwhile, such self-improving agents require costly offline training on specific benchmarks and may not generalize well across different LLMs or benchmarks. In this paper, we propose Live-SWE-agent, the first live software agent that can autonomously and continuously evolve itself on-the-fly during runtime when solving real-world software problems. More specifically, Live-SWE-agent starts with the most basic agent scaffold with only access to bash tools (e.g., mini-SWE-agent), and autonomously evolves its own scaffold implementation while solving real-world software problems. Our evaluation on the widely studied SWE-bench Verified benchmark shows that LIVE-SWE-AGENT can achieve an impressive solve rate of 77.4% without test-time scaling, outperforming all existing software agents, including the best proprietary solution. Moreover, Live-SWE-agent outperforms state-of-the-art manually crafted software agents on the recent SWE-Bench Pro benchmark, achieving the best-known solve rate of 45.8%.

## 文件

- `2511.13646.pdf` — 论文原文
- `meta.json` — 结构化元数据
