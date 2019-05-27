---
title: 创建交货计划
description: 此过程显示如何为销售订单创建交货计划。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d99dfae5e045262d34daf3529a6a3f4716b4afe3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563854"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="04711-103">创建交货计划</span><span class="sxs-lookup"><span data-stu-id="04711-103">Create delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04711-104">此过程显示如何为销售订单创建交货计划。</span><span class="sxs-lookup"><span data-stu-id="04711-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="04711-105">在请求在多个装运中交付订单或报价单上的数量时，使用交货计划。</span><span class="sxs-lookup"><span data-stu-id="04711-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="04711-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="04711-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="04711-107">创建交货计划</span><span class="sxs-lookup"><span data-stu-id="04711-107">Create delivery schedule</span></span>
1. <span data-ttu-id="04711-108">转到“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="04711-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="04711-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="04711-109">Click New.</span></span>
3. <span data-ttu-id="04711-110">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="04711-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="04711-111">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04711-111">Click OK.</span></span>
5. <span data-ttu-id="04711-112">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="04711-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="04711-113">在“数量”字段中，输入大于 1 的数字。</span><span class="sxs-lookup"><span data-stu-id="04711-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="04711-114">单击“销售订单行”。</span><span class="sxs-lookup"><span data-stu-id="04711-114">Click Sales order line.</span></span>
8. <span data-ttu-id="04711-115">单击“交货计划”。</span><span class="sxs-lookup"><span data-stu-id="04711-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="04711-116">“交货计划”页是您可以指定装运数量的位置，订单行的总数量将会交付给客户。</span><span class="sxs-lookup"><span data-stu-id="04711-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="04711-117">默认情况下，系统将复制总数量和原始销售行的交付详细信息到交货计划第一行。</span><span class="sxs-lookup"><span data-stu-id="04711-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="04711-118">在此示例中，我们为两个装运创建一个计划，第一个装运日期抵消第二个装运日期一周。</span><span class="sxs-lookup"><span data-stu-id="04711-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="04711-119">在“数量”字段中，输入为总数量的一部分的数字。</span><span class="sxs-lookup"><span data-stu-id="04711-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="04711-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="04711-120">Click New.</span></span>
11. <span data-ttu-id="04711-121">在“数量”字段中，输入剩余数量。</span><span class="sxs-lookup"><span data-stu-id="04711-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="04711-122">在“要求装运日期”字段中，输入第一行交货日期前一周的日期。</span><span class="sxs-lookup"><span data-stu-id="04711-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="04711-123">一旦已分配费用至原始订单行，“费用转换”快速选项卡上的两个选项控制您想要分配到交货计划行上的费用。</span><span class="sxs-lookup"><span data-stu-id="04711-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="04711-124">如果已选择“复制总额”，同一费用金额将复制到每行。</span><span class="sxs-lookup"><span data-stu-id="04711-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="04711-125">对于“分配到交货行”选项，其将费用平均分摊到交货行。</span><span class="sxs-lookup"><span data-stu-id="04711-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="04711-126">只可以拆分固定费用，而仍将可变费用复制到这些行。</span><span class="sxs-lookup"><span data-stu-id="04711-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="04711-127">将光标远离第二个交货行，以更新页面。</span><span class="sxs-lookup"><span data-stu-id="04711-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="04711-128">您可以通过查看“总计”和“剩余”字段，跟踪查看分配到交货计划行的总数量。</span><span class="sxs-lookup"><span data-stu-id="04711-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="04711-129">在剩余数量为零时，原始行的全部数量已分配到计划中。</span><span class="sxs-lookup"><span data-stu-id="04711-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="04711-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04711-130">Click OK.</span></span>
    * <span data-ttu-id="04711-131">交货计划现在已复制到订单行。</span><span class="sxs-lookup"><span data-stu-id="04711-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="04711-132">原始订单行，即业务行，已转换为具有多个交货项的订单行。</span><span class="sxs-lookup"><span data-stu-id="04711-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="04711-133">其将标有不同图标，且作为交货行的抬头。</span><span class="sxs-lookup"><span data-stu-id="04711-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="04711-134">这两个新行（即交货行）共同构成一个交货计划。</span><span class="sxs-lookup"><span data-stu-id="04711-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="04711-135">该订单将处理这些新行，而不是原始行。</span><span class="sxs-lookup"><span data-stu-id="04711-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="04711-136">如果打印单据（如确认单、领料单、装箱单或发票），则只显示交货行。</span><span class="sxs-lookup"><span data-stu-id="04711-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="04711-137">交货行可以有不同的交货日期、数量、交货方式以及站点和仓库等存储维度。</span><span class="sxs-lookup"><span data-stu-id="04711-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="04711-138">但是，产品维度必须始终与业务行上维度一致，且不能更改。</span><span class="sxs-lookup"><span data-stu-id="04711-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="04711-139">在“数量”字段中，输入大于当前数字的数字。</span><span class="sxs-lookup"><span data-stu-id="04711-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="04711-140">选择业务行，以查看数量重新计算的影响。</span><span class="sxs-lookup"><span data-stu-id="04711-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="04711-141">在操作窗格中，单击“领料和装箱”。</span><span class="sxs-lookup"><span data-stu-id="04711-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="04711-142">单击“发布装箱单”。</span><span class="sxs-lookup"><span data-stu-id="04711-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="04711-143">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="04711-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="04711-144">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="04711-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="04711-145">请注意，将为两个交货计划行，而不是原始订单行创建装箱单。</span><span class="sxs-lookup"><span data-stu-id="04711-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="04711-146">在“打印装箱单”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="04711-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="04711-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04711-147">Click OK.</span></span>
23. <span data-ttu-id="04711-148">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="04711-148">Click Yes.</span></span>
24. <span data-ttu-id="04711-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="04711-149">Close the page.</span></span>

