---
title: "创建客户发票"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="d9ca4-102">创建客户发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d9ca4-103">**“销售订单的客户发票”**是与销售相关的、组织提供给客户的单据。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="d9ca4-104">此类型的客户发票是基于销售订单创建的，其中包括订单行和物料编号。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="d9ca4-105">在分类帐中指定和过帐物料编号。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="d9ca4-106">子分类日志条目为销售订单的客户发票不可用。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="d9ca4-107">有关详细信息，请参阅[创建销售订单发票](tasks/create-sales-order-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="d9ca4-108">**“普通发票”**与销售订单无关。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="d9ca4-109">它包含包括会计科目、自由文本描述和您输入的销售额的订单行。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="d9ca4-110">您无法在此类发票上输入物料编号。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="d9ca4-111">您必须输入相应的增值税信息。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="d9ca4-112">销售的主科目在每个发票行上指示，这样可以通过单击**“普通发票”**页上的**“分摊金额”**分配给多个会计科目。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="d9ca4-113">此外，将客户余额从用于普通发票的过帐模板过帐到汇总科目。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="d9ca4-114">有关详细信息，请参阅: </span><span class="sxs-lookup"><span data-stu-id="d9ca4-114">For more information see:</span></span>

[<span data-ttu-id="d9ca4-115">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="d9ca4-116">创建普通模板</span><span class="sxs-lookup"><span data-stu-id="d9ca4-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="d9ca4-117">向客户分配普通发票模板</span><span class="sxs-lookup"><span data-stu-id="d9ca4-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="d9ca4-118">生成和过帐重复执行普通发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="d9ca4-119">**“估价单”**是一种在过帐发票前作为对实际发票金额的评估而准备的发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="d9ca4-120">您可为用于销售订单的客户发票或普通发票打印估价单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="d9ca4-121">过帐并打印基于销售订单的各个客户发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="d9ca4-122">使用此流程创建基于销售订单的发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="d9ca4-123">如果您决定在交付货物或服务之前给客户开发票，您可以执行此操作。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="d9ca4-124">在您过帐该发票时，每个物料的**未开票数量**都用来自所选销售订单的已开发票的数量的总数更新。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="d9ca4-125">如果销售订单上所有物料的**“未开票数量”**和**“剩余交货量”**均为 0（零），则该销售订单的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="d9ca4-126">如果**“未开票数量”**不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="d9ca4-127">您可以在**“所有销售订单”**列表页上查看销售订单的状态。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="d9ca4-128">使用**“未结客户发票”**列表页可查看您过帐了的发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="d9ca4-129">过帐和打印基于装箱单和日期的各个客户发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="d9ca4-130">当一个或多个装箱单已针对销售订单过帐时，请使用此流程。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="d9ca4-131">客户发票基于这些装箱单并反映来自这些装箱单的数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="d9ca4-132">该发票的财务信息基于在您过帐该发票时输入的信息。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="d9ca4-133">您可以创建基于迄今已发运的装箱单行物料的客户发票，即使尚未发运特定销售订单的所有物料。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="d9ca4-134">例如，如果您的法人每个月为每个客户签发一张支票，该支票涵盖您在该月中发运的所有交货，则可以执行上述操作。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="d9ca4-135">每个装箱单都表示该销售订单上物料的部分或全部交货。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="d9ca4-136">在您过帐该发票时，每个物料的**“未开票数量”**都用来自所选装箱单的已交货数量的总数更新。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="d9ca4-137">如果销售订单上所有物料的**“未开票数量”**和**“剩余交货量”**均为 0（零），则该销售订单的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="d9ca4-138">如果**“未开票数量”**不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="d9ca4-139">库存交易记录用发票编号更新，并且销售订单上的**“行状态”**字段中的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="d9ca4-140">在**“所有销售订单”**列表页中查看销售订单的状态。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="d9ca4-141">合并销售订单或装箱单以进行过帐</span><span class="sxs-lookup"><span data-stu-id="d9ca4-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="d9ca4-142">当一个或多个销售订单已做好开票准备，并且您希望将其合并到一张发票时，使用此流程。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="d9ca4-143">您可以在**“销售订单”**列表页上选择多个发票，然后使用**“生成发票”**来合并它们。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="d9ca4-144">在**过帐发票**页上，可以更改**汇总订单**设置以便按订单编号汇总（其中单个销售订单有多个装箱单）或按发票帐户汇总（其中单个发票帐户有多个销售订单）。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="d9ca4-145">使用**排列**按钮可基于**汇总订单**设置将销售订单合并到单个发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="d9ca4-146">更改过帐行为的附加设置</span><span class="sxs-lookup"><span data-stu-id="d9ca4-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="d9ca4-147">以下字段更改过帐流程的行为。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9ca4-148">字段</span><span class="sxs-lookup"><span data-stu-id="d9ca4-148">Field</span></span></th>
<th><span data-ttu-id="d9ca4-149">描述</span><span class="sxs-lookup"><span data-stu-id="d9ca4-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9ca4-150">数量</span><span class="sxs-lookup"><span data-stu-id="d9ca4-150">Quantity</span></span></td>
<td><span data-ttu-id="d9ca4-151">选择过帐单据所基于的数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="d9ca4-152">可用的选项取决于正在过帐的单据类型，如装箱单或发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="d9ca4-153"><strong>“当前交货量”</strong> – 选择在<strong>“当前交货量”</strong>字段中输入的所有数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="d9ca4-154">使用此选项可以确认或交货部分订单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="d9ca4-155"><strong>已领料</strong> – 选择已领取的全部数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="d9ca4-156"><strong>全部</strong> – 选择尚未按当前文件类型进行更新的全部销售订单的数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="d9ca4-157"><strong>装箱单</strong> – 选择装箱单已更新的所有数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="d9ca4-158"><strong>领料数量和未贮存产品</strong> – 选择领料的全部数量以及未贮存产品的全部数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-159">正在过帐</span><span class="sxs-lookup"><span data-stu-id="d9ca4-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="d9ca4-160">选择此选项可将销售订单记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="d9ca4-161">清除此选项可以打印估价销售订单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="d9ca4-162"><strong>注释：</strong>如果已就付款计划签订协议，付款计划不会显示在估价销售订单上。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="d9ca4-163">付款计划只显示在实际销售订单上。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ca4-164">后期选择</span><span class="sxs-lookup"><span data-stu-id="d9ca4-164">Late selection</span></span></td>
<td><span data-ttu-id="d9ca4-165">选择此选项可稍后应用所选查询。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="d9ca4-166">此选项用于批处理作业。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-166">This option is used for batch jobs.</span></span> <span data-ttu-id="d9ca4-167">在批处理作业运行时，查询会运行。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-168">缩减数量</span><span class="sxs-lookup"><span data-stu-id="d9ca4-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="d9ca4-169">选择此选项可以在过帐单据时自动减少已交货数量，以便已交货数量等于可用库存。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ca4-170">打印</span><span class="sxs-lookup"><span data-stu-id="d9ca4-170">Print</span></span></td>
<td><span data-ttu-id="d9ca4-171">选择打印单据的时间：</span><span class="sxs-lookup"><span data-stu-id="d9ca4-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="d9ca4-172"><strong>当前</strong> – 在更新每张发票后打印单据。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="d9ca4-173"><strong>之后</strong> – 在更新所有发票后打印单据。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="d9ca4-174">
<strong>注释：</strong>只有在选择<strong>“打印发票”</strong>、<strong>“打印确认单”</strong>、<strong>“打印领料单”</strong>或<strong>“打印装箱单”</strong>选项后，<strong>“打印”</strong>字段才可用。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="d9ca4-175">例如，在<strong>“窗体排序”</strong>页上，您已将系统设置为按照发票帐户对信息进行排序。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="d9ca4-176">然后您可以选择<strong>“之后”</strong>以打印按发票帐户进行排序的批次中的单据。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="d9ca4-177">否则，会在完成处理之前打印单据，并且单据不会按<strong>“窗体排序”</strong>页上指定的顺序进行排序。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-178">打印发票</span><span class="sxs-lookup"><span data-stu-id="d9ca4-178">Print invoice</span></span></td>
<td><span data-ttu-id="d9ca4-179">选择此选项可以打印发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-179">Select this option to print the invoice.</span></span> <span data-ttu-id="d9ca4-180">如果该选项已关闭，您可以过帐发票而不打印它。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ca4-181">发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="d9ca4-181">Send e-mail</span></span></td>
<td><span data-ttu-id="d9ca4-182">选择此选项可以在过帐发票后将销售订单的发票作为电子邮件附件发送给客户。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="d9ca4-183">附件将作为 PDF 和 XML 文件发送。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="d9ca4-184">只有当您在<strong>“电子发票参数”</strong>页上选择<strong>“启用 CFD (电子发票)”</strong>选项时，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="d9ca4-185"><strong>注释：</strong>(MEX) 此控件仅对主地址在墨西哥的法人可用。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-186">使用打印管理目标</span><span class="sxs-lookup"><span data-stu-id="d9ca4-186">Use print management destination</span></span></td>
<td><span data-ttu-id="d9ca4-187">选择此选项可以使用在<strong>打印管理设置</strong>页上为交易记录、单据或模块指定的打印设置。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ca4-188">检查信用额度</span><span class="sxs-lookup"><span data-stu-id="d9ca4-188">Check credit limit</span></span></td>
<td><span data-ttu-id="d9ca4-189">选择在执行信用额度检查时分析的内容。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="d9ca4-190"><strong>无</strong> - 对于信用额度检查没有要求。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="d9ca4-191"><strong>余额</strong> - 对客户余额检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="d9ca4-192"><strong>余额+装箱单或产品收据</strong> – 通过客户余额和交货情况检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="d9ca4-193"><strong>余额+所有</strong> - 对客户余额、交货和未结订单检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-194">信用更正</span><span class="sxs-lookup"><span data-stu-id="d9ca4-194">Credit correction</span></span></td>
<td><span data-ttu-id="d9ca4-195">选择此选项可以将贷方通知单显示为凭证交易记录中的借记。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ca4-196">贷方剩余数量</span><span class="sxs-lookup"><span data-stu-id="d9ca4-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="d9ca4-197">如果过帐的是贷方通知单，请选中此选项以保留订单上的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="d9ca4-198">如果清除此选项，剩余数量将设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ca4-199">汇总更新</span><span class="sxs-lookup"><span data-stu-id="d9ca4-199">Summary update for</span></span></td>
<td><span data-ttu-id="d9ca4-200">选择汇总多个销售订单将使用的方法：</span><span class="sxs-lookup"><span data-stu-id="d9ca4-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="d9ca4-201"><strong>无</strong> – 不汇总销售订单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="d9ca4-202">例如，对于每个销售订单创建单独的发票。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="d9ca4-203"><strong>“发票帐户”</strong> – 根据在<strong>“汇总更新参数”</strong>页上设置的条件，汇总所选的所有订单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="d9ca4-204"><strong>订单</strong> – 将所选范围内的订单汇总到指定的一张订单中。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="d9ca4-205">将根据在<strong>“汇总更新参数”</strong>页上设置的条件对所选订单进行汇总。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="d9ca4-206">如果选择此选项，则必须在<strong>“销售订单”</strong>字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="d9ca4-207"><strong>“自动汇总”</strong> – 如果已在<strong>“汇总更新”</strong>页上指定了汇总更新，则根据在<strong>“汇总更新参数”</strong>页上设置的条件对所选的所有订单进行汇总。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="d9ca4-208">如果未指定汇总更新，则将单独过帐订单。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="d9ca4-209"><strong>装箱单</strong> – 对于每张装箱单，将所选范围内的订单汇总到一张发票中。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="d9ca4-210">仅当在<strong>“数量”</strong>字段中选择<strong>“装箱单”</strong>后，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="d9ca4-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





