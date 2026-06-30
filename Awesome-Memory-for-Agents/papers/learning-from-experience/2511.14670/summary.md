# SkillGen: Learning Domain Skills for In-Context Sequential Decision Making

**arXiv:** [2511.14670](https://arxiv.org/abs/2511.14670)
**PDF:** [下载](https://arxiv.org/pdf/2511.14670) · 本地: `2511.14670.pdf`
**作者:** Ding, Ruomeng, Cheng, Wei, Shao, Minglai, Zhao, Chen
**日期:** 2025/11/18

## Abstract

Large language models (LLMs) are increasingly applied to sequential decision-making through in-context learning (ICL), yet their effectiveness is highly sensitive to prompt quality. Effective prompts should meet three principles: focus on decision-critical information, provide step-level granularity, and minimize reliance on expert annotations through label efficiency. However, existing ICL methods often fail to satisfy all three criteria simultaneously. Motivated by these challenges, we introduce SkillGen, a skill-based ICL framework for structured sequential reasoning. It constructs an action-centric, domain-level graph from sampled trajectories, identifies high-utility actions via temporal-difference credit assignment, and retrieves step-wise skills to generate fine-grained, context-aware prompts. We further present a theoretical analysis showing that focusing on high-utility segments supports task identifiability and informs more effective ICL prompt design. Experiments on ALFWorld, BabyAI, and ScienceWorld, using both open-source and proprietary LLMs, show that SkillGen achieves consistent gains, improving progress rate by 5.9%-16.5% on average across models.

## 文件

- `2511.14670.pdf` — 论文原文
- `meta.json` — 结构化元数据
