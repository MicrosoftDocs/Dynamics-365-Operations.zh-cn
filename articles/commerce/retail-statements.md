---
title: 零售报表
description: 本主题描述如何创建报表和过帐。
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410605"
---
# <a name="retail-statements"></a><span data-ttu-id="881f5-103">零售对帐单</span><span class="sxs-lookup"><span data-stu-id="881f5-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="881f5-104">在 Dynamics 365 Commerce 中，报表过帐流程用于说明在云销售点 (POS) 或现代 POS (MPOS) 中发生的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="881f5-105">报表过帐流程使用配送计划将一组 POS 交易记录导入到总部 (HQ) 客户端。</span><span class="sxs-lookup"><span data-stu-id="881f5-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="881f5-106">在 **商业参数** 和 **商店** 页定义的参数用于选择导入到单个报表的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="881f5-107">下图显示了报表过帐流程。</span><span class="sxs-lookup"><span data-stu-id="881f5-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="881f5-108">在此流程中，通过使用商业调度将 POS 中记录的交易记录传输给客户端。</span><span class="sxs-lookup"><span data-stu-id="881f5-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="881f5-109">在客户端接收交易记录后，你可以为商店创建、计算和过帐交易记录报表。</span><span class="sxs-lookup"><span data-stu-id="881f5-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="881f5-110">[![报表过帐流程](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="881f5-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="881f5-111">创建和过帐报表</span><span class="sxs-lookup"><span data-stu-id="881f5-111">Creating and posting statements</span></span>

<span data-ttu-id="881f5-112">您可以手动创建报表或通过使用该批处理您可以设置全天定期运行。</span><span class="sxs-lookup"><span data-stu-id="881f5-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="881f5-113">在这两种情况下，使用以下步骤来创建和过帐报表。</span><span class="sxs-lookup"><span data-stu-id="881f5-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="881f5-114">创建报表</span><span class="sxs-lookup"><span data-stu-id="881f5-114">Create the statement</span></span>

<span data-ttu-id="881f5-115">此步骤标识手动创建商店报表。</span><span class="sxs-lookup"><span data-stu-id="881f5-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="881f5-116">如果您配置批处理，您可以基于您定义的计划自动创建所有商店的报表。</span><span class="sxs-lookup"><span data-stu-id="881f5-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="881f5-117">计算报表</span><span class="sxs-lookup"><span data-stu-id="881f5-117">Calculate the statement</span></span>

<span data-ttu-id="881f5-118">在此步骤中，基于在 **商业参数** 和 **商店** 页为每个商店定义的标准来选择交易记录行。</span><span class="sxs-lookup"><span data-stu-id="881f5-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="881f5-119">在这些页面中，你定义条件并指定如何计算交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="881f5-120">在你计算报表之前，若要查看包含在报表中的交易记录列表，请使用 **交易记录** 页。</span><span class="sxs-lookup"><span data-stu-id="881f5-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="881f5-121">报表计算使用来自收银机的钱币清点作为盘点金额。</span><span class="sxs-lookup"><span data-stu-id="881f5-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="881f5-122">或者，您可以手动输入该盘点金额。</span><span class="sxs-lookup"><span data-stu-id="881f5-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="881f5-123">报表显示交易记录的销售额和所有支付方式中实际盘点金额之间的差额。</span><span class="sxs-lookup"><span data-stu-id="881f5-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="881f5-124">只要此差额小于为商店定义的最大过帐差额就将报表过帐。</span><span class="sxs-lookup"><span data-stu-id="881f5-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="881f5-125">报表计算流程使用全局编号规则。</span><span class="sxs-lookup"><span data-stu-id="881f5-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="881f5-126">在计算报表时，计算包括以下任务：</span><span class="sxs-lookup"><span data-stu-id="881f5-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="881f5-127">对于所选日期范围，标记以前报表计算中不包括的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="881f5-128">计算在所选交易记录中支付的总金额。</span><span class="sxs-lookup"><span data-stu-id="881f5-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="881f5-129">结果将显示在报表行内，根据报表方法：</span><span class="sxs-lookup"><span data-stu-id="881f5-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="881f5-130">如果报表方法是 **总计**，则在所选交易记录中为每种付款方式都创建一行。</span><span class="sxs-lookup"><span data-stu-id="881f5-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="881f5-131">如果报表方法是 **职员**，则在所选职员成员执行的交易记录中为每种付款方式都创建一行。</span><span class="sxs-lookup"><span data-stu-id="881f5-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="881f5-132">如果报表方法是 **POS 终端**，则在所选收银机执行的交易记录中为每种付款方式都创建一行。</span><span class="sxs-lookup"><span data-stu-id="881f5-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="881f5-133">如果报表方法是 **班次**，则在班次期间执行的交易记录中为每种付款方式都创建一行。</span><span class="sxs-lookup"><span data-stu-id="881f5-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="881f5-134">如果在 **商店** 页选中 **按报表拆分方法** 复选框，则基于在 **报表方法** 字段中选择的值创建单独的报表。</span><span class="sxs-lookup"><span data-stu-id="881f5-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="881f5-135">如果你的商店营业时间延长到午夜之后，你可以基于工作日结束时间（而不是日历日结束时间）配置报表过帐。</span><span class="sxs-lookup"><span data-stu-id="881f5-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="881f5-136">在 **商店** 页，在 **报表/结算** 快速选项卡上，在 **工作日结束时** 字段中，输入工作日报表中包括的必须纪录的最后一次交易记录的时间。</span><span class="sxs-lookup"><span data-stu-id="881f5-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="881f5-137">选择 **按工作日过帐** 复选框以将相同工作日中的交易记录过帐。</span><span class="sxs-lookup"><span data-stu-id="881f5-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="881f5-138">当将报表过帐时，在相同工作日内记录的交易记录可以包括在相同销售订单中，即使有些交易记录发生在午夜前，而其他交易记录发生在午夜后。</span><span class="sxs-lookup"><span data-stu-id="881f5-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="881f5-139">示例：对于扩展为两个日历日的一个工作日的过帐报表</span><span class="sxs-lookup"><span data-stu-id="881f5-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="881f5-140">商店的营业时间是上午 8:00 至凌晨 3:00，并且在商店配置中选择 **按工作日过帐** 复选框。</span><span class="sxs-lookup"><span data-stu-id="881f5-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="881f5-141">在 5 月 31 日，商店记录上午 8:00 至午夜之间的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="881f5-142">商店还记录 6 月 1 日凌晨 12:01 至凌晨 3:00 之间的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="881f5-143">当商店在工作日结束过帐报表时，生成包括上午 8:00 至次日凌晨 3:00 之间记录的所有交易记录的销售订单，即便是这些交易记录发生在 5 月 31 日和 6 月 1 日两天。</span><span class="sxs-lookup"><span data-stu-id="881f5-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="881f5-144">如果同一商店清除 **按工作日过帐** 复选框，那么当商店在工作日结束过帐报表时将生成单独的销售订单。</span><span class="sxs-lookup"><span data-stu-id="881f5-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="881f5-145">一个销售订单包括在 5 月 31 日上午 8:00 至午夜之间的营业时间记录的交易记录，并且第二个销售订单包括在 6 月 1 日凌晨 12:01 至凌晨 3:00 之间的营业时间记录的交易记录。</span><span class="sxs-lookup"><span data-stu-id="881f5-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="881f5-146">在创建报表前，您在报表期间应关闭班次。</span><span class="sxs-lookup"><span data-stu-id="881f5-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="881f5-147">将报表过帐</span><span class="sxs-lookup"><span data-stu-id="881f5-147">Post the statement</span></span>

<span data-ttu-id="881f5-148">在您过帐报表时，将针对报表中的销售创建销售订单和发票。</span><span class="sxs-lookup"><span data-stu-id="881f5-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="881f5-149">对于分配给商店的默认客户，将付现自运的销售聚合到一个销售订单和发票上。</span><span class="sxs-lookup"><span data-stu-id="881f5-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="881f5-150">在 POS 中将客户添加到交易记录所针对的销售会生成单独的销售订单和发票，每个针对一个独有客户。</span><span class="sxs-lookup"><span data-stu-id="881f5-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="881f5-151">付款日志在报表中自动为付款创建，并且库存，为 POS 商店更新。</span><span class="sxs-lookup"><span data-stu-id="881f5-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
