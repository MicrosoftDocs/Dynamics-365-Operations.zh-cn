---
title: 出库流程
description: 此主题概要介绍了库存管理中的出库流程。
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 5ac3260f128acbc819d7207f68f17adb085da11c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570451"
---
# <a name="outbound-process"></a><span data-ttu-id="b11b8-103">出库流程</span><span class="sxs-lookup"><span data-stu-id="b11b8-103">Outbound process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b11b8-104">此主题概要介绍了库存管理中的出库流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="b11b8-105">输出单</span><span class="sxs-lookup"><span data-stu-id="b11b8-105">Output orders</span></span>

<span data-ttu-id="b11b8-106">输出单用于关联销售订单行和转移单行与使用领料单的出站领料流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="b11b8-107">从销售订单或转移单生成领料单时，自动创建输出单和装运。</span><span class="sxs-lookup"><span data-stu-id="b11b8-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="b11b8-108">领料单与装运具有一对一的关系。</span><span class="sxs-lookup"><span data-stu-id="b11b8-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="b11b8-109">转移单装运或销售订单装箱单可以从装运进行处理。</span><span class="sxs-lookup"><span data-stu-id="b11b8-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="b11b8-110">下图显示了出货订单流程的概览。</span><span class="sxs-lookup"><span data-stu-id="b11b8-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="b11b8-111">[![出货订单流程概览](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="b11b8-112">您可以设置出货规则，以便定义程序如何处理出货流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="b11b8-113">您可以使用这些规则控制装运流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="b11b8-114">特别是可以使用这些规则控制可以在流程的哪个阶段发送装运。</span><span class="sxs-lookup"><span data-stu-id="b11b8-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="b11b8-115">以下设置定义如何处理出货流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="b11b8-116">销售订单和转移单的领料流程状态</span><span class="sxs-lookup"><span data-stu-id="b11b8-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="b11b8-117">转到**应收账款** \> **设置** \> **应收账款参数**，然后在**更新**选项卡上的**领料流程状态**字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b11b8-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="b11b8-118">[![销售订单的领料流程状态字段](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="b11b8-119">如果**领料流程状态**字段设置为**已完成**，则在生成领料单的流程中自动发生领料流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="b11b8-120">如果字段设置为**已启用**，必须手动更新领料单行。</span><span class="sxs-lookup"><span data-stu-id="b11b8-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="b11b8-121">相同的设置适用于转移单。</span><span class="sxs-lookup"><span data-stu-id="b11b8-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="b11b8-122">转到**库存管理** \> **设置** \> **库存和仓库管理参数**，然后在**运输**选项卡的**领料流程状态**字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b11b8-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="b11b8-123">[![转移单的领料流程状态字段](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="b11b8-124">结束输出库存订单</span><span class="sxs-lookup"><span data-stu-id="b11b8-124">End output inventory orders</span></span>

<span data-ttu-id="b11b8-125">转到**库存管理** \> **设置** \> **库存和仓库管理参数**，然后在**常规**选项卡上设置**结束输出库存订单**选项。</span><span class="sxs-lookup"><span data-stu-id="b11b8-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="b11b8-126">[![结束输出库存订单选项](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="b11b8-127">在仓库工作人员减少领料单数量时，相应的库存订单数量将从装运中删除。</span><span class="sxs-lookup"><span data-stu-id="b11b8-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="b11b8-128">在某个时间点更新了领料单后，如果**结束输出库存订单**选项设置为**是**，其余数量将往回报告给订单。</span><span class="sxs-lookup"><span data-stu-id="b11b8-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="b11b8-129">如果**结束输出库存订单**选项设置为**否**，剩余数量将作为未结输出单数量保留，且必须作为**未结输出单**功能的一部分添加到新的领料单中。</span><span class="sxs-lookup"><span data-stu-id="b11b8-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="b11b8-130">[![功能菜单上的未结输出单命令](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="b11b8-131">[![未结输出单页上的功能菜单](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="b11b8-132">缩减数量</span><span class="sxs-lookup"><span data-stu-id="b11b8-132">Reduce quantity</span></span>

<span data-ttu-id="b11b8-133">在生成领料单的流程中可以使用的第三个参数是**减少数量**参数。</span><span class="sxs-lookup"><span data-stu-id="b11b8-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="b11b8-134">此参数的设置与在发放到仓库时触发预留流程的**预留**设置一起使用。</span><span class="sxs-lookup"><span data-stu-id="b11b8-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="b11b8-135">[![减少数量参数](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="b11b8-136">销售订单出货流程示例</span><span class="sxs-lookup"><span data-stu-id="b11b8-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="b11b8-137">在此例中，有一个具有两个物料的销售订单。</span><span class="sxs-lookup"><span data-stu-id="b11b8-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="b11b8-138">在生成领料单时，选择**减少数量**参数。</span><span class="sxs-lookup"><span data-stu-id="b11b8-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="b11b8-139">因此，您仅对可用的现有库存量发放和创建领料行。</span><span class="sxs-lookup"><span data-stu-id="b11b8-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="b11b8-140">必须通过用于领料单的登记过程报告领料（**领料流程状态**  =  **已启用**）。</span><span class="sxs-lookup"><span data-stu-id="b11b8-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="b11b8-141">尚未预留的库存在生成领料单的过程中预留。</span><span class="sxs-lookup"><span data-stu-id="b11b8-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="b11b8-142">不可用的库存可从销售订单中删除或发放到仓库中用于以后当库存可用于领料时进行发货处理。</span><span class="sxs-lookup"><span data-stu-id="b11b8-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="b11b8-143">[![更新领料单](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="b11b8-144">一旦领取完**领料单登记**页上的所有领料行，关联的装运即已完成。</span><span class="sxs-lookup"><span data-stu-id="b11b8-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="b11b8-145">之后可以基于领取的库存启动销售订单装箱单流程。</span><span class="sxs-lookup"><span data-stu-id="b11b8-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="b11b8-146">[![更新出站装运](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="b11b8-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
