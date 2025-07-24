# Cursor 基本操作指南

> 本文介绍在 Cursor 中进行日常开发的核心操作和快捷键

## 🔍 打开和搜索项目

1. **打开文件夹**：点击欢迎页的 `Open Folder...` 按钮或使用 `Ctrl+K Ctrl+O`
2. **全局搜索**：按 `Ctrl+Shift+F` 输入关键字，回车查看匹配结果
3. **文件快速打开**：按 `Ctrl+P` 输入文件名快速跳转

4. **切换工作区**：使用 `File → Add Folder to Workspace...` 将多个项目加入工作区
5. **最近项目**：在欢迎页选择 `Open Recent` 查看历史记录

## 📝 编辑和导航

- **多光标编辑**：按 `Alt+Click` 在多处插入光标
- **代码折叠**：使用 `Ctrl+Shift+[` 和 `Ctrl+Shift+]` 折叠或展开代码块
- **跳转定义**：右键选择 `Go to Definition`，或按 `F12`
- **查找引用**：按 `Shift+F12` 查看函数或变量被调用的位置
- **格式化代码**：使用 `Shift+Alt+F` (macOS 为 `Shift+Option+F`)

### 批量编辑示例

```javascript
// 批量更改变量名
const oldName = 1;
const oldName2 = 2;
```

1. 选中其中一个变量名并按 `Ctrl+F2`，即可同时编辑所有同名变量
2. 输入新名称后自动同步到所有位置

## 🌐 Git 集成

Cursor 内置 Git 支持，可在侧边栏的 **Source Control** 查看变更：

```bash
# 查看当前分支和状态
git status

# 提交更改
git commit -m "feat: update code"
```

提交后，点击界面右上角的同步按钮即可推送到远程仓库。

### 分支管理

```bash
# 创建并切换到新分支
git checkout -b feature/ui-update

# 合并分支
git merge feature/ui-update
```

## 🤖 使用 AI 助手

1. 在代码中选择一段文本
2. 右键选择 **Ask Cursor**
3. 在弹出的对话框中输入指令，例如 "优化此函数"

生成的代码会自动插入或替换选中部分。

### 代码生成示例

```python
def hello(name):
    return f"Hello, {name}!"

# 选中函数并输入指令："生成单元测试"
```

AI 将生成对应的测试代码并插入到文件。

### 会话提示

在命令面板中选择 `Start Chat` 与 Cursor 聊天，通过上下文对话完成复杂任务。

## 🐚 集成终端

1. 按 `Ctrl+\`` 打开终端
2. 使用下拉箭头切换 shell，如 bash、zsh 或 PowerShell
3. 在终端中可直接运行测试或构建命令：

```bash
npm test
npm run build
```

终端窗口支持多标签，便于同时监控不同任务。

## 🐞 调试流程

1. 按 `F5` 启动调试，或点击调试面板中的 `Run and Debug`
2. 在代码行号处单击以设置断点
3. 调试过程中可在侧边栏查看变量值和调用栈
4. 使用 `Debug Console` 输入表达式进行评估

```json
// .vscode/launch.json
{
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/index.js"
    }
  ]
}
```

## 🎯 小结

掌握上述基本操作后，你就可以在 Cursor 中高效完成常见的开发任务。建议进一步查阅 [项目级规则配置](./project-rules.md) 设置团队规范，也可阅读其他章节了解更多高级功能。

