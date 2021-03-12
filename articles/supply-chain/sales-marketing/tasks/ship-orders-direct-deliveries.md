---
title: 以直接交运方式装运订单
description: 本主题介绍如何为销售订单创建直接交货。
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a8f214a56c6a5013cab8233d5b2e0126deb9220
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966097"
---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="5f4d9-103">以直接交运方式装运订单</span><span class="sxs-lookup"><span data-stu-id="5f4d9-103">Ship orders as direct deliveries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f4d9-104">本主题介绍如何为销售订单创建直接交货。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-104">This topic demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="5f4d9-105">在想要从供应商处直接装运货物给客户，而不是先装运至您自身的仓库时，可使用直接交货。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="5f4d9-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="5f4d9-107">要想成功完成第二个子任务“从工作台创建直接交货”，确保您在销售订单上选择的物料有默认“供应商”，该供应商在“已发布基础产品”的“采购”快速项卡上有指定。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>

## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="5f4d9-108">设置直接交货的单个订单</span><span class="sxs-lookup"><span data-stu-id="5f4d9-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="5f4d9-109">转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-109">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="5f4d9-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-110">Select **New**.</span></span>
3. <span data-ttu-id="5f4d9-111">在 **客户帐户** 字段中输入或选择一个值，然后选择 **确定**</span><span class="sxs-lookup"><span data-stu-id="5f4d9-111">Enter or select a value in the **Customer accound** field, then select **OK**</span></span>
4. <span data-ttu-id="5f4d9-112">在 **物料编号** 和 **站点** 字段中输入或选择值，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-112">Enter or select values in the **Item number** and **Site** fields, then select **Save**.</span></span>
5. <span data-ttu-id="5f4d9-113">在操作窗格上，选择 **销售订单**，然后选择 **直接交运**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-113">On the Action Pane, select **Sales order**, then select **Direct delivery**.</span></span> <span data-ttu-id="5f4d9-114">“创建交货”页面列出所有从销售订单复制的未结销售订单行。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-114">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="5f4d9-115">您可以查看订单的详细信息，并可根据需要修改详细信息，例如创建直接交货前的采购数量和价格条款。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-115">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
6. <span data-ttu-id="5f4d9-116">在 **全部包括** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-116">Select **Yes** in the **Include all** field.</span></span>
    - <span data-ttu-id="5f4d9-117">如果您想要生成仅销售订单行的一个子集的直接交货，则单独选择这些。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-117">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    - <span data-ttu-id="5f4d9-118">**供应商帐户** 字段可能填充也可能不填充供应商编号。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-118">The **Vendor account** field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="5f4d9-119">如果已为产品设置默认供应商（在相关物料范围），则此供应商将会复制到该行。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-119">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="5f4d9-120">否则，您必须手动输入供应商。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-120">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="5f4d9-121">在此示例中，我们将在下一步选择新供应商（即使已填充一个供应商）。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-121">In this example, we'll select a new vendor in the next step, even if one is already populated.</span></span>   
7. <span data-ttu-id="5f4d9-122">在 **供应商帐户** 字段中输入或选择一个值，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-122">Enter or select a value in the **Vendor account** field, then select **OK**.</span></span> <span data-ttu-id="5f4d9-123">消息通知您，现在已创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-123">The message informs you that the purchase order has now been created.</span></span>   
8. <span data-ttu-id="5f4d9-124">展开 **行详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-124">Expand the **Line details** section.</span></span>
9. <span data-ttu-id="5f4d9-125">选择 **交运** 选项卡，然后验证 **直接交运** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-125">Select the **Delivery** tab and verify that the **Direct delivery** field is set to **Yes**.</span></span>
10. <span data-ttu-id="5f4d9-126">在操作窗格上，选择 **常规**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-126">On the Action Pane, select **General**.</span></span>
11. <span data-ttu-id="5f4d9-127">选择 **相关订单**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-127">Select **Related orders**.</span></span>
12. <span data-ttu-id="5f4d9-128">在 **采购订单** 字段中选择链接。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-128">Select the link in the **Purchase order** field.</span></span>
13. <span data-ttu-id="5f4d9-129">展开 **行详细信息** 部分，然后选择 **地址** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-129">Expand the **Line details** section and select the **Address** tab.</span></span>
    - <span data-ttu-id="5f4d9-130">此采购订单行上的交货地址是客户的交货地址，而不是您公司的地址。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-130">The delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    - <span data-ttu-id="5f4d9-131">如果您更改采购订单行或源销售订单行的交货地址，则相应订单行的地址将会自动更新。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-131">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
14. <span data-ttu-id="5f4d9-132">选择 **交付** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-132">Select the **Delivery** tab.</span></span>
    - <span data-ttu-id="5f4d9-133">与销售订单行类似，相关采购订单行也设置为“直接交货”。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-133">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    - <span data-ttu-id="5f4d9-134">采购订单行的“交货日期”和“已确认的交货日期”设置为各自源销售订单行的“要求收货日期”和“已确认的收货日期”。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-134">The purchase order line's Delivery date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    - <span data-ttu-id="5f4d9-135">如果您在采购订单行或销售行更新任何日期，则相应订单的日期将会自动更新。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-135">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    - <span data-ttu-id="5f4d9-136">设置为直接交付货物给客户的采购订单通过特定关联与源销售订单关联。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-136">The purchase order that is set to deliver goods directly to the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="5f4d9-137">此关联施加一项规则，即销售订单的装箱单更新不能从销售订单本身完成，且必须使用销售订单完成。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-137">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="5f4d9-138">但是，必须从销售订单执行客户开票。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-138">However, customer invoicing must be carried out from the sales order.</span></span>  
15. <span data-ttu-id="5f4d9-139">在操作窗格上，选择 **采购**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-139">On the Action Pane, select **Purchase**.</span></span>
16. <span data-ttu-id="5f4d9-140">选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-140">Select **Confirmation**.</span></span>
17. <span data-ttu-id="5f4d9-141">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-141">Select **OK**.</span></span>
18. <span data-ttu-id="5f4d9-142">在操作窗格上，选择 **接收**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-142">On the Action Pane, select **Receive**.</span></span>
19. <span data-ttu-id="5f4d9-143">选择 **物料收货**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-143">Select **Product receipt**.</span></span>
20. <span data-ttu-id="5f4d9-144">在 **产品收据** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-144">In the **Product receipt** field, type a value.</span></span>
21. <span data-ttu-id="5f4d9-145">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-145">Select **OK**.</span></span>
22. <span data-ttu-id="5f4d9-146">在操作窗格上，选择 **常规**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-146">On the Action Pane, select **General**.</span></span>
23. <span data-ttu-id="5f4d9-147">选择 **相关订单**，然后突出显示所需记录。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-147">Select **Related orders** and highlight the desired record.</span></span>
    - <span data-ttu-id="5f4d9-148">在采购订单更新为已接受后，或者说是在供应商已装运货物发给您客户的地址后，源销售订单的状态将自动更新为“交货”。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-148">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    - <span data-ttu-id="5f4d9-149">销售订单现在可以进行开票。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-149">The sales order can now be invoiced.</span></span>    
24. <span data-ttu-id="5f4d9-150">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-150">Select **OK**.</span></span>
25. <span data-ttu-id="5f4d9-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-151">Close the page.</span></span>
26. <span data-ttu-id="5f4d9-152">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-152">Select **OK**.</span></span> <span data-ttu-id="5f4d9-153">关闭页面并返回到主页。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-153">Close the pages and return to the home page.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="5f4d9-154">从工作台创建直接交货</span><span class="sxs-lookup"><span data-stu-id="5f4d9-154">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="5f4d9-155">转到 **导航 > 模块 > 应收帐款 > 订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-155">Go to **Navigation > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="5f4d9-156">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-156">Select **New**.</span></span>
3. <span data-ttu-id="5f4d9-157">在 **客户帐户** 字段中输入或选择一个值，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-157">Enter or select a value in the **Customer account** field, then select **OK**.</span></span>
4. <span data-ttu-id="5f4d9-158">在 **物料编号** 和 **站点** 字段中输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-158">Enter or select a value in the **Item number** and **site** fields.</span></span>
5. <span data-ttu-id="5f4d9-159">展开 **行详细信息** 部分，然后选择 **交付** 选项卡。您可以选择移交此任务到采购专业人员，而不是创建直接交货作为上一过程的销售订单处理的一部分。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-159">Expand the **Line details** section, then select the **Delivery** tab. Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="5f4d9-160">若要将销售订单行加入直接交货处理流程，您必须标记直接交货的行。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-160">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
6. <span data-ttu-id="5f4d9-161">在 **直接交货** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-161">Select **Yes** in the **Direct delivery** field.</span></span>
    - <span data-ttu-id="5f4d9-162">如果物料已默认设置为直接交货，则字段将在订单行条目自动设为“是”。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-162">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="5f4d9-163">您可以通过将“直接交货”选项设置为“是”以及选择默认直接交货仓库来在已发布产品的主数据上设置供直接交货的物料。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-163">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    - <span data-ttu-id="5f4d9-164">由于尚未创建采购订单，“直接交货状态”设置为“将直接交货”。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-164">Because the purchase order has not yet been created, the Direct delivery status is set to "To be direct delivered".</span></span>   
7. <span data-ttu-id="5f4d9-165">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-165">Select **Save**.</span></span>
8. <span data-ttu-id="5f4d9-166">关闭页面，直到返回到主页。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-166">Close pages until you return to the home page.</span></span>
9. <span data-ttu-id="5f4d9-167">在搜索栏中输入 `Direct delivery`。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-167">Enter `Direct delivery` in the search bar.</span></span>
    - <span data-ttu-id="5f4d9-168">“直接交货”页作为提供采购代理和所有将直接交货的销售订单行的概览的工作台，其允许创建单独的采购订单。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-168">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="5f4d9-169">此外，可以在“确认”与“交货”选项卡查看未结的直接交货订单和已确认的订单。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-169">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>  
    - <span data-ttu-id="5f4d9-170">在您创建直接交货订单后，其会自动移到“确认”选项卡。您可以选择直接从此页确认订单。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-170">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="5f4d9-171">在确认采购时，将会从可登记其收货的位置自动移到“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="5f4d9-171">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  

