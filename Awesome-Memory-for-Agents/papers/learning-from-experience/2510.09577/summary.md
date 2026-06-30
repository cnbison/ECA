# Dyna-Mind: Learning to Simulate from Experience for Better AI Agents

**arXiv:** [2510.09577](https://arxiv.org/abs/2510.09577)
**PDF:** [下载](https://arxiv.org/pdf/2510.09577) · 本地: `2510.09577.pdf`
**作者:** Yu, Xiao, Peng, Baolin, Galley, Michel, Cheng, Hao, Wu, Qianhui, Kulkarni, Janardhan, Nath, Suman, Yu, Zhou, Gao, Jianfeng
**日期:** 2025/10/10

## Abstract

Reasoning models have recently shown remarkable progress in domains such as math and coding. However, their expert-level abilities in math and coding contrast sharply with their performance in long-horizon, interactive tasks such as web navigation and computer/phone-use. Inspired by literature on human cognition, we argue that current AI agents need &#39;&#39;vicarious trial and error&#39;&#39; - the capacity to mentally simulate alternative futures before acting - in order to enhance their understanding and performance in complex interactive environments. We introduce Dyna-Mind, a two-stage training framework that explicitly teaches (V)LM agents to integrate such simulation into their reasoning. In stage 1, we introduce Reasoning with Simulations (ReSim), which trains the agent to generate structured reasoning traces from expanded search trees built from real experience gathered through environment interactions. ReSim thus grounds the agent&#39;s reasoning in faithful world dynamics and equips it with the ability to anticipate future states in its reasoning. In stage 2, we propose Dyna-GRPO, an online reinforcement learning method to further strengthen the agent&#39;s simulation and decision-making ability by using both outcome rewards and intermediate states as feedback from real rollouts. Experiments on two synthetic benchmarks (Sokoban and ALFWorld) and one realistic benchmark (AndroidWorld) demonstrate that (1) ReSim effectively infuses simulation ability into AI agents, and (2) Dyna-GRPO leverages outcome and interaction-level signals to learn better policies for long-horizon, planning-intensive tasks. Together, these results highlight the central role of simulation in enabling AI agents to reason, plan, and act more effectively in the ever more challenging environments.

## 文件

- `2510.09577.pdf` — 论文原文
- `meta.json` — 结构化元数据
