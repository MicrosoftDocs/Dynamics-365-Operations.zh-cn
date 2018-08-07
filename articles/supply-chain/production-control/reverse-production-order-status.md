---
title: "冲销生产订单状态"
description: "此主题描述如何反转生产订单状态。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a>冲销生产订单状态

[!include [banner](../includes/banner.md)]

此主题描述如何反转生产订单状态。 

如果您反转生产订单的状态，订单以及与工艺路线相关联的所有工序都反转到生产生命周期中的前一个步骤。 例如，生产订单状态为**已计划**，您将状态更改回**已创建**。 在这种情况下，系统必须首先将状态更改为“**已估计**”，此状态将立即位于“**已计划**”之前。 然后可以将状态更改为所需的状态，**已创建**。 **注意：** 如果您的订单已达到状态**完工入库**，您仍然可以将该订单反转回更早的状态。 但是，您必须重新运行估计和工序级排产、作业级排产或两类排产同时运行，继续更新有关该订单的信息。 需要此步骤的原因在于，也必须重置剩余物料消耗量和运营资源消耗量的任何预留。 本文其余部分将说明在反转生产订单的状态时，通过以下方式查看发生的情况：

-   从**已估计**到**已创建**
-   从**已计划**到**已估计**
-   从**已发布**到**已计划**
-   从**已开始**到**已发布**

## <a name="from-estimated-to-created"></a>从“已估计”到“已创建”
在您将生产订单的状态从**已估计**返回到**已创建**时，将删除为物料清单 (BOM) 中的物料计算的物料消耗量。 生产行上的库存交易记录将被删除，并且生产订单的物料清单行的**余额状态**字段将重置为**已结束**。 当选择**派生采购**和**派生生产**选择时，所有基础采购订单或生产订单都将被删除。 如果您估计生产订单的成本，或如果您手动预留物料以便它们可以用于生产，也将删除这些交易记录。

## <a name="from-scheduled-to-estimated"></a>从“已计划”到“已估计”
在您将生产订单的状态从**已计划**返回到**已估计**时，将删除计划的开始日期和结束日期以及开始时间和结束时间。 还将删除排产期间进行的产能预留，并且删除作业级排产期间创建的作业。 在**生产订单详细信息**页上记录的与工序级排产和作业级排产相关的所有信息将重置。

## <a name="from-released-to-scheduled"></a>从“已发布”到“已计划”
在您将生产订单的状态从**已发布**返回到**已计划**时，发生的唯一变化是状态字段中的值。

## <a name="from-started-to-released"></a>从“已开始”到“已发布”
在您将生产订单的状态从**已开始**返回到**已发布** 时，所有报告为完工入库的物料也将还原。 如果物料已领料或者入库和出库交货已交付生产，则将反转这些设置。 生产订单的物料清单行上的**余额状态**字段从**已结束**更改为**物料消耗量**。 如果登记时间或数量已报告为在生产工艺路线中的工序已完工入库，这些设置将撤消。 生产工艺路线中的**余额状态**字段从**已结束**更改为**工艺路线消耗**。 按流程过帐或在制品的所有物料的设置将反转。 在**生产订单详细信息**页上，显示已开始或完工入库的数量的字段将重置。 还重置这些交易记录的日期。




