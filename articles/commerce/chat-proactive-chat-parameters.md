---
title: 商业聊天模块主动聊天参数
description: 本文介绍了 Microsoft Dynamics 365 Commerce 中商业聊天模块的主动聊天参数。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691047"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>商业聊天模块主动聊天参数

[!include [banner](includes/banner.md)]

本文介绍了 Microsoft Dynamics 365 Commerce 中 Customer Service 全渠道商业聊天和 Power Virtual Agents 聊天商业聊天模块的主动聊天参数。

## <a name="proactive-chat-properties"></a>主动聊天属性

主动聊天属性位于 Commerce 站点构建器中 Customer Service 全渠道商业聊天和 Power Virtual Agents 商业聊天模块的属性窗格中。

> [!NOTE]
> 默认情况下，此处列出的所有主动聊天属性都是空白的。 我们建议您详细了解这些属性，仅在需要时进行设置。 此方法有助于减少触发错误的主动聊天。

### <a name="proactive-chat"></a>主动聊天

| 友好名称 | Description | 默认值 |
|---------------|-------------|---------------|
| 已启用 | 基于不同触发器主动与客户互动。 | 已禁用 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 | 空白 |

### <a name="wait-time-proactive-chat"></a>等待时间（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 等待时间（秒） | 在触发主动聊天之前，站点用户在站点页面上花费的时间（以秒为单位）。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="number-of-page-visits-proactive-chat"></a>页面访问次数（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 页面访问次数 | 触发主动聊天之前页面的访问次数。 站点用户必须首先接受 cookie 同意横幅中的提示。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="specific-pages-proactive-chat"></a>特定页面（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 页面 | 访问时将触发主动聊天的页面的列表。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="from-specific-pages-proactive-chat"></a>从特定页面（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 页面 | 在用户离开页面时触发主动聊天的页面的列表。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="specific-countryregion-proactive-chat"></a>特定国家/地区（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 国家/地区代码 | 从指定国家或地区访问的用户将触发主动聊天。 国家/地区代码应该是两个大写字母（例如，**US**）。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="date-range-proactive-chat"></a>日期范围（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 开始日期 (dd/mm/yyyy) | 在当天或之后触发主动聊天的日期。 |
| 结束日期 (dd/mm/yyyy) | 在当天或之前触发主动聊天的日期。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="total-amount-in-cart-proactive-chat"></a>购物车总金额（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 最小值 | 当用户访问购物车页面时，将触发主动聊天的购物车内的最低货币金额（含）。 |
| 最大值 | 当用户访问购物车页面时，将触发主动聊天的购物车内的最高货币金额（含）。 |
|聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>购物车内的产品总数（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 最小值 | 当用户访问购物车页面时，将触发主动聊天的购物车内的最少产品数（含）。 |
| 最大值 | 当用户访问购物车页面时，将触发主动聊天的购物车内的最多产品数（含）。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

### <a name="specific-products-in-cart-proactive-chat"></a>购物车内的特定产品（主动聊天）

| 友好名称 | Description |
|---------------|-------------|
| 产品 ID/SKU | 当用户访问购物车页面时将触发主动聊天的产品 ID/库存单位 (SKU) 编号的列表。 |
| 聊天问候 | 触发主动聊天时使用的问候消息。 |

## <a name="additional-resources"></a>其他资源

[商业聊天功能概述](commerce-chat-overview.md)

[Customer Service 全渠道商业聊天模块](commerce-chat-module.md)

[Power Virtual Agents 商业聊天模块](chat-module-pva.md)
