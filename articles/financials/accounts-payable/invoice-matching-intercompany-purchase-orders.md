---
title: "发票匹配和内部公司采购订单"
description: "涉及内部公司交易的采购法人设置为使用应付账款发票匹配。 在这种情况下，内部公司交易和应付账款发票匹配的过帐需求必须满足（在内部公司供应商过帐发票前）。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: affdffd5e73958788ed2a5a4959eea71024140ab
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a><span data-ttu-id="8156b-104">发票匹配和内部公司采购订单</span><span class="sxs-lookup"><span data-stu-id="8156b-104">Invoice matching and intercompany purchase orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8156b-105">涉及内部公司交易的采购法人设置为使用应付账款发票匹配。</span><span class="sxs-lookup"><span data-stu-id="8156b-105">The purchasing legal entity that is involved in an intercompany trade transaction might be set up to use accounts payable invoice matching.</span></span> <span data-ttu-id="8156b-106">在这种情况下，内部公司交易和应付账款发票匹配的过帐需求必须满足（在内部公司供应商过帐发票前）。</span><span class="sxs-lookup"><span data-stu-id="8156b-106">In this case, the posting requirements for both intercompany trade and accounts payable invoice matching must be met before intercompany vendor invoices can be posted.</span></span>

<span data-ttu-id="8156b-107">本主题中的示例为内部交易记录使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="8156b-107">The examples in this topic use the following setup for intercompany trade:</span></span>
-   <span data-ttu-id="8156b-108">Fabrikam Purchase 为采购法人。</span><span class="sxs-lookup"><span data-stu-id="8156b-108">Fabrikam Purchase is the purchasing legal entity.</span></span>
-   <span data-ttu-id="8156b-109">Fabrikam Sales 为销售的法人。</span><span class="sxs-lookup"><span data-stu-id="8156b-109">Fabrikam Sales is the selling legal entity.</span></span>
-   <span data-ttu-id="8156b-110">客户 4020 存在于 Fabrikam Sales 中。</span><span class="sxs-lookup"><span data-stu-id="8156b-110">Customer 4020 exists in Fabrikam Sales.</span></span>
-   <span data-ttu-id="8156b-111">供应商 3024 存在于 Fabrikam Purchase 中。</span><span class="sxs-lookup"><span data-stu-id="8156b-111">Vendor 3024 exists in Fabrikam Purchase.</span></span>
-   <span data-ttu-id="8156b-112">在 Fabrikam Purchase 中，为供应商 3024 指定了内部公司信息。</span><span class="sxs-lookup"><span data-stu-id="8156b-112">In Fabrikam Purchase, intercompany information is specified for vendor 3024.</span></span> <span data-ttu-id="8156b-113">Fabrikam Sales 指定为客户公司，并且客户 4020 指定为对应于 Fabrikam Purchase 法人的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="8156b-113">Fabrikam Sales is specified as the customer company, and customer 4020 is specified as the customer account that corresponds to the Fabrikam Purchase legal entity.</span></span>
-   <span data-ttu-id="8156b-114">在 Fabrikam Sales 中，为客户 4020 指定了内部公司信息。</span><span class="sxs-lookup"><span data-stu-id="8156b-114">In Fabrikam Sales, intercompany information is specified for customer 4020.</span></span> <span data-ttu-id="8156b-115">Fabrikam Purchase 指定为供应商公司，并且供应商 3024 指定为对应于 Fabrikam Purchase 法人的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="8156b-115">Fabrikam Purchase is specified as the vendor company, and vendor 3024 is specified as the vendor account that corresponds to the Fabrikam Sales legal entity.</span></span>

<span data-ttu-id="8156b-116">这些示例使用针对 Fabrikam Purchase 的以下应付账款发票匹配设置：</span><span class="sxs-lookup"><span data-stu-id="8156b-116">The examples use the following setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="8156b-117">当在“应付账款参数”页上，选择了“启用发票匹配验证”选项。</span><span class="sxs-lookup"><span data-stu-id="8156b-117">On the Accounts payable parameters page, the Enable invoice matching validation option is selected.</span></span>
-   <span data-ttu-id="8156b-118">在“应付账款参数”页上，“过帐具有差异的发票”选项设置为“要求审核”。</span><span class="sxs-lookup"><span data-stu-id="8156b-118">On the Accounts payable parameters page, the Post invoice with discrepancies field is set to Require approval.</span></span>
-   <span data-ttu-id="8156b-119">法人的价格容差百分比设置为 2。</span><span class="sxs-lookup"><span data-stu-id="8156b-119">The price tolerance percentage for the legal entity is 2 percent.</span></span>

## <a name="example-price-matching-and-intercompany-trade"></a><span data-ttu-id="8156b-120">示例：具有内部公司交易的价格匹配</span><span class="sxs-lookup"><span data-stu-id="8156b-120">Example: Price matching and intercompany trade</span></span>
<span data-ttu-id="8156b-121">内部公司供应商发票和内部公司客户发票的净额必须相等。</span><span class="sxs-lookup"><span data-stu-id="8156b-121">The net amounts for the intercompany vendor invoice and the intercompany customer invoice must be equal.</span></span> <span data-ttu-id="8156b-122">此要求优先于所有适用发票匹配审核或价格容差百分比。</span><span class="sxs-lookup"><span data-stu-id="8156b-122">This requirement overrides any invoice matching approvals or price tolerance percentages that apply.</span></span> <span data-ttu-id="8156b-123">例如，您可以执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8156b-123">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="8156b-124">在 Fabrikam Purchase 中，为客户 4020 创建销售订单 SO888。</span><span class="sxs-lookup"><span data-stu-id="8156b-124">In Fabrikam Purchase, create sales order SO888 for customer 4020.</span></span> <span data-ttu-id="8156b-125">内部公司采购订单 ICPO222 自动在 Fabrikam Purchase 中为供应商 3024 创建，销售订单 ICSO888 自动在 Fabrikam Sales 中创建。</span><span class="sxs-lookup"><span data-stu-id="8156b-125">Intercompany purchase order ICPO222 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO888 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="8156b-126">在 Fabrikam Sales 中，登记已接收的物料并且过帐装箱单。</span><span class="sxs-lookup"><span data-stu-id="8156b-126">In Fabrikam Sales, register that the items have been received, and post a packing slip.</span></span> <span data-ttu-id="8156b-127">ICSO888 的状态更改为“已交货”。</span><span class="sxs-lookup"><span data-stu-id="8156b-127">The status of ICSO888 changes to Delivered.</span></span> <span data-ttu-id="8156b-128">ICPO222 的状态更改为“已收货”。</span><span class="sxs-lookup"><span data-stu-id="8156b-128">The status of ICPO222 changes to Received.</span></span>
3.  <span data-ttu-id="8156b-129">在Fabrikam Sales中，为ICSO888执行发票更新。</span><span class="sxs-lookup"><span data-stu-id="8156b-129">In Fabrikam Sales, perform an invoice update for ICSO888.</span></span> <span data-ttu-id="8156b-130">单位价格是 0.45，并且更新 100 项。</span><span class="sxs-lookup"><span data-stu-id="8156b-130">The unit price is 0.45, and 100 items are updated.</span></span>
4.  <span data-ttu-id="8156b-131">在Fabrikam Purchase中为 ICPO222 创建一个发票。</span><span class="sxs-lookup"><span data-stu-id="8156b-131">In Fabrikam Purchase, create an invoice for ICPO222.</span></span> <span data-ttu-id="8156b-132">偶然将净价从 45.00 更改为 54.00。</span><span class="sxs-lookup"><span data-stu-id="8156b-132">You accidentally change the net price from 45.00 to 54.00.</span></span> <span data-ttu-id="8156b-133">显示一个图标，指示价差超出 2% 的允许价格容差。</span><span class="sxs-lookup"><span data-stu-id="8156b-133">An icon is displayed to indicate that the price exceeds the allowable price tolerance of 2 percent.</span></span>
5.  <span data-ttu-id="8156b-134">在“发票匹配详细信息”页上，选择该选项以审核具有匹配差异的过帐。</span><span class="sxs-lookup"><span data-stu-id="8156b-134">On the Invoice matching details page, select the option to approve posting with matching discrepancies.</span></span> <span data-ttu-id="8156b-135">在“供应商发票”页上，单击“确定”。如果供应商发票不是内部公司供应商发票，则过帐成功。</span><span class="sxs-lookup"><span data-stu-id="8156b-135">On the Vendor invoice page, click OK.If the vendor invoice was not an intercompany vendor invoice, posting would be successful.</span></span> <span data-ttu-id="8156b-136">但是，因此，使用您的内部公司供应商发票时，过帐未获成功。</span><span class="sxs-lookup"><span data-stu-id="8156b-136">However, because you are working with an intercompany vendor invoice, posting is unsuccessful.</span></span> <span data-ttu-id="8156b-137">对于内部交易记录，在内部公司销售订单的发票合计必须等于相应内部公司采购订单上的发票合计。</span><span class="sxs-lookup"><span data-stu-id="8156b-137">For intercompany trade, the invoice totals on the intercompany sales order must equal the invoice totals on the corresponding intercompany purchase order.</span></span> <span data-ttu-id="8156b-138">为了解决此问题，您必须通过将净价更正为发票上的净价默认金额，例如 45.00。</span><span class="sxs-lookup"><span data-stu-id="8156b-138">To resolve this issue, you must correct the net price on the invoice by changing the net price back to the default amount, 45.00.</span></span>

## <a name="example-quantity-matching-with-intercompany-trade"></a><span data-ttu-id="8156b-139">示例：具有内部公司交易的数量匹配</span><span class="sxs-lookup"><span data-stu-id="8156b-139">Example: Quantity matching with intercompany trade</span></span>
<span data-ttu-id="8156b-140">内部公司采购订单和内部公司销售订单数量必须相等。</span><span class="sxs-lookup"><span data-stu-id="8156b-140">The quantities on the intercompany purchase order and the intercompany sales order must be equal.</span></span> <span data-ttu-id="8156b-141">此要求优先于所有适用的发票匹配审核。</span><span class="sxs-lookup"><span data-stu-id="8156b-141">This requirement overrides any invoice matching approvals that apply.</span></span> <span data-ttu-id="8156b-142">此示例使用以下附加内部公司交易设置：</span><span class="sxs-lookup"><span data-stu-id="8156b-142">This example uses the following additional setup for intercompany trade:</span></span>
-   <span data-ttu-id="8156b-143">在 Fabrikam Purchase 中为供应商 3024 设置采购订单操作策略，设置为自动过帐原始客户发票和内部公司供应商发票。</span><span class="sxs-lookup"><span data-stu-id="8156b-143">In Fabrikam Purchase, the purchase order action policy for vendor 3024 is set up to automatically post both the original customer invoice and the intercompany vendor invoice.</span></span>

<span data-ttu-id="8156b-144">此示例使用针对 Fabrikam Purchase 的以下附加的应付账款发票匹配设置：</span><span class="sxs-lookup"><span data-stu-id="8156b-144">This example uses the following additional setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="8156b-145">在物料 B-R14 使用的模型组的“物料模型组”页上，选择了“接收要求”选项。</span><span class="sxs-lookup"><span data-stu-id="8156b-145">On the Item model groups page for the model group that is used by item B-R14, the Receiving requirements option is selected.</span></span>
-   <span data-ttu-id="8156b-146">物料 B-R14 的现有数量是 0（零）。</span><span class="sxs-lookup"><span data-stu-id="8156b-146">The on-hand quantity for item B-R14 is 0 (zero).</span></span>

<span data-ttu-id="8156b-147">例如，您可以执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8156b-147">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="8156b-148">在 Fabrikam Purchase 中，为客户 4020 创建销售订单 SO999。</span><span class="sxs-lookup"><span data-stu-id="8156b-148">In Fabrikam Purchase, create sales order SO999 for customer 4020.</span></span> <span data-ttu-id="8156b-149">此订单何中包含一个行项：100 节电池（物料 B-R14），单位价格为 1.00。</span><span class="sxs-lookup"><span data-stu-id="8156b-149">The order contains one line item: 100 batteries (item B-R14) at a unit price of 1.00 each.</span></span> <span data-ttu-id="8156b-150">内部公司采购订单 ICPO333 自动在 Fabrikam Purchase 中为供应商 3024 创建，销售订单 ICSO999 自动在 Fabrikam Sales 中创建。</span><span class="sxs-lookup"><span data-stu-id="8156b-150">Intercompany purchase order ICPO333 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO999 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="8156b-151">在 Fabrikam Sales 中，执行 ICSO999 的发票更新。</span><span class="sxs-lookup"><span data-stu-id="8156b-151">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="8156b-152">因为物料库存不足并且尚未收货，过帐时未获成功。</span><span class="sxs-lookup"><span data-stu-id="8156b-152">Posting is unsuccessful, because the item is out of stock and has not yet been received.</span></span> <span data-ttu-id="8156b-153">因此，不能更新财务信息。</span><span class="sxs-lookup"><span data-stu-id="8156b-153">Therefore, the financial information cannot be updated.</span></span>
3.  <span data-ttu-id="8156b-154">登记已接收的物料并且为 Fabrikam Sales 中的 ICSO999 过帐装箱单。</span><span class="sxs-lookup"><span data-stu-id="8156b-154">In Fabrikam Sales, register that the items have been received, and post a packing slip for ICSO999.</span></span> <span data-ttu-id="8156b-155">ICPO333 的产品收货在 Fabrikam Purchase 中为自动过帐。</span><span class="sxs-lookup"><span data-stu-id="8156b-155">A product receipt for ICPO333 is automatically posted in Fabrikam Purchase.</span></span> <span data-ttu-id="8156b-156">在 Fabrikam Purchase 中为物料 B-R14 接收的数量更改为 100。</span><span class="sxs-lookup"><span data-stu-id="8156b-156">In Fabrikam Purchase, the received quantity for item B-R14 changes to 100.</span></span>
4.  <span data-ttu-id="8156b-157">在 Fabrikam Sales 中，执行 ICSO999 的发票更新。</span><span class="sxs-lookup"><span data-stu-id="8156b-157">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="8156b-158">过帐在两法人中均成功。</span><span class="sxs-lookup"><span data-stu-id="8156b-158">Posting is successful in both legal entities.</span></span> <span data-ttu-id="8156b-159">在 Fabrikam Purchase 中为物料 B-R14 采购的数量更改为 100。</span><span class="sxs-lookup"><span data-stu-id="8156b-159">In Fabrikam Purchase, the quantity that is purchased for item B-R14 changes to 100.</span></span>






