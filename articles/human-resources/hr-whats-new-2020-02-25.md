---
title: Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
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
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092744"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="7a4a3-103">Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="7a4a3-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="7a4a3-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7a4a3-105">更改适用于内部版本号 8.1.2927。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="7a4a3-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="7a4a3-107">启用案例管理导航和数据管理框架 (DMF) 实体 (414754)</span><span class="sxs-lookup"><span data-stu-id="7a4a3-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="7a4a3-108">此预览功能为案例管理情况增加了导航方式。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="7a4a3-109">可以在**功能管理**工作区中启用此预览功能。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="7a4a3-110">这些菜单项在 Dynamics 365 Human Resources 的**合规性**工作区中显示。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7a4a3-111">通过此更改，Human Resources 可以访问：</span><span class="sxs-lookup"><span data-stu-id="7a4a3-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="7a4a3-112">所有案例</span><span class="sxs-lookup"><span data-stu-id="7a4a3-112">All cases</span></span>
- <span data-ttu-id="7a4a3-113">我的案例</span><span class="sxs-lookup"><span data-stu-id="7a4a3-113">My cases</span></span>
- <span data-ttu-id="7a4a3-114">我的未结案例</span><span class="sxs-lookup"><span data-stu-id="7a4a3-114">My open cases</span></span>
- <span data-ttu-id="7a4a3-115">我的逾期案例</span><span class="sxs-lookup"><span data-stu-id="7a4a3-115">My overdue cases</span></span>
- <span data-ttu-id="7a4a3-116">通过工作流分配给我的案例</span><span class="sxs-lookup"><span data-stu-id="7a4a3-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="7a4a3-117">除了案例的这些新视图，还提供了**案例详细信息** DMF 实体。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="7a4a3-118">在全球通讯簿中启用关系定义 (414762)</span><span class="sxs-lookup"><span data-stu-id="7a4a3-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="7a4a3-119">全球通讯簿中现在已启用关系。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="7a4a3-120">本周的发布之前，**关系**速见表显示系统定义的所有关系。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="7a4a3-121">现在您可以在全球通讯簿页面内定义这些关系。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="7a4a3-122">职位有活动的薪酬记录时可以删除职位 (414568)</span><span class="sxs-lookup"><span data-stu-id="7a4a3-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="7a4a3-123">通过此更改，当您尝试删除职位，而一位工作人员有同一个职位的活动薪酬记录时，将显示警告。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="7a4a3-124">如果发生此情况，必须先更新员工的固定薪酬记录，才能删除该职位。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="7a4a3-125">绩效审核工作流有时会添加不属于该流程的人员的签核 (414171)</span><span class="sxs-lookup"><span data-stu-id="7a4a3-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="7a4a3-126">此更改解决了向绩效审核添加更多签核参与者这一问题。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="7a4a3-127">在“新建工作人员”对话框中选择后不在 Common Data Service 中创建工作人员职位分配 (413479)</span><span class="sxs-lookup"><span data-stu-id="7a4a3-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="7a4a3-128">此更改解决了通过**新建工作人员**对话框雇用新工作人员并为新雇用分配职位时的问题。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="7a4a3-129">现在 Common Data Service 中将体现此项职位分配。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="7a4a3-130">即将到期</span><span class="sxs-lookup"><span data-stu-id="7a4a3-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="7a4a3-131">更新的 Common Data Service 解决方案</span><span class="sxs-lookup"><span data-stu-id="7a4a3-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="7a4a3-132">一个新的 Common Data Service 解决方案很快将推出，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="7a4a3-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="7a4a3-133">说明</span><span class="sxs-lookup"><span data-stu-id="7a4a3-133">Description</span></span> | <span data-ttu-id="7a4a3-134">找零</span><span class="sxs-lookup"><span data-stu-id="7a4a3-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="7a4a3-135">**工作/职位**实体更改</span><span class="sxs-lookup"><span data-stu-id="7a4a3-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="7a4a3-136">添加了**薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-136">**Compensation region** added</span></span></br><span data-ttu-id="7a4a3-137">添加了**财务维度**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="7a4a3-138">**工作人员**实体更改</span><span class="sxs-lookup"><span data-stu-id="7a4a3-138">**Worker** entity changes</span></span> | <span data-ttu-id="7a4a3-139">添加了**姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-139">**Name sequence** added</span></span></br><span data-ttu-id="7a4a3-140">添加了**在家工作**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-140">**Works from home** added</span></span></br><span data-ttu-id="7a4a3-141">添加了**语言**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-141">**Language** added</span></span></br><span data-ttu-id="7a4a3-142">添加了**受聘日期**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-142">**Seniority date** added</span></span></br><span data-ttu-id="7a4a3-143">添加了**周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-143">**Anniversary date** added</span></span></br><span data-ttu-id="7a4a3-144">添加了**原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-144">**Original hire date** added</span></span> |
| <span data-ttu-id="7a4a3-145">**雇用**实体更改</span><span class="sxs-lookup"><span data-stu-id="7a4a3-145">**Employment** entity changes</span></span> | <span data-ttu-id="7a4a3-146">添加了**财务维度**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-146">**Financial dimensions** added</span></span></br><span data-ttu-id="7a4a3-147">添加了**离职原因**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-147">**Termination reason** added</span></span></br><span data-ttu-id="7a4a3-148">**转变日期**重命名为**离职日期**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="7a4a3-149">添加了**试用日期**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-149">**Probation date** added</span></span> |
| <span data-ttu-id="7a4a3-150">**工作人员地址**实体更改</span><span class="sxs-lookup"><span data-stu-id="7a4a3-150">**Worker address** entity changes</span></span> | <span data-ttu-id="7a4a3-151">添加了**街道地址**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-151">**Street address** added</span></span></br><span data-ttu-id="7a4a3-152">**地址行 1**、**地址行 2** 和**地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="7a4a3-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="7a4a3-153">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="7a4a3-153">New variable compensation setup entities</span></span> | <span data-ttu-id="7a4a3-154">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="7a4a3-155">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-155">**Compensation variable plan**</span></span></br><span data-ttu-id="7a4a3-156">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-156">**Vesting rules**</span></span></br><span data-ttu-id="7a4a3-157">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="7a4a3-158">新**工作人员日历雇用**实体</span><span class="sxs-lookup"><span data-stu-id="7a4a3-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="7a4a3-159">添加了**工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="7a4a3-160">新**工资单职位详细信息**实体</span><span class="sxs-lookup"><span data-stu-id="7a4a3-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="7a4a3-161">添加了**工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="7a4a3-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="7a4a3-162">新**职务**实体</span><span class="sxs-lookup"><span data-stu-id="7a4a3-162">New **Title** entity</span></span> | <span data-ttu-id="7a4a3-163">添加了**职务**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-163">**Title** added.</span></span> <span data-ttu-id="7a4a3-164">Human Resources 与 Common Data Service 之间的同步流程中将包含新的**职务**实体。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="7a4a3-165">其最初不是从**工作职位**或**工作**实体引用的。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="7a4a3-166">在接下来的数周内，所有环境中将支持这些实体更改。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="7a4a3-167">若要手动插入适用于 Human Resources 的最新 Common Data Service 解决方案：</span><span class="sxs-lookup"><span data-stu-id="7a4a3-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="7a4a3-168">转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="7a4a3-169">选择**环境**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="7a4a3-170">找到要升级的环境。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="7a4a3-171">这应该对应于 Human Resources 中**关于**窗体内 **Common Data Service 信息**部分中的**环境名称**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="7a4a3-172">选择环境以查看环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="7a4a3-173">在顶部的操作栏中选择**管理解决方案**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="7a4a3-174">将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="7a4a3-175">在**解决方案**列表中，选择 **Dynamics 365 Human Resources 定位点**。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="7a4a3-176">选择**升级**应用最新解决方案。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7a4a3-177">预览模式</span><span class="sxs-lookup"><span data-stu-id="7a4a3-177">In preview</span></span>

<span data-ttu-id="7a4a3-178">以下预览功能已于 2020 年 2 月 3 日可用：</span><span class="sxs-lookup"><span data-stu-id="7a4a3-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="7a4a3-179">**休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="7a4a3-180">**福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="7a4a3-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>
