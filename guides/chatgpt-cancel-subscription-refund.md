---
title: "ChatGPT 取消订阅与退款：网页、Apple、Google Play"
description: "按 ChatGPT 原购买渠道取消 Plus / Pro 自动续费，并分别通过 OpenAI、Apple 或 Google Play 对应入口申请退款。"
permalink: /guides/chatgpt-cancel-subscription-refund/
schema_type: Article
date_published: 2026-08-14
last_modified_at: 2026-08-14
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "取消订阅与退款"
    url: /guides/chatgpt-cancel-subscription-refund/
faq:
  - question: "ChatGPT 取消订阅后会自动退款吗？"
    answer: "不会。取消订阅用于停止未来自动续费，申请退款是另一项操作。已经支付的订单必须按原购买渠道单独提交退款申请，是否符合退款条件由实际收款平台判断。"
  - question: "删除 ChatGPT App 能取消订阅吗？"
    answer: "不能。通过 Apple 或 Google Play 购买的订阅必须在对应商店的订阅管理中取消；通过 chatgpt.com 购买的订阅必须在 ChatGPT 网页 Billing 中取消。"
  - question: "怎样确认 ChatGPT 是从哪里购买的？"
    answer: "先查付款收据的发送方，再分别检查 Apple 订阅、Google Play 订阅和 ChatGPT 网页 Billing。收据与订阅页面能够确定由谁收款和管理续费。"
  - question: "ChatGPT 已经扣款但仍显示 Free，应该先取消吗？"
    answer: "不要先重复购买。先核对收据、原购买账号和订阅状态；如果属于已付款但权益未生效，应进入对应排障流程。取消订阅不能修复账号权益，也不会自动退款。"
  - question: "无法登录原 ChatGPT 账号，还能取消网页订阅吗？"
    answer: "可以联系 OpenAI 支持协助查找并取消，但需要提供订阅账号邮箱、付款卡末四位和最近一次付款日期等核验资料。不要公开完整卡号、验证码或密码。"
  - question: "ChongGrok 订单应该在哪里查询？"
    answer: "已有卡密或订单时，先在 chonggrok.com/verify 查看核销与处理状态，再通过主站售后核对订单。不要把 ChongGrok 订单提交到 Apple、Google Play 或 OpenAI 的退款入口。"
---

# ChatGPT Plus / Pro 怎么取消订阅和申请退款？按原购买渠道操作

**先确认 ChatGPT 是从网页、Apple App Store 还是 Google Play 购买的，再回到同一渠道取消。**取消订阅只会停止下一次自动续费；如果希望退回已经支付的款项，还要向实际收款平台单独申请退款。

不要只卸载 App，也不要在取消结果尚未确认时换到另一个平台重新订阅。这样容易留下两份有效订阅，并产生重复扣款。

> 本文适用于 ChatGPT Plus / Pro 个人订阅，不涉及 API 账单。ChongGrok 与 OpenAI、Apple 和 Google 没有隶属关系。

## 先分清：取消订阅和申请退款不是一回事

| 你的目的 | 操作结果 | 应该在哪里处理 |
| --- | --- | --- |
| 不想在下一个计费周期继续扣款 | 停止未来自动续费，当前权益通常保留到页面显示的到期日 | 原购买渠道的订阅管理 |
| 希望退回已经支付的订单 | 提交退款申请，是否符合条件由收款平台审核 | 原订单的收款平台 |
| 已扣款但账号仍显示 Free | 核对订单、购买账号和权益归属 | [已付款仍显示 Free 排查]({{ '/guides/chatgpt-paid-but-still-free/' | relative_url }}) |
| 同时发现两份有效订阅 | 保留一份，取消另一份未来续费，再按原渠道申请退款 | [重复扣款排查]({{ '/guides/chatgpt-charged-twice/' | relative_url }}) |
| 续费失败后变回 Free | 回原购买渠道检查续费状态和付款方式 | [续费失败排查]({{ '/guides/chatgpt-renewal-failed-back-to-free/' | relative_url }}) |

如果你的问题属于后三种情况，先进入对应专题，不要直接照着本页重复购买或删除账号。

## 开始前准备四项资料

操作前先保存以下信息。它们用于确认购买渠道，也用于后续联系支持：

1. **付款收据。**记录发送方、订单日期、金额和订单号；
2. **原购买账号。**记录购买时使用的 OpenAI、Apple 或 Google 账号；
3. **订阅页面。**记录当前计划、订阅状态和下次续费或到期日期；
4. **交易状态。**确认银行或商店显示的是待处理，还是已经完成的最终扣款。

截图时遮住完整银行卡号、验证码、密码、恢复码和其他无关个人信息。

## 第一步：识别原购买渠道

先查看付款收据，再用下面的入口交叉核对：

| 收据或订阅出现在哪里 | 原购买渠道 | 订阅管理入口 |
| --- | --- | --- |
| OpenAI 或 ChatGPT 网页收据 | `chatgpt.com` 网页 | ChatGPT `Settings → Billing` |
| Apple 收据，iPhone 订阅中有 ChatGPT | Apple App Store | iPhone `设置 → Apple 账户 → 订阅` |
| Google Play 收据，Play 订阅中有 ChatGPT | Google Play | Play 商店 `头像 → 付款和订阅 → 订阅` |
| ChongGrok 卡密或订单记录 | ChongGrok | [卡密核销与状态查询](https://chonggrok.com/verify) |

如果收据和订阅页面对不上，先检查是否登录了购买时使用的另一个 Apple、Google 或 OpenAI 账号。不要凭银行卡短信猜测购买渠道。

## 第二步：在原购买渠道取消自动续费

### A. 在 chatgpt.com 网页购买

1. 打开 [ChatGPT](https://chatgpt.com/)；
2. 使用购买订阅的原 OpenAI 账号登录；
3. 点击个人资料图标，进入 `Settings`；
4. 打开 `Billing`；
5. 在 `Cancel plan` 下选择 `Cancel`；
6. 完成确认，并保存页面显示的到期日期。

**预期结果：**页面应显示订阅已取消或不会继续续费，并给出当前权益结束日期。OpenAI 建议至少在下一个计费日前 24 小时取消。

**停止条件：**如果 Billing 中没有这份订阅，不要建立新订阅。先检查其他 OpenAI 账号、Apple 和 Google Play，确认原购买渠道。

### B. 通过 Apple App Store 购买

1. 在 iPhone 打开“设置”；
2. 点击顶部的 Apple 账户姓名；
3. 点击“订阅”；
4. 选择 `ChatGPT`；
5. 点击“取消订阅”；
6. 确认取消，并保存页面显示的到期日期。

**预期结果：**如果页面不再显示取消按钮，或显示明确的到期信息，Apple 说明这份订阅通常已经取消。取消后，当前权益一般保留到已支付周期结束。

**找不到 ChatGPT：**搜索邮箱中的 Apple 收据，确认付款使用的是哪个 Apple 账户，再用该账户检查。删除 ChatGPT App 不会取消 Apple 订阅。

### C. 通过 Google Play 购买

1. 打开 Google Play；
2. 点击右上角头像；
3. 切换到收据对应的原 Google 账号；
4. 进入“付款和订阅”；
5. 点击“订阅”，选择 `ChatGPT`；
6. 点击“取消订阅”，按页面提示完成确认；
7. 保存取消状态和到期日期。

**预期结果：**Google Play 应显示订阅已取消或将在某个日期到期。卸载 Android App 不会停止续费。

**找不到 ChatGPT：**先检查其他 Google 账号。若有 Google Play 收据但仍找不到订阅，再使用与购买关联的 ChatGPT 账号联系 OpenAI 支持。

## 第三步：按实际收款平台申请退款

取消成功不代表已经提交退款。先确认订单已完成并有正式收据，再选择对应入口。

### chatgpt.com 网页订单

1. 登录被扣款的 ChatGPT 账号；
2. 打开 [OpenAI Help Center](https://help.openai.com/)；
3. 确认帮助中心也登录了同一 OpenAI 账号；
4. 打开右下角聊天窗口；
5. 说明需要申请 ChatGPT 订阅退款；
6. 提交订单日期、金额和脱敏收据。

如果聊天窗口提示需要登录，或找不到订阅，先退出帮助中心并用被扣款的账号重新登录。退款是否符合条件以及最终结果，以 OpenAI 的审核为准。

### Apple App Store 订单

1. 打开 [reportaproblem.apple.com](https://reportaproblem.apple.com/)；
2. 使用收据对应的 Apple 账户登录；
3. 选择“Request a refund”；
4. 选择退款原因；
5. 选择对应的 ChatGPT 订单并提交。

如果订单仍处于待处理状态，Apple 说明暂时不能申请退款。收到正式收据后再重新检查。退款是否获批由 Apple 判断。

### Google Play 订单

OpenAI 当前专门的 ChatGPT 退款说明要求 Google Play 订阅用户使用与扣款关联的 OpenAI 账号，通过 OpenAI Help Center 的聊天窗口提交退款请求。操作步骤与网页订单相同：

1. 登录购买时绑定的 ChatGPT 账号；
2. 打开 OpenAI Help Center；
3. 确认帮助中心登录的是同一账号；
4. 通过聊天窗口提交 Google Play 订单日期、金额和脱敏收据。

平台规则可能变化，提交当天应再次查看[OpenAI 官方退款说明](https://help.openai.com/en/articles/7232895-how-do-i-request-a-refund-for-chatgpt-plus)。

## 无法登录原账号怎么办？

如果网页订阅所在的 OpenAI 账号已经无法访问，不要删除账号，也不要创建新订阅来代替它。

OpenAI 官方取消说明要求联系支持，并准备：

- 订阅账号的邮箱地址；
- 付款卡末四位；
- 最近一次订阅付款日期。

这些信息用于查找订单。不要提交完整卡号、密码、验证码或恢复码。删除 OpenAI 账号是不可逆操作，不应作为普通取消订阅的第一选择。

## ChongGrok 订单应该怎样处理？

如果你持有 ChongGrok 卡密或订单，不要把该订单提交到 Apple、Google Play 或 OpenAI 的退款入口。

1. 打开 [ChongGrok 卡密核销页面](https://chonggrok.com/verify)；
2. 检查卡密是否已核销以及当前处理状态；
3. 保存订单号、付款记录和目标账号的脱敏信息；
4. 通过主站售后入口核对订单和后续处理方式；
5. 同时以 ChatGPT 官方 `Billing` 页面为准，确认账号是否存在自动续费。

ChongGrok 只能核对自己的订单，不能替 Apple、Google Play 或 OpenAI 取消其平台上的订阅。如果官方平台已经有有效订阅或待处理扣款，不要再次下单。

## 完成后的验收清单

处理完成后，逐项确认：

- 已经找到原购买渠道；
- 原渠道显示取消成功或明确到期日期；
- 没有在另一个平台建立第二份订阅；
- 退款申请已提交给实际收款平台；
- 收据、取消确认和支持工单已经保存；
- 当前仍在有效期内的会员状态与页面说明一致；
- 没有尚未查明的待处理交易。

如果已经取消，但账号立即变成 Free，或者出现已扣款却没有权益，请停止继续操作，进入[已付款仍显示 Free 排查]({{ '/guides/chatgpt-paid-but-still-free/' | relative_url }})。

## 常见问题

### ChatGPT 取消订阅后会自动退款吗？

不会。取消订阅用于停止未来自动续费，退款需要按原订单的收款平台另行申请。

### 删除 ChatGPT App 能取消订阅吗？

不能。Apple、Google Play 和网页订阅都必须在各自的订阅管理入口取消。

### 怎样确认 ChatGPT 是从哪里购买的？

先查看收据发送方，再检查 Apple 订阅、Google Play 订阅和 ChatGPT 网页 `Billing`。三处结果能够确定由谁收款和管理续费。

### ChatGPT 已经扣款但仍显示 Free，应该先取消吗？

先核对订单、原购买账号和权益归属，不要再次购买。取消订阅不能修复权益同步，也不会自动退回已付款项。

### 无法登录原 ChatGPT 账号，还能取消网页订阅吗？

可以联系 OpenAI 支持协助查找并取消。准备订阅邮箱、付款卡末四位和最近一次付款日期，不要公开完整卡号或密码。

### 已有 ChongGrok 卡密，应该去哪里处理？

先在 [chonggrok.com/verify](https://chonggrok.com/verify) 检查核销与订单状态，再通过主站售后核对。不要再次购买。

## 官方来源

- [OpenAI：取消 ChatGPT 订阅](https://help.openai.com/en/articles/7232927-how-do-i-cancel-my-chatgpt-subscription)
- [OpenAI：申请 ChatGPT 订阅退款](https://help.openai.com/en/articles/7232895-how-do-i-request-a-refund-for-chatgpt-plus)
- [OpenAI：避免在网页、iOS 和 Android 重复订阅](https://help.openai.com/en/articles/20001043-how-do-i-avoid-being-charged-twice-if-i-subscribe-to-chatgpt-on-ios-android-and-the-web)
- [OpenAI：取消 ChatGPT Android 订阅](https://help.openai.com/en/articles/8258076-how-to-cancel-a-subscription-in-the-chatgpt-android-app)
- [OpenAI：取消 ChatGPT Apple 订阅](https://help.openai.com/en/articles/7905690-how-to-cancel-your-apple-subscription-for-chatgp-in-the-chatgpt-ios-app)
- [Apple：取消订阅](https://support.apple.com/en-us/118428)
- [Apple：申请退款](https://support.apple.com/en-us/118223)
- [Google Play：取消、暂停或更改订阅](https://support.google.com/googleplay/answer/7018481)

**核验日期：2026 年 8 月 14 日。**入口和退款规则可能调整，请以操作当天的官方页面为准。

## 风险与业务边界

- ChongGrok 与 OpenAI、Apple 和 Google 没有隶属关系；
- 取消订阅不等于退款，退款是否获批由实际收款平台判断；
- 不承诺退款结果或固定处理时间；
- 不提供 API 额度、成品号、接码或批量注册；
- 不需要公开密码、验证码、恢复码、完整银行卡号或 session；
- 已有有效订阅、最终扣款或待处理交易时，不应再次购买。
