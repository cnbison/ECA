# TokMem: One-Token Procedural Memory for Large Language Models

**arXiv:** [2510.00444](https://arxiv.org/abs/2510.00444)
**PDF:** [下载](https://arxiv.org/pdf/2510.00444) · 本地: `2510.00444.pdf`
**作者:** Wu, Zijun, Hao, Yongchang, Mou, Lili
**日期:** 2025/10/01

## Abstract

Large language models are typically controlled via prompts, which must be repeatedly re-processed for every new query and are difficult to reuse modularly. We introduce TokMem, a procedural memory framework that compiles each reusable task procedure into a single trainable memory token. Each token serves as both a procedure index and a generation control signal that steers generation, enabling targeted behaviors with constant-size overhead. TokMem keeps the backbone LLM frozen and stores procedural knowledge entirely in these dedicated units, so new procedures can be added continually without interfering with existing ones. We evaluate TokMem on two settings: atomic recall over 1,000 Super-Natural Instructions tasks and compositional recall on multi-step function-calling. Our results show that TokMem consistently outperforms retrieval-augmented prompting while avoiding repeated context overhead. Moreover, it matches or exceeds parameter-efficient fine-tuning with substantially fewer trainable parameters.

## 文件

- `2510.00444.pdf` — 论文原文
- `meta.json` — 结构化元数据
