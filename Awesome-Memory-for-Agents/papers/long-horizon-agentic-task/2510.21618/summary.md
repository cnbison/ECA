# DeepAgent: A General Reasoning Agent with Scalable Toolsets

**arXiv:** [2510.21618](https://arxiv.org/abs/2510.21618)
**PDF:** [下载](https://arxiv.org/pdf/2510.21618) · 本地: `2510.21618.pdf`
**作者:** Li, Xiaoxi, Jiao, Wenxiang, Jin, Jiarui, Dong, Guanting, Jin, Jiajie, Wang, Yinuo, Wang, Hao, Zhu, Yutao, Wen, Ji-Rong, Lu, Yuan, Dou, Zhicheng
**日期:** 2025/10/24

## Abstract

Large reasoning models have demonstrated strong problem-solving abilities, yet real-world tasks often require external tools and long-horizon interactions. Existing agent frameworks typically follow predefined workflows, which limit autonomous and global task completion. In this paper, we introduce DeepAgent, an end-to-end deep reasoning agent that performs autonomous thinking, tool discovery, and action execution within a single, coherent reasoning process. To manage long-horizon interactions, we introduce an autonomous memory folding mechanism that compresses past interactions into structured episodic, working, and tool memories, reducing error accumulation while preserving critical information. To teach general-purpose tool use efficiently and stably, we develop an end-to-end reinforcement learning strategy, namely ToolPO, that leverages LLM-simulated APIs and applies tool-call advantage attribution to assign fine-grained credit to the tool invocation tokens. Extensive experiments on eight benchmarks, including general tool-use tasks (ToolBench, API-Bank, TMDB, Spotify, ToolHop) and downstream applications (ALFWorld, WebShop, GAIA, HLE), demonstrate that DeepAgent consistently outperforms baselines across both labeled-tool and open-set tool retrieval scenarios. The code and demo are available at https://github.com/RUC-NLPIR/DeepAgent.

## 文件

- `2510.21618.pdf` — 论文原文
- `meta.json` — 结构化元数据
