---
title: 收入确认重新分配 - 方案 1
description: 本主题介绍了一种重新分配方案，在此方案中输入了两个销售订单，但仅对它们进行了确认。 如果两个以上的销售订单处于确认状态，则相同的方案将产生相似的结果。
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a0add2d4bc01127c1f359736398123a6a3df9fe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969644"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a><span data-ttu-id="472d9-104">收入确认重新分配 - 方案 1</span><span class="sxs-lookup"><span data-stu-id="472d9-104">Revenue recognition reallocation – Scenario 1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="472d9-105">本主题介绍了一种重新分配方案，在此方案中输入了两个销售订单，但仅对它们进行了确认。</span><span class="sxs-lookup"><span data-stu-id="472d9-105">This topic goes through a reallocation scenario where two sales orders are entered, but they are only confirmed.</span></span> <span data-ttu-id="472d9-106">如果两个以上的销售订单处于确认状态，则相同的方案将产生相似的结果。</span><span class="sxs-lookup"><span data-stu-id="472d9-106">The same scenario will produce similar results if more than two sales orders are in a confirmed state.</span></span>

<span data-ttu-id="472d9-107">对于此方案，**总帐参数** 页面的 **收入确认** 选项卡上的 **将账单更正过帐到应收帐款** 选项设置为 **否**（**收入确认 \> 设置 \> 总帐参数**）。</span><span class="sxs-lookup"><span data-stu-id="472d9-107">For this scenario, the **Post invoice corrections to Accounts receivable** option is set to **No** on the **Revenue recognition** tab of the **General ledger parameters** page (**Revenue recognition \> Setup \> General ledger parameters**).</span></span>

<span data-ttu-id="472d9-108">[![“将账单更正过帐到应收帐款”选项设置为“否”](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-108">[![Post invoice corrections to Accounts receivable option set to No](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="472d9-109">为客户 US\_SI\_0003 创建了一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="472d9-109">A sales order is created for customer US\_SI\_0003.</span></span> <span data-ttu-id="472d9-110">客户正在购买笔记本电脑（项目编号 S0012）和支持计划（项目编号 S0008，“持续的工程服务”）。</span><span class="sxs-lookup"><span data-stu-id="472d9-110">The customer is purchasing a laptop (item number S0012) and a support plan for it (item number S0008, "Sustained Engineering Service").</span></span> <span data-ttu-id="472d9-111">笔记本电脑的收入将立即确认（没有收入确认计划）。</span><span class="sxs-lookup"><span data-stu-id="472d9-111">The revenue for the laptop is immediately recognized (there is no revenue recognition schedule).</span></span> <span data-ttu-id="472d9-112">支持计划的收入将延期并在根据合同中日期范围定义的 12 个月内确认。</span><span class="sxs-lookup"><span data-stu-id="472d9-112">The revenue for the support plan will be deferred and recognized over 12 months, as defined by the date range in the contract.</span></span>

<span data-ttu-id="472d9-113">[![笔记本电脑和支持计划的销售订单行](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-113">[![Sales order lines for the laptop and support plan](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="472d9-114">已确认销售订单。</span><span class="sxs-lookup"><span data-stu-id="472d9-114">The sales order is confirmed.</span></span> <span data-ttu-id="472d9-115">因为两个项目都是为收入价格分配设置的，所以在确认销售订单时将计算收入价格。</span><span class="sxs-lookup"><span data-stu-id="472d9-115">Because both items are set up for revenue price allocation, the revenue price is calculated when the sales order is confirmed.</span></span> <span data-ttu-id="472d9-116">您可以查看将在 **收入价格分配** 页面（在 **销售订单** 页面的操作窗格的 **管理** 选项卡上的 **收入确认** 组中，选择 **收入价格分配**）上确认的收入。</span><span class="sxs-lookup"><span data-stu-id="472d9-116">You can view the revenue that will be recognized on the **Revenue price allocation** page (on the **Sales order** page, on the Action Pane, on the **Manage** tab, in the **Revenue recognition** group, select **Revenue price allocation**).</span></span> <span data-ttu-id="472d9-117">笔记本电脑的收入将以 $1,008.01 的金额过帐到收入帐户。</span><span class="sxs-lookup"><span data-stu-id="472d9-117">The revenue for the laptop will be posted to the Revenue account in the amount of $1,008.01.</span></span> <span data-ttu-id="472d9-118">支持计划的收入将以 $190.99 的金额过帐到延期收入帐户。</span><span class="sxs-lookup"><span data-stu-id="472d9-118">The revenue for the support plan will be posted to the Deferred revenue account in the amount of $190.99.</span></span> <span data-ttu-id="472d9-119">收入价格的总和必须等于为获取收入价格分配 ($1,199.00) 而设置的总行数。</span><span class="sxs-lookup"><span data-stu-id="472d9-119">The sum of the revenue prices must equal the sum of the lines that were set up to capture revenue price allocation ($1,199.00).</span></span>

<span data-ttu-id="472d9-120">[![收入价格分配页面](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-120">[![Revenue price allocation page](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="472d9-121">客户选择在销售时不购买安装服务（项目编号 S0001），但后来改变了主意。</span><span class="sxs-lookup"><span data-stu-id="472d9-121">The customer chose not to purchase installation services (item number S0001) at the time of the sale but later changed their mind.</span></span> <span data-ttu-id="472d9-122">因此，为同一客户输入了第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="472d9-122">Therefore, a second sales order is entered for the same customer.</span></span>

<span data-ttu-id="472d9-123">[![安装服务的销售订单行](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-123">[![Sales order line for installation services](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="472d9-124">已确认第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="472d9-124">The second sales order is confirmed.</span></span> <span data-ttu-id="472d9-125">由于此销售订单仅包含一行，因此在确认销售订单时未进行收入价格分配。</span><span class="sxs-lookup"><span data-stu-id="472d9-125">Because this sales order contains only one line, revenue price allocation isn't done when the sales order is confirmed.</span></span> <span data-ttu-id="472d9-126">仅当存在两个或以上的唯一项目并且设置这些项目以进行收入价格分配时，才会发生收入价格分配。</span><span class="sxs-lookup"><span data-stu-id="472d9-126">Revenue price allocation occurs only if there are two or more unique items, and if those items are set up for revenue price allocation.</span></span>

<span data-ttu-id="472d9-127">如果此新销售订单是对客户合同的唯一更改，则现在可以运行重新分配流程。</span><span class="sxs-lookup"><span data-stu-id="472d9-127">If this new sales order is the only change to the customer's contract, the reallocation process can now be run.</span></span> <span data-ttu-id="472d9-128">在两个销售订单之一中，选择 **使用新订单行重新分配价格** 以打开 **使用新订单行重新分配价格** 页面。</span><span class="sxs-lookup"><span data-stu-id="472d9-128">In one of the two sales orders, select **Reallocate price with new order lines** to open the **Reallocate price with new order lines** page.</span></span> <span data-ttu-id="472d9-129">或者，转到 **收入确认 \> 定期任务 \> 使用新订单行重新分配价格**。</span><span class="sxs-lookup"><span data-stu-id="472d9-129">Alternatively, go to **Revenue recognition \> Periodic tasks \> Reallocate price with new order lines**.</span></span> <span data-ttu-id="472d9-130">选择两个销售订单和相应的销售订单行，然后选择 **更新重新分配**。</span><span class="sxs-lookup"><span data-stu-id="472d9-130">Select the two sales orders and the corresponding sales order lines, and then select **Update reallocation**.</span></span> <span data-ttu-id="472d9-131">**重新分配的金额** 列显示每个销售订单行的新收入价格。</span><span class="sxs-lookup"><span data-stu-id="472d9-131">The **Reallocated amount** column shows the new revenue price for each sales order line.</span></span>

<span data-ttu-id="472d9-132">[![“使用新订单行重新分配价格”页面上的新收入价格](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-132">[![New revenue prices on the Reallocate price with new order lines page](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="472d9-133">如果选择 **预期凭证**，则不会显示任何内容，因为尚未过帐任何账单。</span><span class="sxs-lookup"><span data-stu-id="472d9-133">If you select **Expected voucher**, nothing is shown, because no invoices have been posted.</span></span>

<span data-ttu-id="472d9-134">要完成重新分配，请选择 **处理**。</span><span class="sxs-lookup"><span data-stu-id="472d9-134">To complete the reallocation, select **Process**.</span></span> <span data-ttu-id="472d9-135">系统将会向您提示过帐日期，即使未过帐任何内容。</span><span class="sxs-lookup"><span data-stu-id="472d9-135">You're prompted for a posting date, even if nothing is posted.</span></span> <span data-ttu-id="472d9-136">重新分配完成后，每个销售订单的 **收入价格分配** 页面将显示两个销售订单中所有项目的价格分配。</span><span class="sxs-lookup"><span data-stu-id="472d9-136">After the reallocation is completed, the **Revenue price allocation** page for each sales order will show the price allocation for all items across both sales orders.</span></span> <span data-ttu-id="472d9-137">换句话说，每个销售订单的 **收入价格分配** 页面将包含该销售订单上不存在的项目，因为它属于同一合同，但位于不同的销售订单上。</span><span class="sxs-lookup"><span data-stu-id="472d9-137">In other words, the **Revenue price allocation** page for each sales order will include an item that doesn't exist on that sales order, because it's part of the same contract but on a different sales order.</span></span>

> [!TIP]
> <span data-ttu-id="472d9-138">要提供有关为什么显示这些附加项目的上下文，您可以向网格中添加其他列，例如 **重新分配 ID** 和 **销售订单**。</span><span class="sxs-lookup"><span data-stu-id="472d9-138">To provide context about why these additional items are shown, you can add other columns to the grid, such as **Reallocation ID** and **Sales order**.</span></span>
> 
> <span data-ttu-id="472d9-139">[![“收入价格分配”页面上的其他列](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="472d9-139">[![Additional columns on the Revenue price allocations page](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)</span></span>
