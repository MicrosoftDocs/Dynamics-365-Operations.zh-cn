---
title: 装运无仓库的销售订单
description: 此主题介绍在将产品发运给客户时如何更新销售订单。
author: omulvad
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bd59a16d0fc1cde6e83bd51d1eaf82da7bf26d9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819152"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="09223-103">装运无仓库的销售订单</span><span class="sxs-lookup"><span data-stu-id="09223-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09223-104">此主题介绍在将产品发运给客户时如何更新销售订单。</span><span class="sxs-lookup"><span data-stu-id="09223-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="09223-105">本指南适用于没有为仓库管理设置的履行流程（不论是基本还是高级仓库），因而不需要在装运前登记产品领料。</span><span class="sxs-lookup"><span data-stu-id="09223-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="09223-106">您可以使用演示数据公司 USMF 或您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="09223-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="09223-107">在这两种情况下，在您开始此任务前，为数量大于 1 的库存产品创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="09223-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="09223-108">为了避免过帐错误，您需要检查您在订单上选择的站点和仓库中产品的现有数量包含订单数量。</span><span class="sxs-lookup"><span data-stu-id="09223-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="09223-109">过帐订单的装箱单</span><span class="sxs-lookup"><span data-stu-id="09223-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="09223-110">在导航窗格中，转到 **模块 > 销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="09223-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="09223-111">在列表中，查找并选择您为此任务创建的订单。</span><span class="sxs-lookup"><span data-stu-id="09223-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="09223-112">在操作窗格中，选择 **领料和装箱**。</span><span class="sxs-lookup"><span data-stu-id="09223-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="09223-113">选择 **将装箱单过帐**。</span><span class="sxs-lookup"><span data-stu-id="09223-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="09223-114">展开或收起 **参数** 部分。</span><span class="sxs-lookup"><span data-stu-id="09223-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="09223-115">在 **数量** 字段中，选择 **全部**。</span><span class="sxs-lookup"><span data-stu-id="09223-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="09223-116">其他选项包括 **现在交货** 和 **领料**。</span><span class="sxs-lookup"><span data-stu-id="09223-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="09223-117">如果订单行将部分交货，且订单行上的 **现在交货** 字段列有数量，您可以选择 **现在交货**。</span><span class="sxs-lookup"><span data-stu-id="09223-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="09223-118">如果在您公司的订单履行流程中，领料作为单独的流程并根据领料单管理和登记，您可以选择 **领料**。</span><span class="sxs-lookup"><span data-stu-id="09223-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="09223-119">确认 **过帐** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="09223-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="09223-120">将 **打印装箱单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="09223-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="09223-121">**概览** 选项卡包含在此过帐中生成的装箱单的列表。</span><span class="sxs-lookup"><span data-stu-id="09223-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="09223-122">如果您装运单个订单，通常只有一个装箱单。</span><span class="sxs-lookup"><span data-stu-id="09223-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="09223-123">但是，如果从不同站点装运订单行，过帐将自动拆分成相应的单据数。</span><span class="sxs-lookup"><span data-stu-id="09223-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="09223-124">这是强制性的，不可更改。</span><span class="sxs-lookup"><span data-stu-id="09223-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="09223-125">同样，如果订单行装运到不同的交货地址，且装运政策设置为需要拆分，过帐将会拆分成多个单据。</span><span class="sxs-lookup"><span data-stu-id="09223-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="09223-126">在 **行** 选项卡上，选择要装运的订单行上的行。</span><span class="sxs-lookup"><span data-stu-id="09223-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="09223-127">在 **更新** 字段中，输入小于原始数量的数字。</span><span class="sxs-lookup"><span data-stu-id="09223-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="09223-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="09223-128">Select **OK**.</span></span>
11. <span data-ttu-id="09223-129">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="09223-129">Select **Yes**.</span></span>
12. <span data-ttu-id="09223-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="09223-130">Close the page.</span></span>
13. <span data-ttu-id="09223-131">在操作窗格上，选择 **选项**。</span><span class="sxs-lookup"><span data-stu-id="09223-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="09223-132">选择 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="09223-132">Select **Change view**.</span></span>
15. <span data-ttu-id="09223-133">选择 **标题视图**。</span><span class="sxs-lookup"><span data-stu-id="09223-133">Select **Header view**.</span></span>
    - <span data-ttu-id="09223-134">如果订单上的所有行已全部装运，则订单状态从“未结”更改为“已交货”。</span><span class="sxs-lookup"><span data-stu-id="09223-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="09223-135">在此示例中，订单行已部分装运。</span><span class="sxs-lookup"><span data-stu-id="09223-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="09223-136">这就是订单仍处于未结状态的原因。</span><span class="sxs-lookup"><span data-stu-id="09223-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="09223-137">由于至少有一个订单行已装运，**单据状态** 字段设置为“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="09223-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="09223-138">在操作窗格上，选择 **常规**。</span><span class="sxs-lookup"><span data-stu-id="09223-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="09223-139">选择 **行数量**。</span><span class="sxs-lookup"><span data-stu-id="09223-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="09223-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="09223-140">Close the page.</span></span>
19. <span data-ttu-id="09223-141">在操作窗格中，选择 **领料和装箱**。</span><span class="sxs-lookup"><span data-stu-id="09223-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="09223-142">选择 **装箱单**。</span><span class="sxs-lookup"><span data-stu-id="09223-142">Select **Packing slip**.</span></span> <span data-ttu-id="09223-143">**装箱单日记帐** 页含有您的订单生成的所有装箱单单据。</span><span class="sxs-lookup"><span data-stu-id="09223-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="09223-144">您可以在想要时查看并打印每个单据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="09223-144">You can review details of each document and print them, if you wish.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]