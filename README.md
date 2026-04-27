# 🧠 NeuroCortex

### NeuroCortex — a markdown-native cognitive framework for AI.
### NeuroCortex — 一个基于 Markdown 的 AI 认知框架

*让 AI 思考更有序、更安全、更高效。*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-v2.2-green.svg)]()

---

## 🎯 解决什么问题

| 痛点 | NeuroCortex 的答案 |
|------|-------------------|
| AI 总是重复犯同一个错 | LTP 自维护 → 重复触发自动强化规则 |
| 多个域同时匹配时 AI 乱选 | 三级裁决体系 → 权重+上下文+用户指令 |
| 每次都要重新解释项目背景 | 域知识系统 → 一次配置，持续加载 |
| 安全规则容易被 prompt 注入绕过 | 不可变声明 + 变更日志 → 规则可审计 |
| 思维方法选哪个全凭感觉 | 案例触发词索引 → 匹配问题直接推荐方法 |
| 新手不知道从何配置 | 交互式启动向导 → 10分钟生成专属配置 |

---

## ✨ 核心特性

| 特性 | 说明 |
|------|------|
| **零依赖** | 纯 Markdown 文件，任何 AI 助手可用 |
| **按需加载** | 非一次性读入，降低上下文消耗 |
| **自进化** | AI 会话结束自动更新规则，无需手动维护 |
| **域冲突裁决** | 智能消歧，匹配准确率 +30% |
| **安全内嵌** | HR-001~005 不可变声明，规则可审计 |
| **交互向导** | ONBOARDING.md，10分钟生成专属域和规则 |

---

## 📁 项目结构

```
NeuroCortex/
├── brain/                        # 核心认知模块
│   ├── ACTIVATE.md              # 🚀 启动入口
│   ├── FOCUS.md                 # 🎯 注意力引擎 + 域冲突裁决
│   ├── EPISODES.md              # 📋 情景缓冲区 + AI草稿
│   ├── INTUITION.md             # ⚡ LTP直觉 + 自维护
│   ├── THINKKIT.md              # 🔧 思维工具 + 案例索引
│   ├── META.md                  # 🛡️ 安全防线 + 不可变声明
│   └── cases/                   # 📚 实战案例库（5个案例）
│       ├── 第一性原理_案例1.md
│       ├── 逆向思维_案例1.md
│       ├── 逆向思维_案例2.md
│       ├── 类比迁移_案例1.md
│       └── 魔鬼代言人_案例1.md
├── domains/                      # 📦 可扩展知识域
│   └── example.md               #   域文件模板
├── .github/workflows/            # ⚙️ GitHub Actions
├── IMPROVE.md                    # 🔍 自我优化建议
├── ONBOARDING.md                 # 🎯 交互式启动向导
└── README.md
```

---

## 🚀 快速开始

### 方式一：使用交互向导（推荐新手）

```bash
# 打开 ONBOARDING.md，按提示回答7个问题
# 10分钟后生成专属域和直觉规则
```

### 方式二：手动配置

```bash
# 1. 克隆项目
git clone https://github.com/Ringlingo/NeuroCortex.git
cd NeuroCortex

# 2. 将 brain/ 复制到 AI 工作区
# 3. 每次对话从 ACTIVATE.md 开始读取
```

### 首次对话只需一行

将 `brain/` 文件夹放入工作区后，对 AI 说：

> **"请先读取 brain/ACTIVATE.md，然后告诉我 NeuroCortex 能帮我做什么。"**

AI 会自动加载认知模块，并引导你完成后续配置。

这能极大降低"不知道如何迈出第一步"的心理摩擦。

---

## 🧠 核心模块一览

| 模块 | 负责什么 | 神经科学依据 |
|------|---------|-------------|
| **ACTIVATE** | 会话入口 + 安全检查 + 结束检查点 | 前额叶启动监控 |
| **FOCUS** | 关键词扫描 → 域加载 + 冲突裁决 | 前额叶注意力选择 |
| **EPISODES** | 会话记录索引 + AI 草稿生成 | 海马体情景记忆 |
| **INTUITION** | LTP 强化规则 + AI 自动更新 | 突触长时程增强 |
| **THINKKIT** | 16 种思维方法 + 案例索引 | 前额叶执行功能 |
| **META** | 5 条硬规则 + 不可变声明 | 前扣带回自我监控 |

---

## ⚙️ 启动序列

```
用户输入
    │
    ▼
Step 0: 读 ACTIVATE.md
        │
Step 1: 安全检查（配置写入审查）
        │
Step 2: 注意力扫描 → 域冲突裁决
        │
Step 3: 跨域引用解析
        │
Step 4: INTUITION 快速扫描
        │
Step 5: EPISODES 条件触发
        │
        │ ← 会话进行
        │
Step 6: 会话结束检查点
        • 触发条件：对话轮次≥3 + 结束语
        • INTUITION 自维护（AI 自动更新）
        • EPISODES 草稿（AI 生成 + 用户确认）
```

---

## 🧩 域冲突裁决

**案例一**：用户问 "登录接口的单元测试要怎么写？"

```
匹配域：coding (priority=8) + testing (priority=9)
         ↓
Step 1: 用户未指定域，跳过
Step 2: priority 权重 → testing (9) > coding (8)
Step 3: 上下文窗口检查
        上一轮可能是 coding，窗口期 +3 加成
        coding 实际分 = 8 + 3 = 11 > testing 9
         ↓
最终裁决：加载 coding 域
          （保持同一任务的上下文连贯性）
```

**案例二（反直觉裁决）**：用户问 "怎么给小说情节设计冲突？"

```
匹配域：writing (priority=7, context_boost=3) + design (priority=7, context_boost=4)
         ↓
Step 1: 用户未指定域，跳过
Step 2: priority 权重 → 两者相同（7 = 7）
Step 3: 上下文窗口检查
        无上一轮（全新对话），无窗口加成
        design 看起来更占优（context_boost=4 > 3）
         ↓
但是！FOCUS 检测到关键词"小说情节"在 writing 的 core 词表中
       而 design 的 exclusive 词表不含任何写作相关词
         ↓
裁决修正：writing 域胜出
         ↓
最终裁决：加载 writing 域 ✓
          （"看起来 design 会赢，但系统判对了"）
```

---



## 🔗 跨域引用

```markdown
在域文件中使用：
- SQL 性能优化 → @ref:data/performance
- 单元测试覆盖 → @ref:testing/coverage
```

---

## 📚 案例库

| 方法 | 案例 | 一句话描述 |
|------|------|-----------|
| 第一性原理 | [案例1](brain/cases/第一性原理_案例1.md) | 为什么 SQL 索引能加速查询 |
| 逆向思维 | [案例1](brain/cases/逆向思维_案例1.md) | 定位日志无错误的 Bug |
| 逆向思维 | [案例2](brain/cases/逆向思维_案例2.md) | 职业转型从哪开始 |
| 类比迁移 | [案例1](brain/cases/类比迁移_案例1.md) | 解释区块链分布式账本 |
| 魔鬼代言人 | [案例1](brain/cases/魔鬼代言人_案例1.md) | 质疑产品方案的可靠性 |

---

## 🛡️ 安全规则

HR-001 ~ HR-005 是不可逾越的底线，写入 META.md 元注释：

```yaml
HR-001: 绝不自动执行破坏性操作（删除/覆写/发送）—— 必须先确认
HR-002: 绝不修改系统文件或操作系统配置
HR-003: 绝不在未经确认的情况下进行外部通信
HR-004: 绝不在共享日志中写入私人信息
HR-005: 绝不确定时必须明说
```

---

## 🤝 贡献

1. Fork → 克隆 → 创建分支
2. 提交前确保：`brain/` 下 6 个核心文件完整
3. PR 描述请说明：新增功能 + 涉及文件 + 是否有破坏性变更

---

## 📄 许可证

[MIT](./LICENSE) — 可自由使用、修改、商业化。

---

⭐ **如果 NeuroCortex 让你的 AI 变聪明了，请给个 Star 支持一下**

🗺️ **下个版本 v2.3 计划**：
- 跨域知识图谱可视化
- 一键导出直觉规则热力图
- ONBOARDING.md 中文语音引导版

---
