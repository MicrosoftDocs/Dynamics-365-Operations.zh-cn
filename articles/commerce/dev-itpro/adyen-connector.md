---
title: “面向 Adyen 的 Dynamics 365 Payment Connector”概览
description: 本文概述了适用于 Adyen 的 Microsoft Dynamics 365 付款连接器。
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 6c819e8cf9f5dcb7895ac2633decf0a925c08f2d
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9784984"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>“面向 Adyen 的 Dynamics 365 Payment Connector”概览

[!include [banner](../includes/banner.md)]

本文概述了适用于 Adyen 的 Microsoft Dynamics 365 付款连接器，包括支持的特性和功能的全面列表。 相关文章包括 Adyen 注册、连接器的配置、常见问题和一些常见问题的故障排除指南。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| 付款连接器 | 推进 Microsoft Dynamics 365 Commerce（及相关组件）与付款服务之间通信的扩展。 本文中所述的连接器使用标准付款软件开发套件 (SDK) 实现。 |
| 有卡 | 指在 Dynamics 365 销售点的付款终端连接器上呈现和使用实体卡的付款交易。 |
| 无卡 | 指不呈现实体卡的付款交易，如电子商务或呼叫中心场景。 在这些场景中，付款相关信息在电子商务网站、呼叫中心流或者销售点或付款终端手动输入。 |

## <a name="supported-features-functionality-versions-and-terminals"></a>支持的特性、功能、版本和终端

现成的适用于 Adyen 的 Dynamics 365 付款连接器使用标准付款 SDK。 因此，它没有其他付款连接器也不具有的特殊功能。

### <a name="supported-versions"></a>支持的版本

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 支持的版本
Microsoft Dynamics 365 Finance 版本8.1.3（2019 年 1 月）或更高版本以及 Microsoft Dynamics 365 Retail 版本 8.1.3 或更高版支持适用于 Adyen 的第一方现成 Dynamics 365 付款连接器。 但是，第三方仍然可以为 Microsoft Dynamics 365 的早期版本开发其他适用于 Adyen 的付款连接器。

#### <a name="supported-adyen-firmware-versions"></a>支持的 Adyen 固件版本

下面的列表描述了 Microsoft Dynamics 365 Retail POS 各个版本支持的最低和最高 Adyen 固件版本。

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS 版本 10.0.25
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS 版本 10.0.26
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS 版本 10.0.27
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS 版本 10.0.28
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS 版本 10.0.29
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS 版本 10.0.30
| 最低 Adyen 固件版本 | 最高 Adyen 固件版本 |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen 可能会在 Microsoft 测试主要版本后发布次要版本更新。 只要支持主要版本，就可以在同一主要版本中获得次要版本更新。 只要之前测试过相同的主要固件版本，这些更新通常是非常有针对性的修复，不符合全面重新测试的标准。 更新不应超过文档中列出的最高 Adyen 固件版本。 
>
> 从低于版本 53 的 Adyen 固件版本迁移到版本 53 需要 POS KB **4577957** 才能获得版本 10.0.11 到 10.0.14 的 Commerce 的每月更新。 如果其中一个版本正在被使用且不包含修补程序，付款终端升级后将仅允许通过 NFC 进行付款。 对 POS 应用修补程序可解决此问题。 如果 POS 版本早于 10.0.11 版本，请提交支持请求，指出停止服务的 MPOS 需要修复 KB **4577957**。
> 
> 对于 Adyen 固件版本 59p7 到 62p9，在手动输入礼品卡的情况下，**礼品卡兑现** 操作会请求输入两次 PIN。 刷礼品卡时不会重现此问题。 Adyen 正在调查。 

### <a name="supported-payment-terminals"></a>支持的付款终端
适用于 Adyen 的 Dynamics 365 付款连接器利用与设备无关的 [Adyen 付款终端 API](https://www.adyen.com/blog/introducing-the-terminal-api)。 它支持此应用程序编程接口 (API) 支持的所有付款终端。 有关支持的付款终端的完整列表，请访问 [Adyen POS 终端](https://www.adyen.com/pos-payments/terminals)页面。

以下视频介绍了 Adyen Castles SE1 Android 付款终端的功能。


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>支持的付款方式

#### <a name="supported-debit-and-credit-cards"></a>支持的借记卡和信用卡

| 品牌 | 变型 | 有卡 | 电子商务 | 呼叫中心 |
|---|---|:-:|:-:|:-:|
| MasterCard | 贷方 | ✔ | ✔ | ✔ |
| MasterCard | 借方 | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | 贷方 | ✔ | ✔ | ✔ |
| VISA | 借方 | ✔ | ✔ | ✔ |
| VISA | 阿尔法银行奖励 | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | 贷方 | ✔ | ✔ | ✔ |
| AMEX | 借方 | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| 搜索 | 标准 | ✔ | ✔ | ✔ |
| 搜索 | Android Pay | ✔ |  |  |
| 搜索 | Apple Pay | ✔ |  |  |
| 搜索 | Samsung Pay | ✔ |  |  |
| Diners   | 标准 | ✔ | ✔ | ✔ |
| Dineromail | 标准 | ✔ | ✔ | ✔ |
| JCB | 标准 | ✔ | ✔ | ✔ |
| 银联\* | 标准 | ✔ |  |  |
| Interac Debit\* | 标准 | ✔ |  |  |

\*Adyen 不提供 Interac 和银联定期卡令牌，因此这两个支付渠道不支持无卡交易。

#### <a name="supported-gift-cards"></a>支持的礼品卡
| 计划 | 有卡 | 无卡 |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

要通过适用于 Adyen 的 Dynamics 365 付款连接器支持这些外部礼品卡计划，您必须完成其他一些步骤。 有关详细信息，请参阅[对外部礼品卡的支持](/dynamics365/unified-operations/retail/dev-itpro/gift-card)。

#### <a name="supported-wallets"></a>支持的钱包

| 计划 | 有卡 | 无卡 |
|---|---|---|
| 支付宝 | 将来的版本中将增加支持。 | 否 |
| 微信 | 将来的版本中将增加支持。 | 否 |

#### <a name="supported-card-present-input-methods"></a>支持的卡在位输入法
| 输入方法 | 受支持 | 备注 |
|---|:-:|---|
| 伸入 | ✔ | |
| 刷卡 | ✔ | |
| 点击 | ✔ | |
| 通过 POS UI 手动输入。 |  | 目前不支持 |
| 通过付款终端手动输入。 | ✔ | 支持通过 pin 输入手动输入信用卡、借记卡和礼品卡。 | 


#### <a name="supported-card-present-countries"></a>支持的卡在位国家/地区

以下国家/地区提供 Commerce 组件和来自 Adyen 的卡在位支持。 有关 Commerce 当前的全球可用性，请访问[全球可用性页面](/dynamics365/get-started/availability)。

| 国家/地区 | 受支持 |
| --- | :-: |
| 澳大利亚 | ✔ |
| 奥地利 | ✔ |
| 比利时 | ✔ |
| 加拿大 | ✔ |
| 捷克共和国 | ✔ |
| 丹麦 | ✔ |
| 爱沙尼亚 | ✔ |
| 芬兰 | ✔ |
| 法国 | ✔ |
| 德国 | ✔ |
| 香港特别行政区 | ✔ |
| 匈牙利 | ✔ |
| 冰岛 | ✔ |
| 爱尔兰 | ✔ |
| 意大利 | ✔ |
| 日本 | 将来版本 |
| 拉脱维亚 | ✔ |
| 立陶宛 | ✔ |
| 马来西亚 | ✔ |
| 荷兰 | ✔ |
| 新西兰 | ✔ |
| 挪威 | ✔ |
| 波兰 | ✔ |
| 新加坡 | ✔ |
| 瑞士 | ✔ |
| 西班牙 | ✔ |
| 瑞典 | ✔ |
| 瑞士 | ✔ |
| 英国 | ✔ |
| 美国 | ✔ |
| 巴西 | 将来版本 |

#### <a name="supported-card-not-present-countries"></a>支持的卡不在位国家/地区

Adyen 支持在以下国家/地区进行卡不在位交易。 请[联系 Adyen](https://www.adyen.com/contact/sales) 了解有关特定国家/地区的支持情况的详细信息。 有关 Commerce 当前的全球可用性，请访问[全球可用性页面](/dynamics365/get-started/availability)。

| 国家/地区 | 
| --- |
| 阿根廷 |
| 亚美尼亚 |
| 澳大利亚 |
| 奥地利 |
| 巴林 |
| 比利时 |
| 巴西 |
| 保加利亚 |
| 加拿大 |
| 智利 |
| 中国 |
| 哥伦比亚 |
| 克罗地亚 |
| 塞浦路斯 |
| 捷克共和国  |
| 丹麦 |
| 埃及 |
| 爱沙尼亚 |
| 芬兰 |
| 法国 |
| 格鲁吉亚 |
| 德国 |
| 直布罗陀 |
| 希腊 |
| 根西岛 |
| 香港特别行政区 |
| 匈牙利 |
| 冰岛 |
| 印度 |
| 印度尼西亚 |
| 爱尔兰 |
| 马恩岛 |
| 以色列 |
| 意大利 |
| 日本 |
| 泽西岛 |
| 韩国 |
| 科威特 |
| 拉脱维亚 |
| 立陶宛 |
| 卢森堡 |
| 马来西亚 |
| 马耳他 |
| 墨西哥 |
| 摩洛哥 |
| 荷兰 |
| 新西兰 |
| 挪威 |
| 秘鲁 |
| 波兰 |
| 葡萄牙 |
| 卡塔尔 |
| 罗马尼亚 |
| 沙特阿拉伯 |
| 塞尔维亚 |
| 新加坡 |
| 斯洛伐克 |
| 斯洛文尼亚 |
| 南非 |
| 西班牙 |
| 瑞典 |
| 瑞士 |
| 台湾 |
| 坦桑尼亚 |
| 泰国 |
| 土耳其 |
| 阿拉伯联合酋长国 (UAE) |
| 英国 |
| 美利坚合众国，包括波多黎各  |

#### <a name="supported-dynamics-365-payment-features"></a>支持的 Dynamics 365 付款功能

下表显示了适用于 Adyen 的 Dynamics 365 付款连接器支持的一组功能。 这些功能使用 2018 年 12 月在付款 SDK 和一些组件中引入的增强功能。 它们不是适用于 Adyen 的 Dynamics 365 付款连接器所独有的。 有关如何为不同的付款连接器采用这些增强功能的更多信息，请参阅[为付款终端创建端到端付款集成](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension)。

| 计划 | 有卡 | 无卡 |
|---|:-:|:-:|
| [兑现礼品卡余额](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [重复付款保护](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| 全渠道标志化 | ✔ | ✔ |
| 关联退款 | ✔<br>（从 10.0.1 开始） | ✔<br>（从 10.0.1 开始） |
| [保存在线付款](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>（从 10.0.2 开始） | 
| [呼叫中心和电子商务的外部礼品卡](./gift-card.md) | ✔<br>（从 10.0.10 开始） | 
| [SCA 付款重定向](../adyen_redirect.md) | | ✔<br>（从 10.0.12 开始） |
| [打印机和银箱的专用的付款终端和提示](../pos-multi-hws.md) | ✔<br>（从 10.0.12 开始） | |
| [通过 Adyen 连接器支持 SDK 级别的小费](tipping.md) | ✔<br>（从 10.0.14 开始） | |
| [用于订单开票的增量捕获](incremental-capture.md) |  | ✔<br>（从 10.0.18 开始） |
| [钱包付款](../wallets.md) |  | ✔<br>（从 10.0.20 开始） |
| [Google Pay 与 Adyen](google-pay-adyen.md) |  | ✔<br>（从 10.0.27 开始） |

## <a name="next-steps"></a>后续步骤

有关注册和配置适用于 Adyen 的 Dynamics 365 付款连接器的信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器设置](adyen-connector-setup.md)。

## <a name="additional-resources"></a>其他资源

[设置面向 Adyen 的 Dynamics 365 Payment Connector](adyen-connector-setup.md)

[“面向 Adyen 的 Dynamics 365 Payment Connector”常见问题解答](adyen-connector-faq.md)

[“面向 Adyen 的 Dynamics 365 Payment Connector”疑难解答](adyen-connector-troubleshoot.md)

[付款常见问题](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
