---
title: 部分预留的转移单批发布
description: 此主题描述如何从移动设备设置和应用部分预留的转移单批发布。
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13e3525049c893a7193b549f5b4ba63b8841b87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233263"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>部分预留的转移单批发布

[!include [banner](../includes/banner.md)]

通过部分预留的转移单批发布功能可以使用批处理作业将转移单部分发布到仓库。
由于您可以选择发布部分数量，因此您无需等到全部订单数量在仓库中可用后再发布订单。

将订单发布到仓库是一项高级仓库管理流程。 此流程包括仓库工作人员使用移动设备可以执行的活动，如领料、包装和装运。

## <a name="where-it-applies"></a>适用情况

通过此功能可以使用批处理作业将转移单发布到仓库。 当仓库中没有足够的库存，但您仍然想要将一个仓库的物料转移到另一个仓库时，此功能很有用。

## <a name="how-it-is-set-up"></a>如何设置

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>指定转移单和销售订单的履行条件

可以在批处理中将订单部分发布到仓库前，必须满足履行条件。 这些履行条件由履行策略确定。

转移单和销售订单的履行策略在公司级别指定。 根据履行策略的设置，批发布订单将被接受或拒绝。 然后对订单进行相应的处理。

-   若要为转移单和销售订单创建履行策略，请单击 **仓库管理** \> **设置** \> **发放到仓库** \> **履行策略**，然后通过输入名称和描述创建履行策略。

-   若要指定履行费率、值类型和违反履行策略时要显示的消息，请单击 **仓库管理** \> **设置** \> **发放到仓库** \> **履行策略**，然后设置 **履行费率**、**值类型** 和 **履行违反消息** 字段。

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>设置转移单和销售订单的履行策略

-   若要设置转移单的履行策略，请单击 **库存管理** \> **设置** \>**库存和仓库管理参数** \> **转移单** \> **仓库管理**，然后选择转移单履行策略。

-   若要设置销售订单的履行策略，请单击 **应收账款** \> **设置**\> **应收账款参数** \> **仓库管理**，然后选择销售订单履行策略。

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>允许批发布并指定应批发布的数量。

批处理作业用于在批处理中将订单发布到仓库。 用于区分应在批处理作业中运行的订单的参数在批处理作业本身上进行设置。

**数量** 参数指定是否应批发布全部数量或实际预留的数量。 **允许发布已部分发放的订单** 参数确定批处理中的订单在提前部分发放时是否应接受或拒绝。

-   若要设置转移单的 **数量** 和 **允许发布已部分发放的订单** 参数，请单击 **仓库管理** \> **发放到仓库** \> **自动发放转移单**。

-   若要设置销售订单的 **数量** 和 **允许发布已部分发放的订单** 参数，请单击 **仓库管理** \> **发放到仓库** \> **自动发放销售订单**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]