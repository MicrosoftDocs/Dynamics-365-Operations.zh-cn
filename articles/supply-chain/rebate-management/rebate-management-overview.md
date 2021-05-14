---
title: 返点管理模块概述
description: 本主题提供 Microsoft Dynamics 365 Supply Chain Management 的返点管理模块的概述。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 7917f36d8ff3c1ae2d37c5390806ef82771b5211
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920029"
---
# <a name="rebate-management-module-overview"></a><span data-ttu-id="68cb0-103">返点管理模块概述</span><span class="sxs-lookup"><span data-stu-id="68cb0-103">Rebate management module overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68cb0-104">您可以使用 **返点管理** 模块在您的企业与其客户或供应商之间创建合同、交易或协议，以便您可以计算返点、扣缴和特许使用费。</span><span class="sxs-lookup"><span data-stu-id="68cb0-104">You can use the **Rebate management** module to create contracts, deals, or agreements between your business and its customers or vendors, so that you can calculate rebates, deductions, and royalties.</span></span> <span data-ttu-id="68cb0-105">返点管理在中央位置跟踪和维护返点和扣缴交易记录，用户可以在该位置有效创建、查看和处理这些交易记录。</span><span class="sxs-lookup"><span data-stu-id="68cb0-105">Rebate management tracks and maintains rebate and deduction transactions in a central location where users can effectively create, review, and process them.</span></span>

<span data-ttu-id="68cb0-106">返点管理支持创建、维护和处理 *返点*。</span><span class="sxs-lookup"><span data-stu-id="68cb0-106">Rebate management supports the creation, maintenance, and processing of *rebates*.</span></span> <span data-ttu-id="68cb0-107">返点是卖方或买方返还部分采购价格。</span><span class="sxs-lookup"><span data-stu-id="68cb0-107">A rebate is the return of part of the purchase price by a seller or a buyer.</span></span> <span data-ttu-id="68cb0-108">返点通常基于在特定期间内采购的特定数量或价值的商品。</span><span class="sxs-lookup"><span data-stu-id="68cb0-108">Rebates are typically based on the purchase of a specific quantity or value of goods during a specific period.</span></span> <span data-ttu-id="68cb0-109">与折扣不同，在对采购金额开具全额发票后进行返点。</span><span class="sxs-lookup"><span data-stu-id="68cb0-109">Unlike discounts, rebates are done after the purchase amount is fully invoiced.</span></span>

<span data-ttu-id="68cb0-110">返点管理也支持 *扣缴*。</span><span class="sxs-lookup"><span data-stu-id="68cb0-110">Rebate management also supports *deductions*.</span></span> <span data-ttu-id="68cb0-111">扣缴是指为了获得使用品牌、商标或专利等知识产权的许可或特权或者为了获得将自然资源用于钓鱼、打猎或采矿等目的的特权而支付的薪酬、报酬或费用。</span><span class="sxs-lookup"><span data-stu-id="68cb0-111">A deduction is compensation, a consideration, or a fee that is paid either for a license or the privilege to use intellectual property such as a brand, copyright, or patent, or for the privilege to use a natural resource for a purpose such as for fishing, hunting, or mining.</span></span> <span data-ttu-id="68cb0-112">扣缴通常按已实现使用的收入或利润的百分比计算。</span><span class="sxs-lookup"><span data-stu-id="68cb0-112">Deductions are usually calculated as a percentage of the revenue or profit from realized use.</span></span> <span data-ttu-id="68cb0-113">使用的知识产权或自然资源越多，实现的扣缴就越大。</span><span class="sxs-lookup"><span data-stu-id="68cb0-113">The more the intellectual property or natural resource is used, the greater the deduction that is realized.</span></span>

<span data-ttu-id="68cb0-114">此外，返点管理支持客户 *特许使用费*。</span><span class="sxs-lookup"><span data-stu-id="68cb0-114">Additionally, Rebate management supports customer *royalties*.</span></span> <span data-ttu-id="68cb0-115">特许使用费是指一方为了获得资产使用权向许可接收方或特许经营人支付的款项。</span><span class="sxs-lookup"><span data-stu-id="68cb0-115">Royalties are payments that one party makes to the licensee or franchisee for the right to use an asset.</span></span>

<span data-ttu-id="68cb0-116">返点管理使您可以定义预配、返点和勾销的过帐配置文件。</span><span class="sxs-lookup"><span data-stu-id="68cb0-116">Rebate management lets you define posting profiles for provisions, rebates, and write-offs.</span></span> <span data-ttu-id="68cb0-117">此外，可以为特定客户或供应商定义过帐。</span><span class="sxs-lookup"><span data-stu-id="68cb0-117">Furthermore, the postings can be defined for a specific customer or vendor.</span></span> <span data-ttu-id="68cb0-118">这样，可以通过过帐跟踪不适用于所有客户或供应商方案的交易。</span><span class="sxs-lookup"><span data-stu-id="68cb0-118">In this way, deals that don't apply to all customer or vendor scenarios can be tracked via postings.</span></span>

<span data-ttu-id="68cb0-119">将根据在批处理作业中选择和计划的计算方法自动生成返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="68cb0-119">Rebate transactions are automatically generated, based on the calculation method that is selected and scheduled in batch jobs.</span></span> <span data-ttu-id="68cb0-120">此外，您可以设置工作流来管理、查看和审核协议。</span><span class="sxs-lookup"><span data-stu-id="68cb0-120">Additionally, you can set up workflows to manage, review, and approve agreements.</span></span>

## <a name="basis-calculation"></a><span data-ttu-id="68cb0-121">计算基础</span><span class="sxs-lookup"><span data-stu-id="68cb0-121">Basis calculation</span></span>

<span data-ttu-id="68cb0-122">客户返点、客户特许使用费和供应商返点可以使用不同的基础，具体取决于您的业务需求：</span><span class="sxs-lookup"><span data-stu-id="68cb0-122">Customer rebates, customer royalties, and vendor rebates can all use a different basis, depending on your business requirements:</span></span>

- <span data-ttu-id="68cb0-123">客户返点可以基于销售订单、交货通知或发票。</span><span class="sxs-lookup"><span data-stu-id="68cb0-123">Customer rebates can be based on sales orders, delivery notes, or invoices.</span></span>
- <span data-ttu-id="68cb0-124">客户特许使用费可以基于销售订单、交货通知或已支付发票。</span><span class="sxs-lookup"><span data-stu-id="68cb0-124">Customer royalties can be based on sales orders, delivery notes, or paid invoices.</span></span>
- <span data-ttu-id="68cb0-125">供应商返点可以基于采购订单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="68cb0-125">Vendor rebates can be based on either purchase orders or sales orders.</span></span> <span data-ttu-id="68cb0-126">可以基于从返点供应商处采购和通过销售发票出售给客户的产品来计算它们。</span><span class="sxs-lookup"><span data-stu-id="68cb0-126">They can be calculated based on products that are purchased from the rebate vendor and sold to customers via sales invoices.</span></span>

## <a name="flexible-calculations"></a><span data-ttu-id="68cb0-127">灵活计算</span><span class="sxs-lookup"><span data-stu-id="68cb0-127">Flexible calculations</span></span>

<span data-ttu-id="68cb0-128">返点计算期间同时适用于客户交易和供应商交易。</span><span class="sxs-lookup"><span data-stu-id="68cb0-128">Rebate calculation periods are available for both customer deals and vendor deals.</span></span> <span data-ttu-id="68cb0-129">计算期间定义交易的长度、计算频率和计算期间。</span><span class="sxs-lookup"><span data-stu-id="68cb0-129">A calculation period defines the length of the deal, the calculation frequency, and the calculation period.</span></span> <span data-ttu-id="68cb0-130">可以基于返点期间内合格产品的销售订单数量和金额累计返点。</span><span class="sxs-lookup"><span data-stu-id="68cb0-130">The rebates can be accrued based on the sales order quantities or amounts for qualified products during the rebate period.</span></span>

<span data-ttu-id="68cb0-131">对于每个协议计算，可以设置以下任意期间：</span><span class="sxs-lookup"><span data-stu-id="68cb0-131">For each agreement calculation, any of the following periods can be set:</span></span>

- <span data-ttu-id="68cb0-132">账单</span><span class="sxs-lookup"><span data-stu-id="68cb0-132">Invoice</span></span>
- <span data-ttu-id="68cb0-133">日</span><span class="sxs-lookup"><span data-stu-id="68cb0-133">Day</span></span>
- <span data-ttu-id="68cb0-134">周</span><span class="sxs-lookup"><span data-stu-id="68cb0-134">Week</span></span>
- <span data-ttu-id="68cb0-135">月</span><span class="sxs-lookup"><span data-stu-id="68cb0-135">Month</span></span>
- <span data-ttu-id="68cb0-136">季度</span><span class="sxs-lookup"><span data-stu-id="68cb0-136">Quarter</span></span>
- <span data-ttu-id="68cb0-137">年</span><span class="sxs-lookup"><span data-stu-id="68cb0-137">Year</span></span>
- <span data-ttu-id="68cb0-138">自定义期间</span><span class="sxs-lookup"><span data-stu-id="68cb0-138">Customized period</span></span>
- <span data-ttu-id="68cb0-139">先前列出的任何期间的任意倍数</span><span class="sxs-lookup"><span data-stu-id="68cb0-139">Any multiple of any of the previously listed periods</span></span>

<span data-ttu-id="68cb0-140">该计算可以应用于单个客户和产品、客户和产品组或所有客户和产品。</span><span class="sxs-lookup"><span data-stu-id="68cb0-140">The calculation can be applied to individual customers and products, groups of customers and products, or all customers and products.</span></span> <span data-ttu-id="68cb0-141">具有多个明细行的返点可以具有不同的合格日期范围。</span><span class="sxs-lookup"><span data-stu-id="68cb0-141">Rebates that have multiple detail lines can have different qualifying date ranges.</span></span> <span data-ttu-id="68cb0-142">预配和声明期间可能不同。</span><span class="sxs-lookup"><span data-stu-id="68cb0-142">The provision and claim periods can differ.</span></span> <span data-ttu-id="68cb0-143">例如，预配可以每天访问，而声明每月处理一次。</span><span class="sxs-lookup"><span data-stu-id="68cb0-143">For example, provisions can be processed every day, whereas claims are processed once per month.</span></span>

<span data-ttu-id="68cb0-144">可以根据许多不同的参数配置返点。</span><span class="sxs-lookup"><span data-stu-id="68cb0-144">Rebates can be configured based on many different parameters.</span></span> <span data-ttu-id="68cb0-145">例如，可以将它们配置为百分比、比率或固定金额。</span><span class="sxs-lookup"><span data-stu-id="68cb0-145">For example, they can be configured as a percentage, a rate, or a fixed amount.</span></span> <span data-ttu-id="68cb0-146">有四种主要计算方法：</span><span class="sxs-lookup"><span data-stu-id="68cb0-146">There are four main calculation methods:</span></span>

- <span data-ttu-id="68cb0-147">分步</span><span class="sxs-lookup"><span data-stu-id="68cb0-147">Stepped</span></span>
- <span data-ttu-id="68cb0-148">累计</span><span class="sxs-lookup"><span data-stu-id="68cb0-148">Cumulative</span></span>
- <span data-ttu-id="68cb0-149">滚动</span><span class="sxs-lookup"><span data-stu-id="68cb0-149">Rolling</span></span>
- <span data-ttu-id="68cb0-150">总值</span><span class="sxs-lookup"><span data-stu-id="68cb0-150">Total value</span></span>

<span data-ttu-id="68cb0-151">还可以使用其他返点减去返点计算结果，具体取决于是否将返点设置为基于净额进行计算。</span><span class="sxs-lookup"><span data-stu-id="68cb0-151">Rebate calculation results can also be reduced by other rebates, depending on whether the rebate is set up to calculate based on the net amount.</span></span>

<span data-ttu-id="68cb0-152">在供应商方面，返点可以基于先见先出 (FIFO) 规则、最新采购价格、平均采购价格或销售价格计算价格。</span><span class="sxs-lookup"><span data-stu-id="68cb0-152">On the vendor side, rebates can calculate the price based on a first in, first out (FIFO) rule, the latest purchase price, the average purchase price, or the sales price.</span></span>

## <a name="rebate-target-transactions"></a><span data-ttu-id="68cb0-153">返点目标交易记录</span><span class="sxs-lookup"><span data-stu-id="68cb0-153">Rebate target transactions</span></span>

<span data-ttu-id="68cb0-154">返点交易或协议生成的输出可以是财务或物料。</span><span class="sxs-lookup"><span data-stu-id="68cb0-154">The outputs that the rebate deal or agreement generates can be financials or items.</span></span>

<span data-ttu-id="68cb0-155">财务输出由从过帐配置文件分配给协议的付款类型确定。</span><span class="sxs-lookup"><span data-stu-id="68cb0-155">Financial outputs are determined by the payment type that is assigned to the agreement from the posting profile.</span></span> <span data-ttu-id="68cb0-156">这些输出可以包括客户扣缴日记帐、普通发票和供应商发票。</span><span class="sxs-lookup"><span data-stu-id="68cb0-156">These outputs can include customer deduction journals, free text invoices, and vendor invoices.</span></span> <span data-ttu-id="68cb0-157">出于审计目的，财务返点目标交易记录包括对原始返点协议的引用。</span><span class="sxs-lookup"><span data-stu-id="68cb0-157">For auditing purposes, financial rebate target transactions include a reference to the originating rebate agreement.</span></span>

<span data-ttu-id="68cb0-158">物料输出为客户返点创建可用物料销售订单，为供应商返点创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="68cb0-158">Item outputs create a free item sales order for customer rebates and a purchase order for vendor rebates.</span></span> <span data-ttu-id="68cb0-159">物料返点目标交易记录包含用于确定应在可用物料销售订单或采购订单上输入哪个返点引用的选项。</span><span class="sxs-lookup"><span data-stu-id="68cb0-159">Item rebate target transactions contain options to determine which rebate reference should be entered on the free item sales order or purchase order.</span></span>

## <a name="accurate-rebate-calculations"></a><span data-ttu-id="68cb0-160">准确的返点计算</span><span class="sxs-lookup"><span data-stu-id="68cb0-160">Accurate rebate calculations</span></span>

<span data-ttu-id="68cb0-161">选择的关联交易、计算频率、计算基础和计算方法的组合可确定返点计算的准确性和精确度。</span><span class="sxs-lookup"><span data-stu-id="68cb0-161">The combination of the associated deals, the frequency of the calculations, the calculation basis, and the calculation method that is selected determines the accuracy and precision of rebate calculations.</span></span> <span data-ttu-id="68cb0-162">返点预配可用于累积已过帐和已声明的价值。</span><span class="sxs-lookup"><span data-stu-id="68cb0-162">Rebate provisions can be used to accrue posted and claimed values.</span></span>

<span data-ttu-id="68cb0-163">可以每天或每月管理预配。</span><span class="sxs-lookup"><span data-stu-id="68cb0-163">Provisions can be managed daily or monthly.</span></span> <span data-ttu-id="68cb0-164">但是，该功能可以按任何定义的频率分配或支付返点，或接收其付款。</span><span class="sxs-lookup"><span data-stu-id="68cb0-164">However, the functionality can allocate or pay the rebate, or receive payment of it, at any defined frequency.</span></span> <span data-ttu-id="68cb0-165">在付款期间，用户可以随时轻松调整计划或付款金额。</span><span class="sxs-lookup"><span data-stu-id="68cb0-165">Users can easily adjust a plan or payment amounts at any time during the payout.</span></span>

<span data-ttu-id="68cb0-166">用户不再需要分两步处理交易或预配。</span><span class="sxs-lookup"><span data-stu-id="68cb0-166">Users no longer have to handle deals or provisions in two steps.</span></span> <span data-ttu-id="68cb0-167">预配和勾销将直接过帐到分类帐。</span><span class="sxs-lookup"><span data-stu-id="68cb0-167">Provisions and write-offs are posted directly to the ledger.</span></span> <span data-ttu-id="68cb0-168">此外，可以自动创建贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="68cb0-168">Additionally, credit notes can be created automatically.</span></span> <span data-ttu-id="68cb0-169">因此，存在与应付帐款和应收帐款的完全集成。</span><span class="sxs-lookup"><span data-stu-id="68cb0-169">Therefore, there is full integration with accounts payable and accounts receivable.</span></span> <span data-ttu-id="68cb0-170">在处理过程中，计算将考虑结算折扣、已支付发票、贸易折扣和现有贷方通知单，以确保准确计算金额和价值。</span><span class="sxs-lookup"><span data-stu-id="68cb0-170">During processing, the calculations consider settlement discounts, paid invoices, trade discounts, and existing credit notes to ensure that amounts and values are accurately calculated.</span></span>

<span data-ttu-id="68cb0-171">计算返点时，该流程将创建可在过帐之前查看的交易记录。</span><span class="sxs-lookup"><span data-stu-id="68cb0-171">When rebates are calculated, the process creates transactions that can be reviewed before posting occurs.</span></span> <span data-ttu-id="68cb0-172">然后，可以创建日记帐、贷方通知单或借方交易记录。</span><span class="sxs-lookup"><span data-stu-id="68cb0-172">A journal, credit note, or debit transaction can then be created.</span></span> <span data-ttu-id="68cb0-173">单独的流程过帐返点和扣缴交易记录。</span><span class="sxs-lookup"><span data-stu-id="68cb0-173">A separate process posts rebate and deduction transactions.</span></span> <span data-ttu-id="68cb0-174">可以获取报告对帐单和交易记录列表以确保合规性、有效性和透明度。</span><span class="sxs-lookup"><span data-stu-id="68cb0-174">Reporting statements and transaction listings can be obtained to ensure compliance, effectiveness, and transparency.</span></span>

## <a name="guaranteed-royalty-payments"></a><span data-ttu-id="68cb0-175">担保特许使用费付款</span><span class="sxs-lookup"><span data-stu-id="68cb0-175">Guaranteed royalty payments</span></span>

<span data-ttu-id="68cb0-176">在返点管理中，通过自动付款生成可以快速轻松地处理特许使用费，即使在最低担保适用时。</span><span class="sxs-lookup"><span data-stu-id="68cb0-176">In Rebate management, automatic payment generation enables royalties to be handled quickly and easily, even when guaranteed minimums apply.</span></span> 

## <a name="maximizing-spend-versus-rebates"></a><span data-ttu-id="68cb0-177">最大化支出与返点</span><span class="sxs-lookup"><span data-stu-id="68cb0-177">Maximizing spend versus rebates</span></span>

<span data-ttu-id="68cb0-178">供应商和产品可以按地区分组，并且可以提供不同的产品/服务，具体取决于交易记录的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="68cb0-178">Vendors and products can be grouped by territory, and different offers can be provided, depending on the country or region of the transaction.</span></span> <span data-ttu-id="68cb0-179">当用户选择产品时，他们可以定义包含的物料以及将在返点结算中使用的物料数量。</span><span class="sxs-lookup"><span data-stu-id="68cb0-179">When users select products, they can define the items that are included and the number of items that will be used in the rebate settlement.</span></span>
