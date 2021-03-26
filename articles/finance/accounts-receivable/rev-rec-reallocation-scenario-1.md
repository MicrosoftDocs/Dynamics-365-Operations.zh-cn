---
title: 收入确认重新分配 - 方案 1
description: 本主题介绍了一种重新分配方案，在此方案中输入了两个销售订单，但仅对它们进行了确认。 如果两个以上的销售订单处于确认状态，则相同的方案将产生相似的结果。
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25fb32ce72555e573cd37a0ab092b51b99bb4372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260869"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>收入确认重新分配 - 方案 1

[!include [banner](../includes/banner.md)]

本主题介绍了一种重新分配方案，在此方案中输入了两个销售订单，但仅对它们进行了确认。 如果两个以上的销售订单处于确认状态，则相同的方案将产生相似的结果。

对于此方案，**总帐参数** 页面的 **收入确认** 选项卡上的 **将账单更正过帐到应收帐款** 选项设置为 **否**（**收入确认 \> 设置 \> 总帐参数**）。

[![“将账单更正过帐到应收帐款”选项设置为“否”](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

为客户 US\_SI\_0003 创建了一个销售订单。 客户正在购买笔记本电脑（项目编号 S0012）和支持计划（项目编号 S0008，“持续的工程服务”）。 笔记本电脑的收入将立即确认（没有收入确认计划）。 支持计划的收入将延期并在根据合同中日期范围定义的 12 个月内确认。

[![笔记本电脑和支持计划的销售订单行](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

已确认销售订单。 因为两个项目都是为收入价格分配设置的，所以在确认销售订单时将计算收入价格。 您可以查看将在 **收入价格分配** 页面（在 **销售订单** 页面的操作窗格的 **管理** 选项卡上的 **收入确认** 组中，选择 **收入价格分配**）上确认的收入。 笔记本电脑的收入将以 $1,008.01 的金额过帐到收入帐户。 支持计划的收入将以 $190.99 的金额过帐到延期收入帐户。 收入价格的总和必须等于为获取收入价格分配 ($1,199.00) 而设置的总行数。

[![收入价格分配页面](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

客户选择在销售时不购买安装服务（项目编号 S0001），但后来改变了主意。 因此，为同一客户输入了第二个销售订单。

[![安装服务的销售订单行](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

已确认第二个销售订单。 由于此销售订单仅包含一行，因此在确认销售订单时未进行收入价格分配。 仅当存在两个或以上的唯一项目并且设置这些项目以进行收入价格分配时，才会发生收入价格分配。

如果此新销售订单是对客户合同的唯一更改，则现在可以运行重新分配流程。 在两个销售订单之一中，选择 **使用新订单行重新分配价格** 以打开 **使用新订单行重新分配价格** 页面。 或者，转到 **收入确认 \> 定期任务 \> 使用新订单行重新分配价格**。 选择两个销售订单和相应的销售订单行，然后选择 **更新重新分配**。 **重新分配的金额** 列显示每个销售订单行的新收入价格。

[![“使用新订单行重新分配价格”页面上的新收入价格](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

如果选择 **预期凭证**，则不会显示任何内容，因为尚未过帐任何账单。

要完成重新分配，请选择 **处理**。 系统将会向您提示过帐日期，即使未过帐任何内容。 重新分配完成后，每个销售订单的 **收入价格分配** 页面将显示两个销售订单中所有项目的价格分配。 换句话说，每个销售订单的 **收入价格分配** 页面将包含该销售订单上不存在的项目，因为它属于同一合同，但位于不同的销售订单上。

> [!TIP]
> 要提供有关为什么显示这些附加项目的上下文，您可以向网格中添加其他列，例如 **重新分配 ID** 和 **销售订单**。
> 
> [![“收入价格分配”页面上的其他列](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]