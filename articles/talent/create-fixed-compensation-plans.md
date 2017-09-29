---
title: "创建固定薪酬计划"
description: "固定薪酬指员工的标准总薪水或工资。 本文介绍在创建固定薪酬和登记员工前必须设置的组件。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 399e1fee592c0ab31015e37e87d41c71f9282858
ms.contentlocale: zh-cn
ms.lasthandoff: 06/30/2017


---

# <a name="create-fixed-compensation-plans"></a><span data-ttu-id="b80ee-104">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="b80ee-104">Create fixed compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b80ee-105">固定薪酬指员工的标准总薪水或工资。</span><span class="sxs-lookup"><span data-stu-id="b80ee-105">Fixed compensation refers to an employee's regular gross salary or wages.</span></span> <span data-ttu-id="b80ee-106">本主题介绍在创建固定薪酬和登记员工前必须设置的组件。</span><span class="sxs-lookup"><span data-stu-id="b80ee-106">This topic describes the components that must be set up before you can create a fixed compensation plan and enroll employees.</span></span>

<span data-ttu-id="b80ee-107">固定薪酬金额可以基于绩效、区域和预算增加等系数为您的员工计算。</span><span class="sxs-lookup"><span data-stu-id="b80ee-107">Fixed compensation amounts can be calculated for your employees, based on factors such as performance, region, and budget increases.</span></span> <span data-ttu-id="b80ee-108">Microsoft Talent 支持步幅、等级和分段薪酬类型。</span><span class="sxs-lookup"><span data-stu-id="b80ee-108">Microsoft Talent supports step, grade, and band compensation types.</span></span>

## <a name="fixed-compensation-components"></a><span data-ttu-id="b80ee-109">固定薪酬组件</span><span class="sxs-lookup"><span data-stu-id="b80ee-109">Fixed compensation components</span></span>
### <a name="compensation-levels"></a><span data-ttu-id="b80ee-110">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="b80ee-110">Compensation levels</span></span>

<span data-ttu-id="b80ee-111">您可以使用**薪酬级别**设置各种工作的薪酬，这有助于确保向承担这些工作的员工公平付薪。</span><span class="sxs-lookup"><span data-stu-id="b80ee-111">You can use **compensation levels** to set compensation for various jobs, to help guarantee that the employees who hold those jobs are paid fairly.</span></span> <span data-ttu-id="b80ee-112">在**薪酬级别**页上，您可以设置每个步幅、等级和分段计划所需的薪酬级别。</span><span class="sxs-lookup"><span data-stu-id="b80ee-112">On the **Compensation levels** page, you can set up the compensation levels that are required for each step, grade, and band plan.</span></span> <span data-ttu-id="b80ee-113">使用 **Up** 和 **Down** 按钮根据级别类型将它们放到正确顺序。</span><span class="sxs-lookup"><span data-stu-id="b80ee-113">Use the **Up** and **Down** buttons to put the levels in the correct order, according to their type.</span></span> <span data-ttu-id="b80ee-114">通过为工作设置薪酬级别，您可以帮助确保位于此职位的所有员工在同一级别付薪。</span><span class="sxs-lookup"><span data-stu-id="b80ee-114">By setting compensation levels on a job, you help guarantee that all employees who hold a position for that job are paid at the same level.</span></span>

### <a name="reference-points"></a><span data-ttu-id="b80ee-115">参考点</span><span class="sxs-lookup"><span data-stu-id="b80ee-115">Reference points</span></span>

<span data-ttu-id="b80ee-116">**参考点**是定义每个级别的薪酬范围的网格中的列。</span><span class="sxs-lookup"><span data-stu-id="b80ee-116">**Reference points** are the columns in the grid that define the compensation ranges for each level.</span></span> <span data-ttu-id="b80ee-117">薪酬级别是网格中的行。</span><span class="sxs-lookup"><span data-stu-id="b80ee-117">The compensation level is the row in the grid.</span></span> <span data-ttu-id="b80ee-118">等级类型的计划的典型参考点是最小、中点和最大。</span><span class="sxs-lookup"><span data-stu-id="b80ee-118">Typical reference points for a plan of the grade type are a minimum, a midpoint, and a maximum.</span></span> <span data-ttu-id="b80ee-119">您在**参考点设置**页上创建参考点。</span><span class="sxs-lookup"><span data-stu-id="b80ee-119">You create reference points on the **Reference point setups** page.</span></span>

### <a name="compensation-grids"></a><span data-ttu-id="b80ee-120">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="b80ee-120">Compensation grids</span></span>

<span data-ttu-id="b80ee-121">在设置级别和参考点后，他们可以组合创建**薪酬网格**。</span><span class="sxs-lookup"><span data-stu-id="b80ee-121">After you set up the levels and reference points, they can be combined to create a **compensation grid**.</span></span> <span data-ttu-id="b80ee-122">在**薪酬网格**页上，定义有关网格的信息。</span><span class="sxs-lookup"><span data-stu-id="b80ee-122">On the **Compensation grids** page, define information about the grid.</span></span> <span data-ttu-id="b80ee-123">例如，指定设计网格用于哪些方面，用于哪类计划，以及网格需要的参考点或列。</span><span class="sxs-lookup"><span data-stu-id="b80ee-123">For example, specify what the grid designed to be used for, what type of plan it will be used with, and which reference points or columns are required in the grid.</span></span> <span data-ttu-id="b80ee-124">在您完成输入该信息后，单击**薪酬结构**添加级别和金额到您的网格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-124">After you've finished entering that information, click **Compensation structure** to add levels and amounts to your grid.</span></span> 

<span data-ttu-id="b80ee-125">**提示：**使用薪酬结构的**批量更改**功能来设置初始金额，然后设置整个级别或参考点按百分比或金额递增。</span><span class="sxs-lookup"><span data-stu-id="b80ee-125">**Tip:** Use the **Mass changes** function on the compensation structure to set initial amounts, and then increment by percentages or amounts across your levels or reference points.</span></span>

### <a name="pay-frequencies"></a><span data-ttu-id="b80ee-126">付薪频率</span><span class="sxs-lookup"><span data-stu-id="b80ee-126">Pay frequencies</span></span>

<span data-ttu-id="b80ee-127">**付薪频率**用于定义员工工资或薪金如何指定（例如每小时 $10 与每年 $50,000），以及每小时、每周、每月（12 个月）和每年费率之间的换算。</span><span class="sxs-lookup"><span data-stu-id="b80ee-127">**Pay frequencies** are used to define how an employee's wage or salary is being specified (for example $10 per hour versus $50,000 per year), and the conversion between the hourly, weekly, monthly (12 months), and annual rates.</span></span> <span data-ttu-id="b80ee-128">例如，为时薪员工使用 38 小时工作周的公司设置付薪频率的小时费率为 1，每周费率为 38，每月费率为 164.6666666667 以及每年费率为 1,976。</span><span class="sxs-lookup"><span data-stu-id="b80ee-128">For example, a company that uses a 38-hour work week for its hourly employees sets up a pay frequency that has an hourly rate of 1, a weekly rate of 38, a monthly rate of 164.6666666667, and an annual rate of 1,976.</span></span> <span data-ttu-id="b80ee-129">这些换算用于计算在员工的固定薪酬记录中显示的不同付薪比率。</span><span class="sxs-lookup"><span data-stu-id="b80ee-129">These conversions are used to calculate the various pay rates that appear on an employee's fixed compensation record.</span></span>

## <a name="fixed-compensation-plans"></a><span data-ttu-id="b80ee-130">固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="b80ee-130">Fixed compensation plans</span></span>
<span data-ttu-id="b80ee-131">您可以设计固定薪酬计划组合您配置的所有组件。</span><span class="sxs-lookup"><span data-stu-id="b80ee-131">You can design the fixed compensation plan to combine all the components that you've configured.</span></span> <span data-ttu-id="b80ee-132">若要创建固定薪酬计划，打开**固定薪酬计划**页面。</span><span class="sxs-lookup"><span data-stu-id="b80ee-132">To create a fixed compensation plan, open the **Fixed compensation plans** page.</span></span> <span data-ttu-id="b80ee-133">在这里，您可以为您的计划提供名称和描述，选择它是哪类计划（步幅、等级或分段），选择为员工的付薪比率使用的付薪频率（每小时金额、每年金额，等等），并且设置控制薪酬如何处理的某些选项。</span><span class="sxs-lookup"><span data-stu-id="b80ee-133">Here, you can give your plan a name and description, select what type of plan it is (step, grade, or band), select the pay frequency that you'll use for the employee's pay rate (amount per hour, amount per year, and so on), and set some options that control how compensation is processed.</span></span> 

<span data-ttu-id="b80ee-134">**超出范围容差**设置允许您指定确保薪酬金额介于最小和最大金额之间的严格程度。</span><span class="sxs-lookup"><span data-stu-id="b80ee-134">The **Out of range tolerance** setting lets you specify how strict you want to be about making sure that compensation amounts are between the minimum and maximum amounts.</span></span> <span data-ttu-id="b80ee-135">**硬性**容差要求该薪酬在为给定级别定义的范围内。</span><span class="sxs-lookup"><span data-stu-id="b80ee-135">A **Hard** tolerance requires that compensation be within the range that is defined for a given level.</span></span> <span data-ttu-id="b80ee-136">**软件**容差在薪酬金额超出此范围之外时向您发出警告，但允许您继续。</span><span class="sxs-lookup"><span data-stu-id="b80ee-136">A **Soft** tolerance alerts you when the compensation amount is outside the range but allows you to continue.</span></span> <span data-ttu-id="b80ee-137">如果您将容差设置为**无**，则可以输入任何员工薪酬金额，而无需接收警告或错误消息。</span><span class="sxs-lookup"><span data-stu-id="b80ee-137">If you set the tolerance to **None**, you can enter any compensation amount for an employee without receiving warning or error messages.</span></span> 

<span data-ttu-id="b80ee-138">**雇用规则**设置可以指定是否所有员工均应接收相同的增加，而与其雇用日期无关（**雇用规则**  =  **无**），还是基于员工在周期内被雇用的时长，员工应接收奖励百分比（**雇用规则**  =  **百分比**）。</span><span class="sxs-lookup"><span data-stu-id="b80ee-138">The **Hire rule** setting lets you specify whether all employees should receive the same increase, regardless of the date that they were hired (**Hire rule** = **None**), or whether employees should receive a percentage of the award, based on how long they were employed during the cycle (**Hire rule** = **Percent**).</span></span> 

<span data-ttu-id="b80ee-139">**幅度利用率矩阵**在以下情况下很有用：如果您希望减少员工到达其范围的中点所需的时间，或者增加员工到达范围的最大参考点所需的时间。</span><span class="sxs-lookup"><span data-stu-id="b80ee-139">A **range utilization matrix** is useful if you want either to reduce the time that is required for employees to reach the midpoint of their range, or to increase the time that is required for employees to reach to the maximum reference point in the range.</span></span> <span data-ttu-id="b80ee-140">例如，如果您要给其范围内排名后 25% 的员工其目标奖励的 110%，但您要给其范围内排名前 25% 的员工其目标奖励的 80%，以防止他们很快到达最大金额。</span><span class="sxs-lookup"><span data-stu-id="b80ee-140">For example, you want to give employees who are in the bottom 25 percent of their range 110 percent of their target award, but you want to give employees who are in the top 25 percent of their range only 80 percent of their target award, to prevent them from reaching the maximum as quickly.</span></span> 

<span data-ttu-id="b80ee-141">在您定义固定薪酬计划的基础后，您可以设置计划的薪酬结构。</span><span class="sxs-lookup"><span data-stu-id="b80ee-141">After you define the basics of the fixed compensation plan, you can set up the compensation structure for the plan.</span></span> <span data-ttu-id="b80ee-142">单击**设置薪酬**。</span><span class="sxs-lookup"><span data-stu-id="b80ee-142">Click **Set up compensation**.</span></span> <span data-ttu-id="b80ee-143">打开的对话滑块为您提供三个选项：</span><span class="sxs-lookup"><span data-stu-id="b80ee-143">A dialog slider opens that gives you three options:</span></span>

-   <span data-ttu-id="b80ee-144">通过选择参考点设置并为网格提供名称来创建新的薪酬网格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-144">Create a new compensation grid by selecting a reference point setup and giving the grid a name.</span></span>
-   <span data-ttu-id="b80ee-145">通过复制您可以用作起点的现有网格创建新的薪酬网格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-145">Create a new compensation grid by making a copy of an existing grid that you can use as a starting point.</span></span>
-   <span data-ttu-id="b80ee-146">使用已定义的现有薪酬网格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-146">Use an existing compensation grid that has already been defined.</span></span> <span data-ttu-id="b80ee-147">如果网格更改，使用相同网格的所有薪酬计划将接收更新。</span><span class="sxs-lookup"><span data-stu-id="b80ee-147">All compensation plans that use the same grid receive updates if that grid is changed.</span></span>

<span data-ttu-id="b80ee-148">在您选择一个选项后，**薪酬结构**页将打开，并且，您可以对新的薪酬网格或现有薪酬网格进行更改。</span><span class="sxs-lookup"><span data-stu-id="b80ee-148">After you select an option, the **Compensation structure** page opens, and you can make changes to the new compensation grid or the existing compensation grid.</span></span>

## <a name="fixed-compensation-enrollment"></a><span data-ttu-id="b80ee-149">固定薪酬登记</span><span class="sxs-lookup"><span data-stu-id="b80ee-149">Fixed compensation enrollment</span></span>
### <a name="determine-who-is-eligible-for-the-plan"></a><span data-ttu-id="b80ee-150">确定谁适用于计划</span><span class="sxs-lookup"><span data-stu-id="b80ee-150">Determine who is eligible for the plan</span></span>

<span data-ttu-id="b80ee-151">在固定薪酬计划中登记员工的第一步是确定适用于在计划中定义的薪酬的员工。</span><span class="sxs-lookup"><span data-stu-id="b80ee-151">The first step in enrolling employees in a fixed compensation plan is to determine who is eligible for the compensation that is defined in the plan.</span></span> <span data-ttu-id="b80ee-152">在您确定资格前，您将无法将计划分配到任何员工。</span><span class="sxs-lookup"><span data-stu-id="b80ee-152">Until you determine eligibility, you won't be able to assign the plan to any employees.</span></span> <span data-ttu-id="b80ee-153">若要设置资格，请打开**资格规则**页。</span><span class="sxs-lookup"><span data-stu-id="b80ee-153">To set up eligibility, open the **Eligibility rules** page.</span></span> <span data-ttu-id="b80ee-154">在这里，您创建薪酬计划的新资格规则，并定义员工必须满足才有资格享受计划的条件。</span><span class="sxs-lookup"><span data-stu-id="b80ee-154">Here, you create a new eligibility rule for your compensation plan and define the criteria that an employee must meet to be eligible for a plan.</span></span> <span data-ttu-id="b80ee-155">您可以基于部门、工会、薪酬区域（位置）、工作、工作职能、工作类型或薪酬级别限制资格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-155">You can limit eligibility based on department, labor union, compensation region (location), job, job function, job type, or compensation level.</span></span> <span data-ttu-id="b80ee-156">只有当员工满足在资格规则中设置的所有条件时，他们才能在薪酬计划中登记。</span><span class="sxs-lookup"><span data-stu-id="b80ee-156">Employees can be enrolled in a compensation plan only if they meet all conditions that are set on the eligibility rule.</span></span> 

<span data-ttu-id="b80ee-157">**注意：**资格规则用于确定固定和可变薪酬计划的资格。</span><span class="sxs-lookup"><span data-stu-id="b80ee-157">**Note:** Eligibility rules are used to determine eligibility for both fixed and variable compensation plans.</span></span> 

<span data-ttu-id="b80ee-158">资格规则考虑工作、职位和员工记录中的特定字段的值来确定某员工是否有资格享受薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b80ee-158">The eligibility rule considers the value of specific fields in the Job, Position, and Employee records to determine whether an employee is eligible for a compensation plan.</span></span>

-   <span data-ttu-id="b80ee-159">在**工作**页上，资格规则考虑以下字段：</span><span class="sxs-lookup"><span data-stu-id="b80ee-159">On the **Job** page, the eligibility rule considers the following fields:</span></span>
    -   <span data-ttu-id="b80ee-160">**工作**字段</span><span class="sxs-lookup"><span data-stu-id="b80ee-160">The **Job** field</span></span>
    -   <span data-ttu-id="b80ee-161">在**工作分类**选项卡上，**职能**和**工作类型**字段</span><span class="sxs-lookup"><span data-stu-id="b80ee-161">On the **Job classification** tab, the **Function** and **Job type** fields</span></span>
    -   <span data-ttu-id="b80ee-162">在**薪酬**选项卡上，**级别**字段</span><span class="sxs-lookup"><span data-stu-id="b80ee-162">On the **Compensation** tab, the **Level** field</span></span>
-   <span data-ttu-id="b80ee-163">在**职位**页上，资格规则考虑**部门**和**薪酬区域**字段。</span><span class="sxs-lookup"><span data-stu-id="b80ee-163">On the **Positions** page, the eligibility rule considers the **Department** and **Compensation region** fields.</span></span>

<span data-ttu-id="b80ee-164">资格规则还会考虑与员工关联的工会（在**员工**页上，在**工作人员**选项卡上，单击**个人信息** &gt; **工会**）。</span><span class="sxs-lookup"><span data-stu-id="b80ee-164">The eligibility rule also considers labor unions that are associated with the employee (on the **Employees** page, on the **Worker** tab, click **Personal information** &gt; **Labor unions**).</span></span>

### <a name="define-fixed-compensation-actions"></a><span data-ttu-id="b80ee-165">定义固定薪酬操作</span><span class="sxs-lookup"><span data-stu-id="b80ee-165">Define fixed compensation actions</span></span>

<span data-ttu-id="b80ee-166">如果您设置或将更改应用于某一员工的固定薪酬，则使用**固定薪酬操作**。</span><span class="sxs-lookup"><span data-stu-id="b80ee-166">**Fixed compensation actions** are used when you set or apply changes to an employee's fixed compensation.</span></span> <span data-ttu-id="b80ee-167">固定薪酬操作允许您为薪酬和福利经理可以执行的操作的类型提供描述性名称。</span><span class="sxs-lookup"><span data-stu-id="b80ee-167">Fixed compensation actions let you provide descriptive names for the types of actions that a Compensation and benefits manager can perform.</span></span> <span data-ttu-id="b80ee-168">不同的操作类型具有特定逻辑，以便可以在特定时间使用。</span><span class="sxs-lookup"><span data-stu-id="b80ee-168">Different action types have special logic behind them, so that they can be used at specific times.</span></span> 

<span data-ttu-id="b80ee-169">例如，在为员工设置固定薪酬时，只有具有类型**雇用/重新雇用**的操作可以使用。</span><span class="sxs-lookup"><span data-stu-id="b80ee-169">For example, when the fixed compensation is set up for an employee, only actions that have a type of **Hire/Rehire** can be used.</span></span> <span data-ttu-id="b80ee-170">在这种情况下，您可能希望创建三个不同的**雇用/重新雇用**类型的操作，并命名它们为**雇用**、**重新雇用**和**转岗**。</span><span class="sxs-lookup"><span data-stu-id="b80ee-170">In this case, you might want to create three different actions of the **Hire/Rehire** type, and name them **Hire**, **Rehire**, and **Transfer**.</span></span> <span data-ttu-id="b80ee-171">然后，您有更具描述性的说明，说明固定薪酬给予员工或更改的原因。</span><span class="sxs-lookup"><span data-stu-id="b80ee-171">You then have a more descriptive explanation of why the fixed compensation was given to an employee or changed.</span></span>

### <a name="enroll-the-employee"></a><span data-ttu-id="b80ee-172">登记员工</span><span class="sxs-lookup"><span data-stu-id="b80ee-172">Enroll the employee</span></span>

<span data-ttu-id="b80ee-173">您现在可以将员工分配到固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="b80ee-173">You can now assign an employee to a fixed compensation plan.</span></span> <span data-ttu-id="b80ee-174">打开**员工**页，然后选择要在薪酬计划中登记的员工。</span><span class="sxs-lookup"><span data-stu-id="b80ee-174">Open the **Employees** page, and select the employee to enroll in the compensation plan.</span></span> <span data-ttu-id="b80ee-175">在“操作”窗格上，单击**薪酬** &gt; **固定计划**。</span><span class="sxs-lookup"><span data-stu-id="b80ee-175">On the Action Pane, click **Compensation** &gt; **Fixed plan**.</span></span> <span data-ttu-id="b80ee-176">您现在可以为该员工创建新的固定薪酬操作。</span><span class="sxs-lookup"><span data-stu-id="b80ee-176">You can now create a new fixed compensation action for that employee.</span></span> 

<span data-ttu-id="b80ee-177">**注意：**薪酬计划字段仅显示为每个计划设置的资格规则下员工有资格的计划。</span><span class="sxs-lookup"><span data-stu-id="b80ee-177">**Note:** The compensation plan field shows only the plans that an employee is eligible for under the eligibility rules that were set up for each plan.</span></span> <span data-ttu-id="b80ee-178">如果资格规则没有为计划设置，员工不适用于该计划。</span><span class="sxs-lookup"><span data-stu-id="b80ee-178">If no eligibility rule is set up for a plan, no employees will be eligible for that plan.</span></span> 

<span data-ttu-id="b80ee-179">系统会验证为等级或分段类型的薪酬计划指定的薪酬金额，是否在员工工作的指定薪酬级别的最小和最大参考点内。</span><span class="sxs-lookup"><span data-stu-id="b80ee-179">The system verifies that the compensation amount that is specified for a compensation plan of the grade or band type is within the minimum and maximum reference points for the given compensation level on the employee's job.</span></span> <span data-ttu-id="b80ee-180">如果薪酬金额超出允许的范围，警告或错误消息将显示，具体取决于在固定薪酬计划中设置的容差级别。</span><span class="sxs-lookup"><span data-stu-id="b80ee-180">If the compensation amount is outside the allowed range, a warning or error message is displayed, depending on the tolerance level that is set on the fixed compensation plan.</span></span>

<a name="see-also"></a><span data-ttu-id="b80ee-181">请参阅</span><span class="sxs-lookup"><span data-stu-id="b80ee-181">See also</span></span>
--------

[<span data-ttu-id="b80ee-182">薪酬计划</span><span class="sxs-lookup"><span data-stu-id="b80ee-182">Compensation plans</span></span>](compensation-plans.md)




