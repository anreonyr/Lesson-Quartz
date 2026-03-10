---
id: 202603090014
aliases:
  - MiniMax
tags:
  - tool
date: 2026-03-09
passed: true
---

# MiniMax

MiniMax是中国的一家AI科技公司，提供大语言模型API服务。

## 特点

- 中文理解能力强
- 代码生成能力出色
- 价格相对实惠
- 响应速度快

## 核心概念

```mermaid
flowchart LR
    subgraph 客户端
        A[应用代码<br/>Python/JS] --> B[OpenAI SDK]
    end

    subgraph API请求
        B -->|HTTPS| C[api.minimax.chat]
    end

    subgraph MiniMax云
        D[认证<br/>API Key] --- E[模型推理<br/>MiniMax-Text-01]
    end

    C --> D
    D --> E
    E -->|JSON| B
```

## 使用场景

- AI编程辅助
- 代码生成和解释
- 问题解答

## API调用

```python
from openai import OpenAI

client = OpenAI(
    api_key="your-api-key",
    base_url="https://api.minimax.chat/v1"
)

response = client.chat.completions.create(
    model="MiniMax-Text-01",
    messages=[{"role": "user", "content": "你好"}]
)
```

## 相关工具

- [[工具-CC-Switch]] 支持大模型路由
