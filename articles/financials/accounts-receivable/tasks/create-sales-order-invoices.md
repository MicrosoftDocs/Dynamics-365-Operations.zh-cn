--- 
title: "创建销售订单发票"
description: "此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6f687816fc6393de2a587273a5350858b3503945
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="e67d6-103">创建销售订单发票</span><span class="sxs-lookup"><span data-stu-id="e67d6-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e67d6-104">此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。</span><span class="sxs-lookup"><span data-stu-id="e67d6-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="e67d6-105">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="e67d6-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="e67d6-106">为一个销售订单创建一张发票</span><span class="sxs-lookup"><span data-stu-id="e67d6-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="e67d6-107">转到“应收账款”>“订单”>“已装运但未开票采购订单”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="e67d6-108">从列表中选择一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="e67d6-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="e67d6-109">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e67d6-110">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-110">Click Invoice.</span></span>
    * <span data-ttu-id="e67d6-111">请注意此销售订单具有多个相关的装箱单。</span><span class="sxs-lookup"><span data-stu-id="e67d6-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="e67d6-112">它将只显示单词“<multiple>”，不会显示装箱单编号。</span><span class="sxs-lookup"><span data-stu-id="e67d6-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="e67d6-113">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="e67d6-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="e67d6-114">若要过帐发票，请设定为“是”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="e67d6-115">也可以关闭过帐功能只打印发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="e67d6-116">但是您还可以通过创建形式发票代替发票，效果一样。</span><span class="sxs-lookup"><span data-stu-id="e67d6-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="e67d6-117">此选项用于批处理作业。</span><span class="sxs-lookup"><span data-stu-id="e67d6-117">This option is used for batch jobs.</span></span> <span data-ttu-id="e67d6-118">运行批处理作业，查询将会运行。</span><span class="sxs-lookup"><span data-stu-id="e67d6-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="e67d6-119">在“打印”字段中，选择“以后”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="e67d6-120">选择“是”以“打印发票”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="e67d6-121">“打印管理”可打印多个发票副本并通过电子邮件以 PDF 文档的形式发送发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="e67d6-122">在“打印费用”字段中，选择“汇总”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="e67d6-123">在“检查信用额度”字段中，选择“余额”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="e67d6-124">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="e67d6-125">合并订单为一张发票</span><span class="sxs-lookup"><span data-stu-id="e67d6-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="e67d6-126">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="e67d6-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e67d6-127">选定一个拥有多个发票的客户。</span><span class="sxs-lookup"><span data-stu-id="e67d6-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="e67d6-128">选择一个开放销售订单。</span><span class="sxs-lookup"><span data-stu-id="e67d6-128">Select an open sales order.</span></span>
4. <span data-ttu-id="e67d6-129">再选择同一个客户的另一个未结销售订单。</span><span class="sxs-lookup"><span data-stu-id="e67d6-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="e67d6-130">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="e67d6-131">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-131">Click Invoice.</span></span>
7. <span data-ttu-id="e67d6-132">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="e67d6-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="e67d6-133">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="e67d6-134">请注意在概述部分列出的两张发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="e67d6-135">现在将两张合并为一张发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="e67d6-136">在“汇总更新”字段中，选择“发票帐目”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="e67d6-137">单击“整理”合并这两个销售订单为一张发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="e67d6-138">两个销售订单现在合并为一张发票。</span><span class="sxs-lookup"><span data-stu-id="e67d6-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="e67d6-139">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-139">Click Cancel.</span></span>
12. <span data-ttu-id="e67d6-140">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="e67d6-141">成批过帐发票</span><span class="sxs-lookup"><span data-stu-id="e67d6-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="e67d6-142">转到“应收账款“>”发票“>”批处理发票“>”发票“。</span><span class="sxs-lookup"><span data-stu-id="e67d6-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="e67d6-143">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-143">Click Select.</span></span>
3. <span data-ttu-id="e67d6-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-144">Click OK.</span></span>
4. <span data-ttu-id="e67d6-145">单击“批处理”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-145">Click Batch.</span></span>
5. <span data-ttu-id="e67d6-146">单击“是”打开批处理程序。</span><span class="sxs-lookup"><span data-stu-id="e67d6-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="e67d6-147">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-147">Click Recurrence.</span></span>
7. <span data-ttu-id="e67d6-148">选择“天数”</span><span class="sxs-lookup"><span data-stu-id="e67d6-148">Select Days</span></span>
8. <span data-ttu-id="e67d6-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-149">Click OK.</span></span>
9. <span data-ttu-id="e67d6-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-150">Click OK.</span></span>
10. <span data-ttu-id="e67d6-151">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-151">Click Cancel.</span></span>
11. <span data-ttu-id="e67d6-152">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="e67d6-152">Click Yes.</span></span>


