---
title: "出库流程"
description: "此主题概要介绍了库存管理中的出库流程。"
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: zh-cn
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a>出库流程

[!include[banner](../includes/banner.md)]

此主题概要介绍了库存管理中的出库流程。

## <a name="output-orders"></a>输出单

输出单用于关联销售订单行和转移单行与使用领料单的出站领料流程。

从销售订单或转移单生成领料单时，自动创建输出单和装运。 领料单与装运具有一对一的关系。 转移单装运或销售订单装箱单可以从装运进行处理。 

下图显示了出货订单流程的概览。 

[![出货订单流程概览](./media/outbound-order.png)](./media/outbound-order.png)

您可以设置出货规则，以便定义程序如何处理出货流程。 您可以使用这些规则控制装运流程。 特别是可以使用这些规则控制可以在流程的哪个阶段发送装运。 以下设置定义如何处理出货流程。

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>销售订单和转移单的领料流程状态 

转到**应收账款** \> **设置** \> **应收账款参数**，然后在**更新**选项卡上的**领料流程状态**字段中选择一个值。

[![销售订单的领料流程状态字段](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

如果**领料流程状态**字段设置为**已完成**，则在生成领料单的流程中自动发生领料流程。 如果字段设置为**已启用**，必须手动更新领料单行。

相同的设置适用于转移单。 转到**库存管理** \> **设置** \> **库存和仓库管理参数**，然后在**运输**选项卡的**领料流程状态**字段中选择一个值。

[![转移单的领料流程状态字段](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>结束输出库存订单

转到**库存管理** \> **设置** \> **库存和仓库管理参数**，然后在**常规**选项卡上设置**结束输出库存订单**选项。

[![结束输出库存订单选项](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

在某些情况下，在领料单流程中不能领取库存中的某些物料。 例如，如果仓库工作人员减少领料行上的数量后再处理领料单，就可能发生这种情况。 如果**结束输出库存订单**选项设置为**是**，则剩余的未领取数量则往回报告至订单级别。 如果此选项设置为**否**，则剩余的未领取数量保留为未结输出单数量。 在这种情况下，作为**未结输出单**功能的一部分，这些数量仍然发放到仓库，且必须添加到新的领料单中。

[![功能菜单上的未结输出单命令](./media/open-output-order.png)](./media/open-output-order.png)

[![未结输出单页上的功能菜单](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>缩减数量

在生成领料单的流程中可以使用的第三个参数是**减少数量**参数。 此参数的设置与在发放到仓库时触发预留流程的**预留**设置一起使用。

[![减少数量参数](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>销售订单出货流程示例

在此例中，有一个具有两个物料的销售订单。 在生成领料单时，选择**减少数量**参数。 因此，您仅对可用的现有库存量发放和创建领料行。 必须通过用于领料单的登记过程报告领料（**领料流程状态**  =  **已启用**）。

尚未预留的库存在生成领料单的过程中预留。 不可用的库存可从销售订单中删除或发放到仓库中用于以后当库存可用于领料时进行发货处理。

[![更新领料单](./media/update-picking-list.png)](./media/update-picking-list.png)

一旦领取完**领料单登记**页上的所有领料行，关联的装运即已完成。 之后可以基于领取的库存启动销售订单装箱单流程。

[![更新出站装运](./media/outbound-shipments.png)](./media/outbound-shipments.png)

