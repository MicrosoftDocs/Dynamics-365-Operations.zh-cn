---
title: Dynamics 365 Human Resources（2020 年 3 月 24 日）中的新增功能或更改
description: 本文介绍 2020 年 3 月 24 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 03/24/2020
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
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3f9595bd19026e0dad0a2a2ad3708bd4f8ca1ba
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127937"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a><span data-ttu-id="4ae80-103">Dynamics 365 Human Resources（2020 年 3 月 24 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="4ae80-103">What's new or changed in Dynamics 365 Human Resources (March 24, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4ae80-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="4ae80-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4ae80-105">更改适用于内部版本号 8.1.3073。</span><span class="sxs-lookup"><span data-stu-id="4ae80-105">Changes apply to build number 8.1.3073.</span></span> <span data-ttu-id="4ae80-106">某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。</span><span class="sxs-lookup"><span data-stu-id="4ae80-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a><span data-ttu-id="4ae80-107">Human Resources 环境限制现在基于更新的许可 (394595)</span><span class="sxs-lookup"><span data-stu-id="4ae80-107">Human Resources environment limits are now based on updated licensing (394595)</span></span>

<span data-ttu-id="4ae80-108">Lifecycle Services (LCS) 中每个项目的环境数量限制已更改。</span><span class="sxs-lookup"><span data-stu-id="4ae80-108">The limit on the number of environments per project in Lifecycle Services (LCS) has changed.</span></span> <span data-ttu-id="4ae80-109">先前的限制是两个环境。</span><span class="sxs-lookup"><span data-stu-id="4ae80-109">The previous limit was two environments.</span></span> <span data-ttu-id="4ae80-110">现在，您可以在 LCS 中为 Human Resources 创建的生产环境和沙盒环境的数量限制基于更新的许可。</span><span class="sxs-lookup"><span data-stu-id="4ae80-110">The limit on the number of production and sandbox environments you can create for Human Resources in LCS is now based on updated licensing.</span></span> <span data-ttu-id="4ae80-111">现在，您可以根据购买的许可证数量，为每个 LCS 项目创建所需数量的环境。</span><span class="sxs-lookup"><span data-stu-id="4ae80-111">You can now create as many environments as needed per LCS project, depending on the number of licenses purchased.</span></span> <span data-ttu-id="4ae80-112">2020 年 2 月 1 日更新的新许可允许客户购买其他环境。</span><span class="sxs-lookup"><span data-stu-id="4ae80-112">The new licensing, updated on February 1, 2020, allows customers to purchase additional environments.</span></span> <span data-ttu-id="4ae80-113">有关其他环境的许可要求的详细信息，请参阅 [Dynamics 365 许可指南](https://dynamics.microsoft.com/pricing/#HumanResources)。</span><span class="sxs-lookup"><span data-stu-id="4ae80-113">For more information about licensing requirements for additional environments, see [Dynamics 365 Licensing Guide](https://dynamics.microsoft.com/pricing/#HumanResources).</span></span>

## <a name="platform-changes"></a><span data-ttu-id="4ae80-114">平台变更</span><span class="sxs-lookup"><span data-stu-id="4ae80-114">Platform changes</span></span>

- <span data-ttu-id="4ae80-115">整页应用（预览）- 此预览功能需要您启用“已保存的视图”功能，其允许将 Power Apps 和第三方应用通过仪表板作为整页体验添加。</span><span class="sxs-lookup"><span data-stu-id="4ae80-115">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="4ae80-116">已保存的视图（预览）- 此预览功能启用已保存的视图，这将为个性化子系统提供显著的增强。</span><span class="sxs-lookup"><span data-stu-id="4ae80-116">Saved views (Preview) - This preview feature enables saved views, which provide a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="4ae80-117">此功能让用户每页可以有多组命名的个性化设置。</span><span class="sxs-lookup"><span data-stu-id="4ae80-117">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="4ae80-118">也可以将视图发布给安全角色。</span><span class="sxs-lookup"><span data-stu-id="4ae80-118">You can also publish views to security roles.</span></span>

- <span data-ttu-id="4ae80-119">经过优化的“之一”筛选体验 - 此功能启用了优化的“之一”筛选体验，可以更轻松地输入多个筛选器值，提供更简单的机制来删除单个或所有筛选器值，并可更紧凑直观地以可视化方式呈现筛选器值。</span><span class="sxs-lookup"><span data-stu-id="4ae80-119">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="4ae80-120">“推荐”字段 - 用户通常需要向网格或页面添加字段。</span><span class="sxs-lookup"><span data-stu-id="4ae80-120">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="4ae80-121">因为可用字段太多，这可能很难。</span><span class="sxs-lookup"><span data-stu-id="4ae80-121">This can be difficult with so many available fields.</span></span> <span data-ttu-id="4ae80-122">此功能让系统基于其他用户在类似方案中最常添加的字段显示一组推荐字段，而不必在大型列表中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="4ae80-122">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="4ae80-123">网格中的粘滞默认操作 - 此功能确保网格中的默认操作链接到网格中的特定列，而不管是否移动或隐藏了该列。</span><span class="sxs-lookup"><span data-stu-id="4ae80-123">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a><span data-ttu-id="4ae80-124">无法为创建的没有应计但已启用“多个休假类型”功能的计划调整休假余额 (419635)</span><span class="sxs-lookup"><span data-stu-id="4ae80-124">Unable to adjust leave balance for a plan with no accruals that was created with "multiple leave type" feature on (419635)</span></span>

<span data-ttu-id="4ae80-125">通过此更改，您可以为创建的已在功能管理中启用了多个休假类型（预览功能）的休假计划调整余额。</span><span class="sxs-lookup"><span data-stu-id="4ae80-125">With this change, you can adjust balances for leave plans that have been created with the Multiple leave type (Preview) feature enabled in feature management.</span></span>

## <a name="in-preview"></a><span data-ttu-id="4ae80-126">预览模式</span><span class="sxs-lookup"><span data-stu-id="4ae80-126">In preview</span></span>

<span data-ttu-id="4ae80-127">以下预览功能已于 2020 年 2 月 3 日可用：</span><span class="sxs-lookup"><span data-stu-id="4ae80-127">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="4ae80-128">**休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="4ae80-128">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="4ae80-129">**福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4ae80-129">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="4ae80-130">Dataverse 现已可用，并具有以下更改：</span><span class="sxs-lookup"><span data-stu-id="4ae80-130">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="4ae80-131">说明</span><span class="sxs-lookup"><span data-stu-id="4ae80-131">Description</span></span> | <span data-ttu-id="4ae80-132">找零</span><span class="sxs-lookup"><span data-stu-id="4ae80-132">Change</span></span> |
| --- | --- |
| <span data-ttu-id="4ae80-133">**工作/职位** 实体更改</span><span class="sxs-lookup"><span data-stu-id="4ae80-133">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="4ae80-134">添加了 **薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="4ae80-134">**Compensation region** added</span></span></li>|
| <span data-ttu-id="4ae80-135">添加了 **工作职位维度** 实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-135">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="4ae80-136">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="4ae80-136">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="4ae80-137">**工作人员** 实体更改</span><span class="sxs-lookup"><span data-stu-id="4ae80-137">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="4ae80-138">添加了 **姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="4ae80-138">**Name sequence** added</span></span></li><li><span data-ttu-id="4ae80-139">添加了 **在家工作**</span><span class="sxs-lookup"><span data-stu-id="4ae80-139">**Works from home** added</span></span></li><li><span data-ttu-id="4ae80-140">添加了 **语言**</span><span class="sxs-lookup"><span data-stu-id="4ae80-140">**Language** added</span></span></li><li><span data-ttu-id="4ae80-141">添加了 **受聘日期**</span><span class="sxs-lookup"><span data-stu-id="4ae80-141">**Seniority date** added</span></span></li><li><span data-ttu-id="4ae80-142">添加了 **周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="4ae80-142">**Anniversary date** added</span></span></li><li><span data-ttu-id="4ae80-143">添加了 **原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="4ae80-143">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="4ae80-144">**雇用** 实体更改</span><span class="sxs-lookup"><span data-stu-id="4ae80-144">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="4ae80-145">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="4ae80-145">**Financial dimensions** added</span></span></li><li><span data-ttu-id="4ae80-146">添加了 **离职原因**</span><span class="sxs-lookup"><span data-stu-id="4ae80-146">**Termination reason** added</span></span></li><li><span data-ttu-id="4ae80-147">**转变日期** 重命名为 **离职日期**</span><span class="sxs-lookup"><span data-stu-id="4ae80-147">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="4ae80-148">添加了 **试用日期**</span><span class="sxs-lookup"><span data-stu-id="4ae80-148">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="4ae80-149">**工作人员地址** 实体更改</span><span class="sxs-lookup"><span data-stu-id="4ae80-149">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="4ae80-150">添加了 **街道地址**</span><span class="sxs-lookup"><span data-stu-id="4ae80-150">**Street address** added</span></span></li><li><span data-ttu-id="4ae80-151">**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="4ae80-151">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="4ae80-152">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-152">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="4ae80-153">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="4ae80-153">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="4ae80-154">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="4ae80-154">**Compensation variable plan**</span></span></li><li><span data-ttu-id="4ae80-155">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="4ae80-155">**Vesting rules**</span></span></li><li><span data-ttu-id="4ae80-156">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="4ae80-156">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="4ae80-157">新 **工作人员日历雇用** 实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-157">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="4ae80-158">添加了 **工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="4ae80-158">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="4ae80-159">新 **工资单职位详细信息** 实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-159">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="4ae80-160">添加了 **工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="4ae80-160">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="4ae80-161">新 **职务** 实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-161">New **Title** entity</span></span> | <ul><li><span data-ttu-id="4ae80-162">添加了 **职务**</span><span class="sxs-lookup"><span data-stu-id="4ae80-162">**Title** added</span></span></li></ul><span data-ttu-id="4ae80-163">新的 **职务** 实体位于 Dataverse 中，但是此时不是从 **工作职位** 或 **工作** 实体引用的。</span><span class="sxs-lookup"><span data-stu-id="4ae80-163">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="4ae80-164">职位和雇用的财务维度为从 Human Resources 到 Dataverse 的更新提供单向集成。</span><span class="sxs-lookup"><span data-stu-id="4ae80-164">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="4ae80-165">财务维度更新现在不从 Dataverse 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="4ae80-165">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="4ae80-166">在接下来的数周内，所有环境中将支持这些实体更改。</span><span class="sxs-lookup"><span data-stu-id="4ae80-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="4ae80-167">若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：</span><span class="sxs-lookup"><span data-stu-id="4ae80-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="4ae80-168">转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="4ae80-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="4ae80-169">选择 **环境**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="4ae80-170">找到要升级的环境。</span><span class="sxs-lookup"><span data-stu-id="4ae80-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="4ae80-171">此环境应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-171">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="4ae80-172">选择环境以查看环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="4ae80-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="4ae80-173">在顶部的操作栏中选择 **管理解决方案**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="4ae80-174">将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="4ae80-175">在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="4ae80-176">选择 **升级** 应用最新解决方案。</span><span class="sxs-lookup"><span data-stu-id="4ae80-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="4ae80-177">SharePoint 预览在某些环境下不起作用</span><span class="sxs-lookup"><span data-stu-id="4ae80-177">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="4ae80-178">如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：</span><span class="sxs-lookup"><span data-stu-id="4ae80-178">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="4ae80-179">验证管理员用户帐户是否具有与用户记录关联的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4ae80-179">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="4ae80-180">可在 **用户** 页面查看这些信息。</span><span class="sxs-lookup"><span data-stu-id="4ae80-180">You can view this information in the **User** page.</span></span> <span data-ttu-id="4ae80-181">如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。</span><span class="sxs-lookup"><span data-stu-id="4ae80-181">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="4ae80-182">默认情况下，Excel 设计中不显示电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="4ae80-182">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="4ae80-183">您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。</span><span class="sxs-lookup"><span data-stu-id="4ae80-183">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="4ae80-184">完成这些步骤后，您可以更新管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="4ae80-184">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="4ae80-185">管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="4ae80-185">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="4ae80-186">访问 SharePoint 中的附件启动文档预览。</span><span class="sxs-lookup"><span data-stu-id="4ae80-186">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="4ae80-187">使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="4ae80-187">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="4ae80-188">即将推出</span><span class="sxs-lookup"><span data-stu-id="4ae80-188">Coming Soon</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="4ae80-189">新产品发布频率</span><span class="sxs-lookup"><span data-stu-id="4ae80-189">New production release cadence</span></span>

<span data-ttu-id="4ae80-190">从 4 月开始，Human Resources 的发布频率将从每周更新变为每两周更新。</span><span class="sxs-lookup"><span data-stu-id="4ae80-190">Beginning in April, the release cadence for Human Resources will shift from a weekly update to a bi-weekly update.</span></span> <span data-ttu-id="4ae80-191">为了确保符合安全部署实践，并在服务中保持高标准的稳定性和可靠性，将为期两周把服务更新部署到所有区域。</span><span class="sxs-lookup"><span data-stu-id="4ae80-191">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions will be a two-week rollout.</span></span> <span data-ttu-id="4ae80-192">将部署更多测试和监视人员，以验证流程各个阶段是否成功部署。</span><span class="sxs-lookup"><span data-stu-id="4ae80-192">Additional testing and monitors will be in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="4ae80-193">有关发布频率的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。</span><span class="sxs-lookup"><span data-stu-id="4ae80-193">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="4ae80-194">已知问题</span><span class="sxs-lookup"><span data-stu-id="4ae80-194">Known issues</span></span>

## <a name="employment-detail-entity"></a><span data-ttu-id="4ae80-195">雇用详细信息实体</span><span class="sxs-lookup"><span data-stu-id="4ae80-195">Employment Detail entity</span></span>

<span data-ttu-id="4ae80-196">已经更新了 **雇用详细信息** 实体的以下字段：**付款频率**、**雇用类别 ID**、**雇用类型**、**雇用类型ID** 和 **福利雇用状态**。</span><span class="sxs-lookup"><span data-stu-id="4ae80-196">The **Employment Detail** entity has been updated with the following fields: **PayFrequency**, **Employment Category ID**, **Employment Type**, **EmploymentType ID**, and **Benefit Employment Status**.</span></span> <span data-ttu-id="4ae80-197">这些字段的设置数据依赖于功能管理中启用的福利管理。</span><span class="sxs-lookup"><span data-stu-id="4ae80-197">The setup data for these fields rely on benefits management being enabled in Feature management.</span></span> <span data-ttu-id="4ae80-198">不应在 **雇用详细信息** 实体中填充或更新这些字段，因为将导致导入期间出错。</span><span class="sxs-lookup"><span data-stu-id="4ae80-198">These fields shouldn't be populated or updated in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ae80-199">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ae80-199">See also</span></span>

[<span data-ttu-id="4ae80-200">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="4ae80-200">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="4ae80-201">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="4ae80-201">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="4ae80-202">更新流程</span><span class="sxs-lookup"><span data-stu-id="4ae80-202">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="4ae80-203">管理功能</span><span class="sxs-lookup"><span data-stu-id="4ae80-203">Manage features</span></span>](hr-admin-manage-features.md)