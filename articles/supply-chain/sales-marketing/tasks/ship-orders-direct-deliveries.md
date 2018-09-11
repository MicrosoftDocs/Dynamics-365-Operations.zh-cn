--- 
title: "以直接交运方式装运订单"
description: "该过程显示如何为销售订单创建直接交货。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 218e84b299c75a6ac3bf1bcf6706fbb146f8ab38
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="77ecc-103">以直接交运方式装运订单</span><span class="sxs-lookup"><span data-stu-id="77ecc-103">Ship orders as direct deliveries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77ecc-104">该过程显示如何为销售订单创建直接交货。</span><span class="sxs-lookup"><span data-stu-id="77ecc-104">This procedure demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="77ecc-105">在想要从供应商处直接装运货物给客户，而不是先装运至您自身的仓库时，可使用直接交货。</span><span class="sxs-lookup"><span data-stu-id="77ecc-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="77ecc-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="77ecc-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="77ecc-107">要想成功完成第二个子任务“从工作台创建直接交货”，确保您在销售订单上选择的物料有默认“供应商”，该供应商在“已发布基础产品”的“采购”快速项卡上有指定。</span><span class="sxs-lookup"><span data-stu-id="77ecc-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>


## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="77ecc-108">设置直接交货的单个订单</span><span class="sxs-lookup"><span data-stu-id="77ecc-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="77ecc-109">转到“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-109">Go to All sales orders.</span></span>
2. <span data-ttu-id="77ecc-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-110">Click New.</span></span>
3. <span data-ttu-id="77ecc-111">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-111">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="77ecc-112">如果您正在使用 USMF，可以选择帐户 US-001。</span><span class="sxs-lookup"><span data-stu-id="77ecc-112">If you’re using USMF, you can select account US-001.</span></span>  
4. <span data-ttu-id="77ecc-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-113">Click OK.</span></span>
5. <span data-ttu-id="77ecc-114">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="77ecc-115">如果您正在使用 USMF，可以选择物料 T0020。</span><span class="sxs-lookup"><span data-stu-id="77ecc-115">If you’re using USMF, you can select item T0020.</span></span>  
6. <span data-ttu-id="77ecc-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-116">Click Save.</span></span>
7. <span data-ttu-id="77ecc-117">在操作窗格上，单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-117">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="77ecc-118">单击“直接交运”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-118">Click Direct delivery.</span></span>
    * <span data-ttu-id="77ecc-119">“创建交货”页面列出所有从销售订单复制的未结销售订单行。</span><span class="sxs-lookup"><span data-stu-id="77ecc-119">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="77ecc-120">您可以查看订单的详细信息，并可根据需要修改详细信息，例如创建直接交货前的采购数量和价格条款。</span><span class="sxs-lookup"><span data-stu-id="77ecc-120">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
9. <span data-ttu-id="77ecc-121">在“全部包括”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-121">Select Yes in the Include all field.</span></span>
    * <span data-ttu-id="77ecc-122">如果您想要生成仅销售订单行的一个子集的直接交货，则单独选择这些。</span><span class="sxs-lookup"><span data-stu-id="77ecc-122">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="77ecc-123">“供应商帐户”字段可能填充也可能不填充供应商编号。</span><span class="sxs-lookup"><span data-stu-id="77ecc-123">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="77ecc-124">如果已为产品设置默认供应商（在相关物料范围），则此供应商将会复制到该行。</span><span class="sxs-lookup"><span data-stu-id="77ecc-124">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="77ecc-125">否则，您必须手动输入供应商。</span><span class="sxs-lookup"><span data-stu-id="77ecc-125">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="77ecc-126">在此示例中，我们将在下一步选择新供应商（即使已填充一个供应商）。</span><span class="sxs-lookup"><span data-stu-id="77ecc-126">In this example, we’ll select a new vendor in the next step, even if one is already populated.</span></span>   
10. <span data-ttu-id="77ecc-127">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-127">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="77ecc-128">如果您正在使用 USMF，可以选择帐户 1001。</span><span class="sxs-lookup"><span data-stu-id="77ecc-128">If you’re using USMF, you can select account 1001.</span></span>  
11. <span data-ttu-id="77ecc-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-129">Click OK.</span></span>
    * <span data-ttu-id="77ecc-130">消息通知您，现在已创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="77ecc-130">The message informs you that the purchase order has now been created.</span></span>   
12. <span data-ttu-id="77ecc-131">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="77ecc-131">Expand the Line details section.</span></span>
13. <span data-ttu-id="77ecc-132">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-132">Click the Delivery tab.</span></span>
    * <span data-ttu-id="77ecc-133">“直接交货”字段现在设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-133">The Direct delivery field is now set to Yes.</span></span>  
    * <span data-ttu-id="77ecc-134">“直接交货”状态显示已创建“采购”订单。</span><span class="sxs-lookup"><span data-stu-id="77ecc-134">The Direct delivery status shows the Purchase order created.</span></span>   
14. <span data-ttu-id="77ecc-135">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-135">On the Action Pane, click General.</span></span>
15. <span data-ttu-id="77ecc-136">单击“相关订单”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-136">Click Related orders.</span></span>
16. <span data-ttu-id="77ecc-137">单击以访问“采购订单”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="77ecc-137">Click to follow the link in the Purchase order field.</span></span>
17. <span data-ttu-id="77ecc-138">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="77ecc-138">Expand the Line details section.</span></span>
18. <span data-ttu-id="77ecc-139">单击“地址”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-139">Click the Address tab.</span></span>
    * <span data-ttu-id="77ecc-140">请注意，此采购订单行上的交货地址是客户的交货地址，而不是您公司的地址。</span><span class="sxs-lookup"><span data-stu-id="77ecc-140">Note that the delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    * <span data-ttu-id="77ecc-141">如果您更改采购订单行或源销售订单行的交货地址，则相应订单行的地址将会自动更新。</span><span class="sxs-lookup"><span data-stu-id="77ecc-141">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
19. <span data-ttu-id="77ecc-142">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-142">Click the Delivery tab.</span></span>
    * <span data-ttu-id="77ecc-143">与销售订单行类似，相关采购订单行也设置为“直接交货”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-143">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    * <span data-ttu-id="77ecc-144">采购订单行的“交货日期”和“已确认的交货日期”设置为各自源销售订单行的“要求收货日期”和“已确认的收货日期”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-144">The purchase order line's Delivery  date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    * <span data-ttu-id="77ecc-145">如果您在采购订单行或销售行更新任何日期，则相应订单的日期将会自动更新。</span><span class="sxs-lookup"><span data-stu-id="77ecc-145">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    * <span data-ttu-id="77ecc-146">设置为直接交付货物给客户的采购订单通过特定关联与源销售订单关联。</span><span class="sxs-lookup"><span data-stu-id="77ecc-146">The purchase order that is set to deliver goods directly the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="77ecc-147">此关联施加一项规则，即销售订单的装箱单更新不能从销售订单本身完成，且必须使用销售订单完成。</span><span class="sxs-lookup"><span data-stu-id="77ecc-147">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="77ecc-148">但是，必须从销售订单执行客户开票。</span><span class="sxs-lookup"><span data-stu-id="77ecc-148">However, customer invoicing must be carried out from the sales order.</span></span>  
20. <span data-ttu-id="77ecc-149">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-149">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="77ecc-150">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-150">Click Confirmation.</span></span>
22. <span data-ttu-id="77ecc-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-151">Click OK.</span></span>
23. <span data-ttu-id="77ecc-152">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-152">On the Action Pane, click Receive.</span></span>
24. <span data-ttu-id="77ecc-153">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-153">Click Product receipt.</span></span>
25. <span data-ttu-id="77ecc-154">在“产品收据”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-154">In the Product receipt field, type a value.</span></span>
26. <span data-ttu-id="77ecc-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-155">Click OK.</span></span>
27. <span data-ttu-id="77ecc-156">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-156">On the Action Pane, click General.</span></span>
28. <span data-ttu-id="77ecc-157">单击“相关订单”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-157">Click Related orders.</span></span>
29. <span data-ttu-id="77ecc-158">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="77ecc-158">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="77ecc-159">在采购订单更新为已接受后，或者说是在供应商已装运货物发给您客户的地址后，源销售订单的状态将自动更新为“交货”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-159">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    * <span data-ttu-id="77ecc-160">销售订单现在可以进行开票。</span><span class="sxs-lookup"><span data-stu-id="77ecc-160">The sales order can now be invoiced.</span></span>    
30. <span data-ttu-id="77ecc-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-161">Click OK.</span></span>
31. <span data-ttu-id="77ecc-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77ecc-162">Close the page.</span></span>
32. <span data-ttu-id="77ecc-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-163">Click OK.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="77ecc-164">从工作台创建直接交货</span><span class="sxs-lookup"><span data-stu-id="77ecc-164">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="77ecc-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77ecc-165">Close the page.</span></span>
2. <span data-ttu-id="77ecc-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77ecc-166">Close the page.</span></span>
3. <span data-ttu-id="77ecc-167">转到“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-167">Go to All sales orders.</span></span>
4. <span data-ttu-id="77ecc-168">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-168">Click New.</span></span>
5. <span data-ttu-id="77ecc-169">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-169">In the Customer account field, enter or select a value.</span></span>
6. <span data-ttu-id="77ecc-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-170">Click OK.</span></span>
7. <span data-ttu-id="77ecc-171">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77ecc-171">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="77ecc-172">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="77ecc-172">Expand the Line details section.</span></span>
9. <span data-ttu-id="77ecc-173">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-173">Click the Delivery tab.</span></span>
    * <span data-ttu-id="77ecc-174">您可以选择移交此任务到采购专业人员，而不是创建直接交货作为上一过程的销售订单处理的一部分。</span><span class="sxs-lookup"><span data-stu-id="77ecc-174">Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="77ecc-175">若要将销售订单行加入直接交货处理流程，您必须标记直接交货的行。</span><span class="sxs-lookup"><span data-stu-id="77ecc-175">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
10. <span data-ttu-id="77ecc-176">在“直接交货”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-176">Select Yes in the Direct delivery field.</span></span>
    *   <span data-ttu-id="77ecc-177">如果物料已默认设置为直接交货，则字段将在订单行条目自动设为“是”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-177">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="77ecc-178">您可以通过将“直接交货”选项设置为“是”以及选择默认直接交货仓库来在已发布产品的主数据上设置供直接交货的物料。</span><span class="sxs-lookup"><span data-stu-id="77ecc-178">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    * <span data-ttu-id="77ecc-179">由于尚未创建采购订单，“直接交货状态”设置为“将直接交货”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-179">Because the purchase order has not yet been created, the Direct delivery status is set to To be direct delivered.</span></span>   
11. <span data-ttu-id="77ecc-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77ecc-180">Close the page.</span></span>
12. <span data-ttu-id="77ecc-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77ecc-181">Close the page.</span></span>
13. <span data-ttu-id="77ecc-182">转到“直接交货”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-182">Go to Direct delivery.</span></span>
    * <span data-ttu-id="77ecc-183">“直接交货”页作为提供采购代理和所有将直接交货的销售订单行的概览的工作台，其允许创建单独的采购订单。</span><span class="sxs-lookup"><span data-stu-id="77ecc-183">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="77ecc-184">此外，可以在“确认”与“交货”选项卡查看未结的直接交货订单和已确认的订单。</span><span class="sxs-lookup"><span data-stu-id="77ecc-184">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>   
14. <span data-ttu-id="77ecc-185">单击“创建直接交货”。</span><span class="sxs-lookup"><span data-stu-id="77ecc-185">Click Create direct delivery.</span></span>
15. <span data-ttu-id="77ecc-186">单击“确认”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-186">Click the Confirmation tab.</span></span>
    * <span data-ttu-id="77ecc-187">在您创建直接交货订单后，其会自动移到“确认”选项卡。您可以选择直接从此页确认订单。</span><span class="sxs-lookup"><span data-stu-id="77ecc-187">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="77ecc-188">在确认采购时，将会从可登记其收货的位置自动移到“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="77ecc-188">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  


