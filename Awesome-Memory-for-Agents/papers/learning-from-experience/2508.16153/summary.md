# Memento: Fine-tuning LLM Agents without Fine-tuning LLMs

**arXiv:** [2508.16153](https://arxiv.org/abs/2508.16153)
**PDF:** [下载](https://arxiv.org/pdf/2508.16153) · 本地: `2508.16153.pdf`
**作者:** Zhou, Huichi, Chen, Yihang, Guo, Siyuan, Yan, Xue, Lee, Kin Hei, Wang, Zihan, Lee, Ka Yiu, Zhang, Guchun, Shao, Kun, Yang, Linyi, Wang, Jun
**日期:** 2025/08/22

## Abstract

In this paper, we introduce a novel learning paradigm for Adaptive Large Language Model (LLM) agents that eliminates the need for fine-tuning the underlying LLMs. Existing approaches are often either rigid, relying on static, handcrafted reflection workflows, or computationally intensive, requiring gradient updates of LLM model parameters. In contrast, our method enables low-cost continual adaptation via memory-based online reinforcement learning. We formalise this as a Memory-augmented Markov Decision Process (M-MDP), equipped with a neural case-selection policy to guide action decisions. Past experiences are stored in an episodic memory, either differentiable or non-parametric. The policy is continually updated based on environmental feedback through a memory rewriting mechanism, whereas policy improvement is achieved through efficient memory reading (retrieval). We instantiate our agent model in the deep research setting, namely \emph{Memento}, which attains top-1 on GAIA validation ($87.88\%$ Pass@$3$) and $79.40\%$ on the test set. It reaches $66.6\%$ F1 and $80.4\%$ PM on the DeepResearcher dataset, outperforming the state-of-the-art training-based method, while case-based memory adds $4.7\%$ to $9.6\%$ absolute points on out-of-distribution tasks. Our approach offers a scalable and efficient pathway for developing generalist LLM agents capable of continuous, real-time learning without gradient updates, advancing machine learning towards open-ended skill acquisition and deep research scenarios. The code is available at this https URL.

## 文件

- `2508.16153.pdf` — 论文原文
- `meta.json` — 结构化元数据
