# LEGOMem: Modular Procedural Memory for Multi-agent LLM Systems for Workflow Automation

**arXiv:** [2510.04851](https://arxiv.org/abs/2510.04851)
**PDF:** [下载](https://arxiv.org/pdf/2510.04851) · 本地: `2510.04851.pdf`
**作者:** Han, Dongge, Couturier, Camille, Diaz, Daniel Madrigal, Zhang, Xuchao, Rühle, Victor, Rajmohan, Saravan
**日期:** 2025/10/06

## Abstract

We introduce LEGOMem, a modular procedural memory framework for multi-agent large language model (LLM) systems in workflow automation. LEGOMem decomposes past task trajectories into reusable memory units and flexibly allocates them across orchestrators and task agents to support planning and execution. To explore the design space of memory in multi-agent systems, we use LEGOMem as a lens and conduct a systematic study of procedural memory in multi-agent systems, examining where memory should be placed, how it should be retrieved, and which agents benefit most. Experiments on the OfficeBench benchmark show that orchestrator memory is critical for effective task decomposition and delegation, while fine-grained agent memory improves execution accuracy. We find that even teams composed of smaller language models can benefit substantially from procedural memory, narrowing the performance gap with stronger agents by leveraging prior execution traces for more accurate planning and tool use. These results position LEGOMem as both a practical framework for memory-augmented agent systems and a research tool for understanding memory design in multi-agent workflow automation.

## 文件

- `2510.04851.pdf` — 论文原文
- `meta.json` — 结构化元数据
