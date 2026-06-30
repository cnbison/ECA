# Memento 2: Learning by Stateful Reflective Memory

**arXiv:** [2512.22716](https://arxiv.org/abs/2512.22716)
**PDF:** [下载](https://arxiv.org/pdf/2512.22716) · 本地: `2512.22716.pdf`
**作者:** Wang, Jun
**日期:** 2025/12/27

## Abstract

We present a theoretical study of continual and experiential learning in large language model agents that combine episodic memory with reinforcement learning. We argue that the key mechanism for continual adaptation, without updating model parameters, is reflection: the agent&#39;s ability to use past experience to guide future actions. Empirical findings suggest that episodic, experience-driven reflection enables generalised adaptation across a wide range of open-ended, long-horizon tasks. This indicates that efficient learning can occur during deployment and weakens the traditional separation between training and testing. Motivated by this, we introduce the Stateful Reflective Decision Process, a formal model of reflective memory dynamics. In this abstraction, an agent maintains an episodic memory and performs two core operations. Writing stores interaction outcomes and plays the role of policy evaluation. Reading retrieves relevant past cases to inform decisions and plays the role of policy improvement. This perspective treats reflective memory as a control object that can be analysed using classical reinforcement learning tools. We then develop a read-write reflective learning framework by integrating retrieval into soft policy iteration and establish convergence guarantees. We show that as memory grows and provides denser coverage of the state space, the resulting composite policy converges to the optimal solution. Overall, this framework connects practical memory-based methods with principled reinforcement learning, providing a rigorous mathematical basis for building reflective, memory-embedded agents capable of continual general-purpose learning.

## 文件

- `2512.22716.pdf` — 论文原文
- `meta.json` — 结构化元数据
