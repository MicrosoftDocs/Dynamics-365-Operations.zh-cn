---
title: Dynamics 365 Talent - Core HR（2018 年 9 月 10 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 59cb0203422b7d81b5ca0077370fd9cbdb4a7f89
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010076"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-september-10-2018"></a><span data-ttu-id="25a5f-103">Dynamics 365 Talent: Core HR（2018 年 9 月 10 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="25a5f-103">What's new or changed in Dynamics 365 Talent: Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="25a5f-104">**内部版本 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="25a5f-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="25a5f-105">此主题介绍了 Microsoft Dynamics 365 Talent: Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="25a5f-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="25a5f-106">允许请特定时间段的假（半天）</span><span class="sxs-lookup"><span data-stu-id="25a5f-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="25a5f-107">如果将休假和缺勤设置为以天为单位提交请假，也可以启用半天定义。</span><span class="sxs-lookup"><span data-stu-id="25a5f-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="25a5f-108">然后，当用户提交请假时，可以指定请上半天还是下半天假。</span><span class="sxs-lookup"><span data-stu-id="25a5f-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="25a5f-109">默认情况下，此选项已关闭。</span><span class="sxs-lookup"><span data-stu-id="25a5f-109">By default, this option is turned off.</span></span> <span data-ttu-id="25a5f-110">必须在人力资源参数的**休假和缺勤**区域中文为要请半天假的员工开启此选项。</span><span class="sxs-lookup"><span data-stu-id="25a5f-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="25a5f-111">此功能的安全权限为“维护人力资源参数”。</span><span class="sxs-lookup"><span data-stu-id="25a5f-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="25a5f-112">验证休假和缺勤条目</span><span class="sxs-lookup"><span data-stu-id="25a5f-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="25a5f-113">根据休假的配置方式，尝试请假时间超过工作日的员工会收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="25a5f-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="25a5f-114">换言之，如果在给定日期请求时间超过一整天，就会予以警告。</span><span class="sxs-lookup"><span data-stu-id="25a5f-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="25a5f-115">此验证始终开启。</span><span class="sxs-lookup"><span data-stu-id="25a5f-115">This validation is always turned on.</span></span> <span data-ttu-id="25a5f-116">只要员工超过了定义的天数阈值，都会在请假时收到警告。</span><span class="sxs-lookup"><span data-stu-id="25a5f-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="25a5f-117">工作流中的条件语句的更多字段</span><span class="sxs-lookup"><span data-stu-id="25a5f-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="25a5f-118">已向 Core HR 中的若干工作流的条件语句和占位符添加了更多字段。</span><span class="sxs-lookup"><span data-stu-id="25a5f-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="25a5f-119">已向补偿、离职和转岗工作流添加了以下字段：</span><span class="sxs-lookup"><span data-stu-id="25a5f-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="25a5f-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="25a5f-120">EmploymentType</span></span>
- <span data-ttu-id="25a5f-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="25a5f-121">LegalEntity</span></span>
- <span data-ttu-id="25a5f-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="25a5f-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="25a5f-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="25a5f-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="25a5f-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="25a5f-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="25a5f-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="25a5f-125">TransitionDate</span></span>
- <span data-ttu-id="25a5f-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="25a5f-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="25a5f-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="25a5f-127">WorkerStartDate</span></span>
- <span data-ttu-id="25a5f-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="25a5f-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="25a5f-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="25a5f-129">ProbationEndDate</span></span>
- <span data-ttu-id="25a5f-130">位置</span><span class="sxs-lookup"><span data-stu-id="25a5f-130">Position</span></span>
- <span data-ttu-id="25a5f-131">工会</span><span class="sxs-lookup"><span data-stu-id="25a5f-131">Union</span></span>
- <span data-ttu-id="25a5f-132">部门</span><span class="sxs-lookup"><span data-stu-id="25a5f-132">Department</span></span>
- <span data-ttu-id="25a5f-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="25a5f-133">PositionType</span></span>
- <span data-ttu-id="25a5f-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="25a5f-134">CompLocation</span></span>
- <span data-ttu-id="25a5f-135">职位</span><span class="sxs-lookup"><span data-stu-id="25a5f-135">Title</span></span>
- <span data-ttu-id="25a5f-136">工作</span><span class="sxs-lookup"><span data-stu-id="25a5f-136">Job</span></span>
- <span data-ttu-id="25a5f-137">JobType</span><span class="sxs-lookup"><span data-stu-id="25a5f-137">JobType</span></span>
- <span data-ttu-id="25a5f-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="25a5f-138">JobFamily</span></span>
- <span data-ttu-id="25a5f-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="25a5f-139">JobFunction</span></span>

<span data-ttu-id="25a5f-140">已向职位工作流添加了以下字段：</span><span class="sxs-lookup"><span data-stu-id="25a5f-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="25a5f-141">位置</span><span class="sxs-lookup"><span data-stu-id="25a5f-141">Position</span></span>
- <span data-ttu-id="25a5f-142">工会</span><span class="sxs-lookup"><span data-stu-id="25a5f-142">Union</span></span>
- <span data-ttu-id="25a5f-143">部门</span><span class="sxs-lookup"><span data-stu-id="25a5f-143">Department</span></span>
- <span data-ttu-id="25a5f-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="25a5f-144">PositionType</span></span>
- <span data-ttu-id="25a5f-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="25a5f-145">CompLocation</span></span>
- <span data-ttu-id="25a5f-146">职位</span><span class="sxs-lookup"><span data-stu-id="25a5f-146">Title</span></span>
- <span data-ttu-id="25a5f-147">工作</span><span class="sxs-lookup"><span data-stu-id="25a5f-147">Job</span></span>
- <span data-ttu-id="25a5f-148">JobType</span><span class="sxs-lookup"><span data-stu-id="25a5f-148">JobType</span></span>
- <span data-ttu-id="25a5f-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="25a5f-149">JobFamily</span></span>
- <span data-ttu-id="25a5f-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="25a5f-150">JobFunction</span></span>

<span data-ttu-id="25a5f-151">条件语句和占位符可用于有权配置上面介绍的工作流的所有用户。</span><span class="sxs-lookup"><span data-stu-id="25a5f-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="25a5f-152">从人员管理导航到 Attract</span><span class="sxs-lookup"><span data-stu-id="25a5f-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="25a5f-153">在人员管理中，如果尚未设置 Attract，**可雇用的应聘者**部分将指示用户从 Attract 开始，而不是显示消息“我们未找到要在此处显示的任何内容。”</span><span class="sxs-lookup"><span data-stu-id="25a5f-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="25a5f-154">其他更改</span><span class="sxs-lookup"><span data-stu-id="25a5f-154">Other changes</span></span>

<span data-ttu-id="25a5f-155">此版本中还包含若干缺陷修复：</span><span class="sxs-lookup"><span data-stu-id="25a5f-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="25a5f-156">雇用合同工时，请求/操作页面中的**补偿**选项卡应不可用。</span><span class="sxs-lookup"><span data-stu-id="25a5f-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="25a5f-157">请求终止过程中，所有必填字段均包含数据之前，不能继续操作。</span><span class="sxs-lookup"><span data-stu-id="25a5f-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="25a5f-158">已解决了人员管理分析中的排序和日期显示问题。</span><span class="sxs-lookup"><span data-stu-id="25a5f-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
