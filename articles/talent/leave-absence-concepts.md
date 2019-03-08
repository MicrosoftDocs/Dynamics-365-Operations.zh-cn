---
title: 休假和缺勤概念
description: 此主题描述休假和缺勤概念，以及如何确定休假余额。
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303487"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="ab55b-103">休假和缺勤概念</span><span class="sxs-lookup"><span data-stu-id="ab55b-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab55b-104">此主题中描述的概念和术语可以帮助您确定如何奖励员工休假，以及员工时间余额的计算方式。</span><span class="sxs-lookup"><span data-stu-id="ab55b-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="ab55b-105">有关休假和缺勤管理的详细信息，请参阅[休假和缺勤管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview)。</span><span class="sxs-lookup"><span data-stu-id="ab55b-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="ab55b-106">休假计划详细信息</span><span class="sxs-lookup"><span data-stu-id="ab55b-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="ab55b-107">入职日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-107">Start date</span></span>

<span data-ttu-id="ab55b-108">开始日期是累积处理开始的日期。</span><span class="sxs-lookup"><span data-stu-id="ab55b-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="ab55b-109">开始日期也用作用于计算结转金额的周年纪念日日期。</span><span class="sxs-lookup"><span data-stu-id="ab55b-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="ab55b-110">应计项目</span><span class="sxs-lookup"><span data-stu-id="ab55b-110">Accruals</span></span>

<span data-ttu-id="ab55b-111">应计项目确定奖励员工休假的时间和频率。</span><span class="sxs-lookup"><span data-stu-id="ab55b-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="ab55b-112">有关应在何时奖励应计项目的策略以及按比例分配策略在设置休假和缺勤计划时在**应计项目**部分定义。</span><span class="sxs-lookup"><span data-stu-id="ab55b-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="ab55b-113">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-113">Accrual frequency</span></span>

<span data-ttu-id="ab55b-114">应计频率定义休假计入或奖励的频率。</span><span class="sxs-lookup"><span data-stu-id="ab55b-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="ab55b-115">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-115">The following options are available:</span></span>

- <span data-ttu-id="ab55b-116">日常</span><span class="sxs-lookup"><span data-stu-id="ab55b-116">Daily</span></span>
- <span data-ttu-id="ab55b-117">每周</span><span class="sxs-lookup"><span data-stu-id="ab55b-117">Weekly</span></span>
- <span data-ttu-id="ab55b-118">每两周</span><span class="sxs-lookup"><span data-stu-id="ab55b-118">Biweekly</span></span>
- <span data-ttu-id="ab55b-119">每半月</span><span class="sxs-lookup"><span data-stu-id="ab55b-119">Semimonthly</span></span>
- <span data-ttu-id="ab55b-120">每月</span><span class="sxs-lookup"><span data-stu-id="ab55b-120">Monthly</span></span>
- <span data-ttu-id="ab55b-121">每季度</span><span class="sxs-lookup"><span data-stu-id="ab55b-121">Quarterly</span></span>
- <span data-ttu-id="ab55b-122">每半年</span><span class="sxs-lookup"><span data-stu-id="ab55b-122">Semiannually</span></span>
- <span data-ttu-id="ab55b-123">每年</span><span class="sxs-lookup"><span data-stu-id="ab55b-123">Annually</span></span>
- <span data-ttu-id="ab55b-124">无</span><span class="sxs-lookup"><span data-stu-id="ab55b-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="ab55b-125">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-125">Accrual period basis</span></span>

<span data-ttu-id="ab55b-126">应计期间基数确定用于计算应计期间的日期。</span><span class="sxs-lookup"><span data-stu-id="ab55b-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="ab55b-127">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-127">The following options are available:</span></span>

- <span data-ttu-id="ab55b-128">**计划开始日期**</span><span class="sxs-lookup"><span data-stu-id="ab55b-128">**Plan start date**</span></span>
- <span data-ttu-id="ab55b-129">**员工特定日期** – 在选择该选项时，值确定用于计算应计期间的初始日期值的来源。</span><span class="sxs-lookup"><span data-stu-id="ab55b-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="ab55b-130">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-130">The following options are available:</span></span>

    - <span data-ttu-id="ab55b-131">自定义</span><span class="sxs-lookup"><span data-stu-id="ab55b-131">Custom</span></span>
    - <span data-ttu-id="ab55b-132">周年纪念日日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-132">Anniversary date</span></span>
    - <span data-ttu-id="ab55b-133">原始雇用日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-133">Original hire date</span></span>
    - <span data-ttu-id="ab55b-134">受聘日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-134">Seniority date</span></span>
    - <span data-ttu-id="ab55b-135">工作人员的调整后开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="ab55b-136">工作人员的开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="ab55b-137">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-137">Accrual award date</span></span>

<span data-ttu-id="ab55b-138">应计奖励日期确定奖励员工休假的时间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="ab55b-139">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-139">The following options are available:</span></span>

- <span data-ttu-id="ab55b-140">**应计期间结束日期** – 员工将被奖励在奖励期间的最后一天休假。</span><span class="sxs-lookup"><span data-stu-id="ab55b-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="ab55b-141">若要计入正确金额，应计过程必须涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="ab55b-142">例如，应计期间是 2018 年 1 月 1 到 2018 年 1 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="ab55b-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="ab55b-143">在这种情况下，为包含 1 月，必须为 2018 年 2 月 1 日运行应计。</span><span class="sxs-lookup"><span data-stu-id="ab55b-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="ab55b-144">**应计期间开始日期** – 员工将被奖励在奖励期间的第一天休假。</span><span class="sxs-lookup"><span data-stu-id="ab55b-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="ab55b-145">针对登记的应计策略</span><span class="sxs-lookup"><span data-stu-id="ab55b-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="ab55b-146">针对登记的应计策略定义员工在应计期间中期登记时如何计算应计。</span><span class="sxs-lookup"><span data-stu-id="ab55b-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="ab55b-147">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-147">The following options are available:</span></span>

- <span data-ttu-id="ab55b-148">**按比例分配** – 登记日期和开始日期之间的日期范围用于确定天数差异。</span><span class="sxs-lookup"><span data-stu-id="ab55b-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="ab55b-149">差异在处理应计时应用。</span><span class="sxs-lookup"><span data-stu-id="ab55b-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="ab55b-150">**完全应计** – 完全应计金额基于层，在第一个应计处理期间奖励。</span><span class="sxs-lookup"><span data-stu-id="ab55b-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="ab55b-151">**不计入** – 不计入在下一个应计期间奖励。</span><span class="sxs-lookup"><span data-stu-id="ab55b-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="ab55b-152">针对取消登记的应计策略</span><span class="sxs-lookup"><span data-stu-id="ab55b-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="ab55b-153">针对取消登记的应计策略定义员工在应计期间中期取消登记时如何计算应计。</span><span class="sxs-lookup"><span data-stu-id="ab55b-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="ab55b-154">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="ab55b-154">The following options are available:</span></span>

- <span data-ttu-id="ab55b-155">**按比例分配** – 登记日期和开始日期之间的日期范围用于确定天数差异。</span><span class="sxs-lookup"><span data-stu-id="ab55b-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="ab55b-156">差异在处理应计时应用。</span><span class="sxs-lookup"><span data-stu-id="ab55b-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="ab55b-157">**完全应计** – 完全应计金额基于层，在第一个应计处理期间奖励。</span><span class="sxs-lookup"><span data-stu-id="ab55b-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="ab55b-158">**不计入** – 不计入在下一个应计期间奖励。</span><span class="sxs-lookup"><span data-stu-id="ab55b-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="ab55b-159">应计计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-159">Accrual schedule</span></span>

<span data-ttu-id="ab55b-160">应计计划确定员工将如何累积休假时间，以及员工将累积和结转的金额。</span><span class="sxs-lookup"><span data-stu-id="ab55b-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="ab55b-161">可以创建层，以便基于不同级别奖励休假。</span><span class="sxs-lookup"><span data-stu-id="ab55b-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="ab55b-162">服务月数</span><span class="sxs-lookup"><span data-stu-id="ab55b-162">Months of service</span></span>

<span data-ttu-id="ab55b-163">**服务月数**值定义员工有资格累积所必须工作的最少月数。</span><span class="sxs-lookup"><span data-stu-id="ab55b-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="ab55b-164">如果员工不需要最小数量，将值设置为 **0**。</span><span class="sxs-lookup"><span data-stu-id="ab55b-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="ab55b-165">工作时数</span><span class="sxs-lookup"><span data-stu-id="ab55b-165">Hours worked</span></span>

<span data-ttu-id="ab55b-166">**工作时数**值定义员工有资格累积每个应计期间所必须工作的最少时数。</span><span class="sxs-lookup"><span data-stu-id="ab55b-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="ab55b-167">如果员工不需要最小数量，将值设置为 **0**。</span><span class="sxs-lookup"><span data-stu-id="ab55b-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="ab55b-168">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-168">Accrual amount</span></span>

<span data-ttu-id="ab55b-169">应计金额是员工每个期间将累积的时数或天数。</span><span class="sxs-lookup"><span data-stu-id="ab55b-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="ab55b-170">此期间基于应计频率。</span><span class="sxs-lookup"><span data-stu-id="ab55b-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="ab55b-171">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-171">Minimum balance</span></span>

<span data-ttu-id="ab55b-172">如果员工可以请求多于可用休假的休假，负值可用于最小余额。</span><span class="sxs-lookup"><span data-stu-id="ab55b-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="ab55b-173">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-173">Maximum carry-forward</span></span>

<span data-ttu-id="ab55b-174">应计过程将在开始日期的周年纪念日调整超过最大结转余额的休假余额。</span><span class="sxs-lookup"><span data-stu-id="ab55b-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="ab55b-175">授权金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-175">Grant amount</span></span>

<span data-ttu-id="ab55b-176">授予金额是员工在休假计划中首次登记时被授予的初始时数或天数。</span><span class="sxs-lookup"><span data-stu-id="ab55b-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="ab55b-177">此金额不针对每个应计期间计入。</span><span class="sxs-lookup"><span data-stu-id="ab55b-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="ab55b-178">登记和余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="ab55b-179">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-179">Enrollment date</span></span>

<span data-ttu-id="ab55b-180">登记日期确定员工何时可以开始累积休假时间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="ab55b-181">例如，如果员工在 2018 年 6 月 15 日在休假计划中登记，她在 2018 年 6 月 15 日前不能累积任何休假时间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="ab55b-182">当前余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-182">Current balance</span></span>

<span data-ttu-id="ab55b-183">当前余额为可以发起休假请求的休假金额。</span><span class="sxs-lookup"><span data-stu-id="ab55b-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="ab55b-184">此金额包括截至当前日期的应计、审核的请求和调整。</span><span class="sxs-lookup"><span data-stu-id="ab55b-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="ab55b-185">当前余额示例</span><span class="sxs-lookup"><span data-stu-id="ab55b-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="ab55b-186">年度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-186">Annual plan</span></span>

<span data-ttu-id="ab55b-187">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-187">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-188">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-188">Plan start date</span></span> | <span data-ttu-id="ab55b-189">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-189">Enrollment date</span></span> | <span data-ttu-id="ab55b-190">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-190">Accrual frequency</span></span> | <span data-ttu-id="ab55b-191">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-191">Accrual period basis</span></span> | <span data-ttu-id="ab55b-192">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-193">1/1/2018</span></span>        | <span data-ttu-id="ab55b-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-194">1/1/2018</span></span>        | <span data-ttu-id="ab55b-195">每年</span><span class="sxs-lookup"><span data-stu-id="ab55b-195">Annual</span></span>            | <span data-ttu-id="ab55b-196">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-196">Plan start date</span></span>      | <span data-ttu-id="ab55b-197">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-197">End of accrual period</span></span> |

<span data-ttu-id="ab55b-198">应计在 2019 年 1 月 1 日 (1/1/2019) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-199">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-199">**Results**</span></span>

| <span data-ttu-id="ab55b-200">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-200">Accrual amount</span></span> | <span data-ttu-id="ab55b-201">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-201">Minimum balance</span></span> | <span data-ttu-id="ab55b-202">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-202">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-203">请求金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-203">Request amount</span></span> | <span data-ttu-id="ab55b-204">当前余额（截至 1/1/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab55b-205">200</span><span class="sxs-lookup"><span data-stu-id="ab55b-205">200</span></span>            | <span data-ttu-id="ab55b-206">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-206">0</span></span>               | <span data-ttu-id="ab55b-207">120</span><span class="sxs-lookup"><span data-stu-id="ab55b-207">120</span></span>                   | <span data-ttu-id="ab55b-208">40</span><span class="sxs-lookup"><span data-stu-id="ab55b-208">40</span></span>             | <span data-ttu-id="ab55b-209">160</span><span class="sxs-lookup"><span data-stu-id="ab55b-209">160</span></span>                              |

<span data-ttu-id="ab55b-210">当前余额 (160) = 应计金额 (200) – 请求金额 (40)</span><span class="sxs-lookup"><span data-stu-id="ab55b-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="ab55b-211">半月计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-211">Semimonthly plan</span></span>

<span data-ttu-id="ab55b-212">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-212">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-213">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-213">Plan start date</span></span> | <span data-ttu-id="ab55b-214">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-214">Enrollment date</span></span> | <span data-ttu-id="ab55b-215">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-215">Accrual frequency</span></span> | <span data-ttu-id="ab55b-216">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-216">Accrual period basis</span></span> | <span data-ttu-id="ab55b-217">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-218">1/1/2018</span></span>        | <span data-ttu-id="ab55b-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-219">2/1/2018</span></span>        | <span data-ttu-id="ab55b-220">每半月</span><span class="sxs-lookup"><span data-stu-id="ab55b-220">Semimonthly</span></span>       | <span data-ttu-id="ab55b-221">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-221">Plan start date</span></span>      | <span data-ttu-id="ab55b-222">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-222">End of accrual period</span></span> |

<span data-ttu-id="ab55b-223">应计在 2018 年 5 月 1 日 (5/1/2018) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-224">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-224">**Results**</span></span>

| <span data-ttu-id="ab55b-225">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-225">Accrual amount</span></span> | <span data-ttu-id="ab55b-226">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-226">Minimum balance</span></span> | <span data-ttu-id="ab55b-227">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-227">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-228">请求金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-228">Request amount</span></span> | <span data-ttu-id="ab55b-229">当前余额（截至 1/1/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab55b-230">5</span><span class="sxs-lookup"><span data-stu-id="ab55b-230">5</span></span>              | <span data-ttu-id="ab55b-231">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-231">0</span></span>               | <span data-ttu-id="ab55b-232">120</span><span class="sxs-lookup"><span data-stu-id="ab55b-232">120</span></span>                   | <span data-ttu-id="ab55b-233">8</span><span class="sxs-lookup"><span data-stu-id="ab55b-233">8</span></span>              | <span data-ttu-id="ab55b-234">22</span><span class="sxs-lookup"><span data-stu-id="ab55b-234">22</span></span>                               |

<span data-ttu-id="ab55b-235">当前余额 (22) = 应计金额 (5 × 6) – 请求金额 (8)</span><span class="sxs-lookup"><span data-stu-id="ab55b-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="ab55b-236">月度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-236">Monthly plan</span></span>

<span data-ttu-id="ab55b-237">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-237">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-238">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-238">Plan start date</span></span> | <span data-ttu-id="ab55b-239">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-239">Enrollment date</span></span> | <span data-ttu-id="ab55b-240">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-240">Accrual frequency</span></span> | <span data-ttu-id="ab55b-241">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-241">Accrual period basis</span></span> | <span data-ttu-id="ab55b-242">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-243">1/1/2018</span></span>        | <span data-ttu-id="ab55b-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-244">2/1/2018</span></span>        | <span data-ttu-id="ab55b-245">每半月</span><span class="sxs-lookup"><span data-stu-id="ab55b-245">Semimonthly</span></span>       | <span data-ttu-id="ab55b-246">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-246">Plan start date</span></span>      | <span data-ttu-id="ab55b-247">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-247">End of accrual period</span></span> |

<span data-ttu-id="ab55b-248">应计在 2018 年 5 月 1 日 (5/1/2018) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-249">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-249">**Results**</span></span>

| <span data-ttu-id="ab55b-250">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-250">Accrual amount</span></span> | <span data-ttu-id="ab55b-251">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-251">Minimum balance</span></span> | <span data-ttu-id="ab55b-252">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-252">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-253">请求金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-253">Request amount</span></span> | <span data-ttu-id="ab55b-254">当前余额（截至 1/1/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab55b-255">5</span><span class="sxs-lookup"><span data-stu-id="ab55b-255">5</span></span>              | <span data-ttu-id="ab55b-256">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-256">0</span></span>               | <span data-ttu-id="ab55b-257">120</span><span class="sxs-lookup"><span data-stu-id="ab55b-257">120</span></span>                   | <span data-ttu-id="ab55b-258">8</span><span class="sxs-lookup"><span data-stu-id="ab55b-258">8</span></span>              | <span data-ttu-id="ab55b-259">7</span><span class="sxs-lookup"><span data-stu-id="ab55b-259">7</span></span>                                |

<span data-ttu-id="ab55b-260">当前余额 (7) = 应计金额 (5 × 3) – 请求金额 (8)</span><span class="sxs-lookup"><span data-stu-id="ab55b-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="ab55b-261">预测余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-261">Forecasted balance</span></span>

<span data-ttu-id="ab55b-262">*预测余额*是可在将来日期使用的休假金额。</span><span class="sxs-lookup"><span data-stu-id="ab55b-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="ab55b-263">应计和结转调整一直预测到该日期。</span><span class="sxs-lookup"><span data-stu-id="ab55b-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="ab55b-264">使用以下公式：</span><span class="sxs-lookup"><span data-stu-id="ab55b-264">The following formula is used:</span></span>

<span data-ttu-id="ab55b-265">星期一预测余额 = 当前余额 – 请求 + 应计 – 结转调整</span><span class="sxs-lookup"><span data-stu-id="ab55b-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="ab55b-266">预测余额示例</span><span class="sxs-lookup"><span data-stu-id="ab55b-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="ab55b-267">年度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-267">Annual plan</span></span>

<span data-ttu-id="ab55b-268">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-268">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-269">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-269">Plan start date</span></span> | <span data-ttu-id="ab55b-270">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-270">Enrollment date</span></span> | <span data-ttu-id="ab55b-271">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-271">Accrual frequency</span></span> | <span data-ttu-id="ab55b-272">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-272">Accrual period basis</span></span> | <span data-ttu-id="ab55b-273">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-274">1/1/2018</span></span>        | <span data-ttu-id="ab55b-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-275">1/1/2018</span></span>        | <span data-ttu-id="ab55b-276">每年</span><span class="sxs-lookup"><span data-stu-id="ab55b-276">Annual</span></span>            | <span data-ttu-id="ab55b-277">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-277">Plan start date</span></span>      | <span data-ttu-id="ab55b-278">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-278">End of accrual period</span></span> |

<span data-ttu-id="ab55b-279">应计在 2019 年 2 月 15 日 (2/15/2019) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-280">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-280">**Results**</span></span>

| <span data-ttu-id="ab55b-281">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-281">Accrual amount</span></span> | <span data-ttu-id="ab55b-282">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-282">Minimum balance</span></span> | <span data-ttu-id="ab55b-283">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-283">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-284">当前余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-284">Current balance</span></span> | <span data-ttu-id="ab55b-285">预测余额（截至 2/15/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab55b-286">20</span><span class="sxs-lookup"><span data-stu-id="ab55b-286">20</span></span>             | <span data-ttu-id="ab55b-287">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-287">0</span></span>               | <span data-ttu-id="ab55b-288">20</span><span class="sxs-lookup"><span data-stu-id="ab55b-288">20</span></span>                    | <span data-ttu-id="ab55b-289">40</span><span class="sxs-lookup"><span data-stu-id="ab55b-289">40</span></span>              | <span data-ttu-id="ab55b-290">40</span><span class="sxs-lookup"><span data-stu-id="ab55b-290">40</span></span>                                   |

<span data-ttu-id="ab55b-291">预测余额 (40) = 应计金额 (20) + 当前余额 (40) – 结转调整 (20)</span><span class="sxs-lookup"><span data-stu-id="ab55b-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="ab55b-292">半月计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-292">Semimonthly plan</span></span>

<span data-ttu-id="ab55b-293">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-293">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-294">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-294">Plan start date</span></span> | <span data-ttu-id="ab55b-295">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-295">Enrollment date</span></span> | <span data-ttu-id="ab55b-296">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-296">Accrual frequency</span></span> | <span data-ttu-id="ab55b-297">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-297">Accrual period basis</span></span> | <span data-ttu-id="ab55b-298">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-299">1/1/2018</span></span>        | <span data-ttu-id="ab55b-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-300">2/1/2018</span></span>        | <span data-ttu-id="ab55b-301">每半月</span><span class="sxs-lookup"><span data-stu-id="ab55b-301">Semimonthly</span></span>       | <span data-ttu-id="ab55b-302">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-302">Plan start date</span></span>      | <span data-ttu-id="ab55b-303">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-303">End of accrual period</span></span> |

<span data-ttu-id="ab55b-304">应计在 2019 年 2 月 15 日 (2/15/2019) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-305">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-305">**Results**</span></span>

| <span data-ttu-id="ab55b-306">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-306">Accrual amount</span></span> | <span data-ttu-id="ab55b-307">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-307">Minimum balance</span></span> | <span data-ttu-id="ab55b-308">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-308">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-309">当前余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-309">Current balance</span></span> | <span data-ttu-id="ab55b-310">预测余额（截至 2/15/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab55b-311">5</span><span class="sxs-lookup"><span data-stu-id="ab55b-311">5</span></span>              | <span data-ttu-id="ab55b-312">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-312">0</span></span>               | <span data-ttu-id="ab55b-313">20</span><span class="sxs-lookup"><span data-stu-id="ab55b-313">20</span></span>                    | <span data-ttu-id="ab55b-314">40</span><span class="sxs-lookup"><span data-stu-id="ab55b-314">40</span></span>              | <span data-ttu-id="ab55b-315">35</span><span class="sxs-lookup"><span data-stu-id="ab55b-315">35</span></span>                                   |

<span data-ttu-id="ab55b-316">预测余额 (35) = 应计金额 (5 × 3) + 当前余额 (40) – 结转调整 (20)</span><span class="sxs-lookup"><span data-stu-id="ab55b-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="ab55b-317">月度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-317">Monthly plan</span></span>

<span data-ttu-id="ab55b-318">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-318">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-319">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-319">Plan start date</span></span> | <span data-ttu-id="ab55b-320">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-320">Enrollment date</span></span> | <span data-ttu-id="ab55b-321">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-321">Accrual frequency</span></span> | <span data-ttu-id="ab55b-322">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-322">Accrual period basis</span></span> | <span data-ttu-id="ab55b-323">应计奖励日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab55b-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-324">1/1/2018</span></span>        | <span data-ttu-id="ab55b-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-325">2/1/2018</span></span>        | <span data-ttu-id="ab55b-326">每半月</span><span class="sxs-lookup"><span data-stu-id="ab55b-326">Semimonthly</span></span>       | <span data-ttu-id="ab55b-327">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-327">Plan start date</span></span>      | <span data-ttu-id="ab55b-328">应计期间结束</span><span class="sxs-lookup"><span data-stu-id="ab55b-328">End of accrual period</span></span> |

<span data-ttu-id="ab55b-329">应计在 2019 年 2 月 15 日 (2/15/2019) 处理，以涵盖整个期间。</span><span class="sxs-lookup"><span data-stu-id="ab55b-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab55b-330">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-330">**Results**</span></span>

| <span data-ttu-id="ab55b-331">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-331">Accrual amount</span></span> | <span data-ttu-id="ab55b-332">最低余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-332">Minimum balance</span></span> | <span data-ttu-id="ab55b-333">最大结转</span><span class="sxs-lookup"><span data-stu-id="ab55b-333">Maximum carry-forward</span></span> | <span data-ttu-id="ab55b-334">当前余额</span><span class="sxs-lookup"><span data-stu-id="ab55b-334">Current balance</span></span> | <span data-ttu-id="ab55b-335">预测余额（截至 2/15/2019）</span><span class="sxs-lookup"><span data-stu-id="ab55b-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab55b-336">10</span><span class="sxs-lookup"><span data-stu-id="ab55b-336">10</span></span>             | <span data-ttu-id="ab55b-337">0</span><span class="sxs-lookup"><span data-stu-id="ab55b-337">0</span></span>               | <span data-ttu-id="ab55b-338">20</span><span class="sxs-lookup"><span data-stu-id="ab55b-338">20</span></span>                    | <span data-ttu-id="ab55b-339">40</span><span class="sxs-lookup"><span data-stu-id="ab55b-339">40</span></span>              | <span data-ttu-id="ab55b-340">30</span><span class="sxs-lookup"><span data-stu-id="ab55b-340">30</span></span>                                   |

<span data-ttu-id="ab55b-341">预测余额 (30) = 应计金额 (10 × 1) + 当前余额 (40) – 结转调整 (20)</span><span class="sxs-lookup"><span data-stu-id="ab55b-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="ab55b-342">按比例分配余额示例</span><span class="sxs-lookup"><span data-stu-id="ab55b-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="ab55b-343">按比例分配月度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-343">Prorated monthly plan</span></span>

<span data-ttu-id="ab55b-344">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-344">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-345">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-345">Plan start date</span></span> | <span data-ttu-id="ab55b-346">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-346">Accrual frequency</span></span> | <span data-ttu-id="ab55b-347">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab55b-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-348">1/1/2018</span></span>        | <span data-ttu-id="ab55b-349">每月</span><span class="sxs-lookup"><span data-stu-id="ab55b-349">Monthly</span></span>           | <span data-ttu-id="ab55b-350">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-350">Plan start date</span></span>      |

<span data-ttu-id="ab55b-351">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-351">**Results**</span></span>

| <span data-ttu-id="ab55b-352">盘点责任人</span><span class="sxs-lookup"><span data-stu-id="ab55b-352">Employee</span></span>            | <span data-ttu-id="ab55b-353">服务月数</span><span class="sxs-lookup"><span data-stu-id="ab55b-353">Months of service</span></span> | <span data-ttu-id="ab55b-354">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-354">Enrollment date</span></span> | <span data-ttu-id="ab55b-355">入职日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-355">Start date</span></span> | <span data-ttu-id="ab55b-356">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-356">Accrual amount</span></span> | <span data-ttu-id="ab55b-357">处理应计</span><span class="sxs-lookup"><span data-stu-id="ab55b-357">Process accrual</span></span> | <span data-ttu-id="ab55b-358">所有者权益</span><span class="sxs-lookup"><span data-stu-id="ab55b-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab55b-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab55b-359">Jeannette Nicholson</span></span> | <span data-ttu-id="ab55b-360">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-360">0.00</span></span>              | <span data-ttu-id="ab55b-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-361">6/1/2018</span></span>        | <span data-ttu-id="ab55b-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-362">6/1/2018</span></span>   | <span data-ttu-id="ab55b-363">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-363">1.00</span></span>           | <span data-ttu-id="ab55b-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-364">9/1/2018</span></span>        | <span data-ttu-id="ab55b-365">3.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-365">3.00</span></span>    |
| <span data-ttu-id="ab55b-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab55b-366">Jay Norman</span></span>          | <span data-ttu-id="ab55b-367">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-367">0.00</span></span>              | <span data-ttu-id="ab55b-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-368">6/15/2018</span></span>       | <span data-ttu-id="ab55b-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-369">6/15/2018</span></span>  | <span data-ttu-id="ab55b-370">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-370">1.00</span></span>           | <span data-ttu-id="ab55b-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-371">9/1/2018</span></span>        | <span data-ttu-id="ab55b-372">2.53</span><span class="sxs-lookup"><span data-stu-id="ab55b-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="ab55b-373">完全应计月度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-373">Full accrual monthly plan</span></span>

<span data-ttu-id="ab55b-374">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-374">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-375">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-375">Plan start date</span></span> | <span data-ttu-id="ab55b-376">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-376">Accrual frequency</span></span> | <span data-ttu-id="ab55b-377">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab55b-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-378">1/1/2018</span></span>        | <span data-ttu-id="ab55b-379">每月</span><span class="sxs-lookup"><span data-stu-id="ab55b-379">Monthly</span></span>           | <span data-ttu-id="ab55b-380">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-380">Plan start date</span></span>      |

<span data-ttu-id="ab55b-381">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-381">**Results**</span></span>

| <span data-ttu-id="ab55b-382">盘点责任人</span><span class="sxs-lookup"><span data-stu-id="ab55b-382">Employee</span></span>            | <span data-ttu-id="ab55b-383">服务月数</span><span class="sxs-lookup"><span data-stu-id="ab55b-383">Months of service</span></span> | <span data-ttu-id="ab55b-384">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-384">Enrollment date</span></span> | <span data-ttu-id="ab55b-385">入职日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-385">Start date</span></span> | <span data-ttu-id="ab55b-386">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-386">Accrual amount</span></span> | <span data-ttu-id="ab55b-387">处理应计</span><span class="sxs-lookup"><span data-stu-id="ab55b-387">Process accrual</span></span> | <span data-ttu-id="ab55b-388">所有者权益</span><span class="sxs-lookup"><span data-stu-id="ab55b-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab55b-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab55b-389">Jeannette Nicholson</span></span> | <span data-ttu-id="ab55b-390">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-390">0.00</span></span>              | <span data-ttu-id="ab55b-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-391">6/1/2018</span></span>        | <span data-ttu-id="ab55b-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-392">6/1/2018</span></span>   | <span data-ttu-id="ab55b-393">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-393">1.00</span></span>           | <span data-ttu-id="ab55b-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-394">9/1/2018</span></span>        | <span data-ttu-id="ab55b-395">3.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-395">3.00</span></span>    |
| <span data-ttu-id="ab55b-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab55b-396">Jay Norman</span></span>          | <span data-ttu-id="ab55b-397">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-397">0.00</span></span>              | <span data-ttu-id="ab55b-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-398">6/15/2018</span></span>       | <span data-ttu-id="ab55b-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-399">6/15/2018</span></span>  | <span data-ttu-id="ab55b-400">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-400">1.00</span></span>           | <span data-ttu-id="ab55b-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-401">9/1/2018</span></span>        | <span data-ttu-id="ab55b-402">3.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="ab55b-403">无应计月度计划</span><span class="sxs-lookup"><span data-stu-id="ab55b-403">No accrual monthly plan</span></span>

<span data-ttu-id="ab55b-404">**计划设置**</span><span class="sxs-lookup"><span data-stu-id="ab55b-404">**Plan setup**</span></span>

| <span data-ttu-id="ab55b-405">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-405">Plan start date</span></span> | <span data-ttu-id="ab55b-406">应计频率</span><span class="sxs-lookup"><span data-stu-id="ab55b-406">Accrual frequency</span></span> | <span data-ttu-id="ab55b-407">应计期间基数</span><span class="sxs-lookup"><span data-stu-id="ab55b-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab55b-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-408">1/1/2018</span></span>        | <span data-ttu-id="ab55b-409">每月</span><span class="sxs-lookup"><span data-stu-id="ab55b-409">Monthly</span></span>           | <span data-ttu-id="ab55b-410">计划开始日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-410">Plan start date</span></span>      |

<span data-ttu-id="ab55b-411">**结果**</span><span class="sxs-lookup"><span data-stu-id="ab55b-411">**Results**</span></span>

| <span data-ttu-id="ab55b-412">盘点责任人</span><span class="sxs-lookup"><span data-stu-id="ab55b-412">Employee</span></span>            | <span data-ttu-id="ab55b-413">服务月数</span><span class="sxs-lookup"><span data-stu-id="ab55b-413">Months of service</span></span> | <span data-ttu-id="ab55b-414">登记日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-414">Enrollment date</span></span> | <span data-ttu-id="ab55b-415">入职日期</span><span class="sxs-lookup"><span data-stu-id="ab55b-415">Start date</span></span> | <span data-ttu-id="ab55b-416">应计金额</span><span class="sxs-lookup"><span data-stu-id="ab55b-416">Accrual amount</span></span> | <span data-ttu-id="ab55b-417">处理应计</span><span class="sxs-lookup"><span data-stu-id="ab55b-417">Process accrual</span></span> | <span data-ttu-id="ab55b-418">所有者权益</span><span class="sxs-lookup"><span data-stu-id="ab55b-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab55b-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab55b-419">Jeannette Nicholson</span></span> | <span data-ttu-id="ab55b-420">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-420">0.00</span></span>              | <span data-ttu-id="ab55b-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-421">6/1/2018</span></span>        | <span data-ttu-id="ab55b-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-422">6/1/2018</span></span>   | <span data-ttu-id="ab55b-423">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-423">1.00</span></span>           | <span data-ttu-id="ab55b-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-424">9/1/2018</span></span>        | <span data-ttu-id="ab55b-425">3.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-425">3.00</span></span>    |
| <span data-ttu-id="ab55b-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab55b-426">Jay Norman</span></span>          | <span data-ttu-id="ab55b-427">0.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-427">0.00</span></span>              | <span data-ttu-id="ab55b-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-428">6/15/2018</span></span>       | <span data-ttu-id="ab55b-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-429">6/15/2018</span></span>  | <span data-ttu-id="ab55b-430">1.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-430">1.00</span></span>           | <span data-ttu-id="ab55b-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab55b-431">9/1/2018</span></span>        | <span data-ttu-id="ab55b-432">2.00</span><span class="sxs-lookup"><span data-stu-id="ab55b-432">2.00</span></span>    |
