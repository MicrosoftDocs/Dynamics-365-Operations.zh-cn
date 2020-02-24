---
title: 设置作业组件
description: 本文介绍工作中可包含的概念性元素，并提供有关如何在组织中使用这些元素的示例。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 02475cdc23565c1d49c9f1bb6901101b16acf3a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008255"
---
# <a name="set-up-the-components-of-a-job"></a><span data-ttu-id="a5bc4-103">设置作业组件</span><span class="sxs-lookup"><span data-stu-id="a5bc4-103">Set up the components of a job</span></span>

<span data-ttu-id="a5bc4-104">本文介绍工作中可包含的概念性元素，并提供有关如何在组织中使用这些元素的示例。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-104">This article describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="a5bc4-105">必须先设置一些参考信息，才能创建工作。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="a5bc4-106">创建的工作只能有一个名称。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-106">You can create a job that has only a name.</span></span> <span data-ttu-id="a5bc4-107">但是，通过添加更多信息（如职称“，可以为向其分配工作的职位提供默认值。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="a5bc4-108">此外，还可以将输入的一些信息用于筛选特定工作的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="a5bc4-109">如果要设置可用于筛选特定工作的薪酬计划的资格，应在设置工作之前设置工作职能和工作类型。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="a5bc4-110">通过提供这些默认值，可以在为工作添加职位时节约时间。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="a5bc4-111">某些工作详细信息（如职称、类型和职能）有时效性。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="a5bc4-112">如果今天创建了工作，但未及时添加这些详细信息，然后在创建日期之后查看该工作，将不显示这些详细信息。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="a5bc4-113">因此，即使暂时不需要这些参考信息，也应该创建其中的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="a5bc4-114">这样就可以在创建新工作时向其添加这些信息。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="a5bc4-115">职称</span><span class="sxs-lookup"><span data-stu-id="a5bc4-115">Job titles</span></span>
<span data-ttu-id="a5bc4-116">创建工作前，您必须为这些工作设置职称。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="a5bc4-117">职位从这些职位所关联的作业中继承工作职称。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="a5bc4-118">可使用**职称**页面维护职称，可通过使用搜索功能打开该页面。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="a5bc4-119">在 **职称** 页面中，输入计划用于工作的职称。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-119">On the \*\*Titles \*\*page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="a5bc4-120">工作类型</span><span class="sxs-lookup"><span data-stu-id="a5bc4-120">Job types</span></span>
<span data-ttu-id="a5bc4-121">可使用工作类型将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="a5bc4-122">不需要工作类型。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-122">Job types aren't required.</span></span> <span data-ttu-id="a5bc4-123">但是，如果您在设置薪酬管理的资格规则时计划使用作业类型，则您应在设置作业前设置作业类型。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="a5bc4-124">例如，工作类型可以是全职、兼职或工资和小时工资。.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="a5bc4-125">可通过使用**工作类型**页面维护工作类型。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="a5bc4-126">在**工作类型**页面中，输入工作类型的名称和简要描述。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="a5bc4-127">在**免除情况**字段中，选择以下选项之一以指示拥有此工作类型工作的公平劳动标准法案 (FLSA) 免除情况。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="a5bc4-128">**免除** – 工作从 FLSA 规定下的加班时间中免除。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="a5bc4-129">**不免除** – 工作不从 FLSA 规定下的加班时间中免除。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="a5bc4-130">**不使用** – FLSA 覆盖范围不适用。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="a5bc4-131">工作职能</span><span class="sxs-lookup"><span data-stu-id="a5bc4-131">Job functions</span></span>
<span data-ttu-id="a5bc4-132">工作职能介绍高级别智能类别，并关联高级别职责。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="a5bc4-133">不需要工作职能。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-133">Job functions aren't required.</span></span> <span data-ttu-id="a5bc4-134">可以将工作职能与工作类型一起使用，以筛选用于特定工作的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="a5bc4-135">可以通过在**资格规则**页面中设置资格规则，将工作职能和工作类型与薪酬计划相关联。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="a5bc4-136">然后可以将一组级别附加到应用于工作类型与工作职的特定组合的薪酬计划，该组合是您通过资格规则定义的。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="a5bc4-137">（这些功能适用于固定薪酬计划和可变薪酬计划。）但是，如果您在设置薪酬管理的资格规则时计划使用工作职能，那么应该在设置作业前就设置好工作职能。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="a5bc4-138">下表显示工作职能的一些示例。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="a5bc4-139">作业</span><span class="sxs-lookup"><span data-stu-id="a5bc4-139">Job</span></span>           | <span data-ttu-id="a5bc4-140">工作职能</span><span class="sxs-lookup"><span data-stu-id="a5bc4-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="a5bc4-141">销售经理</span><span class="sxs-lookup"><span data-stu-id="a5bc4-141">Sales manager</span></span> | <span data-ttu-id="a5bc4-142">中级经理</span><span class="sxs-lookup"><span data-stu-id="a5bc4-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="a5bc4-143">会计师</span><span class="sxs-lookup"><span data-stu-id="a5bc4-143">Accountant</span></span>    | <span data-ttu-id="a5bc4-144">专业人员</span><span class="sxs-lookup"><span data-stu-id="a5bc4-144">Professionals</span></span>        |

<span data-ttu-id="a5bc4-145">可通过使用**工作职能**页面维护工作职能。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="a5bc4-146">在**工作职能**页面中，输入工作职能的标识代码和简要描述。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="a5bc4-147">作业任务</span><span class="sxs-lookup"><span data-stu-id="a5bc4-147">Job tasks</span></span>
<span data-ttu-id="a5bc4-148">工作任务描述担任某项工作的职位的工作人员必须完成的基本任务。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="a5bc4-149">同一工作任务可以添加到多个工作，以及使用这些工作任务的工作的职位。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="a5bc4-150">下表显示工作任务的一些示例。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a5bc4-151">作业</span><span class="sxs-lookup"><span data-stu-id="a5bc4-151">Job</span></span></th>
<th><span data-ttu-id="a5bc4-152">作业任务</span><span class="sxs-lookup"><span data-stu-id="a5bc4-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5bc4-153">销售经理</span><span class="sxs-lookup"><span data-stu-id="a5bc4-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="a5bc4-154"><strong>Perf-review</strong> – 查看每个销售人员的作业绩效。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-154"><strong>Perf-review</strong> – Review each salesperson&#39;s job performance.</span></span></li>
<li><span data-ttu-id="a5bc4-155"><strong>Abs-review</strong> – 批准或拒绝每个销售人员的缺勤请求或登记。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-155"><strong>Abs-review</strong> – Approve or reject each salesperson&#39;s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5bc4-156">会计师</span><span class="sxs-lookup"><span data-stu-id="a5bc4-156">Accountant</span></span></td>
<td><span data-ttu-id="a5bc4-157"><strong>FIN-Report</strong> – 向首席财务官呈交每周财务报表。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5bc4-158">可通过使用**工作任务**页面维护工作任务。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="a5bc4-159">在**工作任务**页面中，输入工作任务的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="a5bc4-160">在**注释**字段中，可以选择输入更多信息。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="a5bc4-161">无需更改此处输入的注释，即可针对特定工作更新注释。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="a5bc4-162">职责范围</span><span class="sxs-lookup"><span data-stu-id="a5bc4-162">Areas of responsibility</span></span>
<span data-ttu-id="a5bc4-163">可使用职责范围指示担任工作的职位的工作人员负责的工作角色、流程和产品。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="a5bc4-164">例如，对于名为“会计师”的工作，一个职责范围可能是“产品 A 的财务申报”。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="a5bc4-165">可通过使用**职责范围**页面维护职责范围，您可以通过使用搜索功能找到此页面。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="a5bc4-166">在**职责范围**页面中，输入职责范围的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="a5bc4-167">在**注释**字段中，可以选择输入更多信息。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="a5bc4-168">无需更改此处输入的注释，即可针对特定工作更新注释。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="steps-for-creating-a-job"></a><span data-ttu-id="a5bc4-169">作业创建步骤</span><span class="sxs-lookup"><span data-stu-id="a5bc4-169">Steps for creating a job</span></span>
<span data-ttu-id="a5bc4-170">请参阅[定义新作业](../fin-and-ops/hr/tasks/define-new-jobs.md)一文了解创建新作业的分步过程。</span><span class="sxs-lookup"><span data-stu-id="a5bc4-170">Refer to the [Define new jobs](../fin-and-ops/hr/tasks/define-new-jobs.md) article for the step-by-step procedure for creating a new job.</span></span> 
