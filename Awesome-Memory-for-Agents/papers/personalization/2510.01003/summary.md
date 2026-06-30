# Improving Code Localization with Repository Memory

**arXiv:** [2510.01003](https://arxiv.org/abs/2510.01003)
**PDF:** [下载](https://arxiv.org/pdf/2510.01003) · 本地: `2510.01003.pdf`
**作者:** Wang, Boshi, Xu, Weijian, Li, Yunsheng, Gao, Mei, Xie, Yujia, Sun, Huan, Chen, Dongdong
**日期:** 2025/10/01

## Abstract

Code localization is a fundamental challenge in repository-level software engineering tasks such as bug fixing. While existing methods equip language agents with comprehensive tools/interfaces to fetch information from the repository, they overlook the critical aspect of memory, where each instance is typically handled from scratch assuming no prior repository knowledge. In contrast, human developers naturally build long-term repository memory, such as the functionality of key modules and associations between various bug types and their likely fix locations. In this work, we augment language agents with such memory by leveraging a repository&#39;s commit history -- a rich yet underutilized resource that chronicles the codebase&#39;s evolution. We introduce tools that allow the agent to retrieve from a non-parametric memory encompassing recent historical commits and linked issues, as well as functionality summaries of actively evolving parts of the codebase identified via commit patterns. We demonstrate that augmenting such a memory can significantly improve LocAgent, a state-of-the-art localization framework, on both SWE-bench-verified and the more recent SWE-bench-live benchmarks. Our research contributes towards developing agents that can accumulate and leverage past experience for long-horizon tasks, more closely emulating the expertise of human developers.

## 文件

- `2510.01003.pdf` — 论文原文
- `meta.json` — 结构化元数据
