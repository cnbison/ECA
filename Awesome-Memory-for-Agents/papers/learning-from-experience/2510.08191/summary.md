# Training-Free Group Relative Policy Optimization

**arXiv:** [2510.08191](https://arxiv.org/abs/2510.08191)
**PDF:** [下载](https://arxiv.org/pdf/2510.08191) · 本地: `2510.08191.pdf`
**作者:** Cai, Yuzheng, Cai, Siqi, Shi, Yuchen, Xu, Zihan, Chen, Lichao, Qin, Yulei, Tan, Xiaoyu, Li, Gang, Li, Zongyi, Lin, Haojia, Mao, Yong, Li, Ke, Sun, Xing
**日期:** 2025/10/09

## Abstract

Recent advances in Large Language Model (LLM) agents have demonstrated their promising general capabilities. However, their performance in specialized real-world domains often degrades due to challenges in effectively integrating external tools and specific prompting strategies. While methods like agentic reinforcement learning have been proposed to address this, they typically rely on costly parameter updates, for example, through a process that uses Supervised Fine-Tuning (SFT) followed by a Reinforcement Learning (RL) phase with Group Relative Policy Optimization (GRPO) to alter the output distribution. However, we argue that LLMs can achieve a similar effect on the output distribution by learning experiential knowledge as a token prior, which is a far more lightweight approach that not only addresses practical data scarcity but also avoids the common issue of overfitting. To this end, we propose Training-Free Group Relative Policy Optimization (Training-Free GRPO), a cost-effective solution that enhances LLM agent performance without any parameter updates. Our method leverages the group relative semantic advantage instead of numerical ones within each group of rollouts, iteratively distilling high-quality experiential knowledge during multi-epoch learning on a minimal ground-truth data. Such knowledge serves as the learned token prior, which is seamlessly integrated during LLM API calls to guide model behavior. Experiments on mathematical reasoning and web searching tasks demonstrate that Training-Free GRPO, when applied to DeepSeek-V3.1-Terminus, significantly improves out-of-domain performance. With just a few dozen training samples, Training-Free GRPO outperforms fine-tuned small LLMs with marginal training data and cost.

## 文件

- `2510.08191.pdf` — 论文原文
- `meta.json` — 结构化元数据
