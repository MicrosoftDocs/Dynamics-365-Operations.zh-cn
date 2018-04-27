--- 
title: "创建物料清单（仅 2016 年 2 月）"
description: "此任务的重点是为一件成品和一件半成品创建物料清单结构。"
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
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0cd8d9b90cffe2794b785b2bb391e21ae3b11cf7
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="268d3-103">创建物料清单（仅 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="268d3-103">Create BOMs (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="268d3-104">此任务的重点是为一件成品和一件半成品创建物料清单结构。</span><span class="sxs-lookup"><span data-stu-id="268d3-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="268d3-105">这是 BOM 计算系列中的第四个任务。</span><span class="sxs-lookup"><span data-stu-id="268d3-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="268d3-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="268d3-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="268d3-107">为一件半成品创建物料清单</span><span class="sxs-lookup"><span data-stu-id="268d3-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="268d3-108">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="268d3-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="268d3-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="268d3-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="268d3-110">选择物料编号 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="268d3-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="268d3-111">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="268d3-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="268d3-112">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="268d3-112">Click BOM versions.</span></span>
5. <span data-ttu-id="268d3-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-113">Click New.</span></span>
6. <span data-ttu-id="268d3-114">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="268d3-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="268d3-115">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="268d3-116">例如，键入 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="268d3-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="268d3-117">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-118">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="268d3-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="268d3-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-119">Click OK.</span></span>
10. <span data-ttu-id="268d3-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-120">Click New.</span></span>
11. <span data-ttu-id="268d3-121">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="268d3-122">在这个例子中，输入“ITEM_C”。</span><span class="sxs-lookup"><span data-stu-id="268d3-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="268d3-123">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-124">在这个例子中，请输入或选择“11”.</span><span class="sxs-lookup"><span data-stu-id="268d3-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="268d3-125">单击“单头”。</span><span class="sxs-lookup"><span data-stu-id="268d3-125">Click Header.</span></span>
14. <span data-ttu-id="268d3-126">单击"审核"审核物料清单。</span><span class="sxs-lookup"><span data-stu-id="268d3-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="268d3-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-127">Click OK.</span></span>
16. <span data-ttu-id="268d3-128">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="268d3-128">Click Approve.</span></span>
    * <span data-ttu-id="268d3-129">"审核"按钮位于工具栏中“BOM 版本”部分内。</span><span class="sxs-lookup"><span data-stu-id="268d3-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="268d3-130">如果未显示，请单击“物料清单”页面右上角的页眉显示“审核”。</span><span class="sxs-lookup"><span data-stu-id="268d3-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="268d3-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-131">Click OK.</span></span>
18. <span data-ttu-id="268d3-132">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="268d3-132">Click Activate.</span></span>
19. <span data-ttu-id="268d3-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-133">Close the page.</span></span>
20. <span data-ttu-id="268d3-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-134">Close the page.</span></span>
21. <span data-ttu-id="268d3-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="268d3-136">为一件成品创建物料清单</span><span class="sxs-lookup"><span data-stu-id="268d3-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="268d3-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="268d3-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="268d3-138">选择物料编号 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="268d3-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="268d3-139">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="268d3-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="268d3-140">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="268d3-140">Click BOM versions.</span></span>
4. <span data-ttu-id="268d3-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-141">Click New.</span></span>
5. <span data-ttu-id="268d3-142">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="268d3-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="268d3-143">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="268d3-144">例如，键入 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="268d3-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="268d3-145">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-146">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="268d3-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="268d3-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-147">Click OK.</span></span>
9. <span data-ttu-id="268d3-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-148">Click New.</span></span>
10. <span data-ttu-id="268d3-149">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="268d3-150">在这个例子中，输入 ITEM_A。</span><span class="sxs-lookup"><span data-stu-id="268d3-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="268d3-151">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-152">在这个例子中选择“11”。</span><span class="sxs-lookup"><span data-stu-id="268d3-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="268d3-153">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-153">Click New.</span></span>
13. <span data-ttu-id="268d3-154">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="268d3-155">在这个例子中，输入“ITEM_B”。</span><span class="sxs-lookup"><span data-stu-id="268d3-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="268d3-156">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-157">在这个例子中，请输入或选择“11”.</span><span class="sxs-lookup"><span data-stu-id="268d3-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="268d3-158">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="268d3-158">Click New.</span></span>
16. <span data-ttu-id="268d3-159">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="268d3-160">在这个例子中，输入“BOM_2”。</span><span class="sxs-lookup"><span data-stu-id="268d3-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="268d3-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="268d3-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="268d3-162">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="268d3-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="268d3-163">在这个例子中，请输入或选择“仓库 11”.</span><span class="sxs-lookup"><span data-stu-id="268d3-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="268d3-164">单击“单头”。</span><span class="sxs-lookup"><span data-stu-id="268d3-164">Click Header.</span></span>
20. <span data-ttu-id="268d3-165">单击"审核"审核物料清单。</span><span class="sxs-lookup"><span data-stu-id="268d3-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="268d3-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-166">Click OK.</span></span>
22. <span data-ttu-id="268d3-167">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="268d3-167">Click Approve.</span></span>
    * <span data-ttu-id="268d3-168">"审核"按钮位于工具栏中“BOM 版本”部分内。</span><span class="sxs-lookup"><span data-stu-id="268d3-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="268d3-169">如果未显示，请单击“物料清单”页面右上角的页眉显示“审核”。</span><span class="sxs-lookup"><span data-stu-id="268d3-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="268d3-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="268d3-170">Click OK.</span></span>
24. <span data-ttu-id="268d3-171">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="268d3-171">Click Activate.</span></span>
25. <span data-ttu-id="268d3-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-172">Close the page.</span></span>
26. <span data-ttu-id="268d3-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-173">Close the page.</span></span>
27. <span data-ttu-id="268d3-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="268d3-174">Close the page.</span></span>


