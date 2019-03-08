---
title: 创建含交货计划的采购订单
description: 此过程显示如何为采购订单创建交货计划。
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a9b7b233339d41605e1b115bd14a18b706ef226
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "333821"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="46a7f-103">创建含交货计划的采购订单</span><span class="sxs-lookup"><span data-stu-id="46a7f-103">Create a purchase order with a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46a7f-104">此过程显示如何为采购订单创建交货计划。</span><span class="sxs-lookup"><span data-stu-id="46a7f-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="46a7f-105">在请求在多个装运中交付订单或日记帐上的数量时，使用交货计划。</span><span class="sxs-lookup"><span data-stu-id="46a7f-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="46a7f-106">可以在 USMF 演示数据公司中使用本指南中的示例。</span><span class="sxs-lookup"><span data-stu-id="46a7f-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="46a7f-107">此过程通常由采购代理完成。</span><span class="sxs-lookup"><span data-stu-id="46a7f-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="46a7f-108">创建交货计划</span><span class="sxs-lookup"><span data-stu-id="46a7f-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="46a7f-109">转到“采购”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="46a7f-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-110">Click New.</span></span>
3. <span data-ttu-id="46a7f-111">在“供应商帐户”字段中输入 US-101。</span><span class="sxs-lookup"><span data-stu-id="46a7f-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="46a7f-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-112">Click OK.</span></span>
5. <span data-ttu-id="46a7f-113">在“物料编号”字段中输入 M0001。</span><span class="sxs-lookup"><span data-stu-id="46a7f-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="46a7f-114">在“数量”字段中，输入 10。</span><span class="sxs-lookup"><span data-stu-id="46a7f-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="46a7f-115">单击“采购订单行”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="46a7f-116">单击“交货计划”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="46a7f-117">“交货计划”页可用于指定装运数量的位置，订单行的总数量从供应商交付。</span><span class="sxs-lookup"><span data-stu-id="46a7f-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="46a7f-118">默认情况下，系统将复制总数量和原始采购行的交付详细信息到交货计划第一行。</span><span class="sxs-lookup"><span data-stu-id="46a7f-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="46a7f-119">在此示例中，我们为两个装运创建一个计划，第一个装运日期抵消第二个装运日期一周。</span><span class="sxs-lookup"><span data-stu-id="46a7f-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="46a7f-120">在“数量”字段中，将数量更改为 4。</span><span class="sxs-lookup"><span data-stu-id="46a7f-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="46a7f-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-121">Click New.</span></span>
11. <span data-ttu-id="46a7f-122">在“数量”字段中，输入 6 作为剩余数量。</span><span class="sxs-lookup"><span data-stu-id="46a7f-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="46a7f-123">在交付日期字段中，选择比第一个交付行的日期晚一周的日期。</span><span class="sxs-lookup"><span data-stu-id="46a7f-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="46a7f-124">您可以通过查看“总计”和“剩余”字段，跟踪查看分配到交货计划行的总数量。</span><span class="sxs-lookup"><span data-stu-id="46a7f-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="46a7f-125">在剩余数量为零时，原始行的全部数量已分配到计划中。</span><span class="sxs-lookup"><span data-stu-id="46a7f-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="46a7f-126">展开“费用转换”部分。</span><span class="sxs-lookup"><span data-stu-id="46a7f-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="46a7f-127">此处的选项用于控制如何在交货计划行之间分配费用。</span><span class="sxs-lookup"><span data-stu-id="46a7f-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="46a7f-128">如果选择“复制总额”，将把原始订单行中的费用金额复制到每交付行。</span><span class="sxs-lookup"><span data-stu-id="46a7f-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="46a7f-129">“分配到交货行”选项根据各交付行中的数量划分原始行费用。</span><span class="sxs-lookup"><span data-stu-id="46a7f-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="46a7f-130">折叠“费用转换”部分。</span><span class="sxs-lookup"><span data-stu-id="46a7f-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="46a7f-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-131">Click OK.</span></span>
    * <span data-ttu-id="46a7f-132">交货计划现在已被应用于订单。</span><span class="sxs-lookup"><span data-stu-id="46a7f-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="46a7f-133">原始订单行（现在称为业务行）已转换为具有多个交货项的订单行。</span><span class="sxs-lookup"><span data-stu-id="46a7f-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="46a7f-134">其标有不同图标，作为交货行的标头。</span><span class="sxs-lookup"><span data-stu-id="46a7f-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="46a7f-135">选择第二个订单行，即两个交货行中的第一个。</span><span class="sxs-lookup"><span data-stu-id="46a7f-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="46a7f-136">两个新行，即交货行，构成交货计划。</span><span class="sxs-lookup"><span data-stu-id="46a7f-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="46a7f-137">该订单将处理这些新行，而不是原始行。</span><span class="sxs-lookup"><span data-stu-id="46a7f-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="46a7f-138">如果打印单据（如确认、产品收货日记帐或发票），则只显示交货行。</span><span class="sxs-lookup"><span data-stu-id="46a7f-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="46a7f-139">更改交货计划</span><span class="sxs-lookup"><span data-stu-id="46a7f-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="46a7f-140">您可以更改交货行的数量。</span><span class="sxs-lookup"><span data-stu-id="46a7f-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="46a7f-141">如果更改，业务行将自动更新为交货行中的总数量。</span><span class="sxs-lookup"><span data-stu-id="46a7f-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="46a7f-142">在第一个交货行的“数量”字段中，将数量从 4 更改为 5。</span><span class="sxs-lookup"><span data-stu-id="46a7f-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="46a7f-143">选择第一个订单行（业务行）。</span><span class="sxs-lookup"><span data-stu-id="46a7f-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="46a7f-144">业务行中的数量已更改为 11。</span><span class="sxs-lookup"><span data-stu-id="46a7f-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="46a7f-145">使用交货计划处理产品收货</span><span class="sxs-lookup"><span data-stu-id="46a7f-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="46a7f-146">必须先确认采购订单，才能处理产品收货。</span><span class="sxs-lookup"><span data-stu-id="46a7f-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="46a7f-147">在此示例中，直接在采购订单上记录收货。</span><span class="sxs-lookup"><span data-stu-id="46a7f-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="46a7f-148">也可以在货物到达仓库时记录收货。</span><span class="sxs-lookup"><span data-stu-id="46a7f-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="46a7f-149">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="46a7f-150">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-150">Click Confirm.</span></span>
3. <span data-ttu-id="46a7f-151">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="46a7f-152">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-152">Click Product receipt.</span></span>
5. <span data-ttu-id="46a7f-153">在“物料收货”字段中键入任何值。</span><span class="sxs-lookup"><span data-stu-id="46a7f-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="46a7f-154">此字段用于输入将用作产品收货日记帐的凭证的参考。</span><span class="sxs-lookup"><span data-stu-id="46a7f-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="46a7f-155">在“数量”字段中，选择“订购数量”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="46a7f-156">此选项表示将处理随订单行创建的数量的收货。</span><span class="sxs-lookup"><span data-stu-id="46a7f-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="46a7f-157">确保“打印产品收货”字段设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="46a7f-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="46a7f-158">此示例中无需打印。</span><span class="sxs-lookup"><span data-stu-id="46a7f-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="46a7f-159">展开“行”部分。</span><span class="sxs-lookup"><span data-stu-id="46a7f-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="46a7f-160">请注意如何为两个交付行创建产品收货，而不是为原始订单行创建。</span><span class="sxs-lookup"><span data-stu-id="46a7f-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="46a7f-161">如果收货已在仓库中记录，则还会在交货计划行中记录。</span><span class="sxs-lookup"><span data-stu-id="46a7f-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="46a7f-162">折叠“行”部分。</span><span class="sxs-lookup"><span data-stu-id="46a7f-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="46a7f-163">单击“确定”以过帐收据。</span><span class="sxs-lookup"><span data-stu-id="46a7f-163">Click OK to post the receipt.</span></span>

