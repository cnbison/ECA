# Inducing Programmatic Skills for Agentic Tasks

**arXiv:** [2504.06821](https://arxiv.org/abs/2504.06821)
**PDF:** [下载](https://arxiv.org/pdf/2504.06821) · 本地: `2504.06821.pdf`
**作者:** Wang, Zora Zhiruo, Gandhi, Apurva, Neubig, Graham, Fried, Daniel
**日期:** 2025/04/09

## Abstract

To succeed in common digital tasks such as web navigation, agents must carry out a variety of specialized tasks such as searching for products or planning a travel route. To tackle these tasks, agents can bootstrap themselves by learning task-specific skills online through interaction with the web environment. In this work, we demonstrate that programs are an effective representation for skills. We propose agent skill induction (ASI), which allows agents to adapt themselves by inducing, verifying, and utilizing program-based skills on the fly. We start with an evaluation on the WebArena agent benchmark and show that ASI outperforms the static baseline agent and its text-skill counterpart by 23.5% and 11.3% in success rate, mainly thanks to the programmatic verification guarantee during the induction phase. ASI also improves efficiency by reducing 10.7-15.3% of the steps over baselines, by composing primitive actions (e.g., click) into higher-level skills (e.g., search product). We then highlight the efficacy of ASI in remaining efficient and accurate under scaled-up web activities. Finally, we examine the generalizability of induced skills when transferring between websites, and find that ASI can effectively reuse common skills, while also updating incompatible skills to versatile website changes.

## 文件

- `2504.06821.pdf` — 论文原文
- `meta.json` — 结构化元数据
