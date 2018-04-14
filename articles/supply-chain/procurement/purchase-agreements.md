---
title: "采购协议"
description: "文本提供有关采购协议的信息。 采购协议是提交到某一组织，随时间推移通过使用多个采购订单购买指定的数量或金额的合同。 以此承诺作为交换，买方接收特价和折扣。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8fb72864be4dd3199e5be8384655b5fcb0fc6e2b
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-agreements"></a><span data-ttu-id="d41df-105">采购协议</span><span class="sxs-lookup"><span data-stu-id="d41df-105">Purchase agreements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d41df-106">文本提供有关采购协议的信息。</span><span class="sxs-lookup"><span data-stu-id="d41df-106">This article provides information about purchase agreements.</span></span> <span data-ttu-id="d41df-107">采购协议是提交到某一组织，随时间推移通过使用多个采购订单购买指定的数量或金额的合同。</span><span class="sxs-lookup"><span data-stu-id="d41df-107">A purchase agreement is a contract that commits an organization to buy a specified quantity or amount by using multiple purchase orders over time.</span></span> <span data-ttu-id="d41df-108">以此承诺作为交换，买方接收特价和折扣。</span><span class="sxs-lookup"><span data-stu-id="d41df-108">In exchange for this commitment, the buyer receives special prices and discounts.</span></span> 

<span data-ttu-id="d41df-109">采购协议可应用于采购类别中的产品的特定数量、产品的特定币种金额或该产品的特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-109">Purchase agreements can apply to a specific quantity of a product, a specific currency amount of a product, or a specific currency amount of the products in a procurement category.</span></span> <span data-ttu-id="d41df-110">采购协议的价格和折扣覆盖存在的所有贸易协议中指定的价格和折扣。</span><span class="sxs-lookup"><span data-stu-id="d41df-110">The prices and discounts of the purchase agreement override the prices and discounts that are specified in any trade agreements that exist.</span></span>  

<span data-ttu-id="d41df-111">在**“采购协议”**页上，您可以创建、应用和跟进您的组织及供应商之间存在的采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-111">On the **Purchase agreements** page, you can create, apply, and follow up on purchase agreements that exist between your organization and your vendors.</span></span> <span data-ttu-id="d41df-112">例如，在创建采购协议后，您可以直接从中进行订购。</span><span class="sxs-lookup"><span data-stu-id="d41df-112">For example, after you create a purchase agreement, you can order directly from it.</span></span> <span data-ttu-id="d41df-113">每个采购协议都具有由创建采购协议的人员定义的有效期间。</span><span class="sxs-lookup"><span data-stu-id="d41df-113">Each purchase agreement has a validity period that is defined by the person who creates the purchase agreement.</span></span> <span data-ttu-id="d41df-114">采购的交货日期必须处于此有效期间的生效日期。</span><span class="sxs-lookup"><span data-stu-id="d41df-114">The delivery date of a purchase must be within the effective dates of this validity period.</span></span>  

<span data-ttu-id="d41df-115">在您创建某一采购协议后，必须激活它，然后它才会生效。</span><span class="sxs-lookup"><span data-stu-id="d41df-115">After you create a purchase agreement, you must activate it before it becomes effective.</span></span> <span data-ttu-id="d41df-116">若要激活采购协议，请将**“将协议标记为有效”**选项设置为**“是”**。</span><span class="sxs-lookup"><span data-stu-id="d41df-116">To activate a purchase agreement, set the **Mark agreement as effective** option to **Yes**.</span></span>

## <a name="commitment-types"></a><span data-ttu-id="d41df-117">承诺类型</span><span class="sxs-lookup"><span data-stu-id="d41df-117">Commitment types</span></span>
<span data-ttu-id="d41df-118">采购协议的每一行都是采购的承诺。</span><span class="sxs-lookup"><span data-stu-id="d41df-118">Each line in a purchase agreement is a commitment to buy something.</span></span> <span data-ttu-id="d41df-119">您可以使用来自多个采购订单行 (PO) 履行承诺。</span><span class="sxs-lookup"><span data-stu-id="d41df-119">You can use lines from multiple purchase orders (POs) to fulfill the commitment.</span></span> <span data-ttu-id="d41df-120">有以下四种承诺类型：</span><span class="sxs-lookup"><span data-stu-id="d41df-120">There are four types of commitments:</span></span>

-   <span data-ttu-id="d41df-121">**产品数量承诺** – 您购买产品的特定数量。</span><span class="sxs-lookup"><span data-stu-id="d41df-121">**Product quantity commitment** – You purchase a specific quantity of a product.</span></span>
-   <span data-ttu-id="d41df-122">**产品价值承诺** – 您购买产品的特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-122">**Product value commitment** – You purchase a specific currency amount of a product.</span></span>
-   <span data-ttu-id="d41df-123">**产品类别价值承诺** – 您在采购类别中购买某一特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-123">**Product category value commitment** – You purchase a specific currency amount in a procurement category.</span></span> <span data-ttu-id="d41df-124">可为目录物料或非目录物料的金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-124">The amount can be for a catalog item or a non-catalog item.</span></span>
-   <span data-ttu-id="d41df-125">**价值承诺** – 您在任何采购类别中购买任何产品（一个或多个）的特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-125">**Value commitment** – You purchase a specific currency amount of any product or products in any procurement category.</span></span>

## <a name="pricing-terms-for-purchase-agreements"></a><span data-ttu-id="d41df-126">采购协议的价格条款</span><span class="sxs-lookup"><span data-stu-id="d41df-126">Pricing terms for purchase agreements</span></span>
<span data-ttu-id="d41df-127">价格条款可以根据承诺类型的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="d41df-127">Pricing terms can vary, depending on the type of commitment.</span></span> <span data-ttu-id="d41df-128">采购协议中的价格条款覆盖设置为贸易协议的任何其他价格条款。</span><span class="sxs-lookup"><span data-stu-id="d41df-128">The pricing terms from purchase agreements override any other pricing terms that are set up for trade agreements.</span></span> <span data-ttu-id="d41df-129">下表描述受每个承诺类型影响的价格相关的字段。</span><span class="sxs-lookup"><span data-stu-id="d41df-129">The following table describes the price-related fields that are affected by each commitment type.</span></span> <span data-ttu-id="d41df-130">包含 **是** 的字段可在订单行更新。</span><span class="sxs-lookup"><span data-stu-id="d41df-130">Fields that contain **Yes** can be updated on an order line.</span></span>

| <span data-ttu-id="d41df-131">承诺类型</span><span class="sxs-lookup"><span data-stu-id="d41df-131">Commitment type</span></span>                   | <span data-ttu-id="d41df-132">单位价格</span><span class="sxs-lookup"><span data-stu-id="d41df-132">Unit price</span></span> | <span data-ttu-id="d41df-133">计价单位</span><span class="sxs-lookup"><span data-stu-id="d41df-133">Price unit</span></span> | <span data-ttu-id="d41df-134">折扣率</span><span class="sxs-lookup"><span data-stu-id="d41df-134">Discount percent</span></span> | <span data-ttu-id="d41df-135">现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="d41df-135">Cash discount amount</span></span> |
|-----------------------------------|------------|------------|------------------|----------------------|
| <span data-ttu-id="d41df-136">产品数量承诺</span><span class="sxs-lookup"><span data-stu-id="d41df-136">Product quantity commitment</span></span>       | <span data-ttu-id="d41df-137">是</span><span class="sxs-lookup"><span data-stu-id="d41df-137">Yes</span></span>        | <span data-ttu-id="d41df-138">是</span><span class="sxs-lookup"><span data-stu-id="d41df-138">Yes</span></span>        | <span data-ttu-id="d41df-139">是</span><span class="sxs-lookup"><span data-stu-id="d41df-139">Yes</span></span>              | <span data-ttu-id="d41df-140">是</span><span class="sxs-lookup"><span data-stu-id="d41df-140">Yes</span></span>                  |
| <span data-ttu-id="d41df-141">产品价值承诺</span><span class="sxs-lookup"><span data-stu-id="d41df-141">Product value commitment</span></span>          |            |            | <span data-ttu-id="d41df-142">是</span><span class="sxs-lookup"><span data-stu-id="d41df-142">Yes</span></span>              |                      |
| <span data-ttu-id="d41df-143">产品类别价值承诺</span><span class="sxs-lookup"><span data-stu-id="d41df-143">Product category value commitment</span></span> |            |            | <span data-ttu-id="d41df-144">是</span><span class="sxs-lookup"><span data-stu-id="d41df-144">Yes</span></span>              |                      |
| <span data-ttu-id="d41df-145">价值承诺</span><span class="sxs-lookup"><span data-stu-id="d41df-145">Value commitment</span></span>                  |            |            | <span data-ttu-id="d41df-146">是</span><span class="sxs-lookup"><span data-stu-id="d41df-146">Yes</span></span>              |                      |

## <a name="policies-for-purchase-agreements"></a><span data-ttu-id="d41df-147">采购协议策略</span><span class="sxs-lookup"><span data-stu-id="d41df-147">Policies for purchase agreements</span></span>
<span data-ttu-id="d41df-148">以下策略影响采购协议承诺和相应采购订单行工作之间的链接的方法：</span><span class="sxs-lookup"><span data-stu-id="d41df-148">The following policies affect the way that the link between a purchase agreement commitment and the corresponding PO lines works:</span></span>

-   <span data-ttu-id="d41df-149">**强制为最大** – 所有订单行的总数量或金额不能超过在相关的承诺中指定的数量或金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-149">**Max is enforced** – The total quantity or amount for all order lines can't exceed the quantity or amount that is specified on the related commitment.</span></span>
-   <span data-ttu-id="d41df-150">**价格和折扣是固定的** – 订单行上的价格和相关承诺上的价格必须相同。</span><span class="sxs-lookup"><span data-stu-id="d41df-150">**Price and discount is fixed** – The price on an order line and the price on the related commitment must be the same.</span></span> <span data-ttu-id="d41df-151">如果更改订单行上价格，违反该承诺的链接。</span><span class="sxs-lookup"><span data-stu-id="d41df-151">If the price is changed on the order line, the link to the commitment is broken.</span></span> <span data-ttu-id="d41df-152">如果违反了该链接，该订单行不有助于承诺的履行。</span><span class="sxs-lookup"><span data-stu-id="d41df-152">If the link is broken, the order line doesn't contribute to the fulfillment of the commitment.</span></span>
-   <span data-ttu-id="d41df-153">**最小发放金额和最大发放金额** – 如果指定了金额，则如果更改导致订单行与相关承诺不同的订单行，您会收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="d41df-153">**Minimum release amount and Maximum release amount** – If an amount is specified, you receive a message if you make any change to an order line that causes the order line to differ from the related commitment.</span></span>

## <a name="fulfillment-calculations-for-purchase-agreements"></a><span data-ttu-id="d41df-154">采购协议的履行计算</span><span class="sxs-lookup"><span data-stu-id="d41df-154">Fulfillment calculations for purchase agreements</span></span>
<span data-ttu-id="d41df-155">履行数量和金额显示在**“采购协议”**页的**“行明细”**快速选项卡上的**“履行”**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="d41df-155">Fulfillment quantities and amounts are shown on the **Fulfillment** tab on the **Line details** FastTab of the **Purchase agreements** page.</span></span>  

<span data-ttu-id="d41df-156">**“履行”**区域显示要求履行承诺的剩余金额或数量。</span><span class="sxs-lookup"><span data-stu-id="d41df-156">The **Fulfillment** area shows the remaining amount or quantity that is required to fulfill the commitment.</span></span>  

<span data-ttu-id="d41df-157">**“协议”**区域显示销售协议行有效的总数量或总金额。</span><span class="sxs-lookup"><span data-stu-id="d41df-157">The **Agreement** area shows the total quantity or the total amount that the sales agreement line is valid for.</span></span>  

<span data-ttu-id="d41df-158">您可以通过选择采购订单行和发票行上或采购协议的标题上的**“相关信息”**操作，来访问对履行计算有贡献的采购订单行和发票行。</span><span class="sxs-lookup"><span data-stu-id="d41df-158">You can access the PO lines and the invoice lines that contribute to the fulfillment calculation by selecting the **Related information** action on the lines or on the header of a purchase agreement.</span></span>

## <a name="confirmations-and-version-history-for-purchase-agreements"></a><span data-ttu-id="d41df-159">采购协议的确认和版本历史记录</span><span class="sxs-lookup"><span data-stu-id="d41df-159">Confirmations and version history for purchase agreements</span></span>
<span data-ttu-id="d41df-160">在确认某一采购协议时，将采购协议的当前版本存储在历史记录表中。</span><span class="sxs-lookup"><span data-stu-id="d41df-160">When you confirm a purchase agreement, the current version of the purchase agreement is stored in a history table.</span></span> <span data-ttu-id="d41df-161">如果您更改该采购协议，您可以在历史记录中再次确认，以存储采购协议的其他版本。</span><span class="sxs-lookup"><span data-stu-id="d41df-161">If you change the purchase agreement, you can confirm it again to store another version of the purchase agreement in the history.</span></span> <span data-ttu-id="d41df-162">如果未确认某一采购协议，您还可以将其用于创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="d41df-162">If you don't confirm a purchase agreement, you can still use it to create POs.</span></span> <span data-ttu-id="d41df-163">但是，不存储采购协议的历史记录信息。</span><span class="sxs-lookup"><span data-stu-id="d41df-163">However, the history information for the purchase agreement isn't stored.</span></span> <span data-ttu-id="d41df-164">您可以预览或打印协议的所有版本。</span><span class="sxs-lookup"><span data-stu-id="d41df-164">You can preview or print all versions of the agreement.</span></span> <span data-ttu-id="d41df-165">然后可以与您的供应商共享该修订供审核。</span><span class="sxs-lookup"><span data-stu-id="d41df-165">You can then share the revisions with your vendor to obtain approval.</span></span>

## <a name="applying-purchase-agreements-in-the-ordering-process"></a><span data-ttu-id="d41df-166">将采购协议应用于订购过程</span><span class="sxs-lookup"><span data-stu-id="d41df-166">Applying purchase agreements in the ordering process</span></span>
<span data-ttu-id="d41df-167">在创建采购订单时，可以对它应用采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-167">When you create a PO, you can apply a purchase agreement to it.</span></span> <span data-ttu-id="d41df-168">协议条款中的信息，例如付款期限、交货期限和交货地址，随后会复制到采购订单的标题中。</span><span class="sxs-lookup"><span data-stu-id="d41df-168">Information from the terms for the agreement, such as the payment terms, delivery terms, and delivery address, is then copied to the header of the PO.</span></span> <span data-ttu-id="d41df-169">如果采购订单包含协议所涉及的一个或多个产品或类别行，则采购协议中的价格和折扣用于这些行。</span><span class="sxs-lookup"><span data-stu-id="d41df-169">If the PO contains one or more lines for products or categories that are covered by the agreement, the prices and discounts from the purchase agreement are used for those lines.</span></span> <span data-ttu-id="d41df-170">订单行上的金额或数量对履行采购协议中的承诺有贡献。</span><span class="sxs-lookup"><span data-stu-id="d41df-170">The amount or quantity on the order line contributes to the fulfillment of the commitment in the purchase agreement.</span></span> <span data-ttu-id="d41df-171">同一个采购订单可以包括不与采购协议和具有采购协议承诺的行的两行。</span><span class="sxs-lookup"><span data-stu-id="d41df-171">The same PO can include both lines that aren't related to a purchase agreement and lines that have a commitment for a purchase agreement.</span></span>  

<span data-ttu-id="d41df-172">只有当您创建采购订单时，才可以选择采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-172">You can select a purchase agreement only when you're creating a PO.</span></span> <span data-ttu-id="d41df-173">在已创建采购订单后，您不能选择采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-173">You can't select a purchase agreement after the PO has been created.</span></span>  
<span data-ttu-id="d41df-174">在某些情况下间接创建采购订单，您可以控制 Finance and Operations 是否自动搜索适用的采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-174">In some situations where POs are created indirectly, you can control whether Finance and Operations automatically searches for applicable purchase agreements.</span></span> <span data-ttu-id="d41df-175">例如，在您自动确定计划的采购订单或基于销售订单创建的采购订单时，您可以执行这些操作。</span><span class="sxs-lookup"><span data-stu-id="d41df-175">For example, you might do this when you're automatically firming planned POs or creating POs that are based on sales orders.</span></span>

## <a name="purchase-agreements-and-intercompany-trade"></a><span data-ttu-id="d41df-176">采购协议和内部公司交易</span><span class="sxs-lookup"><span data-stu-id="d41df-176">Purchase agreements and intercompany trade</span></span>
<span data-ttu-id="d41df-177">内部公司贸易关系可以在不同的法人中的供应商帐户和客户帐户之间创建。</span><span class="sxs-lookup"><span data-stu-id="d41df-177">Intercompany trading relationships can be created between vendor accounts and customer accounts that are in different legal entities.</span></span> <span data-ttu-id="d41df-178">在为其中一个当事方创建销售订单或采购订单时，创建内部公司订单链。</span><span class="sxs-lookup"><span data-stu-id="d41df-178">When a sales order or PO is created for one of the parties, an intercompany order chain is created.</span></span> <span data-ttu-id="d41df-179">在订单链中，在相应法人中创建销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="d41df-179">In the order chain, the sales order and PO are created in the appropriate legal entities.</span></span>  

<span data-ttu-id="d41df-180">您可以为内部公司贸易当事方之一创建采购协议或销售协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-180">You can create a purchase agreement or sales agreement for one of the intercompany trading parties.</span></span> <span data-ttu-id="d41df-181">然后，您可以为其他法人中的其他内部公司贸易当事方生成相应的销售协议或采购协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-181">You can then generate the corresponding sales agreement or purchase agreement for the other intercompany trading party in the other legal entity.</span></span>  

<span data-ttu-id="d41df-182">如果您一个法人中创建使用内部公司采购协议的内部公司采购订单，则其他法人中的相应的内部公司采购订单使用相应的内部公司销售协议。</span><span class="sxs-lookup"><span data-stu-id="d41df-182">If you create an intercompany PO that uses the intercompany purchase agreement in one legal entity, the corresponding intercompany sales order uses the corresponding intercompany sales agreement in the other legal entity.</span></span> <span data-ttu-id="d41df-183">同步销售协议承诺的履行和采购协议的履行，就如同同步内部公司销售订单和内部公司采购订单。</span><span class="sxs-lookup"><span data-stu-id="d41df-183">The fulfillment of the sales agreement commitments and the fulfillment of the purchase agreements are synchronized, just as the intercompany sales order and the intercompany PO are synchronized.</span></span>

## <a name="financial-dimensions-on-purchase-agreements"></a><span data-ttu-id="d41df-184">采购协议财务维度</span><span class="sxs-lookup"><span data-stu-id="d41df-184">Financial dimensions on purchase agreements</span></span>
<span data-ttu-id="d41df-185">您可以将财务维度复制到采购协议的文档抬头或单独的行。</span><span class="sxs-lookup"><span data-stu-id="d41df-185">You can copy financial dimensions to document headers or to individual lines of a purchase agreement.</span></span> <span data-ttu-id="d41df-186">如果您在协议标题中或在协议行上更改维度，则更改不影响任何已下达的订单，但会在所有新订单中得到反映。</span><span class="sxs-lookup"><span data-stu-id="d41df-186">If you change the dimensions in the agreement header or on the agreement line, the change doesn't affect any released orders, but it will be reflected on any new orders.</span></span>

<a name="see-also"></a><span data-ttu-id="d41df-187">请参阅</span><span class="sxs-lookup"><span data-stu-id="d41df-187">See also</span></span>
--------

[<span data-ttu-id="d41df-188">创建采购协议（任务指南）</span><span class="sxs-lookup"><span data-stu-id="d41df-188">Create a purchase agreement (Task guide)</span></span>](tasks/create-purchase-agreement.md)

[<span data-ttu-id="d41df-189">从采购协议创建采购下达订单（任务指南）</span><span class="sxs-lookup"><span data-stu-id="d41df-189">Create a purchase release order from a purchase agreement (Task guide)</span></span>](tasks/create-purchase-release-order-purchase-agreement.md)




