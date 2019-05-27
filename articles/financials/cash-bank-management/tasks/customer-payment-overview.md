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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566125"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="67b75-103">客户付款概览</span><span class="sxs-lookup"><span data-stu-id="67b75-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67b75-104">本任务指南逐步介绍用于输入客户付款的各种方法。</span><span class="sxs-lookup"><span data-stu-id="67b75-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="67b75-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="67b75-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="67b75-106">转到“应收账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="67b75-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="67b75-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="67b75-107">Click New.</span></span>
3. <span data-ttu-id="67b75-108">选择将保存客户付款的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="67b75-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="67b75-109">选择或手动输入日记帐。</span><span class="sxs-lookup"><span data-stu-id="67b75-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="67b75-110">单击“输入客户付款”。</span><span class="sxs-lookup"><span data-stu-id="67b75-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="67b75-111">输入客户付款用于一次记录一项客户付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="67b75-112">您在顶部输入付款信息，然后标记该付款支付的发票，全部在同一个页面操作。</span><span class="sxs-lookup"><span data-stu-id="67b75-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="67b75-113">输入您接收其付款的客户。</span><span class="sxs-lookup"><span data-stu-id="67b75-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="67b75-114">如果您不知道客户，但是知道已付款的交易，则可以使用“交易记录”字段输入付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="67b75-115">在“交易记录”字段中输入或选择发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="67b75-116">在选择交易后，客户将自动默认填充。</span><span class="sxs-lookup"><span data-stu-id="67b75-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="67b75-117">在“付款参考”字段中，输入付款参考。</span><span class="sxs-lookup"><span data-stu-id="67b75-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="67b75-118">付款参考可以是客户的支票编号或客户的电子付款参考。</span><span class="sxs-lookup"><span data-stu-id="67b75-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="67b75-119">仅当您标记为在存款单上包括付款时才需要付款参考。</span><span class="sxs-lookup"><span data-stu-id="67b75-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="67b75-120">选择是否在存款单中加入付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="67b75-121">输入客户付款金额。</span><span class="sxs-lookup"><span data-stu-id="67b75-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="67b75-122">付款金额不会默认填充。</span><span class="sxs-lookup"><span data-stu-id="67b75-122">The payment amount will not default.</span></span> <span data-ttu-id="67b75-123">必须手动输入。</span><span class="sxs-lookup"><span data-stu-id="67b75-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="67b75-124">标记客户已支付的发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="67b75-125">如果付款为预付款，您无需为结算标记任何发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="67b75-126">付款仍可以保存和过帐。</span><span class="sxs-lookup"><span data-stu-id="67b75-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="67b75-127">发票结算可在稍后进行。</span><span class="sxs-lookup"><span data-stu-id="67b75-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="67b75-128">输入应结算以标记发票的付款的金额。</span><span class="sxs-lookup"><span data-stu-id="67b75-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="67b75-129">此字段可在付款为部分付款时使用。</span><span class="sxs-lookup"><span data-stu-id="67b75-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="67b75-130">如果您不输入金额，系统将自动为您确定要结算的金额。</span><span class="sxs-lookup"><span data-stu-id="67b75-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="67b75-131">单击“保存在日记帐中”。</span><span class="sxs-lookup"><span data-stu-id="67b75-131">Click Save in journal.</span></span>
    * <span data-ttu-id="67b75-132">在将付款保存到日记帐前，请确保已定义对方科目。</span><span class="sxs-lookup"><span data-stu-id="67b75-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="67b75-133">使用“保存在日记帐中”将保存付款并将其移动到日记帐中。</span><span class="sxs-lookup"><span data-stu-id="67b75-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="67b75-134">然后，您可以继续输入下一笔付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="67b75-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="67b75-135">Close the page.</span></span>
14. <span data-ttu-id="67b75-136">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="67b75-136">Click Lines.</span></span>
    * <span data-ttu-id="67b75-137">在打开“行”时，您将看到您在“输入客户付款”页面记录并保存到日记帐的所有付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="67b75-138">您还可以使用此页输入新的客户付款，或在现有客户付款过帐前对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="67b75-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="67b75-139">单击“新建”创建另一项付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="67b75-140">选择您接收其付款的客户。</span><span class="sxs-lookup"><span data-stu-id="67b75-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="67b75-141">如果您不知道客户，但知道付款支付的发票，则使用“发票”字段手动输入或选择发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="67b75-142">选择发票后，客户将默认填充。</span><span class="sxs-lookup"><span data-stu-id="67b75-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="67b75-143">单击“结算交易记录”标记已支付的发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="67b75-144">您无需将付款结算到任何发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="67b75-145">如果是预付款，或您不知道已支付的发票，您可以输入并过帐付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="67b75-146">付款可以稍后结算到发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="67b75-147">标记付款已支付的发票。</span><span class="sxs-lookup"><span data-stu-id="67b75-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="67b75-148">输入将结算以标记发票的付款金额。</span><span class="sxs-lookup"><span data-stu-id="67b75-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="67b75-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="67b75-149">Click OK.</span></span>
21. <span data-ttu-id="67b75-150">在“付款参考”字段中，输入付款参考。</span><span class="sxs-lookup"><span data-stu-id="67b75-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="67b75-151">。</span><span class="sxs-lookup"><span data-stu-id="67b75-151">.</span></span>
    * <span data-ttu-id="67b75-152">仅当您标记为在存款单上包括付款时才需要付款参考。</span><span class="sxs-lookup"><span data-stu-id="67b75-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="67b75-153">过帐客户付款。</span><span class="sxs-lookup"><span data-stu-id="67b75-153">Post the customer payments.</span></span> 

