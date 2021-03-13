---
title: 价格、折扣、协议和返点故障排除
description: 本主题介绍如何解决在使用价格、折扣、协议和返点时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 14fdddabde7739cbf9ba0fcee0fa0b8b816e74dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007358"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="4c511-103">价格、折扣、协议和返点故障排除</span><span class="sxs-lookup"><span data-stu-id="4c511-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="4c511-104">本主题介绍如何解决在使用价格、折扣、协议和返点时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="4c511-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="4c511-105">创建采购订单后，我无法将采购协议链接到采购订单行。</span><span class="sxs-lookup"><span data-stu-id="4c511-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="4c511-106">创建采购订单时，必须将采购协议与采购订单关联。</span><span class="sxs-lookup"><span data-stu-id="4c511-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="4c511-107">否则，采购订单行无法与采购协议行关联。</span><span class="sxs-lookup"><span data-stu-id="4c511-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="4c511-108">哪项检查会触发“请更新手动输入的价格和折扣或外部单据”消息？</span><span class="sxs-lookup"><span data-stu-id="4c511-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="4c511-109">更改装运日期时，您可能会收到一条消息，显示“请更新手动输入的价格和折扣或外部单据”。</span><span class="sxs-lookup"><span data-stu-id="4c511-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="4c511-110">您收到此消息的原因是，如果更改了装运日期，其他贸易或销售协议可能会被触发，导致价格更改。</span><span class="sxs-lookup"><span data-stu-id="4c511-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="4c511-111">装运日期的更改还会影响仓库计划和其他相关信息。</span><span class="sxs-lookup"><span data-stu-id="4c511-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="4c511-112">每当更改日期或另外一些参数都会触发此消息。</span><span class="sxs-lookup"><span data-stu-id="4c511-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="4c511-113">此消息的目的是确保您知道由于这些更改，可能发生价格更改。</span><span class="sxs-lookup"><span data-stu-id="4c511-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="4c511-114">此消息是贸易协议评估 (TAE) 提示。</span><span class="sxs-lookup"><span data-stu-id="4c511-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="4c511-115">有关完整说明，请参阅[贸易协议评估政策](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)。</span><span class="sxs-lookup"><span data-stu-id="4c511-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="4c511-116">采购订单收货不包括所有费用。</span><span class="sxs-lookup"><span data-stu-id="4c511-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="4c511-117">重现问题</span><span class="sxs-lookup"><span data-stu-id="4c511-117">Reproduce the issue</span></span>

<span data-ttu-id="4c511-118">以下过程显示了一种重现此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="4c511-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="4c511-119">在 **采购参数** 页上的 **交货** 选项卡上，确保将 **在产品收货时生成费用** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="4c511-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="4c511-120">创建包含费用的采购订单。</span><span class="sxs-lookup"><span data-stu-id="4c511-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="4c511-121">确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="4c511-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="4c511-122">接收采购订单。</span><span class="sxs-lookup"><span data-stu-id="4c511-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="4c511-123">查看收货总计，并将其与预期总计进行比较。</span><span class="sxs-lookup"><span data-stu-id="4c511-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="4c511-124">请注意，并非所有费用都包含在采购订单收货中。</span><span class="sxs-lookup"><span data-stu-id="4c511-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c511-125">解决问题</span><span class="sxs-lookup"><span data-stu-id="4c511-125">Issue resolution</span></span>

<span data-ttu-id="4c511-126">解决方法取决于设置杂项费用的方式。</span><span class="sxs-lookup"><span data-stu-id="4c511-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="4c511-127">有关如何设置杂项费用以满足您的要求的信息，请参阅以下博客文章：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。</span><span class="sxs-lookup"><span data-stu-id="4c511-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="4c511-128">贸易协议价格和折扣不应用于通过数据管理导入的销售或采购订单行。</span><span class="sxs-lookup"><span data-stu-id="4c511-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c511-129">问题描述</span><span class="sxs-lookup"><span data-stu-id="4c511-129">Issue description</span></span>

<span data-ttu-id="4c511-130">适用于销售或采购订单行的贸易协议不应用于通过数据管理导入的行。</span><span class="sxs-lookup"><span data-stu-id="4c511-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="4c511-131">但是，相同的贸易协议应用于手动创建的销售或采购订单行。</span><span class="sxs-lookup"><span data-stu-id="4c511-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="4c511-132">问题原因</span><span class="sxs-lookup"><span data-stu-id="4c511-132">Reason for the issue</span></span>

<span data-ttu-id="4c511-133">如果通过数据管理导入的采购订单行已经包含价格信息，将不会重新评估这些行的贸易协议。</span><span class="sxs-lookup"><span data-stu-id="4c511-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="4c511-134">例如，如果 **单行折扣率** 或为某行设置了价格和折扣值，则不会查找该行的贸易协议。</span><span class="sxs-lookup"><span data-stu-id="4c511-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="4c511-135">问题解决方法</span><span class="sxs-lookup"><span data-stu-id="4c511-135">Issue workaround</span></span>

<span data-ttu-id="4c511-136">此行为是预期的，对于销售订单和采购订单是相似的。</span><span class="sxs-lookup"><span data-stu-id="4c511-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="4c511-137">解决方法是，导入采购订单行而不设置任何价格信息。</span><span class="sxs-lookup"><span data-stu-id="4c511-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="4c511-138">然后将应用贸易协议，并将基于定义的贸易协议更新采购订单行。</span><span class="sxs-lookup"><span data-stu-id="4c511-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="4c511-139">不会根据发票累计供应商返点。</span><span class="sxs-lookup"><span data-stu-id="4c511-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c511-140">问题描述</span><span class="sxs-lookup"><span data-stu-id="4c511-140">Issue description</span></span>

<span data-ttu-id="4c511-141">如果过帐的发票具有不同的截止日期，这些发票不会反映在从它们生成的供应商返点中。</span><span class="sxs-lookup"><span data-stu-id="4c511-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c511-142">解决问题</span><span class="sxs-lookup"><span data-stu-id="4c511-142">Issue resolution</span></span>

<span data-ttu-id="4c511-143">根据设计，在计算供应商返点时不考虑截止日期。</span><span class="sxs-lookup"><span data-stu-id="4c511-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="4c511-144">考虑自定义系统，以使截止日期和与发票的关系相对于实际的供应商返点更加明显。</span><span class="sxs-lookup"><span data-stu-id="4c511-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="4c511-145">采购订单上的单位价格不是基于单位转换来计算的。</span><span class="sxs-lookup"><span data-stu-id="4c511-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c511-146">问题描述</span><span class="sxs-lookup"><span data-stu-id="4c511-146">Issue description</span></span>

<span data-ttu-id="4c511-147">在采购订单上更改单位时，不会根据单位转换定义重新计算贸易协议价格。</span><span class="sxs-lookup"><span data-stu-id="4c511-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c511-148">解决问题</span><span class="sxs-lookup"><span data-stu-id="4c511-148">Issue resolution</span></span>

<span data-ttu-id="4c511-149">价格始终从贸易协议（或系统中的其他价格设置，如销售协议或物料价格）获取，它们是针对单位设置的。</span><span class="sxs-lookup"><span data-stu-id="4c511-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="4c511-150">如果在订单行上更改了单位，系统将为新单位查找价格并应用该价格。</span><span class="sxs-lookup"><span data-stu-id="4c511-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="4c511-151">如果未为该单位找到价格，系统不会应用价格。</span><span class="sxs-lookup"><span data-stu-id="4c511-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="4c511-152">单位转换不能用于将价格重新计算为另一个单位。</span><span class="sxs-lookup"><span data-stu-id="4c511-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="4c511-153">从理论上讲，一盒十个的价格可能不等于一盒价格的十倍。</span><span class="sxs-lookup"><span data-stu-id="4c511-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="4c511-154">问题解决方法</span><span class="sxs-lookup"><span data-stu-id="4c511-154">Issue workaround</span></span>

<span data-ttu-id="4c511-155">解决此问题的一种方法是，确保有您预期的单位的贸易协议将用于物料的订单行。</span><span class="sxs-lookup"><span data-stu-id="4c511-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="4c511-156">贸易协议中会发生货币转换问题。</span><span class="sxs-lookup"><span data-stu-id="4c511-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="4c511-157">当采购订单上的货币不同时，不会根据货币重新计算贸易协议价格。</span><span class="sxs-lookup"><span data-stu-id="4c511-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="4c511-158">*通用货币* 功能可让您仅使用一种货币定义价格和折扣。</span><span class="sxs-lookup"><span data-stu-id="4c511-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="4c511-159">然后，您可以根据需要转换为其他货币。</span><span class="sxs-lookup"><span data-stu-id="4c511-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="4c511-160">而且，转换完成后，此功能还可以自动应用智能舍入。</span><span class="sxs-lookup"><span data-stu-id="4c511-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="4c511-161">当我以行视图模式打开“采购协议”页时，我无法通过在该行的概览中添加“计价单位”字段来个性化该页面。</span><span class="sxs-lookup"><span data-stu-id="4c511-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="4c511-162">协议框架中的某些共享字段不能包含在个性化设置中。</span><span class="sxs-lookup"><span data-stu-id="4c511-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="4c511-163">由于实现了数据模型，因此会出现此限制。</span><span class="sxs-lookup"><span data-stu-id="4c511-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="4c511-164">因此，您无法个性化 **计价单位** 字段。</span><span class="sxs-lookup"><span data-stu-id="4c511-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="4c511-165">采购协议的最大限制对采购申请无效。</span><span class="sxs-lookup"><span data-stu-id="4c511-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c511-166">问题描述</span><span class="sxs-lookup"><span data-stu-id="4c511-166">Issue description</span></span>

<span data-ttu-id="4c511-167">当采购申请链接到采购协议时，采购协议的最大限制对采购申请无效。</span><span class="sxs-lookup"><span data-stu-id="4c511-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="4c511-168">默认价格信息已正确输入，但可以在采购申请中订购超过采购协议最大限制的量。</span><span class="sxs-lookup"><span data-stu-id="4c511-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c511-169">解决问题</span><span class="sxs-lookup"><span data-stu-id="4c511-169">Issue resolution</span></span>

<span data-ttu-id="4c511-170">此行为是预期的。</span><span class="sxs-lookup"><span data-stu-id="4c511-170">This behavior is expected.</span></span> <span data-ttu-id="4c511-171">由于采购申请不一定总是得到批准，因此不应在采购协议上保留数量或金额。</span><span class="sxs-lookup"><span data-stu-id="4c511-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="4c511-172">因此，您不会达到采购协议的最大限制。</span><span class="sxs-lookup"><span data-stu-id="4c511-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="4c511-173">贸易协议可以从拒绝的询价创建。</span><span class="sxs-lookup"><span data-stu-id="4c511-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="4c511-174">因此，如果询价行未被接受，系统不会阻止创建贸易协议日记帐。</span><span class="sxs-lookup"><span data-stu-id="4c511-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="4c511-175">您可以为询价 (RFQ) 的任何回复创建贸易协议，无论它们是被接受还是被拒绝。</span><span class="sxs-lookup"><span data-stu-id="4c511-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="4c511-176">有关详细信息，请参阅[询价 (RFQ) 概述](request-quotations.md)。</span><span class="sxs-lookup"><span data-stu-id="4c511-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>

