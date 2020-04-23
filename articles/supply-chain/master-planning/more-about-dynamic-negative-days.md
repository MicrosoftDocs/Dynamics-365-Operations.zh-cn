---
title: 负天数和动态负天数
description: 此主题介绍有关负天数和动态负天数的信息，以及将其如何用于帮助您开展业务。
author: t-benebo
manager: tfehr
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: ''
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e9df6fcdbc894741e56f117ee1a5e370db333d9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208769"
---
# <a name="negative-days-and-dynamic-negative-days"></a><span data-ttu-id="e16a4-103">负天数和动态负天数</span><span class="sxs-lookup"><span data-stu-id="e16a4-103">Negative days and dynamic negative days</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e16a4-104">此主题介绍有关负天数和动态负天数的信息，以及将其如何用于帮助您开展业务。</span><span class="sxs-lookup"><span data-stu-id="e16a4-104">This topic provides information about negative days and dynamic negative days, and how you can use them to help your business.</span></span> <span data-ttu-id="e16a4-105">*负天数时段*表示在您的库存为负时，您愿意等待多久才订购新补货。</span><span class="sxs-lookup"><span data-stu-id="e16a4-105">The *negative days time fence* represents the number of days that you're willing to wait before you order new replenishment when you have negative inventory.</span></span>

<span data-ttu-id="e16a4-106">本主题中包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="e16a4-106">In this topic, you will learn the following information:</span></span>

- <span data-ttu-id="e16a4-107">如何创建计划订单</span><span class="sxs-lookup"><span data-stu-id="e16a4-107">How planned orders are created</span></span>
- <span data-ttu-id="e16a4-108">负天数时段与物料提前期之间的关联</span><span class="sxs-lookup"><span data-stu-id="e16a4-108">The correlation between the negative days time fence and the item's lead time</span></span>
- <span data-ttu-id="e16a4-109">如何计算动态负天数时段，以及计算时如何考虑物料提前期因素</span><span class="sxs-lookup"><span data-stu-id="e16a4-109">How the dynamic negative days time fence is calculated, and how the item's lead time is factored into the calculation</span></span>
- <span data-ttu-id="e16a4-110">如何解释与负天数有关的[有关改进物料需求计划 (MRP) 的运行时间的建议（主计划）](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx)</span><span class="sxs-lookup"><span data-stu-id="e16a4-110">How to interpret the [suggestions for improving the running time for material requirements planning (MRP) (master planning)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) that are related to negative days</span></span>

<span data-ttu-id="e16a4-111">本主题通过三个假设场景帮助您理解此信息。</span><span class="sxs-lookup"><span data-stu-id="e16a4-111">This topic uses three hypothetical scenarios to help you understand this information.</span></span> <span data-ttu-id="e16a4-112">这些场景之间的差别是您获得需求的时间点：在物料提前期前、中还是后。</span><span class="sxs-lookup"><span data-stu-id="e16a4-112">The difference between the scenarios is the point at which you get demand: before, during, or after the item's lead time period.</span></span>

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a><span data-ttu-id="e16a4-113">场景 1：需求是在物料提前期之前获得的</span><span class="sxs-lookup"><span data-stu-id="e16a4-113">Scenario 1: You get demand before the item's lead time period</span></span>

<span data-ttu-id="e16a4-114">您获得需求的时间可能相对物料提前期较早，或就在提前期开始前。</span><span class="sxs-lookup"><span data-stu-id="e16a4-114">You might get demand either relatively early in your item's lead time or just before the lead time period begins.</span></span> <span data-ttu-id="e16a4-115">下面是此场景的一个示例：</span><span class="sxs-lookup"><span data-stu-id="e16a4-115">Here is an example of this scenario:</span></span>

- <span data-ttu-id="e16a4-116">DemoProduct 物料的采购提前期为六天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-116">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="e16a4-117">在第零天（1 月 1 日），DemoProduct 物料的库存级别为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-117">On day zero (January 1), the inventory level for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="e16a4-118">在第零天（1 月 1 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-118">On day zero (January 1), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-119">在第七天（1 月 7 日），有一个现有采购订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-119">On day seven (January 7), there is an existing purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="e16a4-120">下图显示此场景的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-120">The following illustration shows a graphical view of this scenario.</span></span>

![场景 1 的图形视图](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="e16a4-122">案例 A：负天数小于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-122">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="e16a4-123">如果将负天数设置为小于物料提前期的数字，MRP 将查找负天数时段内的 DemoProduct 物料收货。</span><span class="sxs-lookup"><span data-stu-id="e16a4-123">If you set the negative days to a number that is less than the item's lead time, MRP looks for receipts for the DemoProduct item inside the negative days time fence.</span></span> <span data-ttu-id="e16a4-124">因为找不到任何收货，所以 MRP 会创建一个新的计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-124">Because it doesn't find any receipts, MRP creates a new planned purchase order.</span></span> <span data-ttu-id="e16a4-125">将立即把此计划订单推迟六天（即提前期）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-125">This planned order is immediately delayed by six days (the lead time).</span></span> <span data-ttu-id="e16a4-126">因此，将在 1 月 7 日到达。</span><span class="sxs-lookup"><span data-stu-id="e16a4-126">Therefore, it will arrive on January 7.</span></span> <span data-ttu-id="e16a4-127">现有采购订单将收到**取消**行动消息，因为创建新计划采购订单导致现有采购订单变得多余。</span><span class="sxs-lookup"><span data-stu-id="e16a4-127">The existing purchase order gets a **Cancel** action message, because the creation of the new planned purchase order has made it redundant.</span></span>

<span data-ttu-id="e16a4-128">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-128">The following illustration shows a screenshot of this case.</span></span>

![场景 1 的案例 A 屏幕截图](./media/negative-days-2.png)

<span data-ttu-id="e16a4-130">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-130">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 1 的案例 A 图形视图](./media/negative-days-3.png)

<span data-ttu-id="e16a4-132">如果考虑 MRP 绩效和计划紧张，则此案例的效果不佳。</span><span class="sxs-lookup"><span data-stu-id="e16a4-132">If you consider MRP performance and plan nervousness, this case doesn't perform well.</span></span> <span data-ttu-id="e16a4-133">MRP 必须创建新计划订单，并且必须计算延迟和行动。</span><span class="sxs-lookup"><span data-stu-id="e16a4-133">MRP must create a new planned order, and must calculate delays and actions.</span></span> <span data-ttu-id="e16a4-134">这些任务比较耗时。</span><span class="sxs-lookup"><span data-stu-id="e16a4-134">These tasks are time-consuming.</span></span> <span data-ttu-id="e16a4-135">此案例将向计划再添加两个交易。</span><span class="sxs-lookup"><span data-stu-id="e16a4-135">This case also adds two more transactions to your plan.</span></span> <span data-ttu-id="e16a4-136">另一方面，销售订单仅延迟六天，而不是七天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-136">On the other hand, the sales order is delayed by only six days, not seven days.</span></span>

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="e16a4-137">案例 B：负天数大于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-137">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="e16a4-138">若要帮助提高 MRP 绩效，可将负天数设置为大于物料提前期的数字。</span><span class="sxs-lookup"><span data-stu-id="e16a4-138">To help improve MRP performance, you can set the negative days to a number that is more than the item's lead time.</span></span> <span data-ttu-id="e16a4-139">因为此场景中提前期内无法获得供应，所以搜索收货可以一直进行到不能进行为止。</span><span class="sxs-lookup"><span data-stu-id="e16a4-139">Because you can't get the supply inside the lead time in this scenario, you can search for receipts for as long as this search makes sense.</span></span> <span data-ttu-id="e16a4-140">尽管 MRP 的运行时间较短，所以应注意订单是否有更多延迟。</span><span class="sxs-lookup"><span data-stu-id="e16a4-140">Although the running time for MRP will be shorter, you should watch out for additional delays to the orders.</span></span>

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="e16a4-141">案例 C：将物料提前期与负天数时段自动关联</span><span class="sxs-lookup"><span data-stu-id="e16a4-141">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="e16a4-142">若要将物料提前期与负天数时段自动关联，请使用动态负天数。</span><span class="sxs-lookup"><span data-stu-id="e16a4-142">To automatically correlate the item's lead time to the negative days time fence, use dynamic negative days.</span></span> <span data-ttu-id="e16a4-143">若要使用动态负天数，请转到**主计划 \> 设置 \> 主计划参数**，然后在**常规**选项卡上的**覆盖范围**部分中，将**使用动态负天数**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e16a4-143">To use dynamic negative days, go to **Master planning \> Setup \> Master planning parameters**, and then, on the **General** tab, in the **Coverage** section, set the **Use dynamic negative days** option to **Yes**.</span></span> <span data-ttu-id="e16a4-144">然后，MRP 查找动态负天数时段内的收货。</span><span class="sxs-lookup"><span data-stu-id="e16a4-144">MRP then looks for receipts inside the dynamic negative days time fence.</span></span> <span data-ttu-id="e16a4-145">此时段使用以下公式计算：</span><span class="sxs-lookup"><span data-stu-id="e16a4-145">This time fence is calculated by using the following formula:</span></span>

<span data-ttu-id="e16a4-146">动态负天数时段 = 采购提前期 + 负天数时段 +（当前日期 – 需求日期）</span><span class="sxs-lookup"><span data-stu-id="e16a4-146">Dynamic negative days time fence = Purchase lead time + Negative days time fence + (Current date – Requirement date)</span></span>

<span data-ttu-id="e16a4-147">（如果 DemoProduct 物料的默认订单类型为**生产**或**转移**，则提前期为**库存**提前期。）</span><span class="sxs-lookup"><span data-stu-id="e16a4-147">(If the default order type of the DemoProduct item is **Production** or **Transfer**, the lead time is the **inventory** lead time.)</span></span>

<span data-ttu-id="e16a4-148">如果使用动态负天数，则 MRP 查看收货的时段现在为 6 + 2 + 0 = 8 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-148">When dynamic negative days are used, the time fence that MRP looks at for receipts is now 6 + 2 + 0 = 8 days.</span></span> <span data-ttu-id="e16a4-149">MRP 查找现有采购订单并将销售订单与其关联。</span><span class="sxs-lookup"><span data-stu-id="e16a4-149">MRP finds the existing purchase order and pegs the sales order against it.</span></span> <span data-ttu-id="e16a4-150">将不创建任何新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-150">No new planned orders are created.</span></span> <span data-ttu-id="e16a4-151">因此，MRP 的运行时间较短。</span><span class="sxs-lookup"><span data-stu-id="e16a4-151">Therefore, the running time for MRP is shorter.</span></span> <span data-ttu-id="e16a4-152">下图显示 DemoProduct 物料的净需求。</span><span class="sxs-lookup"><span data-stu-id="e16a4-152">The following illustration shows the net requirements for the DemoProduct item.</span></span>

![场景 1 的案例 C 净需求](./media/negative-days-4.png)

<span data-ttu-id="e16a4-154">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-154">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 1 的案例 C 图形视图](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="e16a4-156">案例 D：仅使用动态负天数</span><span class="sxs-lookup"><span data-stu-id="e16a4-156">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="e16a4-157">如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段为 6 + 0 + 0 = 6 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-157">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is 6 + 0 + 0 = 6 days.</span></span> <span data-ttu-id="e16a4-158">在此案例中，结果与此场景的案例 A 的结果相同。</span><span class="sxs-lookup"><span data-stu-id="e16a4-158">In this case, the result is the same as the result in case A for this scenario.</span></span> <span data-ttu-id="e16a4-159">MRP 必须创建新计划订单，并且必须计算延迟和行动。</span><span class="sxs-lookup"><span data-stu-id="e16a4-159">MRP must create a new planned order, and must calculate delays and actions.</span></span> <span data-ttu-id="e16a4-160">这些任务非常耗时，并且还可能让人精疲力尽。</span><span class="sxs-lookup"><span data-stu-id="e16a4-160">These tasks are time-consuming and can also be frustrating.</span></span> <span data-ttu-id="e16a4-161">您还有两个交易需要处理。</span><span class="sxs-lookup"><span data-stu-id="e16a4-161">You also have two more transactions to process.</span></span> <span data-ttu-id="e16a4-162">因为不能准时履行有关物料到达的需求，此案例为计划带来了不必要的复杂性。</span><span class="sxs-lookup"><span data-stu-id="e16a4-162">Because the demand can't be fulfilled on time for the item to arrive, this case adds unnecessary complications to your plan.</span></span>

<span data-ttu-id="e16a4-163">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-163">The following illustration shows a screenshot for this case.</span></span>

![场景 1 的案例 D 屏幕截图](./media/negative-days-6.png)

<span data-ttu-id="e16a4-165">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-165">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 1 的案例 D 图形视图](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="e16a4-167">案例 E：同时使用大于物料提前期的负天数和动态负天数时段</span><span class="sxs-lookup"><span data-stu-id="e16a4-167">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="e16a4-168">如果将负天数设置为大于物料提前期的数字，并且还使用动态负天数时段，则动态负天数时段为 6 + 6 + 0 = 12 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-168">If you set the negative days to a number that is more than the item's lead time, and if you also use the dynamic negative days time fence, the dynamic negative days time fence is 6 + 6 + 0 = 12 days.</span></span> <span data-ttu-id="e16a4-169">这种方法可能会导致 MRP 必须在很长的时段内搜索结果。</span><span class="sxs-lookup"><span data-stu-id="e16a4-169">This approach might produce a very long time fence that MRP must search for results in.</span></span> <span data-ttu-id="e16a4-170">有关案例 E 与将负天数设置为长时段的情况之间的关系的信息，请参阅本主题的[结论](#conclusion)部分。</span><span class="sxs-lookup"><span data-stu-id="e16a4-170">For information about how case E is related to a situation where you set the negative days to a long time fence, see the [Conclusion](#conclusion) section of this topic.</span></span>

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a><span data-ttu-id="e16a4-171">场景 2：需求是在物料提前期中获得的</span><span class="sxs-lookup"><span data-stu-id="e16a4-171">Scenario 2: You get demand during the item's lead time period</span></span>

<span data-ttu-id="e16a4-172">有时可能会在物料提前期内获得需求。</span><span class="sxs-lookup"><span data-stu-id="e16a4-172">You might get demand sometime during your item's lead time.</span></span> <span data-ttu-id="e16a4-173">下面是此场景的一个示例：</span><span class="sxs-lookup"><span data-stu-id="e16a4-173">Here is an example of this scenario:</span></span>

- <span data-ttu-id="e16a4-174">DemoProduct 物料的采购提前期为六天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-174">The DemoProduct item has a six-day purchase lead time.</span></span> 
- <span data-ttu-id="e16a4-175">在第零天（1 月 1 日），DemoProduct 物料的库存级别为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-175">On day zero (January 1), the inventory level for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="e16a4-176">在第四天（1 月 5 日，这在物料提前期内），您获得了一个销售订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-176">On day four (January 5), which is inside the item's lead time, you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-177">在第七天（1 月 8 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-177">On day seven (January 8), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="e16a4-178">下图显示此场景的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-178">The following illustration shows a graphical view of this scenario.</span></span>

![场景 1 的图形视图](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="e16a4-180">案例 A：负天数小于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-180">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="e16a4-181">如果将负天数设置为小于物料提前期的数字，MRP 将查找负天数时段内的 DemoProduct 物料收货。</span><span class="sxs-lookup"><span data-stu-id="e16a4-181">If you set the negative days to a number that is less than the item's lead time, MRP looks for receipts for the DemoProduct item inside the negative days time fence.</span></span> <span data-ttu-id="e16a4-182">因为未找到任何收货，MRP 创建一个新的计划采购订单，该采购订单将当前日期用作订单日期。</span><span class="sxs-lookup"><span data-stu-id="e16a4-182">Because it doesn't find any receipts, MRP creates a new planned purchase order that uses the current date as the order date.</span></span> <span data-ttu-id="e16a4-183">将立即把此计划订单推迟六天（即提前期）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-183">This planned order is immediately delayed by six days (the lead time).</span></span> <span data-ttu-id="e16a4-184">因此，将在 1 月 7 日到达。</span><span class="sxs-lookup"><span data-stu-id="e16a4-184">Therefore, it will arrive on January 7.</span></span> <span data-ttu-id="e16a4-185">现有采购订单将收到**取消**行动消息，因为创建新计划采购订单导致现有采购订单变得多余。</span><span class="sxs-lookup"><span data-stu-id="e16a4-185">The existing purchase order gets a **Cancel** action message, because the creation of the new planned purchase order has made it redundant.</span></span>

<span data-ttu-id="e16a4-186">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-186">The following illustration shows a screenshot for this case.</span></span>

![场景 2 的案例 A 屏幕截图](./media/negative-days-9.png)

<span data-ttu-id="e16a4-188">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-188">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 2 的案例 A 图形视图](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="e16a4-190">案例 B：负天数大于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-190">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="e16a4-191">此案例类似场景 1 的案例 B。</span><span class="sxs-lookup"><span data-stu-id="e16a4-191">This case resembles case B for scenario 1.</span></span> <span data-ttu-id="e16a4-192">如果将负天数设置为大于物料提前期的数字，则不会获得新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-192">If you set the negative days to a number that is more than the item's lead time, you don't get a new planned order.</span></span> <span data-ttu-id="e16a4-193">将把销售订单附加到现有采购订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-193">The sales order is attached to the existing purchase order.</span></span>

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="e16a4-194">案例 C：将物料提前期与负天数时段自动关联</span><span class="sxs-lookup"><span data-stu-id="e16a4-194">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="e16a4-195">此案例类似场景 1 的案例 C，因为动态负天数的效果与在该案例中一样出色。</span><span class="sxs-lookup"><span data-stu-id="e16a4-195">This case resembles case C for scenario 1, because dynamic negative days work just as well as they do in that case.</span></span> <span data-ttu-id="e16a4-196">动态负天数时段现在为 6 + 2 – 4 = 4 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-196">The dynamic negative days time fence is now 6 + 2 – 4 = 4 days.</span></span> <span data-ttu-id="e16a4-197">如果使用此方法，MRP 将找到现有采购订单，并为其附加销售订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-197">If you use this approach, MRP finds the existing purchase order and attaches the sales order to it.</span></span> <span data-ttu-id="e16a4-198">因为不创建新计划订单，所以 MRP 的运行时间较短。</span><span class="sxs-lookup"><span data-stu-id="e16a4-198">Because no new planned orders are created, the running time for MRP is shorter.</span></span>

<span data-ttu-id="e16a4-199">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-199">The following illustration shows a screenshot of this case.</span></span>

![场景 2 的案例 C 屏幕截图](./media/negative-days-11.png)

<span data-ttu-id="e16a4-201">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-201">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 2 的案例 C 图形视图](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="e16a4-203">案例 D：仅使用动态负天数</span><span class="sxs-lookup"><span data-stu-id="e16a4-203">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="e16a4-204">如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段现在为 6 + 0 - 4 = 2 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-204">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is now 6 + 0 – 4 = 2 days.</span></span> <span data-ttu-id="e16a4-205">在此案例中，结果与此场景的案例 A 的结果相同。</span><span class="sxs-lookup"><span data-stu-id="e16a4-205">In this case, the result is the same as the result in case A for this scenario.</span></span> <span data-ttu-id="e16a4-206">有关结果的图形视图，请参见此场景的案例 A。</span><span class="sxs-lookup"><span data-stu-id="e16a4-206">For a graphical view of what occurs, see case A for this scenario.</span></span>

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="e16a4-207">案例 E：同时使用大于物料提前期的负天数和动态负天数时段</span><span class="sxs-lookup"><span data-stu-id="e16a4-207">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="e16a4-208">如果将负天数设置为大于物料提前期的数字，并且还使用动态负天数时段，则动态负天数时段为 6 + 6 - 4 = 8 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-208">If you set the negative days to a number that is more than the item's lead time, and if you also use the dynamic negative days time fence, the dynamic negative days time fence is 6 + 6 – 4 = 8 days.</span></span> <span data-ttu-id="e16a4-209">这种方法可能会导致 MRP 必须在很长的时段内搜索结果。</span><span class="sxs-lookup"><span data-stu-id="e16a4-209">This approach might produce a very long time fence that MRP must search for results in.</span></span> <span data-ttu-id="e16a4-210">有关案例 E 与将负天数设置为长时段的情况之间的关系的信息，请参阅本主题的[结论](#conclusion)部分。</span><span class="sxs-lookup"><span data-stu-id="e16a4-210">For information about how case E is related to a situation where you set the negative days to a long time fence, see the [Conclusion](#conclusion) section of this topic.</span></span>

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a><span data-ttu-id="e16a4-211">场景 3：需求是在物料提前期后获得的</span><span class="sxs-lookup"><span data-stu-id="e16a4-211">Scenario 3: You get demand after the item's lead time period</span></span>

<span data-ttu-id="e16a4-212">需求可能是在物料提前期后获得的。</span><span class="sxs-lookup"><span data-stu-id="e16a4-212">You might get demand after the item's lead time.</span></span> <span data-ttu-id="e16a4-213">下面是此场景的一个示例：</span><span class="sxs-lookup"><span data-stu-id="e16a4-213">Here is an example of this scenario:</span></span>

- <span data-ttu-id="e16a4-214">DemoProduct 物料的采购提前期为六天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-214">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="e16a4-215">在第零天（1 月 1 日），DemoProduct 物料的库存为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-215">On day zero (January 1), the inventory for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="e16a4-216">在第七天（1 月 8 日，这超出了物料提前期），您获得了一个销售订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-216">On day seven (January 8), which is outside the item's lead time, you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-217">在第 10 天（1 月 11 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-217">On day 10 (January 11), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="e16a4-218">下图显示此场景的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-218">The following illustration shows a graphical view of this scenario.</span></span>

![场景 3 的图形视图](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="e16a4-220">案例 A：负天数小于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-220">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="e16a4-221">如果将负天数设置为小于物料提前期的数字，MRP 会在销售订单需求日期前两天查找。</span><span class="sxs-lookup"><span data-stu-id="e16a4-221">If you set the negative days to a number that is less than the item's lead time, MRP looks two days ahead of the sales order's requirement date.</span></span> <span data-ttu-id="e16a4-222">因为找不到任何内容，所以 MRP 会在 1 月 2 日创建一个计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-222">Because it doesn't find anything, MRP creates a planned purchase order on January 2.</span></span> <span data-ttu-id="e16a4-223">将仅为这个计划采购订单及时发货以履行销售订单需求。</span><span class="sxs-lookup"><span data-stu-id="e16a4-223">This planned purchase order will be shipped just in time to fulfill the sales order demand.</span></span> <span data-ttu-id="e16a4-224">现有采购订单将收到**取消**行动消息，因为不需要该订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-224">The existing purchase order gets a **Cancel** action message, because it isn't required.</span></span>

<span data-ttu-id="e16a4-225">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-225">The following illustration shows a screenshot of this case.</span></span>

![场景 3 的案例 A 屏幕截图](./media/negative-days-14.png)

<span data-ttu-id="e16a4-227">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-227">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 3 的案例 A 图形视图](./media/negative-days-15.png)

> [!NOTE]
> <span data-ttu-id="e16a4-229">在前面的屏幕截图中，采购订单需求日期为 1 月 12 日。</span><span class="sxs-lookup"><span data-stu-id="e16a4-229">In the preceding screenshot, the purchase order requirement date is January 12.</span></span> <span data-ttu-id="e16a4-230">因为该屏幕截图是在 2015 年截取的，当时 1 月 11 日是星期日，MRP 将需求日期移到了下一个工作日，即 1 月 12 日，星期一。</span><span class="sxs-lookup"><span data-stu-id="e16a4-230">Because that screenshot was taken in 2015, when January 11 was a Sunday, MRP moved the requirement date to the next working day, which was Monday, January 12.</span></span> <span data-ttu-id="e16a4-231">不过，采购订单的交付日期为 1 月 11 日。</span><span class="sxs-lookup"><span data-stu-id="e16a4-231">Nevertheless, the purchase order has a delivery date of January 11.</span></span>

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="e16a4-232">案例 B：负天数大于物料提前期</span><span class="sxs-lookup"><span data-stu-id="e16a4-232">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="e16a4-233">如果将负天数设置为大于物料提前期的数字，则不会获得新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-233">If you set the negative days to a number that is more than the item's lead time, you don't get a new planned order.</span></span> <span data-ttu-id="e16a4-234">将把销售订单与现有采购订单关联。</span><span class="sxs-lookup"><span data-stu-id="e16a4-234">The sales order is pegged against the existing purchase order.</span></span> <span data-ttu-id="e16a4-235">因此，销售订单将延迟。</span><span class="sxs-lookup"><span data-stu-id="e16a4-235">Therefore, the sales order is delayed.</span></span> <span data-ttu-id="e16a4-236">如果创建计划订单，则可为销售订单准时发货。</span><span class="sxs-lookup"><span data-stu-id="e16a4-236">If you create a planned order, you can ship the sales order on time.</span></span>

<span data-ttu-id="e16a4-237">下图显示此案例的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-237">The following illustration shows a screenshot of this case.</span></span>

![场景 3 的案例 B 屏幕截图](./media/negative-days-16.png)

<span data-ttu-id="e16a4-239">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-239">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 3 的案例 B 图形视图](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="e16a4-241">案例 C：将物料提前期与负天数时段自动关联</span><span class="sxs-lookup"><span data-stu-id="e16a4-241">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="e16a4-242">此案例类似场景 1 的案例 C，因为动态负天数的效果与在该场景的案例 B 中一样出色，如果不更出色的话。</span><span class="sxs-lookup"><span data-stu-id="e16a4-242">This case resembles case C for scenario 1, because dynamic negative days work just as well as, if not better than, they work in case B for this scenario.</span></span>

<span data-ttu-id="e16a4-243">动态负天数时段为 6 + 2 – 7 = 1 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-243">The dynamic negative days time fence is 6 + 2 – 7 = 1 day.</span></span> <span data-ttu-id="e16a4-244">但是，在此案例中，系统仍然会考虑负天数提前期 (2)，因为 MRP 会考虑负天数提前期与动态负天数提前期之间的最大值。</span><span class="sxs-lookup"><span data-stu-id="e16a4-244">However, in this case, the system still considers the negative days lead time (2), because MRP considers the maximum value between the negative days lead time and the dynamic negative days lead time.</span></span> <span data-ttu-id="e16a4-245">因此，此案例中的结果与此场景的案例 A 的结果相同。</span><span class="sxs-lookup"><span data-stu-id="e16a4-245">Therefore, the result in this case is the same as the result in case A for this scenario.</span></span>

<span data-ttu-id="e16a4-246">下图显示此案例中的结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-246">The following illustration shows a graphical view of what occurs in this case.</span></span>

![场景 3 的案例 C 图形视图](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="e16a4-248">案例 D：仅使用动态负天数</span><span class="sxs-lookup"><span data-stu-id="e16a4-248">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="e16a4-249">如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段现在为 6 + 0 - 7 = -1 天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-249">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is now 6 + 0 – 7 = -1 day.</span></span> <span data-ttu-id="e16a4-250">在此案例中，系统仍然考虑负天数提前期 (2)。</span><span class="sxs-lookup"><span data-stu-id="e16a4-250">In this case, the system still considers the negative days lead time (2).</span></span> <span data-ttu-id="e16a4-251">因此，此案例中的结果与此场景的案例 A 的结果相同，缺点也完全一样。</span><span class="sxs-lookup"><span data-stu-id="e16a4-251">Therefore, the result in this case is the same as the result in case A for this scenario and has all the same drawbacks.</span></span> <span data-ttu-id="e16a4-252">有关结果的图形视图，请参见场景 2 的案例 A。</span><span class="sxs-lookup"><span data-stu-id="e16a4-252">For a graphical view of what occurs, see case A for scenario 2.</span></span>

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="e16a4-253">案例 E：同时使用大于物料提前期的负天数和动态负天数时段</span><span class="sxs-lookup"><span data-stu-id="e16a4-253">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="e16a4-254">此案例与场景 1 和 2 的案例 E 相同。</span><span class="sxs-lookup"><span data-stu-id="e16a4-254">This case is the same as case E for scenarios 1 and 2.</span></span> <span data-ttu-id="e16a4-255">优点和缺点基本分别一样。</span><span class="sxs-lookup"><span data-stu-id="e16a4-255">It has basically the same benefits and drawbacks.</span></span>

## <a name="conclusion"></a><span data-ttu-id="e16a4-256">结论</span><span class="sxs-lookup"><span data-stu-id="e16a4-256">Conclusion</span></span>

<span data-ttu-id="e16a4-257">如本主题中的三个场景所示，最好将负天数设置为大于覆盖范围组中的物料提前期的数字。</span><span class="sxs-lookup"><span data-stu-id="e16a4-257">As the three scenarios in this topic show, it's a good idea to set the negative days to a number that is more than the lead time of the items in the coverage group.</span></span> <span data-ttu-id="e16a4-258">此外，最好仅使用动态负天数，并将负天数设置为在您的库存为负时，您愿意在订购新补货之前愿意等待的天数（换句话说，愿意进一步延迟需求的天数）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-258">It's also a good idea to use only dynamic negative days, and to set the negative days to the number of days that you're willing to wait before you order new replenishment when you have negative inventory (in other words, the number of days that you're willing to further delay demand).</span></span> <span data-ttu-id="e16a4-259">此外，同一个覆盖范围组中的物料应具有类似提前期。</span><span class="sxs-lookup"><span data-stu-id="e16a4-259">Additionally, items in the same coverage group should have similar lead times.</span></span>

<span data-ttu-id="e16a4-260">如果将负天数设置为 **0**（零），并且不使用动态负天数，则 MRP 设置创建新计划订单来履行需求。</span><span class="sxs-lookup"><span data-stu-id="e16a4-260">If you set the negative days to **0** (zero) and don't use dynamic negative days, MRP always creates a new planned order to fulfill demand.</span></span> <span data-ttu-id="e16a4-261">在此情况下，务必使用行动消息，以确保库存不会积压。</span><span class="sxs-lookup"><span data-stu-id="e16a4-261">In this situation, it's important that you work with the action messages to make sure that you don't pile up inventory.</span></span>

<span data-ttu-id="e16a4-262">您可能需要将负天数设置为较长时段，然后使用行动消息。</span><span class="sxs-lookup"><span data-stu-id="e16a4-262">You might want to set the negative days to a long time fence and then work with the action messages.</span></span> <span data-ttu-id="e16a4-263">这种方法的计划结果很好，不过速度也有点慢。</span><span class="sxs-lookup"><span data-stu-id="e16a4-263">This approach produces good planning results, but it's also a bit slower.</span></span> <span data-ttu-id="e16a4-264">还可能更难分析，因为必须分析并采用行动消息。</span><span class="sxs-lookup"><span data-stu-id="e16a4-264">It might also be more difficult to analyze, because you must analyze and apply the action messages.</span></span> <span data-ttu-id="e16a4-265">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="e16a4-265">Here is an example:</span></span>

- <span data-ttu-id="e16a4-266">DemoProduct 物料的采购提前期为六天。</span><span class="sxs-lookup"><span data-stu-id="e16a4-266">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="e16a4-267">在第零天（1 月 1 日），DemoProduct 物料的库存为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e16a4-267">On day zero (January 1), the inventory for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="e16a4-268">在第零天（1 月 1 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-268">On day zero (January 1), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-269">在第 10 天（1 月 10 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-269">On day 10 (January 10), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-270">在第 12 天（1 月 12 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。</span><span class="sxs-lookup"><span data-stu-id="e16a4-270">On day 12 (January 12), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="e16a4-271">负天数设置为 **20**，比物料提前期大得多。</span><span class="sxs-lookup"><span data-stu-id="e16a4-271">Negative days are set to **20**, which is much more than the item's lead time.</span></span>

<span data-ttu-id="e16a4-272">下图显示结果的图形视图。</span><span class="sxs-lookup"><span data-stu-id="e16a4-272">The following illustration shows a graphical view of what occurs.</span></span>

![示例的图形回顾](./media/negative-days-19.png)

<span data-ttu-id="e16a4-274">MRP 产生以下结果。</span><span class="sxs-lookup"><span data-stu-id="e16a4-274">MRP produces the following results.</span></span>

![结果](./media/negative-days-20.png)

<span data-ttu-id="e16a4-276">在上一个屏幕截图中，销售订单需求日期为 1 月 9 日，而不是 1 月 10 日。</span><span class="sxs-lookup"><span data-stu-id="e16a4-276">In the preceding screenshot, the sales order requirement date is January 9 instead of January 10.</span></span> <span data-ttu-id="e16a4-277">因为该屏幕截图是在 2015 年截取的，当时 1 月 10 日是星期六，所以订单的需求日期应该是上一个工作日，即 1 月 9 日，星期五。</span><span class="sxs-lookup"><span data-stu-id="e16a4-277">Because that screenshot was taken in 2015, when January 10 was a Saturday, the requirement date of the order should be the previous working day, which was Friday, January 9.</span></span>

<span data-ttu-id="e16a4-278">MRP 创建计划采购订单以履行第一个销售订单请求的需求，但是还建议您取消计划订单，因为可以将现有采购订单提前，并增加其中的数量。</span><span class="sxs-lookup"><span data-stu-id="e16a4-278">MRP creates a planned purchase order to fulfill the demand that is requested by the first sales order, but then it also recommends that you cancel the planned order, because you can advance the existing purchase order and increase the quantity on it.</span></span>

<span data-ttu-id="e16a4-279">结果没有问题，但是 MRP 的运行时间可能较长，因为 MRP 必须创建所有延迟和建议。</span><span class="sxs-lookup"><span data-stu-id="e16a4-279">The results aren't wrong, but the running time for MRP might be longer, because MRP must create all the delays and suggestions.</span></span> <span data-ttu-id="e16a4-280">此外，规划员还可能需要更多时间来理解 MRP 结果。</span><span class="sxs-lookup"><span data-stu-id="e16a4-280">Additionally, the planner might require more time to understand the MRP results.</span></span> <span data-ttu-id="e16a4-281">最重要的是，在此情况下，规划员务必理解和使用行动消息。</span><span class="sxs-lookup"><span data-stu-id="e16a4-281">Most importantly, in this case, it's essential that the planner understand and use the action messages.</span></span>

<span data-ttu-id="e16a4-282">如果将负天数减小到更接近物料提前期的数字，并且使用动态负天数，MRP 将产生以下结果。</span><span class="sxs-lookup"><span data-stu-id="e16a4-282">If you reduce the negative days to a number that's closer to the item's lead time, and you use dynamic negative days, MRP produces the following results.</span></span>

![结果](./media/negative-days-21.png)

<span data-ttu-id="e16a4-284">MRP 创建一个附加到第一个销售订单的计划订单。</span><span class="sxs-lookup"><span data-stu-id="e16a4-284">MRP creates a planned order that is attached to the first sales order.</span></span> <span data-ttu-id="e16a4-285">然后，基于负天数设置将第二个销售订单与现有采购订单关联。这是正常现象。</span><span class="sxs-lookup"><span data-stu-id="e16a4-285">Then, as is expected, the second sales order is pegged against the existing purchase order, based on the negative days setting.</span></span> <span data-ttu-id="e16a4-286">这个计划结果也是正确的，并且 MRP 的运行时间可能较短。</span><span class="sxs-lookup"><span data-stu-id="e16a4-286">This planning result is also correct, and the running time for MRP might be shorter.</span></span> <span data-ttu-id="e16a4-287">在此情况下，务必了解并知道如何使用行动消息。</span><span class="sxs-lookup"><span data-stu-id="e16a4-287">In this case, it isn't essential that you understand and know how to work with the action messages.</span></span>

<span data-ttu-id="e16a4-288">若要帮助确保为您的业务输入正确值，必须同时考虑功能和 MRP 运行时间。</span><span class="sxs-lookup"><span data-stu-id="e16a4-288">To help guarantee that the correct values are entered for your business, you must think in terms of both functionality and MRP running time.</span></span> <span data-ttu-id="e16a4-289">因此，可以通过一些试错来确定最佳值。</span><span class="sxs-lookup"><span data-stu-id="e16a4-289">Therefore, it can take a little trial and error to determine the optimal values.</span></span>

## <a name="see-also"></a><span data-ttu-id="e16a4-290">请参阅</span><span class="sxs-lookup"><span data-stu-id="e16a4-290">See also</span></span>

<span data-ttu-id="e16a4-291">有关详细讨论，请参阅原始博客文章[有关（动态）负天数的详细信息](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/)。</span><span class="sxs-lookup"><span data-stu-id="e16a4-291">For more discussion, see the original [More about (dynamic) negative days](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/) blog post.</span></span>
