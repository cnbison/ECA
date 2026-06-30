# Agent Memory Techniques

**收录日期:** 2026-05

**GitHub:** [https://github.com/NirDiamant/Agent_Memory_Techniques](https://github.com/NirDiamant/Agent_Memory_Techniques)

## 简述

30 runnable Jupyter notebooks on memory for LLM agents: conversation buffers, vector stores, knowledge graphs, episodic and semantic memory, MemGPT, Mem0, Letta, Zep, Graphiti, LoCoMo benchmarks, and production patterns.

## GitHub README 摘要

> **Learn every agent memory technique for LLM agents.**

## README 摘录（GitHub）

```markdown
# 🧠 Agent Memory Techniques

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/hero_dark.png">
    <img src="images/banner.png" alt="Agent Memory Techniques for LLMs: 30 runnable Jupyter notebooks covering every major memory pattern" width="100%"/>
  </picture>
</p>

**Learn every agent memory technique for LLM agents.**

> ⭐  **If you find this useful, please star the repo** so more learners can discover it.

> 🧭  **New here?** Start with [01 Conversation Buffer Memory](all_techniques/01_conversation_buffer_memory/) or pick a [Learning Path](#-learning-paths). Prefer a visual? See the [Decision Tree](#-which-technique-do-i-need) below. 30 runnable Jupyter notebooks covering conversation buffers, vector stores, knowledge graphs, episodic and semantic memory, working memory, MemGPT, Mem0, Letta, Zep, Graphiti, LoCoMo benchmarks, and production memory patterns.

<p align="center">
  <a href="https://www.apache.org/licenses/LICENSE-2.0"><img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg" alt="License: Apache 2.0"></a>
  <a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="Python 3.10+"></a>
  <a href="https://jupyter.org/"><img src="https://img.shields.io/badge/Jupyter-Notebook-orange.svg" alt="Jupyter"></a>
  <a href="https://github.com/NirDiamant/Agent_Memory_Techniques/stargazers"><img src="https://img.shields.io/github/stars/NirDiamant/Agent_Memory_Techniques?style=social" alt="GitHub Stars"></a>
  <a href="https://github.com/NirDiamant/Agent_Memory_Techniques/issues"><img src="https://img.shields.io/github/issues/NirDiamant/Agent_Memory_Techniques" alt="Issues"></a>
  <a href=".github/CONTRIBUTING.md"><img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg" alt="Contributions Welcome"></a>
</p>

---

<p align="center">
  <a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=social-linkedin&target=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fnir-diamant-759323134%2F&text=LinkedIn"><img src="https://img.shields.io/badge/LinkedIn-Connect-blue" alt="LinkedIn"></a>
  <a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=social-twitter&target=https%3A%2F%2Ftwitter.com%2FNirDiamantAI&text=Twitter"><img src="https://img.shields.io/twitter/follow/NirDiamantAI?label=Follow%20%40NirDiamantAI&style=social" alt="Twitter"></a>
  <a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=social-reddit&target=https%3A%2F%2Fwww.reddit.com%2Fr%2FEducationalAI%2F&text=Reddit"><img src="https://img.shields.io/badge/Reddit-Join%20our%20subreddit-FF4500?style=flat-square&logo=reddit&logoColor=white" alt="Reddit"></a>
  <a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=social-discord&target=https%3A%2F%2Fdiscord.gg%2FcA6Aa4uyDX&text=Discord"><img src="https://img.shields.io/badge/Discord-Join%20our%20community-7289da?style=flat-square&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=sponsor-github&target=https%3A%2F%2Fgithub.com%2Fsponsors%2FNirDiamant&text=Sponsor"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=ff69b4" alt="Sponsor"></a>
</p>

## 📖 Go deeper on RAG

<div align="center">

<a href="https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=agent-memory-techniques--readme&amp;click=book-buy-gumroad-rag-image&amp;target=https%3A%2F%2Fdiamant-ai.com%2Frag-made-simple%3Fcode%3DRAGKING&amp;retarget=0&amp;text=book-buy-gumroad-rag-image"><img src="images/rag_book_best_seller.png" alt="RAG Made Simple" width="360"></a>

**[RAG Made Simple](https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=agent-memory-techniques--readme&click=book-buy-gumroad-rag-cta&target=https%3A%2F%2Fdiamant-ai.com%2Frag-made-simple%3Fcode%3DRAGKING&retarget=0&text=book-buy-gumroad-rag-cta)** - the 400-page visual guide to RAG, by the author of this repo.
Amazon Bestseller in Generative AI · 1,500+ readers · ⭐ 4.6

**[Get it - 33% off with code RAGKING →](https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=agent-memory-techniques--readme&click=book-buy-gumroad-rag-cta&target=https%3A%2F%2Fdiamant-ai.com%2Frag-made-simple%3Fcode%3DRAGKING&retarget=0&text=book-buy-gumroad-rag-cta)** · [Read Chapter 1 free](https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=agent-memory-techniques--readme&click=free-chapter&target=https%3A%2F%2Fdiamant-ai.com%2Frag-made-simple%2Fchapter-1&retarget=0&text=free-chapter)

</div>


---

## 📫 Stay Updated

<div align="center">
<table>
<tr>
<td align="center">🚀<br><b>Weekly<br>Updates</b></td>
<td align="center">💡<br><b>Expert<br>Insights</b></td>
<td align="center">🎯<br><b>Top 0.1%<br>Content</b></td>
</tr>
</table>

<a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=newsletter-subscribe-button&target=https%3A%2F%2Fdiamantai.substack.com%2F%3Fr%3D336pe4%26utm_campaign%3Dpub-share-checklist&text=Subscribe%20to%20DiamantAI%20Newsletter"><img src="images/subscribe-button.svg" alt="Subscribe to DiamantAI Newsletter"></a>

*Join over 50,000 readers getting clear AI tutorials every week.* ***Subscribers also get early access and a 33% discount on my book.***
</div>

<a href="https://europe-west1-amt-views-tracker.cloudfunctions.net/amt-tracker?notebook=main-readme&click=newsletter-subscribe-image&target=https%3A%2F%2Fdiamantai.substack.com%2F%3Fr%3D336pe4%26utm_campaign%3Dpub-share-checklist&text=DiamantAI%20newsletter"><img src="images/substack_image.png" alt="DiamantAI newsletter"

... (更多内容请访问上面 GitHub 链接)
```

