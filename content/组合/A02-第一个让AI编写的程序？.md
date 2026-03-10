---
id: 202603100001
aliases:
  - 第一个AI编写的程序？
tags:
  - passage
date: 2026-03-10T00:03:00
passed: true
---
# 工具入门

市面上的AI编程工具繁多，本章将介绍主流工具的特点，帮助你选择适合自己的工具。

## 主流AI编程工具

理解AI编程工具之前，需要先了解三个核心概念：

| 概念                           | 职责             | 例子                                            |
| ---------------------------- | -------------- | --------------------------------------------- |
| **[[概念-API提供商\|AI提供商]]**     | 提供底层AI模型能力     | MiniMax, GLM, DeepSeek, Kimi                  |
| **[[概念-Agent工具\|AI Agent]]** | 理解任务、调度工具、生成回答 | Claude Code, Cursor, GitHub Copilot, OpenCode |
| **[[概念-代码编辑器\|代码编辑器]]**      | 编写和编辑代码的用户界面   | VS Code, JetBrains, Zed                       |
| **[[概念-代码管理\|代码管理]]**        | 代码的备份          | Git，Svn                                       |

## 如何选择适合你的工具

### 从三个层次考虑

选择AI编程工具时，可以从以下三个层次考虑：

1. **[[概念-API提供商\|AI提供商]]**
   - 不同提供商的模型能力有差异
   - 关注模型的语言理解能力、代码生成能力
   - 最重要的价格

2. **[[概念-Agent工具\|AI Agent]]**
   - 工具的任务理解能力、工具调度能力
   - 是否支持你需要的编程场景

3. **[[概念-代码编辑器\|代码编辑器]]**
   - 是否与你熟悉的编辑器集成
   - 是否需要完整的IDE功能

### 推荐选择
- [[工具-MiniMax|MiniMax]] 
	- 订阅制，在订阅期内每个周期内都可以获得一定量的Token，每个周期都会刷新，一个周期是5小时
- [[工具-DeepSeek|DeepSeek]]
	- 买Token，只要幻方量化没倒闭就能一直用，直到Token用完
- [[工具-OpenCode|OpenCode]] 
	- 有免费的大模型可以用，我觉得界面不太好看
- [[工具-ClaudeCode|ClaudeCode]]
	- 没有免费的，要用别家的大模型用[[工具-CC-Switch|CC-Switch]]会比较方便，我觉得界面挺好看
- [[工具-Zed|Zed]]
	- 近年新出的，启动迅速，插件生态不够丰富，但是完全够用
- [[工具-VScode|VScode]]
	- 老牌编辑器，插件很多

## 实践

使用agent和代码编辑器来写一个简单的Python程序并推送到github仓库上
### 搭建环境

- [下载](https://opencode.ai/zh/download) [[工具-OpenCode|OpenCode]] 或 [下载](https://code.visualstudio.com/) [[工具-VScode|VScode]]
- [下载](https://zed.dev/download) [[工具-Zed|Zed]] 或 [下载](https://claude.com/download) [[工具-ClaudeCode|ClaudeCode]]
- [下载](https://uv.doczh.com/getting-started/installation/) [[工具-uv|uv]]
- [下载](https://git-scm.com/install/windows) [[工具-Git|Git]]
- [下载](https://github.com/jesseduffield/lazygit/releases/tag/v0.60.0) [[工具-lazygit|lazygit]]
- [注册](https://github.com/join) [[工具-github|github]]

#### 第一个prompt示例

你可以尝试向AI发送以下问题：

> 请用Python写多个不同实现计算斐波那契数列的函数

### 简单流程

使用 OpenCode + Zed + GitHub + Lazygit
本实践将带你完成一个完整的开发流程：创建 GitHub 仓库 → 克隆到本地 → 用 AI 辅助开发 → 提交推送。

#### 创建 GitHub 仓库

1. 登录 [[工具-github|github]]
2. 点击右上角 **+** → **New repository**
3. 填写仓库名：`fibonacci`
4. 选择 **Public** 或 **Private**
5. 点击 **Create repository**

#### 克隆到本地

```bash
# 复制仓库地址（点击 Code → HTTPS → 复制）
git clone https://github.com/你的用户名/fibonacci.git
cd fibonacci
```

> 其实你现在对于Git来说是无名氏，她可不会回应一个陌生人 :-<
> 你得填写自己的名字和邮箱
> 具体怎么填，问AI吧 :->
#### 第一个分支

> 其实第一个分支是main, 严格来说是新建第一个分支 ;->

在lazygit中：
1. 在分支面板
	1. 方向键选中main分支按'Space'
	2. 按'n'弹出创建面板
	3. 新分支名叫'develop'

> 你已经达成成就 ==第一个分支== ;-)
#### 初始化项目

用uv来初始化项目

> 如果有问题请看uv的使用文档

```bash
uv init
```

#### 第一个提交

> 其实第一个提交是'Initial commit'，github帮你做的 ;-)

在 lazygit 中：
1. 在文件面板
	1. 方向键选中'/'
	2. 按'Space'切换暂存状态
2. 在提交面板
	1. 按'C'弹出提交面板
	2. 填写提交信息

> 你已经达成成就 ==第一个提交== ;-)

#### 用 OpenCode 和 Zed 打开项目

```bash
opencode .
```

```bash
zed .
```

#### 发送prompt

> 请用 Python 写多个不同实现计算斐波那契数列的函数，包括：
> 1. 递归实现
> 2. 迭代实现
> 3. 矩阵快速幂实现
>
> 并将代码保存到 fibonacci.py 文件中，同时写一个 main 函数演示每种实现的用法。

#### 用 uv 运行

```bash
uv run main.py
```

> 如果没问题就可以提交了

#### 提交然后推送到 GitHub

##### 提交

提交操作请依照[[#第一个提交]]

##### 推送

在 lazygit 中：
1. 在分支面板
	1. 方向键选中要推送的分支
	2. 按'Space'切换到对应分支
	3. 按'p'推送

##### 错误

你现在大概率无法推送，因为github的安全措施会拒绝没有访问仓库权限的令牌的请求
你现在连令牌都没有
我太懒了不想写了，你问AI吧 ;->>>

> 请帮我配置 GitHub Token，让我能够推送代码到 GitHub 仓库

配置步骤：
1. [创建 Token](https://github.com/settings/tokens/new)
2. 勾选 `repo` 权限
3. 生成后复制 Token
4. 在命令行执行：
   ```bash
   git remote set-url origin https://你的用户名:你的Token@github.com/你的用户名/仓库名.git
   ```

> 现在再试试推送吧 ;-)

##### 持久化配置

如果你不想每次都复制粘贴 Token，可以配置 credential helper：

```bash
# Windows
git config --global credential.helper manager

# 第一次推送时输入用户名和 Token
# 之后会自动记住
```

> 在 Windows 上，凭证会保存在系统的 Credential Manager 中
> 在 Mac 上，会保存在 Keychain 中
> 在 Linux 上，可能需要安装 `libsecret` 或 `git-credential-libsecret`

#### 第一次合并

要开发一个功能，最好是给这个功能单开一个分支
当一个功能完成时就可以合并开发分支到这个分支的主分支

在 lazygit 中：
1. 在分支面板
	1. 方向键选中要合并分支的主分支
	2. 按'Space'切换到对应分支
	3. 方向键选中要合并的分支
	4. 按'm'开始合并

#### 创建 Pull Request

推送成功后，GitHub 会自动提示创建 Pull Request，或者手动：

1. 打开仓库页面
2. 点击 **Compare & pull request**
3. 选择 base 分支（develop）← compare 分支（feature/todo）
4. 填写标题和描述
5. 点击 **Create pull request**

> 你已经达成成就 ==第一个 PR== ;-)

#### 再一次推送到 Github

![[#推送]]

## 工具使用技巧

### 获取更好的回答

- 提供清晰的上下文
- 说明你的编程语言和环境
- 描述你期望的输出格式
- 如果结果不对，明确指出哪里不对
## 小结

- 工具涉及核心概念：
	- [[概念-API提供商|AI提供商]]
	- [[概念-Agent工具|Agent]]
	- [[概念-代码编辑器|代码编辑器]]
	- [[概念-代码管理|代码管理]]
## 作业

用 AI 辅助开发一个命令行 Todo List 应用。

### 功能要求

1. **添加待办**：输入待办内容，保存到文件
2. **查看待办**：列出所有待办事项
3. **删除待办**：根据序号删除指定待办
4. **标记完成**：根据序号标记待办为已完成
5. **数据持久化**：使用 JSON 文件存储数据

### 示例 prompt

> 请用 Python 写一个命令行 Todo List 应用，功能包括：
> 1. 添加待办事项（输入内容，回车保存）
> 2. 查看所有待办事项（显示序号和内容，已完成的显示 ✓）
> 3. 删除待办事项（输入序号删除）
> 4. 标记完成（输入序号标记为已完成）
> 5. 数据保存到 todos.json 文件

### 状态机视角

用状态机思考这个程序：

```mermaid
stateDiagram-v2
    [*] --> 空闲状态
    空闲状态 --> add命令 : 用户输入
    空闲状态 --> list命令 : 用户输入
    空闲状态 --> done命令 : 用户输入
    空闲状态 --> delete命令 : 用户输入
    add命令 --> 空闲状态 : 保存数据
    list命令 --> 空闲状态 : 显示列表
    done命令 --> 空闲状态 : 修改状态
    delete命令 --> 空闲状态 : 删除数据
```

### 提交要求：完整开发流程

按照以下步骤完成作业：

1. **创建 GitHub 仓库**（参考 [[A02-第一个让AI编写的程序？#创建 GitHub 仓库]]）
2. **克隆到本地**
3. **创建 develop 分支**
4. **从 develop 创建 feature/todo 分支**
5. **用 AI 实现功能**
6. **提交代码**
7. **推送到远程**
8. **创建 PR**（develop ← feature/todo）

---

## 思考题

1. 你之前使用过哪些AI工具？有什么体验？
2. 你选择工具时最看重哪些因素？
3. 你计划使用哪个工具作为主要编程助手
