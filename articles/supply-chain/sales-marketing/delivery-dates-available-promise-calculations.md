---
title: "订单承诺"
description: "本文提供有关订单承诺的信息。 订单承诺帮助您向客户确切承诺交货日期，并给予您履行这些日期的灵活性。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1581fb0e30260acb84f7e77cb3571055181d8bdc
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="order-promising"></a><span data-ttu-id="68ee3-104">订单承诺</span><span class="sxs-lookup"><span data-stu-id="68ee3-104">Order promising</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68ee3-105">本文提供有关订单承诺的信息。</span><span class="sxs-lookup"><span data-stu-id="68ee3-105">This article provides information about order promising.</span></span> <span data-ttu-id="68ee3-106">订单承诺帮助您向客户确切承诺交货日期，并给予您履行这些日期的灵活性。</span><span class="sxs-lookup"><span data-stu-id="68ee3-106">Order promising helps you reliably promise delivery dates to your customers and gives you flexibility so that you can meet those dates.</span></span>

<span data-ttu-id="68ee3-107">订单承诺计算最早的装运日期和接收日期，它是基于交货日期控制方法和运输天数的。</span><span class="sxs-lookup"><span data-stu-id="68ee3-107">Order promising calculates the earliest ship and receipt dates, and is based on the delivery date control method and transport days.</span></span> <span data-ttu-id="68ee3-108">您可以在四个交货日期控制方法中进行选择：</span><span class="sxs-lookup"><span data-stu-id="68ee3-108">You can select among four delivery date control methods:</span></span>

-   <span data-ttu-id="68ee3-109">**销售提前期** - 销售提前期是创建销售订单和装运物料之间的时间。</span><span class="sxs-lookup"><span data-stu-id="68ee3-109">**Sales lead time** – Sales lead time is the time between creation of the sales order and shipment of the items.</span></span> <span data-ttu-id="68ee3-110">交货日期计算基于默认天数，不考虑库存可用性、已知需求或计划供应。</span><span class="sxs-lookup"><span data-stu-id="68ee3-110">The delivery date calculation is based on a default number of days, and does not consider stock availability, known demand, or planned supply.</span></span>
-   <span data-ttu-id="68ee3-111">**ATP（可承诺）**– ATP 是可用的且可对某一客户在特定日期承诺的物料数量。</span><span class="sxs-lookup"><span data-stu-id="68ee3-111">**ATP (available-to-promise)** – ATP is the quantity of an item that is available and can be promised to a customer on a specific date.</span></span> <span data-ttu-id="68ee3-112">ATP 计算包括未承诺库存、提前期、计划收货和发货。</span><span class="sxs-lookup"><span data-stu-id="68ee3-112">The ATP calculation includes uncommitted inventory, lead times, planned receipts, and issues.</span></span>
-   <span data-ttu-id="68ee3-113">**ATP + 发货宽限期**– 装运日期等于 ATP 日期加上物料的发货宽限期。</span><span class="sxs-lookup"><span data-stu-id="68ee3-113">**ATP + Issue margin** – The shipping date is equal to the ATP date plus the issue margin for the item.</span></span> <span data-ttu-id="68ee3-114">发货宽限期是准备物料以进行装运所需的时间。</span><span class="sxs-lookup"><span data-stu-id="68ee3-114">The issue margin is the time that is required to prepare the items for shipment.</span></span>
-   <span data-ttu-id="68ee3-115">**CTP（可承诺量）**– 通过分解计算可用性。</span><span class="sxs-lookup"><span data-stu-id="68ee3-115">**CTP (capable-to-promise)** – Availability is calculated through explosion.</span></span>

## <a name="atp-calculations"></a><span data-ttu-id="68ee3-116">ATP 计算</span><span class="sxs-lookup"><span data-stu-id="68ee3-116">ATP calculations</span></span>
<span data-ttu-id="68ee3-117">通过使用“含预期的累积 ATP”方法计算 ATP 数量。</span><span class="sxs-lookup"><span data-stu-id="68ee3-117">The ATP quantity is calculated by using the “cumulative ATP with look-ahead” method.</span></span> <span data-ttu-id="68ee3-118">这一计算 ATP 的方法的主要优点在于，它可以在收货之间的发货总和大于最新收货时（例如，必须使用来自更早收货的数量来满足需求时）处理案例。</span><span class="sxs-lookup"><span data-stu-id="68ee3-118">The main advantage of this ATP calculation method is that it can handle cases where the sum of issues among receipts is more than the latest receipt (for example, when a quantity from an earlier receipt must be used to meet a requirement).</span></span> <span data-ttu-id="68ee3-119">“含预期的累积 ATP”计算方法包括所有发货，直到累积收货数量超过累积发货数量。</span><span class="sxs-lookup"><span data-stu-id="68ee3-119">The “cumulative ATP with look-ahead” calculation method includes all issues until the cumulative quantity to receive exceeds the cumulative quantity to issue.</span></span> <span data-ttu-id="68ee3-120">因此，该 ATP 计算方法评估更早期间的某些数量是否可用于以后的期间。</span><span class="sxs-lookup"><span data-stu-id="68ee3-120">Therefore, this ATP calculation method evaluates whether some of the quantity from an earlier period can be used in a later period.</span></span>  

<span data-ttu-id="68ee3-121">该 ATP 数量是第一个期间中的未承诺库存余额。</span><span class="sxs-lookup"><span data-stu-id="68ee3-121">The ATP quantity is the uncommitted inventory balance in the first period.</span></span> <span data-ttu-id="68ee3-122">通常，会为计划收货的每个期间计算它。</span><span class="sxs-lookup"><span data-stu-id="68ee3-122">Typically, it's calculated for each period in which a receipt is scheduled.</span></span> <span data-ttu-id="68ee3-123">程序将按天数计算 ATP 期间，并且将当前日期计算为该 ATP 数量的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="68ee3-123">The program calculates the ATP period in days and calculates the current date as the first date for the ATP quantity.</span></span> <span data-ttu-id="68ee3-124">在第一个期间中，ATP 将包括现有库存量减去到期和逾期的客户订单。</span><span class="sxs-lookup"><span data-stu-id="68ee3-124">In the first period, ATP includes on-hand inventory minus customer orders that are due and overdue.</span></span>  

<span data-ttu-id="68ee3-125">ATP 使用以下公式计算：</span><span class="sxs-lookup"><span data-stu-id="68ee3-125">ATP is calculated by using the following formula:</span></span>  

<span data-ttu-id="68ee3-126">ATP = 前一期间的 ATP + 当前期间的收货 - 当前期间的发货 - 截至以下期间前的各个将来期间的净发货数量：在所有将来期间（直到并且包括该将来期间）的收货之和超过发货之和（直到并且包括该将来期间）时的期间。</span><span class="sxs-lookup"><span data-stu-id="68ee3-126">ATP = ATP for the previous period + Receipts for the current period – Issues for the current period – Net issue quantity for each future period until the period when the sum of receipts for all future periods, up to and including the future period, exceeds the sum of issues up to and including the future period.</span></span>  

<span data-ttu-id="68ee3-127">在没有要考虑的更多发货或收货时，用于以下日期的 ATP 数量与最新计算的 ATP 数量相同。</span><span class="sxs-lookup"><span data-stu-id="68ee3-127">When there are no more issues or receipts to consider, the ATP quantity for the following dates is the same as the latest calculated ATP quantity.</span></span>  

<span data-ttu-id="68ee3-128">如果在执行 ATP 检查时未提供用于某一物料的所有维度，则在发货和收货时仍可以指定它们。</span><span class="sxs-lookup"><span data-stu-id="68ee3-128">If not all the dimensions that are used for an item are given when the ATP check is completed, they can still be specified on the issue and receipts.</span></span> <span data-ttu-id="68ee3-129">在此情况下，在 ATP 计算中，收货和发货必须聚合到现有维度中，以便减少在 ATP 计算中使用的收货行和发货行的数目。</span><span class="sxs-lookup"><span data-stu-id="68ee3-129">In this case, in the ATP calculation, the receipts and issues must be aggregated to the existing dimensions to reduce the number of receipt and issue lines that are used in the ATP calculation.</span></span>  

<span data-ttu-id="68ee3-130">显示的 ATP 数量始终大于或等于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="68ee3-130">The ATP quantity that is shown is always greater than or equal to 0 (zero).</span></span> <span data-ttu-id="68ee3-131">如果该计算返回负的 ATP 数量（例如，如果以前承诺的数量超出可用数量），程序会自动将数量设置为 **0**。</span><span class="sxs-lookup"><span data-stu-id="68ee3-131">If the calculation returns a negative ATP quantity (for example, if the quantity that was previously promised exceeds the available quantity), the program automatically sets the quantity to **0**.</span></span>

### <a name="example"></a><span data-ttu-id="68ee3-132">示例</span><span class="sxs-lookup"><span data-stu-id="68ee3-132">Example</span></span>

<span data-ttu-id="68ee3-133">**“ATP 后向需求时限”**字段控制向后多长时间查找延期需求订单或库存发货。</span><span class="sxs-lookup"><span data-stu-id="68ee3-133">The **ATP backward demand time fence** field controls how far back in time to look for delayed demand orders or inventory issues.</span></span> <span data-ttu-id="68ee3-134">**“ATP 后向供应时限”**字段控制向后多长时间查找延期供应订单或库存收货。</span><span class="sxs-lookup"><span data-stu-id="68ee3-134">The **ATP backward supply time fence** field controls how far back in time to look for delayed supply orders or inventory receipts.</span></span> <span data-ttu-id="68ee3-135">例如，如果只延迟七天的订单应被考虑到 ATP 计算中，则两个字段都应设置为 **7**。</span><span class="sxs-lookup"><span data-stu-id="68ee3-135">For example, if orders that are delayed by only seven days should be considered in the ATP calculation, both fields should be set to **7**.</span></span>  

<span data-ttu-id="68ee3-136">**“ATP 延迟需求偏移时间”**和**“ATP 延迟供应偏移时间”**字段控制何时将延期需求或供应考虑到 ATP 计算中。</span><span class="sxs-lookup"><span data-stu-id="68ee3-136">The **ATP delayed demand offset time** and **ATP delayed supply offset time** fields control when the delayed demand or supply will be considered in the ATP calculation.</span></span> <span data-ttu-id="68ee3-137">例如，如果延期供应和需求应被考虑到 ATP 计算中，则两个字段都应设置为 **2**。</span><span class="sxs-lookup"><span data-stu-id="68ee3-137">For example, if the delayed supply and demand should be considered in the ATP calculation the day after tomorrow, both fields should be set to **2**.</span></span> <span data-ttu-id="68ee3-138">值为**“2”**表示应被考虑到 ATP 计算中的延期采购订单的物料数量将在当前日期之后两天可供查看。</span><span class="sxs-lookup"><span data-stu-id="68ee3-138">A value of **2** means that the quantity of an item on a delayed purchase order that should be considered in the ATP calculation will be seen as available two days after the current date.</span></span>  

<span data-ttu-id="68ee3-139">对于以下示例，在**“ATP 后向需求时限”**和**“ATP 后向供应时限”**字段中输入了**“7”**，在**“ATP 延迟需求偏移时间”**和**“ATP 延迟供应偏移时间”**字段中输入了**“1”**。</span><span class="sxs-lookup"><span data-stu-id="68ee3-139">For the following example, **7** is entered in the **ATP backward demand time fence** and **ATP backward supply time fence** fields, and **1** is entered in the **ATP delayed demand offset time** and **ATP delayed supply offset time** fields.</span></span>  

<span data-ttu-id="68ee3-140">应在三天之前收到的 200 件产品的采购订单尚未接收。</span><span class="sxs-lookup"><span data-stu-id="68ee3-140">A purchase order for 200 pieces of a product that should have been received three days ago hasn't been received yet.</span></span> <span data-ttu-id="68ee3-141">因此，昨天应装运的 75件 相同产品的销售订单行尚未装运。</span><span class="sxs-lookup"><span data-stu-id="68ee3-141">Therefore, a sales order line for 75 pieces of the same product that should have been shipped yesterday hasn't been shipped.</span></span>  

<span data-ttu-id="68ee3-142">客户致电并要订购 150 件同一产品。</span><span class="sxs-lookup"><span data-stu-id="68ee3-142">A customer calls and wants to order 150 pieces of the same product.</span></span> <span data-ttu-id="68ee3-143">在您确认产品的可用性时，您会发现将在 10 天交货的其他 100 件产品的采购订单。</span><span class="sxs-lookup"><span data-stu-id="68ee3-143">When you verify the availability of the product, you find that another purchase order for 100 pieces of the product will be delivered 10 days later.</span></span>  

<span data-ttu-id="68ee3-144">您为该产品创建销售订单行并输入**“150”**的数量。</span><span class="sxs-lookup"><span data-stu-id="68ee3-144">You create a sales order line for the product and enter **150** as the quantity.</span></span>  

<span data-ttu-id="68ee3-145">由于交货日期控制方法是 ATP，所以会计算 ATP 数据以找到最早的可能装运日期。</span><span class="sxs-lookup"><span data-stu-id="68ee3-145">Because the delivery date control is method is ATP, the ATP data is calculated to find the earliest possible ship date.</span></span> <span data-ttu-id="68ee3-146">基于设置，延期采购订单和销售订单会被考虑，并且当前日期生成的 ATP 数量是 0。</span><span class="sxs-lookup"><span data-stu-id="68ee3-146">Based on the settings, the delayed purchase order and sales order are considered, and the resulting ATP quantity for the current date is 0.</span></span> <span data-ttu-id="68ee3-147">明天，当预计会收到延期采购订单时，会将 ATP 数量计算为大于 0（在这种情况下，它被计算为 125）。</span><span class="sxs-lookup"><span data-stu-id="68ee3-147">Tomorrow, when the delayed purchase order is expected to be received, the ATP quantity is calculated as more than 0 (in this case, it's calculated as 125).</span></span> <span data-ttu-id="68ee3-148">但是，从现在起 10 天，当预期接收 100 件的其他采购订单时，ATP 数量将变为超过 150。</span><span class="sxs-lookup"><span data-stu-id="68ee3-148">However, 10 days from now, when the additional purchase order for 100 pieces is expected to be received, the ATP quantity becomes more than 150.</span></span>  

<span data-ttu-id="68ee3-149">因此，基于 ATP 计算，装运日期被设置为从现在起 10 天。</span><span class="sxs-lookup"><span data-stu-id="68ee3-149">Therefore, the ship date is set to 10 days from now, based on the ATP calculation.</span></span> <span data-ttu-id="68ee3-150">因此，您告知客户请求数量的可以为从现在起的 10 天交货。</span><span class="sxs-lookup"><span data-stu-id="68ee3-150">Therefore, you tell the customer that the requested quantity can be delivered 10 days from now.</span></span>




