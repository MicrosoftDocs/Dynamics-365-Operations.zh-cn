---
title: "预算计划"
description: "此实验室的目的是提供预算计划领域中 Microsoft Dynamics 365 for Finance and Operations 功能更新的指导性视图。 此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。  此实验室专门介绍以下业务流程或任务：- 为预算计划创建组织层次结构和配置用户安全 - 定义预算计划方案、预算计划列、布局和 Excel 模板 - 创建和启用预算计划流程 - 通过从总帐拉出实际值创建预算计划文档 - 使用分配调整预算计划文档数据 - 在 Excel 中编辑预算计划文档数据"
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c8af5d3343bf8376dfec5a41cd03e1325b10b978
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning"></a><span data-ttu-id="4993c-105">预算计划</span><span class="sxs-lookup"><span data-stu-id="4993c-105">Budget planning</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4993c-106">此实验室的目的是提供预算计划领域中 Microsoft Dynamics 365 for Finance and Operations 功能更新的指导性视图。</span><span class="sxs-lookup"><span data-stu-id="4993c-106">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 for Finance and Operations functionality updates in Budget planning area.</span></span> <span data-ttu-id="4993c-107">此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。</span><span class="sxs-lookup"><span data-stu-id="4993c-107">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="4993c-108">此实验室专门介绍以下业务流程或任务：- 为预算计划创建组织层次结构和配置用户安全 - 定义预算计划方案、预算计划列、布局和 Excel 模板 - 创建和启用预算计划流程 - 通过从总帐拉出实际值创建预算计划文档 - 使用分配调整预算计划文档数据 - 在 Excel 中编辑预算计划文档数据</span><span class="sxs-lookup"><span data-stu-id="4993c-108">This lab will focus specifically on the following business processes or tasks -    - Creating organizational hierarchy for budget planning and configuring user security   - Defining budget plan scenarios, budget plan columns, layouts and Excel templates   - Creating and activating budget planning process   - Creating budget plan document by pulling in actuals from General ledger   - Using allocations to adjust budget plan document data   - Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="4993c-109">必备项</span><span class="sxs-lookup"><span data-stu-id="4993c-109">Prerequisites</span></span> 
------------------

<span data-ttu-id="4993c-110">对于本教程，您需要访问含 Contoso 演示数据的 Finance and Operations 环境，并需要在该实例上被配置为管理员。</span><span class="sxs-lookup"><span data-stu-id="4993c-110">For this tutorial, you’ll need to access the Finance and Operations environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="4993c-111">请勿为此实验室使用“专用”浏览器模式 - 如果需要，从浏览器中的任何其他帐户退出并使用 Finance and Operations 管理员凭据登录。</span><span class="sxs-lookup"><span data-stu-id="4993c-111">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with Finance and Operations administrator credentials.</span></span> <span data-ttu-id="4993c-112">在登录到 Finance and Operations 时，**必须**选中“我保持登录状态”复选框。</span><span class="sxs-lookup"><span data-stu-id="4993c-112">When signing into Finance and Operations, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="4993c-113">这将创建 Excel 应用程序当前需要的永久 Cookie。</span><span class="sxs-lookup"><span data-stu-id="4993c-113">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="4993c-114">如果您使用 IE 之外的浏览器登录到 Finance and Operations，那么系统将提示您在 Excel 应用程序内登录。</span><span class="sxs-lookup"><span data-stu-id="4993c-114">If you sign in to the Finance and Operations using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="4993c-115">在您单击 Excel 应用程序中的“登录”时，IE 弹出窗口将打开，在您登录时您**必须**选中“我保持登录状态”复选框。</span><span class="sxs-lookup"><span data-stu-id="4993c-115">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="4993c-116">如果单击 Excel 应用程序中的“登录”似乎未发生什么，那么您应该清除 IE Cookie 缓存。</span><span class="sxs-lookup"><span data-stu-id="4993c-116">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="4993c-117">**方案概览**</span><span class="sxs-lookup"><span data-stu-id="4993c-117">**Scenario overview**</span></span>
<span data-ttu-id="4993c-118">Julia 担任德国 Contoso Entertainment Systems (DEMF) 的财务经理。</span><span class="sxs-lookup"><span data-stu-id="4993c-118">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="4993c-119">由于 FY2016 即将来临，她需要为下一个年度设定公司的预算。</span><span class="sxs-lookup"><span data-stu-id="4993c-119">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="4993c-120">预算编制看似如下：</span><span class="sxs-lookup"><span data-stu-id="4993c-120">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="4993c-121">Julia 使用前一年的实际金额作为起点创建预算。</span><span class="sxs-lookup"><span data-stu-id="4993c-121">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="4993c-122">基于前一年的实际情况，她创建下一个年度 12 个月的估计</span><span class="sxs-lookup"><span data-stu-id="4993c-122">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="4993c-123">Julia 与首席财务官一起审核预算。</span><span class="sxs-lookup"><span data-stu-id="4993c-123">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="4993c-124">一旦完成，她将对预算进行必要的调整，然后完成预算编制。</span><span class="sxs-lookup"><span data-stu-id="4993c-124">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="4993c-125">方案的预算计划配置架构如下：</span><span class="sxs-lookup"><span data-stu-id="4993c-125">Budget planning configuration schema for the scenario looks as follows:</span></span>

![预算计划配置架构](./media/screenshot1-300x152.png)

<span data-ttu-id="4993c-127">Julia 使用以下 Excel 模板编制预算：</span><span class="sxs-lookup"><span data-stu-id="4993c-127">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="4993c-128">[![Excel 模板](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-128">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="4993c-129">练习 1：配置</span><span class="sxs-lookup"><span data-stu-id="4993c-129">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="4993c-130">**任务 1：创建组织的层次结构**</span><span class="sxs-lookup"><span data-stu-id="4993c-130">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="4993c-131">由于所有预算流程在财务部门进行，因此 Julia 需要创建非常简单的组织层次结构 – 仅包括财务部门。</span><span class="sxs-lookup"><span data-stu-id="4993c-131">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> <span data-ttu-id="4993c-132">1.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-132">1.1.</span></span> <span data-ttu-id="4993c-133">导航到组织层次结构（“组织管理”&gt;>“组织”&gt;“组织层次结构”），然后单击新的按钮</span><span class="sxs-lookup"><span data-stu-id="4993c-133">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click New button</span></span>

![组织层次结构](./media/screenshot3.png) 

<span data-ttu-id="4993c-135">1.2.</span><span class="sxs-lookup"><span data-stu-id="4993c-135">1.2.</span></span> <span data-ttu-id="4993c-136">键入组织层次结构的名称，然后单击按钮“分配用途”</span><span class="sxs-lookup"><span data-stu-id="4993c-136">Type the name for the organizational hierarchy and click button Assign purpose</span></span>

<span data-ttu-id="4993c-137">[![名称](./media/screenshot4.png)](./media/screenshot4.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-137">[![Name](./media/screenshot4.png)](./media/screenshot4.png)</span></span> 

<span data-ttu-id="4993c-138">1.3.</span><span class="sxs-lookup"><span data-stu-id="4993c-138">1.3.</span></span> <span data-ttu-id="4993c-139">选择预算计划用途，单击按钮“添加并分配新创建的组织层次结构”：</span><span class="sxs-lookup"><span data-stu-id="4993c-139">Select Budget planning purpose, click button Add and assign newly created organizational hierarchy:</span></span> 

<span data-ttu-id="4993c-140">[![分配用途](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-140">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="4993c-141">1.4.</span><span class="sxs-lookup"><span data-stu-id="4993c-141">1.4.</span></span> <span data-ttu-id="4993c-142">对安全组织用途重复上述步骤。</span><span class="sxs-lookup"><span data-stu-id="4993c-142">Repeat the step above for Security organizational purpose.</span></span> <span data-ttu-id="4993c-143">完成后关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="4993c-143">Close the form when done.</span></span>

<span data-ttu-id="4993c-144">[![安全组织](./media/screenshot6.png)](./media/screenshot6.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-144">[![Security org](./media/screenshot6.png)](./media/screenshot6.png)</span></span>

<span data-ttu-id="4993c-145">1.5.</span><span class="sxs-lookup"><span data-stu-id="4993c-145">1.5.</span></span> <span data-ttu-id="4993c-146">在“组织层次结构”窗体中单击按钮“查看”。</span><span class="sxs-lookup"><span data-stu-id="4993c-146">In the Organizational Hierarchies form click button View.</span></span> <span data-ttu-id="4993c-147">单击层次结构设计器中的“编辑”，并通过单击按钮“插入”创建层次结构。</span><span class="sxs-lookup"><span data-stu-id="4993c-147">Click Edit in the Hierarchy designer and create a hierarchy by clicking button Insert.</span></span>

<span data-ttu-id="4993c-148">[![插入](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-148">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="4993c-149">1.6.</span><span class="sxs-lookup"><span data-stu-id="4993c-149">1.6.</span></span> <span data-ttu-id="4993c-150">为预算编制层次结构选择财务部门。</span><span class="sxs-lookup"><span data-stu-id="4993c-150">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="4993c-151">[![财务](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-151">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="4993c-152">1.7.</span><span class="sxs-lookup"><span data-stu-id="4993c-152">1.7.</span></span> <span data-ttu-id="4993c-153">在完成后，单击按钮“发布”和“关闭”。</span><span class="sxs-lookup"><span data-stu-id="4993c-153">When done, click button Publish and Close.</span></span> <span data-ttu-id="4993c-154">选择 1/1/2015 用作层次结构发布的生效日期。</span><span class="sxs-lookup"><span data-stu-id="4993c-154">Select 1/1/2015 as effective date for hierarchy publishing.</span></span>

<span data-ttu-id="4993c-155">[![有效日期](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-155">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="4993c-156">任务 2：配置用户安全性</span><span class="sxs-lookup"><span data-stu-id="4993c-156">Task 2: Configure user security</span></span>
<span data-ttu-id="4993c-157">预算计划使用特殊安全策略配置对预算计划数据的访问。</span><span class="sxs-lookup"><span data-stu-id="4993c-157">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="4993c-158">Julia 需要授予她自己对财务预算计划的访问权限。</span><span class="sxs-lookup"><span data-stu-id="4993c-158">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="4993c-159">2.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-159">2.1.</span></span> <span data-ttu-id="4993c-160">切换到 DEMF 法人环境。</span><span class="sxs-lookup"><span data-stu-id="4993c-160">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="4993c-161">2.2。</span><span class="sxs-lookup"><span data-stu-id="4993c-161">2.2.</span></span> <span data-ttu-id="4993c-162">导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。</span><span class="sxs-lookup"><span data-stu-id="4993c-162">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="4993c-163">在“参数”选项卡上，设置“安全模型值”为“基于安全组织”</span><span class="sxs-lookup"><span data-stu-id="4993c-163">In Parameters tab, set the Security model value to Based on security organizations</span></span> 

<span data-ttu-id="4993c-164">[![参数](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-164">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="4993c-165">2.3。</span><span class="sxs-lookup"><span data-stu-id="4993c-165">2.3.</span></span> <span data-ttu-id="4993c-166">导致至“系统管理”&gt;“用户”&gt;“用户”。</span><span class="sxs-lookup"><span data-stu-id="4993c-166">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="4993c-167">给予用户 Admin (Julia Funderburk) 预算经理角色。</span><span class="sxs-lookup"><span data-stu-id="4993c-167">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="4993c-168">[![预算管理器](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-168">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="4993c-169">2.4。</span><span class="sxs-lookup"><span data-stu-id="4993c-169">2.4.</span></span> <span data-ttu-id="4993c-170">领料用户角色单击“分配组织”屏幕截图</span><span class="sxs-lookup"><span data-stu-id="4993c-170">Pick user role and click Assign organizations</span></span> 

<span data-ttu-id="4993c-171">[![分配组织](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-171">[![Assign org](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="4993c-172">2.5。</span><span class="sxs-lookup"><span data-stu-id="4993c-172">2.5.</span></span> <span data-ttu-id="4993c-173">选择“授予访问特定组织的权限”。</span><span class="sxs-lookup"><span data-stu-id="4993c-173">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="4993c-174">在第一步中选择创建的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="4993c-174">Pick Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="4993c-175">选择财务节点然后单击“授予组织及其子组织的访问权限”按钮</span><span class="sxs-lookup"><span data-stu-id="4993c-175">Pick Finance node and click Grant with children button</span></span> 

<span data-ttu-id="4993c-176">***重要信息！***</span><span class="sxs-lookup"><span data-stu-id="4993c-176">***Important!***</span></span> <span data-ttu-id="4993c-177">*确保在执行此任务时您位于 DEMF 法人环境中，因为组织安全按法人应用*</span><span class="sxs-lookup"><span data-stu-id="4993c-177">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

<span data-ttu-id="4993c-178">[![授予访问权](./media/screenshot14.png)](./media/screenshot14.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-178">[![Grant access](./media/screenshot14.png)](./media/screenshot14.png)</span></span>

### <a name="task-3-create-scenarios"></a><span data-ttu-id="4993c-179">任务 3：创建方案</span><span class="sxs-lookup"><span data-stu-id="4993c-179">Task 3: Create scenarios</span></span>
<span data-ttu-id="4993c-180">3.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-180">3.1.</span></span> <span data-ttu-id="4993c-181">导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。</span><span class="sxs-lookup"><span data-stu-id="4993c-181">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="4993c-182">在“方案”页，请注意我们在此实验室将进一步使用的方案：上一年实际和预算。</span><span class="sxs-lookup"><span data-stu-id="4993c-182">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="4993c-183">*注意：如果您需要，可以为此练习创建新的方案并使用这些方案。*</span><span class="sxs-lookup"><span data-stu-id="4993c-183">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="4993c-184">[![新方案](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-184">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="4993c-185">*注意：因为 Julia 未为预算编制使用正式审核流程，我们在此实验室将跳过工作流、阶段和工作流阶段设置，并且将使用现有的自动 – 审核工作流设置。请参阅此工作流配置的附录。*</span><span class="sxs-lookup"><span data-stu-id="4993c-185">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="4993c-186">任务4：创建预算计划列</span><span class="sxs-lookup"><span data-stu-id="4993c-186">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="4993c-187">预算计划列可以是基于货币或基于数量的列，可用于预算计划文档格式。</span><span class="sxs-lookup"><span data-stu-id="4993c-187">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="4993c-188">在我们的示例中，我们需要创建上一年实际列以及在一个预算年度中表示每个月的 12 个列。</span><span class="sxs-lookup"><span data-stu-id="4993c-188">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="4993c-189">列可以通过单击“添加”按钮并填充值来创建，也可以使用数据实体协助。</span><span class="sxs-lookup"><span data-stu-id="4993c-189">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="4993c-190">在此实验室，我们将使用数据实体填充值。</span><span class="sxs-lookup"><span data-stu-id="4993c-190">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="4993c-191">4.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-191">4.1.</span></span> <span data-ttu-id="4993c-192">在“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划配置”中打开“列”页。</span><span class="sxs-lookup"><span data-stu-id="4993c-192">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Columns page.</span></span> <span data-ttu-id="4993c-193">单击窗体右上角的 Office 按钮并且选择“列”（未筛选）</span><span class="sxs-lookup"><span data-stu-id="4993c-193">Click Office button on the top right corner of the form and pick Columns (unfiltered)</span></span> 

<span data-ttu-id="4993c-194">[![未筛选列](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-194">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="4993c-195">4.2。</span><span class="sxs-lookup"><span data-stu-id="4993c-195">4.2.</span></span> <span data-ttu-id="4993c-196">系统将打开用于填充值的 Excel 工作簿。</span><span class="sxs-lookup"><span data-stu-id="4993c-196">System will open Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="4993c-197">如果系统提示，单击“启用编辑”和“信任此应用程序”</span><span class="sxs-lookup"><span data-stu-id="4993c-197">If prompted, click Enable Editing and Trust this app</span></span> 

<span data-ttu-id="4993c-198">[![启用编辑](./media/screenshot18.png)](./media/screenshot18.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-198">[![Enable editing](./media/screenshot18.png)](./media/screenshot18.png)</span></span> 

<span data-ttu-id="4993c-199">[![信任此应用程序](./media/screenshot17.png)](./media/screenshot17.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-199">[![Trust this app](./media/screenshot17.png)](./media/screenshot17.png)</span></span>

<span data-ttu-id="4993c-200">4.3。</span><span class="sxs-lookup"><span data-stu-id="4993c-200">4.3.</span></span> <span data-ttu-id="4993c-201">我们需要更多列来容纳这些值。</span><span class="sxs-lookup"><span data-stu-id="4993c-201">We will need more columns to fill the values in.</span></span> <span data-ttu-id="4993c-202">在右侧窗格中单击“设计”添加列到网格：</span><span class="sxs-lookup"><span data-stu-id="4993c-202">Click Design on the right side pane to add the columns to the grid:</span></span> 

<span data-ttu-id="4993c-203">[![设计](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-203">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="4993c-204">4.4。</span><span class="sxs-lookup"><span data-stu-id="4993c-204">4.4.</span></span> <span data-ttu-id="4993c-205">单击 PlanColumns 旁边的小铅笔按钮查看可添加到网格的列</span><span class="sxs-lookup"><span data-stu-id="4993c-205">Click little pencil button next to PlanColumns to see available columns to add to the grid</span></span> 

<span data-ttu-id="4993c-206">[![编辑](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-206">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="4993c-207">4.5。</span><span class="sxs-lookup"><span data-stu-id="4993c-207">4.5.</span></span> <span data-ttu-id="4993c-208">双击每个可用字段并将其添加到所选字段并单击“更新”</span><span class="sxs-lookup"><span data-stu-id="4993c-208">Double click on each available field to add them to Selected fields and click Update</span></span> 

![更新](./media/screenshot21.png)<span data-ttu-id="4993c-210">](./media/screenshot21.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-210">](./media/screenshot21.png)</span></span> 

<span data-ttu-id="4993c-211">4.6。</span><span class="sxs-lookup"><span data-stu-id="4993c-211">4.6.</span></span> <span data-ttu-id="4993c-212">在 Excel 表中添加需要创建的所有列。</span><span class="sxs-lookup"><span data-stu-id="4993c-212">In Excel table add all the columns that need to be created.</span></span> <span data-ttu-id="4993c-213">在 Excel 中使用 AutoFill 功能快速添加行。</span><span class="sxs-lookup"><span data-stu-id="4993c-213">Use AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="4993c-214">确保行添加为表的一部分（在使用垂直滚动时，您应能够看到网格顶部的列标题）</span><span class="sxs-lookup"><span data-stu-id="4993c-214">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid)</span></span> 

<span data-ttu-id="4993c-215">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-215">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span></span> 

<span data-ttu-id="4993c-216">4.7。</span><span class="sxs-lookup"><span data-stu-id="4993c-216">4.7.</span></span> <span data-ttu-id="4993c-217">返回 Finance and Operations 并刷新页面。</span><span class="sxs-lookup"><span data-stu-id="4993c-217">Return to Finance and Operations and refresh the page.</span></span> <span data-ttu-id="4993c-218">Finance and Operations 中将显示发布的值。</span><span class="sxs-lookup"><span data-stu-id="4993c-218">Published values will appear in Finance and Operations.</span></span> 

<span data-ttu-id="4993c-219">[![刷新](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-219">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="4993c-220">任务 5：创建预算计划文档格式和模板</span><span class="sxs-lookup"><span data-stu-id="4993c-220">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="4993c-221">格式定义当用户打开预算计划文档时，预算计划文档行网格将呈现的外观。</span><span class="sxs-lookup"><span data-stu-id="4993c-221">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="4993c-222">它还可以切换预算计划文档的格式，可以在不同的角度查看相同数据。</span><span class="sxs-lookup"><span data-stu-id="4993c-222">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="4993c-223">现在，因为她将列定义为用于我们的预算计划文档，Julia 需要创建预算计划文档格式，其将看起来类似于她用于创建预算数据的 Excel 表（参见此实验室的“方案概览”部分）</span><span class="sxs-lookup"><span data-stu-id="4993c-223">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="4993c-224">5.1。</span><span class="sxs-lookup"><span data-stu-id="4993c-224">5.1.</span></span> <span data-ttu-id="4993c-225">在“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划配置”中打开“格式”页。</span><span class="sxs-lookup"><span data-stu-id="4993c-225">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Layouts page.</span></span> <span data-ttu-id="4993c-226">创建月度预算条目的新格式：</span><span class="sxs-lookup"><span data-stu-id="4993c-226">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="4993c-227">选择 MA+BU 维度集将主科目和业务单位包括在格式中。</span><span class="sxs-lookup"><span data-stu-id="4993c-227">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="4993c-228">列出在“元素”部分的上一步中创建的所有预算计划列。</span><span class="sxs-lookup"><span data-stu-id="4993c-228">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="4993c-229">允许除上一年度以外的所有实际可以编辑。</span><span class="sxs-lookup"><span data-stu-id="4993c-229">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="4993c-230">单击“描述”按钮选择哪些财务维度应在网格中显示描述。</span><span class="sxs-lookup"><span data-stu-id="4993c-230">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="4993c-231">[![描述](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-231">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="4993c-232">基于预算计划格式定义，我们可以创建一个用作编辑预算数据备选方法的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="4993c-232">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="4993c-233">因为 Excel 模板必须与预算计划格式定义匹配，您在生成 Excel 模板后将无法编辑预算计划格式，因此应在所有格式组件定义后执行此任务。</span><span class="sxs-lookup"><span data-stu-id="4993c-233">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="4993c-234">5.2.</span><span class="sxs-lookup"><span data-stu-id="4993c-234">5.2.</span></span> <span data-ttu-id="4993c-235">对于步骤 5.1. 中创建的布局，</span><span class="sxs-lookup"><span data-stu-id="4993c-235">For the layout created in the 5.1.</span></span> <span data-ttu-id="4993c-236">单击按钮“模板”&gt;“生成”。</span><span class="sxs-lookup"><span data-stu-id="4993c-236">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="4993c-237">确认警告消息。</span><span class="sxs-lookup"><span data-stu-id="4993c-237">Confirm the warning message.</span></span> <span data-ttu-id="4993c-238">若要查看模板，单击“模板”&gt;“查看”。</span><span class="sxs-lookup"><span data-stu-id="4993c-238">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="4993c-239">*注意：确保选择“另存为”并且选择应存储以便编辑该模板的位置。如果用户在对话框中选择打开“打开”而不保存，已完成的文档更改在文件关闭时不会保留。* 
[![模板视图](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-239">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="4993c-240">5.3。</span><span class="sxs-lookup"><span data-stu-id="4993c-240">5.3.</span></span> <span data-ttu-id="4993c-241">&lt;可选步骤&gt; 修改 Excel 模板使它看似对用户更易用 – 添加汇总公式、标题字段、格式等。保存更改并上载该文件到预算计划格式，方法是通过单击“布局”&gt;“上载”[ ![上载](./media/screenshot26.png)](./media/screenshot26.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-241">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload [![Upload](./media/screenshot26.png)](./media/screenshot26.png)</span></span>

### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="4993c-242">任务 6：创建预算计划流程</span><span class="sxs-lookup"><span data-stu-id="4993c-242">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="4993c-243">Julia 需要创建和激活合并上述所有设置的新预算计划流程以开始输入预算计划。</span><span class="sxs-lookup"><span data-stu-id="4993c-243">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="4993c-244">预算计划流程定义哪些预算组织、工作流、格式和模板用于创建预算计划。</span><span class="sxs-lookup"><span data-stu-id="4993c-244">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="4993c-245">6.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-245">6.1.</span></span> <span data-ttu-id="4993c-246">导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划流程”并创建新记录。</span><span class="sxs-lookup"><span data-stu-id="4993c-246">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process and create a new record.</span></span>

-   <span data-ttu-id="4993c-247">预算计划流程 – DEMF 预算编制 FY2016</span><span class="sxs-lookup"><span data-stu-id="4993c-247">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="4993c-248">预算周期 – FY2016</span><span class="sxs-lookup"><span data-stu-id="4993c-248">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="4993c-249">分类帐 – DEMF</span><span class="sxs-lookup"><span data-stu-id="4993c-249">Ledger – DEMF</span></span>
-   <span data-ttu-id="4993c-250">默认科目结构 – 制造损益</span><span class="sxs-lookup"><span data-stu-id="4993c-250">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="4993c-251">组织层次结构 – 选择在实验室开始时创建的层次结构</span><span class="sxs-lookup"><span data-stu-id="4993c-251">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="4993c-252">预算计划工作流 – 为财务部门分配自动 – 审核工作流</span><span class="sxs-lookup"><span data-stu-id="4993c-252">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="4993c-253">在预算计划阶段规则和模板中，为每个工作流预算计划阶段选择是否允许“添加行”和“修改行”，以及哪些格式应在默认情况下使用</span><span class="sxs-lookup"><span data-stu-id="4993c-253">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="4993c-254">*注意：您可以创建其他文档格式，并且通过单击“备选格式”按钮指定它们可用于预算计划工作流阶段。*</span><span class="sxs-lookup"><span data-stu-id="4993c-254">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="4993c-255">[![备用布局](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-255">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="4993c-256">6.2。</span><span class="sxs-lookup"><span data-stu-id="4993c-256">6.2.</span></span> <span data-ttu-id="4993c-257">选择“操作”&gt;“激活”激活此预算计划工作流</span><span class="sxs-lookup"><span data-stu-id="4993c-257">Select Actions &gt; Activate to activate this budget planning workflow</span></span> 

<span data-ttu-id="4993c-258">[![启用](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-258">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="4993c-259">练习 2：流程模似</span><span class="sxs-lookup"><span data-stu-id="4993c-259">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="4993c-260">任务 7：从总帐生成预算计划的初始数据</span><span class="sxs-lookup"><span data-stu-id="4993c-260">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="4993c-261">7.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-261">7.1.</span></span> <span data-ttu-id="4993c-262">导航到“预算编制”&gt;“定期”&gt;“从总帐生成预算计划”。</span><span class="sxs-lookup"><span data-stu-id="4993c-262">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="4993c-263">填写定期流程参数，然后单击“生成”按钮。</span><span class="sxs-lookup"><span data-stu-id="4993c-263">Fill in the periodic process parameters and click button Generate.</span></span> 

<span data-ttu-id="4993c-264">[![生成](./media/screenshot29.png)](./media/screenshot29.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-264">[![Generate](./media/screenshot29.png)](./media/screenshot29.png)</span></span> 

<span data-ttu-id="4993c-265">7.2。</span><span class="sxs-lookup"><span data-stu-id="4993c-265">7.2.</span></span> <span data-ttu-id="4993c-266">导航到“预算编制”&gt;“预算计划”查找“生成”流程创建的预算计划。</span><span class="sxs-lookup"><span data-stu-id="4993c-266">Navigate to Budgeting &gt; Budget plans to find a budget plan created by Generate process.</span></span> 

<span data-ttu-id="4993c-267">[![预算计划](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-267">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="4993c-268">7.3。</span><span class="sxs-lookup"><span data-stu-id="4993c-268">7.3.</span></span> <span data-ttu-id="4993c-269">通过单击文档编号超链接打开文档详细信息。</span><span class="sxs-lookup"><span data-stu-id="4993c-269">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="4993c-270">预算计划将显示为在此实验室期间创建的格式中定义的格式</span><span class="sxs-lookup"><span data-stu-id="4993c-270">Budget plan is displayed as defined in the layout created during this lab</span></span> 

<span data-ttu-id="4993c-271">[![预算计划显示](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-271">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="4993c-272">任务 8：基于上一年度实际创建当前年度预算</span><span class="sxs-lookup"><span data-stu-id="4993c-272">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="4993c-273">分配方法可用于在预算计划中轻松地将预算计划的信息从一个方案复制到另一个/在各个期间内分布它们/分配到维度。</span><span class="sxs-lookup"><span data-stu-id="4993c-273">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="4993c-274">我们将使用分配来从上一年度实际创建当前年度预算。</span><span class="sxs-lookup"><span data-stu-id="4993c-274">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="4993c-275">8.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-275">8.1.</span></span> <span data-ttu-id="4993c-276">在预算计划文档网格中选择所有行，然后单击按钮分配预算</span><span class="sxs-lookup"><span data-stu-id="4993c-276">Pick all lines in the budget plan document grid and click button allocate budget</span></span> 

<span data-ttu-id="4993c-277">[![所有行](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-277">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="4993c-278">8.2。</span><span class="sxs-lookup"><span data-stu-id="4993c-278">8.2.</span></span> <span data-ttu-id="4993c-279">选择分配方法、期间参数、源和目标方案并单击“分配”</span><span class="sxs-lookup"><span data-stu-id="4993c-279">Select allocation method, Period key, Source and destination scenarios and click Allocate</span></span> 

<span data-ttu-id="4993c-280">[![分配](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-280">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="4993c-281">将把上一年的实际金额复制到当年年度预算，并使用销售曲线期间参数在期间内分配它们。</span><span class="sxs-lookup"><span data-stu-id="4993c-281">The previous year actual amounts will be copied to current year budget and allocate them across periods using Sales curve period key.</span></span> 

<span data-ttu-id="4993c-282">[![销售曲线](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-282">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="4993c-283">任务 9：使用 Excel 调整预算计划文档并完成文档</span><span class="sxs-lookup"><span data-stu-id="4993c-283">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="4993c-284">9.1.</span><span class="sxs-lookup"><span data-stu-id="4993c-284">9.1.</span></span> <span data-ttu-id="4993c-285">单击按钮“工作表”在 Excel 中打开文档内容</span><span class="sxs-lookup"><span data-stu-id="4993c-285">Click Button worksheet to open document contents in Excel</span></span>

<span data-ttu-id="4993c-286">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-286">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span></span>

<span data-ttu-id="4993c-287">9.2.</span><span class="sxs-lookup"><span data-stu-id="4993c-287">9.2.</span></span> <span data-ttu-id="4993c-288">在 Excel 工作簿打开时，调整预算计划文档中的数字，然后单击“发布”按钮。</span><span class="sxs-lookup"><span data-stu-id="4993c-288">When Excel workbook opens, adjust the numbers in budget plan document and click button Publish.</span></span>

<span data-ttu-id="4993c-289">[![发布](./media/screenshot36.png)](./media/screenshot36.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-289">[![Publish](./media/screenshot36.png)](./media/screenshot36.png)</span></span>

<span data-ttu-id="4993c-290">9.3.</span><span class="sxs-lookup"><span data-stu-id="4993c-290">9.3.</span></span> <span data-ttu-id="4993c-291">返回到 Finance and Operations 中的预算计划文档。</span><span class="sxs-lookup"><span data-stu-id="4993c-291">Return to budget plan document in Finance and Operations.</span></span> <span data-ttu-id="4993c-292">单击“工作流”&gt;“提交”自动审核文档</span><span class="sxs-lookup"><span data-stu-id="4993c-292">Click Workflow &gt; Submit to Auto-approve the document</span></span>

<span data-ttu-id="4993c-293">[![自动审核](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-293">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="4993c-294">一旦完成工作流，预算计划文档阶段更改为“已审核”。</span><span class="sxs-lookup"><span data-stu-id="4993c-294">Once workflow completes, budget plan document stage changes to Approved.</span></span> <span data-ttu-id="4993c-295">[![已审核](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-295">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="4993c-296">附录</span><span class="sxs-lookup"><span data-stu-id="4993c-296">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="4993c-297">自动审核工作流配置</span><span class="sxs-lookup"><span data-stu-id="4993c-297">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="4993c-298">A.</span><span class="sxs-lookup"><span data-stu-id="4993c-298">A.</span></span> <span data-ttu-id="4993c-299">“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算”工作流 使用模板预算计划工作流创建新工作流：</span><span class="sxs-lookup"><span data-stu-id="4993c-299">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="4993c-300">[![创建新工作流](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-300">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="4993c-301">此工作流只包含一任务 – 阶段转换预算计划</span><span class="sxs-lookup"><span data-stu-id="4993c-301">This workflow will contain only one task – Stage transition budget plan</span></span> 

<span data-ttu-id="4993c-302">[![阶段转换预算计划](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-302">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="4993c-303">保存并激活工作流。</span><span class="sxs-lookup"><span data-stu-id="4993c-303">Save and activate the workflow.</span></span> 

<span data-ttu-id="4993c-304">B.</span><span class="sxs-lookup"><span data-stu-id="4993c-304">B.</span></span> <span data-ttu-id="4993c-305">导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。</span><span class="sxs-lookup"><span data-stu-id="4993c-305">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="4993c-306">在“阶段”选项卡上创建 2 个阶段 – 初始和已提交</span><span class="sxs-lookup"><span data-stu-id="4993c-306">In Stages tab create 2 stages – Initial and Submitted</span></span> 

<span data-ttu-id="4993c-307">[![初始和已提交](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-307">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="4993c-308">C.</span><span class="sxs-lookup"><span data-stu-id="4993c-308">C.</span></span> <span data-ttu-id="4993c-309">导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。</span><span class="sxs-lookup"><span data-stu-id="4993c-309">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="4993c-310">在“工作流阶段”选项卡中，将在步骤 A 中创建的工作流自动 – 审核与阶段“初始”和“已提交”关联</span><span class="sxs-lookup"><span data-stu-id="4993c-310">In Workflow Stages tab Associate the workflow Auto – approve created in A step with the stages Initial and Submitted</span></span> 

<span data-ttu-id="4993c-311">[![预算和预算计划](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="4993c-311">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  




