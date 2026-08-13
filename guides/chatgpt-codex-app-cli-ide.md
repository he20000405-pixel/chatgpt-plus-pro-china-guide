---
title: "ChatGPT Plus / Pro 使用 Codex 指南"
description: "已有 ChatGPT Plus 或 Pro 后，如何用同一账号登录 Codex 桌面端、CLI 和 IDE 扩展，并完成第一次安全的本地项目操作。"
permalink: /guides/chatgpt-codex-app-cli-ide/
schema_type: Article
date_published: 2026-08-14
last_modified_at: 2026-08-14
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Codex App、CLI 与 IDE"
    url: /guides/chatgpt-codex-app-cli-ide/
faq:
  - question: "ChatGPT Plus 或 Pro 可以直接登录 Codex 吗？"
    answer: "可以。选择 Sign in with ChatGPT，并登录拥有有效 Plus 或 Pro 订阅的同一 ChatGPT 账号。OpenAI 当前也在其他部分 ChatGPT 套餐中提供 Codex；本文只说明 Plus 和 Pro 的使用流程，实际入口与用量以账号实时页面为准。"
  - question: "使用 Codex CLI 或 IDE 扩展必须准备 API Key 吗？"
    answer: "不必须。使用 Sign in with ChatGPT 时走 ChatGPT 账号登录；只有主动选择 API Key 工作流时才涉及独立 API 账号和 API 计费。"
  - question: "Codex 桌面端、CLI 和 IDE 扩展需要全部安装吗？"
    answer: "不需要。希望用图形界面管理任务可先用 ChatGPT 桌面端；习惯终端可用 CLI；希望在编辑器中查看代码和差异可用 IDE 扩展。"
  - question: "CLI 登录后为什么没有显示我的 Plus 或 Pro 权益？"
    answer: "先运行 codex login status 确认当前认证方式。若怀疑登录了错误账号，运行 codex logout 清除当前凭据，再运行 codex login，并在浏览器中使用原订阅账号完成授权。/status 用于查看当前会话和剩余用量，不等于账号身份凭证。"
  - question: "Codex 提示达到使用上限，是否代表订阅失效？"
    answer: "不一定。Plus 和 Pro 包含计划内 Codex 用量，达到当前限额不等于会员失效。应先打开官方 Usage Dashboard，确认计划状态和剩余用量，再按账号页面的实时提示处理。"
---

# ChatGPT Plus / Pro 开通后，如何使用 Codex App、CLI 和 IDE？

<style>
.article-page pre {
  max-width: 100%;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

.article-page pre code {
  display: block;
  width: max-content;
  min-width: 100%;
  box-sizing: border-box;
  overflow-wrap: normal;
  word-break: normal;
}
</style>

**直接答案：**如果你的 ChatGPT Plus 或 Pro 订阅已经生效，可以在 Codex 中选择 **Sign in with ChatGPT**，并登录同一个 ChatGPT 账号。你不需要同时安装三个入口：先按自己的工作方式选择桌面端、命令行或编辑器扩展，再用一个只读小任务验证账号、项目目录和权限是否正确。

OpenAI 当前在多种 ChatGPT 套餐中提供 Codex。本文只讨论 Plus 和 Pro，因为这是本站 ChatGPT 服务覆盖的两类付费套餐。很多用户把桌面中的 Codex 工作区简称为“Codex App”，而官方当前文档将它放在 **ChatGPT 桌面应用**中；CLI 和 IDE 扩展则分别面向终端和代码编辑器。

> 本文只解决“已有 ChatGPT Plus / Pro 后，怎样开始使用 Codex”的问题。它不介绍 API 充值，也不把 Codex 的使用上限误写成会员失效。

## 先选入口：App、CLI 和 IDE 有什么区别

三个入口使用的是同一个 ChatGPT 登录身份，但操作位置不同。

| 入口 | 适合的场景 | 第一次使用时要做什么 |
|---|---|---|
| ChatGPT 桌面端中的 Codex | 希望用图形界面打开文件夹、管理对话和查看结果 | 安装桌面应用，登录 ChatGPT 账号，选择 Codex 并打开项目文件夹 |
| Codex CLI | 习惯 PowerShell、Terminal 或命令行，希望直接在项目目录工作 | 安装 CLI，在项目目录运行 `codex`，选择 Sign in with ChatGPT |
| Codex IDE 扩展 | 主要在 VS Code、Cursor、Windsurf、Xcode 或 JetBrains 中写代码 | 安装或启用集成，在编辑器中打开 Codex 并登录同一账号 |

**选择原则很简单：**不熟悉命令行，先用桌面端；日常工作离不开终端，选 CLI；希望一边看代码一边审查修改，选 IDE 扩展。以后可以再增加其他入口，无需一开始全部安装。

## 开始前先完成 3 项检查

### 1. 确认当前 ChatGPT 账号

先在 ChatGPT 网页端登录，记录以下信息：

- 当前使用的登录方式，例如 Google、Apple、Microsoft 或邮箱；
- 当前账号是否显示有效的 Plus 或 Pro 计划；
- 是否存在待处理的付款或账号归属问题。

随后在 Codex 中使用**同一种登录方式和同一个账号**。如果浏览器同时登录了多个 ChatGPT 账号，授权时尤其容易选错。

### 2. 给项目建立可恢复点

在让 Codex 修改文件前，先确认项目已备份，或在 Git 中保存当前状态。OpenAI 的 CLI 和 IDE 快速入门都建议在任务前后建立 Git 检查点，这样出现不符合预期的修改时可以恢复。

### 3. 清理不应交给 AI 的内容

不要把以下信息写进提示词或测试文件：

- 密码、验证码和恢复码；
- 私钥、生产环境令牌和完整 Cookie；
- ChatGPT session；
- 客户资料和未脱敏的订单信息。

Codex 能读取哪些文件、执行哪些命令，取决于你打开的目录和批准的权限。第一次使用时应从只读任务开始。

## 路径一：使用 ChatGPT 桌面端中的 Codex

这个入口适合希望通过图形界面开始的用户。

### 第 1 步：安装官方桌面应用

进入 OpenAI 的 [ChatGPT 桌面应用说明](https://learn.chatgpt.com/docs/app)，选择适合当前系统的官方安装入口。官方当前文档列出 macOS、Windows 和 Linux。

安装完成后打开应用。如果系统已有旧版本，先更新到当前版本，再继续下一步。

### 第 2 步：登录原 ChatGPT 账号

点击登录，并使用前面确认过的 Plus 或 Pro 账号。完成后先核对头像、邮箱或登录方式，不要看到界面后就直接开始任务。

如果桌面端显示的计划与网页端不同，先退出桌面端，再用原账号重新登录。此时不要重新订阅。

### 第 3 步：进入 Codex 并打开项目

官方当前流程允许在桌面端选择 ChatGPT 或 Codex。在 Codex 中新建对话，然后打开要处理的项目文件夹。

第一次不要让它直接改代码，先发送：

```text
只读取当前项目。请说明目录结构、主要技术栈和本地启动命令，不要修改任何文件，也不要运行会写入数据的命令。
```

**预期结果：**Codex 能识别你打开的目录，并给出项目说明，但没有生成文件修改。

如果它读取了错误目录，立即停止当前任务，重新选择正确文件夹。不要用提示词让它跨目录寻找私人文件。

## 路径二：使用 Codex CLI

CLI 适合已经会使用 PowerShell、Terminal 或其他命令行工具的用户。

### 第 1 步：按系统安装

OpenAI 当前提供独立安装脚本，也保留 npm 安装方式。以下命令来自当前官方 CLI 文档。

Windows PowerShell：

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://chatgpt.com/codex/install.ps1 | iex"
```

macOS 或 Linux：

```bash
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

已配置 Node.js 和 npm 的用户，也可以使用：

```bash
npm install -g @openai/codex
```

安装命令可能随版本调整。执行前应再次查看 [Codex CLI 官方页面](https://learn.chatgpt.com/docs/codex/cli)；不要从不明网站下载同名程序。

### 第 2 步：进入项目目录

先在终端切换到项目根目录，再启动 Codex。例如在 PowerShell 中：

```powershell
Set-Location 'C:\你的项目路径'
codex
```

目录必须是你准备让 Codex读取和操作的项目。不要在用户主目录、桌面根目录或包含大量私人文件的位置直接启动。

### 第 3 步：选择 ChatGPT 登录

第一次运行时，选择 **Sign in with ChatGPT**。浏览器打开授权页后，确认页面登录的是原 Plus 或 Pro 账号，再完成授权。

授权完成后，先在普通终端中运行：

```text
codex login status
```

这条命令用于确认当前采用 ChatGPT 登录还是 API Key 登录。然后进入项目目录并运行 `codex`，在交互界面中输入：

```text
/status
```

`/status` 用于查看当前会话配置和剩余用量。它不能单独证明浏览器授权的是哪个 ChatGPT 账号。若怀疑登录了错误账号，退出 Codex 后依次运行：

```text
codex logout
codex login
```

在重新打开的浏览器页面中，使用原 Plus 或 Pro 账号完成授权。确认登录后，再运行：

```text
/permissions
```

检查 Codex 当前被允许执行的操作。不要为了省事直接扩大权限；遇到命令确认时，应先看清命令和作用范围。

### 第 4 步：发送第一次只读任务

```text
检查当前项目的 README 和配置文件，告诉我如何安装依赖和运行测试。不要修改文件，也不要执行安装命令。
```

**预期结果：**CLI 给出基于当前项目的说明，并且没有出现文件差异。

如果终端提示找不到 `codex`，先关闭并重新打开终端，再运行一次。仍无法识别时，回到官方安装页检查安装是否完成以及命令所在目录是否已加入系统 PATH，不要连续执行多个来源不明的修复脚本。

## 路径三：使用 Codex IDE 扩展

IDE 扩展适合希望在编辑器里直接引用当前文件、选中代码和查看差异的用户。

### 第 1 步：安装或启用官方集成

根据 [Codex IDE 官方说明](https://learn.chatgpt.com/docs/codex/ide)选择编辑器：

- VS Code、Cursor、Windsurf 和 VS Code Insiders 使用 Codex 扩展；
- Xcode 和 JetBrains IDE 使用各自的集成入口。

安装时核对发布者和官方链接，不要安装名称相近的第三方扩展。

### 第 2 步：打开 Codex 面板

在 VS Code、Cursor 或 Windsurf 中点击 Codex 图标。如果没有看到图标，打开命令面板并运行：

```text
Codex: Open Codex Sidebar
```

Xcode 用户在 coding assistant 中新建对话并选择 Codex；JetBrains 用户在 AI Chat 中选择 Codex。

### 第 3 步：登录并核对项目

使用同一个 ChatGPT Plus 或 Pro 账号登录，然后打开项目文件夹。先确认编辑器顶部显示的项目名称和文件路径正确，再发送任务。

第一次可以选中一个不含敏感信息的文件，并发送：

```text
解释这段代码的输入、输出和错误处理，不要修改文件。
```

**预期结果：**Codex 能结合当前打开或选中的代码进行解释。确认上下文正确后，再让它进行一个范围明确的小修改。

## 第一次修改任务应该怎样做

完成只读验证后，再按以下顺序尝试修改：

1. 用 Git 保存当前状态；
2. 只提出一个明确的小任务；
3. 限定允许修改的文件；
4. 阅读 Codex 准备执行的命令；
5. 检查最终差异；
6. 运行与这次修改直接相关的测试；
7. 确认无误后再提交。

示例：

```text
只修改 src/components/LoginNotice.tsx：把空状态提示改得更清楚，并补充现有测试。不要修改依赖、路由或其他文件。完成后列出改动，并运行这个组件对应的测试。
```

任务越具体，越容易判断结果是否正确。不要用“把整个项目都优化一下”作为第一次修改任务。

## 常见问题按什么顺序排查

| 症状 | 先检查什么 | 下一步 |
|---|---|---|
| 网页端是 Plus / Pro，Codex 却像未订阅账号 | `codex login status` 显示的认证方式，以及浏览器授权时是否选了另一个 ChatGPT 账号 | 运行 `codex logout`，再运行 `codex login` 并用原订阅账号授权；不要再次购买 |
| CLI 提示找不到 `codex` | 安装是否完成，终端是否在安装后重新打开 | 按官方安装页检查 PATH 或重新执行同一种官方安装方式 |
| IDE 中没有 Codex 图标 | 扩展是否启用，当前编辑器是否受支持 | 使用命令面板运行 `Codex: Open Codex Sidebar` |
| Codex 打开了错误项目 | 当前工作目录或编辑器工作区是否正确 | 停止任务，关闭错误目录，再打开目标项目 |
| 提示达到使用上限 | 账号计划是否仍有效，[Usage Dashboard](https://chatgpt.com/codex/settings/usage) 显示什么 | 区分“计划有效但用量已到上限”和“会员没有附着到该账号” |
| 出现 API Key 输入或 API 账单提示 | 是否选择了 API Key 登录方式 | 若准备使用 ChatGPT 订阅，退出并改选 Sign in with ChatGPT |
| 桌面端没有 Codex 入口 | 应用是否为当前版本，账号和地区是否具备当前可用性 | 更新应用、重新登录，并以 OpenAI 实时页面为准 |

如果 ChatGPT 官方页面也显示 Free，先处理订阅账号问题，而不是反复安装 Codex。可以继续阅读[ChatGPT 已付款仍显示 Free 排查]({{ '/guides/chatgpt-paid-but-still-free/' | relative_url }})；若出现订阅关联其他账号的提示，则查看[订阅关联其他 OpenAI 账号]({{ '/guides/chatgpt-subscription-associated-with-another-account/' | relative_url }})。

## Plus、Pro、Codex 用量和 API 不是一回事

OpenAI 当前还在 Free、Go、Business、Enterprise 和 Edu 等计划中提供不同程度的 Codex 访问。本文聚焦 Plus 和 Pro，并不表示只有这两种套餐才能使用 Codex。

Plus / Pro 用户需要区分三件事：

1. **ChatGPT Plus 或 Pro 订阅**：包含一定的 Codex 使用量；
2. **Codex 账号内的可选 credits**：达到计划内用量后，符合条件的账号可能看到官方追加选项；
3. **OpenAI API 计费**：属于独立的开发者平台账单，不等于 ChatGPT 会员。

OpenAI 当前说明，Plus 和 Pro 包含计划内 Codex 用量；具体上限会受到模型、任务复杂度以及本地或云端执行方式影响。请在 [Codex Usage Dashboard](https://chatgpt.com/codex/settings/usage) 查看账号当前的剩余用量。达到计划内上限后，账号是否提供 ChatGPT credits 选项，以及实际消耗规则，都以该页面和官方实时价格说明为准。

ChongGrok 只提供 ChatGPT 会员订阅协助，不提供 API 额度或 API 充值，也不代购 Codex credits。

## 什么时候才需要查看新的会员方案

如果账号已经有有效 Plus / Pro、已有成功扣款或存在待处理交易，应先处理账号和订阅状态，**不要再次购买**。

只有确认当前账号没有有效订阅、没有待处理付款，也没有需要继续处理的原订单后，才考虑新的 Plus 或 Pro 方案。ChongGrok 的实时方案与交付规则见 [chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)。

## 安全与服务边界

- 在 Codex 中使用官方 ChatGPT 登录时，不要向第三方提供 ChatGPT 密码；
- 只打开任务需要的项目目录，并逐项审查命令和文件差异；
- 不要把 session、私钥、验证码或生产环境令牌放进提示词；
- 不要公开或提交 `~/.codex/auth.json`；官方说明该文件可能包含访问令牌，应按密码同等谨慎保管；
- ChatGPT 会员不等于 OpenAI API 额度；
- ChongGrok 与 OpenAI 没有隶属关系；
- 软件入口、套餐可用性、模型和额度会变化，以 OpenAI 当前页面为准；
- 任何在线服务和自动化代码修改都不是零风险。

## 常见问题

### ChatGPT Plus 或 Pro 可以直接登录 Codex 吗？

可以。启动桌面端、CLI 或 IDE 集成后选择 **Sign in with ChatGPT**，并使用拥有有效订阅的原 ChatGPT 账号完成授权。OpenAI 当前也在其他部分计划中提供 Codex，具体可用性和用量以官方实时页面为准。

### 使用 Codex CLI 或 IDE 扩展必须准备 API Key 吗？

不必须。选择 **Sign in with ChatGPT** 时使用 ChatGPT 账号和计划内用量；只有主动选择 API Key 登录时，才进入独立的 OpenAI Platform 计费流程。

### Codex 桌面端、CLI 和 IDE 扩展需要全部安装吗？

不需要。图形界面用户可先用桌面端；终端用户可用 CLI；主要在编辑器中工作的用户可安装 IDE 扩展。确认一个入口可以正常工作后，再按需要增加其他入口。

### CLI 登录了错误账号应该怎样重来？

先在普通终端运行 `codex login status` 查看认证方式。若需要清除当前凭据，运行 `codex logout`，再运行 `codex login`，并在浏览器中使用原订阅账号完成授权。不要因为登录错账号再次购买会员。

### Codex 达到使用上限是否代表 Plus 或 Pro 已失效？

不一定。先检查 ChatGPT 计划是否仍有效，再打开 [Codex Usage Dashboard](https://chatgpt.com/codex/settings/usage) 查看剩余用量。计划有效但用量达到当前上限，与订阅失效是两种不同状态。

## OpenAI 官方来源

- [ChatGPT 桌面应用](https://learn.chatgpt.com/docs/app)
- [Codex CLI](https://learn.chatgpt.com/docs/codex/cli)
- [Codex IDE 扩展](https://learn.chatgpt.com/docs/codex/ide)
- [Codex 登录与认证方式](https://learn.chatgpt.com/docs/auth)
- [Codex 与 ChatGPT 计划的当前可用性和用量](https://learn.chatgpt.com/docs/pricing)

**核验日期：2026 年 8 月 14 日。**安装方式、界面名称、套餐可用性和用量规则可能变化，请在操作前核对 OpenAI 官方实时页面。
