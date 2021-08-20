---
title: 价格调整和折扣
description: 本文提供有关 Dynamics 365 Commerce 中价格调整和折扣的信息。
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748490"
---
# <a name="price-adjustments-and-discounts"></a>价格调整和折扣

[!include [banner](includes/banner.md)]

本文提供有关 Dynamics 365 Commerce 中价格调整和折扣的信息。

在 Commerce 中，您可以对产品进行价格调整，并可以设置应用于销售点 (POS) 上、呼叫中心销售订单中或在线订单中的一个行项或交易记录的折扣。 价格调整和折扣都可以链接到价格组。 对于价格调整和折扣，您可以指定单一开始日期和结束日期或重复期间、折扣代码和若干其他属性。 

价格调整和折扣可以应用于产品、变型或类别。 如果对某一产品应用多个折扣，客户可能根据折扣的配置接收折扣或组合折扣的一个折扣。 Commerce 将自动应用提供最佳价格给客户的折扣或折扣组合。 在设置价格调整或折扣时，请确保确认价格组分配给您希望折扣应用于的正确渠道、类别、隶属关系或会员计划。 而且，如果您想要自动生成折扣 ID，可以在定义新的价格调整或折扣前在 **商业参数** 页中设置编号序列。

> [!NOTE]
> 您可以删除价格调整或折扣。 但是，统计信息会丢失。

## <a name="types-of-discounts"></a>折扣类型

折扣类型有很多种：

- **简单折扣** –一个单一百分比或金额。
- **数量折扣** – 在两个或多个产品购置时应用的折扣。
- **组合购买折扣** – 在购买特定产品组合时应用的折扣。
- **阈值折扣** – 交易记录合计大于指定金额时应用的折扣。
- **基于支付方式的折扣** – 当交易总计大于指定金额并且使用特定付款类型（例如，现金、信用卡或借记卡）付款时将应用的折扣。
- **装运折扣** – 交易总计大于指定金额且订单上使用特定交货方式（例如，两天装运或隔夜装运）时应用的折扣。

价格调整和折扣都可以关联到价格组。 价格组可与渠道、类别、隶属关系和会员计划关联。

> [!NOTE]
> 组合购买折扣和阈值折扣分别具有名为“计入非折扣产品”和“针对阈值计入非折扣产品”的属性。 如果启用这些属性，不符合任何折扣条件的物料仍然可以帮助使交易符合折扣条件，但不符合条件的物料将无法获得折扣。 
> 
> 例如，如果创建具有两行 A 和 B 的组合购买折扣，其中客户应该在这两个物料上获得 10% 的折扣，但物料 A 已选中“阻止所有折扣”配置，这通常会停止将物料 A 包括在折扣中。 但是，如果启用了“计入非折扣产品”属性，则物料 A 可用于获得组合购买折扣的资格，但 10% 的折扣将仅适用于物料 B。类似逻辑也适用于阈值折扣。 
>
> 但是，与组合购买折扣的“计入非折扣产品”属性相比，“针对阈值计入非折扣产品”属性具有其他功能。 如果启用了阈值折扣，并且如果某个物料具有的现有折扣将阻止物料获得任何其他折扣，则为该物料支付的价格将满足阈值条件，但此物料将不会获得额外的折扣。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
