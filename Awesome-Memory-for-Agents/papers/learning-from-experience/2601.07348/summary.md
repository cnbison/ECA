# Controlled Self-Evolution for Algorithmic Code Optimization

**arXiv:** [2601.07348](https://arxiv.org/abs/2601.07348)
**PDF:** [下载](https://arxiv.org/pdf/2601.07348) · 本地: `2601.07348.pdf`
**作者:** Hu, Tu, Chen, Ronghao, Zhang, Shuo, Yin, Jianghao, Feng, Mou Xiao, Liu, Jingping, Zhang, Shaolei, Jiang, Wenqi, Fang, Yuqi, Hu, Sen, Wang, Huacan, Xu, Yi
**日期:** 2026/01/12

## Abstract

Self-evolution methods enhance code generation through iterative &#34;generate-verify-refine&#34; cycles, yet existing approaches suffer from low exploration efficiency, failing to discover solutions with superior complexity within limited budgets. This inefficiency stems from initialization bias trapping evolution in poor solution regions, uncontrolled stochastic operations lacking feedback guidance, and insufficient experience utilization across tasks. To address these bottlenecks, we propose Controlled Self-Evolution (CSE), which consists of three key components. Diversified Planning Initialization generates structurally distinct algorithmic strategies for broad solution space coverage. Genetic Evolution replaces stochastic operations with feedback-guided mechanisms, enabling targeted mutation and compositional crossover. Hierarchical Evolution Memory captures both successful and failed experiences at inter-task and intra-task levels. Experiments on EffiBench-X demonstrate that CSE consistently outperforms all baselines across various LLM backbones. Furthermore, CSE achieves higher efficiency from early generations and maintains continuous improvement throughout evolution. Our code is publicly available at this https URL.

## 文件

- `2601.07348.pdf` — 论文原文
- `meta.json` — 结构化元数据
