---
id: 202603090051
aliases:
  - Claude
  - ClaudeCode
tags:
  - tool
date: 2026-03-09
passed: true
---

# ClaudeCode

ClaudeCode是Anthropic推出的AI编程助手。

## 特点

- 深度理解代码库
- 安全优先（不会执行危险操作）
- 可以帮你写代码、调试、重构
- 支持代码审阅

## 核心概念

```mermaid
flowchart TB
    subgraph 核心能力["核心能力"]
        A[Read 读取文件]
        B[Write 写入文件]
        C[Bash 执行命令]
    end

    subgraph 搜索["代码搜索"]
        D[Grep 内容搜索]
        E[Glob 文件查找]
    end

    subgraph 项目理解["项目理解"]
        F[代码分析]
        G[项目探索]
        H[依赖理解]
    end

    subgraph MCP["MCP 扩展"]
        I[ MCP 服务器<br/>自定义工具]
        J[外部服务集成<br/>API 调用]
        K[数据库<br/>知识库]
    end

    subgraph 安全["安全机制"]
        L[危险操作确认]
        M[沙箱执行]
        N[用户授权]
    end

    subgraph 任务["任务执行"]
        O[代码生成]
        P[代码审查]
        Q[重构优化]
    end

    A --- B
    B --- C
    C --> D
    D --> E
    A --> F
    F --> G
    G --> H
    C --> I
    I --> J
    J --> K
    C --> L
    L --> M
    M --> N
    B --> O
    O --> P
    P --> Q
```

## 使用场景

- 编程、代码分析、项目探索
- 代码重构和优化
- Bug定位和修复

## 核心能力

- 读写文件
- 执行命令
- 搜索代码库
- 代码审查
- 项目理解

## 相关工具

- [[工具-Zed|Zed]] - 支持 ACP 的代码编辑器
- [[工具-CC-Switch|CC-Switch]] - 模型切换工具
