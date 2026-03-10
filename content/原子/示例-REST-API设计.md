---
id: 202603090048
aliases:
  - REST
tags:
  - example
date: 2026-03-09
passed: false
---

# REST API设计

REST（Representational State Transfer）是一种常见的API设计风格。

## RESTful设计原则

1. **资源导向**：URL表示资源，如 `/users`、`/orders`
2. **HTTP方法**：使用正确的HTTP方法
   - GET：获取资源
   - POST：创建资源
   - PUT：更新资源
   - DELETE：删除资源
3. **无状态**：每个请求都是独立的

## 示例接口

| 方法 | URL | 说明 |
|------|-----|------|
| POST | /users/register | 用户注册 |
| POST | /users/login | 用户登录 |
| GET | /users/me | 获取当前用户 |
| PUT | /users/me | 修改当前用户 |
| DELETE | /users/me | 删除当前用户 |

## AI编程示例

> "用FastAPI实现一个用户管理的REST API，包含以下接口：
> - POST /users/register - 用户注册
> - POST /users/login - 用户登录，返回JWT token
> - GET /users/me - 获取当前用户信息（需要认证）
> - PUT /users/me - 修改当前用户信息（需要认证）
> - DELETE /users/me - 删除当前用户（需要认证）
> 使用SQLite数据库存储用户数据，密码需要加密存储"

## 最佳实践

- 使用正确的HTTP状态码
- 提供清晰的错误信息
- 使用版本控制（如 /v1/users）
- 支持分页和过滤
