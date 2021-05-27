---
title: Retail 中的工时和出勤管理
description: 此主题介绍 Dynamics 365 Commerce 中工时和出勤管理支持的方案。
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021480"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="a7d84-103">Retail 中的工时和出勤管理</span><span class="sxs-lookup"><span data-stu-id="a7d84-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7d84-104">此主题介绍 Dynamics 365 Commerce 中工时和出勤管理支持的方案。</span><span class="sxs-lookup"><span data-stu-id="a7d84-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="a7d84-105">管理工作人员设置和计划</span><span class="sxs-lookup"><span data-stu-id="a7d84-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="a7d84-106">初始配置</span><span class="sxs-lookup"><span data-stu-id="a7d84-106">Initial configuration</span></span>

- <span data-ttu-id="a7d84-107">运行配置向导。</span><span class="sxs-lookup"><span data-stu-id="a7d84-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="a7d84-108">将工作人员登记为时间登记工作人员。</span><span class="sxs-lookup"><span data-stu-id="a7d84-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="a7d84-109">计划工作人员计划</span><span class="sxs-lookup"><span data-stu-id="a7d84-109">Plan worker schedules</span></span>

- <span data-ttu-id="a7d84-110">使用工作进度表应用模板。</span><span class="sxs-lookup"><span data-stu-id="a7d84-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="a7d84-111">有关详细信息，请参阅[使用工作进度表应用模板](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner)。</span><span class="sxs-lookup"><span data-stu-id="a7d84-111">For more information, see [Apply profiles using work planner](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).</span></span>

<span data-ttu-id="a7d84-112">有关配置步骤的信息，请参阅[设置“时间和出勤情况”](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance)。</span><span class="sxs-lookup"><span data-stu-id="a7d84-112">For information about the configuration steps, see [Setting up time and attendance](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="a7d84-113">特定于商业的配置</span><span class="sxs-lookup"><span data-stu-id="a7d84-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="a7d84-114">为您要启用时间登记的工作人员启用打卡时间的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="a7d84-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="a7d84-115">单击 **POS 功能配置文件** &gt; **功能** &gt; **POS 时间登记** &gt; **启用时间登记**。</span><span class="sxs-lookup"><span data-stu-id="a7d84-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="a7d84-116">配置销售点 (POS) 权限组以启用查看打卡时间条目权限。</span><span class="sxs-lookup"><span data-stu-id="a7d84-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="a7d84-117">此权限允许用户查看商店中其他工作人员的打卡时间登记（以及用户与其关联的任何其他商店，通过通讯簿）。</span><span class="sxs-lookup"><span data-stu-id="a7d84-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="a7d84-118">您可能要为经理角色启用此权限，但不为出纳员角色启用。</span><span class="sxs-lookup"><span data-stu-id="a7d84-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="a7d84-119">单击 **POS 权限组** &gt; **查看打卡时间条目**。</span><span class="sxs-lookup"><span data-stu-id="a7d84-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="a7d84-120">登记时间</span><span class="sxs-lookup"><span data-stu-id="a7d84-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="a7d84-121">出纳员和非出纳员时间登记</span><span class="sxs-lookup"><span data-stu-id="a7d84-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="a7d84-122">在 POS 上：</span><span class="sxs-lookup"><span data-stu-id="a7d84-122">On POS:</span></span>

    - <span data-ttu-id="a7d84-123">上班打卡操作：</span><span class="sxs-lookup"><span data-stu-id="a7d84-123">Clock-in operations:</span></span>

        - <span data-ttu-id="a7d84-124">登录非银箱操作或新班次。</span><span class="sxs-lookup"><span data-stu-id="a7d84-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="a7d84-125">选择打卡时间操作。</span><span class="sxs-lookup"><span data-stu-id="a7d84-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="a7d84-126">选择所需操作：</span><span class="sxs-lookup"><span data-stu-id="a7d84-126">Select a desired operation:</span></span>

            - <span data-ttu-id="a7d84-127">上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-127">Clock-in</span></span>
            - <span data-ttu-id="a7d84-128">工间休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-128">Break for Work</span></span>
            - <span data-ttu-id="a7d84-129">午餐休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-129">Break for Lunch</span></span>
            - <span data-ttu-id="a7d84-130">下班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="a7d84-131">当前状态</span><span class="sxs-lookup"><span data-stu-id="a7d84-131">Current state</span></span></th>
        <th><span data-ttu-id="a7d84-132">可用操作</span><span class="sxs-lookup"><span data-stu-id="a7d84-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="a7d84-133">上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="a7d84-134">工间休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-134">Break for Work</span></span></li>
        <li><span data-ttu-id="a7d84-135">午餐休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="a7d84-136">下班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="a7d84-137">工间休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-137">Break for Work</span></span></td>
        <td><span data-ttu-id="a7d84-138">上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="a7d84-139">午餐休息</span><span class="sxs-lookup"><span data-stu-id="a7d84-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="a7d84-140">上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="a7d84-141">下班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-141">Clock-out</span></span></td>
        <td><span data-ttu-id="a7d84-142">上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="a7d84-143">[![打卡时间状态](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="a7d84-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="a7d84-144">查看确认消息，验证当前活动时间是否正确。</span><span class="sxs-lookup"><span data-stu-id="a7d84-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="a7d84-145">日志：</span><span class="sxs-lookup"><span data-stu-id="a7d84-145">Logbook:</span></span>

    - <span data-ttu-id="a7d84-146">单击 **日志** 查看打卡时间活动。</span><span class="sxs-lookup"><span data-stu-id="a7d84-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="a7d84-147">使用时间筛选器可选择不同的时间范围。</span><span class="sxs-lookup"><span data-stu-id="a7d84-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="a7d84-148">如果您在多个商店位置工作，可以查看您在那里记录时间的所有商店的时间登记。</span><span class="sxs-lookup"><span data-stu-id="a7d84-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="a7d84-149">可以使用商店筛选器查看所选商店的时间登记。</span><span class="sxs-lookup"><span data-stu-id="a7d84-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="a7d84-150">不同时区：</span><span class="sxs-lookup"><span data-stu-id="a7d84-150">Different time zones:</span></span>

    - <span data-ttu-id="a7d84-151">如果您从不同位置查看时间（用于出纳员日志，或为经理方案使用 **查看打卡时间条目**），并且该位置在不同的时区，您看到的时间记录将转换为您本地的时区。</span><span class="sxs-lookup"><span data-stu-id="a7d84-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="a7d84-152">例如，您是两个商店的经理，一个在亚利桑那和另一个在内华达。</span><span class="sxs-lookup"><span data-stu-id="a7d84-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="a7d84-153">出纳员在亚利桑那上午 9:00 上班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="a7d84-154">登记。</span><span class="sxs-lookup"><span data-stu-id="a7d84-154">in Arizona.</span></span> <span data-ttu-id="a7d84-155">此时，该时间是内华达的上午 8:00。</span><span class="sxs-lookup"><span data-stu-id="a7d84-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="a7d84-156">因此，如果您是在内华达商店并查看时间登记记录，时间登记标记为上午 8 点。</span><span class="sxs-lookup"><span data-stu-id="a7d84-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="a7d84-157">查看工作人员时间登记</span><span class="sxs-lookup"><span data-stu-id="a7d84-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="a7d84-158">查看工作人员时间登记，并按商店或活动类型筛选</span><span class="sxs-lookup"><span data-stu-id="a7d84-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="a7d84-159">在 POS 上：</span><span class="sxs-lookup"><span data-stu-id="a7d84-159">On POS:</span></span>

- <span data-ttu-id="a7d84-160">选择 **查看打卡时间条目**。</span><span class="sxs-lookup"><span data-stu-id="a7d84-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="a7d84-161">您看到分配到您被分配的同一商店的所有工作人员的打卡时间登记活动。</span><span class="sxs-lookup"><span data-stu-id="a7d84-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="a7d84-162">您可以使用活动类型和商店筛选器筛选时间登记。</span><span class="sxs-lookup"><span data-stu-id="a7d84-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="a7d84-163">处理和管理时间登记</span><span class="sxs-lookup"><span data-stu-id="a7d84-163">Process and manage time registrations</span></span>

<span data-ttu-id="a7d84-164">Commerce 用户按照工作流计算、审核和将时间登记转移到工资单。</span><span class="sxs-lookup"><span data-stu-id="a7d84-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="a7d84-165">主要操作</span><span class="sxs-lookup"><span data-stu-id="a7d84-165">Primary operations</span></span>

- <span data-ttu-id="a7d84-166">计算</span><span class="sxs-lookup"><span data-stu-id="a7d84-166">Calculate</span></span>
- <span data-ttu-id="a7d84-167">批准</span><span class="sxs-lookup"><span data-stu-id="a7d84-167">Approve</span></span>
- <span data-ttu-id="a7d84-168">提交到工资单</span><span class="sxs-lookup"><span data-stu-id="a7d84-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="a7d84-169">其他常用操作</span><span class="sxs-lookup"><span data-stu-id="a7d84-169">Other common operations</span></span>

- <span data-ttu-id="a7d84-170">批量下班打卡</span><span class="sxs-lookup"><span data-stu-id="a7d84-170">Bulk Clock-out</span></span>
- <span data-ttu-id="a7d84-171">登记缺勤</span><span class="sxs-lookup"><span data-stu-id="a7d84-171">Register Absence</span></span>

<span data-ttu-id="a7d84-172">有关如何处理时间和出勤登记的详细信息，请参阅[处理时间和出勤登记](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations)。</span><span class="sxs-lookup"><span data-stu-id="a7d84-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]