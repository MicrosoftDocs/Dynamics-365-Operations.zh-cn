---
title: Dynamics 365 Human Resources（2020 年 4 月 13 日）新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f61283f3bab26f54d55ffe7cbea21b1201ed234
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555139"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="7af78-103">Dynamics 365 Human Resources（2020 年 4 月 13 日）新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="7af78-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="7af78-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="7af78-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7af78-105">更改适用于内部版本号 8.1.3136。</span><span class="sxs-lookup"><span data-stu-id="7af78-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="7af78-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="7af78-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="7af78-107">新产品发布频率</span><span class="sxs-lookup"><span data-stu-id="7af78-107">New production release cadence</span></span>

<span data-ttu-id="7af78-108">在本周的发布中，Human Resources 的发布频率将从每周更新变为每两周更新。</span><span class="sxs-lookup"><span data-stu-id="7af78-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="7af78-109">为了确保符合安全部署实践，并在服务中保持高标准的稳定性和可靠性，现在为期两周把服务更新部署到所有区域。</span><span class="sxs-lookup"><span data-stu-id="7af78-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="7af78-110">将部署更多测试和监视人员，以验证流程各个阶段是否成功部署。</span><span class="sxs-lookup"><span data-stu-id="7af78-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="7af78-111">有关发布频率的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。</span><span class="sxs-lookup"><span data-stu-id="7af78-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="7af78-112">指定化整类型后“化整精度”字段不可编辑 (435616)</span><span class="sxs-lookup"><span data-stu-id="7af78-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="7af78-113">通过此更改，更新**化整类型**字段后，现在可使用**化整精度**字段。</span><span class="sxs-lookup"><span data-stu-id="7af78-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="7af78-114">不能在休假计划中无应计期间时编辑休假登记结束日期 (413628)</span><span class="sxs-lookup"><span data-stu-id="7af78-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="7af78-115">现在可以编辑登记结束日期，不会出现“必须填写应计日期基础字段”错误。</span><span class="sxs-lookup"><span data-stu-id="7af78-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="7af78-116">雇用实体不同步到 Common Data Service (430834)</span><span class="sxs-lookup"><span data-stu-id="7af78-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="7af78-117">此更改解决了添加财务维度后雇用数据不同步到 Common Data Service 这一问题。</span><span class="sxs-lookup"><span data-stu-id="7af78-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="7af78-118">删除工作日历日历时间间隔实体的多父项 (431775)</span><span class="sxs-lookup"><span data-stu-id="7af78-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="7af78-119">此更改解决了**工作日历时间间隔**实体的多父项问题。</span><span class="sxs-lookup"><span data-stu-id="7af78-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="7af78-120">采用 CAST 函数的筛选器对 OData 调用位置工作人员分配实体无效 (431699)</span><span class="sxs-lookup"><span data-stu-id="7af78-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="7af78-121">此更新中包含一项更改，用于允许 OData 内采用 CAST 函数的筛选器用于**位置工作人员分配**实体。</span><span class="sxs-lookup"><span data-stu-id="7af78-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7af78-122">预览模式</span><span class="sxs-lookup"><span data-stu-id="7af78-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="7af78-123">休假暂停</span><span class="sxs-lookup"><span data-stu-id="7af78-123">Leave suspension</span></span>

<span data-ttu-id="7af78-124">可在 Human Resources 中暂停员工的休假和缺勤。</span><span class="sxs-lookup"><span data-stu-id="7af78-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="7af78-125">暂停休假将停止所选休假类型的休假应计。</span><span class="sxs-lookup"><span data-stu-id="7af78-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="7af78-126">如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。</span><span class="sxs-lookup"><span data-stu-id="7af78-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="7af78-127">有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。</span><span class="sxs-lookup"><span data-stu-id="7af78-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="7af78-128">结转规则</span><span class="sxs-lookup"><span data-stu-id="7af78-128">Carry forward rules</span></span>

<span data-ttu-id="7af78-129">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="7af78-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="7af78-130">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="7af78-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="7af78-131">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="7af78-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="7af78-132">已知问题</span><span class="sxs-lookup"><span data-stu-id="7af78-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="7af78-133">雇用详细信息实体</span><span class="sxs-lookup"><span data-stu-id="7af78-133">Employment Details entity</span></span>

<span data-ttu-id="7af78-134">已使用以下字段更新了**雇用详细信息**实体：</span><span class="sxs-lookup"><span data-stu-id="7af78-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="7af78-135">**付款频率**</span><span class="sxs-lookup"><span data-stu-id="7af78-135">**PayFrequency**</span></span>
- <span data-ttu-id="7af78-136">**雇用类别 ID**</span><span class="sxs-lookup"><span data-stu-id="7af78-136">**Employment Category ID**</span></span>
- <span data-ttu-id="7af78-137">**雇用类型**</span><span class="sxs-lookup"><span data-stu-id="7af78-137">**Employment Type**</span></span>
- <span data-ttu-id="7af78-138">**雇用类型 ID**</span><span class="sxs-lookup"><span data-stu-id="7af78-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="7af78-139">**福利雇用状态**</span><span class="sxs-lookup"><span data-stu-id="7af78-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="7af78-140">这些字段的设置数据依赖于**功能管理**工作区中启用的福利管理。</span><span class="sxs-lookup"><span data-stu-id="7af78-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="7af78-141">请勿填写或更新**雇用详细信息**实体中的这些字段，因为将导致导入期间出错。</span><span class="sxs-lookup"><span data-stu-id="7af78-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="7af78-142">SharePoint 预览在某些环境下不起作用</span><span class="sxs-lookup"><span data-stu-id="7af78-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="7af78-143">如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：</span><span class="sxs-lookup"><span data-stu-id="7af78-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="7af78-144">验证管理员用户帐户是否具有与用户记录关联的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="7af78-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="7af78-145">可在**用户**页面查看这些信息。</span><span class="sxs-lookup"><span data-stu-id="7af78-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="7af78-146">如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。</span><span class="sxs-lookup"><span data-stu-id="7af78-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="7af78-147">默认情况下，Excel 设计中不显示电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7af78-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="7af78-148">您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。</span><span class="sxs-lookup"><span data-stu-id="7af78-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="7af78-149">完成这些步骤后，您可以更新管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="7af78-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="7af78-150">管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="7af78-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="7af78-151">访问 SharePoint 中的附件启动文档预览。</span><span class="sxs-lookup"><span data-stu-id="7af78-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="7af78-152">使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="7af78-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="7af78-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="7af78-153">See also</span></span>

[<span data-ttu-id="7af78-154">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="7af78-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7af78-155">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="7af78-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7af78-156">更新流程</span><span class="sxs-lookup"><span data-stu-id="7af78-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7af78-157">管理功能</span><span class="sxs-lookup"><span data-stu-id="7af78-157">Manage features</span></span>](hr-admin-manage-features.md)