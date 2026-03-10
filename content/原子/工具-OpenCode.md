---
id: 202603090111
aliases:
  - OpenCode
tags:
  - tool
date: 2026-03-08
passed: true
---

# OpenCode

基于终端的 AI 编程助手，由 Go 语言编写。

## 特点

- **多模型支持**：支持 75+ LLM（Claude、GPT、DeepSeek、GLM 等）
- **双模式**：Plan（架构设计）+ Build（代码实现）
- **终端界面**：基于 Bubble Tea 的交互式 TUI
- **多会话管理**：支持多个会话切换
- **MCP 支持**：可配合模型上下文协议服务器使用
# 核心概念

```mermaid
flowchart TD
    subgraph 用户层
        A[用户输入需求]
    end

    subgraph Plan模式["Plan 模式（规划）"]
        B[分析需求]
        C[架构设计]
        D[任务拆分]
    end

    subgraph Build模式["Build 模式（执行）"]
        E[读写文件]
        F[执行命令]
        G[代码生成]
    end

    subgraph 模型层
        H[云端模型<br/>Claude/GPT/DeepSeek]
        I[本地模型<br/>Ollama/LM Studio]
    end

    subgraph 工具层
        J[LSP]
        K[Git]
        L[MCP服务器]
    end

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G -->|反馈| A

    B -.-> H
    B -.-> I

    E --> J
    E --> K
    E --> L
```

# 安装

```bash
# macOS / Linux
brew install sst/tap/opencode

# npm
npm i -g opencode-ai@latest

# 脚本安装
curl -fsSL https://opencode.ai/install | bash

# 验证
opencode --version
```

# 使用

## 启动

```bash
opencode
```

## 常用命令

| 操作     | 命令                               |
| ------ | -------------------------------- |
| 启动交互模式 | `opencode`                       |
| 查看版本   | `opencode --version`             |
| 模型配置   | `opencode config set model <模型>` |
| 新建会话   | `opencode new`                   |
| 列出会话   | `opencode sessions`              |

## 相关工具

- [[工具-Zed|Zed]] - 支持 ACP 的代码编辑器
- [[工具-CC-Switch|CC-Switch]] - 模型切换工具
