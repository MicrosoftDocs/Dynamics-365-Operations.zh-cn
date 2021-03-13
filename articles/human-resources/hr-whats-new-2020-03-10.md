---
title: Dynamics 365 Human Resources（2020 年 3 月 10 日）中的新增功能或更改
description: 本文介绍 2020 年 3 月 10 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1819ddb996d83b03151eb228ec740f603f98409
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127985"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a><span data-ttu-id="6e196-103">Dynamics 365 Human Resources（2020 年 3 月 10 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="6e196-103">What's new or changed in Dynamics 365 Human Resources (March 10, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6e196-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="6e196-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6e196-105">更改适用于内部版本号 8.1.2985。</span><span class="sxs-lookup"><span data-stu-id="6e196-105">Changes apply to build number 8.1.2985.</span></span> <span data-ttu-id="6e196-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="6e196-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="cant-access-skill-gap-analysis-report-394460"></a><span data-ttu-id="6e196-107">不能访问技能差距分析报表 (394460)</span><span class="sxs-lookup"><span data-stu-id="6e196-107">Can't access skill gap analysis report (394460)</span></span>

<span data-ttu-id="6e196-108">Dynamics 365 Human Resources 中不支持此报表。</span><span class="sxs-lookup"><span data-stu-id="6e196-108">This report isn't supported in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6e196-109">已删除了用于打印 SSRS 报表的菜单项。</span><span class="sxs-lookup"><span data-stu-id="6e196-109">The menu item to print the SSRS report is removed.</span></span>

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a><span data-ttu-id="6e196-110">访问“开始”页时显示不正确的消息 (417950)</span><span class="sxs-lookup"><span data-stu-id="6e196-110">Incorrect message accessing the Getting Started page (417950)</span></span>

<span data-ttu-id="6e196-111">进行此更改之后，如果您无权访问窗体，安全措施将隐藏此菜单项。</span><span class="sxs-lookup"><span data-stu-id="6e196-111">With this change, security hides this menu item if you don't have access to the form.</span></span>

## <a name="streamlined-task-maintenance-for-employees-380538"></a><span data-ttu-id="6e196-112">简化了员工的任务维护 (380538)</span><span class="sxs-lookup"><span data-stu-id="6e196-112">Streamlined task maintenance for employees (380538)</span></span>

<span data-ttu-id="6e196-113">工作人员任务维护窗体列出了员工在入职、离职、转移和业务流程中的所有任务。</span><span class="sxs-lookup"><span data-stu-id="6e196-113">The worker task maintenance form lists all tasks for an employee across onboarding, offboarding, transitions, and business processes.</span></span> <span data-ttu-id="6e196-114">您可以删除，重新分配或更新任务状态。</span><span class="sxs-lookup"><span data-stu-id="6e196-114">You can delete, reassign, or update the status of tasks.</span></span>

<span data-ttu-id="6e196-115">示例：Benjamin Martin 是福利管理员。</span><span class="sxs-lookup"><span data-stu-id="6e196-115">Example: Benjamin Martin is a benefits administrator.</span></span> <span data-ttu-id="6e196-116">员工入职期间，将创建任务以供 Benjamin 检查新员工选择的福利。</span><span class="sxs-lookup"><span data-stu-id="6e196-116">During employee onboarding, tasks are created for Benjamin to review the new employee’s benefit selection.</span></span> <span data-ttu-id="6e196-117">Benjamin 有自己已完成的过去任务和需要其完成的未来任务。</span><span class="sxs-lookup"><span data-stu-id="6e196-117">Benjamin has past tasks that he's completed, and future tasks that he needs to complete.</span></span> <span data-ttu-id="6e196-118">Benjamin 决定离开公司，因此需要重新分配或删除他的任务。</span><span class="sxs-lookup"><span data-stu-id="6e196-118">Benjamin decides to leave the company, so his tasks need to be either re-assigned or removed.</span></span> <span data-ttu-id="6e196-119">可通过（**工作人员** 窗体的操作窗格中的）任务维护窗体将 Benjamin 的所有任务重新分配给其他工作人员或将其删除。</span><span class="sxs-lookup"><span data-stu-id="6e196-119">The task maintenance form (in the action pane of the **Worker** form) allows all of Benjamin’s tasks to be re-assigned to another worker or removed.</span></span>  

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="6e196-120">Dataverse 现已可用，并具有以下更改：</span><span class="sxs-lookup"><span data-stu-id="6e196-120">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="6e196-121">说明</span><span class="sxs-lookup"><span data-stu-id="6e196-121">Description</span></span> | <span data-ttu-id="6e196-122">找零</span><span class="sxs-lookup"><span data-stu-id="6e196-122">Change</span></span> |
| --- | --- |
| <span data-ttu-id="6e196-123">**工作/职位** 实体更改</span><span class="sxs-lookup"><span data-stu-id="6e196-123">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="6e196-124">添加了 **薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="6e196-124">**Compensation region** added</span></span></li>|
| <span data-ttu-id="6e196-125">添加了 **工作职位维度** 实体</span><span class="sxs-lookup"><span data-stu-id="6e196-125">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="6e196-126">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="6e196-126">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="6e196-127">**工作人员** 实体更改</span><span class="sxs-lookup"><span data-stu-id="6e196-127">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="6e196-128">添加了 **姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="6e196-128">**Name sequence** added</span></span></li><li><span data-ttu-id="6e196-129">添加了 **在家工作**</span><span class="sxs-lookup"><span data-stu-id="6e196-129">**Works from home** added</span></span></li><li><span data-ttu-id="6e196-130">添加了 **语言**</span><span class="sxs-lookup"><span data-stu-id="6e196-130">**Language** added</span></span></li><li><span data-ttu-id="6e196-131">添加了 **受聘日期**</span><span class="sxs-lookup"><span data-stu-id="6e196-131">**Seniority date** added</span></span></li><li><span data-ttu-id="6e196-132">添加了 **周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="6e196-132">**Anniversary date** added</span></span></li><li><span data-ttu-id="6e196-133">添加了 **原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="6e196-133">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="6e196-134">**雇用** 实体更改</span><span class="sxs-lookup"><span data-stu-id="6e196-134">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="6e196-135">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="6e196-135">**Financial dimensions** added</span></span></li><li><span data-ttu-id="6e196-136">添加了 **离职原因**</span><span class="sxs-lookup"><span data-stu-id="6e196-136">**Termination reason** added</span></span></li><li><span data-ttu-id="6e196-137">**转变日期** 重命名为 **离职日期**</span><span class="sxs-lookup"><span data-stu-id="6e196-137">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="6e196-138">添加了 **试用日期**</span><span class="sxs-lookup"><span data-stu-id="6e196-138">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="6e196-139">**工作人员地址** 实体更改</span><span class="sxs-lookup"><span data-stu-id="6e196-139">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="6e196-140">添加了 **街道地址**</span><span class="sxs-lookup"><span data-stu-id="6e196-140">**Street address** added</span></span></li><li><span data-ttu-id="6e196-141">**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="6e196-141">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="6e196-142">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="6e196-142">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="6e196-143">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="6e196-143">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="6e196-144">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="6e196-144">**Compensation variable plan**</span></span></li><li><span data-ttu-id="6e196-145">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="6e196-145">**Vesting rules**</span></span></li><li><span data-ttu-id="6e196-146">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="6e196-146">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="6e196-147">新 **工作人员日历雇用** 实体</span><span class="sxs-lookup"><span data-stu-id="6e196-147">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="6e196-148">添加了 **工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="6e196-148">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="6e196-149">新 **工资单职位详细信息** 实体</span><span class="sxs-lookup"><span data-stu-id="6e196-149">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="6e196-150">添加了 **工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="6e196-150">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="6e196-151">新 **职务** 实体</span><span class="sxs-lookup"><span data-stu-id="6e196-151">New **Title** entity</span></span> | <ul><li><span data-ttu-id="6e196-152">添加了 **职务**</span><span class="sxs-lookup"><span data-stu-id="6e196-152">**Title** added</span></span></li></ul> <span data-ttu-id="6e196-153">新的 **职务** 实体位于 Dataverse 中，但是此时不是从 **工作职位** 或 **工作** 实体引用的。</span><span class="sxs-lookup"><span data-stu-id="6e196-153">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="6e196-154">职位和雇用的财务维度为从 Human Resources 到 Dataverse 的更新提供单向集成。</span><span class="sxs-lookup"><span data-stu-id="6e196-154">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="6e196-155">财务维度更新现在不从 Dataverse 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="6e196-155">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="6e196-156">在接下来的数周内，所有环境中将支持这些实体更改。</span><span class="sxs-lookup"><span data-stu-id="6e196-156">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="6e196-157">若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：</span><span class="sxs-lookup"><span data-stu-id="6e196-157">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="6e196-158">转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="6e196-158">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="6e196-159">选择 **环境**。</span><span class="sxs-lookup"><span data-stu-id="6e196-159">Select **Environments**.</span></span>

3.  <span data-ttu-id="6e196-160">找到要升级的环境。</span><span class="sxs-lookup"><span data-stu-id="6e196-160">Find the environment you want to upgrade.</span></span> <span data-ttu-id="6e196-161">此环境应该对应于 Human Resources 中 **关于** 窗体内 **Dataverse 信息** 部分中的 **环境名称**。</span><span class="sxs-lookup"><span data-stu-id="6e196-161">The environment should correspond to **Environment name** in the **Dataverse information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="6e196-162">选择环境以查看环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="6e196-162">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="6e196-163">在顶部的操作栏中选择 **管理解决方案**。</span><span class="sxs-lookup"><span data-stu-id="6e196-163">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="6e196-164">将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="6e196-164">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="6e196-165">在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。</span><span class="sxs-lookup"><span data-stu-id="6e196-165">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="6e196-166">选择 **升级** 应用最新解决方案。</span><span class="sxs-lookup"><span data-stu-id="6e196-166">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="6e196-167">预览模式</span><span class="sxs-lookup"><span data-stu-id="6e196-167">In preview</span></span>

<span data-ttu-id="6e196-168">以下预览功能于 2020 年 2 月 3 日可用：</span><span class="sxs-lookup"><span data-stu-id="6e196-168">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="6e196-169">**休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="6e196-169">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="6e196-170">**福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6e196-170">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6e196-171">即将推出</span><span class="sxs-lookup"><span data-stu-id="6e196-171">Coming Soon</span></span>

### <a name="platform-update-33"></a><span data-ttu-id="6e196-172">平台 update 33</span><span class="sxs-lookup"><span data-stu-id="6e196-172">Platform update 33</span></span>

- <span data-ttu-id="6e196-173">整页应用（预览）- 此预览功能需要您启用“已保存的视图”功能，其允许将 Power Apps 和第三方应用通过仪表板作为整页体验添加。</span><span class="sxs-lookup"><span data-stu-id="6e196-173">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="6e196-174">已保存的视图（预览）- 此预览功能启用已保存的视图，这是对个性化子系统的显著增强。</span><span class="sxs-lookup"><span data-stu-id="6e196-174">Saved views (Preview) - This preview feature enables saved views, which is a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="6e196-175">此功能让用户每页可以有多组命名的个性化设置。</span><span class="sxs-lookup"><span data-stu-id="6e196-175">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="6e196-176">也可以将视图发布给安全角色。</span><span class="sxs-lookup"><span data-stu-id="6e196-176">You can also publish views to security roles.</span></span>

- <span data-ttu-id="6e196-177">经过优化的“之一”筛选体验 - 此功能启用了优化的“之一”筛选体验，可以更轻松地输入多个筛选器值，提供更简单的机制来删除单个或所有筛选器值，并可更紧凑直观地以可视化方式呈现筛选器值。</span><span class="sxs-lookup"><span data-stu-id="6e196-177">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="6e196-178">“推荐”字段 - 用户通常需要向网格或页面添加字段。</span><span class="sxs-lookup"><span data-stu-id="6e196-178">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="6e196-179">因为可用字段太多，这可能很难。</span><span class="sxs-lookup"><span data-stu-id="6e196-179">This can be difficult with so many available fields.</span></span> <span data-ttu-id="6e196-180">此功能让系统基于其他用户在类似方案中最常添加的字段显示一组推荐字段，而不必在大型列表中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="6e196-180">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="6e196-181">网格中的粘滞默认操作 - 此功能确保网格中的默认操作链接到网格中的特定列，而不管是否移动或隐藏了该列。</span><span class="sxs-lookup"><span data-stu-id="6e196-181">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e196-182">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e196-182">See also</span></span>

[<span data-ttu-id="6e196-183">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="6e196-183">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="6e196-184">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="6e196-184">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="6e196-185">更新流程</span><span class="sxs-lookup"><span data-stu-id="6e196-185">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="6e196-186">管理功能</span><span class="sxs-lookup"><span data-stu-id="6e196-186">Manage features</span></span>](hr-admin-manage-features.md)