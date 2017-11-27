---
title: "订单输入截止时间"
description: "本文提供有关订单条目截止时间的信息。 订单条目截止日期是确定客户订单是否被视作（并履行）在当前日期或第二天接收。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 31308e64d4871a4d09540df16fdcd02cc83bd0be
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="order-entry-deadlines"></a><span data-ttu-id="db6ad-104">订单输入截止时间</span><span class="sxs-lookup"><span data-stu-id="db6ad-104">Order entry deadlines</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="db6ad-105">本文提供有关订单条目截止时间的信息。</span><span class="sxs-lookup"><span data-stu-id="db6ad-105">This article provides information about order entry deadlines.</span></span> <span data-ttu-id="db6ad-106">订单条目截止日期是确定客户订单是否被视作（并履行）在当前日期或第二天接收。</span><span class="sxs-lookup"><span data-stu-id="db6ad-106">An order entry deadline is a cut-off time that determines whether a customer order is treated (and fulfilled) as if it was received on the current day or the next day.</span></span>

<span data-ttu-id="db6ad-107">在许多公司中，仅在一天中的某一时刻之前收到的销售订单被视为在当天收到。</span><span class="sxs-lookup"><span data-stu-id="db6ad-107">In many companies, only sales orders that are received before a certain time of day are treated as if they were received on that day.</span></span> <span data-ttu-id="db6ad-108">从该时间后收到的所有订单均被视为在下一个工作日接收。</span><span class="sxs-lookup"><span data-stu-id="db6ad-108">Any orders that are received after that time are treated as if they are received on the next business day.</span></span> <span data-ttu-id="db6ad-109">此订单的截止时间称作订单条目截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-109">This cut-off time for orders is known as the order entry deadline.</span></span>  

<span data-ttu-id="db6ad-110">订单条目截止时间用作订单承诺的输入。</span><span class="sxs-lookup"><span data-stu-id="db6ad-110">Order entry deadlines are used as input for order promising.</span></span> <span data-ttu-id="db6ad-111">因此，它们帮助您管理有关订单交货的客户预期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-111">Therefore, they help you manage customer expectations about order deliveries.</span></span> <span data-ttu-id="db6ad-112">例如，客户可以看到，如果在特定时间之前向您下订单，您将确定在同一天装运货物。</span><span class="sxs-lookup"><span data-stu-id="db6ad-112">For example, customers can see that, if they place an order with you before a specific time, you will commit to shipping the goods on the same day.</span></span> <span data-ttu-id="db6ad-113">不过，如果缺少该截止日期，他们则可以预期仅在下一个工作日装运。</span><span class="sxs-lookup"><span data-stu-id="db6ad-113">However, if they miss that deadline, they can expect the shipment only on the next business day.</span></span> <span data-ttu-id="db6ad-114">您基于您的仓库能力和装运承运人计划设置订单条目截止日期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-114">You set order entry deadlines based on your warehouse capabilities and shipping carrier schedules.</span></span>  

<span data-ttu-id="db6ad-115">在**订单条目截止日期**页中，您为该周中的每一天都设置订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-115">On the **Order entry deadlines** page, you set up order entry deadline times for all the days of the week.</span></span> <span data-ttu-id="db6ad-116">如果在该时间后收到订单，订单被视为在第二天接收。</span><span class="sxs-lookup"><span data-stu-id="db6ad-116">If orders are received after the specified times, they are treated as if they are received on the next day.</span></span> <span data-ttu-id="db6ad-117">默认情况下，将这些时间设置为 23:59（即当天午夜前的一分钟）。</span><span class="sxs-lookup"><span data-stu-id="db6ad-117">By default, these times are set to 23:59 (that is, one minute before midnight at the end of the relevant day).</span></span> <span data-ttu-id="db6ad-118">可以更改默认时间，以使其与实际的装运或接收截止时间一致。</span><span class="sxs-lookup"><span data-stu-id="db6ad-118">You can change the default times so that they coincide with actual ship or receipt deadline times.</span></span>  

<span data-ttu-id="db6ad-119">您可以为特定组的客户定义订单输入截止日期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-119">You can define order entry deadlines for a specific group of customers.</span></span> <span data-ttu-id="db6ad-120">例如，您可能想要一组特定客户具有比其他客户晚的订单输入截止日期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-120">For example, you might want a specific group of customers to have order entry deadlines that are later than those of other customers.</span></span> <span data-ttu-id="db6ad-121">在这种情况下，您首先定义**订单输入截止时间组**页上的订单输入截止时间的组。</span><span class="sxs-lookup"><span data-stu-id="db6ad-121">In this case, you first define groups for order entry deadlines on the **Order entry deadline groups** page.</span></span> <span data-ttu-id="db6ad-122">然后您将组分配给**客户**页上的客户。</span><span class="sxs-lookup"><span data-stu-id="db6ad-122">You then assign the groups to customers on the **Customers** page.</span></span>  

<span data-ttu-id="db6ad-123">如果您的公司由若干站点构成，则您可以为每个站点设置订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-123">If your company consists of several sites, you can set up order entry deadlines for each site.</span></span> <span data-ttu-id="db6ad-124">如果这些站点位于不同的时区，则在每个站点的时区设置订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-124">If the sites are located in different time zones, the order entry deadlines are set up in each site's time zone.</span></span> <span data-ttu-id="db6ad-125">但是，在您使用销售订单和销售报价单时，订单输入截止时间将在**可用的装运日期和接收日期**页中转换为您的时区。</span><span class="sxs-lookup"><span data-stu-id="db6ad-125">However, when you work with sales orders and sales quotations, the order entry deadline is converted to your time zone on the **Available ship and receipt dates** page.</span></span>  

<span data-ttu-id="db6ad-126">在**启用订单输入截止时间组合**页上，您定义允许的站点和订单输入截止时间组的组合。</span><span class="sxs-lookup"><span data-stu-id="db6ad-126">On the **Activate order entry deadline combinations** page, you define the combinations of sites and order entry deadline groups that are allowed.</span></span>

## <a name="example-order-entry-deadline"></a><span data-ttu-id="db6ad-127">示例：订单输入截止时间</span><span class="sxs-lookup"><span data-stu-id="db6ad-127">Example: Order entry deadline</span></span>
<span data-ttu-id="db6ad-128">星期二的订单输入截止时间已设置为 16:00。</span><span class="sxs-lookup"><span data-stu-id="db6ad-128">The order entry deadline on Tuesdays has been set to 16:00.</span></span> <span data-ttu-id="db6ad-129">在特定星期二，在 17:00，您尝试将当前日期设置为装运日期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-129">On a particular Tuesday, at 17:00, you try to set the current date as the ship date.</span></span> <span data-ttu-id="db6ad-130">（请注意，此示例没有提前期。）如果选中**交货日期控制**复选框，您将收到警告，指出该日期不是有效的。</span><span class="sxs-lookup"><span data-stu-id="db6ad-130">(Note that there is no lead time for this example.) If the **Delivery date control** check box is selected, you receive a warning that states that the date isn't valid.</span></span> <span data-ttu-id="db6ad-131">此警告显示在**可用的装运日期和接收日期**页上，在此页您可以选择备选日期。</span><span class="sxs-lookup"><span data-stu-id="db6ad-131">This warning appears on the **Available ship and receipt dates** page, where you can then select alternative dates.</span></span>

## <a name="example-different-order-entry-deadlines-per-site"></a><span data-ttu-id="db6ad-132">示例：每个站点不同的订单输入截止时间</span><span class="sxs-lookup"><span data-stu-id="db6ad-132">Example: Different order entry deadlines per site</span></span>
<span data-ttu-id="db6ad-133">您的公司由两个站点构成。</span><span class="sxs-lookup"><span data-stu-id="db6ad-133">Your company consists of two sites.</span></span> <span data-ttu-id="db6ad-134">如下表中所示，这些站点位于不同的时区。</span><span class="sxs-lookup"><span data-stu-id="db6ad-134">The sites are located in different time zones, as shown in the following table.</span></span>

| <span data-ttu-id="db6ad-135">站点 A</span><span class="sxs-lookup"><span data-stu-id="db6ad-135">Site A</span></span>                      | <span data-ttu-id="db6ad-136">站点 B</span><span class="sxs-lookup"><span data-stu-id="db6ad-136">Site B</span></span>                      |
|-----------------------------|-----------------------------|
| <span data-ttu-id="db6ad-137">加利福尼亚</span><span class="sxs-lookup"><span data-stu-id="db6ad-137">California</span></span>                  | <span data-ttu-id="db6ad-138">佛罗里达</span><span class="sxs-lookup"><span data-stu-id="db6ad-138">Florida</span></span>                     |
| <span data-ttu-id="db6ad-139">PST（太平洋标准时间）</span><span class="sxs-lookup"><span data-stu-id="db6ad-139">PST (Pacific Standard Time)</span></span> | <span data-ttu-id="db6ad-140">EST（东部标准时间）</span><span class="sxs-lookup"><span data-stu-id="db6ad-140">EST (Eastern Standard Time)</span></span> |

<span data-ttu-id="db6ad-141">站点 A 和站点 B 都定义了以下订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-141">Sites A and B have defined the following order entry deadlines.</span></span>

| <span data-ttu-id="db6ad-142">一周中的日</span><span class="sxs-lookup"><span data-stu-id="db6ad-142">Day of the week</span></span>             | <span data-ttu-id="db6ad-143">A：订单输入截止时间 (PST)</span><span class="sxs-lookup"><span data-stu-id="db6ad-143">A: Order entry deadlines (PST)</span></span> | <span data-ttu-id="db6ad-144">B：订单输入截止时间 (EST)</span><span class="sxs-lookup"><span data-stu-id="db6ad-144">B: Order entry deadlines (EST)</span></span> |
|-----------------------------|--------------------------------|--------------------------------|
| <span data-ttu-id="db6ad-145">星期一</span><span class="sxs-lookup"><span data-stu-id="db6ad-145">Monday</span></span>                      | <span data-ttu-id="db6ad-146">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-146">13:00</span></span>                          | <span data-ttu-id="db6ad-147">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-147">14:00</span></span>                          |
| <span data-ttu-id="db6ad-148">星期二</span><span class="sxs-lookup"><span data-stu-id="db6ad-148">Tuesday</span></span>                     | <span data-ttu-id="db6ad-149">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-149">13:00</span></span>                          | <span data-ttu-id="db6ad-150">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-150">14:00</span></span>                          |
| <span data-ttu-id="db6ad-151">星期三</span><span class="sxs-lookup"><span data-stu-id="db6ad-151">Wednesday</span></span>                   | <span data-ttu-id="db6ad-152">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-152">13:00</span></span>                          | <span data-ttu-id="db6ad-153">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-153">14:00</span></span>                          |
| <span data-ttu-id="db6ad-154">星期四</span><span class="sxs-lookup"><span data-stu-id="db6ad-154">Thursday</span></span>                    | <span data-ttu-id="db6ad-155">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-155">13:00</span></span>                          | <span data-ttu-id="db6ad-156">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-156">14:00</span></span>                          |
| <span data-ttu-id="db6ad-157">星期五</span><span class="sxs-lookup"><span data-stu-id="db6ad-157">Friday</span></span>                      | <span data-ttu-id="db6ad-158">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-158">13:00</span></span>                          | <span data-ttu-id="db6ad-159">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-159">14:00</span></span>                          |

<span data-ttu-id="db6ad-160">您是订单处理员并且位于犹他州，其时区是 MST（山区标准时间）。</span><span class="sxs-lookup"><span data-stu-id="db6ad-160">You're an order processor in Utah, where the time zone is MST (Mountain Standard Time).</span></span> <span data-ttu-id="db6ad-161">因此，假设您在 14:00 MST 前向站点 A 下订单，并且在 12:00 MST 前向站点 B 下订单，则必须满足这两个站点的订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-161">Therefore, provided that you place orders with site A before 14:00 MST and place orders with site B before 12:00 MST, you meet the order entry deadlines for both sites.</span></span>  

<span data-ttu-id="db6ad-162">下表显示站点 A 和站点 B 的订单输入截止时间如何转换为 MST 时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-162">The following table shows how the order entry deadlines for sites A and B are converted to MST time.</span></span>

| <span data-ttu-id="db6ad-163">站点 A：PST</span><span class="sxs-lookup"><span data-stu-id="db6ad-163">Site A: PST</span></span>         | <span data-ttu-id="db6ad-164">站点 A：MST</span><span class="sxs-lookup"><span data-stu-id="db6ad-164">Site A: MST</span></span>        | <span data-ttu-id="db6ad-165">站点 B：EST</span><span class="sxs-lookup"><span data-stu-id="db6ad-165">Site B: EST</span></span>           | <span data-ttu-id="db6ad-166">站点 B：MST</span><span class="sxs-lookup"><span data-stu-id="db6ad-166">Site B: MST</span></span>        |
|---------------------|--------------------|-----------------------|--------------------|
| <span data-ttu-id="db6ad-167">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-167">13:00</span></span>               | <span data-ttu-id="db6ad-168">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-168">14:00</span></span>              | <span data-ttu-id="db6ad-169">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-169">14:00</span></span>                 | <span data-ttu-id="db6ad-170">12:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-170">12:00</span></span>              |

<span data-ttu-id="db6ad-171">**注意：**如果夏时制保存时间调整生效，则相应调整订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-171">**Note:** If adjustment for daylight saving time is in effect, the order entry deadlines are adjusted accordingly.</span></span>

## <a name="example-same-order-entry-deadline-per-site"></a><span data-ttu-id="db6ad-172">示例：每个站点相同的订单输入截止时间</span><span class="sxs-lookup"><span data-stu-id="db6ad-172">Example: Same order entry deadline per site</span></span>
<span data-ttu-id="db6ad-173">您的公司由两个站点构成。</span><span class="sxs-lookup"><span data-stu-id="db6ad-173">Your company consists of two sites.</span></span> <span data-ttu-id="db6ad-174">如下表中所示，这些站点位于不同的时区。</span><span class="sxs-lookup"><span data-stu-id="db6ad-174">The sites are located in different time zones, as shown in the following table.</span></span>

| <span data-ttu-id="db6ad-175">站点 A</span><span class="sxs-lookup"><span data-stu-id="db6ad-175">Site A</span></span>                      | <span data-ttu-id="db6ad-176">站点 B</span><span class="sxs-lookup"><span data-stu-id="db6ad-176">Site B</span></span>                      |
|-----------------------------|-----------------------------|
| <span data-ttu-id="db6ad-177">加利福尼亚</span><span class="sxs-lookup"><span data-stu-id="db6ad-177">California</span></span>                  | <span data-ttu-id="db6ad-178">佛罗里达</span><span class="sxs-lookup"><span data-stu-id="db6ad-178">Florida</span></span>                     |
| <span data-ttu-id="db6ad-179">PST（太平洋标准时间）</span><span class="sxs-lookup"><span data-stu-id="db6ad-179">PST (Pacific Standard Time)</span></span> | <span data-ttu-id="db6ad-180">EST（东部标准时间）</span><span class="sxs-lookup"><span data-stu-id="db6ad-180">EST (Eastern Standard Time)</span></span> |

<span data-ttu-id="db6ad-181">站点 A 和站点 B 都定义了以下订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-181">Sites A and B have defined the following order entry deadlines.</span></span>

| <span data-ttu-id="db6ad-182">一周中的日</span><span class="sxs-lookup"><span data-stu-id="db6ad-182">Day of the week</span></span> | <span data-ttu-id="db6ad-183">PST 和 EST</span><span class="sxs-lookup"><span data-stu-id="db6ad-183">PST and EST</span></span> |
|-----------------|-------------|
| <span data-ttu-id="db6ad-184">星期一</span><span class="sxs-lookup"><span data-stu-id="db6ad-184">Monday</span></span>          | <span data-ttu-id="db6ad-185">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-185">13:00</span></span>       |
| <span data-ttu-id="db6ad-186">星期二</span><span class="sxs-lookup"><span data-stu-id="db6ad-186">Tuesday</span></span>         | <span data-ttu-id="db6ad-187">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-187">13:00</span></span>       |
| <span data-ttu-id="db6ad-188">星期三</span><span class="sxs-lookup"><span data-stu-id="db6ad-188">Wednesday</span></span>       | <span data-ttu-id="db6ad-189">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-189">13:00</span></span>       |
| <span data-ttu-id="db6ad-190">星期四</span><span class="sxs-lookup"><span data-stu-id="db6ad-190">Thursday</span></span>        | <span data-ttu-id="db6ad-191">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-191">13:00</span></span>       |
| <span data-ttu-id="db6ad-192">星期五</span><span class="sxs-lookup"><span data-stu-id="db6ad-192">Friday</span></span>          | <span data-ttu-id="db6ad-193">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-193">13:00</span></span>       |

<span data-ttu-id="db6ad-194">您是订单处理员并且位于犹他州，其时区是 MST。</span><span class="sxs-lookup"><span data-stu-id="db6ad-194">You're an order processor in Utah, where the time zone is MST.</span></span> <span data-ttu-id="db6ad-195">因此，假设您在 14:00 MST 前向站点 A 下订单，并且在 11:00 MST 前向站点 B 下订单，则必须满足这两个站点的订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-195">Therefore, provided that you place orders with site A before 14:00 MST and place orders with site B before 11:00 MST, you meet the order entry deadlines for both sites.</span></span> 

<span data-ttu-id="db6ad-196">下表显示站点 A 和站点 B 的订单输入截止时间如何转换为 MST 时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-196">The following table shows how the order entry deadlines for sites A and B are converted to MST time.</span></span>

| <span data-ttu-id="db6ad-197">站点 A：PST</span><span class="sxs-lookup"><span data-stu-id="db6ad-197">Site A: PST</span></span>         | <span data-ttu-id="db6ad-198">站点 A：MST</span><span class="sxs-lookup"><span data-stu-id="db6ad-198">Site A: MST</span></span>        | <span data-ttu-id="db6ad-199">站点 B：EST</span><span class="sxs-lookup"><span data-stu-id="db6ad-199">Site B: EST</span></span>           | <span data-ttu-id="db6ad-200">站点 B：MST</span><span class="sxs-lookup"><span data-stu-id="db6ad-200">Site B: MST</span></span>        |
|---------------------|--------------------|-----------------------|--------------------|
| <span data-ttu-id="db6ad-201">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-201">13:00</span></span>               | <span data-ttu-id="db6ad-202">14:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-202">14:00</span></span>              | <span data-ttu-id="db6ad-203">13:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-203">13:00</span></span>                 | <span data-ttu-id="db6ad-204">11:00</span><span class="sxs-lookup"><span data-stu-id="db6ad-204">11:00</span></span>              |

<span data-ttu-id="db6ad-205">**注意：**如果夏时制保存时间调整生效，则相应调整订单输入截止时间。</span><span class="sxs-lookup"><span data-stu-id="db6ad-205">**Note:** If adjustment for daylight saving time is in effect, the order entry deadlines are adjusted accordingly.</span></span>

<a name="see-also"></a><span data-ttu-id="db6ad-206">请参阅</span><span class="sxs-lookup"><span data-stu-id="db6ad-206">See also</span></span>
--------

[<span data-ttu-id="db6ad-207">交货计划</span><span class="sxs-lookup"><span data-stu-id="db6ad-207">Delivery schedules</span></span>](delivery-schedules.md)




