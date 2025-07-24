# 贡献指南 🤝

感谢你考虑为 Awesome-AI 项目做出贡献！我们欢迎所有形式的贡献，无论是内容贡献、代码改进、还是问题反馈。

## 📋 贡献类型

### 📝 内容贡献

- 添加新的 AI 工具教程
- 完善现有文档
- 翻译内容到其他语言
- 添加代码示例和最佳实践

### 🔧 代码改进

- 改进自动化脚本
- 优化网站性能
- 修复 bug 和问题
- 添加新功能

### 🐛 问题反馈

- 报告文档错误
- 提出改进建议
- 反馈用户体验问题
- 报告技术问题

### 📚 文档完善

- 改进现有文档
- 添加新的说明
- 更新过时信息
- 完善示例代码

## 🚀 快速开始

### 1. Fork 项目

1. 访问 [Awesome-AI GitHub 仓库](https://github.com/Omnithyn/awesome-ai)
2. 点击右上角的 "Fork" 按钮
3. 等待 Fork 完成

### 2. 克隆仓库

```bash
# 克隆你的Fork
git clone https://github.com/Omnithyn/awesome-ai.git

# 进入项目目录
cd awesome-ai

# 添加上游仓库
git remote add upstream https://github.com/Omnithyn/awesome-ai.git
```

### 3. 创建分支

```bash
# 创建并切换到新分支
git checkout -b feature/your-feature-name

# 或创建修复分支
git checkout -b fix/issue-description
```

### 4. 进行修改

- 编辑文件
- 添加新内容
- 修复问题
- 改进文档

### 5. 提交更改

```bash
# 添加修改的文件
git add .

# 提交更改
git commit -m "feat: add new AI tool tutorial"

# 推送到你的Fork
git push origin feature/your-feature-name
```

### 6. 创建 Pull Request

1. 访问你的 Fork 页面
2. 点击 "Compare & pull request"
3. 填写 PR 描述
4. 提交 PR

## 📝 内容贡献指南

### 文档结构

```
content/
├── tools/                    # AI工具教程
│   ├── cursor/              # Cursor编辑器
│   ├── copilot/             # GitHub Copilot
│   └── chatgpt/             # ChatGPT
├── frameworks/               # AI框架教程
│   ├── langchain/           # LangChain
│   └── openai/              # OpenAI API
├── applications/             # AI应用案例
│   ├── chatbots/            # 聊天机器人
│   └── code-generation/     # 代码生成
├── best-practices/           # 最佳实践
│   ├── prompt-engineering/  # 提示工程
│   └── model-selection/     # 模型选择
└── resources/                # 资源汇总
    ├── datasets/            # 数据集
    └── models/              # 模型资源
```

### 内容模板

我们提供了标准化的内容模板：

- [工具教程模板](./templates/tool-tutorial.md)
- [框架指南模板](./templates/framework-guide.md)
- [最佳实践模板](./templates/best-practice.md)

### 内容规范

#### 文件命名

- 使用小写字母和连字符
- 文件名要有描述性
- 避免特殊字符

```bash
# ✅ 正确的命名
cursor-installation-guide.md
ai-code-generation-tips.md
prompt-engineering-best-practices.md

# ❌ 错误的命名
Cursor_Installation_Guide.md
AI Code Generation Tips.md
prompt engineering best practices.md
```

#### 内容格式

- 使用 Markdown 格式
- 添加适当的标题层级
- 使用代码块和语法高亮
- 添加图片和图表

#### 代码示例

````markdown
# 代码示例

```python
def hello_world():
    print("Hello, World!")
```
````

# 配置示例

```json
{
  "setting": "value",
  "enabled": true
}
```

````

#### 图片和资源
- 图片放在 `assets/` 目录下
- 使用相对路径引用
- 添加适当的alt文本
- 压缩图片以减小文件大小

### 质量要求

#### 内容质量
- 信息准确且最新
- 步骤清晰易懂
- 包含实用的代码示例
- 提供相关链接和参考资料

#### 技术准确性
- 代码示例可以运行
- 配置参数正确
- 版本信息准确
- 兼容性说明清楚

#### 用户体验
- 结构清晰有序
- 语言简洁明了
- 包含必要的截图
- 提供故障排除指南

## 🔧 代码贡献指南

### 代码规范

#### Python代码
```python
# 使用PEP 8规范
def calculate_sum(a: int, b: int) -> int:
    """计算两个数的和。

    Args:
        a: 第一个数
        b: 第二个数

    Returns:
        两个数的和
    """
    return a + b
````

#### JavaScript 代码

```javascript
// 使用ESLint规范
function calculateSum(a, b) {
  return a + b;
}

// 使用箭头函数
const multiply = (a, b) => a * b;
```

#### Markdown 文档

```markdown
# 标题使用 # 号

## 二级标题

### 三级标题

- 列表项使用 - 号
- 保持一致的缩进

1. 有序列表使用数字
2. 保持格式一致

**粗体文本** 和 _斜体文本_

[链接文本](URL)

![图片描述](图片URL)
```

### 提交信息规范

使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```bash
# 功能提交
git commit -m "feat: add new AI tool tutorial"

# 修复提交
git commit -m "fix: correct installation steps"

# 文档提交
git commit -m "docs: update README with new features"

# 重构提交
git commit -m "refactor: improve code organization"

# 测试提交
git commit -m "test: add unit tests for new feature"

# 构建提交
git commit -m "build: update dependencies"
```

### 代码审查

#### 审查清单

- [ ] 代码符合项目规范
- [ ] 功能按预期工作
- [ ] 包含必要的测试
- [ ] 文档已更新
- [ ] 没有引入安全问题

#### 审查流程

1. 提交 PR 后自动触发 CI 检查
2. 维护者进行代码审查
3. 根据反馈进行修改
4. 审查通过后合并

## 🐛 问题反馈指南

### 报告 Bug

#### Bug 报告模板

```markdown
## Bug 描述

简要描述 bug 的内容

## 重现步骤

1. 第一步
2. 第二步
3. 第三步

## 预期行为

描述应该发生什么

## 实际行为

描述实际发生了什么

## 环境信息

- 操作系统: [Windows/macOS/Linux]
- 浏览器: [Chrome/Firefox/Safari]
- 版本: [具体版本号]

## 附加信息

任何其他相关信息
```

### 功能请求

#### 功能请求模板

```markdown
## 功能描述

详细描述你希望添加的功能

## 使用场景

描述这个功能的使用场景

## 实现建议

如果有实现建议，请提供

## 替代方案

如果已有类似功能，请说明
```

## 📋 贡献流程

### 1. 选择贡献类型

- 内容贡献：添加教程、指南、最佳实践
- 代码贡献：改进脚本、修复 bug、添加功能
- 问题反馈：报告 bug、提出建议、反馈问题

### 2. 检查现有内容

- 搜索是否已有相关内容
- 查看相关 Issue 和 PR
- 确认贡献的必要性

### 3. 创建分支

```bash
# 更新主分支
git checkout main
git pull upstream main

# 创建新分支
git checkout -b feature/your-feature-name
```

### 4. 进行修改

- 按照项目规范进行修改
- 确保代码质量和文档质量
- 添加必要的测试

### 5. 提交更改

```bash
# 添加文件
git add .

# 提交更改
git commit -m "type: description"

# 推送到Fork
git push origin feature/your-feature-name
```

### 6. 创建 Pull Request

- 填写 PR 标题和描述
- 选择适当的标签
- 请求相关维护者审查

### 7. 审查和合并

- 根据反馈进行修改
- 通过审查后合并
- 删除临时分支

## 🏷️ 标签说明

### Issue 标签

- `bug`: 错误报告
- `enhancement`: 功能请求
- `documentation`: 文档改进
- `good first issue`: 适合新手的 Issue
- `help wanted`: 需要帮助的 Issue

### PR 标签

- `feature`: 新功能
- `fix`: Bug 修复
- `docs`: 文档更新
- `refactor`: 代码重构
- `test`: 测试相关

## 📞 获取帮助

### 社区资源

- [Discord 社区](https://discord.gg/awesome-ai)
- [GitHub Discussions](https://github.com/your-username/awesome-ai/discussions)
- [Issues 页面](https://github.com/your-username/awesome-ai/issues)

### 联系方式

- 📧 Email: your-email@example.com
- 🐦 Twitter: [@awesome_ai](https://twitter.com/awesome_ai)
- 💬 Discord: [加入我们的社区](https://discord.gg/awesome-ai)

## 🙏 致谢

感谢所有为这个项目做出贡献的开发者、研究人员和 AI 爱好者！

### 贡献者名单

我们会在项目主页上列出所有贡献者，感谢他们的付出。

---

<div align="center">

**让我们一起构建更好的 AI 知识库！** 🚀

Made with ❤️ by the Awesome-AI Community

</div>
