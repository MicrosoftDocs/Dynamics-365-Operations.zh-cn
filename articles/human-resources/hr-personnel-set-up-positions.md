---
title: 设置职位
description: 职位是更低级别的组织层次结构中的重要元素。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22598869a673e91dd17546c46eb12c4d53ef0c9b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008250"
---
# <a name="set-up-positions"></a><span data-ttu-id="342cb-103">设置职位</span><span class="sxs-lookup"><span data-stu-id="342cb-103">Set up positions</span></span>



<span data-ttu-id="342cb-104">职位是更低级别的组织层次结构中的重要元素。</span><span class="sxs-lookup"><span data-stu-id="342cb-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="342cb-105">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="342cb-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="342cb-106">例如，职位“销售经理（东部）”是与工作“销售经理”关联的职位。</span><span class="sxs-lookup"><span data-stu-id="342cb-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="342cb-107">职位存在于部门中，可能只有一个工作人员与之关联。</span><span class="sxs-lookup"><span data-stu-id="342cb-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="342cb-108">在此任务中，我们将全面介绍创建职位所需的各个步骤。</span><span class="sxs-lookup"><span data-stu-id="342cb-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="342cb-109">此过程专门面向人力资源专员。</span><span class="sxs-lookup"><span data-stu-id="342cb-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="342cb-110">单击“劳动力管理”。</span><span class="sxs-lookup"><span data-stu-id="342cb-110">Click Workforce management.</span></span>
2. <span data-ttu-id="342cb-111">单击“空缺职位”。</span><span class="sxs-lookup"><span data-stu-id="342cb-111">Click Open positions.</span></span>
3. <span data-ttu-id="342cb-112">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="342cb-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="342cb-113">在“工作”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="342cb-114">会自动将作业描述、职称和全职等效雇用系数从所选作业复制到职位。</span><span class="sxs-lookup"><span data-stu-id="342cb-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="342cb-115">ResolveChanges 工作。</span><span class="sxs-lookup"><span data-stu-id="342cb-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="342cb-116">单击“创建职位”。</span><span class="sxs-lookup"><span data-stu-id="342cb-116">Click Create position.</span></span>
7. <span data-ttu-id="342cb-117">在“部门”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="342cb-118">在“职位类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="342cb-119">在“薪酬地区”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="342cb-120">“薪酬区域”字段确定适用于该职位的员工的薪酬资格规则和固定增加预算。</span><span class="sxs-lookup"><span data-stu-id="342cb-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="342cb-121">在“可用于分配”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="342cb-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="342cb-122">展开“职位持续时间”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="342cb-123">默认情况下基于之前输入的启用和报废日期输入职位持续时间。</span><span class="sxs-lookup"><span data-stu-id="342cb-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="342cb-124">展开“职位报告”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="342cb-125">将工作人员分配到向另一个职位报告的职位时，创建分配给两个职位的工作人员之间的直接报告关系。</span><span class="sxs-lookup"><span data-stu-id="342cb-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="342cb-126">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="342cb-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="342cb-127">在“报告”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="342cb-128">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="342cb-128">Click Create.</span></span>
16. <span data-ttu-id="342cb-129">展开“工作人员分配”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="342cb-130">展开“关系”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="342cb-131">如果您的组织使用矩阵层次结构或其他自定义层次结构，则可以设置职位层次结构类型，然后将报告关系添加到您设置的每个层次结构类型的职位。</span><span class="sxs-lookup"><span data-stu-id="342cb-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="342cb-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="342cb-132">Click Add.</span></span>
19. <span data-ttu-id="342cb-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="342cb-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="342cb-134">在“层次结构名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="342cb-135">在“直接上级职位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="342cb-136">展开“工资单”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="342cb-137">在“付薪周期”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="342cb-138">在“支付方”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="342cb-139">在“年度常规时间(小时)”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="342cb-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="342cb-140">这是此职位的工作人员预期每年工作的定期支付工时数。</span><span class="sxs-lookup"><span data-stu-id="342cb-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="342cb-141">展开“工会”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="342cb-142">折叠“工会”部分。</span><span class="sxs-lookup"><span data-stu-id="342cb-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="342cb-143">扩展财务维度区段。</span><span class="sxs-lookup"><span data-stu-id="342cb-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="342cb-144">在“分配模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="342cb-145">在“部门”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="342cb-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="342cb-146">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="342cb-146">Click Save.</span></span>
