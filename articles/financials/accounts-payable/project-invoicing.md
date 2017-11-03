---
title: "项目开票"
description: "本文提供时间和材料项目和固定价格项目的项目开票的概览。 它包含有关发票方案（预备发票）、发票控制、分期付款开票、供应商开票和贷方通知单的信息。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2434e0a97846ce9ca0643327a7a032a9998bde5b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="project-invoicing"></a><span data-ttu-id="eacdf-104">项目开票</span><span class="sxs-lookup"><span data-stu-id="eacdf-104">Project invoicing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eacdf-105">本文提供时间和材料项目和固定价格项目的项目开票的概览。</span><span class="sxs-lookup"><span data-stu-id="eacdf-105">This article provides an overview of project invoicing for Time and material projects and Fixed-price projects.</span></span> <span data-ttu-id="eacdf-106">它包含有关发票方案（预备发票）、发票控制、分期付款开票、供应商开票和贷方通知单的信息。</span><span class="sxs-lookup"><span data-stu-id="eacdf-106">It includes information about invoice proposals (preliminary invoices), invoice control, on-account invoicing, vendor invoicing, and credit notes.</span></span>

<span data-ttu-id="eacdf-107">项目类型确定应该应用哪一开票过程。</span><span class="sxs-lookup"><span data-stu-id="eacdf-107">The project type determines which invoicing procedure should be applied.</span></span> <span data-ttu-id="eacdf-108">只能对两个外部项目类型（时间和材料以及固定价格）进行开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-108">Only the two external project types, Time and material and Fixed-price, can be invoiced.</span></span> <span data-ttu-id="eacdf-109">时间和材料项目以及固定价格项目始终附加到项目合同。</span><span class="sxs-lookup"><span data-stu-id="eacdf-109">Time and material projects and Fixed-price projects are always attached to a project contract.</span></span>

-   <span data-ttu-id="eacdf-110">**固定价格项目** – 客户发票金额是基于发票缴费时间表的。</span><span class="sxs-lookup"><span data-stu-id="eacdf-110">**Fixed-price projects** – The customer invoice amount is based on invoice billing schedules.</span></span> <span data-ttu-id="eacdf-111">通过分期付款设置（也称为缴费时间表）进行开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-111">Invoicing is done through an on-account setup, which is also referred to as a billing schedule.</span></span> <span data-ttu-id="eacdf-112">可以按项目或项目合同对固定价格项目开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-112">Fixed-price projects can be invoiced per project or per project contract.</span></span>
-   <span data-ttu-id="eacdf-113">**时间和材料项目** – 客户发票金额基于在项目上输入的交易记录行。</span><span class="sxs-lookup"><span data-stu-id="eacdf-113">**Time and material projects** – The customer invoice amount is based on transaction lines that are entered on projects.</span></span> <span data-ttu-id="eacdf-114">可按项目或项目合同对交易记录开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-114">Transactions can be invoiced per project or per project contract.</span></span>

<span data-ttu-id="eacdf-115">有三周方式可将时间和材料项目以及固定价格项目附加到发票项目：</span><span class="sxs-lookup"><span data-stu-id="eacdf-115">There are three ways to attach Time and material projects and Fixed-price projects to the invoice projects:</span></span>

-   <span data-ttu-id="eacdf-116">**分期付款开票** – 时间和材料项目以及固定价格项目可按分期付款开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-116">**On-account invoicing** – Time and material projects and Fixed-price projects can be invoiced on account.</span></span> <span data-ttu-id="eacdf-117">需要两种类型的分期付款设置，每种项目类型一个。</span><span class="sxs-lookup"><span data-stu-id="eacdf-117">Two types of on-account setup are required, one for each project type.</span></span>
-   <span data-ttu-id="eacdf-118">**在期间部分中开票** – 通过期间功能，可以在多个项目上对交易记录开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-118">**Invoicing in the periodic section** – Through the periodic functions, transactions can be invoiced across projects.</span></span> <span data-ttu-id="eacdf-119">期间功能提供必须开票的交易记录的概览。</span><span class="sxs-lookup"><span data-stu-id="eacdf-119">The periodic functions provide an overview of transactions that must be invoiced.</span></span>
-   <span data-ttu-id="eacdf-120">**通过在开票时使用贷方通知单** – 可为时间和材料项目以及固定价格项目创建贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-120">**By using credit notes in invoicing** – A credit note can be created for both Time and material projects and Fixed-price projects.</span></span>

## <a name="invoice-proposals"></a><span data-ttu-id="eacdf-121">发票方案</span><span class="sxs-lookup"><span data-stu-id="eacdf-121">Invoice proposals</span></span>
<span data-ttu-id="eacdf-122">在为项目创建客户发票前，可以创建预备发票，或创建 发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-122">Before you create a customer invoice for a project, you can create a preliminary invoice, or invoice proposal.</span></span> <span data-ttu-id="eacdf-123">在发票方案中，您可以选择要在项目发票中包括的项目交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-123">In an invoice proposal, you can select project transactions to include in a project invoice.</span></span> <span data-ttu-id="eacdf-124">然后您可以在过帐项目发票并将其发送给客户或其他融资来源之前，查看发票详细信息。</span><span class="sxs-lookup"><span data-stu-id="eacdf-124">You can then review the invoice details before you post the project invoice and send it to the customer or other funding source.</span></span>

### <a name="creating-invoice-proposals"></a><span data-ttu-id="eacdf-125">创建发票方案</span><span class="sxs-lookup"><span data-stu-id="eacdf-125">Creating invoice proposals</span></span>

<span data-ttu-id="eacdf-126">可以通过手动选择指定项目的交易记录列表来创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-126">You can create invoice proposals by manually selecting from a list of transactions for a specified project.</span></span> <span data-ttu-id="eacdf-127">还可以设置计费规则指定何时自动创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-127">You can also set up billing rules that specify when to automatically create an invoice proposal.</span></span> <span data-ttu-id="eacdf-128">例如，在项目工作完成 25%、50%、75% 和 100% 时，可以创建计费规则来创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-128">For example, you can create a billing rule to create an invoice proposal when work on a project is 25 percent, 50 percent, 75 percent, and 100 percent completed.</span></span> 

<span data-ttu-id="eacdf-129">您可以为以下交易记录创建发票方案：</span><span class="sxs-lookup"><span data-stu-id="eacdf-129">You can create invoice proposals for the following transactions:</span></span>

-   <span data-ttu-id="eacdf-130">工时、支出和其他项目交易记录</span><span class="sxs-lookup"><span data-stu-id="eacdf-130">Hours, expenses, and other project transactions</span></span>
-   <span data-ttu-id="eacdf-131">客户按先前的项目发票预扣的金额</span><span class="sxs-lookup"><span data-stu-id="eacdf-131">Amounts that are withheld by customers on previous project invoices</span></span>
-   <span data-ttu-id="eacdf-132">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="eacdf-132">Credit notes</span></span>
-   <span data-ttu-id="eacdf-133">客户在项目开始前支付的金额</span><span class="sxs-lookup"><span data-stu-id="eacdf-133">Amounts that a customer paid to you before a project is started</span></span>

<span data-ttu-id="eacdf-134">您可以在发票方案创建费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-134">You can create fee transactions in an invoice proposal.</span></span> <span data-ttu-id="eacdf-135">还可以修改工时、支出、物料和费用交易记录的销售价。</span><span class="sxs-lookup"><span data-stu-id="eacdf-135">You can also modify the sales price on hour, expense, item, and fee transactions.</span></span> <span data-ttu-id="eacdf-136">在您过帐发票方案时，在项目报告和交易记录历史中添加已更新的价格和交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-136">When you post an invoice proposal, the updated prices and transactions are added to project reports and the transaction history.</span></span> 

<span data-ttu-id="eacdf-137">若要创建多个项目的客户发票，则必须为每张发票创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-137">To create multiple customer invoices for a project, you must create an invoice proposal for each invoice.</span></span> <span data-ttu-id="eacdf-138">例如，可以基于交易记录类型创建发票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-138">For example, you can create invoices based on transaction type.</span></span> <span data-ttu-id="eacdf-139">若要在一个客户发票上指定工时，在另一个客户发票上指定物料，则必须为工时交易记录创建一个发票方案，为费用交易记录创建单独的发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-139">To specify hours on one customer invoice and items on another, you must create separate invoice proposals for hour transactions and fee transactions.</span></span> 

<span data-ttu-id="eacdf-140">如果项目具有多个融资来源，可以为每个融资来源创建单独的发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-140">If a project has more than one funding source, you can create a separate invoice proposal for each funding source.</span></span> <span data-ttu-id="eacdf-141">在**“融资规则分配”**页上，可以定义交易记录金额的百分比以分配给每个融资来源，并定义来源以过帐舍入差额。</span><span class="sxs-lookup"><span data-stu-id="eacdf-141">On the **Funding rule allocations** page, you can define the percentage of the transaction amount to allocate to each funding source, and the source to post rounding differences.</span></span>

### <a name="creating-customer-invoices-from-invoice-proposals"></a><span data-ttu-id="eacdf-142">从发票方案创建客户发票</span><span class="sxs-lookup"><span data-stu-id="eacdf-142">Creating customer invoices from invoice proposals</span></span>

<span data-ttu-id="eacdf-143">在创建和过帐发票方案后，则自动为发票方案中包括的交易记录创建客户发票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-143">After you create and post an invoice proposal, a customer invoice is automatically created for the transactions that are included in the invoice proposal.</span></span> 

<span data-ttu-id="eacdf-144">在过帐发票方案前，可以在其中添加或删除交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-144">Before you post an invoice proposal, you can add transactions to it or delete transactions from it.</span></span> <span data-ttu-id="eacdf-145">例如，可以删除项目中已过帐但不对客户计费的支出交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-145">For example, you can remove expense transactions that were posted to a project, but that are not chargeable to the customer.</span></span> 

<span data-ttu-id="eacdf-146">如果您的组织要求在过帐发票方案前进行审查，则可能需要在过帐之前通过“查看项目发票方案”工作流审核此发票方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-146">If your organization requires that invoice proposals be reviewed before they are posted, the invoice proposal might need to be approved through the "Review project invoice proposals" workflow before it is posted.</span></span>

## <a name="on-account-invoicing"></a><span data-ttu-id="eacdf-147">分期付款开票</span><span class="sxs-lookup"><span data-stu-id="eacdf-147">On-account invoicing</span></span>
<span data-ttu-id="eacdf-148">您在项目的分期付款发票中输入的金额基于时间、完成百分比和相关项目合同中指定的其他帐单条件。</span><span class="sxs-lookup"><span data-stu-id="eacdf-148">The amount that you enter for a project in an on-account invoice is based on the timing, percentage of completion, and other billing conditions that are specified in the related project contract.</span></span> <span data-ttu-id="eacdf-149">金额不基于工时、物料、费用或过帐到项目的费用进行计算。</span><span class="sxs-lookup"><span data-stu-id="eacdf-149">The amount is not calculated based on the hours, items, expenses, or fees that are posted to the project.</span></span> 

<span data-ttu-id="eacdf-150">必须首先为时间及材料项目或固定价格项目创建分期付款业务，然后才可以将分期付款业务添加到项目发票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-150">You must create an on-account transaction for a Time and material project or a Fixed-price project before you can add that on-account transaction to a project invoice.</span></span> <span data-ttu-id="eacdf-151">在分期付款交易记录上，输入要为客户开票的金额。</span><span class="sxs-lookup"><span data-stu-id="eacdf-151">On the on-account transaction, enter the amount to invoice a customer.</span></span> <span data-ttu-id="eacdf-152">若要创建金额的项目发票，请创建预备发票（发票方案）。</span><span class="sxs-lookup"><span data-stu-id="eacdf-152">To create a project invoice for the amount, create a preliminary invoice (invoice proposal).</span></span> <span data-ttu-id="eacdf-153">在发票方案中，选择分期付款业务。</span><span class="sxs-lookup"><span data-stu-id="eacdf-153">In the invoice proposal, select the on-account transaction.</span></span> <span data-ttu-id="eacdf-154">您可以查看发票建议中的分期付款信息，然后可为其创建项目发票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-154">You can review the on-account information in the invoice proposal before you create a project invoice for it.</span></span>

### <a name="fixed-price-projects"></a><span data-ttu-id="eacdf-155">固定价格项目</span><span class="sxs-lookup"><span data-stu-id="eacdf-155">Fixed-price projects</span></span>

<span data-ttu-id="eacdf-156">对于固定价格项目，分期付款业务基于一个达成一致的里程碑、交货单位或项目合同中指定的按进度付款安排。</span><span class="sxs-lookup"><span data-stu-id="eacdf-156">For Fixed-price projects, on-account transactions are based on an agreed-upon milestone, unit of delivery, or progress billing arrangement that is specified in a project contract.</span></span> <span data-ttu-id="eacdf-157">为必须从项目客户接收的每笔付款创建一行。</span><span class="sxs-lookup"><span data-stu-id="eacdf-157">One line is created for each payment that must be received from the project customer.</span></span> <span data-ttu-id="eacdf-158">不需要扣缴。</span><span class="sxs-lookup"><span data-stu-id="eacdf-158">No deductions are required.</span></span>

### <a name="time-and-material-projects"></a><span data-ttu-id="eacdf-159">时间和材料项目</span><span class="sxs-lookup"><span data-stu-id="eacdf-159">Time and material projects</span></span>

<span data-ttu-id="eacdf-160">对于时间和材料项目，可使用分期付款发票建议要求客户或其他资金来源支付预付款金额。</span><span class="sxs-lookup"><span data-stu-id="eacdf-160">For Time and material projects, you can bill a customer or other funding source for a prepayment amount by using an on-account invoice proposal.</span></span> <span data-ttu-id="eacdf-161">输入分期付款交易记录作为一行。</span><span class="sxs-lookup"><span data-stu-id="eacdf-161">Enter on-account transactions as one line.</span></span> <span data-ttu-id="eacdf-162">（可选）您可以输入其他行作为对客户已支付预付款的偏离进行扣减。</span><span class="sxs-lookup"><span data-stu-id="eacdf-162">You can optionally enter additional lines as deductions to offset any prepayments that the customer has already made.</span></span> <span data-ttu-id="eacdf-163">若要创建扣缴行，请在金额前面加上减号。</span><span class="sxs-lookup"><span data-stu-id="eacdf-163">To create deduction lines, precede the amount with a minus sign.</span></span>

## <a name="invoice-control"></a><span data-ttu-id="eacdf-164">发票控制</span><span class="sxs-lookup"><span data-stu-id="eacdf-164">Invoice control</span></span>
<span data-ttu-id="eacdf-165">您可以使用发票控制来跟踪已开票和未开票的交易记录，以及从报价单页到完成分析那些不利于您的项目的一个端对端查看的报价的交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-165">You can use invoice control to track both invoiced and non-invoiced transactions, and to analyze those transactions against quotations for an end-to-end view of your projects from the quotation stage to completion.</span></span> <span data-ttu-id="eacdf-166">您可以看到哪个交易记录计费到特定项目，以及哪些行已开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-166">You can see which transactions have been charged to a specific project and which lines have been invoiced.</span></span> <span data-ttu-id="eacdf-167">您还可以查看单独的交易记录，以便可以在过帐后调整它们。</span><span class="sxs-lookup"><span data-stu-id="eacdf-167">You can also view individual transactions, so that you can adjust them after they are posted.</span></span>

## <a name="invoicing-fixed-price-projects"></a><span data-ttu-id="eacdf-168">开票固定价格项目</span><span class="sxs-lookup"><span data-stu-id="eacdf-168">Invoicing Fixed-price projects</span></span>
<span data-ttu-id="eacdf-169">若要给固定价格项目开发票，您必须定义缴费时间表并完成开发票程序。</span><span class="sxs-lookup"><span data-stu-id="eacdf-169">To invoice a Fixed-price project, you must define a billing schedule and complete the invoicing procedure.</span></span>

### <a name="billing-schedule"></a><span data-ttu-id="eacdf-170">缴费时间表</span><span class="sxs-lookup"><span data-stu-id="eacdf-170">Billing schedule</span></span>

<span data-ttu-id="eacdf-171">您可以按缴费时间表给价格固定的项目开发票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-171">You can invoice Fixed-price projects on a billing schedule.</span></span> <span data-ttu-id="eacdf-172">根据该项目的一个或多个里程碑定义该缴费时间表。</span><span class="sxs-lookup"><span data-stu-id="eacdf-172">The billing schedule is defined in terms of one or more milestones for the project.</span></span> <span data-ttu-id="eacdf-173">对于每个里程碑，您可以定义特定日期、销售币种、销售价和活动。</span><span class="sxs-lookup"><span data-stu-id="eacdf-173">For each milestone, you can define a specific date, sales currency, sales price, and activity.</span></span> 

<span data-ttu-id="eacdf-174">例如，您可以设置以下缴费时间表：</span><span class="sxs-lookup"><span data-stu-id="eacdf-174">For example, you can set up the following billing schedule:</span></span>

-   <span data-ttu-id="eacdf-175">20%（当签该项目合同时）</span><span class="sxs-lookup"><span data-stu-id="eacdf-175">20 percent when the project contract is signed</span></span>
-   <span data-ttu-id="eacdf-176">第一次交货时：30%</span><span class="sxs-lookup"><span data-stu-id="eacdf-176">30 percent on first delivery</span></span>
-   <span data-ttu-id="eacdf-177">第二次交货时：15%</span><span class="sxs-lookup"><span data-stu-id="eacdf-177">15 percent on second delivery</span></span>
-   <span data-ttu-id="eacdf-178">最后一次交货时：35%。</span><span class="sxs-lookup"><span data-stu-id="eacdf-178">35 percent on final delivery</span></span>

### <a name="invoicing-procedure"></a><span data-ttu-id="eacdf-179">开票过程</span><span class="sxs-lookup"><span data-stu-id="eacdf-179">Invoicing procedure</span></span>

<span data-ttu-id="eacdf-180">在可以对里程碑付款开票时，您使用该过程以便为分期付款金额开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-180">When the milestone payments are ready to be invoiced, you use the procedure for invoicing on-account amounts.</span></span>

## <a name="vendor-invoicing"></a><span data-ttu-id="eacdf-181">开供应商发票 </span><span class="sxs-lookup"><span data-stu-id="eacdf-181">Vendor invoicing</span></span>
<span data-ttu-id="eacdf-182">在您从供应商订购物料并将物料分配给项目时，您为物料的采购订单行选择的行属性可确定是否已将采购物料开票给客户。</span><span class="sxs-lookup"><span data-stu-id="eacdf-182">When you order an item from a vendor and assign the item to a project, the line property that you select for the purchase order line for that item determines whether the purchased item is invoiced to a customer.</span></span> <span data-ttu-id="eacdf-183">如果您设置了默认行属性，将在采购订单行（行明细&gt;项目&gt;行属性）上显示物料的默认行属性。</span><span class="sxs-lookup"><span data-stu-id="eacdf-183">If you set up default line properties, they are displayed for the item on the purchase order line (Line details &gt; Project &gt; Line property).</span></span> <span data-ttu-id="eacdf-184">有两种方法可修改记录属性：</span><span class="sxs-lookup"><span data-stu-id="eacdf-184">There are two ways to modify the line property:</span></span>

-   <span data-ttu-id="eacdf-185">对物料的项目客户开票：将物料的行属性设置为采购订单的一个应计费值，然后通过使用正确的项目开票方法对该客户开票。</span><span class="sxs-lookup"><span data-stu-id="eacdf-185">Invoice the project's customer for the item: Set the line property for the item to a chargeable value on the purchase order, and then invoice the customer by using the correct project invoicing method.</span></span>
-   <span data-ttu-id="eacdf-186">请不要为物料的项目客户开票：不要选择物料的采购订单行上的“**应计费**”行属性。</span><span class="sxs-lookup"><span data-stu-id="eacdf-186">Don’t invoice the project's customer for the item: Don’t select the **Chargeable** line property on the purchase order line for the item.</span></span> <span data-ttu-id="eacdf-187">然后您可以采购订单开票，且无需执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="eacdf-187">You can then invoice the purchase order, and no further action is required.</span></span>

## <a name="credit-notes"></a><span data-ttu-id="eacdf-188">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="eacdf-188">Credit notes</span></span>
<span data-ttu-id="eacdf-189">在客户发票的金额具有负值时，该发票将划分为贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-189">When an amount on a customer invoice has a negative value, the invoice is classified as a credit note.</span></span> <span data-ttu-id="eacdf-190">当该文档打印时，该前缀为“贷方通知单”。</span><span class="sxs-lookup"><span data-stu-id="eacdf-190">When the document is printed, it has the title "Credit note."</span></span> 

<span data-ttu-id="eacdf-191">在您创建贷方通知单以便贷记以前开票的金额时，必须首先选择用于贷记的已开票金额。</span><span class="sxs-lookup"><span data-stu-id="eacdf-191">When you create a credit note to credit an amount that was previously invoiced, you must first select the invoiced amount for crediting.</span></span> <span data-ttu-id="eacdf-192">然后，您通过遵循用于创建普通发票的相同过程，创建贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-192">You then create a credit note by following the same procedure that you would use to create an ordinary customer invoice.</span></span> <span data-ttu-id="eacdf-193">换言之，您必须选择以前在发票上过帐的交易记录，然后创建和过帐贷方通知单方案。</span><span class="sxs-lookup"><span data-stu-id="eacdf-193">In other words, you select the transactions that were previously posted on a customer invoice, and then create and post a credit note proposal.</span></span> 

<span data-ttu-id="eacdf-194">同一文档可以包括为贷记选择的交易记录、贷方交易记录和已过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-194">The same document can include transactions that are selected for crediting, credit transactions, and transactions that have been posted.</span></span> <span data-ttu-id="eacdf-195">根据总金额是正还是负，分类将是发票或贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-195">The document is classified as either an invoice or a credit note, depending on whether the total amount is positive or negative.</span></span> 

<span data-ttu-id="eacdf-196">若要贷记已开票金额，您需要首先选择要贷记的已开票金额，然后创建贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-196">To credit an invoiced amount, you first select the invoiced amount to credit and then create a credit note.</span></span> <span data-ttu-id="eacdf-197">您通过遵循用于生成客户发票的相同过程，创建贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-197">You create a credit note by following the same procedure that you would use to generate a customer invoice.</span></span> 

<span data-ttu-id="eacdf-198">您可以创建面额为负数的发票，此发票被归类于贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="eacdf-198">You can create an invoice that has a negative amount, which becomes an invoice that is classified as a credit note.</span></span> <span data-ttu-id="eacdf-199">若要创建和打印贷方通知单，您必须为客户发票选择以前已过帐的交易记录，然后修改交易记录。</span><span class="sxs-lookup"><span data-stu-id="eacdf-199">To create and print a credit note, you must select the transactions that were previously posted for a customer invoice, and then modify the transactions.</span></span> <span data-ttu-id="eacdf-200">除非法人的主要地址在德国，否则发票的标题为“修正发票”。</span><span class="sxs-lookup"><span data-stu-id="eacdf-200">Unless the primary address of the legal entity is in Germany, the title of the invoice will be "Corrective invoice."</span></span>




