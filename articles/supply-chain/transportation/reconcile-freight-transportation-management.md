---
title: 在运输管理中对运费进行对帐
description: 本主题介绍了运费对帐流程。
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809078"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="ca7f8-103">在运输管理中对运费进行对帐</span><span class="sxs-lookup"><span data-stu-id="ca7f8-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca7f8-104">本主题介绍了运费对帐流程。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="ca7f8-105">可以手动完成运费对帐或可以设置为自动发生。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="ca7f8-106">若要使用自动运费对帐，您必须设置审计主数据，在其中可以定义确定自动匹配哪些运费帐单的条件。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="ca7f8-107">运费对帐流程</span><span class="sxs-lookup"><span data-stu-id="ca7f8-107">The freight reconciliation process</span></span>

<span data-ttu-id="ca7f8-108">运费费率由与相关装运承运人相关的费率引擎来计算。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="ca7f8-109">确认负荷后，将生成运费帐单，运费费率被转移到该帐单。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="ca7f8-110">运费费率作为其他费用分摊到相关的原始凭证（采购订单、销售订单和/或转移单），根据用于常规计费流程的设置。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="ca7f8-111">从装运承运人收到运费发票后，就立即可以开始运费对帐流程（这也称为匹配流程）。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="ca7f8-112">可以以电子方式或使用纸张接收发票。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="ca7f8-113">如果使用纸张接收发票，可以通过将运费帐单作为模板使用来生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="ca7f8-114">[![运费对帐流程](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="ca7f8-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="ca7f8-115">手动对帐</span><span class="sxs-lookup"><span data-stu-id="ca7f8-115">Manual reconciliation</span></span>

<span data-ttu-id="ca7f8-116">如果要手动对帐运费，必须将每个发票行与已开票负荷的运费帐单行匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="ca7f8-117">您在 **运费帐单和发票匹配** 页进行此匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="ca7f8-118">如果发票行上的金额与运费帐单金额不匹配，则必须选择上差异对帐原因。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="ca7f8-119">如果有多个对帐原因，您可以在它们之间拆分不匹配的金额。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="ca7f8-120">对帐原因确定如何在总帐中过帐差异金额。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="ca7f8-121">当对帐所计算的整个发票金额时，将金额提交供审批，然后过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="ca7f8-122">下图显示了如何生成运费发票和执行运费对帐。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="ca7f8-123">[![运费对帐任务](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="ca7f8-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="ca7f8-124">自动对帐</span><span class="sxs-lookup"><span data-stu-id="ca7f8-124">Automatic reconciliation</span></span>

<span data-ttu-id="ca7f8-125">若要使用自动对帐，您必须指定对帐计划和发票，以及要使用的装运承运人。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="ca7f8-126">发票行和运费帐单的匹配根据审计主数据和运费帐单类型的设置进行。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="ca7f8-127">运行自动对帐后，必须处理所有系统不能匹配的发票。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="ca7f8-128">然后，您必须手动处理这些发票，然后才能过帐所有付款发票。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="ca7f8-129">使用自动或手动对帐将运费帐单与运费发票进行匹配</span><span class="sxs-lookup"><span data-stu-id="ca7f8-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="ca7f8-130">*匹配* 是查找与每个运费发票相对应的运费帐单的流程。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="ca7f8-131">这可以通过逐一匹配发票行（手动匹配）或一次匹配所有可用发票（自动匹配）来完成。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="ca7f8-132">自动匹配</span><span class="sxs-lookup"><span data-stu-id="ca7f8-132">Auto matching</span></span>

<span data-ttu-id="ca7f8-133">将多个运费发票与同一运费帐单匹配时，自动匹配的流程如下：</span><span class="sxs-lookup"><span data-stu-id="ca7f8-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="ca7f8-134">所有未匹配的运费发票按金额排序，金额最大的在最前面。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="ca7f8-135">逐一匹配运费发票，直到运费帐单上没有剩余正金额。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="ca7f8-136">根据审计主数据的设置和运费发票上的剩余金额，设置剩余金额。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="ca7f8-137">手动匹配</span><span class="sxs-lookup"><span data-stu-id="ca7f8-137">Manual matching</span></span>

<span data-ttu-id="ca7f8-138">所有带有正金额的运费帐单都可以进行匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="ca7f8-139">与自动匹配相似，用户只能将带有负金额的运费发票与未完全匹配的运费帐单进行匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="ca7f8-140">示例</span><span class="sxs-lookup"><span data-stu-id="ca7f8-140">Example</span></span>

<span data-ttu-id="ca7f8-141">假设您有一个金额为 1500 的运费帐单 (FB)，并且已为该运费帐单创建了三个运费发票，每个发票有一个发票行，并进行了以下设置：</span><span class="sxs-lookup"><span data-stu-id="ca7f8-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="ca7f8-142">原始运费帐单 (FB)：金额 1500</span><span class="sxs-lookup"><span data-stu-id="ca7f8-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="ca7f8-143">发票 1 (Inv1)：金额 1000</span><span class="sxs-lookup"><span data-stu-id="ca7f8-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="ca7f8-144">发票 2 (Inv2)：金额 600</span><span class="sxs-lookup"><span data-stu-id="ca7f8-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="ca7f8-145">发票 3 (Inv3)：金额 -100</span><span class="sxs-lookup"><span data-stu-id="ca7f8-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="ca7f8-146">自动匹配结果</span><span class="sxs-lookup"><span data-stu-id="ca7f8-146">Automatic matching result</span></span>

<span data-ttu-id="ca7f8-147">自动匹配将按以下顺序执行：</span><span class="sxs-lookup"><span data-stu-id="ca7f8-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="ca7f8-148">按金额降序排列所有运费发票：Inv1 -> Inv2 -> Inv3。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="ca7f8-149">将 Inv1 与 FB 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-149">Match Inv1 with FB.</span></span> <span data-ttu-id="ca7f8-150">Inv1 匹配了 1000，FB 有 500 剩余金额，因此状态设置为 *部分匹配*。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="ca7f8-151">将 Inv2 与 FB 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-151">Match Inv2 with FB.</span></span> <span data-ttu-id="ca7f8-152">Inv2 匹配了 500，FB 有 0 剩余，因此状态设置为 *完全匹配*。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="ca7f8-153">由于 FB 现在已完全匹配，因此不会处理 Inv3。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="ca7f8-154">手动匹配结果</span><span class="sxs-lookup"><span data-stu-id="ca7f8-154">Manual matching result</span></span>

<span data-ttu-id="ca7f8-155">对于手动匹配，结果因匹配的顺序而异，如以下示例案例所示。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="ca7f8-156">手动匹配案例 1</span><span class="sxs-lookup"><span data-stu-id="ca7f8-156">Manual matching case 1</span></span>

<span data-ttu-id="ca7f8-157">进行本示例的手动匹配的一种方法如下：</span><span class="sxs-lookup"><span data-stu-id="ca7f8-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="ca7f8-158">将 FB 与 Inv1 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-158">Match FB with Inv1.</span></span> <span data-ttu-id="ca7f8-159">FB 有 500 剩余金额，因此状态设置为 *部分匹配*。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="ca7f8-160">将 Inv2 与 FB 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-160">Match Inv2 with FB.</span></span> <span data-ttu-id="ca7f8-161">Inv2 匹配了 500，FB 有 0 剩余，因此状态设置为 *完全匹配*。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="ca7f8-162">手动匹配 Inv3 时，您将找不到任何未匹配的运费帐单。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="ca7f8-163">此案例与自动匹配基本相同</span><span class="sxs-lookup"><span data-stu-id="ca7f8-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="ca7f8-164">手动匹配案例 2</span><span class="sxs-lookup"><span data-stu-id="ca7f8-164">Manual matching case 2</span></span>

<span data-ttu-id="ca7f8-165">进行本示例的手动匹配的另一种方法如下：</span><span class="sxs-lookup"><span data-stu-id="ca7f8-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="ca7f8-166">将 Inv3 与 FB 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-166">Match Inv3 with FB.</span></span> <span data-ttu-id="ca7f8-167">现在 FB 有 1600 剩余金额，这与在 1500 的基础上减去负 100 相同。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="ca7f8-168">FB 和 Inv3 都有匹配数量 -100。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="ca7f8-169">依次将 Inv1 和 Inv 2 与 FB 匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="ca7f8-170">FB 完全匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-170">FB is fully matched.</span></span>

<span data-ttu-id="ca7f8-171">如此示例所示，仅带有负金额的运费发票应手动匹配。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="ca7f8-172">这样可以确保始终可以将带有负金额的运费发票与未完全匹配的运费帐单进行匹配，因为这让您可以控制匹配顺序。</span><span class="sxs-lookup"><span data-stu-id="ca7f8-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]