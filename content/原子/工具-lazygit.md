---
id: 202603101431
aliases:
  - lazygit
tags:
  - tool
date: 2026-03-10
passed: true
---

# lazygit

一个简单的 Git TUI（终端用户界面），用 Go 语言编写。

## 特点

- **简单高效**：告别复杂的 git 命令
- **可视化**：直观显示分支、提交、冲突
- **键盘操作**：完全用键盘操作
- **轻量快速**：启动迅速，资源占用低

## 核心概念

```mermaid
flowchart TB
    subgraph 界面布局["界面布局"]
        A[分支面板<br/>Branches]
        B[提交面板<br/>Commits]
        C[文件面板<br/>Files]
        D[差异面板<br/>Diff]
    end

    subgraph 提交["提交操作"]
        E[Space 暂存]
        F[c 打开提交]
        G[填写信息<br/>Ctrl+o 确认]
    end

    subgraph 远程["远程操作"]
        H[p 推送]
        I[P 拉取+推送]
        J[F 拉取]
    end

    subgraph 分支["分支操作"]
        K[n 新建分支]
        L[m 合并分支]
        M[d 删除]
    end

    A --- B
    B --- C
    C --- D
    C --> E
    E --> F
    F --> G
    A --> H
    H --> I
    I --> J
    A --> K
    K --> L
    L --> M
```

## 安装

```bash
# macOS
brew install lazygit

# Linux
sudo pacman -S lazygit  # Arch
sudo apt install lazygit  # Debian/Ubuntu

# Windows
winget install JesseDuffield.lazygit

# 验证
lazygit --version
```

## 界面

```
┌─ Branches ──────────────────────────────────────────────┐
│ > develop                                               │
│   main                                                  │
├─ Commits ───────────────────────────────────────────────┤
│ ┌─ Files ────────────────────────────────────────────┐  │
│ │ M 组合/02-第一个让AI编写的程序？.md                │  │
│ │ A  原子/工具-DeepSeek.md                           │  │
│ └────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────┘
```

## 常用操作

| 操作 | 按键 |
|------|------|
| 切换面板 | `Tab` / `Shift+Tab` |
| 选择 | `方向键` |
| 确认/Space | `Space` |
| 返回/退出 | `q` 或 `Esc` |
| 提交 | `c` |
| 推送 | `p` |
| 拉取 | `F` |
| 新建分支 | `n` |
| 合并分支 | `m` |
| 暂存文件 | `Space` |
| 查看差异 | `d` |
| 拉取/推送 | `P` |

## 分支操作

1. `n` 新建分支
2. `d` 删除分支
3. `m` 合并分支

## 提交操作

1. 方向键选中文件
2. `Space` 暂存/取消暂存
3. `c` 打开提交面板
4. 填写提交信息
5. `Ctrl+o` 确认提交

## 推送操作

1. 切换到分支面板
2. 选中分支
3. `p` 推送到远程

## 适用场景

- 日常 Git 操作
- 查看提交历史
- 处理合并冲突
- 管理多个分支

## 相关工具

- [[工具-Git|Git]] - Git 命令行工具
