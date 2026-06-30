# ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory

**arXiv:** [2509.25140](https://arxiv.org/abs/2509.25140)
**PDF:** [下载](https://arxiv.org/pdf/2509.25140) · 本地: `2509.25140.pdf`
**作者:** Ouyang, Siru, Yan, Jun, Hsu, I-Hung, Chen, Yanfei, Jiang, Ke, Wang, Zifeng, Han, Rujun, Le, Long T., Daruki, Samira, Tang, Xiangru, Tirumalashetty, Vishy, Lee, George, Rofouei, Mahsan, Lin, Hangfei, Han, Jiawei, Lee, Chen-Yu, Pfister, Tomas
**日期:** 2025/09/29

## Abstract

With the growing adoption of large language model agents in persistent real-world roles, they naturally encounter continuous streams of tasks. A key limitation, however, is their failure to learn from the accumulated interaction history, forcing them to discard valuable insights and repeat past errors. We propose ReasoningBank, a novel memory framework that distills generalizable reasoning strategies from an agent&#39;s self-judged successful and failed experiences. At test time, an agent retrieves relevant memories from ReasoningBank to inform its interaction and then integrates new learnings back, enabling it to become more capable over time. Building on this powerful experience learner, we further introduce memory-aware test-time scaling (MaTTS), which accelerates and diversifies this learning process by scaling up the agent&#39;s interaction experience. By allocating more compute to each task, the agent generates abundant, diverse experiences that provide rich contrastive signals for synthesizing higher-quality memory. The better memory in turn guides more effective scaling, establishing a powerful synergy between memory and test-time scaling. Across web browsing and software engineering benchmarks, ReasoningBank consistently outperforms existing memory mechanisms that store raw trajectories or only successful task routines, improving both effectiveness and efficiency; MaTTS further amplifies these gains. These findings establish memory-driven experience scaling as a new scaling dimension, enabling agents to self-evolve with emergent behaviors naturally arise. Our code can be found at this https URL.

## 文件

- `2509.25140.pdf` — 论文原文
- `meta.json` — 结构化元数据
