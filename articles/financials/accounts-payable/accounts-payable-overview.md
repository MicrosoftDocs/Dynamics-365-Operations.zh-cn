---
title: "配置应付账款"
description: "本文介绍您用于在 Microsoft Dynamics 365 for Finance and Operations 中设置应付帐款的基本和可选功能的页面。 还介绍您在开始设置应付账款前必须完成的设置步骤。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6a832a30870f77578503bae6eea17ad1d0881d91
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="configure-accounts-payable"></a><span data-ttu-id="d829c-104">配置应付账款</span><span class="sxs-lookup"><span data-stu-id="d829c-104">Configure Accounts payable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d829c-105">本文介绍您用于在 Microsoft Dynamics 365 for Finance and Operations 中设置应付帐款的基本和可选功能的页面。</span><span class="sxs-lookup"><span data-stu-id="d829c-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d829c-106">还介绍您在开始设置应付账款前必须完成的设置步骤。</span><span class="sxs-lookup"><span data-stu-id="d829c-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="d829c-107">应付账款设置的先决条件</span><span class="sxs-lookup"><span data-stu-id="d829c-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="d829c-108">在设置应付账款之前，您必须先完成以下设置：</span><span class="sxs-lookup"><span data-stu-id="d829c-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="d829c-109">在总帐中：</span><span class="sxs-lookup"><span data-stu-id="d829c-109">In General ledger:</span></span>
    -   <span data-ttu-id="d829c-110">如果您计划使用付款日记帐，则必须设置付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="d829c-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="d829c-111">如果您计划运行汇率调整，请在“币种”页上设置币种代码，在“汇率类型”页上设置汇率类型，在“币种汇率”页上设置币种汇率。</span><span class="sxs-lookup"><span data-stu-id="d829c-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="d829c-112">在“现金和银行管理”中，设置要与付款方式一同使用的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="d829c-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="d829c-113">应付账款的设置页</span><span class="sxs-lookup"><span data-stu-id="d829c-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="d829c-114">使用以下页面为每个法人设置应付账款的基本功能。</span><span class="sxs-lookup"><span data-stu-id="d829c-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="d829c-115">这些页面按推荐的设置顺序列出。</span><span class="sxs-lookup"><span data-stu-id="d829c-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="d829c-116">若要使设置过程更简单，您可以从创建的第一批记录里创建模板。</span><span class="sxs-lookup"><span data-stu-id="d829c-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="d829c-117">在模板中，通常在许多字段中输入值，以反映组织要为特定类型的供应商实现的功能。</span><span class="sxs-lookup"><span data-stu-id="d829c-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="d829c-118">在“付款期限”页上，定义您指派给销售订单、采购订单、客户和供应商的付款期限，以及确定发票到期日期。</span><span class="sxs-lookup"><span data-stu-id="d829c-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="d829c-119">有关详细信息，请参阅[定义供应商付款费用](tasks/define-vendor-payment-fees.md)。</span><span class="sxs-lookup"><span data-stu-id="d829c-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="d829c-120">在“付款方式 - 供应商”页上，创建和维护有关组织如何向其供应商付款的信息。</span><span class="sxs-lookup"><span data-stu-id="d829c-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="d829c-121">在“供应商组”页上，创建和维护共享用于过帐、结算和付款、报告和预测的重要参数的供应商组。</span><span class="sxs-lookup"><span data-stu-id="d829c-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="d829c-122">在“供应商过帐模板”页上，定义供应商交易记录如何过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="d829c-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="d829c-123">在“应付账款参数”页上，为应付账款设置在未指定具体设置时应用的默认设置、不同功能类型的参数以及各种编号规则。</span><span class="sxs-lookup"><span data-stu-id="d829c-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="d829c-124">在“窗体设置”页上，定义与供应商相关并用于组织中的不同单据格式，以跟踪来自供应商的收据以及输入向供应商付款的原因。</span><span class="sxs-lookup"><span data-stu-id="d829c-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="d829c-125">在“供应商”页上，创建和维护供应商帐户，以及组织向其申报增值税的税务主管机构。</span><span class="sxs-lookup"><span data-stu-id="d829c-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="d829c-126">应付账款的可选设置页</span><span class="sxs-lookup"><span data-stu-id="d829c-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="d829c-127">除了基本功能外，应付账款还具有可设置的其他功能。</span><span class="sxs-lookup"><span data-stu-id="d829c-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="d829c-128">附加的设置页按功能组织。</span><span class="sxs-lookup"><span data-stu-id="d829c-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="d829c-129">**策略**</span><span class="sxs-lookup"><span data-stu-id="d829c-129">**Policies**</span></span>
-   <span data-ttu-id="d829c-130">在“供应商发票政策”页上，设置供应商发票政策。</span><span class="sxs-lookup"><span data-stu-id="d829c-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="d829c-131">**发票匹配**</span><span class="sxs-lookup"><span data-stu-id="d829c-131">**Invoice matching**</span></span>

-   <span data-ttu-id="d829c-132">在“发票合计容差”页上，设置发票合计的容差。</span><span class="sxs-lookup"><span data-stu-id="d829c-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="d829c-133">在“匹配政策”页上，设置双向匹配政策和三向匹配政策。</span><span class="sxs-lookup"><span data-stu-id="d829c-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="d829c-134">在“价格容差”页上，设置单位价格的容差。</span><span class="sxs-lookup"><span data-stu-id="d829c-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="d829c-135">在“物料价格容差组”页上，设置物料价格的容差组。</span><span class="sxs-lookup"><span data-stu-id="d829c-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="d829c-136">在“供应商价格容差组”页上，设置供应商价格的容差组。</span><span class="sxs-lookup"><span data-stu-id="d829c-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="d829c-137">在“费用容差”页上，设置费用的容差。</span><span class="sxs-lookup"><span data-stu-id="d829c-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="d829c-138">**工作流**</span><span class="sxs-lookup"><span data-stu-id="d829c-138">**Workflow**</span></span>

-   <span data-ttu-id="d829c-139">在“应付账款工作流”页上，设置日记帐审核和采购申请的工作流配置。</span><span class="sxs-lookup"><span data-stu-id="d829c-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="d829c-140">**原因**</span><span class="sxs-lookup"><span data-stu-id="d829c-140">**Reasons**</span></span>

-   <span data-ttu-id="d829c-141">在“供应商原因”页上，设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="d829c-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="d829c-142">**费用**</span><span class="sxs-lookup"><span data-stu-id="d829c-142">**Charges**</span></span>

-   <span data-ttu-id="d829c-143">在“费用代码”页上，设置在采购订单中使用的费用的代码。</span><span class="sxs-lookup"><span data-stu-id="d829c-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="d829c-144">在“供应商费用组”页上，创建和维护供应商的费用组。</span><span class="sxs-lookup"><span data-stu-id="d829c-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="d829c-145">在“物料费用组”页上，创建和维护物料的费用组。</span><span class="sxs-lookup"><span data-stu-id="d829c-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="d829c-146">在“自动费用”页上，定义自动分配给订单的费用。</span><span class="sxs-lookup"><span data-stu-id="d829c-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="d829c-147">**附属物料**</span><span class="sxs-lookup"><span data-stu-id="d829c-147">**Supplementary items**</span></span>

-   <span data-ttu-id="d829c-148">在“附属物料组 - 供应商”页上，创建和维护供应商的附属物料组。</span><span class="sxs-lookup"><span data-stu-id="d829c-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="d829c-149">在“附属物料组 - 库存”页上，创建和维护物料的附属物料组。</span><span class="sxs-lookup"><span data-stu-id="d829c-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="d829c-150">**发运**</span><span class="sxs-lookup"><span data-stu-id="d829c-150">**Distribution**</span></span>

-   <span data-ttu-id="d829c-151">在“交货条款”页上，创建和维护将物料从卖方转移到买方的条件。</span><span class="sxs-lookup"><span data-stu-id="d829c-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="d829c-152">在“交货方式”页上，创建和维护在将订单从卖方交付到买方时使用的运输方法。</span><span class="sxs-lookup"><span data-stu-id="d829c-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="d829c-153">在“目的地代码”页上，创建和维护用于交货目的地的标识符和描述。</span><span class="sxs-lookup"><span data-stu-id="d829c-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="d829c-154">**窗体**</span><span class="sxs-lookup"><span data-stu-id="d829c-154">**Forms**</span></span>

-   <span data-ttu-id="d829c-155">在“表格附注”页上，创建在各种页面上出现的标准文本。</span><span class="sxs-lookup"><span data-stu-id="d829c-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="d829c-156">在“窗体排序参数”页上，为申请、收货清单、装箱单和发票设置排序顺序。</span><span class="sxs-lookup"><span data-stu-id="d829c-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="d829c-157">在“打印管理设置”页上，设置页面原件和副本的打印管理信息。</span><span class="sxs-lookup"><span data-stu-id="d829c-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="d829c-158">**付款**</span><span class="sxs-lookup"><span data-stu-id="d829c-158">**Payments**</span></span>

-   <span data-ttu-id="d829c-159">在“现金折扣”页上，设置和管理用于获取现金折扣的条款。</span><span class="sxs-lookup"><span data-stu-id="d829c-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="d829c-160">现金折扣代码链接到供应商并且应用于采购订单。</span><span class="sxs-lookup"><span data-stu-id="d829c-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="d829c-161">在“付款计划”页上，设置用于管理对供应商的分期付款的付款计划。</span><span class="sxs-lookup"><span data-stu-id="d829c-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="d829c-162">在“付款日”页上，定义用于计算到期日期的付款日，以及为星期几或具体日期指定特定付款日。</span><span class="sxs-lookup"><span data-stu-id="d829c-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="d829c-163">在“付款费用”页上，创建和维护与供应商相关联的付款费用。</span><span class="sxs-lookup"><span data-stu-id="d829c-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="d829c-164">在“付款说明”页上，创建和维护付款说明。</span><span class="sxs-lookup"><span data-stu-id="d829c-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="d829c-165">**统计**</span><span class="sxs-lookup"><span data-stu-id="d829c-165">**Statistics**</span></span>

-   <span data-ttu-id="d829c-166">在“帐龄期间定义”页上，设置用于分析供应商帐户的到期分配的用户定义的间隔。</span><span class="sxs-lookup"><span data-stu-id="d829c-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="d829c-167">在“经营范围”页上，创建分配给供应商的经营范围 (LOB) 代码。</span><span class="sxs-lookup"><span data-stu-id="d829c-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="d829c-168">**1099 税**</span><span class="sxs-lookup"><span data-stu-id="d829c-168">**Tax 1099**</span></span>

-   <span data-ttu-id="d829c-169">在 **1099 字段**页上，根据最新的 IRS 要求验证和更新负责必须向美国国税局 (IRS) 申报的最小金额。</span><span class="sxs-lookup"><span data-stu-id="d829c-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="d829c-170">**其他模块的可选设置**</span><span class="sxs-lookup"><span data-stu-id="d829c-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="d829c-171">**组织管理**</span><span class="sxs-lookup"><span data-stu-id="d829c-171">**Organization administration**</span></span>

-   <span data-ttu-id="d829c-172">在“编号规则”页上，设置发票编号的编号规则组。</span><span class="sxs-lookup"><span data-stu-id="d829c-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="d829c-173">在以下页面上，设置地址信息：</span><span class="sxs-lookup"><span data-stu-id="d829c-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="d829c-174">地址设置</span><span class="sxs-lookup"><span data-stu-id="d829c-174">Address setup</span></span>
    -   <span data-ttu-id="d829c-175">NAF 代码</span><span class="sxs-lookup"><span data-stu-id="d829c-175">NAF codes</span></span>
    -   <span data-ttu-id="d829c-176">导入邮政编码</span><span class="sxs-lookup"><span data-stu-id="d829c-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="d829c-177">**总帐**</span><span class="sxs-lookup"><span data-stu-id="d829c-177">**General ledger**</span></span>

-   <span data-ttu-id="d829c-178">在“财务维度”页上，设置财务维度。</span><span class="sxs-lookup"><span data-stu-id="d829c-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="d829c-179">在以下页面上，设置税务信息：</span><span class="sxs-lookup"><span data-stu-id="d829c-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="d829c-180">销售税代码</span><span class="sxs-lookup"><span data-stu-id="d829c-180">Sales tax codes</span></span>
    -   <span data-ttu-id="d829c-181">销售税组</span><span class="sxs-lookup"><span data-stu-id="d829c-181">Sales tax groups</span></span>
    -   <span data-ttu-id="d829c-182">销售税(物料)组</span><span class="sxs-lookup"><span data-stu-id="d829c-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="d829c-183">帐户组</span><span class="sxs-lookup"><span data-stu-id="d829c-183">Account group</span></span>
    -   <span data-ttu-id="d829c-184">免税(销售税)代码</span><span class="sxs-lookup"><span data-stu-id="d829c-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="d829c-185">销售税区域</span><span class="sxs-lookup"><span data-stu-id="d829c-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="d829c-186">销售税主管机构</span><span class="sxs-lookup"><span data-stu-id="d829c-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="d829c-187">销售税结算期间</span><span class="sxs-lookup"><span data-stu-id="d829c-187">Sales tax settlement periods</span></span>

<span data-ttu-id="d829c-188">**现金和银行管理**</span><span class="sxs-lookup"><span data-stu-id="d829c-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="d829c-189">在“付款目的代码”页上，设置主办银行目的代码。</span><span class="sxs-lookup"><span data-stu-id="d829c-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






