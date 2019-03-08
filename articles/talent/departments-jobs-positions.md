---
title: 使用部门、工作和职位组织您的劳动力
description: 部门、作业和职位在人力资源中维护的组织元素。 本主题介绍有关这些元素的概念信息。
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 8b74542b85810409e062a42e323c0527711d562f
ms.sourcegitcommit: 49a642cd5e0519e381ff558f59c993ee77f55108
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "374389"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="7bda4-104">使用部门、工作和职位组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="7bda4-104">Organize your workforce by using departments, jobs, and positions</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="7bda4-105">部门、作业和职位在人力资源中维护的组织元素。</span><span class="sxs-lookup"><span data-stu-id="7bda4-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="7bda4-106">本主题介绍有关这些元素的概念信息。</span><span class="sxs-lookup"><span data-stu-id="7bda4-106">This topic describes conceptual information about these elements.</span></span> 

<span data-ttu-id="7bda4-107">以下示例用于说明本主题中描述的概念。</span><span class="sxs-lookup"><span data-stu-id="7bda4-107">The following example is used to illustrate the concepts described in this topic.</span></span>

|<span data-ttu-id="7bda4-108">**部门**</span><span class="sxs-lookup"><span data-stu-id="7bda4-108">**Department**</span></span>|<span data-ttu-id="7bda4-109">**职位**</span><span class="sxs-lookup"><span data-stu-id="7bda4-109">**Position**</span></span>|<span data-ttu-id="7bda4-110">**作业**</span><span class="sxs-lookup"><span data-stu-id="7bda4-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="7bda4-111">**销售**</span><span class="sxs-lookup"><span data-stu-id="7bda4-111">**Sales**</span></span>|<span data-ttu-id="7bda4-112">销售经理（东部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-112">Sales manager (East)</span></span>|<span data-ttu-id="7bda4-113">销售经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-113">Sales manager</span></span>|
|<span data-ttu-id="7bda4-114">**销售**</span><span class="sxs-lookup"><span data-stu-id="7bda4-114">**Sales**</span></span>|<span data-ttu-id="7bda4-115">销售经理（西部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-115">Sales manager (West)</span></span>|<span data-ttu-id="7bda4-116">销售经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-116">Sales manager</span></span>|
|<span data-ttu-id="7bda4-117">**销售**</span><span class="sxs-lookup"><span data-stu-id="7bda4-117">**Sales**</span></span>|<span data-ttu-id="7bda4-118">销售经理（中部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-118">Sales manager (Central)</span></span>|<span data-ttu-id="7bda4-119">销售经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-119">Sales manager</span></span>|
|<span data-ttu-id="7bda4-120">**核算**</span><span class="sxs-lookup"><span data-stu-id="7bda4-120">**Accounting**</span></span>|<span data-ttu-id="7bda4-121">会计主管</span><span class="sxs-lookup"><span data-stu-id="7bda4-121">Accounting supervisor</span></span>|<span data-ttu-id="7bda4-122">会计经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-122">Accounting manager</span></span>|
|<span data-ttu-id="7bda4-123">**核算**</span><span class="sxs-lookup"><span data-stu-id="7bda4-123">**Accounting**</span></span>|<span data-ttu-id="7bda4-124">会计-A</span><span class="sxs-lookup"><span data-stu-id="7bda4-124">Accounting-A</span></span>|<span data-ttu-id="7bda4-125">会计师</span><span class="sxs-lookup"><span data-stu-id="7bda4-125">Accountant</span></span>|
|<span data-ttu-id="7bda4-126">**人力资源**</span><span class="sxs-lookup"><span data-stu-id="7bda4-126">**Human resources**</span></span>|<span data-ttu-id="7bda4-127">人力资源经理（东部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-127">HR manager (East)</span></span>|<span data-ttu-id="7bda4-128">人力资源经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-128">HR manager</span></span>|
|<span data-ttu-id="7bda4-129">**人力资源**</span><span class="sxs-lookup"><span data-stu-id="7bda4-129">**Human resources**</span></span>|<span data-ttu-id="7bda4-130">人力资源经理（西部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-130">HR manager (West)</span></span>|<span data-ttu-id="7bda4-131">人力资源经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-131">HR manager</span></span>|
|<span data-ttu-id="7bda4-132">**人力资源**</span><span class="sxs-lookup"><span data-stu-id="7bda4-132">**Human resources**</span></span>|<span data-ttu-id="7bda4-133">人力资源经理（中部）</span><span class="sxs-lookup"><span data-stu-id="7bda4-133">HR manager (Central)</span></span>|<span data-ttu-id="7bda4-134">人力资源经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="7bda4-135">部门</span><span class="sxs-lookup"><span data-stu-id="7bda4-135">Departments</span></span>
------------

<span data-ttu-id="7bda4-136">部门是表示组织的类别或功能区域的运营单位，负责组织的特定区域（例如销售或核算）。</span><span class="sxs-lookup"><span data-stu-id="7bda4-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="7bda4-137">部门用于报告功能区域，并且可能具有损益责任。</span><span class="sxs-lookup"><span data-stu-id="7bda4-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="7bda4-138">此外，部门还可能包括成本中心组。</span><span class="sxs-lookup"><span data-stu-id="7bda4-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="7bda4-139">销售、核算和人力资源部门是组织中的部门的一些示例。</span><span class="sxs-lookup"><span data-stu-id="7bda4-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="7bda4-140">作业和职位</span><span class="sxs-lookup"><span data-stu-id="7bda4-140">Jobs and positions</span></span>
<span data-ttu-id="7bda4-141">作业是执行作业的人员需要承担的任务和责任的集合。</span><span class="sxs-lookup"><span data-stu-id="7bda4-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="7bda4-142">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="7bda4-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="7bda4-143">作业所需的职责范围、作业任务、工作职能、技能、教育信息和证书也是与作业关联职位所需的。</span><span class="sxs-lookup"><span data-stu-id="7bda4-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="7bda4-144">作业任务</span><span class="sxs-lookup"><span data-stu-id="7bda4-144">Job tasks</span></span>

<span data-ttu-id="7bda4-145">您可以创建描述基本任务的作业任务，位于针对该作业的职位的工作人员必须完成该任务。</span><span class="sxs-lookup"><span data-stu-id="7bda4-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="7bda4-146">同一作业任务可以添加到多个作业，而针对这些作业的职位将继承这些作业任务。</span><span class="sxs-lookup"><span data-stu-id="7bda4-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="7bda4-147">下表中列出了一些工作任务示例。</span><span class="sxs-lookup"><span data-stu-id="7bda4-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7bda4-148">作业</span><span class="sxs-lookup"><span data-stu-id="7bda4-148">Job</span></span></th>
<th><span data-ttu-id="7bda4-149">作业任务</span><span class="sxs-lookup"><span data-stu-id="7bda4-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bda4-150">销售经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="7bda4-151"><span class="input">Perf-review</span> – 查看每个销售人员的作业绩效。</span><span class="sxs-lookup"><span data-stu-id="7bda4-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="7bda4-152"><span class="input">Abs-review</span> – 批准或拒绝每个销售人员的缺勤请求或登记。</span><span class="sxs-lookup"><span data-stu-id="7bda4-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bda4-153">会计师</span><span class="sxs-lookup"><span data-stu-id="7bda4-153">Accountant</span></span></td>
<td><span data-ttu-id="7bda4-154"><span class="input">FIN-Report</span> – 向首席财务官呈交每周财务报表。</span><span class="sxs-lookup"><span data-stu-id="7bda4-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="7bda4-155">工作职能</span><span class="sxs-lookup"><span data-stu-id="7bda4-155">Job functions</span></span>

<span data-ttu-id="7bda4-156">工作职能就像作业任务。</span><span class="sxs-lookup"><span data-stu-id="7bda4-156">Job functions are like job tasks.</span></span> <span data-ttu-id="7bda4-157">工作职能描述分配给作业的一个或多个任务、职责或责任。</span><span class="sxs-lookup"><span data-stu-id="7bda4-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="7bda4-158">工作职能可分配给作业并用于设置和实现薪酬计划的资格规则。</span><span class="sxs-lookup"><span data-stu-id="7bda4-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="7bda4-159">下表中列出了一些工作职能示例。</span><span class="sxs-lookup"><span data-stu-id="7bda4-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="7bda4-160">作业</span><span class="sxs-lookup"><span data-stu-id="7bda4-160">Job</span></span>           | <span data-ttu-id="7bda4-161">工作职能</span><span class="sxs-lookup"><span data-stu-id="7bda4-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="7bda4-162">销售经理</span><span class="sxs-lookup"><span data-stu-id="7bda4-162">Sales manager</span></span> | <span data-ttu-id="7bda4-163">Mng-people – 管理向您报告的人员。</span><span class="sxs-lookup"><span data-stu-id="7bda4-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="7bda4-164">会计师</span><span class="sxs-lookup"><span data-stu-id="7bda4-164">Accountant</span></span>    | <span data-ttu-id="7bda4-165">FIN-Review – 维护一组帐户的财务数据。</span><span class="sxs-lookup"><span data-stu-id="7bda4-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="7bda4-166">工作类型</span><span class="sxs-lookup"><span data-stu-id="7bda4-166">Job types</span></span>

<span data-ttu-id="7bda4-167">使用作业类型将类似的作业分类到各类别。</span><span class="sxs-lookup"><span data-stu-id="7bda4-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="7bda4-168">作业类型就像工作职能一样，可分配给作业并用于设置和实现薪酬计划的资格规则。</span><span class="sxs-lookup"><span data-stu-id="7bda4-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="7bda4-169">下表中包含作业类型的一些示例：</span><span class="sxs-lookup"><span data-stu-id="7bda4-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="7bda4-170">全职</span><span class="sxs-lookup"><span data-stu-id="7bda4-170">Full-time</span></span>
-   <span data-ttu-id="7bda4-171">兼职</span><span class="sxs-lookup"><span data-stu-id="7bda4-171">Part-time</span></span>
-   <span data-ttu-id="7bda4-172">薪金</span><span class="sxs-lookup"><span data-stu-id="7bda4-172">Salary</span></span>
-   <span data-ttu-id="7bda4-173">小时工资</span><span class="sxs-lookup"><span data-stu-id="7bda4-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="7bda4-174">职责范围</span><span class="sxs-lookup"><span data-stu-id="7bda4-174">Areas of responsibility</span></span>

<span data-ttu-id="7bda4-175">使用职责范围指示处于针对该作业的职位的工作人员将负责的工作角色、流程和产品。</span><span class="sxs-lookup"><span data-stu-id="7bda4-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="7bda4-176">名为“会计师”的工作的职责范围的一个示例可能是“产品 A 的财务报告”。</span><span class="sxs-lookup"><span data-stu-id="7bda4-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="7bda4-177">位置</span><span class="sxs-lookup"><span data-stu-id="7bda4-177">Positions</span></span>
----------

<span data-ttu-id="7bda4-178">职位是更低级别的组织层次结构中的重要元素。</span><span class="sxs-lookup"><span data-stu-id="7bda4-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="7bda4-179">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="7bda4-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="7bda4-180">例如，职位“销售经理（东部）”只是与工作“销售经理”关联的职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="7bda4-181">各职位存在于部门中，并分配给工作人员。</span><span class="sxs-lookup"><span data-stu-id="7bda4-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="7bda4-182">职位创建和维护</span><span class="sxs-lookup"><span data-stu-id="7bda4-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="7bda4-183">您可以在易于访问的列表页中查看与职位先关的系统更改历史记录。</span><span class="sxs-lookup"><span data-stu-id="7bda4-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="7bda4-184">您可以创建您的用户可以在创建或修改职位时选择的原因代码。</span><span class="sxs-lookup"><span data-stu-id="7bda4-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="7bda4-185">您可以创建人事行动类型并将编号规则分配给人事操作。</span><span class="sxs-lookup"><span data-stu-id="7bda4-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="7bda4-186">您可以设置工作流，以便职位添加和更改可要求审核。</span><span class="sxs-lookup"><span data-stu-id="7bda4-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="7bda4-187">职位持续时间</span><span class="sxs-lookup"><span data-stu-id="7bda4-187">Position duration</span></span>

<span data-ttu-id="7bda4-188">每个职位都具有职位处于有效状态的时间长度。</span><span class="sxs-lookup"><span data-stu-id="7bda4-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="7bda4-189">此时间长度被称为持续时间。</span><span class="sxs-lookup"><span data-stu-id="7bda4-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="7bda4-190">例如，夏季职位的持续时间可能为 2015 年 5 月 1 日至 2015 年 8 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="7bda4-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="7bda4-191">工作人员分配</span><span class="sxs-lookup"><span data-stu-id="7bda4-191">Worker assignments</span></span>

<span data-ttu-id="7bda4-192">在您将工作人员分配到职位时，您填写该职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="7bda4-193">您可以将工作人员分配到多个职位，但一次只能将一名工作人员分配到职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="7bda4-194">报告关系</span><span class="sxs-lookup"><span data-stu-id="7bda4-194">Reporting relationships</span></span>

<span data-ttu-id="7bda4-195">职位是更低级别的组织层次结构中的重要元素。</span><span class="sxs-lookup"><span data-stu-id="7bda4-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="7bda4-196">在“职位”窗体中，您可以指定某个职位向其进行报告的职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="7bda4-197">将工作人员分配到向另一个职位报告的职位时，创建分配给两个职位的工作人员之间的报告关系。</span><span class="sxs-lookup"><span data-stu-id="7bda4-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="7bda4-198">例如，职位“会计师-A”向职位“会计主管”报告。</span><span class="sxs-lookup"><span data-stu-id="7bda4-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="7bda4-199">Kim Akers 分配到职位“会计主管”，而 Sanjay Patel 分配到职位“会计师-A”。</span><span class="sxs-lookup"><span data-stu-id="7bda4-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="7bda4-200">这意味着 Sanjay Patel 向 Kim Akers 报告。</span><span class="sxs-lookup"><span data-stu-id="7bda4-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="7bda4-201">如果您的组织使用矩阵层次结构或其他自定义层次结构，则可以设置职位层次结构类型，然后将报告关系添加到您设置的每个层次结构类型的职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="7bda4-202">例如，Lori Penor 是 Adventure Works 的总经理，并分配到职位“总经理”。</span><span class="sxs-lookup"><span data-stu-id="7bda4-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="7bda4-203">Lori 管理用于清洗小机械的产品的开发。</span><span class="sxs-lookup"><span data-stu-id="7bda4-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="7bda4-204">Lori 要求会计帮助其为开发产品融资。</span><span class="sxs-lookup"><span data-stu-id="7bda4-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="7bda4-205">因此，她招聘 Sanjay Patel 为其会计。</span><span class="sxs-lookup"><span data-stu-id="7bda4-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="7bda4-206">Sanjay 直接向 Kim Akers 报告，并与 Lori Penor 一起从事其与为开发小机械清洗剂融资相关的工作。</span><span class="sxs-lookup"><span data-stu-id="7bda4-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="7bda4-207">对于前面的示例，您可以完成以下任务来设置 Sanjay Patel 和 Lori Penor 之间的工作关系：</span><span class="sxs-lookup"><span data-stu-id="7bda4-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="7bda4-208">创建一个名为“小机械”的自定义职位层次结构类型，以创建包括负责从事小机械清洗剂产品工作的职位的层次结构。</span><span class="sxs-lookup"><span data-stu-id="7bda4-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="7bda4-209">在“小机械”层次结构中，将总经理职位分配为会计师-A 职位向其进行报告的职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="7bda4-210">使用职位层次结构查看职位的报告结构。</span><span class="sxs-lookup"><span data-stu-id="7bda4-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="7bda4-211">如果您有多个职位层次结构，则可在职位层次结构中查看每个层次结构类型的层次结构。</span><span class="sxs-lookup"><span data-stu-id="7bda4-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="7bda4-212">此外，您还可按职位 ID 或分配到职位的工作人员的姓名搜索职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="7bda4-213">职位层次结构的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="7bda4-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="7bda4-214">生效日期记录</span><span class="sxs-lookup"><span data-stu-id="7bda4-214">Date effective records</span></span>
<span data-ttu-id="7bda4-215">对于某些记录，可以指定对记录的将来的更改。</span><span class="sxs-lookup"><span data-stu-id="7bda4-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="7bda4-216">以下信息是生效日期。</span><span class="sxs-lookup"><span data-stu-id="7bda4-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7bda4-217">记录</span><span class="sxs-lookup"><span data-stu-id="7bda4-217">Records</span></span></th>
<th><span data-ttu-id="7bda4-218">生效日期信息</span><span class="sxs-lookup"><span data-stu-id="7bda4-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bda4-219">作业</span><span class="sxs-lookup"><span data-stu-id="7bda4-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="7bda4-220">某些详细的作业信息</span><span class="sxs-lookup"><span data-stu-id="7bda4-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="7bda4-221">作业分类信息</span><span class="sxs-lookup"><span data-stu-id="7bda4-221">Job classification information</span></span></li>
<li><span data-ttu-id="7bda4-222">薪酬信息</span><span class="sxs-lookup"><span data-stu-id="7bda4-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bda4-223">位置</span><span class="sxs-lookup"><span data-stu-id="7bda4-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="7bda4-224">某些详细的职位信息</span><span class="sxs-lookup"><span data-stu-id="7bda4-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="7bda4-225">工作人员分配</span><span class="sxs-lookup"><span data-stu-id="7bda4-225">Worker assignments</span></span></li>
<li><span data-ttu-id="7bda4-226">职位持续时间</span><span class="sxs-lookup"><span data-stu-id="7bda4-226">Position durations</span></span></li>
<li><span data-ttu-id="7bda4-227">职位层次结构</span><span class="sxs-lookup"><span data-stu-id="7bda4-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7bda4-228">您可修改针对职位和作业的前一表中提及的信息，并指定对职位或作业进行的修改的生效日期。</span><span class="sxs-lookup"><span data-stu-id="7bda4-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="7bda4-229">例如，职位只能分配给一名工作人员，但分配到会计师-A 的 Sanjay Patel 将在两周内离职。</span><span class="sxs-lookup"><span data-stu-id="7bda4-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="7bda4-230">Joe Healy 将在 Sanjay Patel 离职时代替其职位。</span><span class="sxs-lookup"><span data-stu-id="7bda4-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="7bda4-231">即使 Sanjay 仍分配到他的位置，您仍可以将 Joe Healy 分配到同一个位置，以便分配仅在 Sanjay 的最后一天后生效。</span><span class="sxs-lookup"><span data-stu-id="7bda4-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>





