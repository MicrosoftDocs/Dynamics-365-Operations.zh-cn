---
title: Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改
description: 本文介绍 2020 年 2 月 18 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
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
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66ffd9d0ffcf0e8466be785274ef5fb0fceda7a9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463782"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="85766-103">Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="85766-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="85766-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="85766-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="85766-105">更改适用于内部版本号 8.1.2903。</span><span class="sxs-lookup"><span data-stu-id="85766-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="85766-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="85766-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="85766-107">平台 update 32</span><span class="sxs-lookup"><span data-stu-id="85766-107">Platform update 32</span></span> 

<span data-ttu-id="85766-108">现已推出了平台更新 32。</span><span class="sxs-lookup"><span data-stu-id="85766-108">Platform update 32 is now available.</span></span> <span data-ttu-id="85766-109">有关详细信息，请参阅 [Finance and Operations 应用的平台更新 32（2020 年 2 月）的新增功能或更改的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。</span><span class="sxs-lookup"><span data-stu-id="85766-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="85766-110">更改简化的员工窗体中的查看选项时记忆搜索值 (383833)</span><span class="sxs-lookup"><span data-stu-id="85766-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="85766-111">现在更改查看选项和应用更改时，新的 **工作人员** 窗体将记忆搜索值。</span><span class="sxs-lookup"><span data-stu-id="85766-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="85766-112">预览功能中的薪酬管理摘要磁贴重定向到错误的窗体 (401861)</span><span class="sxs-lookup"><span data-stu-id="85766-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="85766-113">固定和可变薪酬管理磁贴现在在新的 **工作人员** 窗体中显示正确的记录。</span><span class="sxs-lookup"><span data-stu-id="85766-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="85766-114">仅适用于简化的员工窗体预览功能。</span><span class="sxs-lookup"><span data-stu-id="85766-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="85766-115">可以在 **功能管理** 中启用此预览功能。</span><span class="sxs-lookup"><span data-stu-id="85766-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="85766-116">有关更多信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="85766-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="85766-117">Dataverse 中某些请假记录的“状态”字段为空 (414915)</span><span class="sxs-lookup"><span data-stu-id="85766-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="85766-118">此更改更正了 Dataverse中当请假的 **状态** 字段设置为 **审查** 时的问题。</span><span class="sxs-lookup"><span data-stu-id="85766-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="85766-119">Dataverse 现在可以体现此状态。</span><span class="sxs-lookup"><span data-stu-id="85766-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="85766-120">只能跳过所分配作业的差距分析 (411390)</span><span class="sxs-lookup"><span data-stu-id="85766-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="85766-121">现在可以对 Human Resources 中定义的任何作业执行技能差距分析。</span><span class="sxs-lookup"><span data-stu-id="85766-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="85766-122">在新环境中，系统币种不能从 Dataverse 同步到 Human Resources (418011)</span><span class="sxs-lookup"><span data-stu-id="85766-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="85766-123">Dataverse 中的系统币种现在可以同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="85766-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="85766-124">预览模式</span><span class="sxs-lookup"><span data-stu-id="85766-124">In preview</span></span>

- [<span data-ttu-id="85766-125">休假和缺勤预览功能</span><span class="sxs-lookup"><span data-stu-id="85766-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="85766-126">福利管理预览功能</span><span class="sxs-lookup"><span data-stu-id="85766-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="85766-127">即将推出</span><span class="sxs-lookup"><span data-stu-id="85766-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="85766-128">更新的 Dataverse 解决方案</span><span class="sxs-lookup"><span data-stu-id="85766-128">Updated Dataverse solution</span></span>

<span data-ttu-id="85766-129">一个新的 Dataverse 解决方案很快将推出，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="85766-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="85766-130">说明</span><span class="sxs-lookup"><span data-stu-id="85766-130">Description</span></span> | <span data-ttu-id="85766-131">找零</span><span class="sxs-lookup"><span data-stu-id="85766-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="85766-132">**工作/职位** 实体更改</span><span class="sxs-lookup"><span data-stu-id="85766-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="85766-133">添加了 **薪酬区域**</span><span class="sxs-lookup"><span data-stu-id="85766-133">**Compensation region** added</span></span></br><span data-ttu-id="85766-134">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="85766-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="85766-135">**工作人员** 实体更改</span><span class="sxs-lookup"><span data-stu-id="85766-135">**Worker** entity changes</span></span> | <span data-ttu-id="85766-136">添加了 **姓名顺序**</span><span class="sxs-lookup"><span data-stu-id="85766-136">**Name sequence** added</span></span></br><span data-ttu-id="85766-137">添加了 **在家工作**</span><span class="sxs-lookup"><span data-stu-id="85766-137">**Works from home** added</span></span></br><span data-ttu-id="85766-138">添加了 **语言**</span><span class="sxs-lookup"><span data-stu-id="85766-138">**Language** added</span></span></br><span data-ttu-id="85766-139">添加了 **受聘日期**</span><span class="sxs-lookup"><span data-stu-id="85766-139">**Seniority date** added</span></span></br><span data-ttu-id="85766-140">添加了 **周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="85766-140">**Anniversary date** added</span></span></br><span data-ttu-id="85766-141">添加了 **原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="85766-141">**Original hire date** added</span></span> |
| <span data-ttu-id="85766-142">**雇用** 实体更改</span><span class="sxs-lookup"><span data-stu-id="85766-142">**Employment** entity changes</span></span> | <span data-ttu-id="85766-143">添加了 **财务维度**</span><span class="sxs-lookup"><span data-stu-id="85766-143">**Financial dimensions** added</span></span></br><span data-ttu-id="85766-144">添加了 **离职原因**</span><span class="sxs-lookup"><span data-stu-id="85766-144">**Termination reason** added</span></span></br><span data-ttu-id="85766-145">**转变日期** 重命名为 **离职日期**</span><span class="sxs-lookup"><span data-stu-id="85766-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="85766-146">添加了 **试用日期**</span><span class="sxs-lookup"><span data-stu-id="85766-146">**Probation date** added</span></span> |
| <span data-ttu-id="85766-147">**工作人员地址** 实体更改</span><span class="sxs-lookup"><span data-stu-id="85766-147">**Worker address** entity changes</span></span> | <span data-ttu-id="85766-148">添加了 **街道地址**</span><span class="sxs-lookup"><span data-stu-id="85766-148">**Street address** added</span></span></br><span data-ttu-id="85766-149">**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用</span><span class="sxs-lookup"><span data-stu-id="85766-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="85766-150">新的可变薪酬设置实体</span><span class="sxs-lookup"><span data-stu-id="85766-150">New variable compensation setup entities</span></span> | <span data-ttu-id="85766-151">**可变薪酬计划类型**</span><span class="sxs-lookup"><span data-stu-id="85766-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="85766-152">**薪酬可变计划**</span><span class="sxs-lookup"><span data-stu-id="85766-152">**Compensation variable plan**</span></span></br><span data-ttu-id="85766-153">**股份行权规则**</span><span class="sxs-lookup"><span data-stu-id="85766-153">**Vesting rules**</span></span></br><span data-ttu-id="85766-154">**可变薪酬计划级别**</span><span class="sxs-lookup"><span data-stu-id="85766-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="85766-155">新 **工作人员日历雇用** 实体</span><span class="sxs-lookup"><span data-stu-id="85766-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="85766-156">添加了 **工作日历实体**</span><span class="sxs-lookup"><span data-stu-id="85766-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="85766-157">新 **工资单职位详细信息** 实体</span><span class="sxs-lookup"><span data-stu-id="85766-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="85766-158">添加了 **工资单职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="85766-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="85766-159">新 **职务** 实体</span><span class="sxs-lookup"><span data-stu-id="85766-159">New **Title** entity</span></span> | <span data-ttu-id="85766-160">添加了 **职务**。</span><span class="sxs-lookup"><span data-stu-id="85766-160">**Title** added.</span></span> <span data-ttu-id="85766-161">Human Resources 与 Dataverse 之间的同步流程中将包含新的 **职务** 实体。</span><span class="sxs-lookup"><span data-stu-id="85766-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="85766-162">其最初不是从 **工作职位** 或 **工作** 实体引用的。</span><span class="sxs-lookup"><span data-stu-id="85766-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="85766-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="85766-163">See also</span></span>

[<span data-ttu-id="85766-164">Human Resources 新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="85766-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="85766-165">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="85766-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="85766-166">更新流程</span><span class="sxs-lookup"><span data-stu-id="85766-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="85766-167">管理功能</span><span class="sxs-lookup"><span data-stu-id="85766-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]