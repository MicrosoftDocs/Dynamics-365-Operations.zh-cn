---
title: "创建客户发票"
description: "**“销售订单的客户发票”**是与销售相关的、组织提供给客户的单据。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f08131e01fddb259d3bb537b1625ea2615a1e958
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="8ec4b-103">创建客户发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-103">Create a customer invoice</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="8ec4b-104">**“销售订单的客户发票”**是与销售相关的、组织提供给客户的单据。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="8ec4b-105">此类型的客户发票是基于销售订单创建的，其中包括订单行和物料编号。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="8ec4b-106">在分类帐中指定和过帐物料编号。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="8ec4b-107">子分类日志条目为销售订单的客户发票不可用。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="8ec4b-108">有关详细信息，请参阅[创建销售订单发票](tasks/create-sales-order-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="8ec4b-109">**“普通发票”**与销售订单无关。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="8ec4b-110">它包含包括会计科目、自由文本描述和您输入的销售额的订单行。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="8ec4b-111">您无法在此类发票上输入物料编号。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="8ec4b-112">您必须输入相应的增值税信息。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="8ec4b-113">销售的主科目在每个发票行上指示，这样可以通过单击**“普通发票”**页上的**“分摊金额”**分配给多个会计科目。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="8ec4b-114">此外，将客户余额从用于普通发票的过帐模板过帐到汇总科目。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="8ec4b-115">有关详细信息，请参阅: </span><span class="sxs-lookup"><span data-stu-id="8ec4b-115">For more information see:</span></span>

[<span data-ttu-id="8ec4b-116">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-116">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="8ec4b-117">创建普通模板</span><span class="sxs-lookup"><span data-stu-id="8ec4b-117">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="8ec4b-118">向客户分配普通发票模板</span><span class="sxs-lookup"><span data-stu-id="8ec4b-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="8ec4b-119">生成和过帐重复执行普通发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="8ec4b-120">**“估价单”**是一种在过帐发票前作为对实际发票金额的评估而准备的发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="8ec4b-121">您可为用于销售订单的客户发票或普通发票打印估价单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="8ec4b-122">过帐并打印基于销售订单的各个客户发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="8ec4b-123">使用此流程创建基于销售订单的发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="8ec4b-124">如果您决定在交付货物或服务之前给客户开发票，您可以执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="8ec4b-125">在您过帐该发票时，每个物料的**未开票数量**都用来自所选销售订单的已开发票的数量的总数更新。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="8ec4b-126">如果销售订单上所有物料的**“未开票数量”**和**“剩余交货量”**均为 0（零），则该销售订单的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="8ec4b-127">如果**“未开票数量”**不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="8ec4b-128">您可以在**“所有销售订单”**列表页上查看销售订单的状态。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="8ec4b-129">使用**“未结客户发票”**列表页可查看您过帐了的发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="8ec4b-130">过帐和打印基于装箱单和日期的各个客户发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="8ec4b-131">当一个或多个装箱单已针对销售订单过帐时，请使用此流程。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="8ec4b-132">客户发票基于这些装箱单并反映来自这些装箱单的数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="8ec4b-133">该发票的财务信息基于在您过帐该发票时输入的信息。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="8ec4b-134">您可以创建基于迄今已发运的装箱单行物料的客户发票，即使尚未发运特定销售订单的所有物料。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="8ec4b-135">例如，如果您的法人每个月为每个客户签发一张支票，该支票涵盖您在该月中发运的所有交货，则可以执行上述操作。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="8ec4b-136">每个装箱单都表示该销售订单上物料的部分或全部交货。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="8ec4b-137">在您过帐该发票时，每个物料的**“未开票数量”**都用来自所选装箱单的已交货数量的总数更新。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="8ec4b-138">如果销售订单上所有物料的**“未开票数量”**和**“剩余交货量”**均为 0（零），则该销售订单的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="8ec4b-139">如果**“未开票数量”**不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="8ec4b-140">库存交易记录用发票编号更新，并且销售订单上的**“行状态”**字段中的状态将更改为**“已开票”**。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="8ec4b-141">在**“所有销售订单”**列表页中查看销售订单的状态。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="8ec4b-142">合并销售订单或装箱单以进行过帐</span><span class="sxs-lookup"><span data-stu-id="8ec4b-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="8ec4b-143">当一个或多个销售订单已做好开票准备，并且您希望将其合并到一张发票时，使用此流程。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="8ec4b-144">您可以在**“销售订单”**列表页上选择多个发票，然后使用**“生成发票”**来合并它们。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="8ec4b-145">在**过帐发票**页上，可以更改**汇总订单**设置以便按订单编号汇总（其中单个销售订单有多个装箱单）或按发票帐户汇总（其中单个发票帐户有多个销售订单）。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="8ec4b-146">使用**排列**按钮可基于**汇总订单**设置将销售订单合并到单个发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="8ec4b-147">更改过帐行为的附加设置</span><span class="sxs-lookup"><span data-stu-id="8ec4b-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="8ec4b-148">以下字段更改过帐流程的行为。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ec4b-149">字段</span><span class="sxs-lookup"><span data-stu-id="8ec4b-149">Field</span></span></th>
<th><span data-ttu-id="8ec4b-150">描述</span><span class="sxs-lookup"><span data-stu-id="8ec4b-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ec4b-151">数量</span><span class="sxs-lookup"><span data-stu-id="8ec4b-151">Quantity</span></span></td>
<td><span data-ttu-id="8ec4b-152">选择过帐单据所基于的数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="8ec4b-153">可用的选项取决于正在过帐的单据类型，如装箱单或发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="8ec4b-154"><strong>“当前交货量”</strong> – 选择在<strong>“当前交货量”</strong>字段中输入的所有数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="8ec4b-155">使用此选项可以确认或交货部分订单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="8ec4b-156"><strong>已领料</strong> – 选择已领取的全部数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="8ec4b-157"><strong>全部</strong> – 选择尚未按当前文件类型进行更新的全部销售订单的数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="8ec4b-158"><strong>装箱单</strong> – 选择装箱单已更新的所有数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="8ec4b-159"><strong>领料数量和未贮存产品</strong> – 选择领料的全部数量以及未贮存产品的全部数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-160">正在过帐</span><span class="sxs-lookup"><span data-stu-id="8ec4b-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="8ec4b-161">选择此选项可将销售订单记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="8ec4b-162">清除此选项可以打印估价销售订单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="8ec4b-163"><strong>注释：</strong>如果已就付款计划签订协议，付款计划不会显示在估价销售订单上。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="8ec4b-164">付款计划只显示在实际销售订单上。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec4b-165">后期选择</span><span class="sxs-lookup"><span data-stu-id="8ec4b-165">Late selection</span></span></td>
<td><span data-ttu-id="8ec4b-166">选择此选项可稍后应用所选查询。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="8ec4b-167">此选项用于批处理作业。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-167">This option is used for batch jobs.</span></span> <span data-ttu-id="8ec4b-168">在批处理作业运行时，查询会运行。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-169">缩减数量</span><span class="sxs-lookup"><span data-stu-id="8ec4b-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="8ec4b-170">选择此选项可以在过帐单据时自动减少已交货数量，以便已交货数量等于可用库存。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec4b-171">打印</span><span class="sxs-lookup"><span data-stu-id="8ec4b-171">Print</span></span></td>
<td><span data-ttu-id="8ec4b-172">选择打印单据的时间：</span><span class="sxs-lookup"><span data-stu-id="8ec4b-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="8ec4b-173"><strong>当前</strong> – 在更新每张发票后打印单据。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="8ec4b-174"><strong>之后</strong> – 在更新所有发票后打印单据。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="8ec4b-175">
<strong>注释：</strong>只有在选择<strong>“打印发票”</strong>、<strong>“打印确认单”</strong>、<strong>“打印领料单”</strong>或<strong>“打印装箱单”</strong>选项后，<strong>“打印”</strong>字段才可用。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="8ec4b-176">例如，在<strong>“窗体排序”</strong>页上，您已将系统设置为按照发票帐户对信息进行排序。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="8ec4b-177">然后您可以选择<strong>“之后”</strong>以打印按发票帐户进行排序的批次中的单据。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="8ec4b-178">否则，会在完成处理之前打印单据，并且单据不会按<strong>“窗体排序”</strong>页上指定的顺序进行排序。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-179">打印发票</span><span class="sxs-lookup"><span data-stu-id="8ec4b-179">Print invoice</span></span></td>
<td><span data-ttu-id="8ec4b-180">选择此选项可以打印发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-180">Select this option to print the invoice.</span></span> <span data-ttu-id="8ec4b-181">如果该选项已关闭，您可以过帐发票而不打印它。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec4b-182">发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="8ec4b-182">Send e-mail</span></span></td>
<td><span data-ttu-id="8ec4b-183">选择此选项可以在过帐发票后将销售订单的发票作为电子邮件附件发送给客户。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="8ec4b-184">附件将作为 PDF 和 XML 文件发送。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="8ec4b-185">只有当您在<strong>“电子发票参数”</strong>页上选择<strong>“启用 CFD (电子发票)”</strong>选项时，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="8ec4b-186"><strong>注释：</strong>(MEX) 此控件仅对主地址在墨西哥的法人可用。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-187">使用打印管理目标</span><span class="sxs-lookup"><span data-stu-id="8ec4b-187">Use print management destination</span></span></td>
<td><span data-ttu-id="8ec4b-188">选择此选项可以使用在<strong>打印管理设置</strong>页上为交易记录、单据或模块指定的打印设置。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec4b-189">检查信用额度</span><span class="sxs-lookup"><span data-stu-id="8ec4b-189">Check credit limit</span></span></td>
<td><span data-ttu-id="8ec4b-190">选择在执行信用额度检查时分析的内容。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="8ec4b-191"><strong>无</strong> - 对于信用额度检查没有要求。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="8ec4b-192"><strong>余额</strong> - 对客户余额检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="8ec4b-193"><strong>余额+装箱单或产品收据</strong> – 通过客户余额和交货情况检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="8ec4b-194"><strong>余额+所有</strong> - 对客户余额、交货和未结订单检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-195">信用更正</span><span class="sxs-lookup"><span data-stu-id="8ec4b-195">Credit correction</span></span></td>
<td><span data-ttu-id="8ec4b-196">选择此选项可以将贷方通知单显示为凭证交易记录中的借记。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec4b-197">贷方剩余数量</span><span class="sxs-lookup"><span data-stu-id="8ec4b-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="8ec4b-198">如果过帐的是贷方通知单，请选中此选项以保留订单上的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="8ec4b-199">如果清除此选项，剩余数量将设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec4b-200">汇总更新</span><span class="sxs-lookup"><span data-stu-id="8ec4b-200">Summary update for</span></span></td>
<td><span data-ttu-id="8ec4b-201">选择汇总多个销售订单将使用的方法：</span><span class="sxs-lookup"><span data-stu-id="8ec4b-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="8ec4b-202"><strong>无</strong> – 不汇总销售订单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="8ec4b-203">例如，对于每个销售订单创建单独的发票。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="8ec4b-204"><strong>“发票帐户”</strong> – 根据在<strong>“汇总更新参数”</strong>页上设置的条件，汇总所选的所有订单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="8ec4b-205"><strong>订单</strong> – 将所选范围内的订单汇总到指定的一张订单中。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="8ec4b-206">将根据在<strong>“汇总更新参数”</strong>页上设置的条件对所选订单进行汇总。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="8ec4b-207">如果选择此选项，则必须在<strong>“销售订单”</strong>字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="8ec4b-208"><strong>“自动汇总”</strong> – 如果已在<strong>“汇总更新”</strong>页上指定了汇总更新，则根据在<strong>“汇总更新参数”</strong>页上设置的条件对所选的所有订单进行汇总。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="8ec4b-209">如果未指定汇总更新，则将单独过帐订单。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="8ec4b-210"><strong>装箱单</strong> – 对于每张装箱单，将所选范围内的订单汇总到一张发票中。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="8ec4b-211">仅当在<strong>“数量”</strong>字段中选择<strong>“装箱单”</strong>后，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="8ec4b-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






