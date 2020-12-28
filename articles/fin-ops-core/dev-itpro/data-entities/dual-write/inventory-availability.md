---
title: 采用双写入的库存可用性
description: 本主题提供有关如何以双写入方式检查库存可用性的信息。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4450171"
---
# <a name="inventory-availability-in-dual-write"></a>采用双写入的库存可用性

[!include [banner](../../includes/banner.md)]

使用库存可用性，可以在 Microsoft Dynamics 365 Sales 中先检查库存，然后再将产品添加到 **报价单**、**订单** 或 **发票** 页面。 例如，检查库存并将履行日期确定为[目标客户到现金](dual-write-prospect-to-cash.md)流程的一个关键任务。

如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。 您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。

## <a name="on-hand-inventory"></a>现有库存

在 Dynamics 365 Sales 中，**报价单**、**订单** 和 **发票** 页面的标题中已经添加了一个新的 **现有库存量** 按钮。 选择此按钮时，将出现一个对话框，您可以在其中指定要检查其现有库存量的公司和产品。 此对话框显示的信息与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同。

此对话框返回 Dynamics 365 Supply Chain Management 中的库存信息。 此信息包括以下数量：

- 现有数量
- 预留现有数量
- 可用现有数量
- 订购数量
- 在单数量
- 预留的订购数量
- 可用总数

## <a name="atp-information"></a>ATP 信息

在 Sales 中，**报价单**、**订单** 和 **发票** 页面的行项中已经添加了新的 **ATP 信息** 按钮。 选择此按钮时，将出现一个对话框，您可以在其中指定公司、产品、库存站点、库存仓库和订单数量。 此对话框具有与[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置相同的设置。

此对话框返回 Supply Chain Management 中的 ATP 信息。 此信息包括以下数量：

- ATP 数量
- 收货数量
- 发货数量
- 现有数量
