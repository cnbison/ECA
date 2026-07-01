# Cognitive Architecture & Applications

## 认知架构与 ECOS 应用 · 过程汇报

| 项目 | 内容 |
|:--|:--|
| 汇报人 | Bisen |
| 项目 | ECOS (Educational Cognitive Operating System) |
| 日期 | 2026-07-01 |
| 对象 | 项目负责人 |

> **本汇报的一句话主张**：真正重要的不是模块本身，而是模块之间的 *Transformation*（认知转换函数）。ECOS 要做的是 *Cognitive Evolution Runtime*，前 18 个月聚焦单条转换链 `Experience → Concept`。

---

## 一、汇报背景与目标

项目负责人希望了解认知架构方面研究的阶段性进展。经过多轮思考，目前已经把课题从"做完整的认知架构"收敛到"先做 *Experience → Concept* 这条最关键的转换链"。

**重要纠正（务必先说）**：

ECOS 不只是"规划中的设想"，而是已经是一项工程化项目。独立仓库位于 `/Users/loubicheng/project/ecos/`：

- **Phase 0 已 100% 完成（v0.19.0，2026-06-25）** —— 19 个版本 / 57+ 份研究文档 / 19,000+ 行
- **战略层（4）+ 工程层（5）+ 教学法层（4）+ MVP 设计（1） + P0 借鉴（5） = 19 份核心文档**
- **`ecos/` Python 包结构已搭好**：cta（认知孪生）、lca（学习教练）、bloom（目标空间）、dual_agent（互校）、persistence、session、orchestrator、llm_client
- **`pyproject.toml` + 18+ 份 discussions/ + 96KB CHANGELOG.md + CLAUDE.md 全部就位**

本仓库（ECA）放的是"展示给项目负责人的过程材料 + 三份业务演示 + 4 张核心架构图"。理论母体是 `/Users/loubicheng/project/ecos/`。

汇报使用的素材：

- `research/` 目录下 8 份研究思考文档（4 轮 GPT/Gemini 研判 + 反思）
- `wu-ecos/` 图集（4 张核心架构图 + 总览 SVG）
- 三份业务演示：
  - **案例 1（小张 4 周）**：`research/2026-06-25-ecos-workflow-demo.md`
  - **案例 2（小明分数）**：`research/05-user-friendly-demo.md`
  - **案例 3（Claude Skills，本次新增）**：在 wu-ecos/ 四张图中实际跑通的达标实例
- 所有底层理论/工程实现见 `/Users/loubicheng/project/ecos/`

汇报分五个部分：

1. 行业全景：别人走到哪、缺什么、ECOS 站什么位置
2. 理论脉络：走了哪些路、做对了什么、改掉了什么
3. 当前定位：从 ECA 到 Transformation，从"模拟脑"到"压缩认知"
4. ECOS 已落地状态：CTA / LCA / BeliefState / 三案例
5. MVP 切入点：四阶段路线、工程风险与下一步

---

## 二、行业全景：五条路线与 ECOS 的位置

> 关键引文（Gemini02 §一）：*"让 AI 记住 10,000 条聊天记录，AI 依然只是在计算下一个 Token 的概率，它并没有因为记住了这些事实而产生抽象能力。"*
>
> *——这是 "记住了 ≠ 理解了" 这条核心论断的出处，也是 ECOS 选择以 Concept Evolution 为差异化的根本理由。*

整个外置认知架构领域已经自发形成五条路线：

```
第一代  Prompt Memory           — Mem0 / LangMem / SuperMemory
  ↓
第二代  Long-term Memory        — Letta (MemGPT) / Zep
  ↓
第三代  Knowledge Memory        — Graphiti / Cognee / LightRAG
  ↓
第四代  External Cognition      — （目前几乎空白，ECOS 切入此层）
  ↓
第五代  Digital Twin / 2nd Brain — SelfLab / AiBeing / OpenHer
```

GitHub 上 90% 的项目停留在一二代（仅做记忆），少量进入三代（图谱），真正进四代（认知）的几乎没有。

ECOS 的定位：

| 维度 | 选择 | 理由 |
|:--|:--|:--|
| 路线归属 | 第四代 External Cognition | 在 Knowledge 之上，向 Concept / World Model 推进 |
| 行业角色 | 不是"又一个 Memory 框架"，而是 *Cognitive Evolution Runtime* | 与 PyTorch、LangGraph 同级的基础设施 |
| 场景切入 | 教育（K12）→ 通用平台 | 教育场景天然有"长期目标 + 持续反馈 + 数据闭环" |
| 核心抽象 | CTA（Cognitive Twin Agent）= BeliefState + 测量栈 | 与 Cognee Memory Control Plane 同级，但加决策与演化 |

---

## 三、为什么做认知架构

认知架构并不是新课题，但市面上研究三十多年始终没有真正成工业标准——ACT-R 三十多年、SOAR 四十多年、OpenCog 二十多年。原因都是自顶向下先画全图再实现，越做越复杂。

AI 真正成功的项目几乎都是先解决一个基础问题：PyTorch 做 Tensor，LangChain 做 Prompt，MCP 做 Tool Protocol。这就是 ECOS 切入角度的方法论。

从需求侧看，三重缺失同时存在：

| 视角 | 现状 | ECOS 切入 |
|:--|:--|:--|
| 市场 | AI Agent 大量涌现，"记忆"普遍停留在向量库 / JSON 之上 | 长期跨会话的认知演化 |
| 工程 | LangChain / MCP / Letta 等解决单点问题 | 认知运行时缺失 |
| 理论 | ACT-R / SOAR 等缺工程可验证路径 | "先小后大"的认知科学路径 |

**ECOS 的目标**：在市场 × 工程 × 理论三者交集处，建立 *Cognitive Evolution Runtime*，前 18 个月聚焦 `Experience → Concept` 单条转换链的可验证闭环。

---

## 四、理论演进路线

认知架构的思考经历了多轮迭代。以下是 7 份关键文档的脉络（注意：在 `cognitive-architecture-report.md` 初版中漏了 ECA-GPT01 和 Gemini01 这两份基础性文档）：

```
GPT v1  (Cognition-Pipeline-GPT)
  九层架构 ECA 1.0
  + 教育场景的 Learning Model
        ↓
ECA-GPT01 + Gemini01 (原始)
  五条路线画像：竞品定位 + Cognee ECL Pipeline / Graphiti Temporal KG
  + 四大工程障碍（概念漂移 / 状态爆炸 / 主观量化 / 基座依赖）
        ↓
GPT v2  (Cognition-Pipeline-GPT02)
  八层反思：认知不是层，是循环
  从分层到 Evolution Loop
        ↓
GPT ↔ Gemini v2  (External-Cognitive-Architecture-GPT02 / Gemini02)
  Gemini 引用 CoALA / Neuroca，引用"记住了 ≠ 理解了"
  GPT 补充 Transformation 概念
        ↓
GPT v3  (Cognition-Pipeline-GPT03)
  不模拟整个脑，只做 3 个 Transformation
  MVP = Event → Experience → Concept
        ↓
现在
  ECOS MVP 落地，Phase 1–4 路线 + CTA / BeliefState 设计
```

每一轮迭代推翻一个前轮的隐含假设：

- v1 → v1.5：把"九层架构"放回到 *五条路线* 行业地图里——避免做"第 N 个 Memory 框架"
- v2 → v2.5：从 *分层* 改成 *Evolution Loop*——认知不是 Storage，是 Rewrite
- v2.5：把 *Knowledge 当成 Memory 的升级* 错——它实际来自 *Rule Discovery*
- v3：把 *试图模拟整个人脑* 错——只做 TRL ≥ 6 的部分

**贯穿全集的一句核心**：

> 认知的本质不是存储信息，而是持续降低不确定性、提高预测能力，并在新的经验到来时不断 *Rewrite*。这一立场直接呼应 GPT01 提出的"四代 External Cognition"——ECOS 站的位置正是第四代。

---

## 五、关键转折：四层反思

第一轮迭代最大的变化是从分层走向循环。之前的画法：

```
Reality → Event → Experience → Memory → Knowledge → Concept → World Model
```

这张图的问题是"这是数据库，不是大脑"——它只有 *Storage*，没有 *Evolution*。真正的大脑永远是：

```
经历 → 重新解释 → 重新组织 → 重新命名 → 重新预测 → 重新行动
```

认知一直在 Rewrite。所以真实的 Pipeline 应该是这样的循环：

```
         ┌────────────────────────┐
         ▼                        │
Experience                         │
   ↓                               │
Memory ◀──────────┐                │
   ↓             │                │
Knowledge        │                │
   ↓             │                │
Concept          │                │
   ↓             │                │
World Model      │                │
   ↓             │                │
Prediction       │                │
   ↓             │                │
Action           │                │
   ↓             │                │
New Experience ──┴────────────────┘
```

第二层是 *Knowledge ≠ Memory 的升级*。Memory 回答"发生了什么"，Knowledge 回答"为什么"，两者不是一层而是两种不同的数据。Knowledge 实际来自 *Rule Discovery*，所以正确的链路应是：

```
Experience → Memory → Rule Discovery → Knowledge
```

第三层是 *Concept 才是认知真正的起点*。1000 条 `苹果 / 香蕉 / 梨` 自动涌现出 `水果`——这是世界第一次被压缩。**认知 ≈ Entropy Reduction（熵减）**，这就是为什么 *Memory Accuracy* 不是优化目标，*Concept Compression* 才是。

第四层（GPT01 提示但 v2/v3 简中漏掉的）：**Learning Model 是教育场景的专属层**。GPT01 §三 明确指出：

> *"对于教育场景，还需要再增加一层 **Learning Model**，用于持续建模学习者的能力结构、知识状态、学习策略与成长轨迹。"*

这是 ECOS 与通用 Cognitive Architecture（SOAR / ACT-R）的关键差异：通用架构问"AI 如何思考"，Learning Model 问"**这一个学生** 如何学"。BeliefState 中 5D 的 K/P/S/C/X 五个维度恰好对应学习模型的五要素：

| 学习模型要素 | 5D 维度 |
|:--|:--|
| 知识结构 | K (Knowledge) |
| 学习策略 | S (Strategy) |
| 经验基础 | X (eXperience) |
| 元认知状态 | C (Confidence) |
| 程序性能力 | P (Procedure) |

---

## 六、关键词 Transformation

从 Gemini 那份分析得到的最大启发：所有项目都在研究模块（Memory / Knowledge / Planner），但真正缺失的是它们之间的 **Transformation**。如果有人问"Memory 怎么变成 Knowledge"，"Knowledge 怎么变成 Concept"，"Concept 怎么形成 World Model"——目前没人研究。

真正值得投入的是 **Transformation Functions**，而不是模块本身。在 T1–T7 之上另加上三条与教育/认知演化直接相关的扩展：

| 编号 | 转换 | 输入 | 输出 | 与 BeliefState 的关系 |
|:--:|:--|:--|:--|:--|
| T1 | Experience Encoding | Event | Experience | 写入 5D 中的 X + S |
| T2 | Memory Consolidation | Experience | Long Memory | 衰减 vs 巩固，X 中的高置信经验上升 |
| T3 | Rule Mining | 1000 Experiences | Knowledge Rule | 写入 5D 中的 K |
| T4 | Concept Formation | Knowledge | Concept Tree | 写入 Bloom 高阶（Understand/Apply） |
| T5 | Abstraction | Concept | Compressed Concept | 完成 Concept 层级压缩 |
| T6 | Prediction Learning | Concept | Predictive Model | 改变 World Model 字段（暂未实现） |
| T7 | Meta Reflection | Everything | Rewrite Spec | 触发 Confidence 重新校准 |
| **T8** | **Misconception Clearing** | **K + Bloom** | **M_i 清零** | **BeliefState 误概念维度** |
| **T9** | **Goal Update** | **Meta Reflection + Outcome** | **新目标层级** | **调整 Attention（Phase 5 候补）** |
| **T10** | **Learning Profile Update** | **以上全部** | **Student Cognitive Profile** | **生成 Phase 3 的 Cognitive Profile** |

**真正需要原创的不是这些模块，而是它们之间的 Transformation Protocol。**

可复用基建位置（之前漏提）：

| Transformation | 建议复用 |
|:--|:--|
| T2 (Memory Consolidation) | Cognee ECL Pipeline (Extract → Cognify → Load) |
| T3 (Rule Mining) | Graphiti Temporal Knowledge Graph |
| T4–T5 (Concept Formation) | 聚类 + Ontology Learning（聚类用 sklearn，命名用 LLM） |

---

## 七、MVP 切入点选择

经过第三轮反思，MVP 范围被大幅收敛：

| 维度 | 旧立场 | 新立场 |
|:--|:--|:--|
| 范围 | 模拟整个脑 | 解决一个基础问题 |
| 能力 | 全部自研 | 只做 TRL ≥ 6 的部分 |
| World Model / Meta-learning | 必有 | 暂时拿掉 |
| MVP | 完整认知系统 | **3 个 Transformation**：`Event → Experience → Concept` |
| Phase 5 候补 | — | Goal System（T9） |

为什么 `Concept` 如此关键？因为只要 Concept 真的自动成长，这件事就已经和所有 Memory 不同。例如：

- 今天：学生考试失败
- 十天后：系统自动生成概念"时间管理能力不足"
- 100 天后：更新为"学习风格偏视觉型"
- 一年后：形成"认知画像 · 适合项目驱动学习"

**这是 Concept Evolution，不是 Memory。**

成功平台的共性：解决一个基础问题（MCP 做 Tool / PyTorch 做 Tensor / LangChain 做 Prompt）。MVP 越窄，越能被工程验证，越早进入真实场景迭代。

数据闭环——这是教育场景独有的可验证路径（GPT01 §七）：

| 信号来源 | 闭环作用 |
|:--|:--|
| 学习行为（点击、停留、答题） | T1 / T2 的输入 |
| 测试结果（分数、错题） | T3 的规则验证 |
| 反思记录（学生日记 / 教练对话） | T4–T7 的质量评估 |
| 跨题迁移是否成功 | Concept 是否真正稳定的唯一判据 |

---

## 八、工程风险与应对（之前漏掉的关键一节）

Gemini01 §四 列出外置认知架构尚未跨越的四大障碍。ECOS 必须正面回应：

| 障碍 | 在 ECOS 中的具体表现 | 应对策略 |
|:--|:--|:--|
| 1. **概念漂移与记忆退化** | Concept 自动生长后会漂移到不准确方向；增量学习破坏原有认知 | Concept Stability 指标 + Concept Re-evaluation 周期任务 |
| 2. **状态爆炸与推理延迟** | BeliefState 5D × Bloom = 30 格 + TC + 误概念 + 轨迹 → 全状态查询是 O(n) | 测量栈分 L0–L5：热数据放 L0（实时），冷数据按需降级 |
| 3. **主观确定性量化** | Confidence / Goal / Emotion 等难以严格量化 | 测量栈用 BKT/MIRT/CD-CAT 给出数值估计 + Bootstrap 置信区间，避免 LLM 直接给数字 |
| 4. **基座模型依赖** | LLM 仅在感知与解释两端，必须对模型能力下降有韧性 | 测量栈独立于 LLM 数值估计；LLM 只负责结构化行为输入与对人话解释；且降级到更小基座时仍能用 |

**核心原则**（呼应 wu-ecos README 的三条核心观点）：

> LLM 只碰两端（感知层 / 解释层），数值估计全部交给数学栈——这就是 `A → B` 可信、可证伪的前提。

---

## 九、ECOS 现状：CTA + 四张图 + BeliefState 四闸门

ECOS 的核心抽象叫 **CTA（Cognitive Twin Agent）**，由一对紧耦合的东西组成：

- **WHAT（状态表征）** = `BeliefState`：一套带置信度的认知状态坐标系
- **HOW（测量栈）** = L0–L5 数学栈（BKT / MIRT / DKT / CD-CAT），把行为反推成 BeliefState

### 9.1 ECA v1 九层 ↔ BeliefState 5D × Bloom 字段映射

之前漏掉的一步——把 v1 的"九层"对到 BeliefState 实际字段上：

| ECA v1 九层 | 对应 BeliefState 字段 | 当前实现 |
|:--|:--|:--|
| Event Layer | 输入信号（非 BeliefState 字段） | 已实现（JSON Schema） |
| Experience Layer | 5D-X | 已实现（结构化对象） |
| Memory Layer | 5D-X + 5D-C 部分 | 已实现（SQLite） |
| Knowledge Layer | 5D-K | 部分实现（Rule Mining） |
| Concept Layer | Bloom + Concept 层级 | **核心创新点**（Phase 2） |
| Cognition Layer | Inference 引擎 | Phase 2 候选 |
| World Model Layer | Prediction 字段 | 暂未实现（Phase 5） |
| Goal System | Attention 调节器 | 暂未实现（Phase 5） |
| Metacognition Layer | Confidence 字段 | 部分实现（T7） |

第十层（教育专属）：**Learning Model** = 以上全部 + Student Cognitive Profile 输出。

### 9.2 四张核心图之间的关系

```
       ┌─────────────────────┐         ┌─────────────────────┐
图1 →  │ BeliefState 坐标系   │ ⟵填充── │ 图4 达标状态 B       │
       │ (模板)              │         │ (Claude Skills 实例) │
       └──────────┬──────────┘         └──────────▲──────────┘
                  │ 描述                          │ 输出
       ┌──────────┴──────────┐         ┌──────────┴──────────┐
图2 →  │ 测量栈 L0–L5       │ ⟶实跑── │ 图3 测量轨迹        │
       │ (架构)             │         │ (Claude Skills 实跑) │
       └─────────────────────┘         └─────────────────────┘
```

- 图 1 ↔ 图 4：图 4 是图 1 坐标系的一次具体填充（达标快照）
- 图 2 ↔ 图 3：图 3 是图 2 测量栈的一次具体实跑（conf 从 0.40 收敛到 0.86）

### 9.3 BeliefState 的 5 维构成

| 维度 | 含义 |
|:--|:--|
| 5D 资源 | K (Knowledge) · P (Procedure) · S (Strategy) · C (Confidence) · X (eXperience) |
| 6 阶 Bloom | Remember → Understand → Apply → Analyze → Evaluate → Create |
| TC 阈值概念 | 触发质变的关键断言 |
| Misconceptions | 5 个具体误概念，逐项清零 |
| Genetic footprint | DNA + Trajectory，可追溯成长路径 |

完整状态 = 5 × 6 = 30 格，外加 TC、误概念、轨迹。

### 9.4 BeliefState 达标的"四闸门"（wu-ecos/README.md 案例约定）

之前的汇报没把这条命题说死——可信、可证伪度的一个关键：

1. **TC 跨越**：核心阈值概念被重新陈述且通过 anti-test
2. **Bloom 阈值**：Understand ≥ 0.85 ∧ Apply ≥ 0.75（不要求 Create 满级）
3. **误概念清零**：所有 M_i 的置信度低于阈值（如 0.05）
4. **C 是挣来的**：伪置信 = false，即 Confidence 来自正确证据而非模仿

### 9.5 三条贯穿全集的核心观点

1. 认知状态是"信念分布"，不是"点"——每个值都带置信度，`A → B` 是分布的移动
2. 状态 = 5D 资源 × Bloom 深度 的网格——5D（K/P/S/C/X）说"用哪种本事"，Bloom 说"到什么火候"
3. LLM 只碰两端（感知层 / 解释层），数值估计全部交给数学栈——这就是 `A → B` 可信、可证伪的前提

### 9.6 异步运行机制：Night Cognition

GPT01 §九 提到元认知层应"定时异步运行，类似人类睡眠、复盘与长期成长"。ECOS 落地这一点：

| 节奏 | 触发 | 主要做哪些 Transformation |
|:--|:--|:--|
| 实时（每次交互） | Event 流入 | T1 (Experience Encoding) |
| 每晚 (daily) | 0:00 触发 | T2 (Memory Consolidation) + T3 (Rule Mining 部分) |
| 每周 (weekly) | 周日触发 | T7 (Meta Reflection) + T8 (Misconception Clearing) |
| 每月 (monthly) | 月初触发 | T5 (Abstraction) + T10 (Learning Profile Update 候选) |
| 跨样本 | 新 Event 大量涌入 | T4 (Concept Formation) |

这一调度机制是 *Cognitive Evolution Runtime* 这个名字里"Runtime"的真正含义——它不只是调度，还包含时间维度的认知重组。

---

## 十、案例演示：三个真实跑通的场景

> 项目负责人之前收到的两版案例（小张 4 周 / 小明分数）都来自业务演示文档，本次汇报补充 wu-ecos/ 四张图所围绕的第三个核心案例 —— Claude Skills 学习，它是一个**已经收敛到具体 BeliefState 字段 + 五条具体误概念 + 四闸门达标线**的完整闭环。

### 案例 1（最完整）：Claude Skills 学习 —— wu-ecos 四张图就是为这个案例画的

**情景**：学生从"完全不知道 Claude Skill 是什么"出发，把 Skill 概念学到能在正确场景判断并写出最小可用 Skill。

**完整的 BeliefState 字段定义**（这是 ECOS 中可直接编码的部分）：

| 维度 | 状态值 |
|:--|:--|
| 5D-K | Knowledge 维度已具备 Skill 元定义 |
| 5D-P | Procedure 维度能写出 YAML frontmatter |
| 5D-S | Strategy 维度能在"该用 Skill" vs"该用 hook/MCP"时正确分流 |
| 5D-C | Confidence 维度从初始 0.40 → 达标 0.86（CD-CAT 5 步收敛） |
| 5D-X | Experience 维度记录每次 Skill 调用案例 |
| Bloom | Understand ≥ 0.85 + Apply ≥ 0.75（不要求 Create 满级） |
| TC_skill | "skill 是模型按 description 相关性*自主*加载的能力，不是宏、不是外部进程" |
| Misconceptions (5) | M1 斜杠命令 / M2 MCP server / M3 任意自动化 hook / M4 prompt 模板 / M5 总是被加载 |

**四闸门达标线**：

| 闸门 | 标准 | 本案例状态 |
|:--|:--|:--|
| ① TC 跨越 | TC_skill 能被 anti-test 重新陈述且不被绕开 | ✓ |
| ② Bloom 阈值 | Understand ≥ 0.85 ∧ Apply ≥ 0.75 | ✓（conf 0.86）|
| ③ 误概念清零 | M1–M5 全部降到 0.05 以下 | ✓ |
| ④ C 是挣来的 | 伪置信 = false | ✓ |

**最硬的判定证据**：两个"否决"场景——

1. 该用 hook 的情况：学生能正确拒绝用 Skill 并说对理由（"hook 是监听事件，Skill 是按 description 自主加载"）
2. 该用 MCP 的情况：学生能正确拒绝用 Skill 并说对理由（"MCP 是协议，Skill 是模型自行加载的扩展"）

这是无法靠背定义伪造的。完整图集见 `wu-ecos/` 4 张 PNG + 1 份 README。

### 案例 2（业务演示）：初二学生小张 4 周完整流程

针对一个真实学生在 W1–W4 的关键节点，Runtime 自动决策过程：

| 周次 | 经历 | Runtime 决策 | Concept 演化 | 对应 T# |
|:--:|:--|:--|:--|:--|
| W1 | 听讲 + 课内练习 | 实时编码：T1 | — | T1 |
| W2 晚 | 错题 + 反思 | Night: T2 + T3 | "辅助线是几何策略"（Rule） | T2 T3 |
| W2–3 | 单元测验 72 分 | 触发 T3 + T4 | "时间分配能力不足"（Concept） | T3 T4 |
| W4 | 跨题迁移成功 | Weekly: T7 + T10 候选 | "适合项目驱动学习"（Profile） | T7 T10 |

用 BeliefState 四闸门表述达标路径：

| 闸门 | 状态 |
|:--|:--|
| ① TC 跨越 | "辅助线是几何策略" 已能被 anti-test 验证 |
| ② Bloom 阈值 | Understand ≥ 0.85、Apply ≥ 0.75 达到 |
| ③ 误概念清零 | "做几何只能拼凑"的 M_i 降到 0.05 |
| ④ C 是挣来的 | Confidence 来自真实做题数据，非模仿 |

完整文档见 `research/2026-06-25-ecos-workflow-demo.md`（842 行工程参考版）。

### 案例 3（家长友好）：四年级"分数"学习之旅

情境：小明对"分数 = 两个整数"有直觉错误认识。三阶段干预：

- **操作阶段**：分饼 → 建立"等分"概念
- **表达阶段**：图像 → 语言 → 符号
- **迁移阶段**：1/2 + 1/3 ≠ 2/5 的反直觉发现

Runtime 自动追踪到：

- 5D 中 K 与 P 差异化上升
- Bloom 从 Remember 自动跨越到 Understand
- M1 误概念（"分子分母独立"）从 0.78 → 0.05

完整文档见 `research/05-user-friendly-demo.md`（944 行面向家长/教师版）。

### 三个案例的关系

| 案例 | 工程深度 | 受众 | 价值 |
|:--|:--|:--|:--|
| 案例 1 Claude Skills | 完整 BeliefState 字段 + 误概念 + 达标线 | 工程团队 + 项目负责人 | **证明 CTA 测量栈真的能跑通一个可达标的状态估计** |
| 案例 2 小张 4 周 | 14 份核心文档协同工作 | 工程团队 | 证明双 Agent 互校 + Runtime 调度能驱动真实学习循环 |
| 案例 3 小明分数 | 操作→表达→迁移 三阶段 | 家长 / 教师 / 合作方 | 用通俗场景证明 ECOS 在认知状态层面"理解学生 + 改变学生" |

三个案例互补：案例 1 是**状态估计工程化**的样板，案例 2 是**双 Agent 互校运行**的样板，案例 3 是**对外讲解**的样板。

---

## 十一、路线图

整个项目分四阶段：

| 阶段 | 核心目标 | 是否原创 | 时间 | 主要 T# |
|:--|:--|:--|:--:|:--|
| Phase 1 | Event → Experience → Memory | 工程验证 / 集成为主 | M1–M6 | T1 T2 |
| Phase 2 | Experience → Rule → Concept | **第一创新点** | M7–M12 | T3 T4 T5 |
| Phase 3 | Concept → Cognitive Profile | **第二创新点** | M13–M18 | T10 + Memory ≠ Cognition 验证 |
| Phase 4 | Cognitive Runtime SDK | **平台化** | M19–M24 | T7 + Night Cognition 平台化 |
| Phase 5（候补） | Goal System / World Model | 第三创新点 | M25+ | T9 T6 |

World Model 与 Meta-learning 暂时拿掉——不是因为不重要，而是它们对第一代产品既难验证、也难体现价值。

第一代产品的差异化 = 系统能不能持续从经历中抽出越来越准确、越来越稳定的概念，并据此形成可解释的认知画像。

---

## 十二、当前进展与下一步

**已完成（截至 2026-07）** —— 区分"研究文档"和"工程实现"两个层面

### 12.1 ECOS 主项目（`/Users/loubicheng/project/ecos/`）

| 层级 | 数量 | 状态 |
|:--|:--|:--|
| Phase 0 战略层文档 | 4/4 | ✅ 100% |
| Phase 0 工程层文档（CTA / LCA / Bloom / 互校 / 持久化） | 5/5 | ✅ 100% |
| Phase 0 教学法层文档 | 4/4 | ✅ 100% |
| Phase 0 MVP 设计文档 | 1/1 | ✅ 100%（598 行 / 12 章节 / 4 个核心假设 H1–H4）|
| P0 借鉴体系（40-aibeing-borrowing） | 4 份 + 1 README | ✅ 100% |
| MIGRATION-FROM-SELFLAB.md | 1 份 | ✅ |
| deep-research 顶层综合 | 1 份 v2.0 | ✅ |
| `ecos/` Python 包结构 | cta/lca/bloom/dual_agent/persistence/session/orchestrator/llm_client | ✅ 骨架 |
| `pyproject.toml` + `CLAUDE.md` + 96KB CHANGELOG.md | 3 件 | ✅ |
| discussions/ 工作日志 | 18 份 | ✅ 持续 |
| Phase 0 总版本 | v0.19.0 | ✅ 已封板 |

### 12.2 本仓库（`/Users/loubicheng/project/ECA/`）

| 层级 | 数量 | 状态 |
|:--|:--|:--|
| research/ 思考脉络文档 | 8 份（Cognition × 3 + ECA × 4 + 业务演示 × 2）| ✅ 100% |
| wu-ecos/ 架构图集 | 4 张 PNG + 1 份 SVG + 1 份 README | ✅ 100% |
| 过程汇报材料 | 1 份（本文档）| ✅ 100% |
| 三个对照演示案例 | Claude Skills / 小张 4 周 / 小明分数 | ✅ 全部能讲清楚 |
| Transformation 协议 | T1–T10 框架 | ✅ |
| BeliefState 字段定义（5D × Bloom × TC × 误概念 × Genetic footprint） | 已落地 | ✅ |
| CTA 测量栈数学基础（BKT / MIRT / DKT / CD-CAT） | wu-ecos 图 2 已绘 | ✅ |
| Phase 4 启动（Phase 0 完成后下一步） | 待启动 | ⏳ |

**当前已启动但未完成的关键工作**

- BeliefState 四闸门验证算法的工程化（CLAUDE.md 列为 Phase 4 任务）
- Concept Stability 指标的统计检验设计
- 数据闭环中"反思记录"接入的产品形态

**下一步（Phase 4 实施期）**

1. **MVP 编码（M2，4–6 周）**：按 `research/90-mvp/README.md` §4–6 的 W1–W8 任务分解，把 CTA 测量栈 / LCA 策略 / 双 Agent 互校 / 持久化 四个模块各跑一次
2. **指标定义（M2 同步）**：每个 Transformation 配 1 个可验证指标，例如 Concept 数、Bloom 跨越率、误概念清零率、Concept Stability
3. **学校招募（M3，2–4 周）**：与 1 家 K12 合作机构对接，招募 50–100 名初一/初二学生
4. **假设验证（M3）**：跑 H1–H4 四个核心假设的实验组 / 对照组
5. **对外发布**：每月一份 *concept evolution* 报告，建立领域话语权

---

## 附录 A：资源索引

### A.1 本仓库（`/Users/loubicheng/project/ECA/`）

**思考脉络（research/）**

- `Cognition-Pipeline-GPT.md` — 第一轮认知流水线（含 Learning Model）
- `Cognition-Pipeline-GPT02.md` — 八层反思（从分层到循环）
- `Cognition-Pipeline-GPT03.md` — 三层反思 → MVP 落地
- `External-Cognitive-Architecture-GPT.md` — 五条路线画像 + 竞品定位
- `External-Cognitive-Architecture-GPT02.md` — 对 Gemini 回答的研判
- `External-Cognitive-Architecture-Gemini.md` — 行业全景 + 四大工程障碍
- `External-Cognitive-Architecture-Gemini02.md` — "记住了 ≠ 理解了"核心论断

**三个对照演示案例（research/）**

- 案例 1（最完整）：`wu-ecos/` 4 张图 + README = **Claude Skills 学习**
- 案例 2（业务演示）：`research/2026-06-25-ecos-workflow-demo.md` — 初二学生小张 4 周完整流程
- 案例 3（家长友好）：`research/05-user-friendly-demo.md` — 四年级小明"分数"之旅

**架构图集（wu-ecos/）**

- `ecos-cognitive-state-beliefstate.png/svg` — 认知状态坐标系
- `ecos-measurement-stack.png` — 测量栈
- `ecos-measurement-trace-claude-skills.png` — Claude Skills 实跑轨迹
- `ecos-beliefstate-claude-skills-stateB.png` — 达标状态 B 实例
- `ecos-cognitive-architecture-loop.png` — 架构总览

**过程汇报（research/）**

- `cognitive-architecture-report.md` — 本文档

**配套设计图（仓库根）**

- `Cognition-Pipeline-compact.md` — 认知流水线精简版
- `External-Cognitive-Architecture-compact.md` — ECA 精简版

### A.2 ECOS 主项目（`/Users/loubicheng/project/ecos/`）

> **本仓库的过程材料只是 ECOS 项目的对外展示。所有底层理论 / 工程实现 / 实验代码的主仓都在这里。**

**入口**

- `README.md` — ECOS 完整说明（含与 SelfLab 并列的定位说明）
- `CLAUDE.md` — Claude Code 协作指南（含阶段边界、实验代码约定）
- `CHANGELOG.md` — 96KB / 19 份版本演进
- `pyproject.toml` — Python 包配置

**研究文档（已 19 份 / Phase 0 完成）**

- `research/00-overview/` — 战略层 4 份（applications / architecture / roadmap / risks）
- `research/10-engineering/` — 工程层 5 份
  - `01-cta-belief-engine.md` — CTA 测量栈
  - `02-lca-policy-engine.md` — LCA 教练策略
  - `03-bloom-goal-library.md` — Bloom 目标空间
  - `04-dual-agent-calibration.md` — 双 Agent 互校
  - `05-persistence-session.md` — 持久化与会话
- `research/20-pedagogy/` — 教学法层 4 份（认知结构 / Bloom / 策略 / ZPD）
- `research/30-shared-cognitive-tools/` — 共享认知科学工具
- `research/40-aibeing-borrowing/` — P0 借鉴体系 5 份
- `research/90-mvp/README.md` — MVP 设计 v1.0 / 598 行 / 12 章节 / H1–H4
- `research/deep-research/Cognitive-Digital-Twin-Deep-Research.md` v2.0
- `research/MIGRATION-FROM-SELFLAB.md` — 从 SelfLab 迁移说明
- `research/README.md` — research/ 索引

**工程代码（`ecos/` 包）**

- `ecos/cta/` — Cognitive Twin Agent（状态估计）
- `ecos/lca/` — Learning Coach Agent（策略优化）
- `ecos/bloom/` — Bloom 目标空间
- `ecos/dual_agent/` — 双 Agent 互校
- `ecos/persistence/` — 持久化
- `ecos/session/` — 会话管理
- `ecos/orchestrator.py` — 调度
- `ecos/llm_client.py` — LLM 客户端

**工作日志（`discussions/` 18 份）**

- 完整的每日讨论 → 决策记录
- 关键里程碑：2026-06-25 v0.19.0 Phase 0 收官

---

## 附录 B：ECOS 立项以来的认识论轨迹

把这份汇报之前的所有演变摆出来，让项目负责人理解"为什么最终停在现在这个选择"：

1. v1（GPT01）：试图做完整的九层认知架构。教育场景追加 Learning Model。
2. v1.5（Gemini01 + ECA-GPT01）：对照行业五条路线，找出空白在"四代 External Cognition"。
3. v2（GPT02）：认知不是分层，是循环——加上 Evolution Loop。
4. v2.5（GPT ↔ Gemini v2）：核心论断是 *记住了 ≠ 理解了*；方向收敛到 Concept。
5. v3（GPT03）：MVP 收窄到 3 个 Transformation，聚焦 `Experience → Concept`。
6. 现在（ECOS Phase 1–4）：CTA + BeliefState + 测量栈 + Night Cognition，工程化落地。

这一轨迹的关键特征：**每一步都推翻前一步的一个隐含假设**，最终不是大而全的认知架构，而是一条 *可验证、可证伪、可工程化的认知演化最小路径*。

---

## 汇报结尾

> 整个 ECOS 项目已经从"建一个完整的认知架构"收敛为"建一个认知演化运行时（Cognitive Evolution Runtime）"，第一个 MVP 是验证 `Experience → Concept Evolution` 这条目前几乎没人真正解决的转换链。
>
> **截至 2026-07，ECOS 已不是"规划中的设想"**：Phase 0（19 份核心研究文档）已 100% 完成；`ecos/` Python 包骨架已搭好；三个对照案例（Claude Skills / 小张 4 周 / 小明分数）能完整跑通故事。
>
> **下一步是 Phase 4 实施期**：按 `/Users/loubicheng/project/ecos/research/90-mvp/README.md` 的 W1–W8 任务分解，用 4–6 周做工程 MVP（M2），2–4 周做实验分析（M3），验证 H1–H4 四个核心假设。
>
> 同时我们已经识别行业的四大未跨越障碍（概念漂移 / 状态爆炸 / 主观量化 / 基座依赖），并把每一项的应对策略落到 BeliefState 四闸门 + 测量栈 + Night Cognition 这一组合上——这是 ECOS 与其他"高级外置硬盘"型项目的本质区别。

任何阶段需要回顾详细理论、具体案例细节、工程实现路径：

- **本仓库 `/Users/loubicheng/project/ECA/`** 放的是过程汇报材料 + 三个对照案例 + 4 张核心架构图
- **主仓库 `/Users/loubicheng/project/ecos/`** 放的是 19 份研究文档 + Python 包代码 + 完整讨论日志
