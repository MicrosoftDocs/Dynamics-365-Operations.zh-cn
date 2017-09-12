--- 
title: "创建原材料（仅 2016 年 2 月）"
description: "此任务的重点是创建成品和半成品的组件。"
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="12626-103">创建原材料（仅 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="12626-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12626-104">此任务的重点是创建成品和半成品的组件。</span><span class="sxs-lookup"><span data-stu-id="12626-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="12626-105">这是 BOM 计算系列中的第三个任务。</span><span class="sxs-lookup"><span data-stu-id="12626-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="12626-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="12626-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="12626-107">创建第一个材料</span><span class="sxs-lookup"><span data-stu-id="12626-107">Create the first material</span></span>
1. <span data-ttu-id="12626-108">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="12626-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="12626-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-109">Click New.</span></span>
3. <span data-ttu-id="12626-110">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="12626-111">在这个例子中，输入“ITEM_A”。</span><span class="sxs-lookup"><span data-stu-id="12626-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="12626-112">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-113">选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="12626-113">Select STD.</span></span> <span data-ttu-id="12626-114">“标准”指的是标准成本，是计算成本时最常用的模型。</span><span class="sxs-lookup"><span data-stu-id="12626-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="12626-115">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-116">例如，选择“音频”。</span><span class="sxs-lookup"><span data-stu-id="12626-116">For example, select Audio.</span></span> <span data-ttu-id="12626-117">这不影响成本计算。</span><span class="sxs-lookup"><span data-stu-id="12626-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="12626-118">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-119">选择“SiteWH”。</span><span class="sxs-lookup"><span data-stu-id="12626-119">Select SiteWH.</span></span> <span data-ttu-id="12626-120">将对此演示仅使用站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="12626-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="12626-121">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-122">将不对此示例使用跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="12626-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="12626-123">选择“无”。</span><span class="sxs-lookup"><span data-stu-id="12626-123">Select None.</span></span>  
8. <span data-ttu-id="12626-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="12626-124">Click OK.</span></span>
9. <span data-ttu-id="12626-125">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="12626-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="12626-126">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="12626-126">Click Default order settings.</span></span>
11. <span data-ttu-id="12626-127">在“采购站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-128">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="12626-129">在“库存站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-130">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="12626-131">在“销售站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-132">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="12626-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-133">Close the page.</span></span>
15. <span data-ttu-id="12626-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-134">Close the page.</span></span>
16. <span data-ttu-id="12626-135">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12626-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="12626-136">单击“ITEM_A”。</span><span class="sxs-lookup"><span data-stu-id="12626-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="12626-137">展开“管理成本”部分。</span><span class="sxs-lookup"><span data-stu-id="12626-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="12626-138">在“成本组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="12626-139">在这个例子中，输入“M2”。</span><span class="sxs-lookup"><span data-stu-id="12626-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="12626-140">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="12626-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="12626-141">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-141">Click Item price.</span></span>
21. <span data-ttu-id="12626-142">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-142">Click New.</span></span>
22. <span data-ttu-id="12626-143">在“版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-144">对于此示例，请选择“10”，这是标准成本成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="12626-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="12626-145">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-146">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="12626-147">在“价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="12626-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="12626-148">在这个例子中，输入“10”。</span><span class="sxs-lookup"><span data-stu-id="12626-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="12626-149">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12626-149">Click Save.</span></span>
26. <span data-ttu-id="12626-150">单击“激活未决价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="12626-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-151">Close the page.</span></span>
28. <span data-ttu-id="12626-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="12626-153">创建第二个材料</span><span class="sxs-lookup"><span data-stu-id="12626-153">Create the second material</span></span>
1. <span data-ttu-id="12626-154">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-154">Click New.</span></span>
2. <span data-ttu-id="12626-155">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="12626-156">在这个例子中，输入“ITEM_B”。</span><span class="sxs-lookup"><span data-stu-id="12626-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="12626-157">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-158">选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="12626-158">Select STD.</span></span> <span data-ttu-id="12626-159">“标准”指的是标准成本，是计算成本时最常用的模型。</span><span class="sxs-lookup"><span data-stu-id="12626-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="12626-160">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-161">例如，选择“音频”。</span><span class="sxs-lookup"><span data-stu-id="12626-161">For example, select Audio.</span></span> <span data-ttu-id="12626-162">这不影响成本计算。</span><span class="sxs-lookup"><span data-stu-id="12626-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="12626-163">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-164">选择“SiteWH”。</span><span class="sxs-lookup"><span data-stu-id="12626-164">Select SiteWH.</span></span> <span data-ttu-id="12626-165">将对此示例仅使用站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="12626-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="12626-166">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-167">将不对此示例使用跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="12626-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="12626-168">选择“无”。</span><span class="sxs-lookup"><span data-stu-id="12626-168">Select None.</span></span>  
7. <span data-ttu-id="12626-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="12626-169">Click OK.</span></span>
8. <span data-ttu-id="12626-170">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="12626-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="12626-171">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="12626-171">Click Default order settings.</span></span>
10. <span data-ttu-id="12626-172">在“采购站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-173">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="12626-174">在“库存站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-175">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="12626-176">在“销售站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-177">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="12626-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-178">Close the page.</span></span>
14. <span data-ttu-id="12626-179">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-179">Close the page.</span></span>
15. <span data-ttu-id="12626-180">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12626-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="12626-181">单击“ITEM_B”。</span><span class="sxs-lookup"><span data-stu-id="12626-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="12626-182">展开“管理成本”部分。</span><span class="sxs-lookup"><span data-stu-id="12626-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="12626-183">在“成本组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="12626-184">在这个例子中，输入“M2”。</span><span class="sxs-lookup"><span data-stu-id="12626-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="12626-185">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="12626-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="12626-186">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-186">Click Item price.</span></span>
20. <span data-ttu-id="12626-187">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-187">Click New.</span></span>
21. <span data-ttu-id="12626-188">在“版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-189">在这个例子中选择“10”。</span><span class="sxs-lookup"><span data-stu-id="12626-189">For this example, select 10.</span></span> <span data-ttu-id="12626-190">这是标准成本成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="12626-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="12626-191">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-192">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="12626-193">在“价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="12626-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="12626-194">对于此演示，输入“10”。</span><span class="sxs-lookup"><span data-stu-id="12626-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="12626-195">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12626-195">Click Save.</span></span>
25. <span data-ttu-id="12626-196">单击“激活未决价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="12626-197">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-197">Close the page.</span></span>
27. <span data-ttu-id="12626-198">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="12626-199">创建第三个材料</span><span class="sxs-lookup"><span data-stu-id="12626-199">Create the third material</span></span>
1. <span data-ttu-id="12626-200">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-200">Click New.</span></span>
2. <span data-ttu-id="12626-201">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="12626-202">对于此演示，输入“ITEM_C”</span><span class="sxs-lookup"><span data-stu-id="12626-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="12626-203">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-204">选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="12626-204">Select STD.</span></span> <span data-ttu-id="12626-205">“标准”指的是标准成本，是计算成本时最常用的模型。</span><span class="sxs-lookup"><span data-stu-id="12626-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="12626-206">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-207">例如，选择“音频”。</span><span class="sxs-lookup"><span data-stu-id="12626-207">For example, select Audio.</span></span> <span data-ttu-id="12626-208">这不影响成本计算。</span><span class="sxs-lookup"><span data-stu-id="12626-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="12626-209">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-210">选择“SiteWH”。</span><span class="sxs-lookup"><span data-stu-id="12626-210">Select SiteWH.</span></span> <span data-ttu-id="12626-211">将对此演示仅使用站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="12626-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="12626-212">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-213">将不对此示例使用跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="12626-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="12626-214">选择“无”。</span><span class="sxs-lookup"><span data-stu-id="12626-214">Select None.</span></span>  
7. <span data-ttu-id="12626-215">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="12626-215">Click OK.</span></span>
8. <span data-ttu-id="12626-216">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="12626-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="12626-217">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="12626-217">Click Default order settings.</span></span>
10. <span data-ttu-id="12626-218">在“采购站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-219">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="12626-220">在“库存站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-221">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="12626-222">在“销售站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-223">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="12626-224">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-224">Close the page.</span></span>
14. <span data-ttu-id="12626-225">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-225">Close the page.</span></span>
15. <span data-ttu-id="12626-226">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12626-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="12626-227">单击“ITEM_C”。</span><span class="sxs-lookup"><span data-stu-id="12626-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="12626-228">展开“管理成本”部分。</span><span class="sxs-lookup"><span data-stu-id="12626-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="12626-229">在“成本组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="12626-230">在这个例子中，输入“M1”。</span><span class="sxs-lookup"><span data-stu-id="12626-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="12626-231">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="12626-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="12626-232">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-232">Click Item price.</span></span>
20. <span data-ttu-id="12626-233">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12626-233">Click New.</span></span>
21. <span data-ttu-id="12626-234">在“版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-235">在这个例子中选择“10”。</span><span class="sxs-lookup"><span data-stu-id="12626-235">For this example, select 10.</span></span> <span data-ttu-id="12626-236">这是标准成本成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="12626-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="12626-237">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="12626-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="12626-238">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="12626-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="12626-239">在“价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="12626-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="12626-240">在这个例子中，输入“10”。</span><span class="sxs-lookup"><span data-stu-id="12626-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="12626-241">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12626-241">Click Save.</span></span>
25. <span data-ttu-id="12626-242">单击“激活未决价格”。</span><span class="sxs-lookup"><span data-stu-id="12626-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="12626-243">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-243">Close the page.</span></span>
27. <span data-ttu-id="12626-244">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12626-244">Close the page.</span></span>


