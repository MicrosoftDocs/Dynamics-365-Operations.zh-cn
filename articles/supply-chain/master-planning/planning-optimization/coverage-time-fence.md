---
title: 覆盖时限
description: 本主题介绍使用计划优化时如何设置覆盖时限。 覆盖时限指示计划范围和限制。
author: ChristianRytt
manager: tfehr
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f970d7aa9f758d3bc35b7a1b9d1e43be928fd250
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033196"
---
# <a name="coverage-time-fences"></a><span data-ttu-id="42013-104">覆盖时限</span><span class="sxs-lookup"><span data-stu-id="42013-104">Coverage time fences</span></span>

<span data-ttu-id="42013-105">本主题介绍使用计划优化时如何设置 *覆盖时限*。</span><span class="sxs-lookup"><span data-stu-id="42013-105">This topic describes how to set up *coverage time fences* when you're using Planning Optimization.</span></span> <span data-ttu-id="42013-106">计划者可以定义计划范围（以天为单位的覆盖时限），并可以排除超出该范围的供应和需求。</span><span class="sxs-lookup"><span data-stu-id="42013-106">Planners can define the planning horizon (the coverage time fence in days), and exclude supply and demand that falls beyond that horizon.</span></span> <span data-ttu-id="42013-107">因此，覆盖时限可以帮助在几个月内阻止您无需作出反应的供应建议引起的“噪音”。</span><span class="sxs-lookup"><span data-stu-id="42013-107">Therefore, coverage time fences help prevent "noise" that is caused by supply suggestions that you don't have to react to for months.</span></span> <span data-ttu-id="42013-108">例如，下一年的预测和距离正常提前期还有很长时间的客户订单。</span><span class="sxs-lookup"><span data-stu-id="42013-108">Examples include next year's forecast and customer orders that are placed far beyond the normal lead time.</span></span>

<span data-ttu-id="42013-109">覆盖时限是今天日期（或更准确地说，是您进行计划运行的日期）之后的天数，不包括供应和需求。</span><span class="sxs-lookup"><span data-stu-id="42013-109">A coverage time fence is the number of days after today's date (or, more precisely, the date when you do the planning run) that supply and demand is excluded.</span></span> <span data-ttu-id="42013-110">为了避免延迟，您必须确保覆盖时限比总提前期长。</span><span class="sxs-lookup"><span data-stu-id="42013-110">To help avoid delays, you must ensure that the coverage time fence is longer that the total lead time.</span></span> <span data-ttu-id="42013-111">系统默认值为 100 天。</span><span class="sxs-lookup"><span data-stu-id="42013-111">The default system value is 100 days.</span></span>

<span data-ttu-id="42013-112">您可以在以下每个级别指定覆盖时限：</span><span class="sxs-lookup"><span data-stu-id="42013-112">You can specify a coverage time fence at each of the following levels:</span></span>

- <span data-ttu-id="42013-113">**覆盖范围组** – 您可以为每个覆盖范围组设置默认的覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-113">**Coverage group** – You can set a default coverage time fence for each coverage group.</span></span>
- <span data-ttu-id="42013-114">**物料覆盖范围** – 您可以替代从分配给物料的覆盖范围组继承的覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-114">**Item coverage** – You can override the coverage time fence that is inherited from the coverage group that is assigned to an item.</span></span>
- <span data-ttu-id="42013-115">**主计划** – 您可以替代从覆盖范围组和物料覆盖范围设置继承的覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-115">**Master plan** – You can override the coverage time fences that are inherited from the coverage group and item coverage settings.</span></span>

<span data-ttu-id="42013-116">以下各节说明如何在每个级别指定覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="42013-116">The following sections explain how to specify a coverage group at each level.</span></span>

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a><span data-ttu-id="42013-117">为覆盖范围组设置覆盖时限</span><span class="sxs-lookup"><span data-stu-id="42013-117">Set a coverage time fence for a coverage group</span></span>

<span data-ttu-id="42013-118">当您为覆盖范围组指定覆盖时限时，设置将应用于属于该组的所有物料（产品）。</span><span class="sxs-lookup"><span data-stu-id="42013-118">When you specify a coverage time fence for a coverage group, the setting applies to all items (products) that belong to that group.</span></span> <span data-ttu-id="42013-119">但是，您可以替代特定物料或特定主计划的设置。</span><span class="sxs-lookup"><span data-stu-id="42013-119">However, you can override the setting for specific items or specific master plans.</span></span>

<span data-ttu-id="42013-120">要为覆盖范围组指定覆盖时限，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="42013-120">To specify a coverage time fence for a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="42013-121">转至 **主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="42013-121">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
1. <span data-ttu-id="42013-122">在列表中选择一个现有的覆盖范围组，或创建一个新的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="42013-122">Select an existing coverage group in the list, or create a new coverage group.</span></span>
1. <span data-ttu-id="42013-123">在 **常规** 快速选项卡上，将 **覆盖时限(以天为单位)** 字段设置为要用作覆盖范围组的覆盖时限的天数。</span><span class="sxs-lookup"><span data-stu-id="42013-123">On the **General** FastTab, set the **Coverage time fence (days)** field to the number of days that you want to use as the coverage time fence for the coverage group.</span></span>

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a><span data-ttu-id="42013-124">为特定物料设置覆盖时限</span><span class="sxs-lookup"><span data-stu-id="42013-124">Set a coverage time fence for a specific item</span></span>

<span data-ttu-id="42013-125">每个物料（产品）属于一个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="42013-125">Every item (product) belongs to a coverage group.</span></span> <span data-ttu-id="42013-126">如果没有明确为物料分配覆盖范围组，将应用默认覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="42013-126">If no coverage group is explicitly assigned to an item, a default coverage group applies.</span></span> <span data-ttu-id="42013-127">每个物料从其覆盖范围组继承覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-127">Every item inherits a coverage time fence from its coverage group.</span></span> <span data-ttu-id="42013-128">但是，您可以根据需要替代特定物料的时限。</span><span class="sxs-lookup"><span data-stu-id="42013-128">However, you can override this time fence for specific items as you require.</span></span>

<span data-ttu-id="42013-129">要为特定物料指定覆盖时限，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="42013-129">To specify a coverage time fence for a specific item, follow these steps.</span></span>

1. <span data-ttu-id="42013-130">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="42013-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="42013-131">在网格中选择一个产品。</span><span class="sxs-lookup"><span data-stu-id="42013-131">Select a product in the grid.</span></span>
1. <span data-ttu-id="42013-132">在操作窗格上，在 **计划** 选项卡上的 **覆盖范围** 组中，选择 **物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="42013-132">On the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage**.</span></span>
1. <span data-ttu-id="42013-133">在 **物料覆盖范围** 页的 **概览** 选项卡上，为要设置覆盖时限的站点选择或创建一行。</span><span class="sxs-lookup"><span data-stu-id="42013-133">On the **Item coverage** page, on the **Overview** tab, select or create a row for the site where you want to set a coverage time fence.</span></span>
1. <span data-ttu-id="42013-134">选择 **常规** 选项卡打开所选站点的设置。</span><span class="sxs-lookup"><span data-stu-id="42013-134">Select the **General** tab to open the settings for the selected site.</span></span>
1. <span data-ttu-id="42013-135">选中 **替代覆盖范围组** 复选框。</span><span class="sxs-lookup"><span data-stu-id="42013-135">Select the **Override coverage group settings** check box.</span></span>
1. <span data-ttu-id="42013-136">将 **覆盖时限(以天为单位)** 字段设置为要用作物料的覆盖时限的天数。</span><span class="sxs-lookup"><span data-stu-id="42013-136">Set the **Coverage time fence (days)** field to the number of days that you want to use as the coverage time fence for the item.</span></span>

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a><span data-ttu-id="42013-137">为特定主计划设置覆盖时限</span><span class="sxs-lookup"><span data-stu-id="42013-137">Set a coverage time fence for a specific master plan</span></span>

<span data-ttu-id="42013-138">您可以在主计划级别指定覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-138">You can specify a coverage time fence at the master plan level.</span></span> <span data-ttu-id="42013-139">这样，您可以定义主计划计算为主计划覆盖的天数。</span><span class="sxs-lookup"><span data-stu-id="42013-139">In this way, you define the number of days that the master planning calculation covers for a master plan.</span></span> <span data-ttu-id="42013-140">此设置将替代为每个相关项目物料和覆盖范围组定义的任何覆盖时间设置。</span><span class="sxs-lookup"><span data-stu-id="42013-140">This setting overrides any coverage time settings that have been defined for each relevant item and coverage group.</span></span>

<span data-ttu-id="42013-141">要为特定主计划指定覆盖时限，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="42013-141">To specify a coverage time fence for a specific master plan, follow these steps.</span></span>

1. <span data-ttu-id="42013-142">转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="42013-142">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="42013-143">在列表中选择一个现有主计划，或创建一个新的主计划。</span><span class="sxs-lookup"><span data-stu-id="42013-143">Select an existing master plan in the list, or create a new master plan.</span></span>
1. <span data-ttu-id="42013-144">在 **按天计算的时限** 快速选项卡上，将 **覆盖范围** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="42013-144">On the **Time fences in days** FastTab, set the **Coverage** option to *Yes*.</span></span> <span data-ttu-id="42013-145">然后，在此选项下的字段中，输入要用作主计划的覆盖时限的天数。</span><span class="sxs-lookup"><span data-stu-id="42013-145">Then, in the field under the option, enter the number of days that you want to use as the coverage time fence for the master plan.</span></span>

## <a name="considerations-for-coverage-time-fences"></a><span data-ttu-id="42013-146">覆盖时限的注意事项</span><span class="sxs-lookup"><span data-stu-id="42013-146">Considerations for coverage time fences</span></span>

<span data-ttu-id="42013-147">在设置覆盖时限时，请考虑以下几点：</span><span class="sxs-lookup"><span data-stu-id="42013-147">As you're setting up coverage time fences, consider the following points:</span></span>

- <span data-ttu-id="42013-148">覆盖时限仅影响主计划的输入数据。</span><span class="sxs-lookup"><span data-stu-id="42013-148">Coverage time fences affect only input data for master planning.</span></span> <span data-ttu-id="42013-149">如果发生延迟，生成的计划订单的日期可能会晚于今天的日期加上覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-149">If delays occur, the resulting planned orders might have a date that is after today's date plus the coverage time fence.</span></span>
- <span data-ttu-id="42013-150">覆盖时限使用日历日指定。</span><span class="sxs-lookup"><span data-stu-id="42013-150">Coverage time fences are specified in calendar days.</span></span> <span data-ttu-id="42013-151">使用工作日的日历不会影响时限的计算。</span><span class="sxs-lookup"><span data-stu-id="42013-151">Calendars that use working days won't affect the time fence calculation.</span></span> <span data-ttu-id="42013-152">例如，一周始终被视为七天，即使在工作时间日历中将周末设置为休息日。</span><span class="sxs-lookup"><span data-stu-id="42013-152">For example, a week is always considered seven days, even if weekends are set up as closed days in the working time calendar.</span></span>
- <span data-ttu-id="42013-153">不会为覆盖时限以外的任何供应和需求生成要求交易。</span><span class="sxs-lookup"><span data-stu-id="42013-153">Requirement transactions won't be generated for any supply and demand that falls outside the coverage time fence.</span></span>
- <span data-ttu-id="42013-154">如果任何批准的供应和需求超出了覆盖时限，则不会将其加载到引擎中。</span><span class="sxs-lookup"><span data-stu-id="42013-154">If any approved supply and demand falls outside the coverage time fence, it won't be loaded into the engine.</span></span> <span data-ttu-id="42013-155">因此，它不会触发任何补货，也不会计算延迟。</span><span class="sxs-lookup"><span data-stu-id="42013-155">Therefore, it won't trigger any replenishment, and delays won't be calculated.</span></span> <span data-ttu-id="42013-156">但是，此供应和需求不应从系统中去除。</span><span class="sxs-lookup"><span data-stu-id="42013-156">Nevertheless, this supply and demand should not be wiped from the system.</span></span>
- <span data-ttu-id="42013-157">如果安全库存数量的变化（从最小键）超出覆盖时限，将被忽略。</span><span class="sxs-lookup"><span data-stu-id="42013-157">Variations in safety stock quantities (from minimum keys) will be ignored if they fall outside the coverage time fence.</span></span>
- <span data-ttu-id="42013-158">如果计算出的要求装运日期不在覆盖时限内，内部公司需求将被忽略。</span><span class="sxs-lookup"><span data-stu-id="42013-158">Intercompany demand will be ignored if the requested ship date that is calculated isn't inside the coverage time fence.</span></span> <span data-ttu-id="42013-159">请注意，对于内置主计划，内部公司需求不受覆盖时限的限制。</span><span class="sxs-lookup"><span data-stu-id="42013-159">Note that, for built-in master planning, intercompany demand isn't limited by the coverage time fence.</span></span>
- <span data-ttu-id="42013-160">如果预算日期不在覆盖时限内，需求预测将被忽略。</span><span class="sxs-lookup"><span data-stu-id="42013-160">Demand forecasts will be ignored if the budget date isn't inside the coverage time fence.</span></span> <span data-ttu-id="42013-161">请注意，对于内置主计划，需求预测不受覆盖时限的限制。</span><span class="sxs-lookup"><span data-stu-id="42013-161">Note that, for built-in master planning, demand forecasts aren't limited by the coverage time fence.</span></span>
- <span data-ttu-id="42013-162">计划优化可以识别时区。</span><span class="sxs-lookup"><span data-stu-id="42013-162">Planning Optimization is time zone–aware.</span></span> <span data-ttu-id="42013-163">它会考虑供应和需求站点的时区以及计划运行的时间。</span><span class="sxs-lookup"><span data-stu-id="42013-163">It considers the time zone at the supply and demand sites, and the time of the planning run.</span></span> <span data-ttu-id="42013-164">例如，主计划在 10 月 15 日上午 11 点从丹麦（GMT+1 时区）的某个站点触发，使用十天覆盖时限。</span><span class="sxs-lookup"><span data-stu-id="42013-164">For example, master planning is triggered at 11 AM on October 15 from a site in Denmark (GMT+1 time zone), and a coverage time fence of ten days is used.</span></span> <span data-ttu-id="42013-165">在这种情况下，西雅图的某个站点（GMT-8 时区）的供应和需求将被包括在内，直到 10 月 25 日凌晨 2 点（=主计划触发后十个 24 小时日减去九小时的时差）。</span><span class="sxs-lookup"><span data-stu-id="42013-165">In this case, supply and demand from a site in Seattle (GMT-8 time zone) is included until 2 AM on October 25 (= ten 24-hour days after master planning was triggered, minus the time zone difference of nine hours).</span></span> <span data-ttu-id="42013-166">请注意，内置主计划引擎仅考虑时限的日期。</span><span class="sxs-lookup"><span data-stu-id="42013-166">Note that the built-in master planning engine considers only the date of the time fence.</span></span> <span data-ttu-id="42013-167">因此，结果可能不同。</span><span class="sxs-lookup"><span data-stu-id="42013-167">Therefore, the result can differ.</span></span>
