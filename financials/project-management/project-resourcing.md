---
title: "项目资源"
description: "本主题提供有关项目资源的信息。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: fc36d399759b6321995f9bd827849c8a0bced090
ms.contentlocale: zh-cn
ms.lasthandoff: 06/30/2017


---

# <a name="project-resourcing"></a><span data-ttu-id="bb543-103">项目资源</span><span class="sxs-lookup"><span data-stu-id="bb543-103">Project resourcing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bb543-104">本主题提供有关项目资源的信息。</span><span class="sxs-lookup"><span data-stu-id="bb543-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="bb543-105">项目经理和资源经理在项目计划阶段的一个挑战是资源分配，他们必须在此确定和预留处理项目所需的正确资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="bb543-106">在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中，项目的资源能力可以定义预留给特定参与或参与的一部分被视为临时资源的角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement, or part of an engagement.</span></span> <span data-ttu-id="bb543-107">此资源类型允许项目经理和资源经理完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="bb543-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

-   <span data-ttu-id="bb543-108">定义具有所需能力可以让匹配资源更加轻松的角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-108">Define a role that has the required competencies to make it easy to match resources.</span></span>
-   <span data-ttu-id="bb543-109">使用角色基于预留资源定义初始约定计划。</span><span class="sxs-lookup"><span data-stu-id="bb543-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
-   <span data-ttu-id="bb543-110">基于分配的角色和项目的资源估计成本和确定初始预算。</span><span class="sxs-lookup"><span data-stu-id="bb543-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
-   <span data-ttu-id="bb543-111">使用角色估计每个约定所需的资源预留的数量。</span><span class="sxs-lookup"><span data-stu-id="bb543-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
-   <span data-ttu-id="bb543-112">估计项目的整个生命周期所需的资源的数量。</span><span class="sxs-lookup"><span data-stu-id="bb543-112">Estimate the number of resources that are required for the entire life cycle of a project.</span></span>
-   <span data-ttu-id="bb543-113">通过使用初始资源分配设计工作分解结构 (WBS)。</span><span class="sxs-lookup"><span data-stu-id="bb543-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="bb543-114">[![项目生命周期](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span> 

<span data-ttu-id="bb543-115">随着项目计划的继续，计划的资源可以替换为雇用的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="bb543-116">项目经理还可以在任何项目阶段返回和更新资源预留。</span><span class="sxs-lookup"><span data-stu-id="bb543-116">The project manager can also go back and update the resourcing reservations during any of the project stages.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="bb543-117">设置项目资源</span><span class="sxs-lookup"><span data-stu-id="bb543-117">Set up project resources</span></span>
<span data-ttu-id="bb543-118">您必须设置日历并将其与员工或工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="bb543-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="bb543-119">该日历用于计划项目和预留给该项目的资源的工作时间。</span><span class="sxs-lookup"><span data-stu-id="bb543-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="bb543-120">在日历设置期间，项目经理可以作为资源优化的一部分执行资源均衡。</span><span class="sxs-lookup"><span data-stu-id="bb543-120">During calendar setup, project managers can perform resource leveling as part of resource optimization.</span></span> <span data-ttu-id="bb543-121">基于日历计划，可以对资源设定限制。</span><span class="sxs-lookup"><span data-stu-id="bb543-121">Based on the calendar schedule, restrictions can be placed on resources.</span></span> <span data-ttu-id="bb543-122">可以在**日历**页中设置日历。</span><span class="sxs-lookup"><span data-stu-id="bb543-122">You can set up a calendar on the **Calendars** page.</span></span> 

<span data-ttu-id="bb543-123">将工作人员设置为项目资源时，可以从在要为其设置资源的公司中工作的工作人员进行选择，也可以选择您的组织内其他公司中的工作人员。</span><span class="sxs-lookup"><span data-stu-id="bb543-123">When you set up a worker as a project resource, you can select from workers that work in the company for which you are setting up resources or, you can select workers from other companies within your organization.</span></span> <span data-ttu-id="bb543-124">这些是内部公司资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-124">These are intercompany resources.</span></span> <span data-ttu-id="bb543-125">以下过程说明如何将资源设置为公司内的项目资源，以及如何设置内部公司项目资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-125">The following procedures explain how to set up a worker as a project resource within your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="bb543-126">将工作人员设置为项目资源</span><span class="sxs-lookup"><span data-stu-id="bb543-126">Set up a worker as a project resource</span></span>

1.  <span data-ttu-id="bb543-127">在**工作人员**页的**工作人员**列表内，选择您添加为项目资源的工作人员，然后打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="bb543-127">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2.  <span data-ttu-id="bb543-128">在“操作”窗格上，单击**项目** &gt; **设置** &gt; **项目设置**。</span><span class="sxs-lookup"><span data-stu-id="bb543-128">On the Action Pane, click **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3.  <span data-ttu-id="bb543-129">选择日历，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-129">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="bb543-130">您还可以将资源的默认项目指定为预分配类型。</span><span class="sxs-lookup"><span data-stu-id="bb543-130">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="bb543-131">当资源经理或项目经理知道资源将提前处理哪些项目时，可以使用预分配。</span><span class="sxs-lookup"><span data-stu-id="bb543-131">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="bb543-132">预分配还可以基于项目赞助者或客户的请求。</span><span class="sxs-lookup"><span data-stu-id="bb543-132">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="bb543-133">要预分配一个项目，在**分配项目**页上，在**项目**选项卡上，在**其余项目**列表中，选择相应的项目。</span><span class="sxs-lookup"><span data-stu-id="bb543-133">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="bb543-134">设置内部公司资源</span><span class="sxs-lookup"><span data-stu-id="bb543-134">Set up an intercompany resource</span></span>

<span data-ttu-id="bb543-135">将工作人员设置为内部公司资源时，必须完成借出公司和借入公司中的设置。</span><span class="sxs-lookup"><span data-stu-id="bb543-135">When you set up a worker as an intercompany resource, you must complete the setup in the lending company and the borrowing company.</span></span> 

<span data-ttu-id="bb543-136">**在借出公司中：**</span><span class="sxs-lookup"><span data-stu-id="bb543-136">**In the lending company:**</span></span>

1.  <span data-ttu-id="bb543-137">在 Finance and Operations 中，验证已选择借出公司，然后完成上面的过程（“将工作人员设置为项目资源”）。</span><span class="sxs-lookup"><span data-stu-id="bb543-137">In Finance and Operations, verify that the lending company is selected, and then complete the procedure above, "Set up a worker as a project resource."</span></span>
2.  <span data-ttu-id="bb543-138">转至 **总帐** &gt;**过帐设置**&gt; **内部公司核算**。</span><span class="sxs-lookup"><span data-stu-id="bb543-138">Go to **General ledger **&gt; **Posting setup **&gt; **Intercompany accounting**.</span></span> <span data-ttu-id="bb543-139">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="bb543-139">Click **New**.</span></span>
3.  <span data-ttu-id="bb543-140">在 **法人 ID** 字段中，选择借出公司。</span><span class="sxs-lookup"><span data-stu-id="bb543-140">In the **Legal entity ID **field, select the lending company.</span></span> <span data-ttu-id="bb543-141">根据需要填写其余字段，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="bb543-141">Fill in the remaining fields as appropriate, and then click **Save**.</span></span>
4.  <span data-ttu-id="bb543-142">转到**项目管理与核算**&gt; **设置**&gt; **价格**&gt; **转让价格**。**</span><span class="sxs-lookup"><span data-stu-id="bb543-142">Go the **Project management and accounting **&gt; **Setup **&gt; **Prices ** &gt; **Transfer price**.**</span></span> **
5.  <span data-ttu-id="bb543-143">在 **转让价格** 窗体中，单击**新建**，然后在 **借入方法人** 字段中，选择相应公司。</span><span class="sxs-lookup"><span data-stu-id="bb543-143">On the **Transfer price **form, click **New**, and in the **Borrowing legal entity **field, select the appropriate company.</span></span>
6.  <span data-ttu-id="bb543-144">如果要仅借给借入公司您在此部分开始时创建的资源，请在**资源**资源中，选择您创建的资源的名称。</span><span class="sxs-lookup"><span data-stu-id="bb543-144">If you want to only loan the borrowing company the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="bb543-145">如果要将公司内的所有资源都提供给借入公司，请将 **资源** 字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="bb543-145">If you want to make all resources in the company available to the borrowing company, leave the **Resource **field blank.</span></span>
7.  <span data-ttu-id="bb543-146">转至 **资源管理和核算 **&gt; **设置**&gt; **项目管理与核算参数**，然后在 **内部公司** 选项卡上，将 **启用内部公司资源计划和时间表** 字段设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="bb543-146">Go to **Project management and accounting **&gt; **Setup **&gt; **Project management and accounting parameters**, and on the **Intercompany **tab, set the **Enable intercompany resource scheduling and timesheets **field to **Yes**.</span></span>

<span data-ttu-id="bb543-147">**在借入公司中：**</span><span class="sxs-lookup"><span data-stu-id="bb543-147">**In the borrowing company:**</span></span>

1.  <span data-ttu-id="bb543-148">转至**项目管理与核算** &gt; **项目资源** &gt; **资源列表**。</span><span class="sxs-lookup"><span data-stu-id="bb543-148">Go to **Project management and accounting** &gt; **Project resources** &gt; **Resources list**.</span></span>
2.  <span data-ttu-id="bb543-149">在搜索筛选器中，输入您在上一过程中为借出公司创建的资源的名称，以验证借入公司的资源列表中是否包含此名称。</span><span class="sxs-lookup"><span data-stu-id="bb543-149">In the search filter, enter the name of the resource that you created in the previous procedure for the lending company to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="bb543-150">管理资源能力</span><span class="sxs-lookup"><span data-stu-id="bb543-150">Manage resource competencies</span></span>
<span data-ttu-id="bb543-151">资源能力是资源管理必不可少的部分。</span><span class="sxs-lookup"><span data-stu-id="bb543-151">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="bb543-152">能力可用作确定具有正确的技能、教育、证书和项目经验比重的资源的基准。</span><span class="sxs-lookup"><span data-stu-id="bb543-152">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="bb543-153">您应该为每个资源设置此信息并定期更新它。</span><span class="sxs-lookup"><span data-stu-id="bb543-153">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="bb543-154">这样，您可以在项目资源分配期间匹配特定资源能力时让能力实现最大化。</span><span class="sxs-lookup"><span data-stu-id="bb543-154">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span> <span data-ttu-id="bb543-155">[![例如技能、证书、教育和项目经验](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-155">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span> 

<span data-ttu-id="bb543-156">以下过程说明如何设置资源的某些能力。</span><span class="sxs-lookup"><span data-stu-id="bb543-156">The following procedures explain how to set up some of the competencies for a resource.</span></span> 

<span data-ttu-id="bb543-157">若要设置工作人员的能力，您可以使用“人力资源”中的**工作人员**列表页或“项目管理与核算”中的**资源**列表页。</span><span class="sxs-lookup"><span data-stu-id="bb543-157">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="bb543-158">对于以下过程，将使用“人力资源”中的**工作人员**列表页。</span><span class="sxs-lookup"><span data-stu-id="bb543-158">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="bb543-159">设置能力：证书</span><span class="sxs-lookup"><span data-stu-id="bb543-159">Set up competencies: Certificates</span></span>

1.  <span data-ttu-id="bb543-160">在**工作人员**列表页，选择您要为其添加证书信息的工作人员的行。</span><span class="sxs-lookup"><span data-stu-id="bb543-160">On the **Workers** list page, select the line of the worker that you're adding certificate information for.</span></span>
2.  <span data-ttu-id="bb543-161">在“操作”窗格上，在**工作人员**选项卡上，在**能力**组，单击**评书**。</span><span class="sxs-lookup"><span data-stu-id="bb543-161">On the Action Pane, on the **Worker** tab, in the **Competencies** group, click **Certificates**.</span></span>
3.  <span data-ttu-id="bb543-162">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-162">Click **New**.</span></span>
4.  <span data-ttu-id="bb543-163">在**证书类型**字段中，选择 **PMP**。</span><span class="sxs-lookup"><span data-stu-id="bb543-163">In the **Certificate type** field, select **PMP**.</span></span>
5.  <span data-ttu-id="bb543-164">在**开始日期**字段中，选择 **10/1/2015**。</span><span class="sxs-lookup"><span data-stu-id="bb543-164">In the **Start date** field, select **10/1/2015**.</span></span>
6.  <span data-ttu-id="bb543-165">单击**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-165">Click **Save**, and then close the page.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="bb543-166">设置能力：技能</span><span class="sxs-lookup"><span data-stu-id="bb543-166">Set up competencies: Skills</span></span>

1.  <span data-ttu-id="bb543-167">在**工作人员**列表页，确保仍然选择在上一过程中使用的工作人员。</span><span class="sxs-lookup"><span data-stu-id="bb543-167">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="bb543-168">然后，在“操作”窗格上，在**工作人员**选项卡上，在**能力**组，单击**技能**。</span><span class="sxs-lookup"><span data-stu-id="bb543-168">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, click **Skills**.</span></span>
2.  <span data-ttu-id="bb543-169">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-169">Click **New**.</span></span>
3.  <span data-ttu-id="bb543-170">在**技能**字段中，选择**项目管理**。</span><span class="sxs-lookup"><span data-stu-id="bb543-170">In the **Skill** field, select **Project management**.</span></span>
4.  <span data-ttu-id="bb543-171">在**级别**字段中选择 **5 专家**。</span><span class="sxs-lookup"><span data-stu-id="bb543-171">In the **Level** field, select **5 Expert**.</span></span>
5.  <span data-ttu-id="bb543-172">在**等级日期**字段中，选择 **1-/14/2014**。</span><span class="sxs-lookup"><span data-stu-id="bb543-172">In the **Level date** field, select **1-/14/2014**.</span></span>
6.  <span data-ttu-id="bb543-173">在**年资**字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="bb543-173">In the **Years of experience** field, enter **10**.</span></span>
7.  <span data-ttu-id="bb543-174">单击**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-174">Click **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="bb543-175">创建新项目</span><span class="sxs-lookup"><span data-stu-id="bb543-175">Create a new project</span></span>
1.  <span data-ttu-id="bb543-176">单击**项目管理与核算** &gt; **工作区** &gt; **项目管理**。</span><span class="sxs-lookup"><span data-stu-id="bb543-176">Click **Project management and accounting** &gt; **Workspaces** &gt; **Project management**.</span></span>
2.  <span data-ttu-id="bb543-177">单击**新项目**，然后输入以下值：</span><span class="sxs-lookup"><span data-stu-id="bb543-177">Click **New project**, and enter the following values:</span></span>
    -   <span data-ttu-id="bb543-178">**项目类型** - 时间和材料</span><span class="sxs-lookup"><span data-stu-id="bb543-178">**Project type** - Time and material</span></span>
    -   <span data-ttu-id="bb543-179">**项目名称** - XYZ 升级第 2 阶段</span><span class="sxs-lookup"><span data-stu-id="bb543-179">**Project name** - XYZ Upgrade Phase 2</span></span>
    -   <span data-ttu-id="bb543-180">**项目组** - TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="bb543-180">**Project group** - TM\_WIP</span></span>
    -   <span data-ttu-id="bb543-181">**项目合同 ID** - 00000002</span><span class="sxs-lookup"><span data-stu-id="bb543-181">**Project contract ID**  - 00000002</span></span>
3.  <span data-ttu-id="bb543-182">单击**创建项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-182">Click **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="bb543-183">将资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="bb543-183">Assign a resource to a project</span></span>

1.  <span data-ttu-id="bb543-184">单击**人力资源** &gt; **工作人员** &gt; **工作人员**。</span><span class="sxs-lookup"><span data-stu-id="bb543-184">Click **Human resources** &gt; **Workers** &gt; **Workers**.</span></span>
2.  <span data-ttu-id="bb543-185">在**工作人员**列表中，选择您之前为其设置能力的工作人员的记录，然后打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="bb543-185">In the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
3.  <span data-ttu-id="bb543-186">在“操作”窗格中，在**项目**选项卡上，在**设置**组中，单击**分配项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-186">On the Action Pane, on the **Project** tab, in the **Setup** group, click **Assign projects**.</span></span>
4.  <span data-ttu-id="bb543-187">在**资源验证项目分配**页上，单击**项目**选项卡。</span><span class="sxs-lookup"><span data-stu-id="bb543-187">On the **Resource validation project assignments** page, click the **Projects** tab.</span></span>
5.  <span data-ttu-id="bb543-188">在**将项目添加到所选项目**中，筛选项目，XYZ 升级第 2 阶段</span><span class="sxs-lookup"><span data-stu-id="bb543-188">In the **Add the project to selected projects**, filter on the project, XYZ Upgrade Phase 2</span></span>
6.  <span data-ttu-id="bb543-189">在**其余项目**窗格中，选择某一项目，然后单击箭头将其添加到**所选项目**窗格中。</span><span class="sxs-lookup"><span data-stu-id="bb543-189">In the **Remaining projects** pane, select a project, and then click the arrow to add it to the **Selected projects** pane.</span></span>
7.  <span data-ttu-id="bb543-190">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-190">Close the page.</span></span>

<span data-ttu-id="bb543-191">如果需要，您还可以分配资源的类别。</span><span class="sxs-lookup"><span data-stu-id="bb543-191">If needed, you can also assign categories for a resource.</span></span> <span data-ttu-id="bb543-192">类别类型可以是“成本”或“收入”。</span><span class="sxs-lookup"><span data-stu-id="bb543-192">The category type is either Cost or Revenue.</span></span> <span data-ttu-id="bb543-193">这您的组织确定。</span><span class="sxs-lookup"><span data-stu-id="bb543-193">This is determined by your organization.</span></span> <span data-ttu-id="bb543-194">如果没有为资源分配类别，Finance and Operations 查找成本和收入工时价格的默认类别。</span><span class="sxs-lookup"><span data-stu-id="bb543-194">If there are no assigned categories for the resource, Finance and Operations will look up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="bb543-195">设置项目资源和角色特征</span><span class="sxs-lookup"><span data-stu-id="bb543-195">Set up project resource and role characteristics</span></span>

<span data-ttu-id="bb543-196">项目经理可使用项目资源功能创建项目所需的角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-196">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="bb543-197">在确认的资源在预留资源期间仍未知时可以使用角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-197">Roles can be used when confirmed resources are still unknown when reserving resources.</span></span> <span data-ttu-id="bb543-198">角色可临时预留为计划资源，以便您可以继续项目计划阶段。</span><span class="sxs-lookup"><span data-stu-id="bb543-198">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span> 

<span data-ttu-id="bb543-199">[![角色示例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-199">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="bb543-200">**场景**：Contoso 被雇用完成具有已审核项目章节的时间和材料项目。</span><span class="sxs-lookup"><span data-stu-id="bb543-200">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="bb543-201">初级项目经理仍在完成项目的工作范围。</span><span class="sxs-lookup"><span data-stu-id="bb543-201">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="bb543-202">资源经理当前正在确定要预留的处理新项目的特定资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-202">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="bb543-203">由于项目的重要性质，项目赞助者请求的角色之一为高级项目经理。</span><span class="sxs-lookup"><span data-stu-id="bb543-203">One of the roles that the project sponsor requested, because of the critical nature of the project, is the Senior project manager.</span></span> <span data-ttu-id="bb543-204">如果初级项目经理在项目计划期间需要资源信息，资源经理必须获得新的资源并且定义定义系统中的角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-204">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during the project planning.</span></span> 

<span data-ttu-id="bb543-205">以下步骤显示资源经理如何设置高级项目经理角色并将资源特性与其关联。</span><span class="sxs-lookup"><span data-stu-id="bb543-205">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="bb543-206">之后，角色可用于搜索符合所需的资源能力的可用资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-206">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1.  <span data-ttu-id="bb543-207">单击**项目管理与核算** &gt; **设置** &gt; **资源** &gt; **设置角色**。</span><span class="sxs-lookup"><span data-stu-id="bb543-207">Click **Project management and accounting** &gt; **Setup** &gt; **Resources** &gt; **Setup roles**.</span></span>
2.  <span data-ttu-id="bb543-208">单击**新建**，然后输入以下值：</span><span class="sxs-lookup"><span data-stu-id="bb543-208">Click **New**, and enter the following values:</span></span>
    -   <span data-ttu-id="bb543-209">**角色 ID** - 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="bb543-209">**Role ID** - Senior Project Manager</span></span>
    -   <span data-ttu-id="bb543-210">**描述** - 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="bb543-210">**Description** - Senior Project Manager</span></span>
3.  <span data-ttu-id="bb543-211">单击“**创建**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-211">Click **Create**.</span></span>
4.  <span data-ttu-id="bb543-212">选择**高级项目经理**角色，然后单击**配置特性**。</span><span class="sxs-lookup"><span data-stu-id="bb543-212">Select the **Senior Project Manager** role, and then click **Configure characteristics**.</span></span>
5.  <span data-ttu-id="bb543-213">在**特性类型**字段中，选择**技能**。</span><span class="sxs-lookup"><span data-stu-id="bb543-213">In the **Characteristics type** field, select **Skill**.</span></span>
6.  <span data-ttu-id="bb543-214">在**可用特性**字段中，输入您要搜索的技能。</span><span class="sxs-lookup"><span data-stu-id="bb543-214">In the **Available characteristics** field, enter the skill that you're searching for.</span></span>
7.  <span data-ttu-id="bb543-215">在**特性类型**字段中，选择**证书**。</span><span class="sxs-lookup"><span data-stu-id="bb543-215">In the **Characteristic type** field, select **Certificate**.</span></span>
8.  <span data-ttu-id="bb543-216">在**可用特性**字段中，输入您要搜索的证书类型。</span><span class="sxs-lookup"><span data-stu-id="bb543-216">In the **Available characteristics** field, enter the certificate type to search for.</span></span>
9.  <span data-ttu-id="bb543-217">单击**确定**，关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-217">Click **OK**, and close the page.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="bb543-218">将项目资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="bb543-218">Assign a project resource to a project</span></span>

1.  <span data-ttu-id="bb543-219">单击**项目管理与核算** &gt; **通用** &gt; **项目** &gt; **所有项目**，并打开 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="bb543-219">Click **Project management and accounting** &gt; **Common** &gt; **Projects** &gt; **All projects**, and open the **XYZ Upgrade Phase 2** project.</span></span>
2.  <span data-ttu-id="bb543-220">在**项目团队和计划编制**选项卡上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="bb543-220">On the **Project team and scheduling** tab, click **Add**.</span></span>
3.  <span data-ttu-id="bb543-221">在**角色**字段中，选择**团队成员**。</span><span class="sxs-lookup"><span data-stu-id="bb543-221">In the **Role** field, select **Team member**.</span></span>
4.  <span data-ttu-id="bb543-222">单击**从日历预订**。</span><span class="sxs-lookup"><span data-stu-id="bb543-222">Click **Book from calendar**.</span></span>
5.  <span data-ttu-id="bb543-223">在**资源可用性**页上，单击**查看设置**。</span><span class="sxs-lookup"><span data-stu-id="bb543-223">On the **Resource availability** page, click **View settings**.</span></span>
6.  <span data-ttu-id="bb543-224">在**调整视图设置**页上，输入以下值：</span><span class="sxs-lookup"><span data-stu-id="bb543-224">On the **Adjust view settings** page, enter the following values:</span></span>
    -   <span data-ttu-id="bb543-225">**日期范围视图的格式** - 天</span><span class="sxs-lookup"><span data-stu-id="bb543-225">**Format for date range view** - Day</span></span>
    -   <span data-ttu-id="bb543-226">**显示可用性描述** - 是</span><span class="sxs-lookup"><span data-stu-id="bb543-226">**Display availability descriptions** - Yes</span></span>
    -   <span data-ttu-id="bb543-227">**显示剩余产能** - 是</span><span class="sxs-lookup"><span data-stu-id="bb543-227">**Display remaining capacity** - Yes</span></span>
7.  <span data-ttu-id="bb543-228">在资源列表中，选择某一资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-228">In the list of resources, select a resource.</span></span>
8.  <span data-ttu-id="bb543-229">单击**硬性预订** &gt; **全部产能**。</span><span class="sxs-lookup"><span data-stu-id="bb543-229">Click **Hard book** &gt; **Full capacity**.</span></span>
9.  <span data-ttu-id="bb543-230">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-230">Close the page.</span></span>

### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="bb543-231">将资源分配给默认角色</span><span class="sxs-lookup"><span data-stu-id="bb543-231">Assign a resource to a default role</span></span>

<span data-ttu-id="bb543-232">为了帮助项目或资源经理，您可以进一步深化到可以预留给项目的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-232">To help project or resource managers, you can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="bb543-233">您可以将默认值角色与现有资源或新获取的资源进行关联。</span><span class="sxs-lookup"><span data-stu-id="bb543-233">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="bb543-234">例如，如果雇用了 Daniel，所以就有了经验和技能来填补“业务分析”角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-234">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="bb543-235">资源经理将该角色分配为 Daniel 的默认角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-235">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="bb543-236">因此，资源经理将 Daniel 添加到可处理项目的业务分析池中。</span><span class="sxs-lookup"><span data-stu-id="bb543-236">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span> 

<span data-ttu-id="bb543-237">在资源预留期间，项目经理可以筛选可参与项目的角色资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-237">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="bb543-238">在履行资源期间执行多条件决定分析时，他们可以使用此信息作为一个条件。</span><span class="sxs-lookup"><span data-stu-id="bb543-238">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="bb543-239">他们还可以添加其他资源特征到筛选器来搜索具有指定项目的特定技能、教育和经验的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-239">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span> 

<span data-ttu-id="bb543-240">**场景：**已审核的项目已启动，并且高级项目经理角色在项目计划阶段预留为计划的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-240">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="bb543-241">资源经理现在已获得履行高级项目经理角色的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-241">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1.  <span data-ttu-id="bb543-242">单击**项目管理与核算** &gt; **项目资源** &gt; **资源列表**。</span><span class="sxs-lookup"><span data-stu-id="bb543-242">Click **Project management and accounting** &gt; **Project resources** &gt; **Resources list**.</span></span>
2.  <span data-ttu-id="bb543-243">在**资源**列表中，选择 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="bb543-243">In the **Resource** list, select **Daniel Goldschmidt**.</span></span>
3.  <span data-ttu-id="bb543-244">单击**项目资源** &gt; **维护** &gt; **资源角色**。</span><span class="sxs-lookup"><span data-stu-id="bb543-244">Click **Project resource** &gt; **Maintain** &gt; **Resource role**.</span></span>
4.  <span data-ttu-id="bb543-245">单击**新建**，然后输入以下值：</span><span class="sxs-lookup"><span data-stu-id="bb543-245">Click **New**, and enter the following values:</span></span>
    -   <span data-ttu-id="bb543-246">**生效** -（当前日期）</span><span class="sxs-lookup"><span data-stu-id="bb543-246">**Effective** - (The current date)</span></span>
    -   <span data-ttu-id="bb543-247">**到期** - 从不</span><span class="sxs-lookup"><span data-stu-id="bb543-247">**Expiration** - Never</span></span>
    -   <span data-ttu-id="bb543-248">**角色** - 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="bb543-248">**Role** - Senior Project Manager</span></span>
5.  <span data-ttu-id="bb543-249">单击**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-249">Click **Save**, and then close the page.</span></span>
6.  <span data-ttu-id="bb543-250">在**能力**选项卡上，添加 **ProjectMgmt** 技能和 **PMP** 证书。</span><span class="sxs-lookup"><span data-stu-id="bb543-250">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="bb543-251">设置基于角色的定价</span><span class="sxs-lookup"><span data-stu-id="bb543-251">Set up role-based pricing</span></span>
<span data-ttu-id="bb543-252">可为角色设置所有成本、销售以及转让价格。</span><span class="sxs-lookup"><span data-stu-id="bb543-252">All cost, sales, and transfer prices can be set up for roles.</span></span>

1.  <span data-ttu-id="bb543-253">单击**项目管理与核算** &gt; **设置** &gt; **价格** &gt; **销售价(工时)**。</span><span class="sxs-lookup"><span data-stu-id="bb543-253">Click **Project management and accounting** &gt; **Setup** &gt; **Prices** &gt; **Sales price (hour)**.</span></span>
2.  <span data-ttu-id="bb543-254">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="bb543-254">Click **New**.</span></span>
3.  <span data-ttu-id="bb543-255">输入生效日期。</span><span class="sxs-lookup"><span data-stu-id="bb543-255">Enter an effective date.</span></span>
4.  <span data-ttu-id="bb543-256">在**角色**列中，选择角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-256">In the **Role** column, select a role.</span></span>
5.  <span data-ttu-id="bb543-257">在**定价**列中，输入所选资源角色的价格。</span><span class="sxs-lookup"><span data-stu-id="bb543-257">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="bb543-258">建立项目团队</span><span class="sxs-lookup"><span data-stu-id="bb543-258">Form a project team</span></span>
<span data-ttu-id="bb543-259">若要使用之前在项目中设置的角色，项目经理必须将角色与项目关联。</span><span class="sxs-lookup"><span data-stu-id="bb543-259">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="bb543-260">可以为项目分配多个角色，Finance and Operations 将在预留期间自动标记这些角色以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="bb543-260">Multiple roles can be assigned for a project, and Finance and Operations automatically labels these roles during reservation to prevent confusion.</span></span> <span data-ttu-id="bb543-261">例如，如果项目经理需要三位软件工程师，将自动生成具有软件工程师 1、软件工程师 2 和软件工程师 3 作为其标签的软件工程师角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-261">For example, if the project manager requires three software engineers, three Software engineer roles that have software engineer 1, software engineer 2, and software engineer 3 as their labels are automatically generated.</span></span> <span data-ttu-id="bb543-262">如果之前为角色设置了角色特性，则在搜索资源期间，它们将应用为筛选器。</span><span class="sxs-lookup"><span data-stu-id="bb543-262">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="bb543-263">其他特性可以根据需要添加以进一步调整搜索。</span><span class="sxs-lookup"><span data-stu-id="bb543-263">Additional characteristics can be added as required to further refine the search.</span></span> 

<span data-ttu-id="bb543-264">查看设置还可以自定义以提供资源可用性的更好的视图。</span><span class="sxs-lookup"><span data-stu-id="bb543-264">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="bb543-265">具有显示每小时、每日、每周、每月、每季度和每年可用性的选项。</span><span class="sxs-lookup"><span data-stu-id="bb543-265">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="bb543-266">还有可以显示可用资源和剩余资源产能的选项。</span><span class="sxs-lookup"><span data-stu-id="bb543-266">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="bb543-267">在您评估活动或资源可用性的可用时间时，此选项对时间管理很有用。</span><span class="sxs-lookup"><span data-stu-id="bb543-267">This option is useful for time management when you're estimating available time for activities or resource availability.</span></span> 

<span data-ttu-id="bb543-268">项目经理可在页面上选择角色，然后，如果存在满足该需求的一个可用资源，选择预留符合角色的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-268">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="bb543-269">请注意，资源不必在计划阶段的此时间点预留。</span><span class="sxs-lookup"><span data-stu-id="bb543-269">Note that the resources don't have to be reserved at this point during the planning stage.</span></span> <span data-ttu-id="bb543-270">在您创建 WBS 时，可以使用项目的雇用资源替换角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-270">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="bb543-271">如果角色替换为 WBS 中的雇用资源，资源设置将自动更新项目团队列表和计划。</span><span class="sxs-lookup"><span data-stu-id="bb543-271">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span> 

<span data-ttu-id="bb543-272">[![包括角色和实际资源的项目团队列表](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-272">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="bb543-273">项目经理具有预订项目资源的不同选项，例如**剩余产能**、**全部产能**、**产能百分比**和**指定工时**。</span><span class="sxs-lookup"><span data-stu-id="bb543-273">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="bb543-274">如果资源分配更改，这些预订选项可以在任何时间取消。</span><span class="sxs-lookup"><span data-stu-id="bb543-274">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="bb543-275">支持以下两种预订类型：</span><span class="sxs-lookup"><span data-stu-id="bb543-275">Two types of booking are supported:</span></span>

-   <span data-ttu-id="bb543-276">**硬性预订** – 针对指定的持续时间审核并确认处理约定的资源预留。</span><span class="sxs-lookup"><span data-stu-id="bb543-276">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
-   <span data-ttu-id="bb543-277">**软性预订** – 针对指定的持续时间暂时设置处理约定的资源预留。</span><span class="sxs-lookup"><span data-stu-id="bb543-277">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="bb543-278">以下过程说明如何创建项目团队。</span><span class="sxs-lookup"><span data-stu-id="bb543-278">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="bb543-279">创建项目团队</span><span class="sxs-lookup"><span data-stu-id="bb543-279">Create a project team</span></span>

1.  <span data-ttu-id="bb543-280">在**所有项目**列表页上，选择某一项目，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bb543-280">On the **All projects** list page, select a project, and then click **Edit**.</span></span>
2.  <span data-ttu-id="bb543-281">在**项目团队和计划编制**选项卡上，在**计划结束日期**字段中，输入计划开始日期再加上一个月。</span><span class="sxs-lookup"><span data-stu-id="bb543-281">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="bb543-282">例如，如果计划开始日期为 2017 年 6 月 24 日 (24/06/2017)，输入 **24/07/2017**。</span><span class="sxs-lookup"><span data-stu-id="bb543-282">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3.  <span data-ttu-id="bb543-283">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="bb543-283">Click **Add**.</span></span>
4.  <span data-ttu-id="bb543-284">在**将角色添加到项目**窗格中，在**角色**字段中，选择 **高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="bb543-284">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5.  <span data-ttu-id="bb543-285">单击**所需能力**。</span><span class="sxs-lookup"><span data-stu-id="bb543-285">Click **Required competencies**.</span></span>
6.  <span data-ttu-id="bb543-286">默认情况下，在**选择特性**页上，选择您之前为高级项目经理角色设置的特性。</span><span class="sxs-lookup"><span data-stu-id="bb543-286">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="bb543-287">单击“**OK**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-287">Click **OK**.</span></span>
7.  <span data-ttu-id="bb543-288">在**将角色添加到项目**页上，在**资源数**字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="bb543-288">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8.  <span data-ttu-id="bb543-289">在**资源**字段中，查找显示具有所需能力的所有资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-289">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="bb543-290">选择 **Daniel Goldschmidt**，然后单击**创建**。</span><span class="sxs-lookup"><span data-stu-id="bb543-290">Select **Daniel Goldschmidt**, and then click **Create**.</span></span>
9.  <span data-ttu-id="bb543-291">在**项目**页上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="bb543-291">On the **Project** page, click **Add**.</span></span>
10. <span data-ttu-id="bb543-292">在**将角色添加到项目**窗格中，在**角色**字段中，选择 **团队成员**。</span><span class="sxs-lookup"><span data-stu-id="bb543-292">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="bb543-293">在**资源数**字段中输入 **5**。</span><span class="sxs-lookup"><span data-stu-id="bb543-293">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="bb543-294">单击“**创建**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-294">Click **Create**.</span></span>
12. <span data-ttu-id="bb543-295">在**项目**页上，单击**完成资源**。</span><span class="sxs-lookup"><span data-stu-id="bb543-295">On the **Projects** page, click **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="bb543-296">资源产能同步</span><span class="sxs-lookup"><span data-stu-id="bb543-296">Resource capacity synchronization</span></span>
<span data-ttu-id="bb543-297">资源同步流程帮助确保日历和基础日历信息深入到项目资源计划。</span><span class="sxs-lookup"><span data-stu-id="bb543-297">The processes for resource synchronization helps guarantee that the calendar and base calendar information trickles down into project resource scheduling.</span></span> <span data-ttu-id="bb543-298">如果更改日历，流程对项目资源计划进行所需的更新。</span><span class="sxs-lookup"><span data-stu-id="bb543-298">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="bb543-299">流程还有助于提高业绩，因为日历的资源信息提前同步，这样对资源计划信息的更新发生更快。</span><span class="sxs-lookup"><span data-stu-id="bb543-299">The processes also help improve performance, because the calendar’s resource information is synchronized in advance, so that updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="bb543-300">我们建议您批量计划流程，而不是一次计划一个。</span><span class="sxs-lookup"><span data-stu-id="bb543-300">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="bb543-301">否则，某些员工可能忘记上次同步信息的起迄日期。</span><span class="sxs-lookup"><span data-stu-id="bb543-301">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="bb543-302">如果不使用起迄日期，可能在日期同步时发生间隔。</span><span class="sxs-lookup"><span data-stu-id="bb543-302">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![日历同步](./media/projectresourcing04-1024x471.jpg)

<span data-ttu-id="bb543-304">**同步资源产能汇总**</span><span class="sxs-lookup"><span data-stu-id="bb543-304">**Synchronize resource capacity roll-ups**</span></span>

<span data-ttu-id="bb543-305">同步流程被设计为同步所有资源日历信息。</span><span class="sxs-lookup"><span data-stu-id="bb543-305">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="bb543-306">此信息包括有关对项目的资源日历产能表进行的任何更改的基本日历信息。</span><span class="sxs-lookup"><span data-stu-id="bb543-306">This information includes base calendar information about any changes to the project’s Resource calendar capacity table.</span></span> <span data-ttu-id="bb543-307">如果在项目中添加新的资源，同步可以帮助确保更新的日历信息可用。</span><span class="sxs-lookup"><span data-stu-id="bb543-307">If new resources are added in the project, synchronization helps ensure that the updated calendar information is available.</span></span> <span data-ttu-id="bb543-308">此同步随时都可以进行。</span><span class="sxs-lookup"><span data-stu-id="bb543-308">This synchronization can be done at any time.</span></span> 

<span data-ttu-id="bb543-309">我们建议您使用批次执行。</span><span class="sxs-lookup"><span data-stu-id="bb543-309">We recommend that you use a batch.</span></span> <span data-ttu-id="bb543-310">选项在同步产能预留中可用。</span><span class="sxs-lookup"><span data-stu-id="bb543-310">The options are available in synchronizing capacity reservations.</span></span>

-   <span data-ttu-id="bb543-311">单击**项目管理与核算** &gt; **定期** &gt; **产能同步** &gt; **同步资源产能汇总**。</span><span class="sxs-lookup"><span data-stu-id="bb543-311">Click **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>

| <span data-ttu-id="bb543-312">选项</span><span class="sxs-lookup"><span data-stu-id="bb543-312">Option</span></span> | <span data-ttu-id="bb543-313">说明</span><span class="sxs-lookup"><span data-stu-id="bb543-313">Description</span></span>                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb543-314">是</span><span class="sxs-lookup"><span data-stu-id="bb543-314">Yes</span></span>    | <span data-ttu-id="bb543-315">将所有资源数据与日历和基础日历信息同步，并且替换项目的资源产能日历中的所有信息。</span><span class="sxs-lookup"><span data-stu-id="bb543-315">Synchronize all resource data with calendar and base calendar information, and replace all information in the project's resource capacity calendar.</span></span>                                                  |
| <span data-ttu-id="bb543-316">否</span><span class="sxs-lookup"><span data-stu-id="bb543-316">No</span></span>     | <span data-ttu-id="bb543-317">基于日期间隔代码和指定的开始日期和结束日期同步资源数据。</span><span class="sxs-lookup"><span data-stu-id="bb543-317">Synchronize resource data, based on the date interval code, and the specified start and end dates.</span></span> <span data-ttu-id="bb543-318">此选项不删除现有数据，并只更新新添加的资源的信息。</span><span class="sxs-lookup"><span data-stu-id="bb543-318">This option doesn't remove existing data, and updates information only for newly added resources.</span></span> |

<span data-ttu-id="bb543-319">[![同步流程](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-319">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="bb543-320">在 WBS 模板上设置角色</span><span class="sxs-lookup"><span data-stu-id="bb543-320">Set up roles on WBS templates</span></span>
<span data-ttu-id="bb543-321">项目经理可以设置在创建新项目的 WBS 时可以应用的 WBS 模板。</span><span class="sxs-lookup"><span data-stu-id="bb543-321">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="bb543-322">项目经理可以在创建模板时添加角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-322">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="bb543-323">使用以下过程将角色分配到 WBS 模板。** **</span><span class="sxs-lookup"><span data-stu-id="bb543-323">Use the following procedure to assign a role to a WBS template.** **</span></span>

1.  <span data-ttu-id="bb543-324">单击**项目管理与核算** &gt; **设置** &gt; **项目** &gt; **工作结构分解模板**。</span><span class="sxs-lookup"><span data-stu-id="bb543-324">Click **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2.  <span data-ttu-id="bb543-325">单击所选 WBS 模板的**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="bb543-325">Click **Details** for a selected WBS template.</span></span>
3.  <span data-ttu-id="bb543-326">选择列表中的某一任务，然后在**角色**字段中，选择要分配给任务的角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-326">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="bb543-327">使用 WBS</span><span class="sxs-lookup"><span data-stu-id="bb543-327">Work with a WBS</span></span>

<span data-ttu-id="bb543-328">您可以创建新的 WBS，也可以从现有的 WBS 模板复制 WBS。</span><span class="sxs-lookup"><span data-stu-id="bb543-328">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="bb543-329">项目经理可以通过在 WBS 上将角色分配给新任务来轻松管理资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-329">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="bb543-330">角色可以在获取资源后替换，或者在确定执行任务的确认资源后替换。</span><span class="sxs-lookup"><span data-stu-id="bb543-330">Roles can be replaced after a resource is acquired, or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="bb543-331">此灵活性让项目经理可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="bb543-331">This flexibility lets project managers perform the following tasks:</span></span>

-   <span data-ttu-id="bb543-332">确定 WBS 工作包所需的资源的数量。</span><span class="sxs-lookup"><span data-stu-id="bb543-332">Identify the number of resources that are required for WBS work packages.</span></span>
-   <span data-ttu-id="bb543-333">评估项目成本。</span><span class="sxs-lookup"><span data-stu-id="bb543-333">Estimate project costs.</span></span>
-   <span data-ttu-id="bb543-334">确定初步预算。</span><span class="sxs-lookup"><span data-stu-id="bb543-334">Determine a preliminary budget.</span></span>
-   <span data-ttu-id="bb543-335">基于角色和资源估计活动持续时间。</span><span class="sxs-lookup"><span data-stu-id="bb543-335">Estimate activity duration, based on roles and resources.</span></span>
-   <span data-ttu-id="bb543-336">基于可用项目信息制定某些项目管理计划。</span><span class="sxs-lookup"><span data-stu-id="bb543-336">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="bb543-337">附加选项已添加到 WBS 中以便更好地使用资源功能。</span><span class="sxs-lookup"><span data-stu-id="bb543-337">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb543-338">选项</span><span class="sxs-lookup"><span data-stu-id="bb543-338">Option</span></span></th>
<th><span data-ttu-id="bb543-339">描述</span><span class="sxs-lookup"><span data-stu-id="bb543-339">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb543-340">资源分配</span><span class="sxs-lookup"><span data-stu-id="bb543-340">Resource assignments</span></span></td>
<td><span data-ttu-id="bb543-341">在 WBS 中查看任务的分配资源、日期、工时数和预订类型。</span><span class="sxs-lookup"><span data-stu-id="bb543-341">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb543-342">自动生成团队</span><span class="sxs-lookup"><span data-stu-id="bb543-342">Auto generate team</span></span></td>
<td><span data-ttu-id="bb543-343">通过使用与任务关联的角色自动添加计划资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-343">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="bb543-344">Finance and Operations 通过使用基于角色的多条件决策分析来自动建议计划资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-344">Finance and Operations automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="bb543-345">在 WBS 中为任务设置角色和工作量（小时）后，并且已发布结构，单击<strong>自动生成团队</strong>。</span><span class="sxs-lookup"><span data-stu-id="bb543-345">After the roles and effort (hours) have been set for the tasks in a WBS, and the structure has been released, click <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="bb543-346">所需计划资源数量将添加到 WBS 和<strong>项目和团队计划编制</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="bb543-346">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb543-347">资源（下拉列表）</span><span class="sxs-lookup"><span data-stu-id="bb543-347">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="bb543-348">在<strong>启动资源分配</strong>页上，您可以基于指定的持续时间选择要硬性预订或软性预订的资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-348">On the <strong>Launch resource assignment </strong>page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="bb543-349">您可以调整视图设置来查看和设置资源活动的持续时间。</span><span class="sxs-lookup"><span data-stu-id="bb543-349">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="bb543-350">您可以使用以下选项在工作包级别选择和分配资源：</span><span class="sxs-lookup"><span data-stu-id="bb543-350">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="bb543-351"><strong>接受</strong> – 确认对分配给任务的资源的更改。</span><span class="sxs-lookup"><span data-stu-id="bb543-351"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="bb543-352"><strong>取消</strong> – 取消对分配给任务的资源的更改。</span><span class="sxs-lookup"><span data-stu-id="bb543-352"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="bb543-353"><strong>自动分配</strong> –此选项选择角色与所选任务相符的可用雇用资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-353"><strong>Assign automatically</strong> – This option selects an available staffed resource with a matching role to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1.  <span data-ttu-id="bb543-354">单击**项目管理与核算** &gt; **项目** &gt; **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-354">Click **Project management and accounting** &gt; **Projects** &gt; **All projects**.</span></span>
2.  <span data-ttu-id="bb543-355">在列表中，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="bb543-355">In the list, select the **XYZ Upgrade Phase 2** project.</span></span>
3.  <span data-ttu-id="bb543-356">单击**计划** &gt; **活动** &gt; **工作分解结构**。</span><span class="sxs-lookup"><span data-stu-id="bb543-356">Click **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
4.  <span data-ttu-id="bb543-357">单击**新建**将以下一级活动添加到 WBS：</span><span class="sxs-lookup"><span data-stu-id="bb543-357">Click **New** to add the following level-one activities to the WBS:</span></span>
    -   <span data-ttu-id="bb543-358">启动</span><span class="sxs-lookup"><span data-stu-id="bb543-358">Initiating</span></span>
    -   <span data-ttu-id="bb543-359">计划</span><span class="sxs-lookup"><span data-stu-id="bb543-359">Planning</span></span>
    -   <span data-ttu-id="bb543-360">正在执行</span><span class="sxs-lookup"><span data-stu-id="bb543-360">Executing</span></span>
    -   <span data-ttu-id="bb543-361">监控和控制</span><span class="sxs-lookup"><span data-stu-id="bb543-361">Monitoring and Control</span></span>
    -   <span data-ttu-id="bb543-362">结束</span><span class="sxs-lookup"><span data-stu-id="bb543-362">Close</span></span>

5.  <span data-ttu-id="bb543-363">设置日期和工作量（小时），如下以下屏幕快照所示。[![设置日期和工作量](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="bb543-363">Set the dates and effort (hours), as shown in the following screenshot.[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>
6.  <span data-ttu-id="bb543-364">选择**启动**任务行，然后在**角色**字段中，选择**高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="bb543-364">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
7.  <span data-ttu-id="bb543-365">单击**发布**。</span><span class="sxs-lookup"><span data-stu-id="bb543-365">Click **Publish**.</span></span>
8.  <span data-ttu-id="bb543-366">在同一行中，在**资源**字段中，选择 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="bb543-366">On the same line, in the **Resource** field, select **Daniel Goldschmidt**.</span></span>
9.  <span data-ttu-id="bb543-367">单击**接受**。</span><span class="sxs-lookup"><span data-stu-id="bb543-367">Click **Accept**.</span></span>
10. <span data-ttu-id="bb543-368">选择**计划**任务行，然后在**角色**字段中，选择**业务分析员**。</span><span class="sxs-lookup"><span data-stu-id="bb543-368">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
11. <span data-ttu-id="bb543-369">单击**发布**，然后单击**自动生成团队**。</span><span class="sxs-lookup"><span data-stu-id="bb543-369">Click **Publish**, and then click **Auto generate team**.</span></span>
12. <span data-ttu-id="bb543-370">在出现的对话框中单击**是**。</span><span class="sxs-lookup"><span data-stu-id="bb543-370">In the dialog box that appears, click **Yes**.</span></span>
13. <span data-ttu-id="bb543-371">在**资源**字段中，确认值为**业务分析员 1**。</span><span class="sxs-lookup"><span data-stu-id="bb543-371">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
14. <span data-ttu-id="bb543-372">对于**业务分析员 1** 资源，打开查找，单击**启动资源分配窗体**。</span><span class="sxs-lookup"><span data-stu-id="bb543-372">For the **Business analyst 1** resource, open the lookup, and click **Launch resource assignments form**.</span></span>
15. <span data-ttu-id="bb543-373">为任务选择工作人员。</span><span class="sxs-lookup"><span data-stu-id="bb543-373">Select a worker for the task.</span></span>
16. <span data-ttu-id="bb543-374">单击**软性分配** &gt; **全部产能**。</span><span class="sxs-lookup"><span data-stu-id="bb543-374">Click **Soft assign** &gt; **Full capacity**.</span></span>
17. <span data-ttu-id="bb543-375">单击**保存**，关闭页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-375">Click **Save**, and close the page.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bb543-376">您不会收到指定的资源现在是 2 的警报，因为资源数量仍为 1。</span><span class="sxs-lookup"><span data-stu-id="bb543-376">You don't receive a warning that the specified resource is now 2, because the number of resources remains at 1.</span></span>
18. <span data-ttu-id="bb543-377">在**工作分解结构**页上，在 WBS 中验证资源分配，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="bb543-377">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then click **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="bb543-378">计划资源的资源完成</span><span class="sxs-lookup"><span data-stu-id="bb543-378">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="bb543-379">项目经理可为项目计划所需的资源角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-379">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="bb543-380">资源经理将在**资源完成**页上根据请求查看这些计划资源，并且可以分配实际资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-380">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1.  <span data-ttu-id="bb543-381">单击**项目管理与核算** &gt; **项目** &gt; **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-381">Click **Project management and accounting** &gt; **Projects** &gt; **All projects**.</span></span>
2.  <span data-ttu-id="bb543-382">在列表中，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="bb543-382">In the list, select the **XYZ Upgrade Phase 2** project.</span></span>
3.  <span data-ttu-id="bb543-383">单击**项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-383">Click **Project**.</span></span>
4.  <span data-ttu-id="bb543-384">单击**“编辑”**。</span><span class="sxs-lookup"><span data-stu-id="bb543-384">Click **Edit**.</span></span>
5.  <span data-ttu-id="bb543-385">在**项目团队和计划编制**选项卡上，** **单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="bb543-385">On the **Project team and scheduling** tab,** **click **Add**.</span></span>
6.  <span data-ttu-id="bb543-386">在**添加角色**对话框中，选择**软件开发人员**角色。</span><span class="sxs-lookup"><span data-stu-id="bb543-386">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
7.  <span data-ttu-id="bb543-387">单击“**创建**”。</span><span class="sxs-lookup"><span data-stu-id="bb543-387">Click **Create**.</span></span>
8.  <span data-ttu-id="bb543-388">关闭项目页面。</span><span class="sxs-lookup"><span data-stu-id="bb543-388">Close the project page.</span></span>
9.  <span data-ttu-id="bb543-389">单击**项目管理与核算** &gt; **项目资源** &gt; **资源完成**。</span><span class="sxs-lookup"><span data-stu-id="bb543-389">Click **Project management and accounting** &gt; **Project resources** &gt; **Resource fulfillment**.</span></span>
10. <span data-ttu-id="bb543-390">选择 **XYZ 升级项目第 2 阶段**项目的**软件开发人员 1**。</span><span class="sxs-lookup"><span data-stu-id="bb543-390">Select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
11. <span data-ttu-id="bb543-391">选择工作人员，然后单击**分配**。</span><span class="sxs-lookup"><span data-stu-id="bb543-391">Select a worker, and then click **Assign**.</span></span>
12. <span data-ttu-id="bb543-392">验证**软件开发人员 1** 的行已为 **XYZ 升级项目第 2 阶段**项目删除。</span><span class="sxs-lookup"><span data-stu-id="bb543-392">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
13. <span data-ttu-id="bb543-393">在**项目团队和计划编制**选项卡上，对 **XYZ 升级第 2 阶段**项目验证您在步骤 11 中选择的工作人员已添加为**软件开发人员**。</span><span class="sxs-lookup"><span data-stu-id="bb543-393">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in step 11 has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="bb543-394">项目资源询价</span><span class="sxs-lookup"><span data-stu-id="bb543-394">Requests for project resources</span></span>
<span data-ttu-id="bb543-395">项目资源计划功能仅支持资源经理为约定或项目分配雇用资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-395">The project resource scheduling functionality only supports resource managers to distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="bb543-396">若要启用此功能，请完成以下任务，或验证是否已完成这些任务。</span><span class="sxs-lookup"><span data-stu-id="bb543-396">To enable this functionality, complete the following tasks, or verify that they have been completed.</span></span>

-   <span data-ttu-id="bb543-397">设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="bb543-397">Set up number sequences.</span></span>
-   <span data-ttu-id="bb543-398">设置项目管理与核算工作流。</span><span class="sxs-lookup"><span data-stu-id="bb543-398">Set up project management and accounting workflows.</span></span>
-   <span data-ttu-id="bb543-399">启用资源请求工作流。</span><span class="sxs-lookup"><span data-stu-id="bb543-399">Enable resource request workflow.</span></span>

<span data-ttu-id="bb543-400">验证或完成上面的任务之后，可以根据需要完成下面的任务。</span><span class="sxs-lookup"><span data-stu-id="bb543-400">After you have either verified or completed the tasks above, you can complete the following tasks as needed.</span></span>

-   <span data-ttu-id="bb543-401">从软性预订雇用资源创建资源请求。</span><span class="sxs-lookup"><span data-stu-id="bb543-401">Create a resource request from a soft-booked staffed resource.</span></span>
-   <span data-ttu-id="bb543-402">监控资源请求。</span><span class="sxs-lookup"><span data-stu-id="bb543-402">Monitor resource requests.</span></span>
-   <span data-ttu-id="bb543-403">实施资源请求。</span><span class="sxs-lookup"><span data-stu-id="bb543-403">Fulfill resource requests.</span></span>
-   <span data-ttu-id="bb543-404">从 WBS 请求雇用资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-404">Request a staffed resource from WBS.</span></span>
-   <span data-ttu-id="bb543-405">在不请求雇用资源的情况下为项目预订资源。</span><span class="sxs-lookup"><span data-stu-id="bb543-405">Book resources to a project without a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="bb543-406">监控项目团队</span><span class="sxs-lookup"><span data-stu-id="bb543-406">Monitor project teams</span></span>
1.  <span data-ttu-id="bb543-407">单击**项目管理与核算** &gt; **项目** &gt; **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="bb543-407">Click **Project management and accounting** &gt; **Projects** &gt; **All projects**.</span></span>
2.  <span data-ttu-id="bb543-408">在项目列表中，单击 **XYZ 升级第 2 阶段**项目的**项目 ID** 链接。</span><span class="sxs-lookup"><span data-stu-id="bb543-408">In the list of projects, click the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
3.  <span data-ttu-id="bb543-409">在**项目团队和计划编制**快速选项卡上，确认列出的项目资源是正确的。</span><span class="sxs-lookup"><span data-stu-id="bb543-409">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>





