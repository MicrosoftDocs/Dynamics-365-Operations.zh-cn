---
title: Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077453"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="600dc-103">Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="600dc-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="600dc-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="600dc-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="600dc-105">更改适用于内部版本号 8.1.2903。</span><span class="sxs-lookup"><span data-stu-id="600dc-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="600dc-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="600dc-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="600dc-107">平台 update 32</span><span class="sxs-lookup"><span data-stu-id="600dc-107">Platform update 32</span></span> 

<span data-ttu-id="600dc-108">现已推出了平台更新 32。</span><span class="sxs-lookup"><span data-stu-id="600dc-108">Platform update 32 is now available.</span></span> <span data-ttu-id="600dc-109">有关详细信息，请参阅 [Finance and Operations 应用的平台更新 32（2020 年 2 月）的新增功能或更改的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。</span><span class="sxs-lookup"><span data-stu-id="600dc-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="600dc-110">更改简化的员工窗体中的查看选项时记忆搜索值 (383833)</span><span class="sxs-lookup"><span data-stu-id="600dc-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="600dc-111">现在更改查看选项和应用更改时，新的**工作人员**窗体将记忆搜索值。</span><span class="sxs-lookup"><span data-stu-id="600dc-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="600dc-112">预览功能中的薪酬管理摘要磁贴重定向到错误的窗体 (401861)</span><span class="sxs-lookup"><span data-stu-id="600dc-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="600dc-113">固定和可变薪酬管理磁贴现在在新的**工作人员**窗体中显示正确的记录。</span><span class="sxs-lookup"><span data-stu-id="600dc-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="600dc-114">仅适用于简化的员工窗体预览功能。</span><span class="sxs-lookup"><span data-stu-id="600dc-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="600dc-115">可以在**功能管理**中启用此预览功能。</span><span class="sxs-lookup"><span data-stu-id="600dc-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="600dc-116">有关更多信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="600dc-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="600dc-117">Common Data Service 中某些请假记录的“状态”字段为空 (414915)</span><span class="sxs-lookup"><span data-stu-id="600dc-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="600dc-118">此更改更正了 Common Data Service中当请假的**状态**字段设置为**审查** 时的问题。</span><span class="sxs-lookup"><span data-stu-id="600dc-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="600dc-119">Common Data Service 现在可以体现此状态。</span><span class="sxs-lookup"><span data-stu-id="600dc-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="600dc-120">只能跳过所分配作业的差距分析 (411390)</span><span class="sxs-lookup"><span data-stu-id="600dc-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="600dc-121">现在可以对 Human Resources 中定义的任何作业执行技能差距分析。</span><span class="sxs-lookup"><span data-stu-id="600dc-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="600dc-122">在新环境中，系统币种不能从 Common Data Service 同步到 Human Resources (418011)</span><span class="sxs-lookup"><span data-stu-id="600dc-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="600dc-123">Common Data Service 中的系统币种现在可以同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="600dc-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="600dc-124">预览模式</span><span class="sxs-lookup"><span data-stu-id="600dc-124">In preview</span></span>

- [<span data-ttu-id="600dc-125">休假和缺勤预览功能</span><span class="sxs-lookup"><span data-stu-id="600dc-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="600dc-126">福利管理预览功能</span><span class="sxs-lookup"><span data-stu-id="600dc-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="600dc-127">即将推出</span><span class="sxs-lookup"><span data-stu-id="600dc-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="600dc-128">更新的 Common Data Service 解决方案</span><span class="sxs-lookup"><span data-stu-id="600dc-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="600dc-129">一个新的 Common Data Service 解决方案很快将推出，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="600dc-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="600dc-130">说明</span><span class="sxs-lookup"><span data-stu-id="600dc-130">Description</span></span> | <span data-ttu-id="600dc-131">找零</span><span class="sxs-lookup"><span data-stu-id="600dc-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="600dc-132">**工作/职位**实体更改</span><span class="sxs-lookup"><span data-stu-id="600dc-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="600dc-133">添加了**薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="600dc-133">**Compensation region** added</span></span></br><span data-ttu-id="600dc-134">添加了**财务维度**</span><span class="sxs-lookup"><span data-stu-id="600dc-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="600dc-135">**工作人员**实体更改</span><span class="sxs-lookup"><span data-stu-id="600dc-135">**Worker** entity changes</span></span> | <span data-ttu-id="600dc-136">添加了**姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="600dc-136">**Name sequence** added</span></span></br><span data-ttu-id="600dc-137">添加了**在家工作**</span><span class="sxs-lookup"><span data-stu-id="600dc-137">**Works from home** added</span></span></br><span data-ttu-id="600dc-138">添加了**语言**</span><span class="sxs-lookup"><span data-stu-id="600dc-138">**Language** added</span></span></br><span data-ttu-id="600dc-139">添加了**受聘日期**</span><span class="sxs-lookup"><span data-stu-id="600dc-139">**Seniority date** added</span></span></br><span data-ttu-id="600dc-140">添加了**周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="600dc-140">**Anniversary date** added</span></span></br><span data-ttu-id="600dc-141">添加了**原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="600dc-141">**Original hire date** added</span></span> |
| <span data-ttu-id="600dc-142">**雇用**实体更改</span><span class="sxs-lookup"><span data-stu-id="600dc-142">**Employment** entity changes</span></span> | <span data-ttu-id="600dc-143">添加了**财务维度**</span><span class="sxs-lookup"><span data-stu-id="600dc-143">**Financial dimensions** added</span></span></br><span data-ttu-id="600dc-144">添加了**离职原因**</span><span class="sxs-lookup"><span data-stu-id="600dc-144">**Termination reason** added</span></span></br><span data-ttu-id="600dc-145">**转变日期**重命名为**离职日期**</span><span class="sxs-lookup"><span data-stu-id="600dc-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="600dc-146">添加了**试用日期**</span><span class="sxs-lookup"><span data-stu-id="600dc-146">**Probation date** added</span></span> |
| <span data-ttu-id="600dc-147">**工作人员地址**实体更改</span><span class="sxs-lookup"><span data-stu-id="600dc-147">**Worker address** entity changes</span></span> | <span data-ttu-id="600dc-148">添加了**街道地址**</span><span class="sxs-lookup"><span data-stu-id="600dc-148">**Street address** added</span></span></br><span data-ttu-id="600dc-149">**地址行 1**、**地址行 2** 和**地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="600dc-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="600dc-150">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="600dc-150">New variable compensation setup entities</span></span> | <span data-ttu-id="600dc-151">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="600dc-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="600dc-152">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="600dc-152">**Compensation variable plan**</span></span></br><span data-ttu-id="600dc-153">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="600dc-153">**Vesting rules**</span></span></br><span data-ttu-id="600dc-154">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="600dc-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="600dc-155">新**工作人员日历雇用**实体</span><span class="sxs-lookup"><span data-stu-id="600dc-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="600dc-156">添加了**工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="600dc-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="600dc-157">新**工资单职位详细信息**实体</span><span class="sxs-lookup"><span data-stu-id="600dc-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="600dc-158">添加了**工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="600dc-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="600dc-159">新**职务**实体</span><span class="sxs-lookup"><span data-stu-id="600dc-159">New **Title** entity</span></span> | <span data-ttu-id="600dc-160">添加了**职务**。</span><span class="sxs-lookup"><span data-stu-id="600dc-160">**Title** added.</span></span> <span data-ttu-id="600dc-161">Human Resources 与 Common Data Service 之间的同步流程中将包含新的**职务**实体。</span><span class="sxs-lookup"><span data-stu-id="600dc-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="600dc-162">其最初不是从**工作职位**或**工作**实体引用的。</span><span class="sxs-lookup"><span data-stu-id="600dc-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="600dc-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="600dc-163">See also</span></span>

[<span data-ttu-id="600dc-164">Human Resources 新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="600dc-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="600dc-165">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="600dc-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="600dc-166">更新流程</span><span class="sxs-lookup"><span data-stu-id="600dc-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="600dc-167">管理功能</span><span class="sxs-lookup"><span data-stu-id="600dc-167">Manage features</span></span>](hr-admin-manage-features.md)