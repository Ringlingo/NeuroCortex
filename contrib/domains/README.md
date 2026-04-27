# 🌍 社区域库 / Community Domain Library

> 欢迎贡献你的垂直领域域文件！通过社区共建，形成高质量的域知识生态。

---

## 目录结构

```
contrib/
└── domains/           # 社区贡献的域文件
    ├── README.md      # 本文件
    ├── TEMPLATE.md     # 域文件模板
    └── examples/       # 示例域（可直接使用/修改）
        ├── data-science.md
        ├── legal-doc.md
        └── creative-writing.md
```

---

## 如何贡献新域

### 1. Fork 项目

点击 GitHub 右上角 Fork，克隆到本地。

### 2. 创建域文件

在 `contrib/domains/` 下创建你的域文件，命名格式：
```
your-domain-name.md
```

### 3. 使用模板

参考 `TEMPLATE.md` 编写域内容，确保包含：
- `==FRAGMENT:core==` — 核心知识
- `==FRAGMENT:recent==` — 最近使用记录
- `==FRAGMENT:deep==` — 深层知识

### 4. 在 FOCUS.md 中注册

在 FOCUS.md 底部添加：

```yaml
### 🏷️ your_domain — 你的域

priority: 5
context_boost: 3

keywords:
  core: [关键词1, 关键词2]
  exclusive: [专属关键词]

core_file: "contrib/domains/your-domain-name.md"
```

### 5. 提交 PR

- 使用清晰的 PR 标题：`feat: add {domain-name} domain`
- 描述中说明域的用途和适用场景

---

## 域质量标准

| 标准 | 要求 |
|------|------|
| **命名** | 使用英文或拼音，简短清晰 |
| **关键词** | 5-10个，覆盖主要场景 |
| **内容** | 包含至少 1 个 FRAGMENT:core |
| **脱敏** | 不含敏感信息，可公开 |
| **原创** | 不得抄袭已有版权内容 |

---

## 域审核清单

- [ ] 文件名符合规范
- [ ] keywords 列表合理（5-10个）
- [ ] FRAGMENT:core 包含核心知识
- [ ] FRAGMENT:recent 有初始记录
- [ ] 内容已脱敏（无可识别个人信息）
- [ ] 已在 FOCUS.md 注册

---

## 示例域预览

| 域 | 适用场景 | 贡献者 |
|------|---------|--------|
| data-science | 数据科学、机器学习 | @community |
| legal-doc | 法律文书、合同审查 | @community |
| creative-writing | 创意写作、剧本 | @community |

---

*共建共享，让 AI 更懂每个领域。*
