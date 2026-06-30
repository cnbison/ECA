# How Memory Management Impacts LLM Agents: An Empirical Study of Experience-Following Behavior

**arXiv:** [2505.16067](https://arxiv.org/abs/2505.16067)
**PDF:** [下载](https://arxiv.org/pdf/2505.16067) · 本地: `2505.16067.pdf`
**作者:** Xiong, Zidi, Lin, Yuping, Xie, Wenya, He, Pengfei, Liu, Zirui, Tang, Jiliang, Lakkaraju, Himabindu, Xiang, Zhen
**日期:** 2025/05/21

## Abstract

Memory is a critical component in large language model (LLM)-based agents, enabling them to store and retrieve past executions to improve task performance over time. In this paper, we conduct an empirical study on how memory management choices impact the LLM agents&#39; behavior, especially their long-term performance. Specifically, we focus on two fundamental memory management operations that are widely used by many agent frameworks-memory addition and deletion-to systematically study their impact on the agent behavior. Through our quantitative analysis, we find that LLM agents display an experience-following property: high similarity between a task input and the input in a retrieved memory record often results in highly similar agent outputs. Our analysis further reveals two significant challenges associated with this property: error propagation, where inaccuracies in past experiences compound and degrade future performance, and misaligned experience replay, where some seemingly correct executions can provide limited or even misleading value as experiences. Through controlled experiments, we demonstrate the importance of regulating experience quality within the memory bank and show that future task evaluations can serve as free quality labels for stored memory. Our findings offer insights into the behavioral dynamics of LLM agent memory systems and provide practical guidance for designing memory components that support robust, long-term agent performance.

## 文件

- `2505.16067.pdf` — 论文原文
- `meta.json` — 结构化元数据
