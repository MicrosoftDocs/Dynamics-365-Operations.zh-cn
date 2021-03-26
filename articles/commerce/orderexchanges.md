---
title: 配置和处理有关退货单的交换
description: 本主题将介绍如何在 Dynamics 365 Commerce 中配置退货交换。
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5419c18a510b0d35dabe5329a9557780cb7637b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257115"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>配置和处理有关退货单的交换

[!include [banner](includes/banner.md)]

在先前版本的 Dynamics 365 Commerce 中，针对客户订单的退货是采用 Headquarters 中的退货单文档进行处理的。 但是，退货单文档仅可用于处理要退货的产品。 退货产品由退货单行上的负数量指示。 相对比的是，销量由正数量指示。 但是，退货单文档不支持正数量。 由于此限制，先前版本的应用不支持使用退货单文档进行产品交换的方案。

但是，现已添加了相应功能，可支持就退货单进行产品交换的方案。 Commerce 现在使用销售订单文档而不是退货单文档来处理这些类型的交易。

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>配置 Commerce 以支持就退货单进行产品交换

请按以下步骤操作，将系统配置为支持就退货单进行产品交换。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。 在 **客户订单** 快速选项卡上，将 **将退货单作为销售订单处理** 选项设置为 **是**。
2. 运行 **全局配置配送计划** 作业 (**1110**)。

## <a name="make-an-exchange"></a>进行交换

在按照上一部分中所述配置系统之后，与在先前版本的应用中的操作一样，销售点 (POS) 用户仍将选择销售订单或销售账单来处理退货。 但是，在将退回物料添加到购物车之后，用户将能够向购物车添加新的销售行。

对于这些新的销售行，用户必须定义所有必需的属性才能处理客户订单行。 这些属性包括交货方法和履行位置。 交易的到期付款将是退货单行和销售订单行的净额。 当支付交易款项时，退货单将在 Headquarters 中过账为销售订单文档，系统将立即根据退货行开具账单。

为了让用户更好地了解购物车的各项金额，购物车中新增了三个金额字段。 您可以使用屏幕设计器，在 POS 用户界面 (UI) 中提供这些新字段。

- **存款单已应用** - 当用户执行客户订单选择时应用于交易的存款金额。 如果不存在存款覆盖，并且配置了 10% 的存款，则此字段中的金额为客户订单总金额的 90%。
- **执行金额** - 创建或编辑客户订单时或者在客户订单交换期间，交货方式设置为 **执行** 情况下各行的总金额。 此字段中的金额包括税款和费用。
- **退货金额** - 客户订单交换期间具有负数量的行的总金额。 此字段中的金额包括税款和费用。


[!INCLUDE[footer-include](../includes/footer-banner.md)]