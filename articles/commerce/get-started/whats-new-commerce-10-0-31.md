---
title: Dynamics 365 Commerce 10.0.31 预览（2023 年 2 月）
description: 本文介绍 Microsoft Dynamics 365 Commerce 10.0.31 中的新增功能或更改的功能。
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709852"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commerce 10.0.31 预览（2023 年 2 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Commerce 预览版 10.0.31 中的新增或更改的功能。 此版本的构建版本号为 10.0.1406，并按以下时间表提供：

- **预览版：** 2022 年 10 月
- **版本的正式发布时间（自行更新）：** 2023 年 1 月
- **版本的正式发布时间（自动更新）：** 2023 年 2 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 错误代码 | Commerce 引入了标准化的错误参考，以包含在呈现给在线购物者的在线渠道结帐错误中。| [结帐模块错误代码](../checkout-module-error-codes.md)  | 默认打开 |
| 付款 | [使用适用于 Adyen 的 Dynamics 365 付款连接器支持 Apple Pay](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | 使用支持的设备或浏览器时，电子商务客户可以在购物车和结帐页面使用 Apple Pay。 | 开发人员选择加入 |
| 付款  |  Commerce 增加了限制用户在整个 Commerce headquarters 用户界面如何与定期付款令牌交互的功能。 付款窗体（如 **呼叫中心销售订单** 页面）不再显示客户以前使用的定期付款令牌来用于新交易。 在处理新交易的付款时，只有在 Commerce **客户付款** 屏幕输入或在通过销售订单付款时与客户协定的确定的“存档卡”会显示给呼叫中心或 Commerce headquarters 用户。 | [限制付款令牌的使用](../dev-itpro/limit-token-usage.md)  |  功能管理<p>*将付款令牌限制为仅用于订单上下文*  |
| POS | [从 POS 创建采购订单](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  改进了销售点 (POS) 应用中的入站库存操作，允许用户创建、编辑和确认采购订单请求。 |  功能管理<p>*在 POS 中创建采购订单请求的功能*   |



## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Commerce 10.0.31 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.31 的平台更新（2023 年 2 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md)。 
  

### <a name="bug-fixes"></a>缺陷修复

有关版本 10.0.31 中各更新内的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525)。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 和行业云：2022 版本第 2 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2022 版本第 2 波计划](/dynamics365-release-plan/2022wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-commerce-features"></a>删除和弃用的 Commerce 功能

[Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文介绍了针对 Commerce 删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文中发布弃用通知。


对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
