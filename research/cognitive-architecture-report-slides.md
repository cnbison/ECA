# Cognitive Architecture & Applications

## 认知架构与 ECOS 应用 · 过程汇报

| 项目 | 内容 |
|:--|:--|
| 汇报人 | Bisen |
| 项目 | ECOS (Educational Cognitive Operating System) |
| 日期 | 2026-07-01 |
| 对象 | 项目负责人 |

> **本汇报的一句话主张**：真正重要的不是模块本身，而是模块之间的 *Transformation*（认知转换函数）。

---

## 一、汇报背景与目标

项目负责人希望了解认知架构方面研究的阶段性进展。经过多轮思考，目前已经把课题从"做完整的认知架构"收敛到"先做 *Experience → Concept* 这条最关键的转换链"。

汇报使用的素材：

- `research/` 目录下 8 份研究思考文档（4 轮 GPT/Gemini 研判 + 反思）
- `wu-ecos/` 图集（4 张核心架构图 + 总览 SVG）
- `research/2026-06-25-ecos-workflow-demo.md` 与 `research/05-user-friendly-demo.md` 两份业务演示

汇报分四个部分：

1. 理论脉络：走了哪些路、做对了什么、改掉了什么
2. 当前定位：从 ECA 到 Transformation，从"模拟脑"到"压缩认知"
3. MVP 切入点：ECOS 现状与四阶段路线
4. 案例与下一步

---

## 二、为什么做认知架构

认知架构并不是新课题，但市面上研究三十多年始终没有真正成工业标准——ACT-R 三十多年，SOAR 四十多年，OpenCog 二十多年。原因：它们都是自顶向下先画全图再实现，越做越复杂。

AI 真正成功的项目几乎都是先解决一个基础问题：PyTorch 做 Tensor、LangChain 做 Prompt、MCP 做 Tool Protocol。这就是 ECOS 切入角度的方法论。

从需求侧看，三重缺失同时存在：

| 视角 | 现状 | 缺失 |
|:--|:--|:--|
| 市场 | AI Agent 大量涌现，但"记忆"普遍停留在向量库 / JSON 之上 | 长期跨会话的认知演化 |
| 工程 | LangChain / MCP / Letta 等解决单点问题 | 缺统一的认知运行时 |
| 理论 | ACT-R / SOAR 等缺工程可验证路径 | 缺一条"先小后大"的认知科学路径 |

**ECOS 的目标**：在市场 × 工程 × 理论三者交集处，建立 *Cognitive Evolution Runtime*，前 18 个月聚焦单条转换链 `Experience → Concept`。

---

## 三、理论演进路线

认知架构的思考经历了多轮迭代。以下是 4 份关键文档的脉络：

```
GPT v1  (Cognition-Pipeline-GPT)
  "九层架构" ECA 1.0
        ↓
GPT v2  (Cognition-Pipeline-GPT02)
  八层反思：认知不是层，是循环
  从分层到 Evolution Loop
        ↓
External-Cognitive-Architecture-GPT02/Gemini02
  Gemini 引用 CoALA / Neuroca，GPT 补充 Transformation 概念
        ↓
GPT v3  (Cognition-Pipeline-GPT03)
  不模拟整个脑，只做 3 个 Transformation
  MVP = Event → Experience → Concept
        ↓
现在
  ECOS MVP 落地，Phase 1–4 路线
```

每一轮迭代推翻一个前一轮的隐含假设：

- 第一轮推翻"只要分层合理就够" → 改成循环
- 第二轮推翻"Knowledge 是 Memory 的升级" → 改成 Rule Discovery 衍生的独立产物
- 第三轮推翻"试图模拟整个人脑" → 改成只做 TRL ≥ 6 的部分

**贯穿全集的一句核心**：

> 认知的本质不是存储信息，而是持续降低不确定性、提高预测能力，并在新的经验到来时不断 Rewrite。

---

## 四、关键转折：三层反思

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

第二层是*Knowledge ≠ Memory 的升级*。Memory 回答"发生了什么"，Knowledge 回答"为什么"，两者不是一层而是两种不同的数据。Knowledge 实际来自 *Rule Discovery*，所以正确的链路应是：

```
Experience → Memory → Rule Discovery → Knowledge
```

第三层是 *Concept 才是认知真正的起点*。1000 条 `苹果 / 香蕉 / 梨` 自动涌现出 `水果`——这是世界第一次被压缩。**认知 ≈ Entropy Reduction（熵减）**，这就是为什么 *Memory Accuracy* 不是优化目标，*Concept Compression* 才是。

---

## 五、关键词 Transformation

从 Gemini 那份分析得到的最大启发：所有项目都在研究模块（Memory / Knowledge / Planner），但真正缺失的是它们之间的 **Transformation**。如果有人问"Memory 怎么变成 Knowledge"，"Knowledge 怎么变成 Concept"，"Concept 怎么形成 World Model"——目前没人研究。

真正值得投入的是 **Transformation Functions**，而不是模块本身：

| 编号 | 转换 | 输入 | 输出 |
|:--:|:--|:--|:--|
| T1 | Experience Encoding | Event | Experience |
| T2 | Memory Consolidation | Experience | Long Memory |
| T3 | Rule Mining | 1000 Experiences | Knowledge Rule |
| T4 | Concept Formation | Knowledge | Concept Tree |
| T5 | Abstraction | Concept | Compressed Concept |
| T6 | Prediction Learning | Concept | Predictive Model |
| T7 | Meta Reflection | Everything | Rewrite Spec |

**真正需要原创的不是这些模块，而是它们之间的 Transformation Protocol。**

---

## 六、MVP 切入点选择

经过第三轮反思，MVP 范围被大幅收敛：

| 维度 | 旧立场 | 新立场 |
|:--|:--|:--|
| 范围 | 模拟整个脑 | 解决一个基础问题 |
| 能力 | 全部自研 | 只做 TRL ≥ 6 的部分 |
| World Model / Meta-learning | 必有 | 暂时拿掉 |
| MVP | 完整认知系统 | **3 个 Transformation**：`Event → Experience → Concept` |

为什么 `Concept` 如此关键？因为只要 Concept 真的自动成长，这件事就已经和所有 Memory 不同。例如：

- 今天：学生考试失败
- 十天后：系统自动生成概念"时间管理能力不足"
- 100 天后：更新为"学习风格偏视觉型"
- 一年后：形成"认知画像 · 适合项目驱动学习"

**这是 Concept Evolution，不是 Memory。**

成功平台的共性：解决一个基础问题（MCP 做 Tool / PyTorch 做 Tensor / LangChain 做 Prompt）。MVP 越窄，越能被工程验证，越早进入真实场景迭代。

---

## 七、ECOS 现状：CTA + 四张图

ECOS 的核心抽象叫 **CTA（Cognitive Twin Agent）**，由一对紧耦合的东西组成：

- **WHAT（状态表征）** = `BeliefState`：一套带置信度的认知状态坐标系
- **HOW（测量栈）** = L0–L5 数学栈（BKT / MIRT / DKT / CD-CAT），把行为反推成 BeliefState

四张核心图之间的关系：

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

三条贯穿全集的核心观点：

1. 认知状态是"信念分布"，不是"点"——每个值都带置信度，`A → B` 是分布的移动
2. 状态 = 5D 资源 × Bloom 深度 的网格——5D（K/P/S/C/X）说"用哪种本事"，Bloom 说"到什么火候"
3. LLM 只碰两端（感知层 / 解释层），数值估计全部交给数学栈——这就是 `A → B` 可信、可证伪的前提

认知状态坐标系的构成：

| 维度 | 含义 |
|:--|:--|
| 5D 资源 | K (Knowledge) · P (Procedure) · S (Strategy) · C (Confidence) · X (eXperience) |
| 6 阶 Bloom | Remember → Understand → Apply → Analyze → Evaluate → Create |
| TC 阈值概念 | 触发质变的关键断言 |
| Misconceptions | 5 个具体误概念，逐项清零 |
| Genetic footprint | DNA + Trajectory，可追溯成长路径 |

完整状态 = 5 × 6 = 30 格，外加 TC、误概念、轨迹。

---

## 八、案例演示

### 案例 1：初二学生小张 4 周完整流程

针对一个真实学生在 W1–W4 的关键节点，Runtime 自动决策过程：

| 周次 | 经历 | Runtime 决策 | Concept 演化 |
|:--:|:--|:--|:--|
| W1 | 听讲 + 课内练习 | 是否压缩？否 | — |
| W2 | 错题 + 反思 | 触发 Rule Miner | "辅助线是几何策略" |
| W3 | 单元测验 72 分 | 触发 Concept Builder | "时间分配能力不足" |
| W4 | 跨题迁移成功 | 触发认知画像更新 | "适合项目驱动学习" |

完整文档见 `research/2026-06-25-ecos-workflow-demo.md`（842 行工程参考版）。

### 案例 2：四年级"分数"学习之旅

情境：小明对"分数 = 两个整数"有直觉错误认识。三阶段干预：

- **操作阶段**：分饼 → 建立"等分"概念
- **表达阶段**：图像 → 语言 → 符号
- **迁移阶段**：1/2 + 1/3 ≠ 2/5 的反直觉发现

Runtime 自动追踪到：

- 5D 中 K 与 P 差异化上升
- Bloom 从 Remember 自动跨越到 Understand
- M1 误概念（"分子分母独立"）从 0.78 → 0.05

完整文档见 `research/05-user-friendly-demo.md`（944 行面向家长/教师版）。

---

## 九、路线图

整个项目分四阶段：

| 阶段 | 核心目标 | 是否原创 | 时间 |
|:--|:--|:--|:--:|
| Phase 1 | Event → Experience → Memory | 工程验证 / 集成为主 | M1–M6 |
| Phase 2 | Experience → Rule → Concept | **第一创新点** | M7–M12 |
| Phase 3 | Concept → Cognitive Profile（认知画像） | **第二创新点** | M13–M18 |
| Phase 4 | Cognitive Runtime SDK | **平台化** | M19–M24 |

World Model 与 Meta-learning 暂时拿掉，不是因为不重要，而是它们对第一代产品既难验证、也难体现价值。

第一代产品的差异化 = 系统能不能持续从经历中抽出越来越准确、越来越稳定的概念，并据此形成可解释的认知画像。

---

## 十、当前进展与下一步

**已完成（截至 2026-07）**

- 8 份 research/ 思考文档（覆盖 GPT × 3 / Gemini × 2 / ECA × 2 / pipeline 演进）
- wu-ecos/ 4 张核心图 + 1 张架构总览（PNG + SVG 双版本）
- 2 份业务演示（教师友好版 / 家长友好版）
- 1 份 4 周 / 4 年级 双场景流程演示
- Transformation 协议的理论框架（七条 T1–T7）

**下一步**

1. **MVP 编码**：用 6 周工程验证 Phase 1 的 `Event → Memory`，把 BKT / MIRT / CD-CAT 跑通
2. **指标定义**：每个 Transformation 配 1 个可验证指标，例如 Concept 数、Bloom 跨越率、误概念清零率
3. **合作沟通**：把这套框架与一家 K12 机构对接，做真实学生样本，重点验证 Concept Formation 这条链
4. **对外发布**：每月一份 *concept evolution* 报告，建立领域话语权，让"Concept Evolution"成为这一类项目的标杆术语

---

## 附录：资源索引

### 思考脉络（research/）

- `Cognition-Pipeline-GPT.md` — 第一轮认知流水线
- `Cognition-Pipeline-GPT02.md` — 八层反思（从分层到循环）
- `Cognition-Pipeline-GPT03.md` — 三层反思 → MVP 落地
- `External-Cognitive-Architecture-GPT02.md` — 对 Gemini 回答的研判
- `External-Cognitive-Architecture-Gemini02.md` — Gemini 二次回应

### 业务演示（research/）

- `2026-06-25-ecos-workflow-demo.md` — 初二学生 4 周完整学习流程
- `05-user-friendly-demo.md` — 四年级"分数"学习之旅

### 架构图集（wu-ecos/）

- `ecos-cognitive-state-beliefstate.png/svg` — 认知状态坐标系
- `ecos-measurement-stack.png` — 测量栈
- `ecos-measurement-trace-claude-skills.png` — Claude Skills 实跑轨迹
- `ecos-beliefstate-claude-skills-stateB.png` — 达标状态 B 实例
- `ecos-cognitive-architecture-loop.png` — 架构总览

### 相关设计图（仓库根）

- `Cognition-Pipeline-compact.md` — 认知流水线精简版
- `External-Cognitive-Architecture-compact.md` — ECA 精简版

---

## 汇报结尾

> 整个项目已经从"建一个完整的认知架构"收敛为"建一个认知演化运行时（Cognitive Evolution Runtime）"，第一个 MVP 是验证 `Experience → Concept Evolution` 这条目前几乎没人真正解决的转换链。
>
> 这是我认为**既有研究价值、又有工程可行性、同时还能服务长期教育 AI 愿景**的最佳切入点。

下一步是 6 周 MVP 工程验证，加 K12 真实样本对接。任何阶段需要回顾详细理论或具体案例细节，本汇报引用的所有文档都在 `research/` 和 `wu-ecos/` 中可直接打开。
