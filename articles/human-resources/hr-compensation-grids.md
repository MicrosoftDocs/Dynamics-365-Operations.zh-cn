---
title: 设置薪酬网格
description: 薪酬网格用于定义及维持固定薪酬计划的工资结构。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13415f68f41555f3e86cbe699cf921e9a2cf6d5c
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111568"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="60c71-103">设置薪酬网格</span><span class="sxs-lookup"><span data-stu-id="60c71-103">Set up compensation grids</span></span>

<span data-ttu-id="60c71-104">薪酬网格用于定义及维持固定薪酬计划的工资结构。</span><span class="sxs-lookup"><span data-stu-id="60c71-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="60c71-105">新建薪酬计划时薪酬网格可以在多个计划中共享或复制。</span><span class="sxs-lookup"><span data-stu-id="60c71-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="60c71-106">在创建薪酬网格之前，必须设置“级别”和“参考点”。</span><span class="sxs-lookup"><span data-stu-id="60c71-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="60c71-107">此示例将使用“级别”和“参考点”演示数据创建新的薪酬网格等级类型。</span><span class="sxs-lookup"><span data-stu-id="60c71-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="60c71-108">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="60c71-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="60c71-109">设置有关薪酬网格的信息</span><span class="sxs-lookup"><span data-stu-id="60c71-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="60c71-110">转到“人力资源”>“薪酬”>“固定薪酬”>“薪酬网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="60c71-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60c71-111">Click New.</span></span>
3. <span data-ttu-id="60c71-112">在“网格”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="60c71-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60c71-114">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="60c71-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="60c71-115">在“参考设置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="60c71-116">在“货币”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="60c71-117">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="60c71-118">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="60c71-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="60c71-119">在薪酬结构中添加级别</span><span class="sxs-lookup"><span data-stu-id="60c71-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="60c71-120">单击“薪酬结构”。</span><span class="sxs-lookup"><span data-stu-id="60c71-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="60c71-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="60c71-122">在“级别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="60c71-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60c71-123">Click New.</span></span>
5. <span data-ttu-id="60c71-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="60c71-125">在“级别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="60c71-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60c71-126">Click New.</span></span>
8. <span data-ttu-id="60c71-127">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="60c71-128">在“级别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="60c71-129">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60c71-129">Click New.</span></span>
11. <span data-ttu-id="60c71-130">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="60c71-131">在“级别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="60c71-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60c71-132">Click New.</span></span>
14. <span data-ttu-id="60c71-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="60c71-134">在“级别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="60c71-135">在薪酬结构中填入值</span><span class="sxs-lookup"><span data-stu-id="60c71-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="60c71-136">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="60c71-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="60c71-137">此时，在该表中，可以在每个字段手动输入薪酬值，或者使用“批量更改功能”轻松填充多个字段并执行基本的计算功能。</span><span class="sxs-lookup"><span data-stu-id="60c71-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="60c71-138">单击“批量更改”。</span><span class="sxs-lookup"><span data-stu-id="60c71-138">Click Mass change.</span></span>
    * <span data-ttu-id="60c71-139">此网格表中，我们首先把第一级别的中间点值应用到表中的所有字段中。</span><span class="sxs-lookup"><span data-stu-id="60c71-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="60c71-140">这将是薪酬矩阵的基础。</span><span class="sxs-lookup"><span data-stu-id="60c71-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="60c71-141">在“调整类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="60c71-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="60c71-142">在“调整金额”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="60c71-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="60c71-143">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="60c71-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="60c71-144">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="60c71-145">现在我们将使用批量更改功能按照一定的百分比或数目在接下来的每个级别中逐渐增加金额。</span><span class="sxs-lookup"><span data-stu-id="60c71-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="60c71-146">在此示例中，每个等级在中间点值的 12.5% 范围内进行调整。</span><span class="sxs-lookup"><span data-stu-id="60c71-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="60c71-147">在“调整类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="60c71-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="60c71-148">在“调整金额”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="60c71-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="60c71-149">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="60c71-150">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="60c71-151">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="60c71-152">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="60c71-153">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="60c71-154">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="60c71-155">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="60c71-156">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="60c71-157">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="60c71-158">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="60c71-159">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="60c71-160">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="60c71-161">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60c71-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="60c71-162">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="60c71-163">现在使用批量更改功能调整每个级别的“最小”与“最大”参考点值。</span><span class="sxs-lookup"><span data-stu-id="60c71-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="60c71-164">此示例将使用 50% 的点差，那么其最小参考点值将调整 -20%，而最大参考点值调整 +20%。</span><span class="sxs-lookup"><span data-stu-id="60c71-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="60c71-165">在“调整金额”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="60c71-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="60c71-166">在“参考点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="60c71-167">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="60c71-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="60c71-168">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="60c71-169">在“调整金额”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="60c71-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="60c71-170">在“参考点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="60c71-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="60c71-171">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="60c71-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="60c71-172">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="60c71-172">Click Apply to grid.</span></span>

