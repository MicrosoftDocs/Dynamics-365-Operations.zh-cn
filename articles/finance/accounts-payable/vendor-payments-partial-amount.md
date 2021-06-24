---
title: 部分金额的供应商付款
description: 有时您可以向低于发票金额的供应商付款。 本文介绍处理此情况不同的选项。
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ee17aeb75e2bdc3b9c36d50914c24aa9d6218b7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189509"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="43c30-104">部分金额的供应商付款</span><span class="sxs-lookup"><span data-stu-id="43c30-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43c30-105">有时您可以向低于发票金额的供应商付款。</span><span class="sxs-lookup"><span data-stu-id="43c30-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="43c30-106">本文介绍处理此情况不同的选项。</span><span class="sxs-lookup"><span data-stu-id="43c30-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="43c30-107">可供您使用的选项取决于您的业务要求和配置。</span><span class="sxs-lookup"><span data-stu-id="43c30-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

## <a name="cash-discount-amounts"></a><span data-ttu-id="43c30-108">现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="43c30-108">Cash discount amounts</span></span>

<span data-ttu-id="43c30-109">供应商可以在到期日期前提供您支付的发票一个现金折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="43c30-110">例如，如果发票在 10 天内支付，您输入金额为 100.00 的发票，指定 2% 现金折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="43c30-111">到期期限为 30 天。</span><span class="sxs-lookup"><span data-stu-id="43c30-111">The due date terms are 30 days.</span></span> <span data-ttu-id="43c30-112">如果付款方案使用现金折扣作为选择发票的条件，并且，如果该方案在现金折扣日期或之前运行，为付款选择发票，付款创建为 98.00。</span><span class="sxs-lookup"><span data-stu-id="43c30-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="43c30-113">现金折扣还可以为手动创建的一次性付款获取。</span><span class="sxs-lookup"><span data-stu-id="43c30-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="43c30-114">使用现金折扣的部分付款</span><span class="sxs-lookup"><span data-stu-id="43c30-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="43c30-115">在进行部分付款时，您可以计划进行部分付款以完全结算发票。</span><span class="sxs-lookup"><span data-stu-id="43c30-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="43c30-116">要为部分付款获取现金折扣，则必须设置 **应付帐款参数** 页上的 **计算部分付款的现金折扣** 选项为 **是**。</span><span class="sxs-lookup"><span data-stu-id="43c30-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="43c30-117">例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="43c30-118">100.00 的发票已过帐。</span><span class="sxs-lookup"><span data-stu-id="43c30-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="43c30-119">如果您在 10 天内付款 49.00，则在付款日志中将输入借出 49.00。</span><span class="sxs-lookup"><span data-stu-id="43c30-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="43c30-120">在您在 **结算未结交易记录** 页面上结算部分付款时，**1.00** 将出现在 **要提取的现金折扣金额** 字段中。</span><span class="sxs-lookup"><span data-stu-id="43c30-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="43c30-121">如果您输入部分付款并在 **要结算的金额** 字段中保留完整的发票金额，则在您过帐交易记录时，**要提取的现金折扣金额** 字段将自动重新计算。</span><span class="sxs-lookup"><span data-stu-id="43c30-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="43c30-122">使用现金折扣的贷方通知单</span><span class="sxs-lookup"><span data-stu-id="43c30-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="43c30-123">您可能要退回某些发票上的物料，并且接收贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="43c30-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="43c30-124">如果现金折扣已在原始发票上执行，则可以减去折扣的值和接收退回的正确金额。</span><span class="sxs-lookup"><span data-stu-id="43c30-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="43c30-125">如果 **应付帐款参数** 页上的 **计算贷方通知单的现金折扣** 选项设置为 **是**，则将自动计算贷方通知单的折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="43c30-126">例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="43c30-127">100.00 的发票已过帐。</span><span class="sxs-lookup"><span data-stu-id="43c30-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="43c30-128">如果您要退回货物，并且您接受贷方通知单，您可以为原始发票的全部金额 100.00 输入贷方通知单，以及同样在贷项通知单上定义的 2% 现金折扣。</span><span class="sxs-lookup"><span data-stu-id="43c30-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="43c30-129">当您在 **结算交易记录** 页面上查看贷方通知单时，**98.00** 将出现在 **要结算的金额** 字段中，并且 **-2.00** 将出现在 **现金折扣金额** 字段中。</span><span class="sxs-lookup"><span data-stu-id="43c30-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="43c30-130">折扣金额过帐到现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="43c30-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="43c30-131">超额支付/支付不足金额</span><span class="sxs-lookup"><span data-stu-id="43c30-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="43c30-132">仍必须结算的金额非常小时，您可以进行部分付款。</span><span class="sxs-lookup"><span data-stu-id="43c30-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="43c30-133">例如，供应商发票为 1,000.00，您 支付 999.90。</span><span class="sxs-lookup"><span data-stu-id="43c30-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="43c30-134">如果余额少于为 **应付帐款参数** 页的超额支付或支付不足指定的金额，差额将自动过帐到超额支付/支付不足会计科目。</span><span class="sxs-lookup"><span data-stu-id="43c30-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="43c30-135">有关详细信息，请参阅[供应商付款概览](../cash-bank-management/tasks/vendor-payment-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="43c30-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]