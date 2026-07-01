---
marp: true
theme: default
paginate: true
backgroundColor: #ffffff
style: |
  section { font-family: -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif; }
  section h1 { color: #1a4480; border-bottom: 3px solid #1a4480; padding-bottom: 0.3em; }
  section h2 { color: #1a4480; }
  section blockquote { border-left: 4px solid #6aa1d8; color: #444; }
  section table { font-size: 0.7em; }
  section img { max-height: 480px; }
  section small { color: #888; }
  .lead { text-align: center; }
  .lead h1 { border: none; }
---

<!-- slide 1 -->
# Cognitive Architecture & Applications
## 认知架构与 ECOS 应用 — 过程汇报

**汇报人**：Bisen
**项目**：ECOS (Educational Cognitive Operating System)
**日期**：2026-07-01
**对象**：项目负责人

> *本文档已索引全部 research/ 与 wu-ecos/ 资料，可直接 `pandoc` 转 PPTX*

---

<!-- slide 2 -->
## 汇报背景

- **任务来源**：项目负责人希望了解认知架构方面研究的阶段性进展
- **进度素材**：research/ 内 8 份思考文档 + wu-ecos/ 图集 + 2 份业务演示
- **核心问题**：
  - 理论走到哪里？（外部 / 内部多轮研判）
  - 工程切到哪里？（MVP 落地路径）
  - 市场需求对接何处？（学生场景演示）
- **本汇报的一句话主张**：
  > *真正重要的不是模块本身，而是模块之间的 **Transformation**（转换函数）*

---

<!-- slide 3 -->
## 汇报大纲

1. 课题定位 — 为什么做认知架构
2. 理论演进 — 从 ECA 到 Transformation
3. 关键转折 — 三层反思、四点共识
4. 关键词 — Transformation 协议
5. MVP 切入点 — 从"模拟脑"到"压缩认知"
6. ECOS 现状 — 四张图、Cognitive Twin Agent
7. 案例演示 — 初二学生 4 周 / 四年级分数
8. 路线图 — Phase 1–4
9. 当前进展与下一步
10. 资源索引

---

<!-- slide 4 -->
## 一、为什么做认知架构（市场 / 工程 / 理论三重需要）

| 视角 | 现状 | 缺失 |
|:--|:--|:--|
| **市场** | AI Agent 大量涌现，但"记忆"普遍停留在向量库 / JSON | 长期跨会话认知演化 |
| **工程** | LangChain / MCP / Letta 等解决单点问题（Prompt / Tool / Memory） | 缺统一的 **认知运行时** |
| **理论** | ACT-R（30+ 年）/ SOAR（40+ 年）/ OpenCog（20+ 年）未成工业标准 | 缺一条"用工程可验证"的认知科学路径 |

> **ECOS 目标**：在三者交集处建立 *Cognitive Evolution Runtime*，前 18 个月聚焦 `Experience → Concept` 单条转换链。

---

<!-- slide 5 -->
## 二、理论演进路线（4 份 GPT/Gemini 研判）

```
GPT v1          ──►   GPT v2        ──►   GPT v3          ──►   现在
"九层架构"            "ECA 仍          "不模拟整个人脑"
ECA 1.0               偏软件工程"        MVP = 3 个 Transformation
                       ↓                  ↓                  ↓
                    Gemini02           Cognition            ECOS
                    补充 CoALA         Pipeline02           MVP
                    Neuroca            八层反思              (现状)
                                       ↓
                                       从"分层" → "循环"
                                       从"模块" → "Transformation"
```

> **认知的本质不是存储信息，而是持续降低不确定性、提高预测能力，并在新经验到来时不断 Rewrite。**

---

<!-- slide 6 -->
## 三、关键转折：三层反思

### ① 认知不是"层"，而是"循环"
- 之前的 `Event → Memory → … → Metacognition` 是数据库，不是大脑
- 真正的 Pipeline 应该是 Evolution Loop，认知一直在 **Rewrite**

### ② Knowledge ≠ Memory 的升级
- Memory 答"发生了什么"，Knowledge 答"为什么"
- 真实链路应为 `Experience → Memory → Rule Discovery → Knowledge`

### ③ Concept 才是认知起点
- 1000 条 `苹果 / 香蕉 / 梨` → `水果`：世界第一次被压缩
- **认知 ≈ Entropy Reduction**——这就是为什么 Memory Accuracy 不是优化目标

---

<!-- slide 7 -->
## 四、关键词：Transformation（认知转换函数）

> 所有项目都在研究 `Memory / Knowledge / Planner` 模块；真正缺失的是它们之间的 **Transformation**。

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

<!-- slide 8 -->
## 五、MVP 切入点选择 — 认知压缩，不是认知模拟

**过去的雄心**：做一个完整认知架构（覆盖全部 Transformation）。

**第三轮反思后的判断**：

| 维度 | 旧立场 | 新立场 |
|:--|:--|:--|
| 范围 | 模拟整个脑 | 解决一个基础问题 |
| 能力 | 全部自研 | 只做 TRL ≥ 6 的部分 |
| 世界模型 / 元学习 | 必有 | 暂时拿掉 |
| MVP | 完整系统 | **3 个 Transformation** `Event → Experience → Concept` |

> **成功平台的共性**：先解决一个基础问题（PyTorch→Tensor，LangChain→Prompt，MCP→Tool）。

---

<!-- slide 9 -->
## 六、ECOS 现状 — 四张图集（wu-ecos/）

```
       ┌─────────────────────┐         ┌─────────────────────┐
图1 →  │ BeliefState 坐标系   │ ⟵填充── │ 图4 达标状态 B       │
       │ (模板)              │         │ (Claude Skills)     │
       └──────────┬──────────┘         └──────────▲──────────┘
                  │ 描述                          │ 输出
       ┌──────────┴──────────┐         ┌──────────┴──────────┐
图2 →  │ 测量栈 L0–L5       │ ⟶实跑── │ 图3 测量轨迹        │
       │ (架构)             │         │ (Claude Skills)     │
       └─────────────────────┘         └─────────────────────┘
```

- **图1 ↔ 图4**：图4 是图1 坐标系的一次具体填充（达标快照）
- **图2 ↔ 图3**：图3 是图2 测量栈的一次具体实跑（conf 0.40 → 0.86）

---

<!-- slide 10 -->
## 六、ECOS 心智模型 — 状态 + 测量 = CTA

![w:600](wu-ecos/ecos-cognitive-architecture-loop.png)

- **WHAT（状态表征）** = `BeliefState`：5D 资源 × Bloom 深度 × TC × 误概念
- **HOW（测量栈）** = CTA 的 L0–L5 数学栈：BKT / MIRT / DKT / CD-CAT
- **CTA** = Cognitive Twin Agent：用测量栈把行为反推成 BeliefState

> **LLM 只碰两端**（感知层 / 解释层），数值估计全部交给数学栈——这就是 `A→B` 可信、可证伪的前提。

---

<!-- slide 11 -->
## 六、BeliefState 坐标系 — 一个认知状态由什么描述

![w:900](wu-ecos/ecos-cognitive-state-beliefstate.png)

| 维度 | 含义 |
|:--|:--|
| **5D 资源** | K (Knowledge) · P (Procedure) · S (Strategy) · C (Confidence) · X (eXperience) |
| **6 阶 Bloom 深度** | Remember → Understand → Apply → Analyze → Evaluate → Create |
| **TC 阈值概念** | 触发质变的关键断言（如 "skill = 模型按 description 自主加载"） |
| **Misconceptions** | 5 个具体误概念（M1–M5），逐一清零 |
| **Genetic footprint** | DNA + Trajectory，可追溯成长路径 |

> **完整状态 = 5 × 6 = 30 格网格**，外加 TC、误概念、轨迹。

---

<!-- slide 12 -->
## 七、案例演示 1 — 初二学生小张 4 周完整流程

| 周次 | 经历 | Runtime 决策 | Concept 演化 |
|:--:|:--|:--|:--|
| W1 | 听讲 + 课内练习 | 是否压缩？否 | — |
| W2 | 错题 + 反思 | 触发 Rule Miner | "辅助线是几何策略" |
| W3 | 单元测验 72 分 | 触发 Concept Builder | "时间分配能力不足" |
| W4 | 跨题迁移成功 | 触发认知画像更新 | "适合项目驱动学习" |

![w:600](wu-ecos/ecos-measurement-trace-claude-skills.png)

> **完整文档**：`research/2026-06-25-ecos-workflow-demo.md`（842 行工程参考版）

---

<!-- slide 13 -->
## 七、案例演示 2 — 四年级"分数"学习之旅（家长友好版）

- **情境**：小明对"分数 = 两个整数"的直觉错误认识
- **3 阶段干预**：
  - 操作阶段：分饼 → 建立"等分"概念
  - 表达阶段：图像 → 语言 → 符号
  - 迁移阶段：1/2 + 1/3 ≠ 2/5 的反直觉发现
- **Runtime 自动追踪**：
  - 5D 中 K 与 P 的差异化上升
  - Bloom 从 Remember → Understand 自动跨越
  - M1 误概念（"分子分母独立"）从 0.78 → 0.05

![w:600](wu-ecos/ecos-beliefstate-claude-skills-stateB.png)

> **完整文档**：`research/05-user-friendly-demo.md`（944 行面向家长/教师版）

---

<!-- slide 14 -->
## 八、路线图 — 4 个 Phase

| 阶段 | 核心目标 | 是否原创 | 时间 |
|:--|:--|:--|:--:|
| **Phase 1** | Event → Experience → Memory | 工程验证 / 集成为主 | M1–M6 |
| **Phase 2** | Experience → Rule → Concept | **第一创新点** | M7–M12 |
| **Phase 3** | Concept → Cognitive Profile | **第二创新点** | M13–M18 |
| **Phase 4** | Cognitive Runtime SDK | **平台化** | M19–M24 |

> **World Model 与 Meta-learning 暂时拿掉** —— 它们对第一代产品既难验证、也难体现价值。
> 第一代产品的差异化 = *系统能不能自动从经历中抽出越来越准确的概念，并形成可解释的认知画像*。

---

<!-- slide 15 -->
## 九、当前进展与下一步

### 已完成（截至 2026-07）
- 8 份 research/ 思考文档（PPT/Gemini 多轮研判）
- wu-ecos/ 4 张图 + 1 张架构总览（PNG + SVG 双版本）
- 2 份业务演示（教师友好版 / 家长友好版）
- 1 份 4 周 / 4 年级 双场景流程演示
- Transformation 协议的理论框架（七条 T1–T7）

### 下一步
1. **MVP 编码**：Phase 1 用 6 周工程验证 `Event → Memory`
2. **指标定义**：每个 Transformation 配 1 个可验证指标（如 Concept 数 / Bloom 跨越率）
3. **合作沟通**：把这套框架与一家 K12 机构对接，做真实学生样本
4. **对外发布**：每月一份 concept evolution 报告，建立领域话语权

---

<!-- slide 16 -->
## 十、资源索引

### 思考脉络（research/）
- `Cognition-Pipeline-GPT.md` — 第一轮认知流水线
- `Cognition-Pipeline-GPT02.md` — 八层反思（从层到循环）
- `Cognition-Pipeline-GPT03.md` — 三层九节 → MVP 落地
- `External-Cognitive-Architecture-GPT02.md` — 对 Gemini 回答的研判
- `External-Cognitive-Architecture-Gemini02.md` — Gemini 二次回应

### 业务演示（research/）
- `2026-06-25-ecos-workflow-demo.md` — 初二学生 4 周完整学习流程
- `05-user-friendly-demo.md` — 四年级"分数"学习之旅（家长/教师友好版）

### 架构图集（wu-ecos/）
- 4 张 PNG + 1 份 README（认知坐标系 / 测量栈 / 实跑 / 达标 B）

### 生成 PPTX
```bash
pandoc cognitive-architecture-report-slides.md -o report.pptx
```

---

<!-- _class: lead -->
# Q & A

**项目**：ECOS — Educational Cognitive Operating System
**核心主张**：从"模块"到"Transformation"，从"模拟脑"到"压缩认知"
**下一步**：6 周 MVP 工程验证 + K12 真实样本对接
