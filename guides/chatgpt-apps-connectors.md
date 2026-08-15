---
title: "ChatGPT Apps 使用指南：连接、权限与排障"
description: "从 Plugins Directory 连接 Gmail、Google Drive、Outlook 或 GitHub，设置应用权限，完成只读测试，并排查连接、同步和账号问题。"
permalink: /guides/chatgpt-apps-connectors/
schema_type: Article
date_published: 2026-08-15
last_modified_at: 2026-08-15
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "ChatGPT Apps 使用指南"
    url: /guides/chatgpt-apps-connectors/
faq:
  - question: "ChatGPT Connectors、Apps 和 Plugins 是同一项功能吗？"
    answer: "不是完全相同。OpenAI 已将原来的 connectors 统一称为 apps；从 2026 年 7 月 9 日起，Plugins Directory 成为发现工作流能力的主要入口。Plugin 可以包含技能、应用和应用模板，而 App 仍负责连接外部数据或执行外部操作。"
  - question: "为什么 ChatGPT 中的 Connect 按钮是灰色的？"
    answer: "常见原因包括当前计划、地区、使用界面、工作区权限或管理员策略不支持该应用。若页面显示 Disabled by admin，应联系工作区管理员；不要因为一个按钮不可用就重复购买订阅。"
  - question: "连接应用后，怎样在聊天中调用它？"
    answer: "连接完成后，可以在提示词中使用 @ 提及对应插件，或点击输入框旁的加号，再从 More 中选择需要使用的应用。首次测试应只执行读取任务，并核对结果是否来自正确账号和资料。"
  - question: "为什么 ChatGPT 找不到刚连接的 Google Drive 文件？"
    answer: "先确认连接的是正确 Google 账号、自己本来就有权访问该文件，并检查是否启用了 Sync。同步需要一定时间，单位账号还可能因 Google Workspace 授权范围没有获批而失败。"
  - question: "连接 GitHub 后，ChatGPT 可以直接修改或推送代码吗？"
    answer: "不能依赖 ChatGPT 的 GitHub 应用执行写入。OpenAI 当前说明，该应用用于读取、搜索、分析和引用仓库内容；需要生成、修改或推送代码时，应使用 Codex，并单独核对其权限。"
  - question: "ChatGPT Plus 一定能使用所有 Apps 吗？"
    answer: "不能这样保证。Plugins Directory 对多个计划可见，但具体插件和应用能否安装或调用，还取决于计划、地区、工作区、角色、使用界面和应用本身。应以插件详情页和当前账号实际显示为准。"
  - question: "怎样彻底停止 ChatGPT 访问已经连接的 App？"
    answer: "进入 Settings → Apps，打开对应应用并选择 Disconnect。仅修改 Ask permission 不会撤销已经授予的访问；还应按需要在第三方账号中撤销授权，并检查相关聊天、记忆和同步数据。"
  - question: "Voice mode 可以使用已连接的 Apps 吗？"
    answer: "OpenAI 当前说明，Voice mode 暂不支持 Apps。文字聊天中可以使用某个应用，并不代表语音模式也能调用它。"
---

# ChatGPT Apps 怎么用？连接 Gmail、Google Drive、Outlook 与 GitHub 完整流程

**直接答案：**ChatGPT Apps 可以在你授权后读取或操作 Gmail、Google Drive、Outlook、GitHub 等外部服务，当前主要从 **Plugins Directory** 进入。先确认插件包含哪些 App 和权限，再点击 `Connect` 登录第三方账号；连接后用一条只读指令核对账号和数据范围，确认结果正确后再执行创建、修改或发送等操作。

如果 `Connect` 按钮不可用、文件找不到或应用无法执行操作，不要反复授权或重新购买会员。应依次检查当前 ChatGPT 账号、第三方账号、计划与地区、工作区管理员设置、应用权限和同步状态。

> 本文只解决 ChatGPT Apps 的连接、调用、权限、断开和常见排障。它不介绍自建 MCP 应用，也不涉及 OpenAI API 额度或 API 充值。

## 先分清 Plugins、Apps 和旧名称 Connectors

OpenAI 的界面名称已经发生变化。理解下面三者的关系，才能在当前页面中找到正确入口。

| 名称 | 当前含义 | 你实际需要做什么 |
|---|---|---|
| Plugin | 一套面向具体工作流的能力包，可以包含技能、Apps 和应用模板 | 在 Plugins Directory 中查找并查看详情 |
| App | 连接 Gmail、Google Drive、Outlook、GitHub 等外部服务的数据或操作 | 点击 Connect，登录第三方账号并授权 |
| Connector | Apps 的旧称，旧帮助文章或搜索结果仍可能使用 | 看到旧名称时，回到当前 Plugins / Apps 页面核对 |
| App template | 供单位管理员创建工作区专用应用的配置模板 | 普通个人用户通常不能直接把模板当成可用 App |

自 **2026 年 7 月 9 日**起，OpenAI 将应用目录迁移到 Plugins Directory。已有 App 连接不会因此自动失效，但新连接应优先从当前插件目录进入。

## 开始前准备 4 项信息

连接外部服务前，先完成下面的准备。这样可以避免把私人邮箱、工作账号或错误仓库授权给当前 ChatGPT 账号。

1. **确认 ChatGPT 账号。**打开账户菜单，核对登录邮箱、登录方式和当前计划；
2. **确认第三方账号。**决定要连接哪个 Google、Microsoft 或 GitHub 账号，不要在授权页面临时猜选；
3. **确定最小数据范围。**GitHub 只选需要分析的仓库，单位应用只启用当前工作所需权限；
4. **准备一条只读测试。**例如“列出我本周收到的三封项目邮件标题”，不要把“发送邮件”作为第一次测试。

**停止条件：**如果授权页面要求的权限明显超出当前任务，或显示了错误的第三方账号，应取消授权并重新核对，不要先同意再处理。

## 第一步：从 Plugins Directory 找到并连接 App

当前通用连接流程如下：

1. 打开 ChatGPT 网页版或桌面版；
2. 从侧边栏进入 **Plugins**，或打开 `Settings → Plugins`；
3. 在 Plugins Directory 中搜索需要的工作流或服务；
4. 打开详情页，确认它包含哪些 Apps、能读取什么、能执行什么操作；
5. 需要连接第三方服务时，点击 `Connect`；
6. 在第三方登录页面选择正确账号；
7. 阅读授权范围后确认；
8. 返回 ChatGPT，检查详情页是否显示已连接。

**预期结果：**对应 App 显示为已连接，并可在 ChatGPT 对话中调用。

如果 `Connect` 是灰色的，先查看按钮提示：

- 显示 `Disabled by admin`：由工作区管理员启用，个人用户反复刷新无法解决；
- 提示计划或地区不可用：以当前详情页为准，不要根据旧教程反复退出登录；
- 单位账号要求管理员批准：联系 ChatGPT 工作区管理员或第三方系统管理员；
- 详情页可见但无法安装：继续核对当前角色、使用界面和应用支持范围。

## 第二步：先把 App 权限设为可控状态

连接成功只表示 ChatGPT 获得了已授权的访问范围。`Ask permission` 决定 ChatGPT 在使用这些权限时，哪些动作必须再次向你确认。

1. 打开 `Settings → Apps`；
2. 在 **App Preferences** 中找到 `Ask permission`；
3. 第一次使用时，选择 `Always ask` 或 `Any changes`；
4. 若要单独调整某个 App，从 Plugins Directory 打开它的详情；
5. 在该 App 的 `Preferences` 中修改 `Ask permission`；
6. 保存后重新打开详情页，确认设置没有恢复为其他选项。

| 权限级别 | ChatGPT 何时询问 | 适合什么情况 |
|---|---|---|
| Always ask | 读取和执行操作前都询问 | 第一次连接，或数据较敏感 |
| Any changes | 读取可以自动进行，修改前询问 | 已核对读取范围，但不希望自动写入 |
| Important actions | 读取可自动进行，重要外部操作前询问；这是当前默认级别 | 已熟悉应用，并愿意逐次审核重要操作 |
| Never ask | 可以在不再次确认的情况下读取或执行操作 | 风险较高，不适合作为首次连接设置 |

权限卡片出现时，先阅读它准备使用的 App、数据和动作，再选择 `Deny`、`Allow once` 或页面提供的其他选项。不要为了省一次确认而直接长期允许发送邮件、删除内容、修改共享权限或执行交易。

需要注意：修改 `Ask permission` **不会扩大或缩小第三方已经授权的数据范围**。要撤销访问，必须断开 App 或在第三方账号中撤销授权。

## 第三步：用一条只读指令验证连接

连接后不要马上让 ChatGPT 修改外部数据。先验证它是否连接了正确账号、能否访问预期内容，以及引用是否可以核对。

1. 新建一个普通文字聊天；
2. 在提示词中输入 `@` 并选择相应插件，或点击输入框旁的 `+ → More` 选择 App；
3. 输入一条范围很小的只读任务；
4. 核对返回结果中的账号、文件、邮件、仓库或日期；
5. 打开原服务，确认结果与原始内容一致；
6. 只有读取测试正确后，才进入后续工作流。

可以使用这些测试指令：

- Gmail：`列出昨天主题中包含“项目周报”的邮件，只返回发件人、主题和时间。`
- Google Drive：`找到标题中包含“预算草案”的文件，只列出文件名和修改日期。`
- Outlook：`列出今天未读的三封邮件，只返回发件人和主题。`
- GitHub：`在我授权的仓库中查找 README，并说明每个仓库的用途。`

**停止条件：**如果结果出现不属于自己的文件、邮件或仓库，应立即停止使用，回到 `Settings → Apps` 检查连接账号和访问范围。

## Gmail 与 Google Drive：先核对账号，再判断是否需要 Sync

Google Apps 可以读取当前授权账号中的相关内容。部分应用还支持 **Sync（同步）**，即提前建立索引，让 ChatGPT 更快找到更新后的资料。

### 连接与验证

1. 从 Plugins Directory 找到包含 Gmail 或 Google Drive 的插件；
2. 点击 `Connect`，选择正确 Google 账号；
3. 阅读 Google 授权页面列出的权限；
4. 返回 ChatGPT，使用只读指令查找一封邮件或一个文件；
5. 打开 Google 原页面，核对标题、日期和内容来源。

Google Docs、Sheets 和 Slides 的相关操作现在归入 **Google Drive App**。当前目录中不再提供三个独立的 Docs、Sheets、Slides App，因此找不到独立入口时，不要继续搜索旧名称。

### Google Drive Sync 的边界

OpenAI 当前明确说明，Google Drive App with Sync 的自助配置面向 ChatGPT Pro 用户，以及符合条件的 Business、Enterprise 工作区管理员。入口为：

`Profile → Settings → Apps → Google Drive → Connect → Sync`

同步不会立即完成，官方没有承诺固定时长。刚连接后找不到文件时：

1. 确认 `Sync` 已经开启；
2. 确认自己在 Google Drive 原页面有访问权；
3. 等待同步建立，不要连续断开和重新连接；
4. 单位账号出现授权错误时，让 Google Workspace 管理员核对所需 OAuth scopes；
5. 仍无法访问时，保存错误原文和发生时间，再联系工作区管理员或 OpenAI 支持。

Google Workspace 的管理员级部署需要单位域名；`gmail.com` 和 `googlemail.com` 不能作为该类工作区域名配置。这个限制不等于所有个人 Google 账号都不能连接普通 Google Apps，应根据当前功能和详情页分别判断。

## Outlook Email 与 Calendar：邮件和日历权限不是一回事

Outlook Email App 可以搜索邮件、人员和联系人；在管理员启用相应 Actions 后，还可能创建或修改联系人。Outlook Calendar App 可以读取和搜索日历事件、参会人和空闲时间，但 OpenAI 当前说明，日历事件数据仍为只读。

### 个人账号或已获单位批准的账号

1. 从 Plugins Directory 找到 Outlook Email 或 Outlook Calendar；
2. 点击 `Connect` 并登录正确 Microsoft 账号；
3. 完成授权后，先查询当天邮件或未来一天的日程；
4. 核对返回内容是否来自正确邮箱和日历；
5. 需要联系人写入操作时，再单独确认权限卡片。

### 出现 Microsoft Entra 管理员错误

单位 Microsoft 账号可能需要 Microsoft Entra 管理员批准 Graph 权限。还要注意，**Entra 批准不等于 ChatGPT 工作区已经启用 App，也不等于用户已经完成连接**。

管理员应分别核对：

1. ChatGPT 工作区中的相应 Action 是否启用；
2. Microsoft Entra 中的权限授权是否仍有效；
3. 用户是否在权限变化后重新连接或刷新了 Microsoft 账号。

如果刚收到的邮件没有出现，可以先缩小查询日期和关键词，再等待索引更新。查询数月或数年的全部邮件也可能触发 Microsoft 服务限制，此时应拆成较短日期范围，不要重复提交同一个大请求。

## GitHub：仓库访问范围和 Sync 选择要分别检查

GitHub App 适合在 ChatGPT 中读取、搜索、分析和引用仓库代码或文档。它不是代码推送工具。

### 连接 GitHub

1. 打开 `Settings → Apps`，找到 GitHub；
2. 点击连接后进入 GitHub 授权页面；
3. 只选择当前需要分析的仓库；
4. 返回 ChatGPT，按页面提示选择常用的同步仓库；
5. 使用只读问题测试，例如“这个仓库的入口文件在哪里？”；
6. 打开 GitHub 原仓库，核对 ChatGPT 引用的文件和代码片段。

GitHub 中允许访问哪些仓库，与 ChatGPT 中选择哪些仓库优先 Sync 是两项不同设置。即使某个仓库没有被选为同步对象，只要 GitHub 授权允许，ChatGPT 仍可能按需访问它。

### 仓库没有出现时

按下面顺序排查：

1. 连接后先等待约 5 分钟；
2. 进入 `Settings → Apps → GitHub → Choose repositories`；
3. 检查 GitHub 端是否允许访问该私有或新建仓库；
4. 单位仓库需要管理员批准时，先提交访问申请；
5. GitHub 尚未建立搜索索引时，在 GitHub 中搜索 `repo:用户名/仓库名 import` 触发索引，再等待几分钟；
6. 仍不可见时，保存仓库名称、授权范围、发生时间和错误提示。

OpenAI 当前说明，ChatGPT 的 GitHub App 只能读取和分析仓库。需要修改文件、创建提交或推送代码时，应使用 [ChatGPT Plus / Pro 使用 Codex 指南]({{ '/guides/chatgpt-codex-app-cli-ide/' | relative_url }})，并在执行前检查 Codex 的仓库和文件权限。

## 连接成功但无法使用：按这个顺序排查

| 页面现象 | 先判断什么 | 下一步 |
|---|---|---|
| Connect 按钮是灰色 | 计划、地区、角色或管理员限制 | 阅读按钮提示；显示管理员禁用时联系管理员 |
| 授权后又回到未连接 | 是否选错账号、弹窗被拦截或授权范围被拒绝 | 允许授权弹窗，核对第三方账号后只重连一次 |
| App 已连接，但聊天中找不到 | 是否使用支持的界面，是否从 `@` 或 `+ → More` 调用 | 更新 ChatGPT，打开插件详情核对支持的界面和模型 |
| Google 文件找不到 | 原账号权限、Sync 状态和 Workspace scopes | 核对账号与权限，等待同步；单位账号联系管理员 |
| Outlook 连接失败 | Entra 权限和 ChatGPT Action 是否都已启用 | 让两侧管理员分别核对，再刷新用户连接 |
| GitHub 仓库缺失 | 仓库授权、管理员审批和索引是否完成 | 重新选择仓库并等待索引，不要重复安装 App |
| 能读取但不能修改 | App 或管理员只允许读取，或动作需要批准 | 查看权限卡片和 Action control；不要绕过限制 |
| 语音对话无法调用 | Voice mode 当前不支持 Apps | 切换到文字聊天完成任务 |

如果所有 Apps 都同时异常，应先查看 [OpenAI Status](https://status.openai.com/)。只有某一个第三方服务异常时，同时检查该服务状态和账号权限。

## 断开连接和清理数据

不再使用某个 App 时，不要只删除当前聊天。应同时撤销连接并处理已经进入聊天或记忆的数据。

1. 打开 `Settings → Apps`；
2. 选择对应 App；
3. 点击 `Disconnect`；
4. 在 Google、Microsoft 或 GitHub 的账号安全页面检查并撤销不再需要的第三方授权；
5. 删除包含敏感外部数据的相关聊天；
6. 打开 `Settings → Personalization`，检查 Memory 是否保存了相关信息；
7. 打开 `Settings → Data Controls`，按需要关闭 `Improve the model for everyone`。

OpenAI 当前说明，断开 Google App 后，其同步建立的索引副本会在 30 天内删除。删除一条聊天时，保留在该聊天中的连接应用数据也会在 30 天内删除。不同第三方服务仍有各自的数据条款，断开 ChatGPT 并不会自动删除原服务中的文件、邮件或仓库。

个人计划的数据使用还要分开判断：一般 Apps 内容在 `Improve the model for everyone` 开启时可能用于改进模型；Google 同步数据另有专门规则，OpenAI 表示不会直接用同步的 Google App 数据训练通用模型，但用户反馈、手动复制或上传的数据，以及已经进入回答的内容存在其官方列出的例外。不要把“连接 Google”简单理解为所有数据都用于训练，也不要理解为完全没有数据处理。

## 套餐、工作区和服务入口边界

Plugins Directory 对多个 ChatGPT 计划可见，但具体插件、Apps、Sync、Actions 和模型支持范围取决于：

- 当前 ChatGPT 计划；
- 国家或地区；
- 个人账号或单位工作区；
- 工作区角色和管理员设置；
- 网页、桌面端、移动端或特定模式；
- App 自身的功能和第三方账号权限。

因此，不能承诺升级 Plus 或 Pro 后一定出现所有 Apps。Google Drive Sync 当前有明确的 Pro 和工作区条件；GitHub App 在 Plus 中也可能只出现在 Deep Research 或 Agent 等特定体验，而不出现在普通聊天。

已有有效订阅、成功扣款或待处理交易时，不要为了某个 App 入口再次购买。只有确认当前没有有效或待处理订阅，并且 OpenAI 官方详情页明确显示目标计划包含所需能力时，才考虑新的会员方案；ChongGrok 当前 ChatGPT 方案见 [chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)。ChongGrok 无法保证受地区、工作区或第三方管理员控制的 App 立即开放。

## 完成验收清单

完成连接后，逐项确认：

- ChatGPT 和第三方服务都登录了正确账号；
- 只授权了当前工作需要的数据和仓库；
- `Ask permission` 没有在不知情的情况下设为 `Never ask`；
- 一条小范围只读测试已经返回正确内容；
- 结果可以回到原邮件、文件、日历或仓库核对；
- 需要写入的动作会显示确认卡片；
- 管理员权限、第三方权限和用户连接没有被混为一件事；
- 不再使用的 App 已断开，并检查了聊天、Memory 和第三方授权；
- 没有提交密码、验证码、恢复码、session、Cookie 或访问令牌。

## 常见问题

### ChatGPT Connectors、Apps 和 Plugins 是同一项功能吗？

不是完全相同。OpenAI 已将原来的 connectors 统一称为 Apps；从 2026 年 7 月 9 日起，Plugins Directory 成为发现工作流能力的主要入口。Plugin 可以包含技能、Apps 和应用模板，而 App 仍负责连接外部数据或执行外部操作。

### 为什么 ChatGPT 中的 Connect 按钮是灰色的？

常见原因包括当前计划、地区、使用界面、工作区权限或管理员策略不支持该 App。若页面显示 `Disabled by admin`，应联系工作区管理员；不要因为一个按钮不可用就重复购买订阅。

### 连接应用后，怎样在聊天中调用它？

连接完成后，可以在提示词中使用 `@` 提及对应插件，或点击输入框旁的 `+`，再从 `More` 中选择需要使用的 App。首次测试应只执行读取任务，并核对结果是否来自正确账号和资料。

### 为什么 ChatGPT 找不到刚连接的 Google Drive 文件？

先确认连接的是正确 Google 账号、自己本来就有权访问该文件，并检查是否启用了 Sync。同步需要一定时间，单位账号还可能因 Google Workspace 授权范围没有获批而失败。

### 连接 GitHub 后，ChatGPT 可以直接修改或推送代码吗？

不能依赖 ChatGPT 的 GitHub App 执行写入。OpenAI 当前说明，该 App 用于读取、搜索、分析和引用仓库内容；需要生成、修改或推送代码时，应使用 Codex，并单独核对其权限。

### ChatGPT Plus 一定能使用所有 Apps 吗？

不能这样保证。Plugins Directory 对多个计划可见，但具体插件和 App 能否安装或调用，还取决于计划、地区、工作区、角色、使用界面和 App 本身。应以插件详情页和当前账号实际显示为准。

### 怎样彻底停止 ChatGPT 访问已经连接的 App？

进入 `Settings → Apps`，打开对应 App 并选择 `Disconnect`。仅修改 `Ask permission` 不会撤销已经授予的访问；还应按需要在第三方账号中撤销授权，并检查相关聊天、Memory 和同步数据。

### Voice mode 可以使用已连接的 Apps 吗？

OpenAI 当前说明，Voice mode 暂不支持 Apps。文字聊天中可以使用某个 App，并不代表语音模式也能调用它。

## OpenAI 官方来源

本文于 **2026 年 8 月 15 日**核验。Plugins、Apps、支持计划、地区和界面仍可能变化，操作前请以当前详情页和账号实际显示为准。

- [Plugins in ChatGPT and Codex](https://help.openai.com/en/articles/20001256)
- [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-apps-in-chatgpt)
- [Plugin use cases and prompts](https://help.openai.com/en/articles/12084614-app-use-cases-and-prompts)
- [Google App for ChatGPT - Data Controls FAQ](https://help.openai.com/en/articles/10408842)
- [Google Drive app with sync - Self-Service Setup](https://help.openai.com/en/articles/10948259-google-drive-synced-connectors-self-service-setup)
- [Connecting GitHub to ChatGPT](https://help.openai.com/en/articles/11145903-connecting-github-to-chatgpt-deep-research)
- [Outlook Email and Calendar app for ChatGPT](https://help.openai.com/en/articles/12512241-outlook-email-and-calendar-connectors-for-chatgpt)
- [Data Controls FAQ](https://help.openai.com/en/articles/7730893-chatgpt-data-controls-faq)

## 安全与服务边界

- 连接 App 时只授权当前任务需要的账号、文件、邮箱或仓库；
- 不向任何第三方提供 ChatGPT 密码、邮箱验证码或恢复码；
- 不在聊天中提交 session、完整 Cookie、访问令牌或未脱敏的私人资料；
- ChatGPT 会员不等于 OpenAI API 额度，ChongGrok 不提供 API 充值；
- ChongGrok 与 OpenAI、Google、Microsoft、GitHub 无隶属或官方合作关系；
- App 的开放范围、同步速度和第三方权限均可能变化，任何线上服务都不是零风险。
