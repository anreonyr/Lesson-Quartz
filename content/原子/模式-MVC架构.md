---
id: 202603090044
aliases:
  - MVC
tags:
  - pattern
date: 2026-03-09
passed: false
---

# MVC架构

Web开发中最经典的架构模式。

## 核心概念

- **M**odel（模型）：数据层，处理数据逻辑
- **V**iew（视图）：展示层，处理界面显示
- **C**ontroller（控制器）：业务层，处理请求响应

## Python示例（Flask）

```python
# Model（模型）
class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(100))

# Controller（控制器）
@app.route('/user/<int:user_id>')
def get_user(user_id):
    user = User.query.get(user_id)
    return render_template('user.html', user=user)  # View
```

## 优点

- 职责分离
- 便于维护
- 适合Web开发

## 适用场景

- Web应用
- 需要团队协作的中大型项目
