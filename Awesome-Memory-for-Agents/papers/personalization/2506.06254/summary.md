# PersonaAgent: Bridging Memory and Action for Personalized LLM Agents

**arXiv:** [2506.06254](https://arxiv.org/abs/2506.06254)
**PDF:** [下载](https://arxiv.org/pdf/2506.06254) · 本地: `2506.06254.pdf`
**作者:** Zhang, Weizhi, Zhang, Xinyang, Zhang, Chenwei, Yang, Liangwei, Shang, Jingbo, Wei, Zhepei, Zou, Henry Peng, Huang, Zijie, Wang, Zhengyang, Gao, Yifan, Pan, Xiaoman, Xiong, Lian, Liu, Jingguo, Yu, Philip S., Li, Xian
**日期:** 2025/06/06

## Abstract

Large Language Model (LLM) empowered agents have recently emerged as advanced paradigms that exhibit impressive capabilities in a wide range of domains and tasks. Despite their potential, current LLM agents often adopt a one-size-fits-all approach, lacking the flexibility to respond to users&#39; varying needs and preferences. This limitation motivates us to develop PersonaAgent, the first personalized LLM agent framework designed to address versatile personalization tasks. Specifically, PersonaAgent integrates two complementary components - a personalized memory module that includes episodic and semantic memory mechanisms; a personalized action module that enables the agent to perform tool actions tailored to the user. At the core, the persona (defined as unique system prompt for each user) functions as an intermediary: it leverages insights from personalized memory to control agent actions, while the outcomes of these actions in turn refine the memory. Based on the framework, we propose a test-time user-preference alignment strategy that simulate the latest n interactions to optimize the persona prompt, ensuring real-time user preference alignment through textual loss feedback between simulated and ground-truth responses. Experimental evaluations demonstrate that PersonaAgent significantly outperforms other baseline methods by not only personalizing the action space effectively but also scaling during test-time real-world applications. These results underscore the feasibility and potential of our approach in delivering tailored, dynamic user experiences.

## 文件

- `2506.06254.pdf` — 论文原文
- `meta.json` — 结构化元数据
