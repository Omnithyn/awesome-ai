# Cursor 编辑器界面功能介绍

> 了解 Cursor 的主界面组成和常用视图，快速上手日常开发流程

## 📺 主界面概览

启动 Cursor 后，默认界面分为以下区域：

1. **侧边栏**：文件浏览器、搜索、源代码管理等入口
2. **编辑器区域**：编写和查看代码的主要区域
3. **底部面板**：终端、问题列表和输出窗口
4. **状态栏**：显示 Git 状态、编码格式和行列号

下图展示了典型的界面布局：

```text
┌──────────────────────────────┐
│ ⬤ 文件树     |   编辑器区        │
│             |                  │
│             |                  │
│             |                  │
│             |                  │
├─────────────┴──────────────────┤
│ 终端 | 问题 | 输出 | 调试控制台 │
└──────────────────────────────┘
```

## 🧰 功能面板

### 1. 文件资源管理器

- 浏览和管理项目文件
- 支持拖拽移动和重命名
- 右键菜单可快速创建文件或文件夹

### 2. 搜索面板

- 全局搜索文本或正则表达式
- 支持在结果中直接替换
- 可按文件类型过滤

### 3. 源代码管理

- 显示 Git 变更、提交历史和分支
- 提供可视化的合并冲突解决界面

### 4. 扩展市场

- 浏览并安装社区扩展或主题
- 管理已安装的扩展

### 5. 调试面板

- 设置断点、启动调试会话
- 查看变量、调用栈和监视表达式
- 通过调试控制台执行命令

### 6. 集成终端

- 在底部面板直接运行命令行
- 支持多个终端会话并可切换 shell 类型
- 通过快捷键 `Ctrl+\`` (macOS 同为 `Ctrl+\``) 打开

### 7. 输出窗口

- 查看任务和扩展的输出日志
- 错误和警告会在此面板汇总

## ⌨️ 常用快捷键

| 操作             | 快捷键 (Windows/Linux) | 快捷键 (macOS) |
| ---------------- | ---------------------- | -------------- |
| 打开命令面板     | `Ctrl+Shift+P`         | `Cmd+Shift+P`  |
| 全局搜索         | `Ctrl+Shift+F`         | `Cmd+Shift+F`  |
| 切换侧边栏显示   | `Ctrl+B`               | `Cmd+B`        |
| 打开终端         | `Ctrl+\``             | `Ctrl+\``     |
| 打开设置         | `Ctrl+,`              | `Cmd+,`       |
| 拆分编辑器       | `Ctrl+\\`             | `Cmd+\\`      |
| 切换全屏         | `F11`                 | `Ctrl+Cmd+F`  |

## 🎨 布局与主题自定义

### 拖拽与拆分窗口

1. 将文件标签拖拽到编辑器两侧，即可创建水平或垂直分屏
2. 或通过菜单 `View → Editor Layout` 选择预设布局
3. 拆分后的每个编辑器都可独立显示不同文件

### 主题与配色

1. 打开命令面板，输入 `Preferences: Color Theme`
2. 选择内置主题或在扩展市场搜索主题包
3. 在 `settings.json` 中自定义字体和颜色：

```json
{
  "workbench.colorTheme": "Default Dark+",
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontSize": 14
}
```

### 键盘快捷键管理

1. 打开 `File → Preferences → Keyboard Shortcuts`
2. 搜索并修改现有快捷键，或添加自定义绑定
3. 所有自定义键位会保存到 `keybindings.json`

## 🎯 小结

熟悉界面布局和功能面板后，可以更高效地在 Cursor 中完成开发任务。接下来，可继续阅读 [基本操作指南](./basic-operations.md) 学习具体的日常操作流程，或查看 [项目级规则配置](./project-rules.md) 了解如何自定义 AI 行为。

