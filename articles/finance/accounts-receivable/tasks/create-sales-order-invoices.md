---
title: 创建销售订单发票
description: 此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837097"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="2f34b-103">创建销售订单发票</span><span class="sxs-lookup"><span data-stu-id="2f34b-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f34b-104">此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。</span><span class="sxs-lookup"><span data-stu-id="2f34b-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="2f34b-105">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="2f34b-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="2f34b-106">为一个销售订单创建一张发票</span><span class="sxs-lookup"><span data-stu-id="2f34b-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="2f34b-107">转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 已装运但未开票的销售订单**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="2f34b-108">从列表中选择一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="2f34b-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="2f34b-109">在 **操作窗格** 上，单击 **发票 > 生成 > 发票**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="2f34b-110">请注意此销售订单具有多个相关的装箱单。</span><span class="sxs-lookup"><span data-stu-id="2f34b-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="2f34b-111">它将只显示单词“<multiple>”，不会显示装箱单编号。</span><span class="sxs-lookup"><span data-stu-id="2f34b-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="2f34b-112">展开 **参数** 部分。</span><span class="sxs-lookup"><span data-stu-id="2f34b-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="2f34b-113">若要过帐发票，请设定为“是”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="2f34b-114">也可以关闭过帐功能只打印发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="2f34b-115">但是您还可以通过创建形式发票代替发票，效果一样。</span><span class="sxs-lookup"><span data-stu-id="2f34b-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="2f34b-116">此选项用于批处理作业。</span><span class="sxs-lookup"><span data-stu-id="2f34b-116">This option is used for batch jobs.</span></span> <span data-ttu-id="2f34b-117">运行批处理作业，查询将会运行。</span><span class="sxs-lookup"><span data-stu-id="2f34b-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="2f34b-118">在 **打印** 字段中，选择“以后”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="2f34b-119">为 **打印发票** 选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="2f34b-120">“打印管理”可打印多个发票副本并通过电子邮件以 PDF 文档的形式发送发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="2f34b-121">在 **打印费用** 字段中，选择“汇总”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="2f34b-122">在 **检查信用额度** 字段中，选择“余额”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="2f34b-123">单击 **取消**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="2f34b-124">合并订单为一张发票</span><span class="sxs-lookup"><span data-stu-id="2f34b-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="2f34b-125">转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="2f34b-126">选定一个拥有多个发票的客户。</span><span class="sxs-lookup"><span data-stu-id="2f34b-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="2f34b-127">选择来自同一客户的多个未结销售订单。</span><span class="sxs-lookup"><span data-stu-id="2f34b-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="2f34b-128">在 **操作窗格** 上，单击 **发票 > 生成 > 发票**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="2f34b-129">展开 **参数** 部分。</span><span class="sxs-lookup"><span data-stu-id="2f34b-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="2f34b-130">在 **数量** 字段中，选择“全部”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="2f34b-131">请注意在概述部分列出的两张发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="2f34b-132">现在将两张合并为一张发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="2f34b-133">在 **汇总更新** 字段中，选择“发票帐目”。</span><span class="sxs-lookup"><span data-stu-id="2f34b-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="2f34b-134">单击 **整理** 合并这两个销售订单为一张发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="2f34b-135">两个销售订单现在合并为一张发票。</span><span class="sxs-lookup"><span data-stu-id="2f34b-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="2f34b-136">单击 **取消**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="2f34b-137">单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="2f34b-138">成批过帐发票</span><span class="sxs-lookup"><span data-stu-id="2f34b-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="2f34b-139">转至 **导航窗格 > 模块 > 应收帐款 > 发票 > 批处理开票 > 发票**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="2f34b-140">单击 **选择**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-140">Click **Select**.</span></span>
3. <span data-ttu-id="2f34b-141">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-141">Click **OK**.</span></span>
4. <span data-ttu-id="2f34b-142">单击 **批处理**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-142">Click **Batch**.</span></span>
5. <span data-ttu-id="2f34b-143">在 **批处理** 中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="2f34b-144">单击 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="2f34b-145">选择 **天**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-145">Select **Days**.</span></span>
8. <span data-ttu-id="2f34b-146">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-146">Click **OK**.</span></span>
9. <span data-ttu-id="2f34b-147">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-147">Click **OK**.</span></span>
10. <span data-ttu-id="2f34b-148">单击 **取消**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="2f34b-149">单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="2f34b-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]