# BrowserAgent: Building Web Agents with Human-Inspired Web Browsing Actions

**arXiv:** [2510.10666](https://arxiv.org/abs/2510.10666)
**PDF:** [下载](https://arxiv.org/pdf/2510.10666) · 本地: `2510.10666.pdf`
**作者:** Yu, Tao, Zhang, Zhengbo, Lyu, Zhiheng, Gong, Junhao, Yi, Hongzhu, Wang, Xinming, Zhou, Yuxuan, Yang, Jiabing, Nie, Ping, Huang, Yan, Chen, Wenhu
**日期:** 2025/10/12

## Abstract

Efficiently solving real-world problems with LLMs increasingly hinges on their ability to interact with dynamic web environments and autonomously acquire external information. While recent research like Search-R1 and WebDancer demonstrates strong performance in solving web tasks, they heavily rely on additional tools to convert the interactive web environment into static text content. This is in contrast to human browsing behaviors, which involve diverse interactions with the browser, such as scrolling, clicking, and typing. In this paper, we propose BrowserAgent, a more interactive agent that solves complex tasks through human-inspired browser actions. BrowserAgent operates directly on raw web pages via Playwright through a set of predefined browser actions. We adopt a two-stage training (Supervised Fine-Tuning (SFT) and Rejection Fine-Tuning (RFT)) to improve the model's generalization abilities. Despite using significantly less training data than Search-R1, BrowserAgent achieves more competitive results across different Open-QA tasks. Additionally, we introduce an explicit memory mechanism to store key conclusions across steps, further enhancing the model's reasoning capabilities for long-horizon tasks. Notably, BrowserAgent-7B can achieve around 20\% improvement over Search-R1 on multi-hop QA tasks like HotpotQA, 2Wiki, and Bamboogle. These results indicate that BrowserAgent can serve as a more advanced framework for more interactive and scalable web agents.

## 文件

- `2510.10666.pdf` — 论文原文
- `meta.json` — 结构化元数据
