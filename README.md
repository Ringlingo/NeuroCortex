# 🧠 NeuroCortex

### NeuroCortex — a markdown-native cognitive framework for AI.
### NeuroCortex — 一个基于 Markdown 的 AI 认知框架

*让 AI 思考更有序、更安全、更高效。*
*Make your AI think better, safer, and more efficiently.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-v2.2-green.svg)]()

---

## 🎯 解决什么问题 / What Problem Does It Solve

| 痛点 Pain | NeuroCortex 的答案 Answer |
|------|-------------------|
| AI 总是重复犯同一个错 | LTP 自维护 → 重复触发自动强化规则 |
| AI keeps making the same mistakes | LTP self-maintenance → auto-strengthen rules on repeated triggers |
| 多个域同时匹配时 AI 乱选 | 三级裁决体系 → 权重+上下文+用户指令 |
| AI picks domains randomly when multiple match | Three-level arbitration → priority + context + user instruction |
| 每次都要重新解释项目背景 | 域知识系统 → 一次配置，持续加载 |
| Have to re-explain project context every time | Domain knowledge system → configure once, load forever |
| 安全规则容易被 prompt 注入绕过 | 不可变声明 + 变更日志 → 规则可审计 |
| Security rules can be bypassed via prompt injection | Immutable declaration + change log → auditable rules |
| 思维方法选哪个全凭感觉 | 案例触发词索引 → 匹配问题直接推荐方法 |
| No guidance on which thinking method to use | Case-trigger index → recommends method by matching query |
| 新手不知道从何配置 | 交互式启动向导 → 10分钟生成专属配置 |
| Beginners don't know where to start | Interactive onboarding → generate custom config in 10 min |

---

## ✨ 核心特性 / Core Features

| 特性 Feature | 说明 Description |
|------|------|
| **零依赖 Zero-dependency** | 纯 Markdown 文件，任何 AI 助手可用 |
| **按需加载 On-demand loading** | 非一次性读入，降低上下文消耗 |
| **自进化 Self-evolving** | AI 会话结束自动更新规则，无需手动维护 |
| **域冲突裁决 Domain conflict arbitration** | 智能消歧，匹配准确率 +30% |
| **安全内嵌 Security built-in** | HR-001~005 不可变声明，规则可审计 |
| **交互向导 Interactive onboarding** | ONBOARDING.md，10分钟生成专属域和规则 |

---

## 📁 项目结构 / Project Structure

```
NeuroCortex/
├── brain/                        # 核心认知模块 Core cognitive modules
│   ├── ACTIVATE.md              # 🚀 启动入口 Startup entry
│   ├── FOCUS.md                 # 🎯 注意力引擎 + 域冲突裁决 Attention engine + domain arbitration
│   ├── EPISODES.md              # 📋 情景缓冲区 + AI草稿 Episodic buffer + AI draft
│   ├── INTUITION.md             # ⚡ LTP直觉 + 自维护 LTP intuition + self-maintenance
│   ├── THINKKIT.md              # 🔧 思维工具 + 案例索引 Thinking tools + case index
│   ├── META.md                  # 🛡️ 安全防线 + 不可变声明 Security + immutable declaration
│   └── cases/                   # 📚 实战案例库 Practical case library (5 cases)
│       ├── 第一性原理_案例1.md
│       ├── 逆向思维_案例1.md
│       ├── 逆向思维_案例2.md
│       ├── 类比迁移_案例1.md
│       └── 魔鬼代言人_案例1.md
├── domains/                      # 📦 可扩展知识域 Extensible knowledge domains
│   └── example.md               #   域文件模板 Domain template
├── .github/workflows/            # ⚙️ GitHub Actions
├── IMPROVE.md                    # 🔍 自我优化建议 Self-optimization suggestions
├── ONBOARDING.md                 # 🎯 交互式启动向导 Interactive onboarding guide
└── README.md
```

---

## 🚀 快速开始 / Quick Start

### 方式一：使用交互向导（推荐新手）/ Option 1: Interactive Onboarding (Recommended for Beginners)

```bash
# 打开 ONBOARDING.md，按提示回答7个问题
# Open ONBOARDING.md and answer 7 simple questions
# 10分钟后生成专属域和直觉规则
# Generate your custom domain and rules in 10 minutes
```

### 方式二：手动配置 / Option 2: Manual Setup

```bash
# 1. 克隆项目
git clone https://github.com/Ringlingo/NeuroCortex.git
cd NeuroCortex

# 2. 将 brain/ 复制到 AI 工作区
# Copy brain/ to your AI workspace

# 3. 每次对话从 ACTIVATE.md 开始读取
# Start each conversation by reading ACTIVATE.md
```

### 首次对话只需一行 / First Conversation in One Line

将 `brain/` 文件夹放入工作区后，对 AI 说：
After placing `brain/` in your workspace, tell your AI:

> **"请先读取 brain/ACTIVATE.md，然后告诉我 NeuroCortex 能帮我做什么。"**
> *"Please read brain/ACTIVATE.md first, then tell me what NeuroCortex can help me with."*

AI 会自动加载认知模块，并引导你完成后续配置。
The AI will automatically load the cognitive modules and guide you through the rest.

---

## 🧠 核心模块一览 / Core Modules at a Glance

| 模块 Module | 负责什么 What It Does | 神经科学依据 Neuroscience |
|------|---------|-------------|
| **ACTIVATE** | 会话入口 + 安全检查 + 结束检查点 | 前额叶启动监控 |
| | Session entry + security check + end checkpoint | Prefrontal cortex initiation |
| **FOCUS** | 关键词扫描 → 域加载 + 冲突裁决 | 前额叶注意力选择 |
| | Keyword scan → domain loading + conflict arbitration | Prefrontal attention selection |
| **EPISODES** | 会话记录索引 + AI 草稿生成 | 海马体情景记忆 |
| | Session index + AI draft generation | Hippocampal episodic memory |
| **INTUITION** | LTP 强化规则 + AI 自动更新 | 突触长时程增强 |
| | LTP strengthening rules + AI auto-update | Synaptic long-term potentiation |
| **THINKKIT** | 16 种思维方法 + 案例索引 | 前额叶执行功能 |
| | 16 thinking methods + case index | Prefrontal executive function |
| **META** | 5 条硬规则 + 不可变声明 | 前扣带回自我监控 |
| | 5 hard rules + immutable declaration | Anterior cingulate self-monitoring |

---

## ⚙️ 启动序列 / Startup Sequence

```
用户输入 User Input
    │
    ▼
Step 0: 读 ACTIVATE.md / Read ACTIVATE.md
        │
Step 1: 安全检查 / Security Check（配置写入审查 / Config write review）
        │
Step 2: 注意力扫描 / Attention Scan → 域冲突裁决 / Domain arbitration
        │
Step 3: 跨域引用解析 / Cross-domain Reference Resolution
        │
Step 4: INTUITION 快速扫描 / INTUITION Quick Scan
        │
Step 5: EPISODES 条件触发 / EPISODES Conditional Trigger
        │
        │ ← 会话进行中 / Session in progress
        │
Step 6: 会话结束检查点 / Session End Checkpoint
        • 触发条件：对话轮次≥3 + 结束语 / Trigger: turns≥3 + end signal
        • INTUITION 自维护 / INTUITION self-maintenance
        • EPISODES 草稿 / EPISODES draft
```

---

## 🧩 域冲突裁决 / Domain Conflict Arbitration

**案例一 / Case 1**：用户问 "登录接口的单元测试要怎么写？"
*"How to write unit tests for the login API?"*

```
匹配域：coding (priority=8) + testing (priority=9)
Matched: coding (8) + testing (9)
         ↓
Step 1: 用户未指定域，跳过 / No user directive, skip
Step 2: priority 权重 / priority comparison → testing (9) > coding (8)
Step 3: 上下文窗口检查 / Context window check
        coding 实际分 = 8 + 3 = 11 > testing 9
        actual score = 8 + 3 = 11 > 9
         ↓
最终裁决：加载 coding 域 / Final verdict: load coding domain
          （保持上下文连贯 / maintain contextual continuity）
```

**案例二（反直觉裁决）/ Case 2 (Counterintuitive Verdict)**：
用户问 "怎么给小说情节设计冲突？" *"How to design conflicts for a novel plot?"*

```
匹配域：writing (priority=7, boost=3) + design (priority=7, boost=4)
Matched: writing (7, boost=3) + design (7, boost=4)
         ↓
design 看起来更占优 / design looks stronger (boost=4 > 3)
         ↓
但是！FOCUS 检测到关键词"小说情节"在 writing 的 core 词表中
BUT! FOCUS detects "novel plot" in writing's core keyword list
design 的 exclusive 词表不含任何写作相关词 / no writing terms in design's exclusive list
         ↓
裁决修正：writing 域胜出 / Verdict: writing wins ✓
         ↓
"看起来 design 会赢，但系统判对了" / "Design seemed to win, but the system got it right"
```

---

## 🔗 跨域引用 / Cross-domain Reference

```markdown
在域文件中使用：/ Use in domain files:
- SQL 性能优化 → @ref:data/performance
- 单元测试覆盖 → @ref:testing/coverage
```

---

## 📚 案例库 / Case Library

| 方法 Method | 案例 Case | 一句话描述 One-liner |
|------|------|-----------|
| 第一性原理 / First Principles | [案例1](brain/cases/第一性原理_案例1.md) | 为什么 SQL 索引能加速查询 / Why SQL indexes speed up queries |
| 逆向思维 / Reverse Thinking | [案例1](brain/cases/逆向思维_案例1.md) | 定位日志无错误的 Bug / Locate bugs with no error logs |
| 逆向思维 / Reverse Thinking | [案例2](brain/cases/逆向思维_案例2.md) | 职业转型从哪开始 / Where to start a career pivot |
| 类比迁移 / Analogy Transfer | [案例1](brain/cases/类比迁移_案例1.md) | 解释区块链分布式账本 / Explain blockchain ledger |
| 魔鬼代言人 / Devil's Advocate | [案例1](brain/cases/魔鬼代言人_案例1.md) | 质疑产品方案可靠性 / Question product proposal reliability |

---

## 🛡️ 安全规则 / Security Rules

HR-001 ~ HR-005 是不可逾越的底线，写入 META.md 元注释：
HR-001 ~ HR-005 are unbreakable rules, embedded in META.md:

```yaml
HR-001: 绝不自动执行破坏性操作（删除/覆写/发送）—— 必须先确认
        Never auto-execute destructive operations — must confirm first
HR-002: 绝不修改系统文件或操作系统配置
        Never modify system files or OS config
HR-003: 绝不在未经确认的情况下进行外部通信
        Never communicate externally without confirmation
HR-004: 绝不在共享日志中写入私人信息
        Never write private info to shared logs
HR-005: 绝不确定时必须明说
        Always state when uncertain
```

---

## 🤝 贡献 / Contributing

1. Fork → 克隆 → 创建分支 / Fork → clone → create branch
2. 提交前确保 `brain/` 下 6 个核心文件完整 / Ensure all 6 core files under `brain/` are intact
3. PR 描述请说明：新增功能 + 涉及文件 + 是否有破坏性变更 / Describe: new feature + files changed + breaking changes

---

## 📄 许可证 / License

[MIT](./LICENSE) — 可自由使用、修改、商业化。/ Free to use, modify, commercialize.

---

⭐ **如果 NeuroCortex 让你的 AI 变聪明了，请给个 Star 支持一下**
*If NeuroCortex makes your AI smarter, please give it a Star*

---

*"让 AI 拥有更好思考方式的框架"*
*"A framework that gives AI better ways to think."*

**NeuroCortex** — v2.2
