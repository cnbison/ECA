# PARL-MT: Learning to Call Functions in Multi-Turn Conversation with Progress Awareness

**arXiv:** [2509.23206](https://arxiv.org/abs/2509.23206)
**PDF:** [下载](https://arxiv.org/pdf/2509.23206) · 本地: `2509.23206.pdf`
**作者:** Chai, Huacan, Cao, Zijie, Ran, Maolin, Yang, Yingxuan, Lin, Jianghao, Peng, Xin, Wang, Hairui, Ding, Renjie, Wan, Ziyu, Wen, Muning, Liu, Weiwen, Zhang, Weinan, Huang, Fei, Wen, Ying
**日期:** 2025/09/27

## Abstract

Large language models (LLMs) have achieved impressive success in single-turn function calling, yet real-world applications such as travel planning or multi-stage data analysis typically unfold across multi-turn conversations. In these settings, LLMs must not only issue accurate function calls at each step but also maintain progress awareness, the ability to summarize past interactions and plan future actions to ensure coherent, long-horizon task execution. Existing approaches, however, either reduce multi-turn training to isolated single-turn samples, which neglects task-level planning, or employ end-to-end reinforcement learning (RL) that struggles with redundancy and lacks explicit integration of progress awareness. To overcome these limitations, we introduce PARL-MT, a framework that explicitly incorporates progress awareness into LLM training for multi-turn function calling. PARL-MT combines (i) a Progress Awareness Generation (PAG) pipeline, which automatically constructs datasets coupling conversation summaries with future task planning, and (ii) a Progress Awareness-Guided Reinforcement Learning (PAG-RL) algorithm, which integrates progress awareness into RL training to reduce contextual redundancy and improve alignment between local actions and global task completion. Empirical results on two public benchmarks demonstrate that PARL-MT significantly outperforms existing methods, highlighting the effectiveness of progress awareness in enabling robust and efficient multi-turn function calling.

## 文件

- `2509.23206.pdf` — 论文原文
- `meta.json` — 结构化元数据
