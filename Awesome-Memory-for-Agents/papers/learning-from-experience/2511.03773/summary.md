# Scaling Agent Learning via Experience Synthesis

**arXiv:** [2511.03773](https://arxiv.org/abs/2511.03773)
**PDF:** [下载](https://arxiv.org/pdf/2511.03773) · 本地: `2511.03773.pdf`
**作者:** Chen, Zhaorun, Zhao, Zhuokai, Zhang, Kai, Liu, Bo, Qi, Qi, Wu, Yifan, Kalluri, Tarun, Cao, Sara, Xiong, Yuanhao, Tong, Haibo, Yao, Huaxiu, Li, Hengduo, Zhu, Jiacheng, Li, Xian, Song, Dawn, Li, Bo, Weston, Jason, Huynh, Dat
**日期:** 2025/11/05

## Abstract

While reinforcement learning (RL) can empower autonomous agents by enabling self-improvement through interaction, its practical adoption remains challenging due to costly rollouts, limited task diversity, unreliable reward signals, and infrastructure complexity, all of which obstruct the collection of scalable experience data. To address these challenges, we introduce DreamGym, the first unified framework designed to synthesize diverse experiences with scalability in mind to enable effective online RL training for autonomous agents. Rather than relying on expensive real-environment rollouts, DreamGym distills environment dynamics into a reasoning-based experience model that derives consistent state transitions and feedback signals through step-by-step reasoning, enabling scalable agent rollout collection for RL. To improve the stability and quality of transitions, DreamGym leverages an experience replay buffer initialized with offline real-world data and continuously enriched with fresh interactions to actively support agent training. To improve knowledge acquisition, DreamGym adaptively generates new tasks that challenge the current agent policy, enabling more effective online curriculum learning. Experiments across diverse environments and agent backbones demonstrate that DreamGym substantially improves RL training, both in fully synthetic settings and in sim-to-real transfer scenarios. On non-RL-ready tasks like WebArena, DreamGym outperforms all baselines by over 30%. And in RL-ready but costly settings, it matches GRPO and PPO performance using only synthetic interactions. When transferring a policy trained purely on synthetic experiences to real-environment RL, DreamGym yields significant additional performance gains while requiring far fewer real-world interactions, providing a scalable warm-start strategy for general-purpose RL.

## 文件

- `2511.03773.pdf` — 论文原文
- `meta.json` — 结构化元数据
