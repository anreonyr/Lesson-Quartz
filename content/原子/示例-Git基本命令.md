---
id: 202603090081
aliases:
  - Git命令
tags:
  - example
date: 2026-03-09
passed: false
---

# Git基本命令

## 基础操作

### 保存版本

```bash
# 添加所有修改
git add .

# 提交修改
git commit -m "提交信息"
```

### 查看状态

```bash
# 查看状态
git status

# 查看差异
git diff
```

### 版本历史

```bash
# 查看提交历史
git log

# 简洁版
git log --oneline
```

## 常用Git命令速查

| 操作 | 命令 |
|------|------|
| 初始化仓库 | `git init` |
| 克隆仓库 | `git clone <url>` |
| 添加修改 | `git add .` |
| 提交 | `git commit -m "信息"` |
| 查看状态 | `git status` |
| 查看差异 | `git diff` |
| 查看历史 | `git log` |

## AI编程建议

在让AI重写一段代码之前，先提交当前的版本：

```bash
git add .
git commit -m "AI修改前的备份"
```

## 相关工具

- [[工具-Git|Git]] - Git 版本控制概念
- [[示例-GitHub协作|GitHub协作]] - GitHub 协作流程
- [[工具-lazygit|lazygit]] - Git TUI 界面
