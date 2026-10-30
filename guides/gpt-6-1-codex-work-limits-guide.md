---
title: "GPT-6.1 (Terra / Sol) 与 GPT-6 Astra、Codex 额度详解：2026 年 10 月 Plus 与 Pro 怎么选？"
description: "2026年10月最新说明：详解 OpenAI 最新发布的 GPT-6.1 Terra、GPT-6.1 Sol 与 GPT-6 Astra 模型分工，拆解 Codex 编程与 ChatGPT Work 在 Free、Go ($8)、Plus ($20)、Pro 100/200/500 下的额度差异及 Pro 200 用量规则调整，附国内通过 chonggrok.com 本号开通指南。"
permalink: /guides/gpt-6-1-codex-work-limits-guide/
date: 2026-10-28
last_modified_at: 2026-10-30
---

# GPT-6.1 (Terra / Sol) 与 GPT-6 Astra、Codex 额度详解：2026 年 10 月 Plus 与 Pro 怎么选？

**直接结论：** 截至 2026 年 10 月底，OpenAI 已将核心模型矩阵升级至 **GPT-6 Astra、GPT-6.1 Sol 与 10 月 26 日最新发布的 GPT-6.1 Terra**，并将 **Codex（AI 编程工具）** 与 **ChatGPT Work（ChatGPT 工作）** 深度集成至付费订阅中。其中 **$8/月的 ChatGPT Go** 可以让你比免费版生成更多图片、上传更多文件、使用更多次数据分析，但不包含 GPT-6.1 Terra / Sol 等高阶模型；**$20/月的 ChatGPT Plus** 是绝大多数开发者与办公用户的性价比首选，支持在 ChatGPT Work 和 Codex 中调用 GPT-6.1 Terra / Sol 与 GPT-6 Astra；**ChatGPT Pro（官方设 Pro 100 / Pro 200 / Pro 500 档）** 则面向每天持续进行高强度推理、长文档研究与重度编程的用户。国内用户若没有境外信用卡或遇到 Stripe 绑卡被拒，可通过 **[ChongGrok (chonggrok.com)](https://chonggrok.com)**（ChatGPT 专区：**[chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)**）使用支付宝或微信，为自己的 ChatGPT 账号开通 Plus 或 Pro。

---

## 一、 2026 年 10 月最新模型矩阵：GPT-6.1 Terra、Sol 与 GPT-6 Astra 怎么分工？

继 2026 年 7 月的 GPT-5.6 系列（详见 [GPT-5.6 更新、可用套餐与国内体验入口](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/gpt-5-6-update/)）之后，OpenAI 在 2026 年 10 月推出了新一代模型。对于日常使用 ChatGPT、ChatGPT Work 和 Codex 的用户，三大核心模型的真实定位与开放范围如下：

| 模型名称                       | 发布时间与核心定位                                           | 速度、成本与能力边界                                         | 开放入口与订阅套餐范围                                       |
| :----------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **GPT-6.1 Terra**              | **2026 年 10 月 26 日发布**；高性价比的日常专业工作与计算机操作（Computer Use）模型 | 在 OpenAI 公布的测试中，任务完成速度是 GPT-6 Astra 和 GPT-6.1 Sol 的 **3 倍以上**；擅长起草提案、解读技术图纸、填写表单、录入发票与剪辑视频。**在相同套餐额度下，使用 Terra 可完成的任务比使用 Sol 或 Astra 多得多** | 面向 **Plus、Pro、Business、Enterprise 和 Edu** 用户在 **ChatGPT Work（ChatGPT 工作）** 和 **Codex** 中开放 |
| **GPT-6.1 Sol**                | 复杂多步骤编程与智能体（Agent）深度主力模型                  | 以较低的成本，提供接近 GPT-6 Astra 的能力；相较于上一代 **GPT-6 Sol**，在低推理强度下事实准确度大幅提升。**OpenAI 官方指出：对于最复杂、要求最高的编程任务，GPT-6.1 Sol 与 GPT-6 Astra 依然是比 Terra 更优的选择** | 面向 **Plus、Pro、Business、Enterprise 和 Edu** 用户在 **ChatGPT Work** 和 **Codex** 中开放 |
| **GPT-6 Astra**                | 旗舰级前沿推理与最复杂工程架构模型                           | OpenAI 在最复杂计算机操控、高难度科研推导与大型工程任务上的最强模型，但单次消耗配额较高（Pro 500 档额外包含 Astra 与 6.1 Sol 的超高速模式） | **Plus：**可在 ChatGPT Work 和 Codex 中使用 GPT-6 Astra。<br>**Pro：**除了在 Work / Codex 中使用 Astra，还可在 ChatGPT 聊天中使用由 Astra 驱动的 GPT-6 Pro；聊天中的用量与 Work / Codex 分开计算。<br>企业用户按所购套餐及工作区权限使用。 |
| **GPT-5.6 Luna / GPT-6 Sol（快速回答）** | 低延迟日常快速对话模型                                       | 响应极快，适合日常问答、基础翻译与轻量文件处理 | 在 **ChatGPT 日常聊天**中，Free、**Go ($8)** 的快速回答使用 GPT-5.6 Luna；已开放 GPT-6 的 Plus、Pro 账号，快速回答由 GPT-6 Sol 提供，界面显示为“GPT-6”。（[官方说明](https://help.openai.com/en/articles/20001354-gpt-6-and-other-models-in-chatgpt)）                          |

> **选型与额度省流技巧：** 如果你开通了 $20/月的 ChatGPT Plus，日常办公自动化、读图纸、改常规代码时优先在 ChatGPT Work 和 Codex 里选 **GPT-6.1 Terra**，能在同样额度下完成更多任务；遇到最棘手的底层算法或复杂架构重构时，再切换至 **GPT-6.1 Sol** 或 **GPT-6 Astra**。国内用户如需升级个人原账号，可直接访问 **[chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)** 办理。

---

## 二、 官方套餐档位对比：Free、Go ($8)、Plus ($20) 与 Pro ($100 / $200 / $500) 怎么选？

真正影响日常使用体验的，不是一个笼统的“无限”标签，而是你会不会频繁触发特定模型或工具（如 Codex、ChatGPT Work、Deep Research）的用量限制：

| 套餐档位                  | 官方月费      | 总体额度与核心模型权限                                       | 适用人群与国内办理方式                                       |
| :------------------------ | :------------ | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **Free / Go**             | $0 / $8 每月  | Free 和 Go 都可以不限次数地进行日常文字聊天，仍受防滥用规则约束。相比 Free，Go 可以生成更多图片、上传更多文件、使用更多次数据分析，并让 ChatGPT 记住更多对话信息。 | 适合日常问答，以及尝试用 AI 写简单代码。功能开放后，Free / Go 用户可在桌面端 Codex 中使用 GPT-6 Luna。若需要使用 GPT-6.1 Terra、Sol 等模型处理更复杂的编程或办公任务，再考虑 Plus 或 Pro。（[官方说明](https://learn.chatgpt.com/docs/pricing)） |
| **ChatGPT Plus**          | **$20 / 月**  | 可使用 GPT-6.1 Terra / Sol、GPT-6 Astra、Codex、ChatGPT Work 与 Deep Research | **绝大多数个人用户的首选**；在 **[chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)** 下单取得卡密后，支持到 **`/verify` 全自动核销** |
| **ChatGPT Pro 100**  | **$100 / 月** | **Work / Codex 的使用额度高于 Plus**；在 ChatGPT 聊天中可使用 **GPT-6 Pro**，使用 GPT-6 Sol 时还可选择 **Extra High（最高档）思考强度**。Plus 不包含后两项聊天权限。（[官方说明](https://help.openai.com/en/articles/20001354-gpt-6-and-other-models-in-chatgpt)） | 适合 Plus 的额度经常不够用，希望先增加使用额度的用户；**先通过 [Pro 专区](https://chonggrok.com/chatgpt-pro) 提供的联系方式添加客服，咨询清楚账号要求、办理方式和费用后再办理，不使用 Plus 的自动核销流程**。 |
| **ChatGPT Pro 200** | **$200 / 月** | **Work / Codex 的每周使用额度高于 Pro 100**；目前可以新开通 Pro 200 订阅。 | 适合 Pro 100 的额度仍不够用，需要每周完成更多编程、分析和研究任务的用户；**办理前同样需要先添加客服，咨询清楚账号要求、办理方式和费用后再办理，不走 Plus 自动核销**。 |
| **ChatGPT Pro 500**       | **$500 / 月** | **OpenAI 最新推出的最高用量档位**，包含 **GPT-6 Astra 和 GPT-6.1 Sol 的超高速模式（Ultrafast）** | 适合 Pro 200 的每周额度仍不够用，或需要使用 Astra、Sol 超高速模式的用户。 |

**额度怎样计算：** ChatGPT Work 和 Codex 共用一份额度：在其中一个产品使用后，另一个产品的可用额度就少了。Plus 同时有每 5 小时和每周的额度限制；Pro 100、200、500 目前没有每 5 小时的额度限制，但仍有每周额度限制。打开 ChatGPT 的“设置 → 用量”，可以看到自己还剩多少可用额度，以及系统会在什么日期、几点恢复额度。

简单任务和复杂任务消耗的额度不同，所选模型和推理强度也会影响消耗。因此，同一档会员每周能完成的任务次数并不固定。（参见 [Work / Codex 用量说明](https://learn.chatgpt.com/docs/pricing)与[各套餐额度周期](https://help.openai.com/en/articles/20001498-how-resets-work-in-codex)）

**Ultrafast 的额度消耗：** Pro 500 用户使用 GPT-6 Astra 或 GPT-6.1 Sol 时，可以选择 Ultrafast（超高速）模式。两种额度的扣除规则不同：

- **使用会员自带额度时：** 与同一模型的 Standard（标准）模式相比，Ultrafast 按 **8 倍**的标准消耗额度。
- **会员自带额度用完后：** 如果另外购买额度继续使用，Ultrafast 则按同一模型标准模式的 **6 倍**消耗这些额外购买的额度。（参见 [Pro 官方说明](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)）

### ⚠️ 关于 ChatGPT Pro 套餐档位与 Pro 200 用量规则的最新说明

根据 OpenAI 官方帮助中心[《关于 ChatGPT Pro 套餐档位》英文最新版](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)及 [2026 年 10 月 29 日更新公告](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)：

1. **Pro 200 新老用户额度已统一：** Pro 200（$200/月）目前可以新开通。10 月 29 日起，官方取消此前的降额安排；已经采用下调后 Work / Codex 额度的订阅，额度提高一倍，与保留原额度的订阅一致。现在新开通和现有 Pro 200 订阅获得相同的 Work / Codex 额度，月费仍为 $200。
2. **Pro 100 / 500 额度增加：** 自 2026 年 10 月 29 日起，这两档的 Work / Codex 套餐额度提高至此前的两倍，已订阅用户在当前订阅期内就会自动增加额度，不用等到下次续费；Plus 的额度不变。
3. **理性升级建议：** 第一次付费或尚未摸清自己真实消耗量的用户，请优先从 **$20/月的 ChatGPT Plus** 开始使用（选型细节见 [ChatGPT Plus 与 Pro 怎么选](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-vs-pro/)）；只有当你在日常使用中真实、频繁地撞上 Plus 的额度上限，且确认使用收益明显高于套餐成本时，再根据每周使用量和是否需要超高速模式，选择 **Pro 100、Pro 200 或 Pro 500**（历史档位对比见 [ChatGPT Pro 100 美元与 Pro 200 美元：5x / 20x 怎么选](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-pro-100-200/)）。

---

## 三、 下单前先检查

| 检查项                           | 正确状态与停止条件                                           |
| :------------------------------- | :----------------------------------------------------------- |
| **1. 账号登录状态**              | 已在常用浏览器正常打开并登录 `chatgpt.com`，确认当前登录的是准备升级的个人目标账号 |
| **2. 区分 Plus 与 Pro 办理方式** | • **ChatGPT Plus：** 在 `chonggrok.com/chatgpt` 下单拿卡密，再到 `chonggrok.com/verify` 自助核销<br>• **Pro 100 / Pro 200 / Pro 500：** 先通过 [Pro 专区](https://chonggrok.com/chatgpt-pro) 提供的联系方式添加客服，咨询清楚账号要求、办理方式和费用后再办理，**不使用 Plus 的自动核销流程**。 |
| **3. 了解 AuthSession 凭证边界** | Plus 自助兑换需提交**卡密和完整 `AuthSession`（官方 session JSON，含访问令牌）**，不是只需邮箱；**仅在确认域名为 `chonggrok.com` 的兑换页提交，不要发到微信/QQ 群聊或私聊，也不要公开截图** |
| **4. 现有移动端订阅核查**        | 若此前通过 Apple App Store 或 Google Play 订阅过 Plus，请先看 [苹果/谷歌内购转网页端直充指南](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-apple-google-to-web-migration/) 检查旧订阅是否已到期 |
| **5. 留存订单凭据**              | 准备好保存订单号、卡密、付款时间与页面状态截图，处理期间不要重复提交或重复购买 |

---

## 四、 国内如何通过支付宝/微信开通 ChatGPT Plus 或 Pro？

当你在 OpenAI 官方结账页遇到银行卡被拒（`card declined`）、账单地址校验不通过或 3D Secure 验证失败时（排查详见 [ChatGPT 付款被拒与支付认证失败排查](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-payment-errors/)），可通过 **[chonggrok.com](https://chonggrok.com)** 办理个人原账号升级。

**以下为 ChatGPT Plus 自助办理流程。** Pro 100 / 200 / 500 请先通过 [Pro 专区](https://chonggrok.com/chatgpt-pro) 提供的联系方式添加客服，咨询清楚套餐、账号要求、办理方式和费用后，再办理。

1. **进入服务页查看实时方案并付款：**
   打开 **[https://chonggrok.com/chatgpt](https://chonggrok.com/chatgpt)**（或主站 **[https://chonggrok.com](https://chonggrok.com)**），阅读当时展示的周期、账号要求、价格与售后规则。本文不固定写死人民币价格，实际商品、金额和办理条件以下单页实时展示为准。使用支付宝或微信完成付款后，保存好**卡密与订单号**。
2. **进入 ChongGrok 核销页验证卡密与提交 AuthSession（Plus 自助流程）：**
   打开 **[https://chonggrok.com/verify](https://chonggrok.com/verify)**（务必确认域名为 `chonggrok.com`），输入卡密验证后，按页面提示提交本次升级所需的完整 `AuthSession`（无需提供登录密码、邮箱密码或验证码）。系统识别出账号后，**仔细核对页面显示的账号信息确实属于你本人且需要升级**，再点击确认充值（完整 7 步详解见 [ChatGPT Plus 全自动充值与卡密核销流程](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-auto-recharge/)）。
3. **退出并重新登录 ChatGPT，再验收订阅状态：**
   核销页面显示完成后，**退出并重新登录 ChatGPT**，再回到 `chatgpt.com` 检查订阅状态是否已更新为 Plus，并查看 ChatGPT Work、Codex 与 GPT-6.1 模型列表。若已付款核销但页面仍显示 `Free`，请停止重复付款，按 [ChatGPT Plus 已付款但仍显示 Free](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-paid-but-still-free/) 逐项排查。

---

## 五、 风险与业务边界说明

* **自有账号会员订阅升级：** 本文介绍的 ChongGrok ChatGPT 服务为个人原账号会员订阅升级，不做 OpenAI API 余额充值、不做 ChatGPT 成品号、不做接码或批量注册。
* **凭证安全与风险提示：** ChatGPT 自助兑换无需另交账号密码或验证码，但所提交的 `AuthSession` 包含访问令牌，属于敏感登录凭证。请仅在确认域名为 `chonggrok.com` 的兑换页面提交，切勿发到微信/QQ 群聊或私聊，也不要公开截图，并在完成后重新登录 ChatGPT。任何第三方线上充值服务均存在会话泄露与账号限制风险，本文不作绝对零风险承诺。
* **独立第三方声明：** `chonggrok.com` 是独立的会员订阅充值服务网站，与 OpenAI 不存在隶属、授权或官方合作关系。

---

## 六、 常见问题解答（FAQ）

### 在 ChatGPT Work 和 Codex 里，日常应该选 GPT-6.1 Terra 还是 GPT-6.1 Sol？

根据 OpenAI 官方测试数据，**GPT-6.1 Terra** 的任务完成速度是 GPT-6.1 Sol 和 GPT-6 Astra 的 3 倍以上，且在相同套餐额度下能完成多得多的日常任务（如解读图纸、填表、写提案、常规代码修改）；而当你需要处理**最复杂、要求最高的多步骤编程与架构任务**时，OpenAI 官方建议优先切换为 **GPT-6.1 Sol** 或 **GPT-6 Astra**。

### 开通 ChatGPT Plus 或 Pro 包含 OpenAI API 余额吗？

Plus 不包含 API 余额。符合条件的 **Pro 100 / 200 / 500** 用户可领取官方 API 赠金，需满足付费订阅已生效至少 **7 天**等要求，并完成官方领取与账号关联；是否开放还取决于账号和地区。ChatGPT 与 API 仍分别计费，API 赠金也不会增加 Work / Codex 的套餐额度。`chonggrok.com` 仅提供会员订阅充值，不售卖 API 余额。（详见 [API 赠金官方说明](https://help.openai.com/en/articles/20001626-api-credits-benefit-for-eligible-chatgpt-subscriptions)）

### 为什么 Pro 100 / Pro 200 / Pro 500 不能直接用 Plus 的自助核销流程？

因为 Pro 100 / 200 / 500 的金额较高，为避免用户尚未了解清楚套餐、账号要求和办理方式就直接付款，ChongGrok 要求先添加客服、咨询清楚后再办理，因此不使用 Plus 的自助核销流程。请通过 [Pro 专区](https://chonggrok.com/chatgpt-pro) 提供的联系方式添加客服。

---

## 七、 参考资料与关联排障专题

* **ChatGPT 知识库核心专题：**
  * [ChatGPT Plus 全自动充值与卡密核销流程](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-auto-recharge/)
  * [ChatGPT Plus 与 Pro 怎么选：国内用户订阅对比](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-vs-pro/)
  * [ChatGPT Pro 100 美元与 Pro 200 美元：5x / 20x 怎么选](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-pro-100-200/)
  * [GPT-5.6 更新、可用套餐与国内体验入口](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/gpt-5-6-update/)
  * [ChatGPT Plus / Pro 免密码代充安全吗？AuthSession 凭证边界与充后刷新指南](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-session-security-verification-guide/)
  * [苹果 App Store / Google Play 内购的 ChatGPT Plus 怎么转网页端直充？](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-apple-google-to-web-migration/)
  * [2026 主流 AI 会员选型总表：ChatGPT vs Grok 国内用户该开哪一个？](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-vs-grok-2026-comparison/)
  * [ChatGPT 付款被拒与支付认证失败排查](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-payment-errors/)
  * [ChatGPT Plus 已付款但仍显示 Free](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-paid-but-still-free/)
* **ChongGrok 主站与指南门户：**
  * [ChongGrok 主站首页 (https://chonggrok.com)](https://chonggrok.com/)
  * [ChongGrok ChatGPT Plus / Pro 充值专区 (https://chonggrok.com/chatgpt)](https://chonggrok.com/chatgpt)
  * [ChongGrok 卡密与会员自助核销页 (https://chonggrok.com/verify)](https://chonggrok.com/verify)
  * [ChongGrok 知识库总门户 (https://guides.chonggrok.com)](https://guides.chonggrok.com/)
* **官方参考资料：**
  * [推出 GPT-6.1 Terra (OpenAI 官方中文公告)](https://openai.com/zh-Hans-CN/index/introducing-gpt-6-1-terra/)
  * [推出 GPT-6.1 Sol (OpenAI 官方中文公告)](https://openai.com/zh-Hans-CN/index/introducing-gpt-6-1-sol/)
  * [关于 ChatGPT Pro 套餐档位：Pro 100 / 200 / 500 说明 (OpenAI Help Center，英文最新版)](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)
  * [ChatGPT 官方更新记录](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)
  * [ChatGPT Work / Codex 套餐与用量说明](https://learn.chatgpt.com/docs/pricing)
  * [Codex 各套餐额度周期与重置说明](https://help.openai.com/en/articles/20001498-how-resets-work-in-codex)
  * [ChatGPT 当前模型与用量说明](https://help.openai.com/en/articles/20001354-gpt-6-and-other-models-in-chatgpt)
  * [ChatGPT Go 权益说明](https://help.openai.com/en/articles/11989085-what-is-chatgpt-go)
  * [符合条件的 ChatGPT 订阅用户领取 API 赠金](https://help.openai.com/en/articles/20001626-api-credits-benefit-for-eligible-chatgpt-subscriptions)

*事实与流程核验日期：2026-10-30。ChongGrok is not affiliated with OpenAI.*
*Keywords: GPT-6.1 Terra · GPT-6.1 Sol · GPT-6 Astra · ChatGPT Pro 500 · ChatGPT Pro 200 · ChatGPT Work · OpenAI Codex 额度 · ChatGPT Plus 国内充值 · chonggrok.com*
