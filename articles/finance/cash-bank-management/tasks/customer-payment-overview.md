---
title: 客户付款概览
description: 本任务指南逐步介绍用于输入客户付款的各种方法。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e93703815d899baa7045f2c5f1e0323944e91c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225409"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="050fc-103">客户付款概览</span><span class="sxs-lookup"><span data-stu-id="050fc-103">Customer payment overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="050fc-104">本任务指南逐步介绍用于输入客户付款的各种方法。</span><span class="sxs-lookup"><span data-stu-id="050fc-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="050fc-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="050fc-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="050fc-106">转到 **导航窗格 > 模块 > 应收帐款 > 付款 > 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="050fc-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="050fc-107">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="050fc-107">Click **New**.</span></span>
3. <span data-ttu-id="050fc-108">选择将保存客户付款的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="050fc-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="050fc-109">选择或手动输入日记帐。</span><span class="sxs-lookup"><span data-stu-id="050fc-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="050fc-110">在 **操作窗格** 上，单击 **输入客户付款**。</span><span class="sxs-lookup"><span data-stu-id="050fc-110">On **Action pane**, click **Enter customer payments**.</span></span> <span data-ttu-id="050fc-111">输入客户付款用于一次记录一项客户付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="050fc-112">您在顶部输入付款信息，然后标记该付款支付的发票，全部在同一个页面操作。</span><span class="sxs-lookup"><span data-stu-id="050fc-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="050fc-113">输入您接收其付款的客户。</span><span class="sxs-lookup"><span data-stu-id="050fc-113">Enter the customer from whom you received the payment.</span></span> <span data-ttu-id="050fc-114">如果您不知道客户，但是知道已付款的交易，则可以使用“交易记录”字段输入付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="050fc-115">在“交易记录”字段中输入或选择发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="050fc-116">在选择交易后，客户将自动默认填充。</span><span class="sxs-lookup"><span data-stu-id="050fc-116">The customer will automatically default after you select the transaction.</span></span>
7. <span data-ttu-id="050fc-117">在 **付款参考** 字段中，输入付款参考。</span><span class="sxs-lookup"><span data-stu-id="050fc-117">In the **Payment reference** field, enter a payment reference.</span></span> <span data-ttu-id="050fc-118">付款参考可以是客户的支票编号或客户的电子付款参考。</span><span class="sxs-lookup"><span data-stu-id="050fc-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="050fc-119">仅当您标记为在存款单上包括付款时才需要付款参考。</span><span class="sxs-lookup"><span data-stu-id="050fc-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="050fc-120">在 **存款单** 字段中，选择是否在存款单中加入付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-120">In the **Deposit slip** field, select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="050fc-121">在 **金额** 字段，输入客户付款金额。</span><span class="sxs-lookup"><span data-stu-id="050fc-121">In the **Amount** field, enter the amount of the customer payment.</span></span> <span data-ttu-id="050fc-122">付款金额不会默认填充。</span><span class="sxs-lookup"><span data-stu-id="050fc-122">The payment amount will not default.</span></span> <span data-ttu-id="050fc-123">必须手动输入。</span><span class="sxs-lookup"><span data-stu-id="050fc-123">It must be manually entered.</span></span> 
10. <span data-ttu-id="050fc-124">标记客户已支付的发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-124">Mark the invoices that were paid by the customer.</span></span> <span data-ttu-id="050fc-125">如果付款为预付款，您无需为结算标记任何发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="050fc-126">付款仍可以保存和过帐。</span><span class="sxs-lookup"><span data-stu-id="050fc-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="050fc-127">发票结算可在稍后进行。</span><span class="sxs-lookup"><span data-stu-id="050fc-127">Settlement to an invoice can happen at a later time.</span></span>
11. <span data-ttu-id="050fc-128">输入应结算以标记发票的付款的金额。</span><span class="sxs-lookup"><span data-stu-id="050fc-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> <span data-ttu-id="050fc-129">此字段可在付款为部分付款时使用。</span><span class="sxs-lookup"><span data-stu-id="050fc-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="050fc-130">如果您不输入金额，系统将自动为您确定要结算的金额。</span><span class="sxs-lookup"><span data-stu-id="050fc-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>
12. <span data-ttu-id="050fc-131">单击 **保存在日记帐中**。</span><span class="sxs-lookup"><span data-stu-id="050fc-131">Click **Save in journal**.</span></span> <span data-ttu-id="050fc-132">在将付款保存到日记帐前，请确保已定义对方科目。</span><span class="sxs-lookup"><span data-stu-id="050fc-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="050fc-133">使用 **保存在日记帐中** 将保存付款并将其移动到日记帐中。</span><span class="sxs-lookup"><span data-stu-id="050fc-133">Using **Save in journal** will save the payment and move it to the journal.</span></span> <span data-ttu-id="050fc-134">然后，您可以继续输入下一笔付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-134">You can then continue entering the next payment.</span></span>
13. <span data-ttu-id="050fc-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="050fc-135">Close the page.</span></span>
14. <span data-ttu-id="050fc-136">在 **操作窗格** 上，单击“行”。</span><span class="sxs-lookup"><span data-stu-id="050fc-136">On **Action pane**, click Lines.</span></span> <span data-ttu-id="050fc-137">在打开“行”时，您将看到您在 **输入客户付款** 页面记录并保存到日记帐的所有付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-137">When opening Lines, you will see any payments you recorded on the **Enter customer payments** page and saved into the journal.</span></span> <span data-ttu-id="050fc-138">您还可以使用此页输入新的客户付款，或在现有客户付款过帐前对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="050fc-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>
15. <span data-ttu-id="050fc-139">单击 **新建** 创建另一项付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-139">Click **New** to create another payment.</span></span> 
16. <span data-ttu-id="050fc-140">选择您接收其付款的客户。</span><span class="sxs-lookup"><span data-stu-id="050fc-140">Select the customer from whom you received the payment.</span></span> <span data-ttu-id="050fc-141">如果您不知道客户，但知道付款支付的发票，则使用“发票”字段手动输入或选择发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="050fc-142">选择发票后，客户将默认填充。</span><span class="sxs-lookup"><span data-stu-id="050fc-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="050fc-143">单击 **结算交易** 以标记已付款发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-143">Click **Settle transactions** to mark invoices that were paid.</span></span> <span data-ttu-id="050fc-144">您无需结算付款，以开具发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="050fc-145">如果是预付款，或您不知道已支付的发票，您可以输入并过帐付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="050fc-146">付款可以稍后结算到发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="050fc-147">标记付款已支付的发票。</span><span class="sxs-lookup"><span data-stu-id="050fc-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="050fc-148">在 **金额** 字段中，输入将结算以标记发票的付款金额。</span><span class="sxs-lookup"><span data-stu-id="050fc-148">In the **Amount** field, enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="050fc-149">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="050fc-149">Click **OK**.</span></span>
21. <span data-ttu-id="050fc-150">在 **付款参考** 字段中，输入付款参考。</span><span class="sxs-lookup"><span data-stu-id="050fc-150">In the **Payment reference** field, enter a payment reference.</span></span> <span data-ttu-id="050fc-151">仅当您标记为在存款单上包括付款时才需要付款参考。</span><span class="sxs-lookup"><span data-stu-id="050fc-151">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="050fc-152">在 **操作窗格** 上，单击 **过帐** 以过帐客户付款。</span><span class="sxs-lookup"><span data-stu-id="050fc-152">On **Action pane**, click **Post** to post the customer payments.</span></span> 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]