---
title: 直接交货
description: 本文提供有关直接交运的信息。 直接交运是直接从供应商发送到您的客户的交货。
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa5349de635bbad8f32c24b82e297784600463ea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209965"
---
# <a name="direct-deliveries"></a><span data-ttu-id="e1e34-104">直接交货</span><span class="sxs-lookup"><span data-stu-id="e1e34-104">Direct deliveries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1e34-105">本文提供有关直接交运的信息。</span><span class="sxs-lookup"><span data-stu-id="e1e34-105">This article provides information about direct deliveries.</span></span> <span data-ttu-id="e1e34-106">直接交运是直接从供应商发送到您的客户的交货。</span><span class="sxs-lookup"><span data-stu-id="e1e34-106">Direct deliveries are deliveries that are sent directly from the vendor to your customer.</span></span>

<span data-ttu-id="e1e34-107">直接交运节省交货时间并减少与存储库存关联的成本，因为您直接向客户发运，无需在您的仓库中存储产品。</span><span class="sxs-lookup"><span data-stu-id="e1e34-107">Direct deliveries save delivery time and reduce the costs that are associated with carrying inventory, because you don't hold the products in your warehouse before you ship them to the customer.</span></span>  

<span data-ttu-id="e1e34-108">您可以从**销售订单**页创建直接交运。</span><span class="sxs-lookup"><span data-stu-id="e1e34-108">You can create direct deliveries from the **Sales order** page.</span></span> <span data-ttu-id="e1e34-109">首先，创建销售订单和订单行。</span><span class="sxs-lookup"><span data-stu-id="e1e34-109">First, create a sales order and order lines.</span></span> <span data-ttu-id="e1e34-110">然后在操作窗格上，在**销售订单**选项卡，选择**直接交运**。</span><span class="sxs-lookup"><span data-stu-id="e1e34-110">Then, on the Action Pane, on the **Sales order** tab, select **Direct delivery**.</span></span> <span data-ttu-id="e1e34-111">最后，指定必须处理为直接交运的行。</span><span class="sxs-lookup"><span data-stu-id="e1e34-111">Finally, specify the lines that must be handled as a direct delivery.</span></span> <span data-ttu-id="e1e34-112">现在即在直接交运销售订单行及其相应的采购订单行之间创建了一个链接。</span><span class="sxs-lookup"><span data-stu-id="e1e34-112">A link is now created between the sales order lines for the direct delivery and the corresponding purchase order lines.</span></span>  

<span data-ttu-id="e1e34-113">**注意：** 如果订购数量的一部分已交货，则必须拆分剩余数量。</span><span class="sxs-lookup"><span data-stu-id="e1e34-113">**Note:** If part of the ordered quantity has already been delivered, you must split the remaining quantity.</span></span> <span data-ttu-id="e1e34-114">创建必须直接交运的数量新行，从原始行的数量中减去此数量。</span><span class="sxs-lookup"><span data-stu-id="e1e34-114">Create a new line for the quantity that must be directly delivered, and subtract that quantity from the quantity on the original line.</span></span> <span data-ttu-id="e1e34-115">例如，如果原始数量为 15，而发货的数量为 5，则必须为剩余数量 10 创建新行，然后根据此数额减少原始数量。</span><span class="sxs-lookup"><span data-stu-id="e1e34-115">For example, if the original quantity was 15, and five have been delivered, you must create a new line for the remaining quantity, 10, and then reduce the original quantity by that amount.</span></span>  

<span data-ttu-id="e1e34-116">在您在销售订单行和采购订单行之间创建直接交运链接后，可以通过使用装箱单更新销售订单。</span><span class="sxs-lookup"><span data-stu-id="e1e34-116">After you create the direct delivery link between the sales order lines and the purchase order lines, you can update the sales order by using a packing slip.</span></span> <span data-ttu-id="e1e34-117">从采购订单运行装箱单更新或发票更新。</span><span class="sxs-lookup"><span data-stu-id="e1e34-117">Run either a packing slip update or an invoice update from the purchase order.</span></span> <span data-ttu-id="e1e34-118">您必须从**销售订单**页更新销售订单发票。</span><span class="sxs-lookup"><span data-stu-id="e1e34-118">You must invoice-update the sales order from the **Sales order** page.</span></span> <span data-ttu-id="e1e34-119">更新发票不会造成销售订单的数量超过登记为已接收的数量。</span><span class="sxs-lookup"><span data-stu-id="e1e34-119">An invoice update can't cause the quantity on the sales order to exceed the quantity that has been registered as received.</span></span> <span data-ttu-id="e1e34-120">例如，销售订单行都有 10 件，不过通过装箱单只从销售订单行更新 5 件。</span><span class="sxs-lookup"><span data-stu-id="e1e34-120">For example, a sales order line has 10 pieces, but only five pieces from the sales order line have been updated by using a packing slip.</span></span> <span data-ttu-id="e1e34-121">如果选择**列表**中的**全部**，当您对销售订单进行发票更新时，使用装箱单，因此，只有已实际接收的物料更新发票。</span><span class="sxs-lookup"><span data-stu-id="e1e34-121">If you select **All** in the **Quantity** list when you invoice-update the sales order, only those items that have been physically received, or updated by using a packing slip, are invoice-updated.</span></span> <span data-ttu-id="e1e34-122">不会更新整个销售订单行。</span><span class="sxs-lookup"><span data-stu-id="e1e34-122">The whole sales order line isn't updated.</span></span>

## <a name="delivery-date"></a><span data-ttu-id="e1e34-123">交货日期</span><span class="sxs-lookup"><span data-stu-id="e1e34-123">Delivery date</span></span>
<span data-ttu-id="e1e34-124">在您更新销售订单行上的**要求接收日期**字段时，也更新相应采购订单行上的**交货日期**字段。</span><span class="sxs-lookup"><span data-stu-id="e1e34-124">When you update the **Requested receipt date** field on the sales order line, the **Delivery date** field on the corresponding purchase order line is also updated.</span></span> <span data-ttu-id="e1e34-125">相似地，在您更新采购订单行上的**已确认**字段时，也更新相应销售订单行上的**已确认的接收日期**和**已确认的装运日期**字段。</span><span class="sxs-lookup"><span data-stu-id="e1e34-125">Similarly, when you update the **Confirmed** field on the purchase order line, the **Confirmed receipt date** and **Confirmed ship date** fields on the corresponding sales order line are also updated.</span></span>

## <a name="delivery-address"></a><span data-ttu-id="e1e34-126">交货地址</span><span class="sxs-lookup"><span data-stu-id="e1e34-126">Delivery address</span></span>
<span data-ttu-id="e1e34-127">通常情况下，采购订单的交货地址是公司的地址。</span><span class="sxs-lookup"><span data-stu-id="e1e34-127">Typically, the delivery address for a purchase order is the company's address.</span></span> <span data-ttu-id="e1e34-128">但是，在您创建直接交运时，输入客户的地址将作为交货地址。</span><span class="sxs-lookup"><span data-stu-id="e1e34-128">However, when you create a direct delivery, you enter the customer's address as the delivery address.</span></span> <span data-ttu-id="e1e34-129">如果您为**直接交运**交货类型的采购订单行更改交货地址，则也更新相应销售订单行的交货地址。</span><span class="sxs-lookup"><span data-stu-id="e1e34-129">If you change the delivery address on a purchase order line that has a delivery type of **Direct delivery**, the delivery address on the corresponding sales order line is also updated.</span></span> <span data-ttu-id="e1e34-130">与此相似，如果您更改销售订单行上的交货地址，则也会更新采购订单行上的交货地址。</span><span class="sxs-lookup"><span data-stu-id="e1e34-130">Similarly, if you change the delivery address on the sales order line, the delivery address on the purchase order line is also updated.</span></span>

## <a name="deleting-order-lines"></a><span data-ttu-id="e1e34-131">删除订单行</span><span class="sxs-lookup"><span data-stu-id="e1e34-131">Deleting order lines</span></span>
<span data-ttu-id="e1e34-132">如果您尝试删除交货类型为**直接交运**的某一销售订单行，消息框指出多个采购订单行已附加到该行。</span><span class="sxs-lookup"><span data-stu-id="e1e34-132">If you try to delete a sales order line that has a delivery type of **Direct delivery**, a message box states that purchase order lines are attached to the line.</span></span> <span data-ttu-id="e1e34-133">如果该销售订单行已部分交货，则您不能删除该销售订单行或其附加的采购订单行。</span><span class="sxs-lookup"><span data-stu-id="e1e34-133">If the sales order line has been partially delivered, you can't delete the sales order line or the purchase order lines that are attached to it.</span></span>

## <a name="warehouse"></a><span data-ttu-id="e1e34-134">仓库</span><span class="sxs-lookup"><span data-stu-id="e1e34-134">Warehouse</span></span>
<span data-ttu-id="e1e34-135">在您创建直接交运时，销售的物料永远不会实际到达您的仓库。</span><span class="sxs-lookup"><span data-stu-id="e1e34-135">When you create a direct delivery, the items that you sell never physically arrive at your warehouse.</span></span> <span data-ttu-id="e1e34-136">不过，您仍必须在销售订单行指定仓库。</span><span class="sxs-lookup"><span data-stu-id="e1e34-136">However, you must still specify a warehouse on the sales order line.</span></span> <span data-ttu-id="e1e34-137">相似地，领料要求可能在物料的物料模型组中指定。</span><span class="sxs-lookup"><span data-stu-id="e1e34-137">Similarly, picking requirements might be specified on the item model group for the item.</span></span> <span data-ttu-id="e1e34-138">但是，由于物料永远不会实际到达您的仓库，在销售订单为直接交运时，会忽略这些需求。</span><span class="sxs-lookup"><span data-stu-id="e1e34-138">However, because the items never physically arrive at your warehouse, these requirements are ignored when the sales order is a direct delivery.</span></span>



