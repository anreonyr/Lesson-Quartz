---
id: 202603090058
aliases:
  - Prompt示例
tags:
  - example
date: 2026-03-09
passed: false
---

# 好的Prompt示例

## 代码生成

**不好的prompt**：
> 写一个排序算法

**好的prompt**：
> 用Python实现快速排序算法。要求：
> - 函数名为quick_sort
> - 输入是一个整数列表
> - 返回排序后的新列表（不修改原列表）
> - 使用递归实现

## 代码解释

**不好的prompt**：
> 解释这段代码

**好的prompt**：
> 解释下面的Python代码，说明每行代码的作用：
> ```python
> def fib(n):
>     if n <= 1:
>         return n
>     return fib(n-1) + fib(n-2)
> ```

## Bug修复

**不好的prompt**：
> 代码报错了，帮我修

**好的prompt**：
> 下面的代码运行时出现IndexError错误，请帮我找出问题并修复：
> ```python
> list = [1, 2, 3]
> print(list[5])
> ```

## 前端开发

**不好的prompt**：
> 写一个待办事项组件

**好的prompt**：
> 用React实现一个待办事项列表组件。要求：
> - 使用函数组件和useState管理状态
> - 支持添加新待办事项
> - 支持删除待办事项
> - 支持标记完成/未完成
> - 显示待办事项数量统计
