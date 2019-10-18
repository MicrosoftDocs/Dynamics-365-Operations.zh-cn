---
title: 部分金额的客户付款
description: 有时客户付款低于的发票金额。 本文介绍处理此情况不同的选项。 可供您使用的选项取决于您的业务要求和配置。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymEntry
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a74803d3adf71ef1495ec5b42753d0988cea4133
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189077"
---
# <a name="customer-payments-for-a-partial-amount"></a><span data-ttu-id="61e66-105">部分金额的客户付款</span><span class="sxs-lookup"><span data-stu-id="61e66-105">Customer payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61e66-106">有时客户付款低于的发票金额。</span><span class="sxs-lookup"><span data-stu-id="61e66-106">Sometimes, customers make a payment that is less than the amount of an invoice.</span></span> <span data-ttu-id="61e66-107">本文介绍处理此情况不同的选项。</span><span class="sxs-lookup"><span data-stu-id="61e66-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="61e66-108">可供您使用的选项取决于您的业务要求和配置。</span><span class="sxs-lookup"><span data-stu-id="61e66-108">The options that are available to you depend on your business requirements and configuration.</span></span>

<a name="partial-payment-with-no-discount"></a><span data-ttu-id="61e66-109">无折扣的部分付款</span><span class="sxs-lookup"><span data-stu-id="61e66-109">Partial payment with no discount</span></span>
--------------------------------

<span data-ttu-id="61e66-110">客户可以进行部分付款，因为他们手头上没有足够的现金来完全支付发票，或者因为发票上的某个物料存在争议。</span><span class="sxs-lookup"><span data-stu-id="61e66-110">Customers might make a partial payment because they just don't have enough cash on hand to pay the invoice in full, or because there is a dispute about an item on the invoice.</span></span> <span data-ttu-id="61e66-111">在这种情况下，可以利用付款来部分结算发票。</span><span class="sxs-lookup"><span data-stu-id="61e66-111">In this situation, the invoice can be partially settled with the payment.</span></span> <span data-ttu-id="61e66-112">发票将保持未结状态并显示剩余未结金额。</span><span class="sxs-lookup"><span data-stu-id="61e66-112">The invoice will remain open and will show a balance.</span></span>

## <a name="discount-amounts"></a><span data-ttu-id="61e66-113">折扣金额</span><span class="sxs-lookup"><span data-stu-id="61e66-113">Discount amounts</span></span>
<span data-ttu-id="61e66-114">您可以在到期日期前为客户支付的发票提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="61e66-114">You can offer customers a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="61e66-115">例如，如果发票在 10 天内付款，您输入 100.00 的发票，该发票指定 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="61e66-115">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="61e66-116">到期期限为 30 天。</span><span class="sxs-lookup"><span data-stu-id="61e66-116">The due-date terms are 30 days.</span></span> <span data-ttu-id="61e66-117">如果您在 10 天内收到 98.00 的付款，则输入 98.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="61e66-117">If you receive a payment of 98.00 within 10 days, you enter the payment for 98.00.</span></span> <span data-ttu-id="61e66-118">然后，当发票标记为已结算时，现金折扣将自动执行。</span><span class="sxs-lookup"><span data-stu-id="61e66-118">Then, when the invoice is marked for settlement, the cash discount it taken automatically.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="61e66-119">使用现金折扣的部分付款</span><span class="sxs-lookup"><span data-stu-id="61e66-119">Partial payments with cash discounts</span></span>
<span data-ttu-id="61e66-120">当客户进行部分付款后，他们可以计划再进行一次部分付款以完全结算发票。</span><span class="sxs-lookup"><span data-stu-id="61e66-120">When customers make a partial payment, they might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="61e66-121">要为部分付款获取现金折扣，则必须将**应收帐款参数**页面上的**计算部分付款的现金折扣**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="61e66-121">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Accounts receivable parameters** page.</span></span> 

<span data-ttu-id="61e66-122">例如，如果发票在签发后的 10 天内付款，您将提供 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="61e66-122">For example, you offer a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="61e66-123">100.00 的发票已过帐。</span><span class="sxs-lookup"><span data-stu-id="61e66-123">An invoice is posted for 100.00.</span></span> <span data-ttu-id="61e66-124">如果您在 10 天内收到 49.00 的付款，您将在付款日记帐中输入 49.00 的贷记。</span><span class="sxs-lookup"><span data-stu-id="61e66-124">If you receive a payment of 49.00 within 10 days, you enter a credit of 49.00 in a payment journal.</span></span> <span data-ttu-id="61e66-125">在您在**结算交易记录**页面上结算部分付款时，**1.00** 将出现在**要提取的现金折扣金额**字段中。</span><span class="sxs-lookup"><span data-stu-id="61e66-125">When you settle the partial payment on the **Settle transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> <span data-ttu-id="61e66-126">折扣金额过帐到现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="61e66-126">The discount amount is posted to a cash discount account.</span></span> 

> [!NOTE] 
> <span data-ttu-id="61e66-127">如果您输入部分付款并在**要结算的金额**字段中保留完整的发票金额，则在您过帐交易记录时，**要提取的现金折扣金额**字段将自动重新计算。</span><span class="sxs-lookup"><span data-stu-id="61e66-127">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-discounts"></a><span data-ttu-id="61e66-128">使用折扣的贷方通知单</span><span class="sxs-lookup"><span data-stu-id="61e66-128">Credit notes with discounts</span></span>
<span data-ttu-id="61e66-129">如果客户退回某个发票上的物料，您可能发出贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="61e66-129">If customers return some of the items on an invoice, you might issue a credit note.</span></span> <span data-ttu-id="61e66-130">如果在原始发票上获得了现金折扣，客户的贷项通知单应该是由客户获得的现金折扣的净额。</span><span class="sxs-lookup"><span data-stu-id="61e66-130">If a cash discount was taken on the original invoice, the credit memo to the customer should be net of the cash discount that was taken by the customer.</span></span> <span data-ttu-id="61e66-131">如果**应收账款参数**页面上的**计算贷方通知单的现金折扣**选项设置为**是**，则将自动计算贷方通知单的折扣。</span><span class="sxs-lookup"><span data-stu-id="61e66-131">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts receivable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="61e66-132">例如，如果发票在签发后的 10 天内付款，您提供了指定 2% 的现金折扣的付款期限。</span><span class="sxs-lookup"><span data-stu-id="61e66-132">For example, you offered terms of payment that specify a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="61e66-133">100.00 的发票已过帐，并且客户获得了现金折扣。</span><span class="sxs-lookup"><span data-stu-id="61e66-133">An invoice for 100.00 was posted, and the customer took the cash discount.</span></span> <span data-ttu-id="61e66-134">如果客户退回货物，并且您发出贷方通知单，那么您可以输入 -100.00 的贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="61e66-134">If the customer returns the goods and you issue a credit note, you can enter the credit note for -100.00.</span></span> <span data-ttu-id="61e66-135">当您在**结算未结交易记录**页面上查看贷方通知单时，**98.00** 将出现在**要结算的金额**字段中，并且 **-2.00** 将出现在**现金折扣金额**字段中。</span><span class="sxs-lookup"><span data-stu-id="61e66-135">When you view the credit note on the **Settle open transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="61e66-136">折扣金额过帐到现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="61e66-136">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="61e66-137">超额支付/支付不足金额</span><span class="sxs-lookup"><span data-stu-id="61e66-137">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="61e66-138">当客户进行付款时，可能还有必须结算的数量非常少的金额。</span><span class="sxs-lookup"><span data-stu-id="61e66-138">When customers make a payment, there might be a very small amount that must still be settled.</span></span> <span data-ttu-id="61e66-139">例如，您为客户开票 1,000.00，而客户支付 999.90。</span><span class="sxs-lookup"><span data-stu-id="61e66-139">For example, you invoice the customer for 1,000.00, and the customer pays 999.90.</span></span> <span data-ttu-id="61e66-140">如果剩余的金额少于为**应收账款参数**页面上的超额支付或不足支付指定的金额，差额将自动过帐到超额支付/不足支付会计科目。</span><span class="sxs-lookup"><span data-stu-id="61e66-140">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts receivable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>

## <a name="full-settlement"></a><span data-ttu-id="61e66-141">完全结算</span><span class="sxs-lookup"><span data-stu-id="61e66-141">Full settlement</span></span>
<span data-ttu-id="61e66-142">当剩余金额不会被支付但大于在**应付账款参数**页面上指定的不足支付金额时，客户可进行部分付款。</span><span class="sxs-lookup"><span data-stu-id="61e66-142">Customers might make a partial payment where the remaining amount won't be paid but is greater than the underpayment amount that is specified on the **Account payable parameters** page.</span></span> <span data-ttu-id="61e66-143">如果您要将发票标记为完全结算，则可以使用**结算交易记录**页面上的**完全结算**选项。</span><span class="sxs-lookup"><span data-stu-id="61e66-143">If you want to mark the invoice as fully settled, you can use the **Full settlement** option on the **Settle transaction** page.</span></span> <span data-ttu-id="61e66-144">（您可以使用 Configuration key 启用完全结算功能。）例如，发票被执行 1,000.00 的过帐，并且客户进行了 990.00 付款的付款。</span><span class="sxs-lookup"><span data-stu-id="61e66-144">(You can enable the full settlement functionality by using a configuration key.) For example, an invoice is posted for 1,000.00, and the customer makes a payment of 990.00.</span></span> <span data-ttu-id="61e66-145">您已同意客户不必支付剩余的 10.00。</span><span class="sxs-lookup"><span data-stu-id="61e66-145">You've agreed that the customer doesn't have to pay the remaining 10.00.</span></span> <span data-ttu-id="61e66-146">在将发票标记为已结算后，您还可以标记选择**完全结算**。</span><span class="sxs-lookup"><span data-stu-id="61e66-146">After you mark the invoice for settlement, you can also mark select **Full settlement**.</span></span> <span data-ttu-id="61e66-147">发票随后将被视为完全结算。</span><span class="sxs-lookup"><span data-stu-id="61e66-147">The invoice will then be considered fully settled.</span></span> <span data-ttu-id="61e66-148">10.00 的差额将作为额外的现金折扣金额过帐到现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="61e66-148">The 10.00 difference is posted to a cash discount account as an additional cash discount amount.</span></span>


<span data-ttu-id="61e66-149">有关详细信息，请参阅[存入客户付款](tasks/deposit-customer-payments.md)。</span><span class="sxs-lookup"><span data-stu-id="61e66-149">For more information, see [Deposit customer payments](tasks/deposit-customer-payments.md).</span></span>
