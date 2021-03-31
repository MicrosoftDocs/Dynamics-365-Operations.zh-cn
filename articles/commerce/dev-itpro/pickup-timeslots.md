---
title: 创建和更新客户提货时隙
description: 此主题介绍如何在 Commerce Headquarters 中创建、配置和更新客户提货时隙。
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 6dc2be8a6f62ce13068ce2242f92ef17830c2447
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205739"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a><span data-ttu-id="93aa5-103">创建和更新客户提货时隙</span><span class="sxs-lookup"><span data-stu-id="93aa5-103">Create and update time slots for customer pickup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93aa5-104">此主题介绍如何在 Commerce Headquarters 中创建、配置和更新客户提货时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-104">This topic describes how to create, configure, and update customer pickup time slots in Commerce headquarters.</span></span>

<span data-ttu-id="93aa5-105">时隙功能让零售商可以为打开客户提货交货方式的物料定义时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-105">The time slot feature gives retailers a way to define a time slot for items that the customer pickup delivery mode is turned on for.</span></span> <span data-ttu-id="93aa5-106">时隙让零售商可以定义可以从商店提货的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="93aa5-106">Time slots let retailers define the days and times when orders can be picked up from a store.</span></span> <span data-ttu-id="93aa5-107">零售商还可以定义可以在给定期间内提货的订单数量。</span><span class="sxs-lookup"><span data-stu-id="93aa5-107">Retailers can also define the number of orders that can be picked up during a given period.</span></span> <span data-ttu-id="93aa5-108">通过这种方式，零售商可以限制可以在给定日期和给定时间提货的订单数量。</span><span class="sxs-lookup"><span data-stu-id="93aa5-108">In this way, retailers can limit the number of orders that can be picked up on a given day and at a given time.</span></span> <span data-ttu-id="93aa5-109">结果是为其客户提供更高质量的体验。</span><span class="sxs-lookup"><span data-stu-id="93aa5-109">The result is a better-quality experience for their customers.</span></span>

> [!NOTE]
> <span data-ttu-id="93aa5-110">时隙功能在 Microsoft Dynamics 365 Commerce 版本 10.0.15 和更高版本中提供。</span><span class="sxs-lookup"><span data-stu-id="93aa5-110">The time slot feature is available in Microsoft Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="93aa5-111">下图显示了在电子商务结帐期间选择时隙的示例。</span><span class="sxs-lookup"><span data-stu-id="93aa5-111">The following illustration shows an example of time slot selection during e-commerce checkout.</span></span>

![电子商务结帐期间选择时隙的示例](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a><span data-ttu-id="93aa5-113">时隙属性</span><span class="sxs-lookup"><span data-stu-id="93aa5-113">Time slot properties</span></span>

<span data-ttu-id="93aa5-114">时隙是客户可以选择从特定商店或位置提货的特定间隔。</span><span class="sxs-lookup"><span data-stu-id="93aa5-114">A time slot is a specific interval when a customer can choose to pick up an order from a specific store or location.</span></span> <span data-ttu-id="93aa5-115">只有在 Dynamics 365 Commerce 中配置了客户提货交货方式时，时隙管理功能才可用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-115">The time slot management feature is available only when the customer pickup delivery mode is configured in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="93aa5-116">时隙使用以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="93aa5-116">A time slot is defined by using the following properties:</span></span>

- <span data-ttu-id="93aa5-117">**交货方式** – 指定应用时隙的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="93aa5-117">**Mode of delivery** – Specify the pickup mode of delivery that the time slot applies to.</span></span>
- <span data-ttu-id="93aa5-118">**最少天数** 和 **最多天数** – 指定相对于下订单日期可以选择提货的最早和最晚日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-118">**Minimum Days** and **Maximum Days** – Specify the earliest and latest dates that can be selected for pickup relative to the date when the order is placed.</span></span> 

    <span data-ttu-id="93aa5-119">**最少天数** 属性确保零售商在提货之前有足够的时间处理订单来为提货准备好订单。</span><span class="sxs-lookup"><span data-stu-id="93aa5-119">The **Minimum Days** property ensures that there is enough time for the retailer to process the order before it's ready for pickup.</span></span> <span data-ttu-id="93aa5-120">**最多天数** 属性确保用户不能选择距离现在太远的将来日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-120">The **Maximum Days** property ensures that the user can't select a date that is too far in the future.</span></span> <span data-ttu-id="93aa5-121">例如，如果最小值设置为 **1**，下订单的日期是 9 月 20 日，订单可以提货的最早日期是下一个合格日期（9 月 21 日）。</span><span class="sxs-lookup"><span data-stu-id="93aa5-121">For example, if the minimum value is set to **1**, and an order is placed on September 20, the earliest day that the order will be available for pickup is the next eligible day (September 21).</span></span> <span data-ttu-id="93aa5-122">以类似的方式，通过设置最大值，您可以定义可以提取订单的最大天数。</span><span class="sxs-lookup"><span data-stu-id="93aa5-122">In a similar way, by setting a maximum value, you can define the maximum number of days that an order can be picked up.</span></span> <span data-ttu-id="93aa5-123">定义最小值和最大值后，站点用户在结帐期间只能看到和选择一组特定日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-123">When minimum and maximum values are defined, site users can see and select only a specific set of days during their checkout experience.</span></span>

    <span data-ttu-id="93aa5-124">您可以将最小值设置为小于 1 的十进制值。</span><span class="sxs-lookup"><span data-stu-id="93aa5-124">You can set the minimum value to a decimal value that is less than 1.</span></span> <span data-ttu-id="93aa5-125">例如，如果下订单之后四个小时可以提货，应将最小值设置为 **0.17**（= 4÷24，四舍五入到小数点后两位）。</span><span class="sxs-lookup"><span data-stu-id="93aa5-125">For example, if pickup is available four hours after an order is placed, set the minimum value to **0.17** (= 4 ÷ 24, rounded up to two decimal places).</span></span> <span data-ttu-id="93aa5-126">但是，如果将最小值设置为大于 1 的十进制值，值始终会向上舍入到最接近的整数。</span><span class="sxs-lookup"><span data-stu-id="93aa5-126">However, if you set the minimum value to a decimal value that is more than 1, it's always rounded up to the nearest whole number.</span></span> <span data-ttu-id="93aa5-127">例如，值 **1.2** 将向上舍入到 **2**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-127">For example, a value of **1.2** will be rounded up to **2**.</span></span> <span data-ttu-id="93aa5-128">同样，如果将最大值设置为一个十进制值，值也始终会向上舍入到最接近的整数。</span><span class="sxs-lookup"><span data-stu-id="93aa5-128">Similarly, if you set the maximum value to a decimal value, it's always rounded up to the nearest whole number.</span></span> 

- <span data-ttu-id="93aa5-129">**开始日期** 和 **结束日期** – 指定时隙的开始和结束日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-129">**Start Date** and **End Date** – Specify the start and end dates of the time slot.</span></span> <span data-ttu-id="93aa5-130">每个时隙条目都有开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-130">Each time slot entry has a start date and an end date.</span></span> <span data-ttu-id="93aa5-131">因此，您可以灵活地在全年中添加不同的时隙（例如，假日期间提货）。</span><span class="sxs-lookup"><span data-stu-id="93aa5-131">Therefore, you have the flexibility to add different time slots throughout the year (for example, pickups during holiday hours).</span></span> <span data-ttu-id="93aa5-132">如果下订单后更改了时隙的开始日期，更改不会应用于该订单。</span><span class="sxs-lookup"><span data-stu-id="93aa5-132">If a time slot's start and dates are changed after an order is placed, the changes won't apply to that order.</span></span> <span data-ttu-id="93aa5-133">在定义开始日期和结束日期时，必须考虑商店歇业日期（例如，圣诞节），应确保不要为那些日期定义时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-133">When you define start and end dates, you must consider store closure dates (for example, Christmas day) and ensure that time slots aren't defined for those days.</span></span>
- <span data-ttu-id="93aa5-134">**有效提货时间** – 指定允许提货的时间段。</span><span class="sxs-lookup"><span data-stu-id="93aa5-134">**Active Hours of Pickup** – Specify the period when pickup is allowed.</span></span> <span data-ttu-id="93aa5-135">例如，每天的提货时间可以在下午 2 点到 5 点之间。</span><span class="sxs-lookup"><span data-stu-id="93aa5-135">For example, the pickup times might be between 2 PM and 5 PM every day.</span></span> <span data-ttu-id="93aa5-136">此属性让提货时间可以不受商店营业时间的影响。</span><span class="sxs-lookup"><span data-stu-id="93aa5-136">This property enables the pickup times to be independent of store hours.</span></span> <span data-ttu-id="93aa5-137">因此，零售商可以配置满足其特定业务要求的提货时间。</span><span class="sxs-lookup"><span data-stu-id="93aa5-137">Therefore, the retailer can configure pickup times that meet its specific business requirements.</span></span> <span data-ttu-id="93aa5-138">定义有效提货时间时，必须考虑商店营业时间，确保没有将商店关门后的时间定义为提货时间。</span><span class="sxs-lookup"><span data-stu-id="93aa5-138">When you define the active hours of pickup, you must consider store hours and ensure that pickup times aren't defined for times when the store is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="93aa5-139">商店提货时间必须使用相应商店的时区定义。</span><span class="sxs-lookup"><span data-stu-id="93aa5-139">The hours for store pickup must be defined in the time zone of the appropriate store.</span></span>

- <span data-ttu-id="93aa5-140">**时隙间隔** – 指定可以分配给每个时隙的持续时间。</span><span class="sxs-lookup"><span data-stu-id="93aa5-140">**Time Slot Interval** – Specify the duration that can be allotted to each time slot.</span></span> <span data-ttu-id="93aa5-141">例如，每个时隙的持续时间可以以 15 分钟、30 分钟或一个小时为增量。</span><span class="sxs-lookup"><span data-stu-id="93aa5-141">For example, the duration of each time slot might be in increments of 15 minutes, 30 minutes, or one hour.</span></span> <span data-ttu-id="93aa5-142">如果时隙值为 0，该时隙在开始时间和结束时间之间的整个持续时间内都可用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-142">If time slot value is 0, the time slot is available for the entire duration between the start and end time.</span></span>
- <span data-ttu-id="93aa5-143">**每间隔时隙** – 指定每个时隙间隔内可以提货的客户或订单数量。</span><span class="sxs-lookup"><span data-stu-id="93aa5-143">**Slots Per Interval** – Specify the number of customer or orders that can be served for pickup during each time slot interval.</span></span> <span data-ttu-id="93aa5-144">例如，输入 **1**、**2**、**3** 或任何其他整数。</span><span class="sxs-lookup"><span data-stu-id="93aa5-144">For example, enter **1**, **2**, **3**, or any other whole number.</span></span>
- <span data-ttu-id="93aa5-145">**有效日期** – 指定提货时隙在一周的哪一天有效。</span><span class="sxs-lookup"><span data-stu-id="93aa5-145">**Active Days** – Specify the days of the week when the pickup time slots are active.</span></span> <span data-ttu-id="93aa5-146">此属性让零售商可以定义要支持提供订单的日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-146">This property lets the retailer define the days when it wants to support pickup orders.</span></span>
- <span data-ttu-id="93aa5-147">**零售渠道** – 指定零售渠道。</span><span class="sxs-lookup"><span data-stu-id="93aa5-147">**Retail Channels** – Specify the retail channels.</span></span> <span data-ttu-id="93aa5-148">每个时隙可以与一个或多个零售商店关联。</span><span class="sxs-lookup"><span data-stu-id="93aa5-148">Each time slot can be associated with one or more retail stores.</span></span> <span data-ttu-id="93aa5-149">根据每个商店的营业时间，可以创建一个或多个时隙条目并将其与渠道关联。</span><span class="sxs-lookup"><span data-stu-id="93aa5-149">Depending on each store's hours of operation, one or more time slot entries can be created and associated with a channel.</span></span> 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

<span data-ttu-id="93aa5-150">每个渠道只能配置一个时隙模板。</span><span class="sxs-lookup"><span data-stu-id="93aa5-150">Only one time slot template can be configured per channel.</span></span> <span data-ttu-id="93aa5-151">这些渠道包括实体商店、呼叫中心、移动设备和电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="93aa5-151">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a><span data-ttu-id="93aa5-152">在 Commerce headquarters 中配置时隙功能</span><span class="sxs-lookup"><span data-stu-id="93aa5-152">Configure the time slot feature in Commerce headquarters</span></span>

<span data-ttu-id="93aa5-153">必须在 Commerce headquarters 中为每种提货交货方式定义时隙，销售点 (POS) 和电子商务渠道才能够进行引用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-153">Time slots must be defined for each pickup mode of delivery in Commerce headquarters, so that point of sale (POS) and e-commerce channels can reference them.</span></span>

- <span data-ttu-id="93aa5-154">每个商店或渠道只能与一个时隙模板关联。</span><span class="sxs-lookup"><span data-stu-id="93aa5-154">Only one time slot template can be associated with each store or channel.</span></span>
- <span data-ttu-id="93aa5-155">创建的每个时隙对于每个模板中的每个交货方式应该是唯一的。</span><span class="sxs-lookup"><span data-stu-id="93aa5-155">Each time slot that is created should be unique to each delivery mode in each template.</span></span>
- <span data-ttu-id="93aa5-156">配置时隙功能后，时隙日历将对所选商店或商店组可用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-156">After the time slot feature is configured, the time slot calendar will be available to the selected stores or store groups.</span></span> <span data-ttu-id="93aa5-157">它还会在 POS 上可见，供用户引用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-157">It will also be visible at the POS, for reference.</span></span>

<span data-ttu-id="93aa5-158">要在 Commerce headquarters 中配置时隙功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="93aa5-158">To configure the time slot feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="93aa5-159">转到 **Commerce** \> **渠道设置** \> **商店提货时隙**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-159">Go to **Commerce** \> **Channel setup** \> **Store pickup time slot**.</span></span>
1. <span data-ttu-id="93aa5-160">选择 **新建** 创建新时隙模板。</span><span class="sxs-lookup"><span data-stu-id="93aa5-160">Select **New** to create a new time slot template.</span></span> <span data-ttu-id="93aa5-161">若要使用现有模板，请在左窗格中选择模板。</span><span class="sxs-lookup"><span data-stu-id="93aa5-161">To use an existing template, select the template in the left pane.</span></span>
1. <span data-ttu-id="93aa5-162">在 **时隙 ID** 和 **说明** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="93aa5-162">Enter values in the **Time Slot ID** and **Description** fields.</span></span>
1. <span data-ttu-id="93aa5-163">在 **订单提货 - 时间设置** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-163">On the **Order Pickup - Time Settings** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="93aa5-164">在 **订单提货 - 时间设置** 对话框中，定义日期范围、交货方式、交货有效时间、有效日期、时隙间隔、每个间隔的时隙以及其他设置。</span><span class="sxs-lookup"><span data-stu-id="93aa5-164">In the **Order Pickup - Time Settings** dialog box, define the date range, mode of delivery, active hours of delivery, active days, time slot interval, slots per interval, and other settings.</span></span>

    <span data-ttu-id="93aa5-165">如果在可预见的将来时隙是静态的，将 **结束日期** 字段设置为 **从不**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-165">If time slots will be static for the foreseeable future, set the **End Date** field to **Never**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="93aa5-166">您可以创建多个模板，但只有一个模板可以与一个渠道或商店关联。</span><span class="sxs-lookup"><span data-stu-id="93aa5-166">You can create multiple templates, but only one template can be associated with a single channel or store.</span></span>

    ![“订单提货 - 时间设置”对话框](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. <span data-ttu-id="93aa5-168">当您完成时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-168">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="93aa5-169">如果一天中的时隙会变化，请在 **订单提货 - 时间设置** 快速选项卡上创建其他条目，以确保日期和时间不会重叠。</span><span class="sxs-lookup"><span data-stu-id="93aa5-169">If the time slots in a day will vary, create additional entries on the **Order Pickup - Time Settings** FastTab to ensure that the dates and times don't overlap.</span></span>
1. <span data-ttu-id="93aa5-170">在 **零售渠道** 快速选项卡上，选择 **添加** 将时隙模板与将使用该模板的商店或渠道关联。</span><span class="sxs-lookup"><span data-stu-id="93aa5-170">On the **Retail Channels** FastTab, select **Add** to associate the time slot template with the stores or channels where it will be used.</span></span>
1. <span data-ttu-id="93aa5-171">在 **选择组织节点** 对话框中，使用箭头按钮选择（或清除选择）应与模板关联的商店、地区和组织。</span><span class="sxs-lookup"><span data-stu-id="93aa5-171">In the **Choose organization nodes** dialog box, use the arrow buttons to select (or clear the selection of) the stores, regions, and organizations that the template should be associated with.</span></span>

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. <span data-ttu-id="93aa5-172">当您完成时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="93aa5-172">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="93aa5-173">在 **配送计划** 页，运行 **1070** 和 **1135** 作业将数据与渠道同步。</span><span class="sxs-lookup"><span data-stu-id="93aa5-173">On the **Distribution schedule** page, run the **1070** and **1135** jobs to sync the data to the channels.</span></span>

## <a name="time-slot-selection-for-pos-orders"></a><span data-ttu-id="93aa5-174">POS 订单的时隙选择</span><span class="sxs-lookup"><span data-stu-id="93aa5-174">Time slot selection for POS orders</span></span>

<span data-ttu-id="93aa5-175">在 POS，当订单或订单行标识要提货时，出纳可以选择提货商店或位置以及日期和时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-175">At the POS, when an order or order line is identified for pickup, the cashier can select the pickup store or location, and a date and time slot.</span></span> <span data-ttu-id="93aa5-176">如果客户有其他商店的提货单，收银员可以选择该商店的可提货日期。</span><span class="sxs-lookup"><span data-stu-id="93aa5-176">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="93aa5-177">商店查找将提供对日期和商店营业时间的引用。</span><span class="sxs-lookup"><span data-stu-id="93aa5-177">The store lookup will provide a reference to the dates and store times.</span></span>

<span data-ttu-id="93aa5-178">下图显示了 POS 订单的时隙选择的示例。</span><span class="sxs-lookup"><span data-stu-id="93aa5-178">The following illustration shows an example of time slot selection for a POS order.</span></span>

![POS 订单的时隙选择示例](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a><span data-ttu-id="93aa5-180">电子商务订单的时隙选择</span><span class="sxs-lookup"><span data-stu-id="93aa5-180">Time slot selection for e-commerce orders</span></span>

<span data-ttu-id="93aa5-181">有关如何让时隙选择对电子商务订单可用的信息，请参阅[提货信息模块](../pickup-info-module.md)。</span><span class="sxs-lookup"><span data-stu-id="93aa5-181">For information about how to make time slot selection available for e-commerce orders, see [Pickup information module](../pickup-info-module.md).</span></span>

> [!NOTE]
> <span data-ttu-id="93aa5-182">仅当提货信息模块已添加到该页面时，用户才能在 Commerce 站点的结帐页面查看或编辑提货时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-182">Users can view or edit pickup time slots on a Commerce site's checkout page only if the pickup information module has been added to that page.</span></span> <span data-ttu-id="93aa5-183">如果结帐页面不包含提货信息模块，下订单时不会让用户指定或查看时隙信息。</span><span class="sxs-lookup"><span data-stu-id="93aa5-183">If the checkout page doesn't include the pickup information module, orders will be placed without letting users specify or view time slot information.</span></span>

<span data-ttu-id="93aa5-184">下图显示了一个已选择提货时隙的电子商务订单的示例。</span><span class="sxs-lookup"><span data-stu-id="93aa5-184">The following illustration shows an example of an e-commerce order where a pickup time slot has been selected.</span></span>

![已选择提货时隙的电子商务订单的示例](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a><span data-ttu-id="93aa5-186">呼叫中心订单的时隙选择</span><span class="sxs-lookup"><span data-stu-id="93aa5-186">Time slot selection for call center orders</span></span>

<span data-ttu-id="93aa5-187">在呼叫中心应用中，呼叫中心代理可以选择提货商店或位置，以及下图中突出显示的日期和时隙。</span><span class="sxs-lookup"><span data-stu-id="93aa5-187">In the call center app, call center agents can select the pickup store or location, as well as a date and time slot as highlighted in the following illustration.</span></span>

![已选择提货时隙的呼叫中心订单的示例](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a><span data-ttu-id="93aa5-189">其他资源</span><span class="sxs-lookup"><span data-stu-id="93aa5-189">Additional resources</span></span>

[<span data-ttu-id="93aa5-190">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="93aa5-190">Pickup information module</span></span>](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]