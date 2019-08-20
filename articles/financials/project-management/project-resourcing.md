---
title: 项目资源
description: 本主题提供有关项目资源的信息。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f6f9c4a6b89997d3d5223d56a5beb4bc11898bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838431"
---
# <a name="project-resourcing"></a><span data-ttu-id="485b3-103">项目资源</span><span class="sxs-lookup"><span data-stu-id="485b3-103">Project resourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="485b3-104">本主题提供有关项目资源的信息。</span><span class="sxs-lookup"><span data-stu-id="485b3-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="485b3-105">项目经理和资源经理在项目计划阶段的一个挑战是资源分配，他们必须在此确定和预留处理项目所需的正确资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="485b3-106">在 Microsoft Dynamics 365 for Finance and Operations 中，项目的资源能力可以定义预留给特定参与或参与的一部分被视为临时资源的角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-106">In Microsoft Dynamics 365 for Finance and Operations, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="485b3-107">此资源类型允许项目经理和资源经理完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="485b3-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="485b3-108">定义具有所需能力的角色，以便轻松匹配资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="485b3-109">使用角色基于预留资源定义初始约定计划。</span><span class="sxs-lookup"><span data-stu-id="485b3-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="485b3-110">基于分配的角色和项目的资源估计成本和确定初始预算。</span><span class="sxs-lookup"><span data-stu-id="485b3-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="485b3-111">使用角色估计每个约定所需的资源预留的数量。</span><span class="sxs-lookup"><span data-stu-id="485b3-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="485b3-112">估计项目的整个生命周期所需的资源的数量。</span><span class="sxs-lookup"><span data-stu-id="485b3-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="485b3-113">通过使用初始资源分配设计工作分解结构 (WBS)。</span><span class="sxs-lookup"><span data-stu-id="485b3-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="485b3-114">[![项目生命周期](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="485b3-115">随着项目计划的继续，计划的资源可以替换为雇用的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="485b3-116">项目经理还可以在任何项目阶段返回和更新资源预留。</span><span class="sxs-lookup"><span data-stu-id="485b3-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="485b3-117">设置项目资源</span><span class="sxs-lookup"><span data-stu-id="485b3-117">Set up project resources</span></span>
<span data-ttu-id="485b3-118">您必须设置日历并将其与员工或工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="485b3-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="485b3-119">该日历用于计划项目和预留给该项目的资源的工作时间。</span><span class="sxs-lookup"><span data-stu-id="485b3-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="485b3-120">在日历设置期间，项目经理可以作为资源优化的一部分执行资源均衡。</span><span class="sxs-lookup"><span data-stu-id="485b3-120">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="485b3-121">基于日历安排，可以对资源设定限制。</span><span class="sxs-lookup"><span data-stu-id="485b3-121">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="485b3-122">可以在**日历**页中设置日历。</span><span class="sxs-lookup"><span data-stu-id="485b3-122">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="485b3-123">将工作人员设置为项目资源时，可以从您为其设置资源的公司中工作的工作人员中进行选择。</span><span class="sxs-lookup"><span data-stu-id="485b3-123">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="485b3-124">或者也可以从您的组织中的其他公司中选择工作人员。</span><span class="sxs-lookup"><span data-stu-id="485b3-124">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="485b3-125">这些工作人员被称为内部公司资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-125">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="485b3-126">以下过程阐述了如何将工作人员设置为贵公司中的项目资源以及如何设置内部公司项目资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-126">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="485b3-127">将工作人员设置为项目资源</span><span class="sxs-lookup"><span data-stu-id="485b3-127">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="485b3-128">在**工作人员**页的**工作人员**列表内，选择您添加为项目资源的工作人员，然后打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="485b3-128">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="485b3-129">在操作窗格中，选择**项目** &gt; **设置** &gt; **项目设置**。</span><span class="sxs-lookup"><span data-stu-id="485b3-129">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="485b3-130">选择日历，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="485b3-130">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="485b3-131">您还可以将资源的默认项目指定为预分配类型。</span><span class="sxs-lookup"><span data-stu-id="485b3-131">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="485b3-132">当资源经理或项目经理知道资源将提前处理哪些项目时，可以使用预分配。</span><span class="sxs-lookup"><span data-stu-id="485b3-132">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="485b3-133">预分配还可以基于项目赞助者或客户的请求。</span><span class="sxs-lookup"><span data-stu-id="485b3-133">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="485b3-134">要预分配一个项目，在**分配项目**页上，在**项目**选项卡上，在**其余项目**列表中，选择相应的项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-134">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="485b3-135">设置内部公司资源</span><span class="sxs-lookup"><span data-stu-id="485b3-135">Set up an intercompany resource</span></span>

<span data-ttu-id="485b3-136">将工作人员设置为内部公司资源时，必须完成借出公司和借入公司中的设置。</span><span class="sxs-lookup"><span data-stu-id="485b3-136">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

<span data-ttu-id="485b3-137">**在借出公司中**</span><span class="sxs-lookup"><span data-stu-id="485b3-137">**In the lending company**</span></span>

1. <span data-ttu-id="485b3-138">在 Finance and Operations 中，验证已选择借出公司，然后完成上一部分“将工作人员设置为项目资源”中的过程。</span><span class="sxs-lookup"><span data-stu-id="485b3-138">In Finance and Operations, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="485b3-139">在**内部公司会计**页，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-139">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="485b3-140">在**法人 ID** 字段中，选择借出公司。</span><span class="sxs-lookup"><span data-stu-id="485b3-140">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="485b3-141">根据需要填写其余字段，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="485b3-141">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="485b3-142">在**转让价格**页，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-142">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="485b3-143">在**借入实体**字段中，选择适当的公司。</span><span class="sxs-lookup"><span data-stu-id="485b3-143">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="485b3-144">如果要仅借给借入公司您在此部分开始时创建的资源，请在**资源**字段中选择您创建的资源的名称。</span><span class="sxs-lookup"><span data-stu-id="485b3-144">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="485b3-145">如果要将公司内的所有资源都提供给借入公司，请将**资源**字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="485b3-145">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="485b3-146">在**项目管理与核算参数**页的**内部公司**选项卡上，将**启用公司间资源计划编制和工时单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="485b3-146">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

<span data-ttu-id="485b3-147">**在借入公司中**</span><span class="sxs-lookup"><span data-stu-id="485b3-147">**In the borrowing company**</span></span>

- <span data-ttu-id="485b3-148">在**资源列表**页上的搜索筛选器中，输入您为借出公司创建的资源名称，以验证借入公司的资源列表中是否包含此名称。</span><span class="sxs-lookup"><span data-stu-id="485b3-148">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="485b3-149">管理资源能力</span><span class="sxs-lookup"><span data-stu-id="485b3-149">Manage resource competencies</span></span>
<span data-ttu-id="485b3-150">资源能力是资源管理必不可少的部分。</span><span class="sxs-lookup"><span data-stu-id="485b3-150">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="485b3-151">能力可用作确定具有正确的技能、教育、证书和项目经验比重的资源的基准。</span><span class="sxs-lookup"><span data-stu-id="485b3-151">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="485b3-152">您应该为每个资源设置此信息并定期更新它。</span><span class="sxs-lookup"><span data-stu-id="485b3-152">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="485b3-153">这样，您可以在项目资源分配期间匹配特定资源能力时让能力实现最大化。</span><span class="sxs-lookup"><span data-stu-id="485b3-153">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="485b3-154">[![例如技能、证书、教育和项目经验](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-154">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="485b3-155">以下过程说明如何设置资源的某些能力。</span><span class="sxs-lookup"><span data-stu-id="485b3-155">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="485b3-156">若要设置工作人员的能力，您可以使用“人力资源”中的**工作人员**列表页或“项目管理与核算”中的**资源**列表页。</span><span class="sxs-lookup"><span data-stu-id="485b3-156">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="485b3-157">对于以下过程，将使用“人力资源”中的**工作人员**列表页。</span><span class="sxs-lookup"><span data-stu-id="485b3-157">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="485b3-158">设置能力：证书</span><span class="sxs-lookup"><span data-stu-id="485b3-158">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="485b3-159">在**工作人员**列表页上，选择您要为其添加证书信息的工作人员的行。</span><span class="sxs-lookup"><span data-stu-id="485b3-159">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="485b3-160">在操作窗格的**工作人员**选项卡的**能力**组中，选择**证书**。</span><span class="sxs-lookup"><span data-stu-id="485b3-160">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="485b3-161">选择**新建**，然后在**证书类型**字段中选择 **PMP**。</span><span class="sxs-lookup"><span data-stu-id="485b3-161">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="485b3-162">在**开始日期**字段中，选择 **10/1/2015**，并选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="485b3-162">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="485b3-163">设置能力：技能</span><span class="sxs-lookup"><span data-stu-id="485b3-163">Set up competencies: Skills</span></span>

1. <span data-ttu-id="485b3-164">在**工作人员**列表页，确保仍然选择在上一过程中使用的工作人员。</span><span class="sxs-lookup"><span data-stu-id="485b3-164">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="485b3-165">然后在操作窗格的**工作人员**选项卡的**能力**组中，选择**技能**。</span><span class="sxs-lookup"><span data-stu-id="485b3-165">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="485b3-166">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-166">Select **New**.</span></span>
3. <span data-ttu-id="485b3-167">在**技能**字段中，选择**项目管理**。</span><span class="sxs-lookup"><span data-stu-id="485b3-167">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="485b3-168">在**级别**字段中选择 **5 专家**。</span><span class="sxs-lookup"><span data-stu-id="485b3-168">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="485b3-169">在**等级日期**字段中，选择 **1-/14/2014**。</span><span class="sxs-lookup"><span data-stu-id="485b3-169">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="485b3-170">在**年资**字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="485b3-170">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="485b3-171">选择**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="485b3-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="485b3-172">创建新项目</span><span class="sxs-lookup"><span data-stu-id="485b3-172">Create a new project</span></span>
1. <span data-ttu-id="485b3-173">在**项目管理**页上，选择**新项目**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="485b3-173">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="485b3-174">**项目类型：** 时间和材料</span><span class="sxs-lookup"><span data-stu-id="485b3-174">**Project type:** Time and material</span></span>
    - <span data-ttu-id="485b3-175">**项目名称：** XYZ 升级第 2 阶段</span><span class="sxs-lookup"><span data-stu-id="485b3-175">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="485b3-176">**项目组：** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="485b3-176">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="485b3-177">**项目合同 ID：** 00000002</span><span class="sxs-lookup"><span data-stu-id="485b3-177">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="485b3-178">选择**创建项目**。</span><span class="sxs-lookup"><span data-stu-id="485b3-178">Select **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="485b3-179">将资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="485b3-179">Assign a resource to a project</span></span>

1. <span data-ttu-id="485b3-180">在**工作人员**页上的**工作人员**列表中，选择您之前为其设置能力的工作人员的记录，并打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="485b3-180">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="485b3-181">在操作窗格的**项目**选项卡的**设置**组中，选择**分配项目**。</span><span class="sxs-lookup"><span data-stu-id="485b3-181">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="485b3-182">在**资源验证项目分配**页的**项目**选项卡的**将项目添加到所选项目**字段中，筛选 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-182">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="485b3-183">在**其余项目**窗格中，选择一个项目，然后选择箭头按钮将其添加到**所选项目**窗格中。</span><span class="sxs-lookup"><span data-stu-id="485b3-183">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="485b3-184">您也可以按自己的需要分配资源的类别。</span><span class="sxs-lookup"><span data-stu-id="485b3-184">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="485b3-185">类别类型可以是**成本**或**收入**。</span><span class="sxs-lookup"><span data-stu-id="485b3-185">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="485b3-186">类别类型由您的组织确定。</span><span class="sxs-lookup"><span data-stu-id="485b3-186">The category type is determined by your organization.</span></span> <span data-ttu-id="485b3-187">如果没有为资源分配类别，则 Finance and Operations 查找成本和收入工时价格的默认类别。</span><span class="sxs-lookup"><span data-stu-id="485b3-187">If no categories are assigned for a resource, Finance and Operations looks up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="485b3-188">设置项目资源和角色特征</span><span class="sxs-lookup"><span data-stu-id="485b3-188">Set up project resource and role characteristics</span></span>

<span data-ttu-id="485b3-189">项目经理可使用项目资源功能创建项目所需的角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-189">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="485b3-190">在确认的资源在预留资源期间仍未知时可以使用角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-190">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="485b3-191">角色可临时预留为计划资源，以便您可以继续项目计划阶段。</span><span class="sxs-lookup"><span data-stu-id="485b3-191">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="485b3-192">[![角色示例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-192">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="485b3-193">**场景**：Contoso 被雇用完成具有已审核项目章节的时间和材料项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-193">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="485b3-194">初级项目经理仍在完成项目的工作范围。</span><span class="sxs-lookup"><span data-stu-id="485b3-194">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="485b3-195">资源经理当前正在确定要预留的处理新项目的特定资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-195">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="485b3-196">由于项目的重要性质，项目出资人请求高级项目经理作为其中一个角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-196">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="485b3-197">如果初级项目经理在项目计划期间需要资源信息，资源经理必须获得新的资源并且定义定义系统中的角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-197">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="485b3-198">以下步骤显示资源经理如何设置高级项目经理角色并将资源特性与其关联。</span><span class="sxs-lookup"><span data-stu-id="485b3-198">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="485b3-199">之后，角色可用于搜索符合所需的资源能力的可用资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-199">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="485b3-200">在**设置角色**页上，选择**新建**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="485b3-200">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="485b3-201">**角色 ID：** 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="485b3-201">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="485b3-202">**描述：** 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="485b3-202">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="485b3-203">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-203">Select **Create**.</span></span>
3. <span data-ttu-id="485b3-204">选择**高级项目经理**角色，然后选择**配置特性**。</span><span class="sxs-lookup"><span data-stu-id="485b3-204">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="485b3-205">在**特性类型**字段中，选择**技能**。</span><span class="sxs-lookup"><span data-stu-id="485b3-205">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="485b3-206">在**可用特性**字段中，输入要搜索的技能。</span><span class="sxs-lookup"><span data-stu-id="485b3-206">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="485b3-207">在**特性类型**字段中，选择**证书**。</span><span class="sxs-lookup"><span data-stu-id="485b3-207">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="485b3-208">在**可用特性**字段中，输入您要搜索的证书类型。</span><span class="sxs-lookup"><span data-stu-id="485b3-208">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="485b3-209">将项目资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="485b3-209">Assign a project resource to a project</span></span>

1. <span data-ttu-id="485b3-210">在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-210">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="485b3-211">在**项目团队和计划编制**选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="485b3-211">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="485b3-212">在**角色**字段中，选择**团队成员**。</span><span class="sxs-lookup"><span data-stu-id="485b3-212">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="485b3-213">选择**从日历预订**。</span><span class="sxs-lookup"><span data-stu-id="485b3-213">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="485b3-214">在**资源可用性**页上，选择**查看设置**。</span><span class="sxs-lookup"><span data-stu-id="485b3-214">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="485b3-215">在**调整视图设置**页上，输入以下值：</span><span class="sxs-lookup"><span data-stu-id="485b3-215">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="485b3-216">**日期范围视图的格式：** 天</span><span class="sxs-lookup"><span data-stu-id="485b3-216">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="485b3-217">**显示可用性描述：** 是</span><span class="sxs-lookup"><span data-stu-id="485b3-217">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="485b3-218">**显示剩余产能：** 是</span><span class="sxs-lookup"><span data-stu-id="485b3-218">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="485b3-219">在资源列表中，选择某一资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-219">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="485b3-220">选择**硬性预订**和**全部产能**。</span><span class="sxs-lookup"><span data-stu-id="485b3-220">Select **Hard book** and **Full capacity**.</span></span>


### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="485b3-221">将资源分配给默认角色</span><span class="sxs-lookup"><span data-stu-id="485b3-221">Assign a resource to a default role</span></span>

<span data-ttu-id="485b3-222">为了帮助项目或资源经理，可以进一步深化到可以预留给项目的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-222">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="485b3-223">您可以将默认值角色与现有资源或新获取的资源进行关联。</span><span class="sxs-lookup"><span data-stu-id="485b3-223">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="485b3-224">例如，如果雇用了 Daniel，所以就有了经验和技能来填补“业务分析”角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-224">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="485b3-225">资源经理将该角色分配为 Daniel 的默认角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-225">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="485b3-226">因此，资源经理将 Daniel 添加到可处理项目的业务分析池中。</span><span class="sxs-lookup"><span data-stu-id="485b3-226">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="485b3-227">在资源预留期间，项目经理可以筛选可参与项目的角色资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-227">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="485b3-228">在履行资源期间执行多条件决定分析时，他们可以使用此信息作为一个条件。</span><span class="sxs-lookup"><span data-stu-id="485b3-228">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="485b3-229">他们还可以添加其他资源特征到筛选器来搜索具有指定项目的特定技能、教育和经验的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-229">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="485b3-230">**场景：** 已审核的项目已启动，并且高级项目经理角色在项目计划阶段预留为计划的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-230">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="485b3-231">资源经理现在已获得履行高级项目经理角色的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-231">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="485b3-232">在**资源列表**页上，选择 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="485b3-232">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="485b3-233">在**资源角色**页上，选择**新建**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="485b3-233">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="485b3-234">**生效日期：** 输入当前日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-234">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="485b3-235">**到期日期：** 输入**从不**。</span><span class="sxs-lookup"><span data-stu-id="485b3-235">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="485b3-236">**角色：** 输入**高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="485b3-236">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="485b3-237">选择**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="485b3-237">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="485b3-238">在**能力**选项卡上，添加 **ProjectMgmt** 技能和 **PMP** 证书。</span><span class="sxs-lookup"><span data-stu-id="485b3-238">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="485b3-239">设置基于角色的定价</span><span class="sxs-lookup"><span data-stu-id="485b3-239">Set up role-based pricing</span></span>
<span data-ttu-id="485b3-240">可为角色设置所有成本、销售以及转让价格。</span><span class="sxs-lookup"><span data-stu-id="485b3-240">All cost, sales, and transfer prices can be set up for roles.</span></span>

1. <span data-ttu-id="485b3-241">在**销售价(工时)** 页上，选择**新建**，并输入生效日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-241">On the **Sales price (hour)** page, select **New**, and enter an effective date.</span></span>
2. <span data-ttu-id="485b3-242">在**角色**列中，选择角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-242">In the **Role** column, select a role.</span></span>
3. <span data-ttu-id="485b3-243">在**定价**列中，输入所选资源角色的价格。</span><span class="sxs-lookup"><span data-stu-id="485b3-243">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="485b3-244">建立项目团队</span><span class="sxs-lookup"><span data-stu-id="485b3-244">Form a project team</span></span>
<span data-ttu-id="485b3-245">若要使用之前在项目中设置的角色，项目经理必须将角色与项目关联。</span><span class="sxs-lookup"><span data-stu-id="485b3-245">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="485b3-246">可以为一个项目分配多个角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-246">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="485b3-247">为了避免混淆，Finance and Operations 在预留期间自动标记这些角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-247">To prevent confusion, Finance and Operations automatically labels these roles during reservation.</span></span> <span data-ttu-id="485b3-248">例如，如果项目经理需要三位软件工程师，将自动生成具有**软件工程师 1**、**软件工程师 2** 和**软件工程师 3** 作为其标签的软件工程师角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-248">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="485b3-249">如果之前为角色设置了角色特性，则在搜索资源期间，它们将应用为筛选器。</span><span class="sxs-lookup"><span data-stu-id="485b3-249">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="485b3-250">其他特性可以根据需要添加以进一步调整搜索。</span><span class="sxs-lookup"><span data-stu-id="485b3-250">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="485b3-251">查看设置还可以自定义以提供资源可用性的更好的视图。</span><span class="sxs-lookup"><span data-stu-id="485b3-251">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="485b3-252">具有显示每小时、每日、每周、每月、每季度和每年可用性的选项。</span><span class="sxs-lookup"><span data-stu-id="485b3-252">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="485b3-253">还有可以显示可用资源和剩余资源产能的选项。</span><span class="sxs-lookup"><span data-stu-id="485b3-253">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="485b3-254">在您评估活动或资源可用性的可用时间时，此选项对时间管理很有用。</span><span class="sxs-lookup"><span data-stu-id="485b3-254">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="485b3-255">项目经理可在页面上选择角色，然后，如果存在满足该需求的一个可用资源，选择预留符合角色的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-255">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="485b3-256">请注意，资源不必在计划阶段的此时间点预留。</span><span class="sxs-lookup"><span data-stu-id="485b3-256">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="485b3-257">在您创建 WBS 时，可以使用项目的雇用资源替换角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-257">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="485b3-258">如果角色替换为 WBS 中的雇用资源，资源设置将自动更新项目团队列表和计划。</span><span class="sxs-lookup"><span data-stu-id="485b3-258">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="485b3-259">[![包括角色和实际资源的项目团队列表](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-259">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="485b3-260">项目经理具有预订项目资源的不同选项，例如**剩余产能**、**全部产能**、**产能百分比**和**指定工时**。</span><span class="sxs-lookup"><span data-stu-id="485b3-260">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="485b3-261">如果资源分配更改，这些预订选项可以在任何时间取消。</span><span class="sxs-lookup"><span data-stu-id="485b3-261">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="485b3-262">支持以下两种预订类型：</span><span class="sxs-lookup"><span data-stu-id="485b3-262">Two types of booking are supported:</span></span>

- <span data-ttu-id="485b3-263">**硬性预订** – 针对指定的持续时间审核并确认处理约定的资源预留。</span><span class="sxs-lookup"><span data-stu-id="485b3-263">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="485b3-264">**软性预订** – 针对指定的持续时间暂时设置处理约定的资源预留。</span><span class="sxs-lookup"><span data-stu-id="485b3-264">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="485b3-265">以下过程说明如何创建项目团队。</span><span class="sxs-lookup"><span data-stu-id="485b3-265">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="485b3-266">创建项目团队</span><span class="sxs-lookup"><span data-stu-id="485b3-266">Create a project team</span></span>

1. <span data-ttu-id="485b3-267">在**所有项目**列表页上，选择一个项目，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="485b3-267">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="485b3-268">在**项目团队和计划编制**选项卡上，在**计划结束日期**字段中，输入计划开始日期再加上一个月。</span><span class="sxs-lookup"><span data-stu-id="485b3-268">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="485b3-269">例如，如果计划开始日期为 2017 年 6 月 24 日 (24/06/2017)，输入 **24/07/2017**。</span><span class="sxs-lookup"><span data-stu-id="485b3-269">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="485b3-270">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="485b3-270">Select **Add**.</span></span>
4. <span data-ttu-id="485b3-271">在**将角色添加到项目**窗格中，在**角色**字段中，选择 **高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="485b3-271">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="485b3-272">选择**所需能力**。</span><span class="sxs-lookup"><span data-stu-id="485b3-272">Select **Required competencies**.</span></span>
6. <span data-ttu-id="485b3-273">默认情况下，在**选择特性**页上，选择您之前为高级项目经理角色设置的特性。</span><span class="sxs-lookup"><span data-stu-id="485b3-273">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="485b3-274">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="485b3-274">Select **OK**.</span></span>
7. <span data-ttu-id="485b3-275">在**将角色添加到项目**页上，在**资源数**字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="485b3-275">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="485b3-276">在**资源**字段中，查找显示具有所需能力的所有资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-276">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="485b3-277">选择 **Daniel Goldschmidt**，然后选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-277">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="485b3-278">在**项目**页上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="485b3-278">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="485b3-279">在**将角色添加到项目**窗格中，在**角色**字段中，选择 **团队成员**。</span><span class="sxs-lookup"><span data-stu-id="485b3-279">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="485b3-280">在**资源数**字段中输入 **5**。</span><span class="sxs-lookup"><span data-stu-id="485b3-280">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="485b3-281">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="485b3-281">Select **Create**.</span></span>
12. <span data-ttu-id="485b3-282">在**项目**页上，选择**完成资源**。</span><span class="sxs-lookup"><span data-stu-id="485b3-282">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="485b3-283">资源产能同步</span><span class="sxs-lookup"><span data-stu-id="485b3-283">Resource capacity synchronization</span></span>
<span data-ttu-id="485b3-284">资源同步流程帮助确保日历和基础日历信息深入到项目资源计划。</span><span class="sxs-lookup"><span data-stu-id="485b3-284">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="485b3-285">如果更改日历，流程对项目资源计划进行所需的更新。</span><span class="sxs-lookup"><span data-stu-id="485b3-285">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="485b3-286">因为日历的资源信息提前同步，这些流程还有助于改进性能。</span><span class="sxs-lookup"><span data-stu-id="485b3-286">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="485b3-287">因此，资源计划信息的更新更快。</span><span class="sxs-lookup"><span data-stu-id="485b3-287">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="485b3-288">我们建议您批量计划流程，而不是一次计划一个。</span><span class="sxs-lookup"><span data-stu-id="485b3-288">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="485b3-289">否则，某些员工可能忘记上次同步信息的起迄日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-289">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="485b3-290">如果不使用起迄日期，可能在日期同步时发生间隔。</span><span class="sxs-lookup"><span data-stu-id="485b3-290">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![日历同步](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="485b3-292">同步资源产能汇总</span><span class="sxs-lookup"><span data-stu-id="485b3-292">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="485b3-293">同步流程被设计为同步所有资源日历信息。</span><span class="sxs-lookup"><span data-stu-id="485b3-293">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="485b3-294">此信息包括有关对项目的资源日历产能表进行的任何更改的基本日历信息。</span><span class="sxs-lookup"><span data-stu-id="485b3-294">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="485b3-295">如果在项目中添加新的资源，同步可以帮助确保更新的日历信息可用。</span><span class="sxs-lookup"><span data-stu-id="485b3-295">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="485b3-296">此同步随时都可以进行。</span><span class="sxs-lookup"><span data-stu-id="485b3-296">This synchronization can be done at any time.</span></span>

<span data-ttu-id="485b3-297">我们建议您使用批次执行。</span><span class="sxs-lookup"><span data-stu-id="485b3-297">We recommend that you use a batch.</span></span> <span data-ttu-id="485b3-298">选项在同步产能预留中可用。</span><span class="sxs-lookup"><span data-stu-id="485b3-298">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="485b3-299">选择**项目管理与核算** &gt; **定期** &gt; **产能同步** &gt; **同步资源产能汇总**。</span><span class="sxs-lookup"><span data-stu-id="485b3-299">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="485b3-300">设置下表中的选项。</span><span class="sxs-lookup"><span data-stu-id="485b3-300">Set the options in the following table.</span></span>

    | <span data-ttu-id="485b3-301">选项</span><span class="sxs-lookup"><span data-stu-id="485b3-301">Option</span></span>      | <span data-ttu-id="485b3-302">说明</span><span class="sxs-lookup"><span data-stu-id="485b3-302">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="485b3-303">期间代码</span><span class="sxs-lookup"><span data-stu-id="485b3-303">Period code</span></span> | <span data-ttu-id="485b3-304">选择性地选择总帐日期间隔代码，以设置资源产能汇总的同步流程的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-304">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="485b3-305">入职日期</span><span class="sxs-lookup"><span data-stu-id="485b3-305">Start date</span></span>  | <span data-ttu-id="485b3-306">输入资源产能汇总的同步流程的开始日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-306">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="485b3-307">结束日期</span><span class="sxs-lookup"><span data-stu-id="485b3-307">End date</span></span>    | <span data-ttu-id="485b3-308">输入资源产能汇总的同步流程的结束日期。</span><span class="sxs-lookup"><span data-stu-id="485b3-308">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="485b3-309">[![同步流程](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-309">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="485b3-310">在 WBS 模板上设置角色</span><span class="sxs-lookup"><span data-stu-id="485b3-310">Set up roles on WBS templates</span></span>
<span data-ttu-id="485b3-311">项目经理可以设置在创建新项目的 WBS 时可以应用的 WBS 模板。</span><span class="sxs-lookup"><span data-stu-id="485b3-311">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="485b3-312">项目经理可以在创建模板时添加角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-312">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="485b3-313">使用以下过程将角色分配到 WBS 模板。 </span><span class="sxs-lookup"><span data-stu-id="485b3-313">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="485b3-314">选择**项目管理与核算** &gt; **设置** &gt; **项目** &gt; **工作分解结构模板**。</span><span class="sxs-lookup"><span data-stu-id="485b3-314">Select **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="485b3-315">选择所选 WBS 模板的**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="485b3-315">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="485b3-316">选择列表中的某一任务，然后在**角色**字段中，选择要分配给任务的角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-316">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="485b3-317">使用 WBS</span><span class="sxs-lookup"><span data-stu-id="485b3-317">Work with a WBS</span></span>

<span data-ttu-id="485b3-318">您可以创建新的 WBS，也可以从现有的 WBS 模板复制 WBS。</span><span class="sxs-lookup"><span data-stu-id="485b3-318">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="485b3-319">项目经理可以通过在 WBS 上将角色分配给新任务来轻松管理资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-319">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="485b3-320">角色可以在获取资源后替换，或者在确定执行任务的确认资源后替换。</span><span class="sxs-lookup"><span data-stu-id="485b3-320">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="485b3-321">此灵活性让项目经理可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="485b3-321">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="485b3-322">确定 WBS 工作包所需的资源的数量。</span><span class="sxs-lookup"><span data-stu-id="485b3-322">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="485b3-323">评估项目成本。</span><span class="sxs-lookup"><span data-stu-id="485b3-323">Estimate project costs.</span></span>
- <span data-ttu-id="485b3-324">确定初步预算。</span><span class="sxs-lookup"><span data-stu-id="485b3-324">Determine a preliminary budget.</span></span>
- <span data-ttu-id="485b3-325">基于角色和资源估计活动持续时间。</span><span class="sxs-lookup"><span data-stu-id="485b3-325">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="485b3-326">基于可用项目信息制定某些项目管理计划。</span><span class="sxs-lookup"><span data-stu-id="485b3-326">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="485b3-327">附加选项已添加到 WBS 中以便更好地使用资源功能。</span><span class="sxs-lookup"><span data-stu-id="485b3-327">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="485b3-328">选项</span><span class="sxs-lookup"><span data-stu-id="485b3-328">Option</span></span></th>
<th><span data-ttu-id="485b3-329">描述</span><span class="sxs-lookup"><span data-stu-id="485b3-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="485b3-330">资源分配</span><span class="sxs-lookup"><span data-stu-id="485b3-330">Resource assignments</span></span></td>
<td><span data-ttu-id="485b3-331">在 WBS 中查看任务的分配资源、日期、工时数和预订类型。</span><span class="sxs-lookup"><span data-stu-id="485b3-331">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="485b3-332">自动生成团队</span><span class="sxs-lookup"><span data-stu-id="485b3-332">Auto generate team</span></span></td>
<td><span data-ttu-id="485b3-333">通过使用与任务关联的角色自动添加计划资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-333">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="485b3-334">Finance and Operations 通过使用基于角色的多条件决策分析来自动建议计划资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-334">Finance and Operations automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="485b3-335">在 WBS 中为任务设置角色和工作量（工时）后，并且在发布结构之后，选择<strong>自动生成团队</strong>。</span><span class="sxs-lookup"><span data-stu-id="485b3-335">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="485b3-336">所需计划资源数量将添加到 WBS 和<strong>项目和团队计划编制</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="485b3-336">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="485b3-337">资源（下拉列表）</span><span class="sxs-lookup"><span data-stu-id="485b3-337">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="485b3-338">在<strong>启动资源分配</strong>页上，您可以基于指定的持续时间选择要硬性预订或软性预订的资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-338">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="485b3-339">您可以调整视图设置来查看和设置资源活动的持续时间。</span><span class="sxs-lookup"><span data-stu-id="485b3-339">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="485b3-340">您可以使用以下选项在工作包级别选择和分配资源：</span><span class="sxs-lookup"><span data-stu-id="485b3-340">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="485b3-341"><strong>接受</strong> – 确认对分配给任务的资源的更改。</span><span class="sxs-lookup"><span data-stu-id="485b3-341"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="485b3-342"><strong>取消</strong> – 取消对分配给任务的资源的更改。</span><span class="sxs-lookup"><span data-stu-id="485b3-342"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="485b3-343"><strong>自动分配</strong> - 自动选择具有匹配角色的可用雇用资源并分配到所选任务。</span><span class="sxs-lookup"><span data-stu-id="485b3-343"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="485b3-344">在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-344">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="485b3-345">选择**计划** &gt; **活动** &gt; **工作分解结构**。</span><span class="sxs-lookup"><span data-stu-id="485b3-345">Select **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
3. <span data-ttu-id="485b3-346">选择**新建**将以下一级活动添加到 WBS：</span><span class="sxs-lookup"><span data-stu-id="485b3-346">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="485b3-347">启动</span><span class="sxs-lookup"><span data-stu-id="485b3-347">Initiating</span></span>
    - <span data-ttu-id="485b3-348">计划</span><span class="sxs-lookup"><span data-stu-id="485b3-348">Planning</span></span>
    - <span data-ttu-id="485b3-349">正在执行</span><span class="sxs-lookup"><span data-stu-id="485b3-349">Executing</span></span>
    - <span data-ttu-id="485b3-350">监控和控制</span><span class="sxs-lookup"><span data-stu-id="485b3-350">Monitoring and Control</span></span>
    - <span data-ttu-id="485b3-351">期结</span><span class="sxs-lookup"><span data-stu-id="485b3-351">Close</span></span>

4. <span data-ttu-id="485b3-352">设置日期和工作量（工时），如以下插图所示。</span><span class="sxs-lookup"><span data-stu-id="485b3-352">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="485b3-353">[![设置日期和工作量](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="485b3-353">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="485b3-354">选择**启动**任务行，然后在**角色**字段中，选择**高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="485b3-354">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="485b3-355">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="485b3-355">Select **Publish**.</span></span>
7. <span data-ttu-id="485b3-356">在同一行的**资源**字段中，选择 **Daniel Goldschmidt**，然后选择**接受**。</span><span class="sxs-lookup"><span data-stu-id="485b3-356">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="485b3-357">选择**计划**任务行，然后在**角色**字段中，选择**业务分析员**。</span><span class="sxs-lookup"><span data-stu-id="485b3-357">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="485b3-358">选择**发布**，然后选择**自动生成团队**。</span><span class="sxs-lookup"><span data-stu-id="485b3-358">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="485b3-359">在出现的消息框中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="485b3-359">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="485b3-360">在**资源**字段中，确认值为**业务分析员 1**。</span><span class="sxs-lookup"><span data-stu-id="485b3-360">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="485b3-361">对于**业务分析员 1** 资源，打开查找，并选择**启动资源分配**。</span><span class="sxs-lookup"><span data-stu-id="485b3-361">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="485b3-362">然后为任务选择一个工作人员。</span><span class="sxs-lookup"><span data-stu-id="485b3-362">Then select a worker for the task.</span></span>
13. <span data-ttu-id="485b3-363">选择**软性分配** &gt; **全部产能**。</span><span class="sxs-lookup"><span data-stu-id="485b3-363">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="485b3-364">您不会收到指定资源现在是 2 的警告，因为资源数量仍为 1。</span><span class="sxs-lookup"><span data-stu-id="485b3-364">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="485b3-365">在**工作分解结构**页上，在 WBS 中验证资源分配，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="485b3-365">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="485b3-366">计划资源的资源完成</span><span class="sxs-lookup"><span data-stu-id="485b3-366">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="485b3-367">项目经理可为项目计划所需的资源角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-367">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="485b3-368">资源经理将在**资源完成**页上根据请求查看这些计划资源，并且可以分配实际资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-368">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="485b3-369">在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="485b3-369">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="485b3-370">选择**项目**，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="485b3-370">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="485b3-371">在**项目团队和计划编制**选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="485b3-371">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="485b3-372">在**添加角色**对话框中，选择**软件开发人员**角色。</span><span class="sxs-lookup"><span data-stu-id="485b3-372">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="485b3-373">选择**创建**，然后关闭项目页。</span><span class="sxs-lookup"><span data-stu-id="485b3-373">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="485b3-374">在**资源完成**页上，为 **XYZ 升级项目第 2 阶段**项目选择**软件开发人员 1**。</span><span class="sxs-lookup"><span data-stu-id="485b3-374">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="485b3-375">选择一个工作人员，然后选择**分配**。</span><span class="sxs-lookup"><span data-stu-id="485b3-375">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="485b3-376">验证**软件开发人员 1** 的行已为 **XYZ 升级项目第 2 阶段**项目删除。</span><span class="sxs-lookup"><span data-stu-id="485b3-376">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="485b3-377">在**项目团队和计划编制**选项卡上，对 **XYZ 升级项目第 2 阶段**项目验证您在上一步中选择的工作人员已添加为**软件开发人员**。</span><span class="sxs-lookup"><span data-stu-id="485b3-377">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="485b3-378">项目资源询价</span><span class="sxs-lookup"><span data-stu-id="485b3-378">Requests for project resources</span></span>
<span data-ttu-id="485b3-379">项目资源计划功能仅支持资源经理为约定或项目分配雇用资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-379">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="485b3-380">若要启用此功能，请完成以下任务，或验证是否已完成这些任务：</span><span class="sxs-lookup"><span data-stu-id="485b3-380">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="485b3-381">设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="485b3-381">Set up number sequences.</span></span>
- <span data-ttu-id="485b3-382">设置项目管理与核算工作流。</span><span class="sxs-lookup"><span data-stu-id="485b3-382">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="485b3-383">启用资源请求工作流。</span><span class="sxs-lookup"><span data-stu-id="485b3-383">Enable resource request workflows.</span></span>

<span data-ttu-id="485b3-384">完成前面的任务后，可以根据需要完成下面的任务：</span><span class="sxs-lookup"><span data-stu-id="485b3-384">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="485b3-385">从软性预订雇用资源创建资源请求。</span><span class="sxs-lookup"><span data-stu-id="485b3-385">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="485b3-386">监控资源请求。</span><span class="sxs-lookup"><span data-stu-id="485b3-386">Monitor resource requests.</span></span>
- <span data-ttu-id="485b3-387">实施资源请求。</span><span class="sxs-lookup"><span data-stu-id="485b3-387">Fulfill resource requests.</span></span>
- <span data-ttu-id="485b3-388">从 WBS 请求雇用资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-388">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="485b3-389">在不请求雇用资源的情况下为项目预订资源。</span><span class="sxs-lookup"><span data-stu-id="485b3-389">Book resources to a project without having a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="485b3-390">监控项目团队</span><span class="sxs-lookup"><span data-stu-id="485b3-390">Monitor project teams</span></span>
1. <span data-ttu-id="485b3-391">在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目的**项目 ID** 链接。</span><span class="sxs-lookup"><span data-stu-id="485b3-391">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="485b3-392">在**项目团队和计划编制**快速选项卡上，确认列出的项目资源是正确的。</span><span class="sxs-lookup"><span data-stu-id="485b3-392">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
