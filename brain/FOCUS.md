# 🎯 NeuroCortex — 注意力引擎

> **定位**：聚焦相关知识域，抑制干扰
> **版本**：v2.2 | **更新**：+域冲突三级裁决 + 跨域引用协议

---

## 核心机制

```
用户输入 → 关键词扫描 → 命中域？
    │                     │
    ├─ 命中 → 加载域核心知识
    │
    └─ 未命中 → 通用能力
```

---

## 域定义模板

每个域可声明以下字段：

```yaml
### 🏷️ domain_name — 域名称

priority: 5      # 权重 1-10，默认5，用于冲突裁决
context_boost: 3 # 上下文窗口加成值，默认3

keywords:
  core: [核心关键词1, 核心关键词2]    # 域共用词
  exclusive: [专属关键词]              # 域专属词，用于消歧

core_file: "domains/domain_name.md"  # 域文件路径
```

---

## 内置域示例

### ✍️ writing — 写作创作

```yaml
priority: 7
context_boost: 3

keywords:
  core: [写, 创作, 内容]
  exclusive: [小说, 章节, 大纲, 角色, 剧情]

core_file: "domains/writing.md"
```

### 🔬 research — 科学研究

```yaml
priority: 7
context_boost: 3

keywords:
  core: [研究, 分析]
  exclusive: [实验, 论文, 数据, 科学]

core_file: "domains/research.md"
```

### 💻 coding — 编程开发

```yaml
priority: 8
context_boost: 3

keywords:
  core: [代码, 编程, 开发]
  exclusive: [函数, 调试, Git, SQL, 接口, 后端, Java, Python]

core_file: "domains/coding.md"
```

### 📊 data — 数据分析

```yaml
priority: 7
context_boost: 3

keywords:
  core: [SQL, 查询, 数据]
  exclusive: [分析, 性能, 统计, 图表]

core_file: "domains/data.md"
```

### 🧪 testing — 测试工程

```yaml
priority: 9
context_boost: 2

keywords:
  core: [测试]
  exclusive: [单元测试, 集成测试, TDD, 覆盖率, 自动化]

core_file: "domains/testing.md"
```

### 🎨 design — 设计创意

```yaml
priority: 7
context_boost: 4

keywords:
  core: [设计, 视觉]
  exclusive: [UI, 配色, 排版, 原型, Figma]

core_file: "domains/design.md"
```

---

## ⚖️ 域冲突解决规则

> **冲突定义**：一次用户输入同时匹配两个或以上域的关键词
> **解决原则**：不猜、不跳、显式裁决

### 冲突等级

| 等级 | 说明 | AI 行为 |
|------|------|--------|
| ⚠️ **弱冲突** | 匹配2个域，无权重差异 | 进入「上下文延续」裁决 |
| 🔴 **强冲突** | 匹配3个及以上域 | 进入「三级裁决」流程 |
| 💬 **用户干预** | 用户明确指定域 | 跳过裁决，直接加载 |

### 三级裁决体系

**第一级：显式域优先级权重**
- 优先加载 `priority` 最高的域

**第二级：上下文窗口延续**
- 上一轮加载的域在窗口期（3轮）内，+3 加成
- 相关度判定：用户提问含上一轮域关键词 +30%；话题延续 +40%

**第三级：用户明确指令**
- 用户说"切换到XX域"/"从XX角度" → 最高优先

### 冲突解析流程

```
用户输入
    │
    ▼
关键词扫描，匹配所有域 → [A, B, C]
    │
    ▼
只有一个域命中？ ──YES──→ 直接加载
    │
   NO
    │
    ▼
用户显式指定域？ ──YES──→ 加载用户指定域
    │
   NO
    │
    ▼
比较 priority 权重 → 最高权重域
    │
    ▼
检查上下文窗口（3轮）→ 上一轮域在窗口期？
    │
   YES ──+3加成──→ 重新比较
    │
   NO
    │
    ▼
加载最终裁决域
```

### 实际案例

**案例1**："这个 SQL 查询的性能问题怎么优化？"
- 匹配：coding(SQL) + data(SQL, 性能)
- 裁决：coding(priority=8) vs data(priority=7) → **coding胜**

**案例2**："登录接口的单元测试要怎么写？"
- 匹配：coding(接口, 登录) + testing(单元测试)
- 裁决：testing(priority=9) > coding(priority=8)，但上下文窗口+3加成给coding
- 实际结果：**coding**（上下文延续使窗口期内的任务衔接更自然）

---

## 🔗 跨域引用协议

> **格式**：`@ref:domain_name/entry_key`
> **用途**：一处定义，多处引用，避免重复

### 使用规则

- 在域文件中使用 `@ref:other_domain/keyword` 引用其他域的知识
- 加载时递归展开被引用域的 `FRAGMENT:core`（深度≤2层）
- 检测到循环引用时停止并警告

### 示例

```markdown
## 我的coding域

- SQL优化 → @ref:data/performance
- 单元测试 → @ref:testing/unit_test
```

---

## 自定义域

在下方添加新域配置，使用上述模板：

```yaml
### 🎯 your_domain — 你的域

priority: 5
context_boost: 3

keywords:
  core: [关键词1, 关键词2]
  exclusive: [专属关键词]

core_file: "domains/your_domain.md"
```

---

_注意力引擎：让每一次思考都聚焦在正确的地方。_
