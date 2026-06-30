# su-memory

**收录日期:** 2026-04

**GitHub:** [https://github.com/su-memory/su-memory-sdk](https://github.com/su-memory/su-memory-sdk)

## 简述

su-memory SDK: Open-source memory engine for AI agents with causal reasoning, temporal awareness, and spatial cognition. Works as Memory component in VMC world model architecture.

## GitHub README 摘要

> ---

## README 摘录（GitHub）

```markdown
---
language:
  - zh
  - en
license: apache-2.0
tags:
  - semantic-memory
  - vector-search
  - causal-reasoning
  - rag
  - temporal-awareness
  - llm
  - python
  - chinese
  - retrieval-augmented-generation
  - local-first
  - error-handling
  - fallback
datasets:
  - su-memory/demo-data
library_name: su-memory
pypi: su-memory
---

# su-memory SDK v4.0 · Semantic Memory Engine

> **"你的 AI 记不住上次聊过什么？su-memory 给它一个不会忘的大脑。"**
>
> **"为什么这条建议？——点击查看完整推理链。"**
>
> v4.0：统一单一产品线（取消 Lite/LitePro 分级，全部能力释放）· 三路融合 MultiHopReader + 本地 LLM reader (MLX Qwen) · algebra 数学层（GF(2)³/概率图/群论）· 三路融合 MultiHopReader · FAISS + bge-m3 原生 batch
>
> **统一引擎**：`SuMemory` 一个类含全部能力（向量语义检索 + 多跳推理 + 因果推理 + 时空关联）。`SuMemoryLite`/`SuMemoryLitePro` 为向后兼容别名。

---

## 📊 性能基准（真实 HotpotQA，可复现）

> **真实可复现（标准 EM 口径）**（官方 HotpotQA validation，200 题，全 hard level，标准 EM 口径：reader 抽取 span == gold）：

| 系统 | HotpotQA 标准 EM | F1 |
|---|:---:|:---:|
| **su-memory v4.0 (DeepSeek + CausalDAG桥接)** | **62.5%** | **75.4%** |
| su-memory v4.0 (本地 7B reader) | 48.0% | 58.6% |
| Hindsight | 70.83% | — |
| IRRR + BERT | 55.0% | — |
| DFGN (pure retrieval) | 48.2% | — |

- su-memory 最强配置（DeepSeek reader + CausalDAG 罕见实体桥接）标准 EM **62.5%**、F1 **75.4%**，**真实超越 DFGN（48.2%）与本地 7B（48%）约 14 个百分点**；comparison 题 73.5% **已超 Hindsight**；CausalDAG 桥接发现率 90%（vs title 匹配 44%）；本地 7B reader 标准 EM 48.0%（轻量回退）
- **检索能力 SOTA 级**：支持事实双召回 Full@5 = 95%，答案词 94% 原样出现在召回段落（纯算法 span 抽取上限 ~89%）
- 复现：`python benchmarks/hotpotqa_full_eval.py`（标准 EM，自动用本地 MLX Qwen reader；`--no-llm` 回退启发式）

> **历史诚实声明**：
> - v3.x 曾宣称「58% 超 SOTA」——经核实为合成数据自测，已删除。
> - v4.0 早期曾宣称「82.5% 超 Hindsight」——经核实为**召回覆盖口径**（gold 词出现在召回段落，非 reader 精确抽取），与官方 EM 口径不符，**属口径虚标，已修正为标准 EM 48.0%**。
> - 当前最强配置（DeepSeek-V3 + CausalDAG 桥接）标准 EM 62.5% / F1 75.4%，**真实超越 DFGN(48.2%)与本地7B(48%)约14点，comparison题73.5%已超Hindsight**；CausalDAG罕见实体桥接发现率90%（vs title匹配44%，algebra层真实能力）；bridge题60.2%仍拖累整体，距Hindsight 70.83%差~8点。
> - 已系统验证所有路径（7B/DeepSeek/GLM reader × 直抽/多跳推理/CausalDAG桥接标注/span对齐/refine/self-consistency）。第一性原理分析表明：14.5点边界损失（F1 75.4% - EM 62.5%）源于 LLM 生成式答案与严格 EM 字符串匹配的固有不对齐（gold边界主观，无规则可循），不可被后处理消除。**Hindsight 70.83% 的优势来自专门的多跳架构微调**，真实突破需专属多跳模型微调或更强旗舰模型。
>
> 微基准与更多数字见 [BENCHMARK.md](BENCHMARK.md)（`python benchmarks/real_microbench.py` 复现）。

---

## 📚 文档

| 资源 | 说明 |
|------|------|
| [API 文档](https://su-memory.readthedocs.io) | Sphinx 自动生成的完整 API 参考 |
| [异常体系](src/su_memory/exceptions.py) | 42 ErrorCode 错误码速查 |
| [降级矩阵](docs/fallback-matrix.md) | 7 组件降级路径全景 |
| [迁移指南](docs/MIGRATION_v2.5_to_v2.6.md) | v2.5 → v2.6 迁移步骤 |
| [性能基准](BENCHMARK.md) | 真实可复现性能（honest benchmark） |
| [更新日志](CHANGELOG.md) | Keep a Changelog 格式 |

---

## ⚡ 安装

```bash
pip install su-memory
```

**一行代码，让 AI 拥有记忆能力：**

```python
from su_memory import SuMemory

client = SuMemory()
client.add("张总在周一会议上提到Q3目标增长25%")
results = client.query("Q3目标")  # 秒级返回，带推理路径
```

---

## ⚡ 安装指南

### 环境要求

- Python 3.10+
- 推荐使用虚拟环境 (venv) 或 conda

### 安装前检查

**重要**: 安装前请确认 `pip` 和 `python` 指向同一环境。

```bash
# 检查环境一致性
which python
which pip

# 如果不一致，使用以下方式安装
python -m pip install su-memory
```

### 安装方式

#### 方式1: 标准安装 (推荐)

```bash
pip install su-memory
```

> ✨ **开箱即用多跳推理** - 默认集成FAISS + sentence-transformers

#### 方式2: 使用 python -m pip (确保环境一致)

```bash
python -m pip install su-memory
```

#### 方式3: 从 GitHub 安装最新版本

```bash
pip install git+https://github.com/su-memory/su-memory-sdk.git
```

#### 方式4: 源码安装

```bash
git clone https://github.com/su-memory/su-memory-sdk.git
cd su-memory-sdk
pip install .
```

#### 方式5: 开发模式安装

```bash
git clone https://github.com/su-memory/su-memory-sdk.git
cd su-memory-sdk
pip install -e ".[dev]"
```

### 可选依赖

| 安装选项 | 命令 | 包含 |
|---------|------|------|
| **标准版** | `pip install su-memory` | ⭐ 核心 + FAISS + sentence-transformers |
| **完整版** | `pip install su-memory[full]` | + 向量存储 (Qdrant/SQLAlchemy) |
| **Dashboard** | `pip install su-memory[dashboard]` | + Flask可视化界面 |
| **REST API** | `pip install su-memory[api]` | + FastAPI + uvicorn |

```bash
# 标准版即包含多跳推理能力
pip install su-memory

# 可视化Dashboard
pip install su-memory[dashboard]
python -m su_memory.dashboard
# 访问 http://localhost:8765

# REST API（支持 JS/Go/curl 调用）
pip install su-memory[api]
uvicorn su_memory.api.server:app --reload --port 8000
# 访问 http://localhost:8000/docs 查看 API 文档
```

### 安装验证

安装完成后，运行验证脚本:

```bash
# 快速检查
python -c "from su_memory import SuMemoryLitePro; print('✅ 安装成功')"

# 完整验证
python -c "from su_memory.verify_install import main; main()"
```

### 常见问题排查

#### 问题1: ModuleNotFoundError

```
pip show su-memory  # 显示已安装
python -c "import su_memory"  # 报错
```

**原因**: pip 和 python 指向不同环境

**解决**:
```bash
python -m pip install --force-reinstall su-memory
```

#### 问题2: 环境不匹配警告

```
⚠️ pip 和 python 指向不同环境
```

**解决**:
```bash
# 方式1: 使用 python -m pip
python -m pip install su-memory

# 方式2: 创建虚拟环境
python -m venv myenv
source myenv/bin/activate
pip install su-memory
```

#### 问题3: 诊断工具

如果遇到其他问题，运行诊断工具:

```bash
python -c "from su_memory.diagnostics import main; main()"
```

---

## 🚀 快速开始

| 能力 | 用户感知价值 | 技术支撑 |
|------|-------------|----------|
| **记住一切** | 上周聊的项目，AI秒级回忆 | 本地向量存储 |
| **因果线索检测** | "为什么推荐这个？" | 基于中文连接词的关键词模式匹配（非统计因果推断） |
| **时间感知** | 越新的记忆越相关 | 时序衰减 |
| **可解释** | 推理路径透明可见 | Multi-hop RAG |

---

### 一行代码入门

```python
from su_memory import SuMemory

# 初始化（开箱即用多跳推理）
client = SuMemory()

# 添加记忆
client.add("用户偏好深色主题", metadata={"user": "alice"})
client.add("用户上周购买了笔记本电脑")

# 语义检索
results = client.query("电脑")

# 多跳推理（默认hybrid模式，向量+图谱融合）
chain = client.query_multihop("用户的购买偏好", max_hops=3)
```

### 推荐入口

| 类 | 场景 | 说明 |
|-----|------|------|
| **SuMemory** | ⭐推荐 | 一行代码，本地运行，简单易用 |
| SuMemoryLite | 轻量场景 | 内存<50MB |
| SuMemoryLitePro | 专业场景 | 向量推理+多跳 |

# 添加记忆
client.add("今天天气很好，阳光明媚")
client.add("明天可能下雨，记得带伞")
client.add("我喜欢学习编程")

# 查询记忆
results = client.query("天气", top_k=2)
for r in results:
    print(f"{r['content']} (score: {r['score']})")
```

### 增强版 Pro

```python
from su_memory.sdk import SuMemoryLitePro

# 创建增强版客户端
pro = SuMemoryLitePro(
    sto

... (更多内容请访问上面 GitHub 链接)
```

