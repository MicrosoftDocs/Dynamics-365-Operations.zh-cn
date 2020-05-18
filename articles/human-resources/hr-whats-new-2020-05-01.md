---
title: Dynamics 365 Human Resources 中的新增功能或更改（2020 年 5 月 1 日）
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a0cfd1c1b0dcc9defaad7e4cce22ebe1e91fae
ms.sourcegitcommit: cc5dc0bd90277f1ba684dd310da3274886ce573c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "3320911"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="2a661-103">Dynamics 365 Human Resources 中的新增功能或更改（2020 年 5 月 1 日）</span><span class="sxs-lookup"><span data-stu-id="2a661-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

<span data-ttu-id="2a661-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="2a661-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2a661-105">更改适用于内部版本号 8.1.3196。</span><span class="sxs-lookup"><span data-stu-id="2a661-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="2a661-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="2a661-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="2a661-107">数据管理框架 (DMF) 中提供了新的绩效管理实体</span><span class="sxs-lookup"><span data-stu-id="2a661-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="2a661-108">以下实体现在可用。</span><span class="sxs-lookup"><span data-stu-id="2a661-108">The following entities are now available.</span></span> <span data-ttu-id="2a661-109">如果发现实体列表中未列出这些实体，请使用**框架参数 > 实体设置 > 刷新实体列表**中的**刷新实体**选项。</span><span class="sxs-lookup"><span data-stu-id="2a661-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="2a661-110">**讨论资格**</span><span class="sxs-lookup"><span data-stu-id="2a661-110">**Discussion Competency**</span></span>
- <span data-ttu-id="2a661-111">**讨论目标**</span><span class="sxs-lookup"><span data-stu-id="2a661-111">**Discussion Goals**</span></span>
- <span data-ttu-id="2a661-112">**讨论度量**</span><span class="sxs-lookup"><span data-stu-id="2a661-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="2a661-113">**讨论主题**</span><span class="sxs-lookup"><span data-stu-id="2a661-113">**Discussion Topic**</span></span>
- <span data-ttu-id="2a661-114">**绩效日记帐**</span><span class="sxs-lookup"><span data-stu-id="2a661-114">**Performance Journal**</span></span>
- <span data-ttu-id="2a661-115">**量化指标**</span><span class="sxs-lookup"><span data-stu-id="2a661-115">**Measurement**</span></span>
- <span data-ttu-id="2a661-116">**目标度量**</span><span class="sxs-lookup"><span data-stu-id="2a661-116">**Goal Measurement**</span></span>

<span data-ttu-id="2a661-117">此外，**总分**和**平均分数**已添加到**讨论**实体中。</span><span class="sxs-lookup"><span data-stu-id="2a661-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="2a661-118">增加休假请求长度注释 (275641)</span><span class="sxs-lookup"><span data-stu-id="2a661-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="2a661-119">现在，关于休假请求的注释可以超过 100 个字符。</span><span class="sxs-lookup"><span data-stu-id="2a661-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="2a661-120">当经理或员工登录到其他公司后，不会出现对审核的最终注释 (431688)</span><span class="sxs-lookup"><span data-stu-id="2a661-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="2a661-121">现在，在查看审核时将显示所有注释。</span><span class="sxs-lookup"><span data-stu-id="2a661-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="2a661-122">新的工作人员窗体不支持用户定义的链接 (390374)</span><span class="sxs-lookup"><span data-stu-id="2a661-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="2a661-123">现在，简化的**工作人员**窗体支持用户定义的链接。</span><span class="sxs-lookup"><span data-stu-id="2a661-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="2a661-124">HcmRatingLevelEntity 导致 OData API 崩溃 (439476)</span><span class="sxs-lookup"><span data-stu-id="2a661-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="2a661-125">此更改可更正 API 崩溃错误。</span><span class="sxs-lookup"><span data-stu-id="2a661-125">This change corrects the API crash.</span></span> <span data-ttu-id="2a661-126">重复的名称引起了此错误。</span><span class="sxs-lookup"><span data-stu-id="2a661-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2a661-127">预览模式</span><span class="sxs-lookup"><span data-stu-id="2a661-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="2a661-128">休假暂停</span><span class="sxs-lookup"><span data-stu-id="2a661-128">Leave suspension</span></span>

<span data-ttu-id="2a661-129">可在 Human Resources 中暂停员工的休假和缺勤。</span><span class="sxs-lookup"><span data-stu-id="2a661-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="2a661-130">暂停休假将停止所选休假类型的休假应计。</span><span class="sxs-lookup"><span data-stu-id="2a661-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="2a661-131">如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。</span><span class="sxs-lookup"><span data-stu-id="2a661-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="2a661-132">有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。</span><span class="sxs-lookup"><span data-stu-id="2a661-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="2a661-133">更新用户体验以表明应计已暂停 (429550)</span><span class="sxs-lookup"><span data-stu-id="2a661-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="2a661-134">用户体验现在表明计划已暂停应计。</span><span class="sxs-lookup"><span data-stu-id="2a661-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="2a661-135">暂停指定休假类型的休假应计 (272447)</span><span class="sxs-lookup"><span data-stu-id="2a661-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="2a661-136">在此版本中，HR 可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="2a661-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2a661-137">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="2a661-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2a661-138">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="2a661-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="2a661-139">可用于暂停应计的 DMF 实体 (429549)</span><span class="sxs-lookup"><span data-stu-id="2a661-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="2a661-140">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="2a661-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="2a661-141">将原因代码添加到应计暂停 (429547)</span><span class="sxs-lookup"><span data-stu-id="2a661-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="2a661-142">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="2a661-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="2a661-143">开始从人力资源参数转换到休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="2a661-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="2a661-144">此版本开始将人力资源参数与休假和缺勤参数进行合并。</span><span class="sxs-lookup"><span data-stu-id="2a661-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2a661-145">结转规则</span><span class="sxs-lookup"><span data-stu-id="2a661-145">Carry forward rules</span></span>

<span data-ttu-id="2a661-146">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="2a661-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2a661-147">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="2a661-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2a661-148">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="2a661-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2a661-149">已知问题</span><span class="sxs-lookup"><span data-stu-id="2a661-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="2a661-150">SharePoint 预览在某些环境下不起作用</span><span class="sxs-lookup"><span data-stu-id="2a661-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="2a661-151">如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：</span><span class="sxs-lookup"><span data-stu-id="2a661-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="2a661-152">验证管理员用户帐户是否具有与用户记录关联的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="2a661-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="2a661-153">可在**用户**页面查看这些信息。</span><span class="sxs-lookup"><span data-stu-id="2a661-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="2a661-154">如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。</span><span class="sxs-lookup"><span data-stu-id="2a661-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="2a661-155">默认情况下，Excel 设计中不显示电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2a661-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="2a661-156">您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。</span><span class="sxs-lookup"><span data-stu-id="2a661-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="2a661-157">完成这些步骤后，您可以更新管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="2a661-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="2a661-158">管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="2a661-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="2a661-159">访问 SharePoint 中的附件启动文档预览。</span><span class="sxs-lookup"><span data-stu-id="2a661-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="2a661-160">使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="2a661-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>