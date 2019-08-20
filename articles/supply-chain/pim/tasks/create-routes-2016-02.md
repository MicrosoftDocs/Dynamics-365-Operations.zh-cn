---
title: 创建工艺路线（2016 年 2 月）
description: 此任务的重点是为一件成品和一件半成品创建生产工艺路线。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844553"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="b2bcb-103">创建工艺路线（2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="b2bcb-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2bcb-104">此任务的重点是为一件成品和一件半成品创建生产工艺路线。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="b2bcb-105">这是 BOM 计算系列中的第五个任务。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="b2bcb-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="b2bcb-107">为一件半成品创建工艺路线</span><span class="sxs-lookup"><span data-stu-id="b2bcb-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="b2bcb-108">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b2bcb-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2bcb-110">选择物料编号 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="b2bcb-111">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="b2bcb-112">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-112">Click Route.</span></span>
5. <span data-ttu-id="b2bcb-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-113">Click New.</span></span>
6. <span data-ttu-id="b2bcb-114">单击“工艺路线”和“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-114">Click Route and route version.</span></span>
7. <span data-ttu-id="b2bcb-115">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b2bcb-116">例如，键入“ROUTE_2”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="b2bcb-117">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-118">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="b2bcb-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="b2bcb-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-119">Click OK.</span></span>
10. <span data-ttu-id="b2bcb-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-120">Click New.</span></span>
11. <span data-ttu-id="b2bcb-121">在“运营”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-122">在这个例子中，选择“组装件”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="b2bcb-123">在“运行时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="b2bcb-124">例如，键入“1”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-124">For example, type 1.</span></span> <span data-ttu-id="b2bcb-125">运行时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="b2bcb-126">在“路线组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-127">在这个例子中，选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="b2bcb-128">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="b2bcb-129">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-130">在这个例子中，选择“组装件”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="b2bcb-131">单击“时间”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-131">Click the Times tab.</span></span>
17. <span data-ttu-id="b2bcb-132">在“设置时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="b2bcb-133">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-133">For this example, type 1.</span></span> <span data-ttu-id="b2bcb-134">设置时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="b2bcb-135">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="b2bcb-136">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-136">Click Approve.</span></span>
20. <span data-ttu-id="b2bcb-137">在“是否还要审核该工艺路线?“字段中选择”是“。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="b2bcb-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-138">Click OK.</span></span>
22. <span data-ttu-id="b2bcb-139">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="b2bcb-140">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-140">Click Activate.</span></span>
24. <span data-ttu-id="b2bcb-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-141">Close the page.</span></span>
25. <span data-ttu-id="b2bcb-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="b2bcb-143">创建成品的工艺路线</span><span class="sxs-lookup"><span data-stu-id="b2bcb-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="b2bcb-144">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2bcb-145">选择物料编号 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="b2bcb-146">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="b2bcb-147">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-147">Click Route.</span></span>
4. <span data-ttu-id="b2bcb-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-148">Click New.</span></span>
5. <span data-ttu-id="b2bcb-149">单击“工艺路线”和“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-149">Click Route and route version.</span></span>
6. <span data-ttu-id="b2bcb-150">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b2bcb-151">在这个例子中，键入“ROUTE_1”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="b2bcb-152">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-153">在这个例子中，请输入或选择“站点 1”.</span><span class="sxs-lookup"><span data-stu-id="b2bcb-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="b2bcb-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-154">Click OK.</span></span>
9. <span data-ttu-id="b2bcb-155">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-155">Click New.</span></span>
10. <span data-ttu-id="b2bcb-156">在“运营”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-157">在这个例子中，选择“包装”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="b2bcb-158">在“运行时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="b2bcb-159">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="b2bcb-160">在“路线组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-161">在这个例子中，选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="b2bcb-162">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="b2bcb-163">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="b2bcb-164">在这个例子中，选择“包装”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="b2bcb-165">单击“时间”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-165">Click the Times tab.</span></span>
16. <span data-ttu-id="b2bcb-166">在“设置时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="b2bcb-167">在这个例子中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="b2bcb-168">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="b2bcb-169">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-169">Click Approve.</span></span>
19. <span data-ttu-id="b2bcb-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-170">Click OK.</span></span>
20. <span data-ttu-id="b2bcb-171">在“操作窗格”上单击“工艺路线版本”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="b2bcb-172">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-172">Click Activate.</span></span>
22. <span data-ttu-id="b2bcb-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-173">Close the page.</span></span>
23. <span data-ttu-id="b2bcb-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="b2bcb-175">启用自动消耗设置时间</span><span class="sxs-lookup"><span data-stu-id="b2bcb-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="b2bcb-176">转到“生产控制 > 设置 > 工艺路线 > 工艺路线组”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="b2bcb-177">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b2bcb-178">选择列表中的“标准”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="b2bcb-179">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-179">Click Edit.</span></span>
4. <span data-ttu-id="b2bcb-180">在“设置时间”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="b2bcb-181">设置时间通常是为某项计算的价格的组成部分。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="b2bcb-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-182">Click Save.</span></span>
6. <span data-ttu-id="b2bcb-183">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b2bcb-183">Close the page.</span></span>

