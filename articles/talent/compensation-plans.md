---
title: "薪酬计划"
description: "薪酬和福利经理可以使用薪酬管理来维护和处理组织的员工的固定薪酬计划和可变薪酬计划。"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 86070204769b866b947405436437eb0eb746de11
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="compensation-plans"></a><span data-ttu-id="3c8c3-103">薪酬计划</span><span class="sxs-lookup"><span data-stu-id="3c8c3-103">Compensation plans</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="3c8c3-104">薪酬和福利经理可以使用薪酬管理来维护和处理组织的员工的固定薪酬计划和可变薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="3c8c3-105">简介</span><span class="sxs-lookup"><span data-stu-id="3c8c3-105">Introduction</span></span>

<span data-ttu-id="3c8c3-106">薪酬管理用于控制基本工资和奖励的发放。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="3c8c3-107">员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="3c8c3-108">激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="3c8c3-109">员工可登记一个或多个这两种类型的计划。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="3c8c3-110">员工必须满足以下要求以便符合在薪酬计划中登记的条件：</span><span class="sxs-lookup"><span data-stu-id="3c8c3-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="3c8c3-111">员工必须具有有效职位分配。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="3c8c3-112">员工必须满足由薪酬计划资格规则定义的条件。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="3c8c3-113">薪酬设置</span><span class="sxs-lookup"><span data-stu-id="3c8c3-113">Compensation setup</span></span>
<span data-ttu-id="3c8c3-114">下表列出可整体设置贵公司的薪酬计划的薪酬过程的组成。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3c8c3-115">组件</span><span class="sxs-lookup"><span data-stu-id="3c8c3-115">Component</span></span></th>
<th><span data-ttu-id="3c8c3-116">更多信息…</span><span class="sxs-lookup"><span data-stu-id="3c8c3-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c8c3-117">固定薪酬操作</span><span class="sxs-lookup"><span data-stu-id="3c8c3-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="3c8c3-118">固定薪酬操作实现两个目的：</span><span class="sxs-lookup"><span data-stu-id="3c8c3-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="3c8c3-119">操作可以指定在员工薪酬更改时必须记录的信息种类。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="3c8c3-120">例如，您可以要求记录更改（例如晋升或降级）的原因。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="3c8c3-121">操作可以确保在处理固定薪酬计划时应用计算。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="3c8c3-122">例如，类型“权益”的操作会将员工付薪与员工所在级别的最小参考点进行比较，并确保员工的工资至少为最小值。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-123">级别</span><span class="sxs-lookup"><span data-stu-id="3c8c3-123">Levels</span></span></td>
<td><span data-ttu-id="3c8c3-124">级别与工作以及作业引用有关的所有职位关联。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="3c8c3-125">您可以为三个薪酬计划类型创建独立的级别：等级、分段或步幅。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-126">幅度利用率矩阵</span><span class="sxs-lookup"><span data-stu-id="3c8c3-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="3c8c3-127">幅度利用率矩阵帮助您员工转移到其作业的控制点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="3c8c3-128">您还可以使用幅度利用率来控制公司内的付薪比率公正性，而与单独员工的绩效或公司的整体绩效无关。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="3c8c3-129">例如，在其幅度内薪资低的员工比薪资高的员工获得更高的增长率。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="3c8c3-130">以此种方式，您可以系统化地抵消股本差异。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="3c8c3-131">按如下公式计算幅度利用率：（固定付薪比率 - 最小幅度）÷（最大幅度 - 最小幅度）。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-132">参考点设置</span><span class="sxs-lookup"><span data-stu-id="3c8c3-132">Reference point setups</span></span></td>
<td><span data-ttu-id="3c8c3-133">参考点设置包括在矩阵表中构成工资幅度的一组参考点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="3c8c3-134">每个幅度均可以与付薪比率关联。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="3c8c3-135">例如，等级计划通常将具有最小、中间和最大参考点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-136">薪酬矩阵</span><span class="sxs-lookup"><span data-stu-id="3c8c3-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="3c8c3-137">薪酬矩阵是用于创建薪酬结构的一组参考点和级别。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-138">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="3c8c3-138">Compensation structure</span></span></td>
<td><span data-ttu-id="3c8c3-139">薪酬结构是一个薪酬矩阵，其付薪比率与每个级别的参考点关联。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-140">资格规则</span><span class="sxs-lookup"><span data-stu-id="3c8c3-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="3c8c3-141">资格规则用于标识特定作业、作业职能、作业类型、部门、工会或由特定薪酬计划覆盖的薪酬地区的员工。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="3c8c3-142">您必须为可变和固定薪酬计划创建资格规则，以便在计划中登记员工。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="3c8c3-143">指定薪酬计划的资格规则后，可以定义将要应用于计划所覆盖的工作的一组级别。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-144">付薪频率</span><span class="sxs-lookup"><span data-stu-id="3c8c3-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="3c8c3-145">付薪频率用于定义指定薪酬的时段。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="3c8c3-146">例如，付薪频率帮助您理解薪酬金额是否指定为年薪与付薪比率。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="3c8c3-147">付薪频率还用于设置换算系数以便将薪酬金额从按月、周、小时的付薪频率转换为按年的付薪频率。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-148">薪酬地区</span><span class="sxs-lookup"><span data-stu-id="3c8c3-148">Compensation regions</span></span></td>
<td><span data-ttu-id="3c8c3-149">付薪区域基于工作地点的位置用于指定员工薪酬。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-150">控制点</span><span class="sxs-lookup"><span data-stu-id="3c8c3-150">Control point</span></span></td>
<td><span data-ttu-id="3c8c3-151">该控制点定义您认为处于某一薪酬水平的所有员工的理想付薪比率是什么。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="3c8c3-152">对于等级计划结构，控制点通常是范围的中点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="3c8c3-153">分段结构很少用于控制点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-153">Band structures rarely use control points.</span></span> <span data-ttu-id="3c8c3-154">您可以在“固定薪酬计划”窗体中指定固定薪酬计划的控制点。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-155">工作职能</span><span class="sxs-lookup"><span data-stu-id="3c8c3-155">Job functions</span></span></td>
<td><span data-ttu-id="3c8c3-156">工作职能用于分类和筛选针对特定工作的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-157">工作类型</span><span class="sxs-lookup"><span data-stu-id="3c8c3-157">Job types</span></span></td>
<td><span data-ttu-id="3c8c3-158">工作类型用于分类和筛选针对特定工作的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-159">可变薪酬类型</span><span class="sxs-lookup"><span data-stu-id="3c8c3-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="3c8c3-160">在可变薪酬计划中设置可变薪酬类型（如股票奖励或现金奖励）。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-161">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="3c8c3-161">Compensation grids</span></span></td>
<td><span data-ttu-id="3c8c3-162">薪酬网格包含薪酬结构。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="3c8c3-163">薪酬网格可以由一个或多个薪酬计划使用。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c8c3-164">绩效计划</span><span class="sxs-lookup"><span data-stu-id="3c8c3-164">Performance plans</span></span></td>
<td><span data-ttu-id="3c8c3-165">绩效计划用于蒋性能与分配矩阵表进行关联，以便以按绩效付薪策略使用此计划。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c8c3-166">绩效等级</span><span class="sxs-lookup"><span data-stu-id="3c8c3-166">Performance ratings</span></span></td>
<td><span data-ttu-id="3c8c3-167">薪酬等级用于绩效计划中，以确定优异奖或绩效奖的金额。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="3c8c3-168">流程事件</span><span class="sxs-lookup"><span data-stu-id="3c8c3-168">Process events</span></span>
<span data-ttu-id="3c8c3-169">流程事件是用于计算特定期间在一个或多个固定或可变薪酬计划中登记的所有员工的薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="3c8c3-170">可以重复运行流程事件以便测试或更新薪酬结果。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="3c8c3-171">薪酬事件</span><span class="sxs-lookup"><span data-stu-id="3c8c3-171">Compensation events</span></span>
-------------------

<span data-ttu-id="3c8c3-172">每次运行流程事件时，都会创建一个薪酬事件。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="3c8c3-173">薪酬事件包含该流程事件中包括的每个员工的薪酬流程的结果。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="3c8c3-174">当计算正确时，您可以加载薪酬事件以更新受流程事件影响的员工的薪酬记录。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="3c8c3-175">建议</span><span class="sxs-lookup"><span data-stu-id="3c8c3-175">Recommendations</span></span>
<span data-ttu-id="3c8c3-176">在运行流程事件后，可以建议基于流程事件的计算所得指导性对员工的调薪或奖励金额的调整。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="3c8c3-177">若要向员工的建议，必须在您设置了薪酬计划或设置流程事件时启用建议。</span><span class="sxs-lookup"><span data-stu-id="3c8c3-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




