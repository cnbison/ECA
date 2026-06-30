# FileGram: Grounding Agent Personalization in File-System Behavioral Traces

**arXiv:** [2604.04901](https://arxiv.org/abs/2604.04901)
**PDF:** [下载](https://arxiv.org/pdf/2604.04901) · 本地: `2604.04901.pdf`
**作者:** Liu, Shuai, Tian, Shulin, Hu, Kairui, Dong, Yuhao, Yang, Zhe, Li, Bo, Yang, Jingkang, Loy, Chen Change, Liu, Ziwei
**日期:** 2026/04/06

## Abstract

Coworking AI agents operating within local file systems are rapidly emerging as a paradigm in human-AI interaction; however, effective personalization remains limited by severe data constraints, as strict privacy barriers and the difficulty of jointly collecting multimodal real-world traces prevent scalable training and evaluation, and existing methods remain interaction-centric while overlooking dense behavioral traces in file-system operations; to address this gap, we propose FileGram, a comprehensive framework that grounds agent memory and personalization in file-system behavioral traces, comprising three core components: (1) FileGramEngine, a scalable persona-driven data engine that simulates realistic workflows and generates fine-grained multimodal action sequences at scale; (2) FileGramBench, a diagnostic benchmark grounded in file-system behavioral traces for evaluating memory systems on profile reconstruction, trace disentanglement, persona drift detection, and multimodal grounding; and (3) FileGramOS, a bottom-up memory architecture that builds user profiles directly from atomic actions and content deltas rather than dialogue summaries, encoding these traces into procedural, semantic, and episodic channels with query-time abstraction; extensive experiments show that FileGramBench remains challenging for state-of-the-art memory systems and that FileGramEngine and FileGramOS are effective, and by open-sourcing the framework, we hope to support future research on personalized memory-centric file-system agents.

## 文件

- `2604.04901.pdf` — 论文原文
- `meta.json` — 结构化元数据
