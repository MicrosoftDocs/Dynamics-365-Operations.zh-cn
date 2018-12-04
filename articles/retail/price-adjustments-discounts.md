---
title: "价格调整和折扣"
description: "本文提供有关 Microsoft Dynamics 365 for Retail 中价格调整和折扣的信息。"
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9220cc12abf7134d425e088939d20ea03239a75a
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="price-adjustments-and-discounts"></a>价格调整和折扣

[!include [banner](includes/banner.md)]

本文提供有关 Microsoft Dynamics 365 for Retail 中价格调整和折扣的信息。

在 Dynamics 365 for Retail 中，您可以对产品进行价格调整，并且还可以设置应用于销售点 (POS)、呼叫中心销售订单或者联机订单的行项或交易记录的折扣。 价格调整和折扣都可以链接到价格组。 对于价格调整和折扣，您可以指定单一开始日期和结束日期或重复期间、折扣代码和若干其他属性。 价格调整和折扣可以应用于产品、变型或类别。 如果对某一产品应用多个折扣，客户可能根据折扣的配置接收折扣或组合折扣的一个折扣。 Dynamics 365 for Retail 将自动应用提供最佳价格给客户的折扣或折扣组合。 在设置价格调整或折扣时，请确保确认价格组分配给您希望折扣应用于的正确渠道、类别、隶属关系或会员计划。 而且，如果您想要自动生成折扣 ID，可以在定义新的价格调整或折扣前在**零售参数**页中设置编号序列。 **注意：**您可以删除价格调整或折扣。 但是，统计信息会丢失。

### <a name="types-of-discounts"></a>折扣类型

存在四种零售折扣：

-   **简单折扣** –一个单一百分比或金额。
-   **数量折扣** – 在两个或多个产品购置时应用的折扣。
-   **组合购买折扣** – 在购买特定产品组合时应用的折扣。
-   **阈值折扣** – 交易记录合计大于指定金额时应用的折扣。

价格调整和折扣都可以关联到价格组。 价格组可与渠道、类别、隶属关系和会员计划关联。




