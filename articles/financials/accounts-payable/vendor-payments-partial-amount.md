---
title: "部分金额的供应商付款"
description: "有时您可以向低于发票金额的供应商付款。 本文介绍处理此情况不同的选项。 可供您使用的选项取决于您的业务要求和配置。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cc8e2864343b5e9fee8eaf058a51360d15e425a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="63aec-105">部分金额的供应商付款</span><span class="sxs-lookup"><span data-stu-id="63aec-105">Vendor payments for a partial amount</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="63aec-106">有时您可以向低于发票金额的供应商付款。</span><span class="sxs-lookup"><span data-stu-id="63aec-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="63aec-107">本文介绍处理此情况不同的选项。</span><span class="sxs-lookup"><span data-stu-id="63aec-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="63aec-108">可供您使用的选项取决于您的业务要求和配置。</span><span class="sxs-lookup"><span data-stu-id="63aec-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="63aec-109">现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="63aec-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="63aec-110">供应商可以在到期日期前提供您支付的发票一个现金折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="63aec-111">例如，如果发票在 10 天内支付，您输入金额为 100.00 的发票，指定 2% 现金折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="63aec-112">到期期限为 30 天。</span><span class="sxs-lookup"><span data-stu-id="63aec-112">The due date terms are 30 days.</span></span> <span data-ttu-id="63aec-113">如果付款方案使用现金折扣作为选择发票的条件，并且，如果该方案在现金折扣日期或之前运行，为付款选择发票，付款创建为 98.00。</span><span class="sxs-lookup"><span data-stu-id="63aec-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="63aec-114">现金折扣还可以为手动创建的一次性付款获取。</span><span class="sxs-lookup"><span data-stu-id="63aec-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="63aec-115">使用现金折扣的部分付款</span><span class="sxs-lookup"><span data-stu-id="63aec-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="63aec-116">在进行部分付款时，您可以计划进行部分付款以完全结算发票。</span><span class="sxs-lookup"><span data-stu-id="63aec-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="63aec-117">要为部分付款获取现金折扣，则必须设置**应付账款参数**页上的 **计算部分付款的现金折扣** 选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="63aec-117">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments **option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="63aec-118">例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="63aec-119">100.00 的发票已过帐。</span><span class="sxs-lookup"><span data-stu-id="63aec-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="63aec-120">如果您在 10 天内付款 49.00，则在付款日志中将输入借出 49.00。</span><span class="sxs-lookup"><span data-stu-id="63aec-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="63aec-121">在您在**结算未结交易记录**页面上结算部分付款时，**1.00** 将出现在**要提取的现金折扣金额**字段中。</span><span class="sxs-lookup"><span data-stu-id="63aec-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="63aec-122">如果您输入部分付款并在**要结算的金额**字段中保留完整的发票金额，则在您过帐交易记录时，**要提取的现金折扣金额**字段将自动重新计算。</span><span class="sxs-lookup"><span data-stu-id="63aec-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="63aec-123">使用现金折扣的贷方通知单</span><span class="sxs-lookup"><span data-stu-id="63aec-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="63aec-124">您可能要退回某些发票上的物料，并且接收贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="63aec-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="63aec-125">如果现金折扣已在原始发票上执行，则可以减去折扣的值和接收退回的正确金额。</span><span class="sxs-lookup"><span data-stu-id="63aec-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="63aec-126">如果**应付账款参数**页上的 **计算贷方通知单的现金折扣** 选项设置为**是**，则将自动计算贷方通知单的折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-126">If the **Calculate cash discounts for credit notes **option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="63aec-127">例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="63aec-128">100.00 的发票已过帐。</span><span class="sxs-lookup"><span data-stu-id="63aec-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="63aec-129">如果您要退回货物，并且您接受贷方通知单，您可以为原始发票的全部金额 100.00 输入贷方通知单，以及同样在贷项通知单上定义的 2% 现金折扣。</span><span class="sxs-lookup"><span data-stu-id="63aec-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="63aec-130">当您在**结算交易记录**页面上查看贷方通知单时，**98.00** 将出现在**要结算的金额**字段中，并且 **-2.00** 将出现在**现金折扣金额**字段中。</span><span class="sxs-lookup"><span data-stu-id="63aec-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="63aec-131">折扣金额过帐到现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="63aec-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="63aec-132">超额支付/支付不足金额</span><span class="sxs-lookup"><span data-stu-id="63aec-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="63aec-133">仍必须结算的金额非常小时，您可以进行部分付款。</span><span class="sxs-lookup"><span data-stu-id="63aec-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="63aec-134">例如，供应商发票为 1,000.00，您 支付 999.90。</span><span class="sxs-lookup"><span data-stu-id="63aec-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="63aec-135">如果余额少于为**应付账款参数**页的超额支付或支付不足指定的金额，差额将自动过帐到超额支付/支付不足会计科目。</span><span class="sxs-lookup"><span data-stu-id="63aec-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="63aec-136">有关详细信息，请参阅[供应商付款概览](../cash-bank-management/tasks/vendor-payment-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="63aec-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>
