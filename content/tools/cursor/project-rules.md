# Cursor 项目级规则配置

> 通过自定义规则文件，精准控制 AI 助手在项目中的行为

## 规则文件位置

在项目根目录创建 `.cursor/rules.json`（或 `cursor-rules.json`），用于定义针对本项目的专属规则。

```bash
# 示例目录结构
my-project/
├── .cursor/
│   └── rules.json
├── src/
│   └── index.ts
└── package.json
```

## 常见规则示例

```json
{
  "style": {
    "indent": 2,
    "quotes": "double",
    "lineWidth": 100
  },
  "prompts": {
    "todoComment": "请为以下 TODO 补充实现并保持注释",
    "explainCode": "用中文解释下面代码的作用"
  },
  "filters": [
    "node_modules",
    "dist"
  ]
}
```

- **style**：约定代码风格，AI 生成代码时会遵循缩进、引号和行宽设置
- **prompts**：定义常用指令的默认提示语，提升交互效率
- **filters**：排除不需要分析的目录，减少干扰

## 使用步骤

1. 在 `.cursor/rules.json` 中编写所需规则
2. 重新加载 Cursor 或按 `Ctrl+Shift+P` 执行 `Reload Window`
3. AI 助手将在生成和修改代码时自动应用这些规则

## 进阶技巧

- 可以为不同子目录创建独立规则文件，满足多模块项目的需求
- 将常用规则整理为模板，复制到新项目即可复用
- 结合 Git 版本控制，让团队成员共享同一套规则

## 小结

合理配置项目级规则，可以让 AI 更加贴合你的编码规范和团队流程，提高整体开发效率。
