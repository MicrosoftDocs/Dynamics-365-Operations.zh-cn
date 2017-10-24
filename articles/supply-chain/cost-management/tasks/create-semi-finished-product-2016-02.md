--- 
title: "创建半成品（仅 2016 年 2 月）"
description: "此任务的重点是创建半成品。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4d06f291036c656731a00fcf312e229ed9e9f3d0
ms.openlocfilehash: 038d8cd9333635d3269bb4f62a5402c2309bfd3c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="c3197-103">创建半成品（仅 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="c3197-103">Create a semi-finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3197-104">此任务的重点是创建半成品。</span><span class="sxs-lookup"><span data-stu-id="c3197-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="c3197-105">这是 BOM 计算系列中的第二个任务。</span><span class="sxs-lookup"><span data-stu-id="c3197-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="c3197-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="c3197-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="c3197-107">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="c3197-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c3197-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c3197-108">Click New.</span></span>
3. <span data-ttu-id="c3197-109">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c3197-110">在这个例子中，输入“BOM_2”。</span><span class="sxs-lookup"><span data-stu-id="c3197-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="c3197-111">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-112">选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="c3197-112">Select STD.</span></span> <span data-ttu-id="c3197-113">“标准”指的是标准成本，是计算成本时最常用的模型。</span><span class="sxs-lookup"><span data-stu-id="c3197-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="c3197-114">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-115">例如，选择“音频”。</span><span class="sxs-lookup"><span data-stu-id="c3197-115">For example, select Audio.</span></span> <span data-ttu-id="c3197-116">这不影响成本计算。</span><span class="sxs-lookup"><span data-stu-id="c3197-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="c3197-117">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-118">选择“SiteWH”。</span><span class="sxs-lookup"><span data-stu-id="c3197-118">Select SiteWH.</span></span> <span data-ttu-id="c3197-119">将对此示例仅使用站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="c3197-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="c3197-120">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-121">将不对此示例使用跟踪维度。请选择"无"。</span><span class="sxs-lookup"><span data-stu-id="c3197-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="c3197-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c3197-122">Click OK.</span></span>
9. <span data-ttu-id="c3197-123">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="c3197-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="c3197-124">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="c3197-124">Click Default order settings.</span></span>
11. <span data-ttu-id="c3197-125">在“默认订单类型”字段中，选择“生产”。</span><span class="sxs-lookup"><span data-stu-id="c3197-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="c3197-126">因为这是将生产的半成品，所以请选择“生产”。</span><span class="sxs-lookup"><span data-stu-id="c3197-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="c3197-127">在“采购站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-128">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="c3197-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c3197-129">在“库存站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-130">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="c3197-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="c3197-131">在“销售站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-132">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="c3197-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="c3197-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c3197-133">Close the page.</span></span>
16. <span data-ttu-id="c3197-134">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="c3197-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="c3197-135">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="c3197-135">Click Item price.</span></span>
18. <span data-ttu-id="c3197-136">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c3197-136">Click New.</span></span>
19. <span data-ttu-id="c3197-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c3197-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="c3197-138">在“版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-139">在这个例子中选择“版本 10”。</span><span class="sxs-lookup"><span data-stu-id="c3197-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="c3197-140">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-141">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="c3197-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="c3197-142">将“价格”设为“10”。</span><span class="sxs-lookup"><span data-stu-id="c3197-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="c3197-143">对于此示例，请输入成本价 10。</span><span class="sxs-lookup"><span data-stu-id="c3197-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="c3197-144">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c3197-144">Click Save.</span></span>
24. <span data-ttu-id="c3197-145">单击“激活未决价格”。</span><span class="sxs-lookup"><span data-stu-id="c3197-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="c3197-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c3197-146">Close the page.</span></span>
26. <span data-ttu-id="c3197-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c3197-147">Close the page.</span></span>
27. <span data-ttu-id="c3197-148">单击“BOM_2”将其打开。</span><span class="sxs-lookup"><span data-stu-id="c3197-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="c3197-149">展开“管理成本”部分。</span><span class="sxs-lookup"><span data-stu-id="c3197-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="c3197-150">在“成本组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c3197-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="c3197-151">在这个例子中，选择“成本组 M1”。</span><span class="sxs-lookup"><span data-stu-id="c3197-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="c3197-152">使用保存记录的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="c3197-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="c3197-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c3197-153">Close the page.</span></span>


