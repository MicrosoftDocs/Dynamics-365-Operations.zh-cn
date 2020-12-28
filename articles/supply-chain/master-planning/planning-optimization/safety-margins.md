---
title: 安全宽限期
description: 本主题介绍如何对适用于 Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项使用安全宽限期。
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8ab5f1c3cdfa990a73951ddc5a7469644954d5c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422871"
---
# <a name="safety-margins"></a><span data-ttu-id="f9085-103">安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9085-104">本主题介绍如何对适用于 Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项使用安全宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="f9085-105">安全宽限期概述</span><span class="sxs-lookup"><span data-stu-id="f9085-105">Safety margins overview</span></span>

<span data-ttu-id="f9085-106">安全宽限期的用途是启用设置以提供比正常提前期更长的一些缓冲时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="f9085-107">例如，如果在供应商的物料到达后必须拆开物料的包装或检查物料，则不能仅向购买提前期添加额外时间，因为这种方法将为提供商提供额外缓冲时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="f9085-108">在此示例中，可以使用收货宽限期确保供应商提早交货。</span><span class="sxs-lookup"><span data-stu-id="f9085-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="f9085-109">这种方法提供了缓冲时间，以便在内部处理货物。</span><span class="sxs-lookup"><span data-stu-id="f9085-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="f9085-110">安全宽限期有三种类型：</span><span class="sxs-lookup"><span data-stu-id="f9085-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="f9085-111">**再订购宽限期** – 用于下达供应订单的缓冲时间</span><span class="sxs-lookup"><span data-stu-id="f9085-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="f9085-112">**收货宽限期** – 用于处理传入供应的缓冲时间</span><span class="sxs-lookup"><span data-stu-id="f9085-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="f9085-113">**发货宽限期** – 用于处理装运的缓冲时间</span><span class="sxs-lookup"><span data-stu-id="f9085-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="f9085-114">下图显示这些安全宽限期在一段时间的应用情况。</span><span class="sxs-lookup"><span data-stu-id="f9085-114">The following illustration shows how these safety margins apply over time.</span></span>

![安全宽限期](media/safety-margins-1.png)

<span data-ttu-id="f9085-116">所有宽限期均以天为单位定义。</span><span class="sxs-lookup"><span data-stu-id="f9085-116">All margins are defined in days.</span></span> <span data-ttu-id="f9085-117">默认值 *0*（零）表示不应用宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="f9085-118">如果设置多个宽限期，这些宽限期将全部添加到从供应 *订单日期* 到需求 *要求日期* 的总时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="f9085-119">例如，某个设置没有提前期，并且所有三种宽限期都设置为一天。</span><span class="sxs-lookup"><span data-stu-id="f9085-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="f9085-120">在这种情况下，供应订单日期和需求要求日期之间将相隔三天，因此，如果订单日期为 7 月 1 日，则要求日期将为 7 月 4 日。</span><span class="sxs-lookup"><span data-stu-id="f9085-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="f9085-121">收货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-121">Receipt margin</span></span>

<span data-ttu-id="f9085-122">收货宽限期可能是这三种安全宽限期中最常用的。</span><span class="sxs-lookup"><span data-stu-id="f9085-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="f9085-123">其应用于 *交货日期*，并从 *要求日期* 向后推。</span><span class="sxs-lookup"><span data-stu-id="f9085-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="f9085-124">换句话说，产品的接收日期应该比其需求日期早指定的收货宽限期天数。</span><span class="sxs-lookup"><span data-stu-id="f9085-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="f9085-125">下图突出显示了收货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-125">The following illustration highlights the receipt margin.</span></span>

![收货宽限期](media/safety-margins-2.png)

<span data-ttu-id="f9085-127">收货宽限期通常用作缓冲来确保仓库等记或系统中不作为常规提前期一部分捕获的其他耗时流程提供时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="f9085-128">对于采购来说，其中一个优点是采购订单的 *计划日期* 相应向前推。</span><span class="sxs-lookup"><span data-stu-id="f9085-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="f9085-129">如果增加提前期而不是使用安全宽限期，仍然会请供应商在最后一分钟交货。</span><span class="sxs-lookup"><span data-stu-id="f9085-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="f9085-130">请注意，收货宽限期不会改变供应的 *要求日期*。</span><span class="sxs-lookup"><span data-stu-id="f9085-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="f9085-131">因此，比较需求和供应的要求日期时（例如，在 **净要求** 页面中），不会直接显示收货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="f9085-132">例如，如果将收货宽限期设置为四天，而采购订单行计划在该月的第十五天收货，则主计划编制期间将对收货日期做出相应的调整，使得最终算出的收货日期为该月的第十九天。</span><span class="sxs-lookup"><span data-stu-id="f9085-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="f9085-133">请注意，在将现有库存用作供应时，不应用收货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="f9085-134">无论现有库存实际是在何时收到的，都将把所有现有库存视为立即可用。</span><span class="sxs-lookup"><span data-stu-id="f9085-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="f9085-135">再订购宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="f9085-136">**即将推出：** 计划优化尚不支持此功能。</span><span class="sxs-lookup"><span data-stu-id="f9085-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="f9085-137">在支持之前，将把为 **再订购宽限期添加到物料提前期** 输入的所有值视为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="f9085-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="f9085-138">下图突出显示了再订购宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-138">The following illustration highlights the reorder margin.</span></span>

![再订购宽限期](media/safety-margins-3.png)

<span data-ttu-id="f9085-140">再订购宽限期在主计划期间所有计划订单的物料提前期之前添加。</span><span class="sxs-lookup"><span data-stu-id="f9085-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="f9085-141">因此，确保了为下达供应订单提供额外时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="f9085-142">此宽限期通常用作缓冲来确保为创建供应订单期间所需审批流程或其他内部流程提供时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="f9085-143">再订购宽限期介于供应 *订单日期* 和 *开始日期* 之间。</span><span class="sxs-lookup"><span data-stu-id="f9085-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="f9085-144">发货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="f9085-145">**即将推出：** 计划优化尚不支持此功能。</span><span class="sxs-lookup"><span data-stu-id="f9085-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="f9085-146">在支持之前，将把为 **从要求日期扣除的发货宽限期** 输入的所有值视为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="f9085-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="f9085-147">下图突出显示了发货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-147">The following illustration highlights the issue margin.</span></span>

![发货宽限期](media/safety-margins-4.png)

<span data-ttu-id="f9085-149">主计划期间将从需求要求日期扣除发货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="f9085-150">这有助于确保有时间处理和装运传入的需求订单。</span><span class="sxs-lookup"><span data-stu-id="f9085-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="f9085-151">此宽限期通常用作缓冲区来确保为装运和相关传出仓库流程提供时间。</span><span class="sxs-lookup"><span data-stu-id="f9085-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="f9085-152">请注意，如果应用发货宽限期，则相关供应日期和需求要求日期不匹配。</span><span class="sxs-lookup"><span data-stu-id="f9085-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="f9085-153">相反，它们在发货宽限期方面存在不同，因为发货宽限期添加在供应 *要求日期* 和需求 *要求日期* 之间。</span><span class="sxs-lookup"><span data-stu-id="f9085-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="f9085-154">设置安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="f9085-155">在功能管理中开启安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="f9085-156">此功能只有在系统中开启之后才能用于计划优化。</span><span class="sxs-lookup"><span data-stu-id="f9085-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="f9085-157">管理员可以使用[功能管理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="f9085-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f9085-158">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="f9085-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f9085-159">**模块**：_主计划_</span><span class="sxs-lookup"><span data-stu-id="f9085-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="f9085-160">**功能名称**：_计划优化的宽限期_</span><span class="sxs-lookup"><span data-stu-id="f9085-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="f9085-161">定义安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-161">Define safety margins</span></span>

<span data-ttu-id="f9085-162">安全宽限期的设置非常灵活。</span><span class="sxs-lookup"><span data-stu-id="f9085-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="f9085-163">*覆盖范围组* 和 *主计划* 中都可以设置。</span><span class="sxs-lookup"><span data-stu-id="f9085-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="f9085-164">请务必了解宽限期彼此叠加。</span><span class="sxs-lookup"><span data-stu-id="f9085-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="f9085-165">例如，覆盖范围组中为期两天的收货宽限期和主计划中的三天加起来为五天的有效收货宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="f9085-166">如果希望模拟特定计划的更长提前期或不确定性，同时不影响日常计划，则在主计划中设置宽限期这一功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="f9085-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="f9085-167">覆盖范围组安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-167">Coverage group safety margins</span></span>

<span data-ttu-id="f9085-168">若要对覆盖范围组应用安全宽限期，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f9085-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="f9085-169">转至 **主计划 \> 设置 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="f9085-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="f9085-170">在列表窗格中，选择所需的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="f9085-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="f9085-171">在 **其他** 快速选项卡的 **安全宽限期(天)** 部分中，使用以下字段设置所需的安全宽限期（以天为单位）：</span><span class="sxs-lookup"><span data-stu-id="f9085-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="f9085-172">添加到需求日期的收货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="f9085-173">从需求日期扣除的发货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="f9085-174">已添加到物料提前期的再订购宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="f9085-175">主计划安全宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-175">Master plan safety margins</span></span>

<span data-ttu-id="f9085-176">若要对主计划应用安全宽限期，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f9085-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="f9085-177">转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="f9085-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="f9085-178">在列表窗格中，选择所需的主计划。</span><span class="sxs-lookup"><span data-stu-id="f9085-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="f9085-179">在 **安全宽限期(天)** 快速选项卡中，使用以下字段设置所需的安全宽限期（以天为单位）：</span><span class="sxs-lookup"><span data-stu-id="f9085-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="f9085-180">添加到需求日期的收货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="f9085-181">从需求日期扣除的发货宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="f9085-182">已添加到物料提前期的再订购宽限期</span><span class="sxs-lookup"><span data-stu-id="f9085-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="f9085-183">定义计算基于日历日还是工作日</span><span class="sxs-lookup"><span data-stu-id="f9085-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="f9085-184">可以设置所有安全宽限期，以便基于日历日或工作日进行计算。</span><span class="sxs-lookup"><span data-stu-id="f9085-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="f9085-185">转到 **主计划 \> 设置 \> 主计划参数**。</span><span class="sxs-lookup"><span data-stu-id="f9085-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="f9085-186">在 **常规** 选项卡的 **安全宽限期(天)** 部分中，将 **工作日** 选项设置为 *是* 以基于工作日计算宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="f9085-187">将选项设置为 *否* 则根据日历日计算宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="f9085-188">例如，日历在星期一到星期五打开，在星期六到星期日关闭。</span><span class="sxs-lookup"><span data-stu-id="f9085-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="f9085-189">如果收货宽限期为一天，则星期一的要求日期生成前一个星期五的交货日期，因为星期六和星期日不是工作日。</span><span class="sxs-lookup"><span data-stu-id="f9085-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="f9085-190">用于确定工作日的日历取决于设置和供应类型。</span><span class="sxs-lookup"><span data-stu-id="f9085-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="f9085-191">可以由覆盖范围组的日历、仓库和供应商控制。</span><span class="sxs-lookup"><span data-stu-id="f9085-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="f9085-192">如果覆盖范围维度中不包含 *仓库*（即计划仅基于 *站点*），则不使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="f9085-193">系统可以处理定义了一个或多个日历的设置。</span><span class="sxs-lookup"><span data-stu-id="f9085-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="f9085-194">以下小节介绍可用于控制结果的组合。</span><span class="sxs-lookup"><span data-stu-id="f9085-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="f9085-195">用于持续时间的日历</span><span class="sxs-lookup"><span data-stu-id="f9085-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="f9085-196">定义的日历控制日历日中从供应订单日期到需求要求日期的实际总提前期。</span><span class="sxs-lookup"><span data-stu-id="f9085-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="f9085-197">将使用以下日历优先级：</span><span class="sxs-lookup"><span data-stu-id="f9085-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="f9085-198">**采购提前期** – 仅考虑覆盖范围组日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="f9085-199">**收货宽限期** – 使用覆盖范围组日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-200">否则，会使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="f9085-201">**发货宽限期** – 使用覆盖范围组日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-202">否则，会使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="f9085-203">**订单提前期** – 仅考虑覆盖范围组日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="f9085-204">用于结束日期的日历</span><span class="sxs-lookup"><span data-stu-id="f9085-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="f9085-205">将应用以下规则以确定计划引擎是否可对给定日期类型使用给定日期：</span><span class="sxs-lookup"><span data-stu-id="f9085-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="f9085-206">**采购收货日期** – 使用供应商日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-207">否则，使用覆盖范围组日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-208">如果未定义这两个日历中的任何一个，则使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="f9085-209">**转移收货日期** – 使用覆盖范围组日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-210">否则，会使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="f9085-211">**生产收货日期** – 使用覆盖范围组日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-212">否则，会使用仓库日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="f9085-213">**需求发货开始日期** – 使用仓库日历（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="f9085-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="f9085-214">否则，使用覆盖范围组日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="f9085-215">**订单开始日期** – 使用覆盖范围组日历和供应商日历的组合（交集）。</span><span class="sxs-lookup"><span data-stu-id="f9085-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="f9085-216">必须打开这两种日历才能使用该日期。</span><span class="sxs-lookup"><span data-stu-id="f9085-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="f9085-217">如果仅定义这些日历中的一个，则单独使用该日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="f9085-218">日历设置概览矩阵</span><span class="sxs-lookup"><span data-stu-id="f9085-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="f9085-219">下图提供矩阵来汇总计算安全宽限期时应用哪些日历。</span><span class="sxs-lookup"><span data-stu-id="f9085-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="f9085-220">（选择图像打开其高分辨率版本。）以下缩写和颜色用于指示指定每种日历的位置：</span><span class="sxs-lookup"><span data-stu-id="f9085-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="f9085-221">**覆盖范围组 (CG)：** 绿色</span><span class="sxs-lookup"><span data-stu-id="f9085-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="f9085-222">**仓库 (WH)：** 白色</span><span class="sxs-lookup"><span data-stu-id="f9085-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="f9085-223">**供应商 (V)：** 蓝色</span><span class="sxs-lookup"><span data-stu-id="f9085-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="f9085-224">[![日历设置概览矩阵](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="f9085-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="f9085-225">计算延迟</span><span class="sxs-lookup"><span data-stu-id="f9085-225">Calculating delays</span></span>

<span data-ttu-id="f9085-226">系统确定订单是否已延迟时，将包括所有三种安全宽限期。</span><span class="sxs-lookup"><span data-stu-id="f9085-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="f9085-227">例如，一件商品的提前期为一天，收货宽限期为三天。</span><span class="sxs-lookup"><span data-stu-id="f9085-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="f9085-228">此商品的销售订单根据需要设置为今天。</span><span class="sxs-lookup"><span data-stu-id="f9085-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="f9085-229">在此情况下，延迟的计算方法为 *提前期* + *收货宽限期* = 四天。</span><span class="sxs-lookup"><span data-stu-id="f9085-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="f9085-230">因此，如果今天是 8 月 14 日，则四天的延迟会导致交货日期为 8 月 18 日。</span><span class="sxs-lookup"><span data-stu-id="f9085-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="f9085-231">下图显示此示例。</span><span class="sxs-lookup"><span data-stu-id="f9085-231">The following illustration shows this example.</span></span>

![延迟计算示例](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="f9085-233">其他资源</span><span class="sxs-lookup"><span data-stu-id="f9085-233">Additional resources</span></span>

[<span data-ttu-id="f9085-234">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="f9085-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="f9085-235">计划优化适应分析</span><span class="sxs-lookup"><span data-stu-id="f9085-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
