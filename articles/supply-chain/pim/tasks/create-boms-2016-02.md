--- 
title: "创建 BOM（2016 年 2 月）"
description: "此任务的重点是为一件成品和一件半成品创建物料清单结构。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="d841b-103">创建 BOM（2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="d841b-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d841b-104">此任务的重点是为一件成品和一件半成品创建物料清单结构。</span><span class="sxs-lookup"><span data-stu-id="d841b-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="d841b-105">这是 BOM 计算系列中的第四个任务。</span><span class="sxs-lookup"><span data-stu-id="d841b-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="d841b-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="d841b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="d841b-107">为一件半成品创建物料清单</span><span class="sxs-lookup"><span data-stu-id="d841b-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="d841b-108">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="d841b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d841b-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d841b-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d841b-110">选择物料编号 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="d841b-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="d841b-111">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="d841b-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="d841b-112">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="d841b-112">Click BOM versions.</span></span>
5. <span data-ttu-id="d841b-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-113">Click New.</span></span>
6. <span data-ttu-id="d841b-114">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="d841b-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="d841b-115">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d841b-116">例如，键入 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="d841b-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="d841b-117">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-118">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="d841b-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="d841b-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-119">Click OK.</span></span>
10. <span data-ttu-id="d841b-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-120">Click New.</span></span>
11. <span data-ttu-id="d841b-121">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d841b-122">在这个例子中，输入“ITEM_C”。</span><span class="sxs-lookup"><span data-stu-id="d841b-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="d841b-123">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-124">在这个例子中，请输入或选择“11”.</span><span class="sxs-lookup"><span data-stu-id="d841b-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="d841b-125">单击“单头”。</span><span class="sxs-lookup"><span data-stu-id="d841b-125">Click Header.</span></span>
14. <span data-ttu-id="d841b-126">单击"审核"审核物料清单。</span><span class="sxs-lookup"><span data-stu-id="d841b-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="d841b-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-127">Click OK.</span></span>
16. <span data-ttu-id="d841b-128">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="d841b-128">Click Approve.</span></span>
    * <span data-ttu-id="d841b-129">"审核"按钮位于工具栏中“BOM 版本”部分内。</span><span class="sxs-lookup"><span data-stu-id="d841b-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d841b-130">如果未显示，请单击“物料清单”页面右上角的页眉显示“审核”。</span><span class="sxs-lookup"><span data-stu-id="d841b-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="d841b-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-131">Click OK.</span></span>
18. <span data-ttu-id="d841b-132">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="d841b-132">Click Activate.</span></span>
19. <span data-ttu-id="d841b-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-133">Close the page.</span></span>
20. <span data-ttu-id="d841b-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-134">Close the page.</span></span>
21. <span data-ttu-id="d841b-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="d841b-136">为一件成品创建物料清单</span><span class="sxs-lookup"><span data-stu-id="d841b-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="d841b-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d841b-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d841b-138">选择物料编号 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="d841b-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="d841b-139">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="d841b-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="d841b-140">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="d841b-140">Click BOM versions.</span></span>
4. <span data-ttu-id="d841b-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-141">Click New.</span></span>
5. <span data-ttu-id="d841b-142">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="d841b-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="d841b-143">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d841b-144">例如，键入 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="d841b-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="d841b-145">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-146">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="d841b-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="d841b-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-147">Click OK.</span></span>
9. <span data-ttu-id="d841b-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-148">Click New.</span></span>
10. <span data-ttu-id="d841b-149">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d841b-150">在这个例子中，输入 ITEM_A。</span><span class="sxs-lookup"><span data-stu-id="d841b-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="d841b-151">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-152">在这个例子中选择“11”。</span><span class="sxs-lookup"><span data-stu-id="d841b-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="d841b-153">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-153">Click New.</span></span>
13. <span data-ttu-id="d841b-154">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d841b-155">在这个例子中，输入“ITEM_B”。</span><span class="sxs-lookup"><span data-stu-id="d841b-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="d841b-156">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-157">在这个例子中，请输入或选择“11”.</span><span class="sxs-lookup"><span data-stu-id="d841b-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="d841b-158">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d841b-158">Click New.</span></span>
16. <span data-ttu-id="d841b-159">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d841b-160">在这个例子中，输入“BOM_2”。</span><span class="sxs-lookup"><span data-stu-id="d841b-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="d841b-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d841b-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="d841b-162">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d841b-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d841b-163">在这个例子中，请输入或选择“仓库 11”.</span><span class="sxs-lookup"><span data-stu-id="d841b-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="d841b-164">单击“单头”。</span><span class="sxs-lookup"><span data-stu-id="d841b-164">Click Header.</span></span>
20. <span data-ttu-id="d841b-165">单击"审核"审核物料清单。</span><span class="sxs-lookup"><span data-stu-id="d841b-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="d841b-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-166">Click OK.</span></span>
22. <span data-ttu-id="d841b-167">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="d841b-167">Click Approve.</span></span>
    * <span data-ttu-id="d841b-168">"审核"按钮位于工具栏中“BOM 版本”部分内。</span><span class="sxs-lookup"><span data-stu-id="d841b-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d841b-169">如果未显示，请单击“物料清单”页面右上角的页眉显示“审核”。</span><span class="sxs-lookup"><span data-stu-id="d841b-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="d841b-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d841b-170">Click OK.</span></span>
24. <span data-ttu-id="d841b-171">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="d841b-171">Click Activate.</span></span>
25. <span data-ttu-id="d841b-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-172">Close the page.</span></span>
26. <span data-ttu-id="d841b-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-173">Close the page.</span></span>
27. <span data-ttu-id="d841b-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d841b-174">Close the page.</span></span>


