--- 
title: "创建工艺路线（仅 2016 年 2 月）"
description: "此任务的重点是为一件成品和一件半成品创建生产工艺路线。"
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
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="70a8b-103">创建工艺路线（仅 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="70a8b-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70a8b-104">此任务的重点是为一件成品和一件半成品创建生产工艺路线。</span><span class="sxs-lookup"><span data-stu-id="70a8b-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="70a8b-105">这是 BOM 计算系列中的第五个任务。</span><span class="sxs-lookup"><span data-stu-id="70a8b-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="70a8b-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="70a8b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="70a8b-107">为一件半成品创建工艺路线</span><span class="sxs-lookup"><span data-stu-id="70a8b-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="70a8b-108">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="70a8b-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="70a8b-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="70a8b-110">选择物料编号 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="70a8b-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="70a8b-111">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="70a8b-112">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-112">Click Route.</span></span>
5. <span data-ttu-id="70a8b-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-113">Click New.</span></span>
6. <span data-ttu-id="70a8b-114">单击“工艺路线”和“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-114">Click Route and route version.</span></span>
7. <span data-ttu-id="70a8b-115">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="70a8b-116">例如，键入“ROUTE_2”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="70a8b-117">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-118">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="70a8b-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="70a8b-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-119">Click OK.</span></span>
10. <span data-ttu-id="70a8b-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-120">Click New.</span></span>
11. <span data-ttu-id="70a8b-121">在“运营”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-122">在这个例子中，选择“组装件”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="70a8b-123">在“运行时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="70a8b-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="70a8b-124">例如，键入“1”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-124">For example, type 1.</span></span> <span data-ttu-id="70a8b-125">运行时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="70a8b-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="70a8b-126">在“路线组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-127">在这个例子中，选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="70a8b-128">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="70a8b-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="70a8b-129">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-130">在这个例子中，选择“组装件”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="70a8b-131">单击“时间”选项卡。</span><span class="sxs-lookup"><span data-stu-id="70a8b-131">Click the Times tab.</span></span>
17. <span data-ttu-id="70a8b-132">在“设置时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="70a8b-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="70a8b-133">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="70a8b-133">For this example, type 1.</span></span> <span data-ttu-id="70a8b-134">设置时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="70a8b-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="70a8b-135">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="70a8b-136">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-136">Click Approve.</span></span>
20. <span data-ttu-id="70a8b-137">在“是否还要审核该工艺路线?“字段中选择”是“。</span><span class="sxs-lookup"><span data-stu-id="70a8b-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="70a8b-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-138">Click OK.</span></span>
22. <span data-ttu-id="70a8b-139">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="70a8b-140">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-140">Click Activate.</span></span>
24. <span data-ttu-id="70a8b-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="70a8b-141">Close the page.</span></span>
25. <span data-ttu-id="70a8b-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="70a8b-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="70a8b-143">创建成品的工艺路线</span><span class="sxs-lookup"><span data-stu-id="70a8b-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="70a8b-144">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="70a8b-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="70a8b-145">选择物料编号 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="70a8b-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="70a8b-146">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="70a8b-147">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-147">Click Route.</span></span>
4. <span data-ttu-id="70a8b-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-148">Click New.</span></span>
5. <span data-ttu-id="70a8b-149">单击“工艺路线”和“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-149">Click Route and route version.</span></span>
6. <span data-ttu-id="70a8b-150">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="70a8b-151">在这个例子中，键入“ROUTE_1”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="70a8b-152">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-153">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="70a8b-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="70a8b-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-154">Click OK.</span></span>
9. <span data-ttu-id="70a8b-155">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-155">Click New.</span></span>
10. <span data-ttu-id="70a8b-156">在“运营”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-157">在这个例子中，选择“包装”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="70a8b-158">在“运行时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="70a8b-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="70a8b-159">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="70a8b-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="70a8b-160">在“路线组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-161">在这个例子中，选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="70a8b-162">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="70a8b-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="70a8b-163">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="70a8b-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="70a8b-164">在这个例子中，选择“包装”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="70a8b-165">单击“时间”选项卡。</span><span class="sxs-lookup"><span data-stu-id="70a8b-165">Click the Times tab.</span></span>
16. <span data-ttu-id="70a8b-166">在“设置时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="70a8b-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="70a8b-167">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="70a8b-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="70a8b-168">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="70a8b-169">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-169">Click Approve.</span></span>
19. <span data-ttu-id="70a8b-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-170">Click OK.</span></span>
20. <span data-ttu-id="70a8b-171">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="70a8b-172">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-172">Click Activate.</span></span>
22. <span data-ttu-id="70a8b-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="70a8b-173">Close the page.</span></span>
23. <span data-ttu-id="70a8b-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="70a8b-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="70a8b-175">启用自动消耗设置时间</span><span class="sxs-lookup"><span data-stu-id="70a8b-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="70a8b-176">转到“生产控制 > 设置 > 工艺路线 > 工艺路线组”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="70a8b-177">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="70a8b-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="70a8b-178">选择列表中的“标准”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="70a8b-179">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-179">Click Edit.</span></span>
4. <span data-ttu-id="70a8b-180">在“设置时间”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="70a8b-181">设置时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="70a8b-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="70a8b-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="70a8b-182">Click Save.</span></span>
6. <span data-ttu-id="70a8b-183">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="70a8b-183">Close the page.</span></span>


