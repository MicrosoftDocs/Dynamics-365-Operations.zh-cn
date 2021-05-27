---
title: 税款计算性能影响交易
description: 本主题提供与税款计算性能及其对交易的影响有关的故障排除信息。
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020131"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="f2d8c-103">税款计算性能影响交易</span><span class="sxs-lookup"><span data-stu-id="f2d8c-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2d8c-104">有时，交易会受到税款计算存在的性能问题的影响。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="f2d8c-105">要解决此问题，请根据需要按照以下各节中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="f2d8c-106">查看交易行计数</span><span class="sxs-lookup"><span data-stu-id="f2d8c-106">Review the transaction line count</span></span>

<span data-ttu-id="f2d8c-107">确定交易是否有很多行（例如，多于几百行）。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="f2d8c-108">如果没有，请转到下一节。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="f2d8c-109">如果交易确实有几百行，应延迟税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="f2d8c-110">有关详细信息，请参阅[为日记帐启用延迟税款计算](enable-delayed-tax-calculation.md)。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="f2d8c-111">接下来，您可以确定是否满足以下任何条件：</span><span class="sxs-lookup"><span data-stu-id="f2d8c-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="f2d8c-112">有来自大文件的导入交易。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="f2d8c-113">多个会话同时处理同一个交易税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="f2d8c-114">交易有多个行，视图会实时更新。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="f2d8c-115">例如，更改行的字段时，会实时更新 **普通日记帐** 页上的 **计算销售税金额** 字段。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="f2d8c-116">[![日记帐凭证页上的“计算销售税金额”字段](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="f2d8c-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="f2d8c-117">如果满足这些条件的任何一个，请延迟税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="f2d8c-118">查看调用堆栈</span><span class="sxs-lookup"><span data-stu-id="f2d8c-118">Review the call stack</span></span>

<span data-ttu-id="f2d8c-119">查看调用堆栈，确定是否多次调用了税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="f2d8c-120">如果不是，请转到下一节。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="f2d8c-121">如果调用堆栈被多次调用，请按照下列步骤帮助减少税款计算次数。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="f2d8c-122">如果日记帐已考虑了交易，请延迟税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="f2d8c-123">有关详细信息，请参阅[为日记帐启用延迟税款计算](enable-delayed-tax-calculation.md)。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="f2d8c-124">如果交易是采购订单，应用程序版本晚于 10.0.15，可以通过启用 **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** 的外部测试将税款计算延迟到最终计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="f2d8c-125">查看调用堆栈时间线</span><span class="sxs-lookup"><span data-stu-id="f2d8c-125">Review the call stack timeline</span></span>

<span data-ttu-id="f2d8c-126">查看调用堆栈时间线，确定是否存在以下问题。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="f2d8c-127">如果存在，启用 **TaxUncommittedDoIsolateScopeFlighting** 的外部测试来解决该问题。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="f2d8c-128">交易将导致系统停止响应，直到会话结束。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="f2d8c-129">因此，交易无法计算税收结果。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="f2d8c-130">下图显示了您收到的“会话已结束”消息框。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="f2d8c-131">[![会话已结束消息](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="f2d8c-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="f2d8c-132">**TaxUncommitted** 方法会比其他方法花费更多时间。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="f2d8c-133">例如，在下图中，**TaxUncommitted::updateTaxUncommitted()** 方法需要 43,347.42 秒，而其他方法则需要 0.09 秒。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="f2d8c-134">[![方法持续时间](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="f2d8c-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="f2d8c-135">自定义和调用税款计算</span><span class="sxs-lookup"><span data-stu-id="f2d8c-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="f2d8c-136">自定义时，请勿在每一行的 **insert()** 或 **update()** 方法中调用税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="f2d8c-137">应在交易级别调用税款计算。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="f2d8c-138">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="f2d8c-138">Determine whether customization exists</span></span>

<span data-ttu-id="f2d8c-139">如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="f2d8c-140">如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。</span><span class="sxs-lookup"><span data-stu-id="f2d8c-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
