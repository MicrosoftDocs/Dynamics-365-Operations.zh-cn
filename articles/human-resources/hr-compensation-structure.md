---
title: 制订薪水/薪酬结构和计划
description: 此任务指南将介绍创建固定薪酬计划的流程，以及通过资格规则筛选加入薪资计划的员工。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5711dc8a7fbd44ea9c27e1d57b936765808d199e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008274"
---
# <a name="develop-salarycompensation-structure-and-plan"></a><span data-ttu-id="77dfd-103">制订薪水/薪酬结构和计划</span><span class="sxs-lookup"><span data-stu-id="77dfd-103">Develop salary/compensation structure and plan</span></span>



<span data-ttu-id="77dfd-104">此任务指南将介绍创建固定薪酬计划的流程，以及通过资格规则筛选加入薪资计划的员工。</span><span class="sxs-lookup"><span data-stu-id="77dfd-104">This task guide walks though the process of creating a Fixed compensation plan and enabling employees to be enrolled in the plan through eligibility rules.</span></span> <span data-ttu-id="77dfd-105">创建此任务的演示数据公司是 USMF，此任务专门面向薪酬和福利经理。</span><span class="sxs-lookup"><span data-stu-id="77dfd-105">The demo data company used to create this task is USMF and the task is intended for Compensation and Benefits Managers.</span></span>


## <a name="create-fixed-compensation-plan"></a><span data-ttu-id="77dfd-106">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="77dfd-106">Create fixed compensation plan</span></span>
1. <span data-ttu-id="77dfd-107">单击“薪酬管理”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-107">Click Compensation management.</span></span>
2. <span data-ttu-id="77dfd-108">单击“固定薪酬计划”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-108">Click Fixed compensation plans.</span></span>
3. <span data-ttu-id="77dfd-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-109">Click New.</span></span>
4. <span data-ttu-id="77dfd-110">在“计划”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-110">In the Plan field, type a value.</span></span>
5. <span data-ttu-id="77dfd-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="77dfd-112">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="77dfd-112">In the Effective date field, enter a date.</span></span>
7. <span data-ttu-id="77dfd-113">在“类型”字段中，选择固定薪酬计划为分段、级别还是步骤计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-113">In the Type field, select whether the Fixed compensation plan is a Band, Grade, or Step plan.</span></span>
8. <span data-ttu-id="77dfd-114">“推荐”允许复选框作为流程事件中添加到此计划的所有行动的默认值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-114">The Recommendation allowed checkbox acts as a default value for any actions added to this plan in a Process event.</span></span>  <span data-ttu-id="77dfd-115">允许“推荐”让您在处理薪酬时覆盖计算出的指导性金额。</span><span class="sxs-lookup"><span data-stu-id="77dfd-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>
9. <span data-ttu-id="77dfd-116">“容差范围”允许您决定如何处理，下降到给定薪酬结构范围之外的的薪酬金额。</span><span class="sxs-lookup"><span data-stu-id="77dfd-116">The Out of range tolerance allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span>  <span data-ttu-id="77dfd-117"> “无容差范围”将允许使用任何薪酬金额。</span><span class="sxs-lookup"><span data-stu-id="77dfd-117">An Out of range tolerance of None will allow any compensation amount to be used.</span></span>  <span data-ttu-id="77dfd-118">若薪酬金额低于该等级的最小参考点金额，或高于该等级的最大参考点金额，“虚拟容差”将向用户发出警告。</span><span class="sxs-lookup"><span data-stu-id="77dfd-118">A Soft tolerance will warn the user if the compensation amount is less than the minimum reference point amount for that level, or greater than the maximum amount for that level.</span></span> <span data-ttu-id="77dfd-119">用户可以忽略该警告并继续。</span><span class="sxs-lookup"><span data-stu-id="77dfd-119">The user can ignore the warning and continue.</span></span>  <span data-ttu-id="77dfd-120">如果一员工的薪酬在该级别最低和最高参考范围之外，且在可用范围内自动调整员工薪酬失败，则“硬容差”将产生错误。</span><span class="sxs-lookup"><span data-stu-id="77dfd-120">A Hard tolerance will generate an error if an employee's compensation is set outside of the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>
10. <span data-ttu-id="77dfd-121">若运行薪酬处理事件计算员工薪酬，则需使用“雇用规则”字段。</span><span class="sxs-lookup"><span data-stu-id="77dfd-121">The Hire rule field is used when a compensation Process event is run to calculate an employee's compensation.</span></span>  <span data-ttu-id="77dfd-122"> 百分比雇用规则将计算，在雇佣周期内，工人增加时长比例。</span><span class="sxs-lookup"><span data-stu-id="77dfd-122">A Hire rule of Percent will calculate an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>
11. <span data-ttu-id="77dfd-123">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-123">In the Currency field, type a value.</span></span>
12. <span data-ttu-id="77dfd-124">在“付薪比率转换”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-124">In the Pay rate conversion field, enter or select a value.</span></span>
13. <span data-ttu-id="77dfd-125">展开“幅度利用率矩阵”部分。</span><span class="sxs-lookup"><span data-stu-id="77dfd-125">Expand the Range utilization matrix section.</span></span>
    * <span data-ttu-id="77dfd-126">或者，添加幅度利用记录，使员工可以快速获取中间值，但较慢获得最大范围。</span><span class="sxs-lookup"><span data-stu-id="77dfd-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>  
14. <span data-ttu-id="77dfd-127">此时，您在保存固定薪酬计划后，才可启用“设置薪酬”按钮，定义您的计划的薪酬结构。</span><span class="sxs-lookup"><span data-stu-id="77dfd-127">At this point, you must save the Fixed compensation plan to enable the Set up compensation button and continue defining your compensation structure for the plan.</span></span>  <span data-ttu-id="77dfd-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-128">Click Save.</span></span>
15. <span data-ttu-id="77dfd-129">单击“设置薪酬”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-129">Click Set up compensation.</span></span>
    * <span data-ttu-id="77dfd-130">创建薪酬结构有三种方法。</span><span class="sxs-lookup"><span data-stu-id="77dfd-130">There are three ways to create a compensation structure.</span></span> <span data-ttu-id="77dfd-131">1：通过选择一组参考点并添加级别，创建一个您自己的全新的结构。</span><span class="sxs-lookup"><span data-stu-id="77dfd-131">1: Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span> <span data-ttu-id="77dfd-132">2：首先复制现有计划的薪酬结构并对其进行修改，已完成新的计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-132">2: Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span> <span data-ttu-id="77dfd-133">3：必须选择现有薪酬网格。</span><span class="sxs-lookup"><span data-stu-id="77dfd-133">3: Select an existing compensation grid.</span></span> <span data-ttu-id="77dfd-134">如果其他计划已使用薪酬网格，那么对网格进行更改，也将反映在其他计划中。</span><span class="sxs-lookup"><span data-stu-id="77dfd-134">If the compensation grid is already being used by another plan, any changes made to the grid will also be reflected in the other plan.</span></span>  
16. <span data-ttu-id="77dfd-135">选中“根据现有薪酬矩阵创建新表格”选项。</span><span class="sxs-lookup"><span data-stu-id="77dfd-135">Select the Create new from existing compensation matrix option.</span></span>
17. <span data-ttu-id="77dfd-136">在“从网格复制”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-136">In the Copy from grid field, enter or select a value.</span></span>
    * <span data-ttu-id="77dfd-137">或者您可以更改从所选网格复制而来的，新建的薪酬网格的名称。</span><span class="sxs-lookup"><span data-stu-id="77dfd-137">Optionally you can change the name of the new compensation grid that will be created as a copy of the selected grid.</span></span>  
18. <span data-ttu-id="77dfd-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-138">Click OK.</span></span>
19. <span data-ttu-id="77dfd-139">单击“批量更改”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-139">Click Mass change.</span></span>
    * <span data-ttu-id="77dfd-140">批次更改允许您通过应用一个或更多级别和/或参考点的合并百分比或金额的增加，来维护薪酬矩阵金额。</span><span class="sxs-lookup"><span data-stu-id="77dfd-140">Mass change allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels and/or reference points.</span></span>  
20. <span data-ttu-id="77dfd-141">在“调整金额”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-141">In the Adjustment amount field, enter a number.</span></span>
21. <span data-ttu-id="77dfd-142">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="77dfd-142">In the list, mark or unmark all rows.</span></span>
22. <span data-ttu-id="77dfd-143">单击“应用于网格”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-143">Click Apply to grid.</span></span>
23. <span data-ttu-id="77dfd-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77dfd-144">Close the page.</span></span>
    * <span data-ttu-id="77dfd-145">一旦薪酬结构被创建或选择，您将可以选择使用哪一个参考点作为固定薪酬计划的控制点。</span><span class="sxs-lookup"><span data-stu-id="77dfd-145">Once a compensation structure has been created or selected, you can select which of the reference points should be used as the Control point for the Fixed compensation plan.</span></span>  <span data-ttu-id="77dfd-146">控制点用于计算员工的比较比率。</span><span class="sxs-lookup"><span data-stu-id="77dfd-146">The Control point is used to calculate an employee's Compa Ratio.</span></span>  
24. <span data-ttu-id="77dfd-147">在“控制点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-147">In the Control point field, enter or select a value.</span></span>
25. <span data-ttu-id="77dfd-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77dfd-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a><span data-ttu-id="77dfd-149">为此新固定薪酬计划创建资格规则。</span><span class="sxs-lookup"><span data-stu-id="77dfd-149">Create an eligibility rule for the new Fixed compensation plan</span></span>
    * <span data-ttu-id="77dfd-150">只有在该计划已定义资格规则后，新固定薪酬计划才能分配给员工。</span><span class="sxs-lookup"><span data-stu-id="77dfd-150">The new Fixed compensation plan cannot be assigned to an employee until Eligibility rules have been defined for the plan.</span></span>  
1. <span data-ttu-id="77dfd-151">单击“资格规则”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-151">Click Eligibility rules.</span></span>
2. <span data-ttu-id="77dfd-152">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="77dfd-152">Click New.</span></span>
3. <span data-ttu-id="77dfd-153">在“资格”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-153">In the Eligibility field, type a value.</span></span>
4. <span data-ttu-id="77dfd-154">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="77dfd-155">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="77dfd-155">In the Effective date field, enter a date.</span></span>
    * <span data-ttu-id="77dfd-156">资格规则适用于固定薪酬计划和可变薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-156">Eligibility rules are used for both Fixed and Variable compensation plans.</span></span>  <span data-ttu-id="77dfd-157">在“类型”字段中，选择此资格规则适用于哪种计划类型。</span><span class="sxs-lookup"><span data-stu-id="77dfd-157">In the Type field, select which type of plan this set of eligibility rules is for.</span></span>  
6. <span data-ttu-id="77dfd-158">在“计划”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77dfd-158">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="77dfd-159">选择员工符合薪酬计划所需满足的条件。</span><span class="sxs-lookup"><span data-stu-id="77dfd-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="77dfd-160">标准包括部门、工会、位置（薪酬区域）、工作、职能、工作类型或薪酬水平。</span><span class="sxs-lookup"><span data-stu-id="77dfd-160">Criteria can include a Department, Labor union, Location (Compensation region), Job, Function, Job type, or Compensation level.</span></span> <span data-ttu-id="77dfd-161">员工必须满足所有指定条件才能符合薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-161">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="77dfd-162">如果未指定条件，则所有员工符合薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-162">If no criteria are specified, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="77dfd-163">如果员工不满足指定的资格规则，或薪酬计划并未指定资格规则，那么在创建员工固定薪酬记录时，查找中将不会出现薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="77dfd-163">If an employee does not meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan will not appear in the lookup when creating a Fixed compensation record for an employee.</span></span>  
7. <span data-ttu-id="77dfd-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77dfd-164">Close the page.</span></span>
8. <span data-ttu-id="77dfd-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77dfd-165">Close the page.</span></span>

