---
title: 供应商付款概览
description: 此任务指南将向您介绍用于创建供应商付款的各种方法，包括如何使用付款方案或手动输入一次性付款。
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fe4c42a87d448bc486de07b4db2180e22e69eae
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841793"
---
# <a name="vendor-payment-overview"></a><span data-ttu-id="d021f-103">供应商付款概览</span><span class="sxs-lookup"><span data-stu-id="d021f-103">Vendor payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d021f-104">此任务指南将向您介绍用于创建供应商付款的各种方法，包括如何使用付款方案或手动输入一次性付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-104">This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually entering a one-off payment.</span></span> <span data-ttu-id="d021f-105">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="d021f-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d021f-106">转至“应付账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="d021f-106">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="d021f-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d021f-107">Click New.</span></span>
3. <span data-ttu-id="d021f-108">选择保存供应商付款的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="d021f-108">Select the payment journal in which to save the vendor payments.</span></span> 
4. <span data-ttu-id="d021f-109">选择日记帐或手动输入日记帐。</span><span class="sxs-lookup"><span data-stu-id="d021f-109">Select the journal or manually enter it.</span></span>
5. <span data-ttu-id="d021f-110">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="d021f-110">Click Lines.</span></span>
6. <span data-ttu-id="d021f-111">单击“付款方案”。</span><span class="sxs-lookup"><span data-stu-id="d021f-111">Click Payment proposal.</span></span>
7. <span data-ttu-id="d021f-112">单击”创建付款方案“。</span><span class="sxs-lookup"><span data-stu-id="d021f-112">Click Create payment proposal.</span></span>
    * <span data-ttu-id="d021f-113">付款方案是用于选择付款发票的查询项。</span><span class="sxs-lookup"><span data-stu-id="d021f-113">The payment proposal is a query used to select invoices for payment.</span></span> <span data-ttu-id="d021f-114">您可以在创建或生成供应商付款发票前编辑发票列表。</span><span class="sxs-lookup"><span data-stu-id="d021f-114">You can edit the list of invoices to pay before creating or generating the vendor payments.</span></span>  
8. <span data-ttu-id="d021f-115">依据到期日期、现金折扣或两者选择付款发票。</span><span class="sxs-lookup"><span data-stu-id="d021f-115">Select invoices for payment by due date, cash discount, or both.</span></span> 
9. <span data-ttu-id="d021f-116">输入对比到期日期或现金折扣的日期。</span><span class="sxs-lookup"><span data-stu-id="d021f-116">Enter the date for comparing to the due date or cash discount.</span></span> 
10. <span data-ttu-id="d021f-117">可选：输入用于所有付款的付款日期。</span><span class="sxs-lookup"><span data-stu-id="d021f-117">Optional: Enter a payment date used for all payments.</span></span>
    * <span data-ttu-id="d021f-118">在此处输入的日期将是创建的所有付款的付款日期，无论到期日期或现金折扣日期是哪一天。</span><span class="sxs-lookup"><span data-stu-id="d021f-118">The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.</span></span>  
11. <span data-ttu-id="d021f-119">可选：输入可用作付款日期的最早付款日期。</span><span class="sxs-lookup"><span data-stu-id="d021f-119">Optional: Enter a minimum payment date which may be used as the payment date.</span></span>
    * <span data-ttu-id="d021f-120">在创建付款时，最早付款日期将是使用的最早日期。</span><span class="sxs-lookup"><span data-stu-id="d021f-120">The minimum payment date will be the earliest date used when creating payments.</span></span> <span data-ttu-id="d021f-121">例如，如果发票的到期日期在最早付款日期之后，付款日期将会是到期日期（而不是最早付款日期），以在可能的最晚日期支付发票。</span><span class="sxs-lookup"><span data-stu-id="d021f-121">For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.</span></span>  
12. <span data-ttu-id="d021f-122">在“添加记录”项下输入其他查询限制。</span><span class="sxs-lookup"><span data-stu-id="d021f-122">Enter additional query restrictions under Records to include.</span></span>
    * <span data-ttu-id="d021f-123">筛选器通常用于限制由供应商组为付款选择的发票或付款方式。</span><span class="sxs-lookup"><span data-stu-id="d021f-123">The filter is often used to restrict the invoices selected for payment by vendor group or method of payment.</span></span> <span data-ttu-id="d021f-124">例如，您可以添加在此付薪周期用支票支付发票的筛选器。</span><span class="sxs-lookup"><span data-stu-id="d021f-124">For example, you may add a filter to only pay invoices by check in this pay run.</span></span>  
13. <span data-ttu-id="d021f-125">输入其他查询限制或付款默认值。</span><span class="sxs-lookup"><span data-stu-id="d021f-125">Enter additional query restriction or payment defaults.</span></span> 
    * <span data-ttu-id="d021f-126">附加参数可以用于定义付款货币或启用此付薪期间的集中付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-126">The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.</span></span>  
14. <span data-ttu-id="d021f-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d021f-127">Click OK.</span></span>
    * <span data-ttu-id="d021f-128">在单击“确定”后，将显示该查询的结果。</span><span class="sxs-lookup"><span data-stu-id="d021f-128">After clicking OK, the results of the query will appear.</span></span> <span data-ttu-id="d021f-129">如果您不想预览选中供付款的发票列表，可返回到“参数”快速选项卡，并将设置更改为“创建无发票预览付款 = 是”。</span><span class="sxs-lookup"><span data-stu-id="d021f-129">If you don't want to preview the list of invoices selected to pay, you can go back to the Parameters fast tab and change the setting Create payments without invoice preview = Yes.</span></span>  
15. <span data-ttu-id="d021f-130">选择“显示付款概览”按钮以查看为所选发票的供应商创建的付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-130">Choose the Show payment overview button to view the payments that will be created for the vendor on the invoice selected.</span></span>
16. <span data-ttu-id="d021f-131">选择“隐藏付款概览”按钮以隐藏付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-131">Choose the Hide payment overview button to hide the payments.</span></span> 
17. <span data-ttu-id="d021f-132">单击”创建付款“。</span><span class="sxs-lookup"><span data-stu-id="d021f-132">Click Create payments.</span></span>
    * <span data-ttu-id="d021f-133">在选择“创建付款”前，您可以右键单击网格，然后导出发票列表到 Excel 中。</span><span class="sxs-lookup"><span data-stu-id="d021f-133">Before choosing Create payments, you can right click on the grid and export the list of invoices to Excel.</span></span> <span data-ttu-id="d021f-134">单击“创建付款”按钮后将在付款日记帐中创建供应商付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-134">The Create payments button will create the vendor payments in the payment journal.</span></span>  
18. <span data-ttu-id="d021f-135">浏览您的付款并确保已定义所有付款的付款方式。</span><span class="sxs-lookup"><span data-stu-id="d021f-135">Scan your payments and make sure the method of payment is defined for all payments.</span></span> 
    * <span data-ttu-id="d021f-136">如果您生成付款单据，例如打印支票或创建电子付款单据，则必须定义付款方式。</span><span class="sxs-lookup"><span data-stu-id="d021f-136">If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined.</span></span> <span data-ttu-id="d021f-137">付款方式还将默认来自付款的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="d021f-137">The method of payment will also default the bank account from the payment will be made.</span></span>  
19. <span data-ttu-id="d021f-138">单击“新建”创建一次性付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-138">Click New to create a one-off payment.</span></span>
    * <span data-ttu-id="d021f-139">一次性付款可以在过帐前的任何时间添加到付款日记帐中。</span><span class="sxs-lookup"><span data-stu-id="d021f-139">A one-off payment can be added to a payment journal at any time prior to posting.</span></span> <span data-ttu-id="d021f-140">单击“新建”按钮手动添加付款信息，而非使用付款方案来完成。</span><span class="sxs-lookup"><span data-stu-id="d021f-140">This is done by clicking the New button and adding the payment information manually, rather than using the Payment proposal.</span></span>  
20. <span data-ttu-id="d021f-141">选择接受付款的供应商。</span><span class="sxs-lookup"><span data-stu-id="d021f-141">Select the vendor to whom the payment will be made.</span></span>
21. <span data-ttu-id="d021f-142">如果存在供付款的发票，选择“结算交易”以选择付款的发票。</span><span class="sxs-lookup"><span data-stu-id="d021f-142">If an invoice exists to pay, select Settle transactions to select the invoice for payment.</span></span>
    * <span data-ttu-id="d021f-143">如果这是预付款，此步骤是可选项。</span><span class="sxs-lookup"><span data-stu-id="d021f-143">If this is a prepayment, this step is optional.</span></span> <span data-ttu-id="d021f-144">您可以创建未选择任何发票的付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-144">You can create the payment without selecting any invoice.</span></span>  
22. <span data-ttu-id="d021f-145">标记要支付的所有发票。</span><span class="sxs-lookup"><span data-stu-id="d021f-145">Mark any invoices that will be paid.</span></span>
    * <span data-ttu-id="d021f-146">如果您使用“结算交易”来选择付款发票，付款金额将根据您标记为付款的发票以及您在“结算金额”中输入的金额自动计算。</span><span class="sxs-lookup"><span data-stu-id="d021f-146">If you use the Settle transactions to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the Amount to settle.</span></span>  
23. <span data-ttu-id="d021f-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d021f-147">Click OK.</span></span>
24. <span data-ttu-id="d021f-148">如果您要删除付款，则标记行。</span><span class="sxs-lookup"><span data-stu-id="d021f-148">If you want to delete a payment, mark the row.</span></span>
25. <span data-ttu-id="d021f-149">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="d021f-149">Click Delete.</span></span>
    * <span data-ttu-id="d021f-150">删除一项付款将只删除该付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-150">Deleting a payment will only delete the payment.</span></span> <span data-ttu-id="d021f-151">任何标记为付款的发票将仍可由另一付款进行支付。</span><span class="sxs-lookup"><span data-stu-id="d021f-151">Any invoices marked for payment will still be available to be paid by another payment.</span></span>  
26. <span data-ttu-id="d021f-152">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="d021f-152">Click Yes.</span></span>
27. <span data-ttu-id="d021f-153">选择“生成付款”以打印支票或创建电子付款文件。</span><span class="sxs-lookup"><span data-stu-id="d021f-153">Choose Generate payment to print Checks or create the electronic payment file.</span></span>
28. <span data-ttu-id="d021f-154">选择要生成的付款类型。</span><span class="sxs-lookup"><span data-stu-id="d021f-154">Select the method of payment that you want to generate.</span></span>
    * <span data-ttu-id="d021f-155">付款日记帐可包含支票付款和电子付款，但您一次仅可生成一个付款类型。</span><span class="sxs-lookup"><span data-stu-id="d021f-155">The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.</span></span>  
29. <span data-ttu-id="d021f-156">选择生成付款的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="d021f-156">Select the bank account from which to generate the payments.</span></span>
30. <span data-ttu-id="d021f-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d021f-157">Click OK.</span></span>
    * <span data-ttu-id="d021f-158">将只生成与付款方式和您选择的银行帐户匹配的付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-158">Payments will only be generated for payments that match the Method of payment and Bank account you selected.</span></span>  
31. <span data-ttu-id="d021f-159">如果要生成支票，请选择文件以确保支票的打印目标正确。</span><span class="sxs-lookup"><span data-stu-id="d021f-159">If you are generating Checks, choose Document to ensure the correct print destination for the Checks.</span></span>
32. <span data-ttu-id="d021f-160">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d021f-160">Click OK.</span></span>
33. <span data-ttu-id="d021f-161">单击“确定”以生成付款。</span><span class="sxs-lookup"><span data-stu-id="d021f-161">Click OK to generate the payments.</span></span>
34. <span data-ttu-id="d021f-162">如果所有付款已获得审批和生成，单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="d021f-162">Click Post if all the payments are approved and generated.</span></span> 

