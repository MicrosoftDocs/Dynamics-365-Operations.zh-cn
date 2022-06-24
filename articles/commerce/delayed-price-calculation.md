---
title: 延迟准确价格和折扣计算以提高性能
description: 本文介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 和呼叫中心提供的延迟价格计算功能。
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6926c288a91dbe66b6ffc2e6c06f866d3ebd7652
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845889"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>延迟准确价格和折扣计算以提高性能

[!include [banner](includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 和呼叫中心提供的延迟价格计算功能。

Dynamics 365 Commerce 支持创建多行折扣，在合并销售订单或销售报价单的多个销售行时应用这些折扣。 这些折扣包括组合购买、阈值和数量折扣。

每当向订单添加新行时，Commerce 定价引擎都会评估整个购物车来确定是否可以应用这些多行折扣。 由于这种重新计算，随着销售订单的增长，添加新行可能会影响性能。

但是，企业到企业 (B2B) 公司和一些企业对消费者 (B2C) 公司的订单量通常很大。 因此，在将每件商品添加到购物车后等待定价引擎重新计算可能非常耗时。 而且，对于大型订单，每次将商品添加到购物车时显示确切的价格和折扣通常不是很重要。 更重要的是用户能够快速添加商品。 延迟准确价格和折扣计算直到用户请求或订单完成的功能可以显著提高性能。 这还可以减少完成下订单所需的时间。

POS 中早已提供延迟准确价格和折扣计算的功能。 从 Commerce 版本 10.0.22 版本开始，它也可用于呼叫中心。

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>为 POS 启用延迟价格和折扣计算

要为 POS 启用延迟价格和折扣计算，请按照下列步骤操作。

1. 在 Commerce Headquarters 中，转到与实体店关联的功能配置文件。
1. 在 **金额** 快速选项卡上，启用 **手动计算多个商品折扣** 配置。
1. 打开应启用延迟计算的收银机的屏幕布局设计器。
1. 将 **计算合计** 操作的按钮添加到所需的按钮网格。
1. 运行 **1070** 和 **1090** 作业。

现在，当商品被添加到交易时，除非出纳选择 **计算合计** 按钮，否则不会计算多行折扣。 为交易选择 **计算合计** 后，将始终为其计算多行折扣。 出纳不必再次选择按钮，即使有其他商品被添加到购物车。 系统将不允许出纳捕获付款，直到选择 **计算合计**。

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>为呼叫中心启用延迟价格和折扣计算

要为呼叫中心启用延迟价格和折扣计算，请按照下列步骤操作。

1. 在 Commerce headquarters 中，转到 **工作区 \>功能管理**。
1. 启用 **防止意外计算商业订单价格** 功能。 此功能是延迟价格和折扣计算功能的先决条件。

    > [!NOTE]
    > 对于新部署，**防止意外计算商业订单价格** 功能默认启用。

1. 转到 **Commerce 参数 \> 价格和折扣**。
1. 在 **其他** 部分，启用 **手动计算多行价格和折扣** 配置。

现在，当在呼叫中心创建或编辑销售订单或销售报价单时，其准确价格和折扣计算将被延迟。 定价引擎将仅考虑正在添加或编辑的销售行，而忽略所有其他销售行。 商品的净额包括价格计算和简单折扣（单个商品的折扣百分比或折扣金额）。 但是，不会应用组合购买、阈值和数量折扣。 想要查看准确价格（包括所有折扣）的呼叫中心用户可以选择以下三个按钮之一：**重新计算**、**总计** 或 **完成**。

> [!NOTE]
> 对于呼叫中心订单，系统会显示一条警告消息，提醒用户必须选择 **重新计算**、**总计** 或 **完成** 按钮来完成准确价格和折扣的计算。 对于 **完成** 按钮可用的订单，呼叫中心用户无法跳过准确价格和折扣计算，因为他们必须选择 **完成** 才能完成订单捕获。 对于 **完成** 按钮不可用的订单，没有指示订单捕获完成的操作。 因此，呼叫中心用户负责在完成订单捕获之前选择 **重新计算** 或 **总计**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
