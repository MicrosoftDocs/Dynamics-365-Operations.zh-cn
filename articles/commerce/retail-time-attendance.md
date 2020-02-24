---
title: Retail 中的工时和出勤管理
description: 此主题介绍 Dynamics 365 Commerce 中工时和出勤管理支持的方案。
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021766"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="9dc58-103">Retail 中的工时和出勤管理</span><span class="sxs-lookup"><span data-stu-id="9dc58-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9dc58-104">此主题介绍 Dynamics 365 Commerce 中工时和出勤管理支持的方案。</span><span class="sxs-lookup"><span data-stu-id="9dc58-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="9dc58-105">管理工作人员设置和计划</span><span class="sxs-lookup"><span data-stu-id="9dc58-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="9dc58-106">初始配置</span><span class="sxs-lookup"><span data-stu-id="9dc58-106">Initial configuration</span></span>

- <span data-ttu-id="9dc58-107">运行配置向导。</span><span class="sxs-lookup"><span data-stu-id="9dc58-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="9dc58-108">将工作人员登记为时间登记工作人员。</span><span class="sxs-lookup"><span data-stu-id="9dc58-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="9dc58-109">计划工作人员计划</span><span class="sxs-lookup"><span data-stu-id="9dc58-109">Plan worker schedules</span></span>

- <span data-ttu-id="9dc58-110">使用工作进度表应用模板。</span><span class="sxs-lookup"><span data-stu-id="9dc58-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="9dc58-111">有关详细信息，请参阅[使用工作进度表应用模板](https://technet.microsoft.com/library/aa551234.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9dc58-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="9dc58-112">有关配置步骤的信息，请参阅[设置“时间和出勤情况”](https://technet.microsoft.com/library/aa496971.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9dc58-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="9dc58-113">特定于商业的配置</span><span class="sxs-lookup"><span data-stu-id="9dc58-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="9dc58-114">为您要启用时间登记的工作人员启用打卡时间的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="9dc58-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="9dc58-115">单击 **POS 功能配置文件** &gt; **功能** &gt; **POS 时间登记** &gt; **启用时间登记**。</span><span class="sxs-lookup"><span data-stu-id="9dc58-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="9dc58-116">配置销售点 (POS) 权限组以启用查看打卡时间条目权限。</span><span class="sxs-lookup"><span data-stu-id="9dc58-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="9dc58-117">此权限允许用户查看商店中其他工作人员的打卡时间登记（以及用户与其关联的任何其他商店，通过通讯簿）。</span><span class="sxs-lookup"><span data-stu-id="9dc58-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="9dc58-118">您可能要为经理角色启用此权限，但不为出纳员角色启用。</span><span class="sxs-lookup"><span data-stu-id="9dc58-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="9dc58-119">单击 **POS 权限组** &gt; **查看打卡时间条目**。</span><span class="sxs-lookup"><span data-stu-id="9dc58-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="9dc58-120">登记时间</span><span class="sxs-lookup"><span data-stu-id="9dc58-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="9dc58-121">出纳员和非出纳员时间登记</span><span class="sxs-lookup"><span data-stu-id="9dc58-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="9dc58-122">在 POS 上：</span><span class="sxs-lookup"><span data-stu-id="9dc58-122">On POS:</span></span>

    - <span data-ttu-id="9dc58-123">上班打卡操作：</span><span class="sxs-lookup"><span data-stu-id="9dc58-123">Clock-in operations:</span></span>

        - <span data-ttu-id="9dc58-124">登录非银箱操作或新班次。</span><span class="sxs-lookup"><span data-stu-id="9dc58-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="9dc58-125">选择打卡时间操作。</span><span class="sxs-lookup"><span data-stu-id="9dc58-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="9dc58-126">选择所需操作：</span><span class="sxs-lookup"><span data-stu-id="9dc58-126">Select a desired operation:</span></span>

            - <span data-ttu-id="9dc58-127">上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-127">Clock-in</span></span>
            - <span data-ttu-id="9dc58-128">工间休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-128">Break for Work</span></span>
            - <span data-ttu-id="9dc58-129">午餐休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-129">Break for Lunch</span></span>
            - <span data-ttu-id="9dc58-130">下班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="9dc58-131">当前状态</span><span class="sxs-lookup"><span data-stu-id="9dc58-131">Current state</span></span></th>
        <th><span data-ttu-id="9dc58-132">可用操作</span><span class="sxs-lookup"><span data-stu-id="9dc58-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="9dc58-133">上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="9dc58-134">工间休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-134">Break for Work</span></span></li>
        <li><span data-ttu-id="9dc58-135">午餐休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="9dc58-136">下班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="9dc58-137">工间休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-137">Break for Work</span></span></td>
        <td><span data-ttu-id="9dc58-138">上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="9dc58-139">午餐休息</span><span class="sxs-lookup"><span data-stu-id="9dc58-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="9dc58-140">上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="9dc58-141">下班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-141">Clock-out</span></span></td>
        <td><span data-ttu-id="9dc58-142">上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="9dc58-143">[![打卡时间状态](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="9dc58-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="9dc58-144">查看确认消息，验证当前活动时间是否正确。</span><span class="sxs-lookup"><span data-stu-id="9dc58-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="9dc58-145">日志：</span><span class="sxs-lookup"><span data-stu-id="9dc58-145">Logbook:</span></span>

    - <span data-ttu-id="9dc58-146">单击**日志**查看打卡时间活动。</span><span class="sxs-lookup"><span data-stu-id="9dc58-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="9dc58-147">使用时间筛选器可选择不同的时间范围。</span><span class="sxs-lookup"><span data-stu-id="9dc58-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="9dc58-148">如果您在多个商店位置工作，可以查看您在那里记录时间的所有商店的时间登记。</span><span class="sxs-lookup"><span data-stu-id="9dc58-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="9dc58-149">可以使用商店筛选器查看所选商店的时间登记。</span><span class="sxs-lookup"><span data-stu-id="9dc58-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="9dc58-150">不同时区：</span><span class="sxs-lookup"><span data-stu-id="9dc58-150">Different time zones:</span></span>

    - <span data-ttu-id="9dc58-151">如果您从不同位置查看时间（用于出纳员日志，或为经理方案使用**查看打卡时间条目**），并且该位置在不同的时区，您看到的时间记录将转换为您本地的时区。</span><span class="sxs-lookup"><span data-stu-id="9dc58-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="9dc58-152">例如，您是两个商店的经理，一个在亚利桑那和另一个在内华达。</span><span class="sxs-lookup"><span data-stu-id="9dc58-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="9dc58-153">出纳员在亚利桑那上午 9:00 上班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="9dc58-154">登记。</span><span class="sxs-lookup"><span data-stu-id="9dc58-154">in Arizona.</span></span> <span data-ttu-id="9dc58-155">此时，该时间是内华达的上午 8:00。</span><span class="sxs-lookup"><span data-stu-id="9dc58-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="9dc58-156">因此，如果您是在内华达商店并查看时间登记记录，时间登记标记为上午 8 点。</span><span class="sxs-lookup"><span data-stu-id="9dc58-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="9dc58-157">查看工作人员时间登记</span><span class="sxs-lookup"><span data-stu-id="9dc58-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="9dc58-158">查看工作人员时间登记，并按商店或活动类型筛选</span><span class="sxs-lookup"><span data-stu-id="9dc58-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="9dc58-159">在 POS 上：</span><span class="sxs-lookup"><span data-stu-id="9dc58-159">On POS:</span></span>

- <span data-ttu-id="9dc58-160">选择**查看打卡时间条目**。</span><span class="sxs-lookup"><span data-stu-id="9dc58-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="9dc58-161">您看到分配到您被分配的同一商店的所有工作人员的打卡时间登记活动。</span><span class="sxs-lookup"><span data-stu-id="9dc58-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="9dc58-162">您可以使用活动类型和商店筛选器筛选时间登记。</span><span class="sxs-lookup"><span data-stu-id="9dc58-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="9dc58-163">处理和管理时间登记</span><span class="sxs-lookup"><span data-stu-id="9dc58-163">Process and manage time registrations</span></span>

<span data-ttu-id="9dc58-164">Commerce 用户按照工作流计算、审核和将时间登记转移到工资单。</span><span class="sxs-lookup"><span data-stu-id="9dc58-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="9dc58-165">主要操作</span><span class="sxs-lookup"><span data-stu-id="9dc58-165">Primary operations</span></span>

- <span data-ttu-id="9dc58-166">计算</span><span class="sxs-lookup"><span data-stu-id="9dc58-166">Calculate</span></span>
- <span data-ttu-id="9dc58-167">批准</span><span class="sxs-lookup"><span data-stu-id="9dc58-167">Approve</span></span>
- <span data-ttu-id="9dc58-168">提交到工资单</span><span class="sxs-lookup"><span data-stu-id="9dc58-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="9dc58-169">其他常用操作</span><span class="sxs-lookup"><span data-stu-id="9dc58-169">Other common operations</span></span>

- <span data-ttu-id="9dc58-170">批量下班打卡</span><span class="sxs-lookup"><span data-stu-id="9dc58-170">Bulk Clock-out</span></span>
- <span data-ttu-id="9dc58-171">登记缺勤</span><span class="sxs-lookup"><span data-stu-id="9dc58-171">Register Absence</span></span>

<span data-ttu-id="9dc58-172">有关如何处理时间和出勤登记的详细信息，请参阅[处理时间和出勤登记](https://technet.microsoft.com/library/aa573180.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9dc58-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
