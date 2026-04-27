# 🤝 贡献指南

感谢您对 NeuroCortex 的兴趣！我们欢迎各种形式的贡献。

## 📋 贡献方式

### 🐛 报告问题
- 使用 GitHub Issues
- 描述清楚问题现象和环境
- 附上相关配置文件（注意脱敏）

### 💡 提出建议
- 使用 GitHub Discussions
- 描述您的使用场景和需求
- 解释为什么现有方案不足

### 🔧 提交代码

1. **Fork 本仓库**
2. **创建分支**
   ```bash
   git checkout -b feature/YourFeature
   # 或
   git checkout -b fix/YourBug
   ```
3. **提交更改**
   ```bash
   git commit -m 'Add some feature'
   ```
4. **推送到分支**
   ```bash
   git push origin feature/YourFeature
   ```
5. **创建 Pull Request**

## 📐 代码规范

### Markdown 文件
- 使用中文标点符号
- 标题层级清晰（h1 → h2 → h3）
- 代码块注明语言

### 域文件格式
```
==FRAGMENT:core==  # 核心知识
...
==END==

==FRAGMENT:recent==  # 最近使用
...
==END==

==FRAGMENT:deep==  # 深层知识
...
==END==
```

## 🧪 测试

提交前请确认：
- [ ] 新增域已添加索引到 FOCUS.md
- [ ] 安全规则符合 META.md 规范
- [ ] 文档已同步更新

## 📝 更新日志

提交 PR 时，请在描述中说明：
- 新增功能或修复内容
- 涉及的文件
- 是否有破坏性变更

---

再次感谢您的贡献！
