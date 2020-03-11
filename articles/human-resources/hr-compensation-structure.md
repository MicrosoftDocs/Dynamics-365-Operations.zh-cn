---
title: 制订薪酬结构
description: 本文介绍如何创建固定薪酬计划，以及如何通过资格规则在该计划中等记员工。
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: de715b7fda2f1548f2f443b9e0f6d09f5b881d61
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2020
ms.locfileid: "3034255"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="b0ae4-103">制订薪酬结构</span><span class="sxs-lookup"><span data-stu-id="b0ae4-103">Develop a compensation structure</span></span>

<span data-ttu-id="b0ae4-104">本文介绍如何创建固定薪酬计划，以及如何通过资格规则在该计划中等记员工。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="b0ae4-105">本文使用 USMF 演示数据，适用于薪酬和福利经理。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="b0ae4-106">创建固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="b0ae4-107">选择**薪酬管理**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="b0ae4-108">选择**固定薪酬计划**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="b0ae4-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-109">Select **New**.</span></span>

4. <span data-ttu-id="b0ae4-110">在**计划**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="b0ae4-111">在**描述**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="b0ae4-112">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="b0ae4-113">在**类型**字段中，选择固定薪酬计划为**分段**、**级别**还是**步骤**计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="b0ae4-114">**允许推荐**复选框作为流程事件中添加到此计划的所有行动的默认值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="b0ae4-115">允许“推荐”让您在处理薪酬时覆盖计算出的指导性金额。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="b0ae4-116">**超出容差范围**允许您决定如何处理，下降到给定薪酬结构范围之外的的薪酬金额。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="b0ae4-117">将**超出容差范围**字段设置为 **无**将允许您使用任何薪酬金额。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="b0ae4-118">若薪酬金额低于该等级的最小参考点金额，或高于该等级的最大参考点金额，**虚拟容差**将向用户发出警告。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="b0ae4-119">用户可以忽略该警告并继续。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="b0ae4-120">如果一员工的薪酬在该级别最低和最高参考范围之外，且在可用范围内自动调整员工薪酬失败，则**硬容差**将产生错误。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="b0ae4-121">**雇用规则**字段在流程事件中计算员工的薪酬。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="b0ae4-122">类型为**百分比**的**雇用规则**计算在雇佣周期内工人的增加时长比例。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="b0ae4-123">在**货币**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="b0ae4-124">在**付薪比率转换**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="b0ae4-125">展开**幅度利用率矩阵**部分。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="b0ae4-126">或者，添加幅度利用记录，使员工可以快速获取中间值，但较慢获得最大范围。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="b0ae4-127">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-127">Select **Save**.</span></span> <span data-ttu-id="b0ae4-128">这将启用**设置薪酬**按钮，并继续为计划定义薪酬结构。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="b0ae4-129">选择**设置薪酬**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-129">Select **Set up compensation**.</span></span> <span data-ttu-id="b0ae4-130">可以使用以下三种方法之一创建薪酬结构：</span><span class="sxs-lookup"><span data-stu-id="b0ae4-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="b0ae4-131">通过选择一组参考点并添加级别，创建一个您自己的全新的结构。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="b0ae4-132">首先复制现有计划的薪酬结构并对其进行修改，已完成新的计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="b0ae4-133">选择现有薪酬网格。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-133">Select an existing compensation grid.</span></span> <span data-ttu-id="b0ae4-134">如果其他计划已使用薪酬网格，则另一个计划也会体现您对网格进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="b0ae4-135">选择**从现有薪酬矩阵新建**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="b0ae4-136">在**从网格复制**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="b0ae4-137">（可选）您可以更改通过复制所选网格创建的新薪酬网格的名称。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="b0ae4-138">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-138">Select **OK**.</span></span>

19. <span data-ttu-id="b0ae4-139">选择**批量更改**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-139">Select **Mass change**.</span></span> <span data-ttu-id="b0ae4-140">**批量更改**允许您通过应用一个或更多级别或参考点的合并百分比或金额的增加，来维护薪酬矩阵金额。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="b0ae4-141">在**调整金额**字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="b0ae4-142">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="b0ae4-143">单击**应用于网格**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="b0ae4-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-144">Close the page.</span></span> <span data-ttu-id="b0ae4-145">创建薪酬结构之后，可以选择使用哪一个参考点作为固定薪酬计划的控制点。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="b0ae4-146">控制点用于计算员工的比较比率。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="b0ae4-147">在**控制点**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="b0ae4-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="b0ae4-149">为固定薪酬计划创建资格规则</span><span class="sxs-lookup"><span data-stu-id="b0ae4-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="b0ae4-150">为计划定义资格之前，不能为员工分配固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="b0ae4-151">选择**资格规则**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="b0ae4-152">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-152">Select **New**.</span></span>

3. <span data-ttu-id="b0ae4-153">在**资格**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="b0ae4-154">在**描述**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="b0ae4-155">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="b0ae4-156">固定薪酬计划和可变薪酬计划都使用资格规则。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="b0ae4-157">在**类型**字段中，选择计划的类型。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="b0ae4-158">在**计划**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="b0ae4-159">选择员工符合薪酬计划所需满足的条件。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="b0ae4-160">条件可以包括：</span><span class="sxs-lookup"><span data-stu-id="b0ae4-160">Criteria can include:</span></span>

    - <span data-ttu-id="b0ae4-161">**部门**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-161">**Department**</span></span>
    - <span data-ttu-id="b0ae4-162">**工会**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-162">**Labor union**</span></span>
    - <span data-ttu-id="b0ae4-163">**位置**（**薪酬区域**）</span><span class="sxs-lookup"><span data-stu-id="b0ae4-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="b0ae4-164">**作业**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-164">**Job**</span></span>
    - <span data-ttu-id="b0ae4-165">**职能**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-165">**Function**</span></span>
    - <span data-ttu-id="b0ae4-166">**作业类型**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-166">**Job type**</span></span>
    - <span data-ttu-id="b0ae4-167">**薪酬级别**</span><span class="sxs-lookup"><span data-stu-id="b0ae4-167">**Compensation level**</span></span>
    
    <span data-ttu-id="b0ae4-168">员工必须满足所有指定条件才能符合薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="b0ae4-169">如果不指定任何条件，则所有员工符合薪酬计划的资格。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="b0ae4-170">如果员工不满足指定的资格规则，或薪酬计划并未指定资格规则，那么在创建员工固定薪酬记录时，查找中将不会出现薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="b0ae4-171">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-171">Close the page.</span></span>

8. <span data-ttu-id="b0ae4-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-172">Close the page.</span></span>

