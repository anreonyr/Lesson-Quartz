---
id: 202603090085
aliases:
  - GitHub
tags:
  - example
date: 2026-03-09
passed: false
---

# GitHub协作

GitHub是最常用的代码托管平台。

## 常用操作

### 推送代码

```bash
# 推送到远程
git push origin main
```

### 拉取代码

```bash
# 拉取最新代码
git pull origin main
```

### 远程操作

```bash
# 添加远程仓库
git remote add origin <url>

# 查看远程仓库
git remote -v
```

## 协作方式

### 1. Fork + Pull Request

1. Fork 别人的仓库
2. 在你的副本中修改
3. 发起 Pull Request

### 2. 团队协作

1. 邀请团队成员
2. 分支管理
3. 代码审查

## Gitignore

创建 `.gitignore` 文件，排除不需要管理的文件：

```
# Python
__pycache__/
*.pyc
.venv/
venv/

# IDE
.vscode/
.idea/

# 临时文件
*.log
*.tmp
```

## 相关工具

- [[工具-Git|Git]] - 版本控制
- [[示例-Git基本命令|Git基本命令]] - Git 命令
- [[工具-lazygit|lazygit]] - Git TUI
```
