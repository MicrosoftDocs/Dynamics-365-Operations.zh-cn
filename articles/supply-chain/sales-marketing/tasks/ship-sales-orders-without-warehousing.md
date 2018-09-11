--- 
title: "装运无仓库的销售订单"
description: "本指南演示在将产品发运给客户时如何更新销售订单。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1d4d43ca62901ecd2280f21dfbeee9cb70ec600e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="6b0a0-103">装运无仓库的销售订单</span><span class="sxs-lookup"><span data-stu-id="6b0a0-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b0a0-104">本指南演示在将产品发运给客户时如何更新销售订单。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="6b0a0-105">本指南适用于没有为仓库管理设置的履行流程（不论是基本还是高级仓库），因而不需要在装运前登记产品领料。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="6b0a0-106">您可以使用演示数据公司 USMF 或您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="6b0a0-107">在这两种情况下，在您开始此任务前，为数量大于 1 的库存产品创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="6b0a0-108">为了避免过帐错误，您需要检查您在订单上选择的站点和仓库中产品的现有数量包含订单数量。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="6b0a0-109">过帐订单的装箱单</span><span class="sxs-lookup"><span data-stu-id="6b0a0-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="6b0a0-110">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6b0a0-111">在列表中，查找并选择您为此任务创建的订单。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="6b0a0-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6b0a0-113">在操作窗格，单击“领料和装箱”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="6b0a0-114">单击“发布装箱单”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="6b0a0-115">展开或收起“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="6b0a0-116">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="6b0a0-117">其他选项包括“现在交货”和“领料”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="6b0a0-118">如果订单行将部分交货，且订单行上的“现在交货”字段列有数量，您可以选择“现在交货”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="6b0a0-119">如果在您公司的订单履行流程中，领料作为单独的流程并根据领料单管理和登记，您可以选择“领料”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="6b0a0-120">确认“过帐”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="6b0a0-121">将“打印装箱单”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="6b0a0-122">“概览”选项卡包含在此过帐中生成的装箱单的列表。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="6b0a0-123">如果您装运单个订单，通常只有一个装箱单。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="6b0a0-124">但是，如果从不同站点装运订单行，过帐将自动拆分成相应的单据数。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="6b0a0-125">这是强制性的，不可更改。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="6b0a0-126">同样，如果订单行装运到不同的交货地址，且装运政策设置为需要拆分，过帐将会拆分成多个单据。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="6b0a0-127">在“行”选项卡上，选择要装运的订单行上的行。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="6b0a0-128">在“更新”字段中，输入小于原始数量的数字。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="6b0a0-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-129">Click OK.</span></span>
12. <span data-ttu-id="6b0a0-130">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-130">Click Yes.</span></span>
13. <span data-ttu-id="6b0a0-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-131">Close the page.</span></span>
14. <span data-ttu-id="6b0a0-132">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="6b0a0-133">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-133">Click Change view.</span></span>
16. <span data-ttu-id="6b0a0-134">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-134">Click Header view.</span></span>
    * <span data-ttu-id="6b0a0-135">如果订单上的所有行已全部装运，则订单状态从“未结”更改为“已交货”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="6b0a0-136">在此示例中，订单行已部分装运。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="6b0a0-137">这就是订单仍处于未结状态的原因。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="6b0a0-138">由于至少有一个订单行已装运，“单据状态”字段设置为“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="6b0a0-139">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="6b0a0-140">单击“行数量”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-140">Click Line quantity.</span></span>
19. <span data-ttu-id="6b0a0-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-141">Close the page.</span></span>
20. <span data-ttu-id="6b0a0-142">在操作窗格中，单击“领料和装箱”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="6b0a0-143">单击“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-143">Click Packing slip.</span></span>
    * <span data-ttu-id="6b0a0-144">“装箱单日记帐”页含有您的订单生成的所有装箱单单据。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="6b0a0-145">您可以在想要时查看并打印每个单据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6b0a0-145">You can review details of each document and print them, if you wish.</span></span>  


