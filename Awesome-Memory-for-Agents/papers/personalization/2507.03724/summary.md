# MemOS: A Memory OS for AI System

**arXiv:** [2507.03724](https://arxiv.org/abs/2507.03724)
**PDF:** [下载](https://arxiv.org/pdf/2507.03724) · 本地: `2507.03724.pdf`
**作者:** Li, Zhiyu, Xi, Chenyang, Li, Chunyu, Chen, Ding, Chen, Boyu, Song, Shichao, Niu, Simin, Wang, Hanyu, Yang, Jiawei, Tang, Chen, Yu, Qingchen, Zhao, Jihao, Wang, Yezhaohui, Liu, Peng, Lin, Zehao, Wang, Pengyuan, Huo, Jiahao, Chen, Tianyi, Chen, Kai, Li, Kehang, Tao, Zhen, Lai, Huayi, Wu, Hao, Tang, Bo, Wang, Zhengren, Fan, Zhaoxin, Zhang, Ningyu, Zhang, Linfeng, Yan, Junchi, Yang, Mingchuan, Xu, Tong, Xu, Wei, Chen, Huajun, Wang, Haofen, Yang, Hongkang, Zhang, Wentao, Xu, Zhi-Qin John, Chen, Siheng, Xiong, Feiyu
**日期:** 2025/07/04

## Abstract

Large Language Models (LLMs) have become an essential infrastructure for Artificial General Intelligence (AGI), yet their lack of well-defined memory management systems hinders the development of long-context reasoning, continual personalization, and knowledge this http URL models mainly rely on static parameters and short-lived contextual states, limiting their ability to track user preferences or update knowledge over extended this http URL Retrieval-Augmented Generation (RAG) introduces external knowledge in plain text, it remains a stateless workaround without lifecycle control or integration with persistent this http URL work has modeled the training and inference cost of LLMs from a memory hierarchy perspective, showing that introducing an explicit memory layer between parameter memory and external retrieval can substantially reduce these costs by externalizing specific knowledge. Beyond computational efficiency, LLMs face broader challenges arising from how information is distributed over time and context, requiring systems capable of managing heterogeneous knowledge spanning different temporal scales and sources. To address this challenge, we propose MemOS, a memory operating system that treats memory as a manageable system resource. It unifies the representation, scheduling, and evolution of plaintext, activation-based, and parameter-level memories, enabling cost-efficient storage and retrieval. As the basic unit, a MemCube encapsulates both memory content and metadata such as provenance and versioning. MemCubes can be composed, migrated, and fused over time, enabling flexible transitions between memory types and bridging retrieval with parameter-based learning. MemOS establishes a memory-centric system framework that brings controllability, plasticity, and evolvability to LLMs, laying the foundation for continual learning and personalized modeling.

## 文件

- `2507.03724.pdf` — 论文原文
- `meta.json` — 结构化元数据
