# Metacognitive Reuse: Turning Recurring LLM Reasoning Into Concise Behaviors

**arXiv:** [2509.13237](https://arxiv.org/abs/2509.13237)
**PDF:** [下载](https://arxiv.org/pdf/2509.13237) · 本地: `2509.13237.pdf`
**作者:** Didolkar, Aniket, Ballas, Nicolas, Arora, Sanjeev, Goyal, Anirudh
**日期:** 2025/09/16

## Abstract

Large language models (LLMs) now solve multi-step problems by emitting extended chains of thought. During the process, they often re-derive the same intermediate steps across problems, inflating token usage and latency. This saturation of the context window leaves less capacity for exploration. We study a simple mechanism that converts recurring reasoning fragments into concise, reusable &#34;behaviors&#34; (name + instruction) via the model&#39;s own metacognitive analysis of prior traces. These behaviors are stored in a &#34;behavior handbook&#34; which supplies them to the model in-context at inference or distills them into parameters via supervised fine-tuning. This approach achieves improved test-time reasoning across three different settings - 1) Behavior-conditioned inference: Providing the LLM relevant behaviors in-context during reasoning reduces number of reasoning tokens by up to 46% while matching or improving baseline accuracy; 2) Behavior-guided self-improvement: Without any parameter updates, the model improves its own future reasoning by leveraging behaviors from its own past problem solving attempts. This yields up to 10% higher accuracy than a naive critique-and-revise baseline; and 3) Behavior-conditioned SFT: SFT on behavior-conditioned reasoning traces is more effective at converting non-reasoning models into reasoning models as compared to vanilla SFT. Together, these results indicate that turning slow derivations into fast procedural hints enables LLMs to remember how to reason, not just what to conclude.

## 文件

- `2509.13237.pdf` — 论文原文
- `meta.json` — 结构化元数据
