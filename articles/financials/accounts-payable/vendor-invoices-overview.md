---
title: "供应商发票概览"
description: "本文提供有关供应商发票的一般信息。 供应商发票收到的产品和服务的付款请求。 供应商发票可以表示正在进行中的服务的帐单，也可以基于特定物料和服务的采购订单。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 83d325b6511cb17156d3ef40d08cf09258d3f285
ms.openlocfilehash: 90e30200d508b45da3891776aac6014840cc1ecf
ms.contentlocale: zh-cn
ms.lasthandoff: 01/10/2018

---

# <a name="vendor-invoices-overview"></a><span data-ttu-id="1398f-105">供应商发票概览</span><span class="sxs-lookup"><span data-stu-id="1398f-105">Vendor invoices overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1398f-106">本文提供有关供应商发票的一般信息。</span><span class="sxs-lookup"><span data-stu-id="1398f-106">This article provides general information about vendor invoices.</span></span> <span data-ttu-id="1398f-107">供应商发票收到的产品和服务的付款请求。</span><span class="sxs-lookup"><span data-stu-id="1398f-107">Vendor invoices are requests for payment for products and services that were received.</span></span> <span data-ttu-id="1398f-108">供应商发票可以表示正在进行中的服务的帐单，也可以基于特定物料和服务的采购订单。</span><span class="sxs-lookup"><span data-stu-id="1398f-108">Vendor invoices can represent a bill for ongoing services, or they can be based on purchase orders for specific items and services.</span></span> 

<a name="vendor-invoices"></a><span data-ttu-id="1398f-109">供应商发票</span><span class="sxs-lookup"><span data-stu-id="1398f-109">Vendor invoices</span></span>
---------------

<span data-ttu-id="1398f-110">采购订单中的供应商发票是在根据对供应商下达的采购订单收到产品或服务时生产的发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-110">A vendor invoice from a purchase order is an invoice that is produced when products or services are received according to a purchase order that was placed with a vendor.</span></span> <span data-ttu-id="1398f-111">供应商发票包含一个标题以及一个或多个物料或服务行。</span><span class="sxs-lookup"><span data-stu-id="1398f-111">The vendor invoice contains a header, and one or more lines for items or services.</span></span> <span data-ttu-id="1398f-112">供应商发票完成从采购订单到物料收货到供应商发票的周期。</span><span class="sxs-lookup"><span data-stu-id="1398f-112">A vendor invoice completes the cycle from purchase order to product receipt to vendor invoice.</span></span> 

<span data-ttu-id="1398f-113">尽管某些供应商发票连接到采购订单，但供应商发票还可以包含不对应于采购订单行的行。</span><span class="sxs-lookup"><span data-stu-id="1398f-113">Although some vendor invoices are connected to a purchase order, vendor invoices can also contain lines that don't correspond to purchase order lines.</span></span> <span data-ttu-id="1398f-114">您还可以创建与任何采购订单都没有关联的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-114">You can also create vendor invoices that aren't associated with any purchase order.</span></span> <span data-ttu-id="1398f-115">这些供应商发票可能代表正在进行中的服务，例如电费单，并且您不必在添加它们时参考采购订单。</span><span class="sxs-lookup"><span data-stu-id="1398f-115">These vendor invoices might represent ongoing services, such as a utility bill, and you don't have to reference a purchase order when you add them.</span></span> 

<span data-ttu-id="1398f-116">有多种方式来输入供应商发票：</span><span class="sxs-lookup"><span data-stu-id="1398f-116">There are several ways to enter a vendor invoice:</span></span>

-   <span data-ttu-id="1398f-117">供应商发票登记簿能让您快速输入不引用采购订单的发票，因此，您可以计入费用。</span><span class="sxs-lookup"><span data-stu-id="1398f-117">The vendor invoice register lets you quickly enter invoices that don't reference a purchase order, so that you can accrue the expense.</span></span> <span data-ttu-id="1398f-118">通过使用供应商发票审核日记帐，您可以选择这些发票并将其过帐到供应商余额以冲销应计。</span><span class="sxs-lookup"><span data-stu-id="1398f-118">By using the vendor invoice approval journal, you can select those invoices and post them to the vendor balance to reverse the accrual.</span></span>
-   <span data-ttu-id="1398f-119">供应商发票日记帐能让您仅用一个步骤即可快速输入不引用采购订单的发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-119">The vendor invoice journal lets you quickly enter invoices that don't reference a purchase order, in a single step.</span></span>
-   <span data-ttu-id="1398f-120">与供应商发票池一起，供应商发票登记簿能让您快速输入发票以计入费用。</span><span class="sxs-lookup"><span data-stu-id="1398f-120">Together with the vendor invoice pool, the vendor invoice register lets you quickly enter invoices to accrue the expense.</span></span> <span data-ttu-id="1398f-121">您可以以后打开关联的采购订单以比对支出帐户过帐发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-121">You can open the associated purchase orders later to post the invoice against the expense account.</span></span>
-   <span data-ttu-id="1398f-122">“**打开供应商发票**”和“**待定供应商发票**”页能让您从已确认的采购订单创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-122">The **Open vendor invoices** and **Pending vendor invoices** pages let you create vendor invoices from confirmed purchase orders.</span></span>

<span data-ttu-id="1398f-123">以下讨论提供有关如何使用**“未结供应商发票”**或**“待定供应商发票”**页从采购订单创建供应商发票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1398f-123">The following discussion provide more information about how to use the **Open vendor invoices** or **Pending vendor invoices** page to create a vendor invoice from a purchase order.</span></span>

## <a name="understanding-invoice-line-quantities"></a><span data-ttu-id="1398f-124">了解发票行数量</span><span class="sxs-lookup"><span data-stu-id="1398f-124">Understanding invoice line quantities</span></span>
<span data-ttu-id="1398f-125">当从相关采购订单中打开供应商发票时，会从采购订单创建发票行。</span><span class="sxs-lookup"><span data-stu-id="1398f-125">When you open a vendor invoice from a related purchase order, invoice lines are created from the purchase order.</span></span> <span data-ttu-id="1398f-126">默认情况下，会从产品收货数量中减去此数量。</span><span class="sxs-lookup"><span data-stu-id="1398f-126">By default, the quantities are taken from the product receipt quantity.</span></span> <span data-ttu-id="1398f-127">但是，您可以使用以下任何默认行为：</span><span class="sxs-lookup"><span data-stu-id="1398f-127">However, you can use any of the following default behaviors:</span></span>

-   <span data-ttu-id="1398f-128">**当前接收量** – 对部分装运使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1398f-128">**Receive now quantity** – Use this option for partial shipments.</span></span> <span data-ttu-id="1398f-129">**“数量”**字段中的默认值来自采购订单上的**“当前接收量”**。</span><span class="sxs-lookup"><span data-stu-id="1398f-129">The default value in the **Quantity** field is taken from the **Receive now** quantity field on the purchase order.</span></span>
-   <span data-ttu-id="1398f-130">**订购数量** – 对整个装运使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1398f-130">**Ordered quantity** – Use this option for complete shipments.</span></span> <span data-ttu-id="1398f-131">**“数量”**字段中的默认数量来自采购订单上的**“订购数量”**。</span><span class="sxs-lookup"><span data-stu-id="1398f-131">The default value in the **Quantity** field is taken from the **Ordered** quantity field on the purchase order.</span></span>
-   <span data-ttu-id="1398f-132">**登记数量** – 如果物料需要登记，则使用此选项，如在**“物料模型组”**页上指定的一样。</span><span class="sxs-lookup"><span data-stu-id="1398f-132">**Registered quantity** – Use this option if the item requires registration, as specified on the **Item model groups** page.</span></span> <span data-ttu-id="1398f-133">“**数量**”字段中的默认值是已登记的实际更新数量。</span><span class="sxs-lookup"><span data-stu-id="1398f-133">The default value in the **Quantity** field is the physical update quantity that has been registered.</span></span>
-   <span data-ttu-id="1398f-134">**产品收据数量** – 如果已经针对订单收到了产品收据，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1398f-134">**Product receipt quantity** – Use this option if a product receipt has already been received for the order.</span></span> <span data-ttu-id="1398f-135">“**数量**”字段中的默认值来自可用产品收据的总数量。</span><span class="sxs-lookup"><span data-stu-id="1398f-135">The default value in the **Quantity** field is taken from the total quantity of available product receipts.</span></span>
-   <span data-ttu-id="1398f-136">**已注册数量和服务** – 如果已经针对已库存或未库存的物料在到达日志中登记数量，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1398f-136">**Registered quantity and services** – Use this option if quantities have been registered in arrival journals for stocked items or items that aren't stocked.</span></span> <span data-ttu-id="1398f-137">此选项还包括服务（无论是否登记）。</span><span class="sxs-lookup"><span data-stu-id="1398f-137">This option also includes services, regardless of whether they are registered.</span></span>

<span data-ttu-id="1398f-138">如果您的法人使用发票匹配，您可以在“**产品收据数量匹配**”列中查看数量匹配的结果。</span><span class="sxs-lookup"><span data-stu-id="1398f-138">If your legal entity uses invoice matching, you can view the results of the quantity matching in the **Product receipt quantity match** column.</span></span> <span data-ttu-id="1398f-139">您还可以使用**“检查”**选项卡上的**“匹配详细信息”**菜单命令查看数量匹配的结果。</span><span class="sxs-lookup"><span data-stu-id="1398f-139">You can also use the **Matching details** menu command on the **Review** tab to view the results of the quantity matching.</span></span>

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a><span data-ttu-id="1398f-140">添加不在采购订单上的行</span><span class="sxs-lookup"><span data-stu-id="1398f-140">Adding a line that wasn't on the purchase order</span></span>
<span data-ttu-id="1398f-141">您可以将不在采购订单上的行添加到供应商发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-141">You can add a new line that wasn't on the purchase order to the vendor invoice.</span></span> <span data-ttu-id="1398f-142">您必须选择物料编号或采购类别。</span><span class="sxs-lookup"><span data-stu-id="1398f-142">You must select an item number or procurement category.</span></span> <span data-ttu-id="1398f-143">您可以向该行添加数量、价格和金额。</span><span class="sxs-lookup"><span data-stu-id="1398f-143">You can then add quantities, prices, and amounts to the line.</span></span> <span data-ttu-id="1398f-144">该行将仅包括在发票合计的匹配政策中。</span><span class="sxs-lookup"><span data-stu-id="1398f-144">The line will be included only in matching policies for invoice totals.</span></span>

## <a name="submitting-a-vendor-invoice-for-review"></a><span data-ttu-id="1398f-145">提交供应商发票，以供审核</span><span class="sxs-lookup"><span data-stu-id="1398f-145">Submitting a vendor invoice for review</span></span>
<span data-ttu-id="1398f-146">您的组织可以使用工作流来管理供应商发票的审核流程。</span><span class="sxs-lookup"><span data-stu-id="1398f-146">Your organization might use workflows to manage the review process for vendor invoices.</span></span> <span data-ttu-id="1398f-147">可能需要对发票抬头、发票行或两者进行工作流审核。</span><span class="sxs-lookup"><span data-stu-id="1398f-147">Workflow review can be required for the invoice header, the invoice line, or both.</span></span> <span data-ttu-id="1398f-148">工作流控件适用于抬头或行，具体取决于单击该控件时焦点的位置。</span><span class="sxs-lookup"><span data-stu-id="1398f-148">The workflow controls apply to the header or the line, depending on where the focus is when you click the control.</span></span> <span data-ttu-id="1398f-149">您将看到的不是**“过帐”**按钮，而是**“提交”**按钮，您可以使用它来通过审核流程发送供应商发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-149">Instead of the **Post** button, you will see a **Submit** button that you can use to send the vendor invoice through the review process.</span></span>

## <a name="matching-vendor-invoices-to-product-receipts"></a><span data-ttu-id="1398f-150">将供应商发票与产品收据匹配</span><span class="sxs-lookup"><span data-stu-id="1398f-150">Matching vendor invoices to product receipts</span></span>
<span data-ttu-id="1398f-151">您可以输入和保存供应商发票的信息，您还可以将发票行匹配产品收据行。</span><span class="sxs-lookup"><span data-stu-id="1398f-151">You can enter and save information for vendor invoices, and you can match invoice lines to product receipt lines.</span></span> <span data-ttu-id="1398f-152">如果需要，还可以匹配行的部分数量。</span><span class="sxs-lookup"><span data-stu-id="1398f-152">You can also match partial quantities for a line.</span></span> 

<span data-ttu-id="1398f-153">您可以创建基于迄今已接收的产品收据行物料的供应商发票，即使尚未接收特定采购订单的所有物料。</span><span class="sxs-lookup"><span data-stu-id="1398f-153">You can create a vendor invoice that is based on the product receipt line items that have been received to date, even if all the items for a particular purchase order haven't yet been received.</span></span> <span data-ttu-id="1398f-154">例如，如果供应商每个月发送一张支票，该供应商支票涵盖您在该月中发运的所有交货，则可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1398f-154">For example, you might use this option if a vendor sends one invoice per month that covers all the deliveries that the vendor shipped during that month.</span></span> <span data-ttu-id="1398f-155">每个产品收据都表示该采购订单上物料的部分或全部交货。</span><span class="sxs-lookup"><span data-stu-id="1398f-155">Each product receipt represents a partial or complete delivery of the items on the purchase order.</span></span> 

<span data-ttu-id="1398f-156">在您过帐该发票时，每个物料的“**未开票数量**”都用来自所选产品收据的已收货数量的总数更新。</span><span class="sxs-lookup"><span data-stu-id="1398f-156">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the received quantities from the selected product receipts.</span></span> <span data-ttu-id="1398f-157">如果采购订单上所有物料的**未开票数量**和**剩余交货量**均为 0（零），则该采购订单的状态将更改为**已开票**。</span><span class="sxs-lookup"><span data-stu-id="1398f-157">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the purchase order are 0 (zero), the status of the purchase order is changed to **Invoiced**.</span></span> <span data-ttu-id="1398f-158">如果**“未开票数量”**不为 0，则该采购订单的状态将不更改，并且可为其输入其他发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-158">If the **Invoice remainder** quantity isn't 0, the status of the purchase order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="1398f-159">此选项假定为该采购订单至少过帐了一个产品收据。</span><span class="sxs-lookup"><span data-stu-id="1398f-159">This option assumes that at least one product receipt has been posted for the purchase order.</span></span> <span data-ttu-id="1398f-160">供应商发票基于这些产品收据并反映来自这些装箱单的数量。</span><span class="sxs-lookup"><span data-stu-id="1398f-160">The vendor invoice is based on these product receipts and reflects the quantities from them.</span></span> <span data-ttu-id="1398f-161">该发票的财务信息基于在您过帐该发票时输入的信息。</span><span class="sxs-lookup"><span data-stu-id="1398f-161">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span>

<span data-ttu-id="1398f-162">有关详细信息，请参阅[记录供应商发票和匹配接收的数量](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)。</span><span class="sxs-lookup"><span data-stu-id="1398f-162">For more information, see [Record vendor invoice and match against received quantity](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).</span></span>

## <a name="working-with-multiple-invoices"></a><span data-ttu-id="1398f-163">使用多个发票</span><span class="sxs-lookup"><span data-stu-id="1398f-163">Working with multiple invoices</span></span>

<span data-ttu-id="1398f-164">您可以同时处理多张发票以及同时全部过帐。</span><span class="sxs-lookup"><span data-stu-id="1398f-164">You can work with multiple invoices at the same time and post them all at the same time.</span></span> <span data-ttu-id="1398f-165">如果您必须创建多个发票，请使用**“待定供应商发票”**页。</span><span class="sxs-lookup"><span data-stu-id="1398f-165">If you must create multiple invoices, use the **Pending vendor invoices** page.</span></span> <span data-ttu-id="1398f-166">如果您必须过帐和打印多个供应商发票，请使用发票审核日记帐页。</span><span class="sxs-lookup"><span data-stu-id="1398f-166">If you must post and print multiple vendor invoices, use the invoice approval journal page.</span></span> <span data-ttu-id="1398f-167">如果您使用发票审核日记帐，则必须针对该采购订单过帐至少一个产品收据，并且在发票登记簿中必须过帐该采购订单的发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-167">If you're using the invoice approval journal, at least one product receipt must be posted for the purchase order, and an invoice for the purchase order must be posted in an invoice register.</span></span> <span data-ttu-id="1398f-168">该发票的财务信息来自在该发票登记簿中已过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="1398f-168">The financial information for the invoice comes from the invoice that was posted in the register.</span></span>


<span data-ttu-id="1398f-169">有关详细信息，请参阅: </span><span class="sxs-lookup"><span data-stu-id="1398f-169">For more information see:</span></span>

 - [<span data-ttu-id="1398f-170">设置供应商发票策略</span><span class="sxs-lookup"><span data-stu-id="1398f-170">Set up vendor invoice policies</span></span>](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [<span data-ttu-id="1398f-171">使用供应商发票将发票数据键入应付账款</span><span class="sxs-lookup"><span data-stu-id="1398f-171">Key invoice data into accounts payable using a vendor invoice</span></span>](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [<span data-ttu-id="1398f-172">使用审核日记帐将发票数据键入应付帐款</span><span class="sxs-lookup"><span data-stu-id="1398f-172">Key invoice data into accounts payable using an approval journal</span></span>](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [<span data-ttu-id="1398f-173">使用发票池将发票数据键入 AP 系统</span><span class="sxs-lookup"><span data-stu-id="1398f-173">Key invoice data into the AP system using invoice pool</span></span>](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [<span data-ttu-id="1398f-174">在发票日记帐中记录供应商发票</span><span class="sxs-lookup"><span data-stu-id="1398f-174">Record a vendor invoice in the invoice journal</span></span>](tasks/record-vendor-invoice-invoice-journal.md)


