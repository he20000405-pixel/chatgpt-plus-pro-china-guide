---
title: "ChatGPT Plus 已付款但仍显示 Free：账号、订阅入口、App Store / Google Play 与卡密核销排查"
description: "排查 ChatGPT Plus 已扣款仍显示 Free、App Store 订阅未同步、Google Play 原购买账号不一致、订阅关联其他 OpenAI 账号和 ChongGrok 卡密核销状态。"
permalink: /guides/chatgpt-paid-but-still-free/
date_published: "2026-07-12"
last_modified_at: "2026-07-12"
breadcrumbs:
  - name: 首页
    url: /
  - name: 专题
    url: /guides/
  - name: 已付款仍显示 Free
    url: /guides/chatgpt-paid-but-still-free/
faq:
  - question: "ChatGPT Plus 已经扣款但仍显示 Free，第一步该做什么？"
    answer: "先不要重复付款。确认购买发生在 chatgpt.com、Apple App Store、Google Play 还是 ChongGrok，再核对当前登录账号是否就是原购买时绑定的 OpenAI 账号。"
  - question: "收到付款收据是否代表 ChatGPT Plus 已经在当前账号生效？"
    answer: "不一定。收据能证明某个渠道产生了交易，但还要在网页 Billing、Apple 订阅或 Google Play 订阅中确认状态，并核对订阅绑定的原 ChatGPT 账号。"
  - question: "iPhone 上怎样恢复 ChatGPT Plus 购买？"
    answer: "使用原购买时的 Apple ID 和 ChatGPT 账号登录，在 ChatGPT iOS App 中进入 Settings、Account，然后选择 Restore purchases。"
  - question: "Android 版 ChatGPT 应该使用 Restore purchases 吗？"
    answer: "OpenAI 给出的 Restore purchases 路径针对 iOS。Android 应检查 Google Play 中原购买账号的订阅状态，并使用订阅最初绑定的 ChatGPT 账号登录。"
  - question: "提示订阅关联另一个 OpenAI 账号是什么意思？"
    answer: "移动端订阅会同时关联购买时的 Apple ID 或 Google Play 账号，以及当时登录的 ChatGPT 账号。订阅不能转移到另一个 ChatGPT 账号，应登录原购买账号使用。"
  - question: "ChongGrok 卡密核销后仍显示 Free 怎么办？"
    answer: "不要再次购买。保留卡密、订单和核销状态，通过 chonggrok.com/verify 核对目标账号及处理记录；确认账号无误后再按页面或售后指引处理。"
---

# ChatGPT Plus 已付款但仍显示 Free

**先说结论：不要因为页面没有立即显示 Plus 就再次付款。** 先确认购买入口，再确认当前登录的是否为原购买时绑定的 OpenAI 账号。网页、Apple App Store、Google Play 和 ChongGrok 卡密核销是四条不同路径，处理方法不能混用。

> 本文讨论 ChatGPT 会员订阅，不涉及 API 额度。ChongGrok 是独立的会员订阅充值服务网站，与 OpenAI 不存在隶属、授权或官方合作关系。

## 一分钟诊断顺序

1. 查清购买入口：`chatgpt.com`、Apple App Store、Google Play，还是 ChongGrok；
2. 查清交易状态：待处理、已入账、有收据，还是渠道内显示有效订阅；
3. 核对当前 ChatGPT 账号是否为购买时使用的原账号；
4. 只执行对应渠道的恢复、核销或售后流程；
5. 在状态查清之前，不要跨平台再次订阅。

## 先区分四种“付款成功”

| 你看到的证据 | 能说明什么 | 还不能说明什么 |
| --- | --- | --- |
| 银行卡显示待处理或预授权 | 支付请求已进入银行流程 | 不能证明交易最终入账或订阅已生效 |
| 银行卡最终扣款 | 该笔交易已记账 | 不能单独证明当前登录账号获得了 Plus |
| Apple、Google Play 或 OpenAI 收据 | 对应渠道生成了订单 | 仍需核对订阅状态和绑定账号 |
| 渠道内显示有效订阅 | 购买渠道认可订阅有效 | 仍需确认 ChatGPT 登录的是原购买账号 |

不要只根据短信通知或银行卡余额判断会员状态。真正需要核对的是：**购买渠道、有效订阅和账号绑定是否一致。**

## 路径一：在 chatgpt.com 网页购买

如果通过 ChatGPT 网页结账：

1. 使用购买时的同一 OpenAI 账号登录 `chatgpt.com`；
2. 打开 `Settings → Billing`，检查订阅和账单信息；
3. 核对登录方式是否一致，例如 Google、Apple、Microsoft 或邮箱登录；
4. 在其他设备使用时，也必须登录同一个 OpenAI 账号；
5. Billing 没有有效订阅但存在最终扣款时，保留收据并联系 OpenAI 支持。

OpenAI 将 ChatGPT 网页订阅的 Billing 与 API Platform 账单分开管理。本文只检查 ChatGPT 会员，不使用 API 账单页面判断 Plus 状态。

<!-- SCREENSHOT PLACEHOLDER
建议文件：../assets/images/chatgpt-web-billing.webp
内容：ChatGPT Settings 中的 Billing 入口，不显示个人订单号或付款信息
alt：ChatGPT 网页端 Billing 订阅检查入口
-->

## 路径二：通过 Apple App Store 购买

先在 iPhone 的 Apple 订阅中确认 ChatGPT 订阅是否有效，再核对 ChatGPT App 中登录的账号。

OpenAI 官方提供的 iOS 恢复路径是：

`ChatGPT App → Settings → Account → Restore purchases`

执行前应同时满足：

- iPhone 使用原购买时的 Apple ID；
- ChatGPT App 登录原购买时绑定的 OpenAI 账号；
- Apple 订阅页面仍显示该订阅有效。

如果购买时使用了“通过 Apple 登录”或 Apple 隐藏邮箱，不要改用另一个邮箱新建账号。应继续使用原 Apple 登录方式，必要时检查该账号对应的 Apple 私有转发邮箱。

<!-- SCREENSHOT PLACEHOLDER
建议文件：../assets/images/chatgpt-ios-restore-purchases.webp
内容：ChatGPT iOS Settings → Account → Restore purchases，不显示 Apple ID
alt：ChatGPT iOS 恢复 App Store 购买入口
-->

## 路径三：通过 Google Play 购买

Android 不应照搬 iOS 的 `Restore purchases` 操作。应按以下顺序检查：

1. 打开 Google Play，切换到原购买时使用的 Google 账号；
2. 在订阅管理中确认 ChatGPT 订阅是否有效；
3. 打开 ChatGPT Android App，确认登录的是购买时绑定的原 OpenAI 账号；
4. 更新 App 后重新登录原账号；
5. Google Play 显示有效但 ChatGPT 仍为 Free 时，准备订单收据并联系 OpenAI 支持。

切换 Google Play 账号或重新安装 App，不会把订阅转移到另一个 ChatGPT 账号。

## “订阅关联另一个 OpenAI 账号”是什么意思？

OpenAI 说明，移动端订阅会同时关联：

- 购买时使用的 Apple ID 或 Google Play 账号；
- 购买当时登录的 ChatGPT 账号。

移动订阅不能转移到另一个 ChatGPT 账号。删除 App、重新安装或改用新账号，也不会改变原绑定关系。出现关联提示时，应停止再次购买，退出当前账号并用原购买账号登录。

如果不记得原账号，可从以下线索核对：

- 原购买设备上的 ChatGPT 登录方式；
- Apple 隐藏邮箱地址；
- Google、Apple 或 Microsoft 登录入口；
- OpenAI、Apple 或 Google Play 收据发送到的邮箱；
- 其他仍保持登录的设备。

## 多平台订阅为什么可能重复扣款？

ChatGPT 可以分别通过网页、iOS 和 Android 建立订阅。若一个渠道的订阅尚未取消，又在另一渠道重新购买，可能同时存在两笔订阅并分别扣款。

再次付款前，逐项检查：

| 渠道 | 检查位置 | 取消或退款由谁处理 |
| --- | --- | --- |
| chatgpt.com 网页 | ChatGPT `Settings → Billing` | OpenAI 支持 |
| Apple App Store | Apple ID 的订阅管理 | Apple |
| Google Play | Google Play 的订阅管理 | Google Play / OpenAI 官方退款流程 |

如果已经出现重复订阅，应先确认每笔订单的渠道和账号，再按原购买渠道申请取消或退款，不要用第三笔订单“覆盖”问题。

如果问题发生在原有 Plus / Pro 的续费环节，且续费尚未成功扣款，请转到[续费失败后变回 Free 专题](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-renewal-failed-back-to-free/)，先处理原平台的续费状态，不要跨平台重新订阅。

## 不同设备仍显示 Free 怎么办？

同一 ChatGPT 订阅可以在其他设备使用，关键是登录**同一个 OpenAI 账号**。手机和电脑看起来使用了同一邮箱，并不一定代表登录入口相同；尤其要核对 Google、Apple、Microsoft 与邮箱密码登录。

可依次尝试：

1. 记录当前账号和订阅证据；
2. 退出 ChatGPT；
3. 更新 App 或清理网页缓存；
4. 用原购买时的登录方式重新登录；
5. iOS 订单再执行一次官方 `Restore purchases`；
6. 仍不一致时联系对应渠道支持。

## ChongGrok 卡密或订单路径

如果订单来自 chonggrok.com，不要转去 Apple、Google Play 或 OpenAI 的恢复购买流程，也不要重新下单。

1. 打开 [ChongGrok 卡密核销页面](https://chonggrok.com/verify)；
2. 核对卡密是否完整、是否已经核销以及当前处理状态；
3. 核对核销时确认的目标 ChatGPT 账号是否为自己的原账号；
4. 保留卡密、订单页面、付款记录和核销结果；
5. 账号或处理状态不一致时，按主站页面提供的售后入口核对记录。

Plus 核销流程不需要 ChatGPT 密码，但会按核销页提示使用本次升级所需的 session。session 仍是敏感凭证，只应在卡密验证后的受控页面提交；处理完成后建议退出并重新登录以刷新原 session。

<!-- SCREENSHOT PLACEHOLDER
建议文件：../assets/images/chatgpt-verify-status.webp
内容：chonggrok.com/verify 的卡密状态入口，不使用真实卡密、session 或订单
alt：ChongGrok ChatGPT 卡密核销状态检查入口
-->

## 需要准备哪些证据？

联系客服前准备以下信息，可以减少来回确认：

- 购买入口和购买日期；
- 订单号或收据，但不要公开完整银行卡信息；
- 银行交易是待处理还是最终入账；
- Apple、Google Play 或网页 Billing 的订阅状态；
- 当前 ChatGPT 登录方式；
- 页面显示 Free、Plus 或关联其他账号的实际提示；
- ChongGrok 订单则补充卡密状态和核销记录。

不要在公开评论区提交密码、验证码、恢复码、完整银行卡号、session 或完整卡密。

## 应该联系谁？

| 问题发生位置 | 优先联系对象 |
| --- | --- |
| chatgpt.com 网页订阅、账号绑定或网页扣款 | OpenAI 支持 |
| Apple App Store 订阅、取消或退款 | Apple 支持 |
| Google Play 订阅状态 | Google Play；退款按 OpenAI 官方说明进入对应流程 |
| ChongGrok 卡密、核销或目标账号记录 | ChongGrok 售后 |
| 银行卡待处理、拒付或不明交易 | 发卡银行 |

OpenAI 网页和 Google Play 订单的退款入口与 Apple 订单不同。Apple 订阅退款需要直接向 Apple 申请；其他符合条件的 ChatGPT 订阅退款按 OpenAI 帮助中心流程处理。

## 确认原订单没有成功后，是否需要重新购买？

只有在以下三点都确认后，才应考虑重新购买：

1. 原交易没有形成有效订阅；
2. 当前账号在网页、Apple 和 Google Play 均没有有效订阅；
3. 没有待处理退款、重复订阅或尚未完成的 ChongGrok 核销订单。

此时如果没有合适的海外付款方式，可以查看 [chonggrok.com ChatGPT 实时方案](https://chonggrok.com/chatgpt)。这只是重新购买前的可选入口，不用于处理已经扣款或仍在核销中的订单。

## 常见问题

### ChatGPT Plus 已经扣款但仍显示 Free，第一步该做什么？

先不要重复付款。确认购买发生在 chatgpt.com、Apple App Store、Google Play 还是 ChongGrok，再核对当前登录账号是否就是原购买时绑定的 OpenAI 账号。

### 收到付款收据是否代表 ChatGPT Plus 已经在当前账号生效？

不一定。收据能证明某个渠道产生了交易，但还要在网页 Billing、Apple 订阅或 Google Play 订阅中确认状态，并核对订阅绑定的原 ChatGPT 账号。

### iPhone 上怎样恢复 ChatGPT Plus 购买？

使用原购买时的 Apple ID 和 ChatGPT 账号登录，在 ChatGPT iOS App 中进入 `Settings → Account → Restore purchases`。

### Android 版 ChatGPT 应该使用 Restore purchases 吗？

OpenAI 给出的 `Restore purchases` 路径针对 iOS。Android 应检查 Google Play 中原购买账号的订阅状态，并使用订阅最初绑定的 ChatGPT 账号登录。

### 提示订阅关联另一个 OpenAI 账号怎么办？

停止再次购买，退出当前账号并登录原购买时绑定的 ChatGPT 账号。移动订阅不能转移到另一个 ChatGPT 账号，重新安装 App 也不会改变绑定。

### ChongGrok 卡密核销后仍显示 Free 怎么办？

不要再次购买。通过 [卡密核销页面](https://chonggrok.com/verify)核对卡密、目标账号和处理状态，并保留订单及核销记录供售后查询。

## OpenAI 官方来源

- [Why am I seeing a message that my subscription is associated with another account?](https://help.openai.com/en/articles/20001056)
- [How do I restore my ChatGPT subscription?](https://help.openai.com/en/articles/8346573)
- [How do I avoid being charged twice if I subscribe to ChatGPT on iOS, Android, and the web?](https://help.openai.com/en/articles/20001043-how-do-i-avoid-being-charged-twice-if-i-subscribe-to-chatgpt-on-ios-android-and-the-web)
- [Billing settings in ChatGPT vs Platform](https://help.openai.com/en/articles/9039756-billing-settings-in-chatgpt-vs-platform)
- [How do I request a refund for ChatGPT Plus?](https://help.openai.com/en/articles/7232895-how-do-i-request-a-refund-for-chatgpt-plus)
- [Can I access my ChatGPT subscription from another device?](https://help.openai.com/en/articles/8980438-can-i-access-my-chatgpt-subscription-from-another-device)

[返回全部专题](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/) · [查看付款被拒排查](https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-payment-errors/)
