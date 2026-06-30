# REALTALK: A 21-Day Real-World Dataset for Long-Term Conversation

**arXiv:** [2502.13270](https://arxiv.org/abs/2502.13270)
**PDF:** [下载](https://arxiv.org/pdf/2502.13270) · 本地: `2502.13270.pdf`
**作者:** Lee, Dong-Ho, Maharana, Adyasha, Pujara, Jay, Ren, Xiang, Barbieri, Francesco
**日期:** 2025/02
**GitHub:** [danny911kr/REALTALK](https://github.com/danny911kr/REALTALK)
**名称:** RealTalk

## Abstract

Long-term, open-domain dialogue capabilities are essential for chatbots aiming to recall past interactions and demonstrate emotional intelligence (EI). Yet, most existing research relies on synthetic, LLM-generated data, leaving open questions about real-world conversational patterns. To address this gap, we introduce REALTALK, a 21-day corpus of authentic messaging app dialogues, providing a direct benchmark against genuine human interactions. We first conduct a dataset analysis, focusing on EI attributes and persona consistency to understand the unique challenges posed by real-world dialogues. By comparing with LLM-generated conversations, we highlight key differences, including diverse emotional expressions and variations in persona stability that synthetic dialogues often fail to capture. Building on these insights, we introduce two benchmark tasks: (1) persona simulation where a model continues a conversation on behalf of a specific user given prior dialogue context; and (2) memory probing where a model answers targeted questions requiring long-term memory of past interactions. Our findings reveal that models struggle to simulate a user solely from dialogue history, while fine-tuning on specific user chats improves persona emulation. Additionally, existing models face significant challenges in recalling and leveraging long-term context within real-world conversations.

## 文件

- `2502.13270.pdf` — 论文原文
- `meta.json` — 结构化元数据
