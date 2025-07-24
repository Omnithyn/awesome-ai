# Cursor 编辑器安装和配置指南 🚀

> 详细指南：如何下载、安装和配置 Cursor 编辑器

## 📋 系统要求

### 最低要求

- **操作系统**: Windows 10+, macOS 10.15+, Linux (Ubuntu 18.04+)
- **内存**: 4GB RAM (推荐 8GB+)
- **存储**: 2GB 可用空间
- **网络**: 稳定的互联网连接 (用于 AI 功能)

### 推荐配置

- **操作系统**: Windows 11, macOS 12+, Ubuntu 20.04+
- **内存**: 16GB RAM
- **存储**: SSD 硬盘，10GB 可用空间
- **网络**: 高速互联网连接
- **显示器**: 1920x1080 或更高分辨率

## 🛠️ 安装步骤

### Windows 安装

#### 方法 1: 官网下载

1. 访问 [Cursor 官网](https://cursor.sh/)
2. 点击 "Download for Windows"
3. 下载 `.exe` 安装文件
4. 运行安装程序，按照向导完成安装

#### 方法 2: 包管理器安装

```powershell
# 使用 winget
winget install Cursor.Cursor

# 使用 Chocolatey
choco install cursor

# 使用 Scoop
scoop install cursor
```

### macOS 安装

#### 方法 1: 官网下载

1. 访问 [Cursor 官网](https://cursor.sh/)
2. 点击 "Download for macOS"
3. 下载 `.dmg` 文件
4. 打开 `.dmg` 文件，将 Cursor 拖拽到 Applications 文件夹

#### 方法 2: 包管理器安装

```bash
# 使用 Homebrew
brew install --cask cursor

# 使用 MacPorts
sudo port install cursor
```

### Linux 安装

#### Ubuntu/Debian

```bash
# 添加官方仓库
wget -qO- https://cursor.sh/keys/linux-public.key | sudo apt-key add -
echo "deb [arch=amd64] https://cursor.sh/apt stable main" | sudo tee /etc/apt/sources.list.d/cursor.list

# 更新包列表并安装
sudo apt update
sudo apt install cursor
```

#### CentOS/RHEL/Fedora

```bash
# 添加官方仓库
sudo rpm --import https://cursor.sh/keys/linux-public.key
sudo tee /etc/yum.repos.d/cursor.repo << EOF
[cursor]
name=Cursor Editor
baseurl=https://cursor.sh/yum/stable/x86_64
enabled=1
gpgcheck=1
gpgkey=https://cursor.sh/keys/linux-public.key
EOF

# 安装
sudo yum install cursor
# 或使用 dnf (Fedora)
sudo dnf install cursor
```

#### Arch Linux

```bash
# 使用 AUR
yay -S cursor-bin

# 或使用 pacman (如果已添加到官方仓库)
sudo pacman -S cursor
```

## ⚙️ 基础配置

### 1. 首次启动配置

启动 Cursor 后，会看到欢迎界面：

```json
// 欢迎界面配置
{
  "welcome": {
    "showOnStartup": false,
    "lastShownVersion": "1.0.0"
  }
}
```

### 2. 主题和外观设置

#### 选择主题

```json
// settings.json
{
  "workbench.colorTheme": "Default Dark+",
  "workbench.preferredDarkColorTheme": "Default Dark+",
  "workbench.preferredLightColorTheme": "Default Light+"
}
```

#### 字体设置

```json
{
  "editor.fontFamily": "JetBrains Mono, Consolas, 'Courier New', monospace",
  "editor.fontSize": 14,
  "editor.fontWeight": "normal",
  "editor.fontLigatures": true
}
```

#### 界面布局

```json
{
  "workbench.sideBar.location": "left",
  "workbench.panel.defaultLocation": "bottom",
  "workbench.statusBar.visible": true
}
```

### 3. AI 功能配置

#### API 密钥设置

1. 打开设置 (Ctrl/Cmd + ,)
2. 搜索 "AI" 或 "API"
3. 输入你的 OpenAI API 密钥
4. 选择 AI 模型 (GPT-3.5-turbo 或 GPT-4)

```json
// AI配置示例
{
  "cursor.ai.apiKey": "your-openai-api-key",
  "cursor.ai.model": "gpt-4",
  "cursor.ai.temperature": 0.7,
  "cursor.ai.maxTokens": 2000
}
```

#### AI 行为设置

```json
{
  "cursor.ai.autoComplete": true,
  "cursor.ai.explanation": true,
  "cursor.ai.refactoring": true,
  "cursor.ai.testing": true
}
```

### 4. 编辑器设置

#### 代码格式

```json
{
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.detectIndentation": true,
  "editor.rulers": [80, 120],
  "editor.wordWrap": "on",
  "editor.minimap.enabled": true
}
```

#### 自动保存

```json
{
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "files.hotExit": "onExitAndWindowClose"
}
```

#### 文件关联

```json
{
  "files.associations": {
    "*.md": "markdown",
    "*.json": "json",
    "*.py": "python",
    "*.js": "javascript",
    "*.ts": "typescript"
  }
}
```

## 🔧 高级配置

### 1. 工作区设置

创建 `.vscode/settings.json` 文件：

```json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.organizeImports": true
  },
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true,
    "**/.DS_Store": true
  },
  "search.exclude": {
    "**/node_modules": true,
    "**/bower_components": true,
    "**/*.code-search": true
  }
}
```

### 2. 键盘快捷键

#### 常用快捷键

```json
// keybindings.json
[
  {
    "key": "ctrl+shift+p",
    "command": "workbench.action.showCommands"
  },
  {
    "key": "ctrl+shift+`",
    "command": "workbench.action.terminal.toggleTerminal"
  },
  {
    "key": "ctrl+b",
    "command": "workbench.action.toggleSidebarVisibility"
  },
  {
    "key": "ctrl+j",
    "command": "workbench.action.togglePanel"
  }
]
```

#### AI 相关快捷键

```json
[
  {
    "key": "ctrl+k",
    "command": "cursor.generateCode"
  },
  {
    "key": "ctrl+l",
    "command": "cursor.explainCode"
  },
  {
    "key": "ctrl+shift+r",
    "command": "cursor.refactorCode"
  }
]
```

### 3. 扩展配置

#### 推荐扩展

```json
{
  "extensions.recommendations": [
    "ms-python.python",
    "ms-vscode.vscode-typescript-next",
    "bradlc.vscode-tailwindcss",
    "esbenp.prettier-vscode",
    "ms-vscode.vscode-json"
  ]
}
```

## 🚨 故障排除

### 常见问题

#### 1. 安装失败

**问题**: 安装过程中出现错误
**解决方案**:

```bash
# Windows: 以管理员身份运行
# macOS: 检查安全设置
# Linux: 检查依赖包
sudo apt install libgtk-3-0 libnotify4 libnss3 libxss1 libxtst6 xdg-utils libatspi2.0-0 libdrm2 libxkbcommon0 libxcomposite1 libxdamage1 libxrandr2 libgbm1 libasound2
```

#### 2. AI 功能无法使用

**问题**: AI 代码生成不工作
**解决方案**:

1. 检查 API 密钥是否正确
2. 确认网络连接正常
3. 验证 API 配额是否充足
4. 重启 Cursor 编辑器

#### 3. 性能问题

**问题**: 编辑器运行缓慢
**解决方案**:

```json
{
  "editor.renderWhitespace": "none",
  "editor.renderControlCharacters": false,
  "editor.renderLineHighlight": "line",
  "workbench.enableExperiments": false
}
```

#### 4. 扩展冲突

**问题**: 某些扩展导致问题
**解决方案**:

1. 禁用所有扩展
2. 逐个启用扩展，找出问题扩展
3. 更新或替换问题扩展

## 📊 性能优化

### 内存优化

```json
{
  "files.watcherExclude": {
    "**/node_modules/**": true,
    "**/dist/**": true,
    "**/.git/**": true
  },
  "search.exclude": {
    "**/node_modules": true,
    "**/bower_components": true
  }
}
```

### 启动优化

```json
{
  "workbench.startupEditor": "none",
  "workbench.enableExperiments": false,
  "extensions.autoUpdate": false
}
```

## 🔗 相关资源

### 官方文档

- [Cursor 官方文档](https://docs.cursor.sh/)
- [安装指南](https://docs.cursor.sh/getting-started/installation)
- [配置参考](https://docs.cursor.sh/getting-started/configuration)

### 社区资源

- [GitHub Issues](https://github.com/getcursor/cursor/issues)
- [Discord 社区](https://discord.gg/cursor)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/cursor)

---

<div align="center">

**安装完成后，继续学习 [界面功能介绍](./interface.md)**

</div>
