# SEAgent: Self-Evolving Computer Use Agent with Autonomous Learning from Experience

**arXiv:** [2508.04700](https://arxiv.org/abs/2508.04700)
**PDF:** [下载](https://arxiv.org/pdf/2508.04700) · 本地: `2508.04700.pdf`
**作者:** Sun, Zeyi, Liu, Ziyu, Zang, Yuhang, Cao, Yuhang, Dong, Xiaoyi, Wu, Tong, Lin, Dahua, Wang, Jiaqi
**日期:** 2025/08/06

## Abstract

Repurposing large vision-language models (LVLMs) as computer use agents (CUAs) has led to substantial breakthroughs, primarily driven by human-labeled data. However, these models often struggle with novel and specialized software, particularly in scenarios lacking human annotations. To address this challenge, we propose SEAgent, an agentic self-evolving framework enabling CUAs to autonomously evolve through interactions with unfamiliar software. Specifically, SEAgent empowers computer-use agents to autonomously master novel software environments via experiential learning, where agents explore new software, learn through iterative trial-and-error, and progressively tackle auto-generated tasks organized from simple to complex. To achieve this goal, we design a World State Model for step-wise trajectory assessment, along with a Curriculum Generator that generates increasingly diverse and challenging tasks. The agent&#39;s policy is updated through experiential learning, comprised of adversarial imitation of failure actions and Group Relative Policy Optimization (GRPO) on successful ones. Furthermore, we introduce a specialist-to-generalist training strategy that integrates individual experiential insights from specialist agents, facilitating the development of a stronger generalist CUA capable of continuous autonomous evolution. This unified agent ultimately achieves performance surpassing ensembles of individual specialist agents on their specialized software. We validate the effectiveness of SEAgent across five novel software environments within OS-World. Our approach achieves a significant improvement of 23.2% in success rate, from 11.3% to 34.5%, over a competitive open-source CUA, i.e., UI-TARS.

## 文件

- `2508.04700.pdf` — 论文原文
- `meta.json` — 结构化元数据
