---
title: Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改
description: 本文介绍 2020 年 2 月 25 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5048c94543d0ee35bbc0f210a86a5d58ae901510
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463758"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="90d9b-103">Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="90d9b-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="90d9b-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="90d9b-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="90d9b-105">更改适用于内部版本号 8.1.2927。</span><span class="sxs-lookup"><span data-stu-id="90d9b-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="90d9b-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="90d9b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="90d9b-107">启用案例管理导航和数据管理框架 (DMF) 实体 (414754)</span><span class="sxs-lookup"><span data-stu-id="90d9b-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="90d9b-108">此预览功能为案例管理情况增加了导航方式。</span><span class="sxs-lookup"><span data-stu-id="90d9b-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="90d9b-109">可以在 **功能管理** 工作区中启用此预览功能。</span><span class="sxs-lookup"><span data-stu-id="90d9b-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="90d9b-110">这些菜单项在 Dynamics 365 Human Resources 的 **合规性** 工作区中显示。</span><span class="sxs-lookup"><span data-stu-id="90d9b-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="90d9b-111">通过此更改，Human Resources 可以访问：</span><span class="sxs-lookup"><span data-stu-id="90d9b-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="90d9b-112">所有案例</span><span class="sxs-lookup"><span data-stu-id="90d9b-112">All cases</span></span>
- <span data-ttu-id="90d9b-113">我的案例</span><span class="sxs-lookup"><span data-stu-id="90d9b-113">My cases</span></span>
- <span data-ttu-id="90d9b-114">我的未结案例</span><span class="sxs-lookup"><span data-stu-id="90d9b-114">My open cases</span></span>
- <span data-ttu-id="90d9b-115">我的逾期案例</span><span class="sxs-lookup"><span data-stu-id="90d9b-115">My overdue cases</span></span>
- <span data-ttu-id="90d9b-116">通过工作流分配给我的案例</span><span class="sxs-lookup"><span data-stu-id="90d9b-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="90d9b-117">除了案例的这些新视图，还提供了 **案例详细信息** DMF 实体。</span><span class="sxs-lookup"><span data-stu-id="90d9b-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="90d9b-118">在全球通讯簿中启用关系定义 (414762)</span><span class="sxs-lookup"><span data-stu-id="90d9b-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="90d9b-119">全球通讯簿中现在已启用关系。</span><span class="sxs-lookup"><span data-stu-id="90d9b-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="90d9b-120">本周的发布之前，**关系** 速见表显示系统定义的所有关系。</span><span class="sxs-lookup"><span data-stu-id="90d9b-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="90d9b-121">现在您可以在全球通讯簿页面内定义这些关系。</span><span class="sxs-lookup"><span data-stu-id="90d9b-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="90d9b-122">职位有活动的薪酬记录时可以删除职位 (414568)</span><span class="sxs-lookup"><span data-stu-id="90d9b-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="90d9b-123">通过此更改，当您尝试删除职位，而一位工作人员有同一个职位的活动薪酬记录时，将显示警告。</span><span class="sxs-lookup"><span data-stu-id="90d9b-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="90d9b-124">如果发生此情况，必须先更新员工的固定薪酬记录，才能删除该职位。</span><span class="sxs-lookup"><span data-stu-id="90d9b-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="90d9b-125">绩效审核工作流有时会添加不属于该流程的人员的签核 (414171)</span><span class="sxs-lookup"><span data-stu-id="90d9b-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="90d9b-126">此更改解决了向绩效审核添加更多签核参与者这一问题。</span><span class="sxs-lookup"><span data-stu-id="90d9b-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="90d9b-127">在“新建工作人员”对话框中选择后不在 Dataverse 中创建工作人员职位分配 (413479)</span><span class="sxs-lookup"><span data-stu-id="90d9b-127">Worker position assignment not created in Dataverse when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="90d9b-128">此更改解决了通过 **新建工作人员** 对话框雇用新工作人员并为新雇用分配职位时的问题。</span><span class="sxs-lookup"><span data-stu-id="90d9b-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="90d9b-129">现在 Dataverse 中将体现此项职位分配。</span><span class="sxs-lookup"><span data-stu-id="90d9b-129">Now the position assignment is reflected in Dataverse.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="90d9b-130">即将到期</span><span class="sxs-lookup"><span data-stu-id="90d9b-130">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="90d9b-131">更新的 Dataverse 解决方案</span><span class="sxs-lookup"><span data-stu-id="90d9b-131">Updated Dataverse solution</span></span>

<span data-ttu-id="90d9b-132">一个新的 Dataverse 解决方案很快将推出，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="90d9b-132">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="90d9b-133">说明</span><span class="sxs-lookup"><span data-stu-id="90d9b-133">Description</span></span> | <span data-ttu-id="90d9b-134">找零</span><span class="sxs-lookup"><span data-stu-id="90d9b-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="90d9b-135">**工作/职位** 实体更改</span><span class="sxs-lookup"><span data-stu-id="90d9b-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="90d9b-136">添加了 **薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="90d9b-136">**Compensation region** added</span></span></br><span data-ttu-id="90d9b-137">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="90d9b-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="90d9b-138">**工作人员** 实体更改</span><span class="sxs-lookup"><span data-stu-id="90d9b-138">**Worker** entity changes</span></span> | <span data-ttu-id="90d9b-139">添加了 **姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="90d9b-139">**Name sequence** added</span></span></br><span data-ttu-id="90d9b-140">添加了 **在家工作**</span><span class="sxs-lookup"><span data-stu-id="90d9b-140">**Works from home** added</span></span></br><span data-ttu-id="90d9b-141">添加了 **语言**</span><span class="sxs-lookup"><span data-stu-id="90d9b-141">**Language** added</span></span></br><span data-ttu-id="90d9b-142">添加了 **受聘日期**</span><span class="sxs-lookup"><span data-stu-id="90d9b-142">**Seniority date** added</span></span></br><span data-ttu-id="90d9b-143">添加了 **周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="90d9b-143">**Anniversary date** added</span></span></br><span data-ttu-id="90d9b-144">添加了 **原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="90d9b-144">**Original hire date** added</span></span> |
| <span data-ttu-id="90d9b-145">**雇用** 实体更改</span><span class="sxs-lookup"><span data-stu-id="90d9b-145">**Employment** entity changes</span></span> | <span data-ttu-id="90d9b-146">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="90d9b-146">**Financial dimensions** added</span></span></br><span data-ttu-id="90d9b-147">添加了 **离职原因**</span><span class="sxs-lookup"><span data-stu-id="90d9b-147">**Termination reason** added</span></span></br><span data-ttu-id="90d9b-148">**转变日期** 重命名为 **离职日期**</span><span class="sxs-lookup"><span data-stu-id="90d9b-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="90d9b-149">添加了 **试用日期**</span><span class="sxs-lookup"><span data-stu-id="90d9b-149">**Probation date** added</span></span> |
| <span data-ttu-id="90d9b-150">**工作人员地址** 实体更改</span><span class="sxs-lookup"><span data-stu-id="90d9b-150">**Worker address** entity changes</span></span> | <span data-ttu-id="90d9b-151">添加了 **街道地址**</span><span class="sxs-lookup"><span data-stu-id="90d9b-151">**Street address** added</span></span></br><span data-ttu-id="90d9b-152">**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="90d9b-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="90d9b-153">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="90d9b-153">New variable compensation setup entities</span></span> | <span data-ttu-id="90d9b-154">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="90d9b-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="90d9b-155">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="90d9b-155">**Compensation variable plan**</span></span></br><span data-ttu-id="90d9b-156">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="90d9b-156">**Vesting rules**</span></span></br><span data-ttu-id="90d9b-157">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="90d9b-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="90d9b-158">新 **工作人员日历雇用** 实体</span><span class="sxs-lookup"><span data-stu-id="90d9b-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="90d9b-159">添加了 **工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="90d9b-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="90d9b-160">新 **工资单职位详细信息** 实体</span><span class="sxs-lookup"><span data-stu-id="90d9b-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="90d9b-161">添加了 **工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="90d9b-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="90d9b-162">新 **职务** 实体</span><span class="sxs-lookup"><span data-stu-id="90d9b-162">New **Title** entity</span></span> | <span data-ttu-id="90d9b-163">添加了 **职务**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-163">**Title** added.</span></span> <span data-ttu-id="90d9b-164">Human Resources 与 Dataverse 之间的同步流程中将包含新的 **职务** 实体。</span><span class="sxs-lookup"><span data-stu-id="90d9b-164">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="90d9b-165">其最初不是从 **工作职位** 或 **工作** 实体引用的。</span><span class="sxs-lookup"><span data-stu-id="90d9b-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="90d9b-166">在接下来的数周内，所有环境中将支持这些实体更改。</span><span class="sxs-lookup"><span data-stu-id="90d9b-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="90d9b-167">若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：</span><span class="sxs-lookup"><span data-stu-id="90d9b-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="90d9b-168">转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="90d9b-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="90d9b-169">选择 **环境**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="90d9b-170">找到要升级的环境。</span><span class="sxs-lookup"><span data-stu-id="90d9b-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="90d9b-171">这应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="90d9b-172">选择环境以查看环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="90d9b-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="90d9b-173">在顶部的操作栏中选择 **管理解决方案**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="90d9b-174">将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="90d9b-175">在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。</span><span class="sxs-lookup"><span data-stu-id="90d9b-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="90d9b-176">选择 **升级** 应用最新解决方案。</span><span class="sxs-lookup"><span data-stu-id="90d9b-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="90d9b-177">预览模式</span><span class="sxs-lookup"><span data-stu-id="90d9b-177">In preview</span></span>

<span data-ttu-id="90d9b-178">以下预览功能已于 2020 年 2 月 3 日可用：</span><span class="sxs-lookup"><span data-stu-id="90d9b-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="90d9b-179">**休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="90d9b-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="90d9b-180">**福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="90d9b-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="90d9b-181">请参阅</span><span class="sxs-lookup"><span data-stu-id="90d9b-181">See also</span></span>

[<span data-ttu-id="90d9b-182">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="90d9b-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="90d9b-183">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="90d9b-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="90d9b-184">更新流程</span><span class="sxs-lookup"><span data-stu-id="90d9b-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="90d9b-185">管理功能</span><span class="sxs-lookup"><span data-stu-id="90d9b-185">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]