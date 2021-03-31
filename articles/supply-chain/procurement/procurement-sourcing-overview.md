---
title: 采购概览
description: 文本提供在采购模块中可用的功能的概览。
author: RichardLuan
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecb785a53bc9e0f761ba904ee674bd091bf8c444
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206935"
---
# <a name="procurement-and-sourcing-overview"></a><span data-ttu-id="0481f-103">采购概览</span><span class="sxs-lookup"><span data-stu-id="0481f-103">Procurement and sourcing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0481f-104">文本提供在采购模块中可用的功能的概览。</span><span class="sxs-lookup"><span data-stu-id="0481f-104">This article gives an overview of the functionality that's available in the Procurement and sourcing module.</span></span>

<span data-ttu-id="0481f-105">采购包括从确定产品和服务需求到采购产品、收货、开票和处理供应商付款的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="0481f-105">Procurement and sourcing covers all the steps from identifying a need for product and services through procuring the product, receipt, invoicing, and processing of payment with vendors.</span></span> <span data-ttu-id="0481f-106">采购流程可以通过定义采购策略和工作流来针对特定业务需求进行配置。</span><span class="sxs-lookup"><span data-stu-id="0481f-106">Procurement processes can be configured toward specific business needs by defining purchasing policies and workflows.</span></span>

## <a name="identifying-a-need-for-product-and-services"></a><span data-ttu-id="0481f-107">确定产品和服务的需求</span><span class="sxs-lookup"><span data-stu-id="0481f-107">Identifying a need for product and services</span></span>

<span data-ttu-id="0481f-108">产品或服务的需求可能源自 *申请*，例如，当员工需要产品时。</span><span class="sxs-lookup"><span data-stu-id="0481f-108">The need for products or services may arise from *requisitions*, for example, when an employee requires a product.</span></span> <span data-ttu-id="0481f-109">可以设置 *产品目录* 来引导从中进行选择的可用产品的选择，或对目录中尚未可用的产品提出请求，从而允许采购部门考虑如何供应产品。</span><span class="sxs-lookup"><span data-stu-id="0481f-109">*Product catalogs* can be set up to guide the selection of available products to select from, or requests can be made for products that are not yet made available in a catalog, allowing the purchasing department to consider how the product can be supplied.</span></span>  

<span data-ttu-id="0481f-110">*花费限制* 可以用于约束申请花费，*采购工作流* 添加在订购发生前要求审核的选项。</span><span class="sxs-lookup"><span data-stu-id="0481f-110">*Spending limits* can be used to constrain requisition spending, and the *purchasing workflow* adds the option of requiring approval before ordering happen.</span></span> <span data-ttu-id="0481f-111">如果需要，还可以指定预算资金分配。</span><span class="sxs-lookup"><span data-stu-id="0481f-111">It's also possible to specify budget fund allocation, if required.</span></span>  

<span data-ttu-id="0481f-112">采购部门为所需的产品和服务确定供应商，这可能涉及发送给多个潜在供应商的 *询价*。</span><span class="sxs-lookup"><span data-stu-id="0481f-112">The procurement department identifies suppliers for required products and services, and this can involve a *request for quotation* being sent out to multiple potential suppliers.</span></span> <span data-ttu-id="0481f-113">可以共享请求产品的规格，并且供应商能够查看这些信息来确定其能否交付符合这些规格的产品。</span><span class="sxs-lookup"><span data-stu-id="0481f-113">It's possible to share the specifications of the product that's being requested and potential vendors can view these to see if they can deliver a product that conforms with them.</span></span> <span data-ttu-id="0481f-114">供应商返回出价，采购部门然后在选择要采购的供应商前审查该出价。</span><span class="sxs-lookup"><span data-stu-id="0481f-114">Vendors return their bids which are then reviewed by the procurement department before they select the supplier that they want to procure from.</span></span>  

<span data-ttu-id="0481f-115">采购订单包括将 *采购查询* 发送到供应商的选项，作为更为全面的询价流程的备选。</span><span class="sxs-lookup"><span data-stu-id="0481f-115">Purchase orders include an option to send out a *purchase inquiry* to the vendor as an alternative to a more comprehensive request for quotation process.</span></span> <span data-ttu-id="0481f-116">采购查询可用于帮助设定诸如订单的价格、折扣和交货日期等期限。</span><span class="sxs-lookup"><span data-stu-id="0481f-116">The purchase inquiry can be used to help establish terms like prices, discounts, and delivery date for the order.</span></span> <span data-ttu-id="0481f-117">如果供应商被设置为使用 **供应商** 门户，采购查询功能将禁用。</span><span class="sxs-lookup"><span data-stu-id="0481f-117">If vendors are set up to use the **Vendor** portal, purchase inquiry functionality is disabled.</span></span> <span data-ttu-id="0481f-118">而如果该订单在 **供应商** 门户共享，当 *确认请求* 发送时，供应商可以直接确认该订单。</span><span class="sxs-lookup"><span data-stu-id="0481f-118">Instead the order is shared on the **Vendor** portal, and when a *confirmation request* is sent the vendor can directly confirm the order.</span></span>  

<span data-ttu-id="0481f-119">*供应商目录* 可以用于收集有关供应商可以供应的产品分类的信息。</span><span class="sxs-lookup"><span data-stu-id="0481f-119">*Vendor catalogs* can be used to collect information on the product assortment that vendors can supply.</span></span> <span data-ttu-id="0481f-120">供应商可以发布他们自己的目录，因此，更易保持最新目录。</span><span class="sxs-lookup"><span data-stu-id="0481f-120">Vendors can publish their own catalog, so it's easier to keep the catalog up to date.</span></span> <span data-ttu-id="0481f-121">可以将 *核准供应商列表* 附加到产品，这可以帮助在打开新采购订单时指导供应商选择，并防止使用意外的供应商。</span><span class="sxs-lookup"><span data-stu-id="0481f-121">It's possible to attach an *approved vendor list* to a product, and this can help guide vendor selection when new purchase orders are opened, and prevent the use of unintended vendors.</span></span>

## <a name="procurement"></a><span data-ttu-id="0481f-122">采购</span><span class="sxs-lookup"><span data-stu-id="0481f-122">Procurement</span></span>

<span data-ttu-id="0481f-123">*采购订单* 可以使用一些不同的方法创建，包括：</span><span class="sxs-lookup"><span data-stu-id="0481f-123">*Purchase orders* can be created in a number of different ways including:</span></span>

- <span data-ttu-id="0481f-124">作为确定要求采购的需求的主计划的结果。</span><span class="sxs-lookup"><span data-stu-id="0481f-124">As an outcome of master planning which has identified a demand that requires a purchase.</span></span> <span data-ttu-id="0481f-125">此流程生成计划采购订单，在下达这些订单时，采购订单将生成。</span><span class="sxs-lookup"><span data-stu-id="0481f-125">This process generates planned purchase orders, and when these are released, purchase orders are generated.</span></span>
- <span data-ttu-id="0481f-126">通过处理生成采购的采购申请。</span><span class="sxs-lookup"><span data-stu-id="0481f-126">Through the processing of purchase requisitions that result in procurement.</span></span>
- <span data-ttu-id="0481f-127">通过处理采购协议，其中采购订单从协议作为下达单创建。</span><span class="sxs-lookup"><span data-stu-id="0481f-127">Through the processing of purchase agreements, where purchase orders are created as released orders from the agreements.</span></span> <span data-ttu-id="0481f-128">通常用于在采购协议用来表示总订单时。</span><span class="sxs-lookup"><span data-stu-id="0481f-128">This is commonly used when purchase agreements are used to represent blanket orders.</span></span>
- <span data-ttu-id="0481f-129">手动创建，创建的采购订单不基于其他单据时。</span><span class="sxs-lookup"><span data-stu-id="0481f-129">Manually, when the purchase order that's created is not based on another document.</span></span>

<span data-ttu-id="0481f-130">使用 *采购审核工作流* 配置的采购订单在被记录为已审核之前需要进行审核，在该订单可以进一步处理前也需要审核。</span><span class="sxs-lookup"><span data-stu-id="0481f-130">Purchase orders that are configured with *purchase approval workflows* require approval before they are recorded as approved, and this is required before the order can be processed further.</span></span>

<span data-ttu-id="0481f-131">*确认* 采购订单以表示已与该供应商建立了协议。</span><span class="sxs-lookup"><span data-stu-id="0481f-131">Purchase orders are *confirmed* to represent that an agreement has been established with the vendor.</span></span> <span data-ttu-id="0481f-132">采购订单然后将逐渐经历不同状态，直到最后开票或取消。</span><span class="sxs-lookup"><span data-stu-id="0481f-132">The purchase order will then gradually progress through different states until ultimately being invoiced or canceled.</span></span>  

<span data-ttu-id="0481f-133">创建采购订单时，许多字段预先填充了值，这些值默认自 **供应商** 页面中存储的供应商相关信息。</span><span class="sxs-lookup"><span data-stu-id="0481f-133">When you create a purchase order, many of the fields are pre-populated with values that default from the information stored about the vendor in the **Vendors** page.</span></span> <span data-ttu-id="0481f-134">这意味着您需要在采购订单上填写有限数量的字段，虽然您可以选择覆盖默认值。</span><span class="sxs-lookup"><span data-stu-id="0481f-134">This means that there are a limited number of fields that you need to fill in on the purchase order, although you can choose to override the default values.</span></span>

### <a name="prices-and-discounts"></a><span data-ttu-id="0481f-135">价格和折扣</span><span class="sxs-lookup"><span data-stu-id="0481f-135">Prices and discounts</span></span>

<span data-ttu-id="0481f-136">价格和折扣包括有关价格、折扣及其提供的返利条款的信息。</span><span class="sxs-lookup"><span data-stu-id="0481f-136">Prices and discounts includes information about the prices, discounts, and rebate terms that they offer.</span></span> <span data-ttu-id="0481f-137">价格和折扣可以表示为 *贸易协议*。</span><span class="sxs-lookup"><span data-stu-id="0481f-137">Prices and discounts can be represented as *trade agreements*.</span></span> <span data-ttu-id="0481f-138">贸易协议表示包含价格或折扣的供应商价目表，并且具有协议生效的一组特定日期。</span><span class="sxs-lookup"><span data-stu-id="0481f-138">Trade agreements represent vendor price lists with prices or discounts, and have a specific set of dates for which the agreement is valid.</span></span> <span data-ttu-id="0481f-139">价格和折扣可以通过包含诸如承诺等条件的 *采购协议* 进行协商和表示，以作为协商条款的前提条件购买特定数量或货币金额。</span><span class="sxs-lookup"><span data-stu-id="0481f-139">Prices and discounts can be negotiated and represented through *purchase agreements* with conditions like commitments to buy certain volumes or monetary amounts as a precondition for the negotiated terms.</span></span> <span data-ttu-id="0481f-140">可以与供应商建立 *返利协议*，规定特定产品或产品组的采购可以根据采购金额或数量触发从供应商的返利。</span><span class="sxs-lookup"><span data-stu-id="0481f-140">*Rebate agreements* can be created with vendors where the procurement of specific products or groups of products may trigger a rebate from the vendor depending on the purchase amount or volume.</span></span>

### <a name="delivery-options"></a><span data-ttu-id="0481f-141">交货选项</span><span class="sxs-lookup"><span data-stu-id="0481f-141">Delivery options</span></span>

<span data-ttu-id="0481f-142">存在与采购订单相关的交货流程的不同选项。</span><span class="sxs-lookup"><span data-stu-id="0481f-142">There are different options for the delivery process associated with a purchase order.</span></span> <span data-ttu-id="0481f-143">订购的产品可以拆分为若干 *交货* 计划，在计划中，订购数量的各个部分可以计划在不同的日期交货。</span><span class="sxs-lookup"><span data-stu-id="0481f-143">Ordered products can be split into *delivery* schedules, where parts of the ordered quantity can be planned for delivery on different dates.</span></span> <span data-ttu-id="0481f-144">交货还可以包括从销售订单启动的 *直接交运*，在与采购订单上记录的产品收货相同的时间自动在销售订单上生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="0481f-144">Delivery can also include *direct delivery* initiated from a sales order, which automates the generation of the packing slip on the sales order at the same time as the product receipt is recorded on the purchase order.</span></span> <span data-ttu-id="0481f-145">采购订单还可以为 *内部公司订单* 链的一部分，也称作内部公司采购订单，在其中产品从匹配的内部公司销售订单订购。</span><span class="sxs-lookup"><span data-stu-id="0481f-145">Purchase orders can also be part an *intercompany order* chain, also referred to as intercompany purchase orders, where products are ordered from a matching intercompany sales order.</span></span> <span data-ttu-id="0481f-146">在此情况下，某些步骤自动跨两个相关的内部公司订单。</span><span class="sxs-lookup"><span data-stu-id="0481f-146">In this situation, some steps are automated across the two related intercompany orders.</span></span>

### <a name="supplementary-items"></a><span data-ttu-id="0481f-147">附属物料</span><span class="sxs-lookup"><span data-stu-id="0481f-147">Supplementary items</span></span>

<span data-ttu-id="0481f-148">产品可以设置为包括 *附属物料*。</span><span class="sxs-lookup"><span data-stu-id="0481f-148">Products can be set up to include *supplementary items*.</span></span> <span data-ttu-id="0481f-149">这是为了建议与已订购的产品相关的产品。</span><span class="sxs-lookup"><span data-stu-id="0481f-149">This is to propose products that are related to the product that's being ordered.</span></span> <span data-ttu-id="0481f-150">附加产品可以是必需的也可以是可选的。</span><span class="sxs-lookup"><span data-stu-id="0481f-150">The additional products may be required, or may be optional.</span></span> <span data-ttu-id="0481f-151">在某些情况下，附属物料可以添加为随其他产品采购的免费产品。</span><span class="sxs-lookup"><span data-stu-id="0481f-151">In some cases, supplementary items may be added as free products that accompany the purchase of other products.</span></span>

### <a name="purchase-order-charges"></a><span data-ttu-id="0481f-152">采购订单费用</span><span class="sxs-lookup"><span data-stu-id="0481f-152">Purchase order charges</span></span>

<span data-ttu-id="0481f-153">费用可以分配给采购订单。</span><span class="sxs-lookup"><span data-stu-id="0481f-153">Charges can be assigned to the purchase order.</span></span> <span data-ttu-id="0481f-154">这可以通过设置自动费用或通过手动添加费用自动发生。</span><span class="sxs-lookup"><span data-stu-id="0481f-154">This can happen automatically through setup of automatic charges or by adding the charges manually.</span></span> <span data-ttu-id="0481f-155">费用可在订单头级别或订单行级别分配到订单。</span><span class="sxs-lookup"><span data-stu-id="0481f-155">Charges can be assigned to the order at the header level, or at the order line level.</span></span> <span data-ttu-id="0481f-156">费用核算可以通过不同方式设置。</span><span class="sxs-lookup"><span data-stu-id="0481f-156">Accounting of charges can be set up in different ways.</span></span> <span data-ttu-id="0481f-157">例如，您可以设置作为产品成本核算费用。</span><span class="sxs-lookup"><span data-stu-id="0481f-157">For example, you can set up a charge to be accounted as a product cost.</span></span> <span data-ttu-id="0481f-158">如果您执行此操作，费用必须在订单可以确认前在订单行级别分配。</span><span class="sxs-lookup"><span data-stu-id="0481f-158">If you do this, the charges must be assigned at the order line level before the order can be confirmed.</span></span> <span data-ttu-id="0481f-159">有一个选项可以帮助将费用从订单头分配到各行。</span><span class="sxs-lookup"><span data-stu-id="0481f-159">There is an option that can help allocate charges from the order header to the lines.</span></span>

## <a name="product-receipt-and-invoicing"></a><span data-ttu-id="0481f-160">产品收货和开票</span><span class="sxs-lookup"><span data-stu-id="0481f-160">Product receipt and invoicing</span></span>

<span data-ttu-id="0481f-161">包括实际产品的采购订单通常要求在仓库内进行 *到达登记*，然后为订单登记 *产品收货*。</span><span class="sxs-lookup"><span data-stu-id="0481f-161">Purchase orders that include physical products commonly require *arrival registration* to happen within a warehouse, and after this a *product receipt* is registered for the order.</span></span> <span data-ttu-id="0481f-162">可以配置包含符合需要的产品的采购订单，这样请求产品的员工也需要提供 *收货确认*。</span><span class="sxs-lookup"><span data-stu-id="0481f-162">Purchase orders with products that fulfill requisitions may be configured so that the employee who has requested the products also needs to provide a *confirmation of receipt*.</span></span>  

<span data-ttu-id="0481f-163">有些采购订单包括属于服务或其他非实际产品（不需要在仓库中收货）的产品。</span><span class="sxs-lookup"><span data-stu-id="0481f-163">Some purchase orders include products that are services or other non-physical products where receipt in a warehouse is not needed.</span></span> <span data-ttu-id="0481f-164">产品可以创建为服务或 *采购类别* 可直接用于此类订单的采购订单。</span><span class="sxs-lookup"><span data-stu-id="0481f-164">Products can be created as services or *procurement categories* can be used directly on the purchase order for such orders.</span></span> <span data-ttu-id="0481f-165">使用这些订单，有时会跳过产品收货核算，并且订单直接开票，或产品收货登记在没有任何先前到达登记的采购订单上完成。</span><span class="sxs-lookup"><span data-stu-id="0481f-165">With these orders, accounting of product receipt is sometimes skipped and the order is invoiced directly, or alternatively product receipt registration is done on the purchase order without any prior arrival registration.</span></span>  

<span data-ttu-id="0481f-166">产品收货可能导致特定目的的自动消耗。</span><span class="sxs-lookup"><span data-stu-id="0481f-166">Receipt of products may result in automatic consumption for a specific purpose.</span></span> <span data-ttu-id="0481f-167">这包括直接交运的隐含消耗、项目消耗或核算作为固定资产的产品的消耗。</span><span class="sxs-lookup"><span data-stu-id="0481f-167">This includes implied consumption with direct delivery, consumption towards a project, or accounting the product as a fixed asset.</span></span>  

<span data-ttu-id="0481f-168">在 *供应商发票* 从供应商到达时，它们可能首先在 *发票登记簿* 记录，与采购订单无关，然后对照采购订单作为记录审核。</span><span class="sxs-lookup"><span data-stu-id="0481f-168">When *vendor invoices* arrive from the vendor they may first be recorded in the *invoice register* independent of the purchase order, and then later approved as a record against the purchase order.</span></span> <span data-ttu-id="0481f-169">记录包含采购订单的供应商发票包括匹配针对发票的产品收货。</span><span class="sxs-lookup"><span data-stu-id="0481f-169">Recording the vendor invoice with the purchase order includes matching of the product receipt toward the invoice.</span></span>  

<span data-ttu-id="0481f-170">*会计分配* 可以在采购订单上指定以描述如何在分类帐中执行核算，并且还可以定义当预算资金分配包含在您的配置中时如何获取分配。</span><span class="sxs-lookup"><span data-stu-id="0481f-170">*Accounting distributions* can be specified on the purchase order to describe how accounting should be done within the ledger, and can also define how budget fund allocation is obtained when this is included in your configuration.</span></span>  

<span data-ttu-id="0481f-171">开票的采购订单会将负债记录到应付帐款系统内的供应商帐户中，通过该系统可以处理 *供应商付款*。</span><span class="sxs-lookup"><span data-stu-id="0481f-171">Invoiced purchase orders will record the liability into the vendor account within accounts payable, from where the *vendor payment* can be processed.</span></span>

## <a name="vendor-performance"></a><span data-ttu-id="0481f-172">供应商表现</span><span class="sxs-lookup"><span data-stu-id="0481f-172">Vendor performance</span></span>

<span data-ttu-id="0481f-173">*采购和应付帐款报告* 包括支出分析和供应商绩效分析，通过这些报告可以了解绩效和审核采购。</span><span class="sxs-lookup"><span data-stu-id="0481f-173">Performance and review of purchasing is supported through *procurement and account payable reports*, which include spend analysis and vendor performance analysis.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]