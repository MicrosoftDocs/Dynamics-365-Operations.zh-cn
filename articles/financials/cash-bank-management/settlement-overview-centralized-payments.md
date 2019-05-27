---
title: 集中付款的结算概览
description: 此主题介绍 Microsoft Dynamics 365 for Finance and Operations 的集中付款的结算。
author: abruer
manager: AnnBe
ms.date: 08/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fecc9027d0df7b268a3241ea0f1797849db2d90
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565454"
---
# <a name="settlement-overview-for-centralized-payments"></a><span data-ttu-id="c19f2-103">集中付款的结算概览</span><span class="sxs-lookup"><span data-stu-id="c19f2-103">Settlement overview for centralized payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c19f2-104">包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="c19f2-104">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="c19f2-105">这样，就无需在多个法人分别输入相同的交易记录，通过优化付款方案流程、结算流程、未结交易记录编辑和针对集中式付款的已结算交易记录编辑来节约时间。</span><span class="sxs-lookup"><span data-stu-id="c19f2-105">This eliminates the need to enter the same transaction in multiple legal entities and saves time by streamlining the payment proposal process, the settlement process, open transaction editing, and closed transaction editing for centralized payments.</span></span> 

<span data-ttu-id="c19f2-106">当在一个法人中输入客户或供应商付款，并且用在其他法人中输入的发票结算该付款时，将自动为每个法人生成适用的结算、应付和应收交易记录。</span><span class="sxs-lookup"><span data-stu-id="c19f2-106">When a customer or vendor payment is entered in one legal entity and is settled with an invoice that was entered in another legal entity, the applicable settlement, due-to, and due-from transactions are automatically generated for each legal entity.</span></span> <span data-ttu-id="c19f2-107">将为该交易记录中每个发票和付款组合创建一个结算记录。</span><span class="sxs-lookup"><span data-stu-id="c19f2-107">A settlement record is created for each combination of invoice and payment in the transaction.</span></span> <span data-ttu-id="c19f2-108">每一个结算记录都分配了一个新的凭证号，它基于在针对客户的**应收账款参数**页和针对供应商的**应付账款参数**页上指定的付款凭证编号规则系列。</span><span class="sxs-lookup"><span data-stu-id="c19f2-108">Each settlement record is assigned a new voucher number, which is based on the payment voucher number sequence series that is specified on the **Accounts receivable parameters** page for customers and on the **Accounts payable parameters** page for vendors.</span></span> 

<span data-ttu-id="c19f2-109">如果为现金折扣、外币汇率重估、尾差、超额付款或支付不足生成附加的结算记录，则向它们分配更晚的付款或发票交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="c19f2-109">If additional settlement records are generated for cash discounts, foreign currency revaluations, penny differences, overpayments, or underpayments, they are assigned the later date of the payment or invoice transaction.</span></span> <span data-ttu-id="c19f2-110">如果结算在过帐付款后发生，则结算记录将使用在**结算未结交易记录**页指定的结算过帐日期。</span><span class="sxs-lookup"><span data-stu-id="c19f2-110">If settlement occurs after the payment is posted, the settlement records use the settlement posting date that is specified on the **Settle open transactions** page.</span></span>

## <a name="posting-types-transaction-types-and-default-descriptions"></a><span data-ttu-id="c19f2-111">过帐类型、交易记录类型和默认描述</span><span class="sxs-lookup"><span data-stu-id="c19f2-111">Posting types, transaction types, and default descriptions</span></span>

<span data-ttu-id="c19f2-112">内部公司结算凭证交易记录使用内部公司结算过帐类型、内部公司客户结算和内部公司供应商结算交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="c19f2-112">Intercompany settlement voucher transactions use the intercompany settlement posting type, intercompany customer settlement, and intercompany vendor settlement transaction types.</span></span> <span data-ttu-id="c19f2-113">您可以在**默认描述**页设置与该交易记录类型有关的信息。</span><span class="sxs-lookup"><span data-stu-id="c19f2-113">You can set up information for the transaction type on the **Default descriptions** page.</span></span> 

<span data-ttu-id="c19f2-114">以下交易记录类型可供在单个公司和跨公司结算中使用：</span><span class="sxs-lookup"><span data-stu-id="c19f2-114">The following transaction types are available for use in single-company and cross-company settlements:</span></span>

-   <span data-ttu-id="c19f2-115">结算</span><span class="sxs-lookup"><span data-stu-id="c19f2-115">Settlement</span></span>
-   <span data-ttu-id="c19f2-116">现金折扣</span><span class="sxs-lookup"><span data-stu-id="c19f2-116">Cash discount</span></span>
-   <span data-ttu-id="c19f2-117">外币重估（包括已实现和未实现的外币重估）</span><span class="sxs-lookup"><span data-stu-id="c19f2-117">Foreign currency revaluations (includes realized and unrealized foreign currency revaluations)</span></span>
-   <span data-ttu-id="c19f2-118">尾差</span><span class="sxs-lookup"><span data-stu-id="c19f2-118">Penny difference</span></span>
-   <span data-ttu-id="c19f2-119">超额支付/支付不足</span><span class="sxs-lookup"><span data-stu-id="c19f2-119">Overpayment/underpayment</span></span>

<span data-ttu-id="c19f2-120">您还可为内部公司结算凭证定义默认描述。</span><span class="sxs-lookup"><span data-stu-id="c19f2-120">You can also define default descriptions for intercompany settlement vouchers.</span></span>

## <a name="currency-exchange-gains-or-losses"></a><span data-ttu-id="c19f2-121">币种汇兑损益</span><span class="sxs-lookup"><span data-stu-id="c19f2-121">Currency exchange gains or losses</span></span>

<span data-ttu-id="c19f2-122">用于客户或供应商交易记录的汇率与交易记录一起存储。</span><span class="sxs-lookup"><span data-stu-id="c19f2-122">The exchange rate that is used for customer or vendor transactions is stored with the transaction.</span></span> <span data-ttu-id="c19f2-123">币种转换的已有损益过帐到发票法人或付款法人，具体取决于在针对付款法人的**内部公司会计**页的**过帐币种转换损益**字段中选择的选项。</span><span class="sxs-lookup"><span data-stu-id="c19f2-123">Realized gains or losses for currency exchanges are posted to either the legal entity of the invoice or the legal entity of the payment, depending on the option that is selected in the **Post currency exchange gain or loss** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="c19f2-124">以下示例将使用这些币种：</span><span class="sxs-lookup"><span data-stu-id="c19f2-124">The following examples use these currencies:</span></span>
-   <span data-ttu-id="c19f2-125">付款记帐币种：EUR</span><span class="sxs-lookup"><span data-stu-id="c19f2-125">Payment accounting currency: EUR</span></span>
-   <span data-ttu-id="c19f2-126">发票记帐币种：USD</span><span class="sxs-lookup"><span data-stu-id="c19f2-126">Invoice accounting currency: USD</span></span>
-   <span data-ttu-id="c19f2-127">付款交易记录币种：DKK</span><span class="sxs-lookup"><span data-stu-id="c19f2-127">Payment transaction currency: DKK</span></span>
-   <span data-ttu-id="c19f2-128">发票交易记录币种：CAD</span><span class="sxs-lookup"><span data-stu-id="c19f2-128">Invoice transaction currency: CAD</span></span>

### <a name="currency-calculations"></a><span data-ttu-id="c19f2-129">币种计算</span><span class="sxs-lookup"><span data-stu-id="c19f2-129">Currency calculations</span></span>

<span data-ttu-id="c19f2-130">在用在一个法人中输入的付款结算输入到其他法人中的发票时，该付款的交易记录币种 (DKK) 将用以下三个步骤转换：</span><span class="sxs-lookup"><span data-stu-id="c19f2-130">When settling an invoice that is entered in one legal entity with a payment that is entered in another legal entity, the transaction currency of the payment (DKK) is converted in three steps:</span></span>
1.  <span data-ttu-id="c19f2-131">使用来自付款法人的汇率，转换为付款的记帐币种 (EUR)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-131">Converted to the accounting currency of the payment (EUR), using the exchange rates from the legal entity of the payment.</span></span>
2.  <span data-ttu-id="c19f2-132">转换为发票的记帐币种 (USD)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-132">Converted to the accounting currency of the invoice (USD).</span></span>
3.  <span data-ttu-id="c19f2-133">使用来自发票法人的汇率，转换为发票的交易记录币种 (CAD)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-133">Converted to the transaction currency of the invoice (CAD), using the exchange rates from the legal entity of the invoice.</span></span>

<span data-ttu-id="c19f2-134">该转换过程使用截至付款日期的汇率。</span><span class="sxs-lookup"><span data-stu-id="c19f2-134">The conversion process uses the exchange rates as of the payment date.</span></span> <span data-ttu-id="c19f2-135">如果采用发票交易记录币种 (CAD) 的最终付款金额等于发票金额 (CAD)，则该发票将被视为完全支付。</span><span class="sxs-lookup"><span data-stu-id="c19f2-135">If the resulting payment amount in the transaction currency of the invoice (CAD) is equal to the invoice amount (CAD), the invoice is considered fully paid.</span></span> 

<span data-ttu-id="c19f2-136">在未输入付款金额的付款日记帐中打开**结算未结交易记录**页时，基于在**结算未结交易记录**页上选择的要结算的发票计算结算金额。</span><span class="sxs-lookup"><span data-stu-id="c19f2-136">When the **Settle open transactions** page is opened from a payment journal where the payment amount was not entered, the amount to settle is calculated based on the invoices that are selected for settlement on the **Settle open transactions** page.</span></span> <span data-ttu-id="c19f2-137">要结算的金额将通过以下三个步骤转换：</span><span class="sxs-lookup"><span data-stu-id="c19f2-137">The amount to settle is converted in three steps:</span></span>
1.  <span data-ttu-id="c19f2-138">使用付款日期的来自发票法人的汇率，转换为发票的记帐币种 (USD)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-138">Converted to the accounting currency of the invoice (USD), using the exchange rates from the legal entity of the invoice as of the payment date.</span></span>
2.  <span data-ttu-id="c19f2-139">使用付款日期的来自发票法人的汇率，转换为付款的记帐币种 (EUR)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-139">Converted to the accounting currency of the payment (EUR), using the exchange rates from the legal entity of the invoice as of the payment date.</span></span>
3.  <span data-ttu-id="c19f2-140">转换为付款的交易记录币种 (DKK)。</span><span class="sxs-lookup"><span data-stu-id="c19f2-140">Converted to the transaction currency of the payment (DKK).</span></span>

<span data-ttu-id="c19f2-141">在您关闭**结算未结交易记录**页时，最终的付款金额将转移到付款日志帐行。</span><span class="sxs-lookup"><span data-stu-id="c19f2-141">The resulting payment amount is transferred to the payment journal line when you close the **Settle open transactions** page.</span></span>

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a><span data-ttu-id="c19f2-142">损益的过帐由于不同的分期付款币种</span><span class="sxs-lookup"><span data-stu-id="c19f2-142">Posting for gain or loss because of different accounting currencies</span></span>

<span data-ttu-id="c19f2-143">如果存在币种转换损益，损益将过帐到为付款法人的**内部公司会计**页的**过帐币种转换损益**字段指定的法人。</span><span class="sxs-lookup"><span data-stu-id="c19f2-143">If there is a currency exchange gain or loss, the gain or loss is posted to the legal entity that is specified for the **Post currency exchange gain or loss** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="c19f2-144">损益金额换算为损益金额过帐法人的分期付款币种，使用为该法人定义的汇率。</span><span class="sxs-lookup"><span data-stu-id="c19f2-144">The gain or loss amount is converted to the accounting currency of the legal entity where the gain or loss amount is posted, using the exchange rate that is defined for that legal entity.</span></span>

## <a name="cash-discounts"></a><span data-ttu-id="c19f2-145">现金折扣</span><span class="sxs-lookup"><span data-stu-id="c19f2-145">Cash discounts</span></span>

<span data-ttu-id="c19f2-146">在内部公司结算流程中生成的现金折扣过帐到发票法人或付款法人，具体取决于为付款法人的**内部公司会计**页的**过帐现金折扣**字段选择的选项。</span><span class="sxs-lookup"><span data-stu-id="c19f2-146">Cash discounts that are generated during the cross-company settlement process are posted to either the legal entity of the invoice or the legal entity of the payment, depending on the option that is selected for the **Post cash discount** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="c19f2-147">在发票的法人中生成相应的结算交易记录。</span><span class="sxs-lookup"><span data-stu-id="c19f2-147">A corresponding settlement transaction is generated in the legal entity of the invoice.</span></span>

## <a name="overpayments-and-underpayments"></a><span data-ttu-id="c19f2-148">超额支付和支付不足</span><span class="sxs-lookup"><span data-stu-id="c19f2-148">Overpayments and underpayments</span></span>

<span data-ttu-id="c19f2-149">超额支付、支付不足和尾差容差基于超额支付的付款法人以及支付不足的发票法人确定。</span><span class="sxs-lookup"><span data-stu-id="c19f2-149">Overpayment, underpayment, and penny difference tolerances are determined based on the legal entity of the payment for overpayments, and on the legal entity of the invoice for underpayments.</span></span> <span data-ttu-id="c19f2-150">使用的过帐科目取决于针对客户的**应收账款参数**页的**现金折扣管理**字段和针对供应商的**应付账款参数**页的**现金折扣管理**字段中的设置。</span><span class="sxs-lookup"><span data-stu-id="c19f2-150">The posting account that is used is determined by the setting in the **Cash discount administration** field on the **Accounts receivable parameters** page for customers, and the **Cash discount administration** field on the **Accounts payable parameters** page for vendors.</span></span>

-   <span data-ttu-id="c19f2-151">如果现金折扣管理设置为“特定”，或者如果设置为“非特定”，且在超额支付的不同法人中过帐适用的现金折扣，则使用“客户现金折扣”、“供应商现金折扣”或“以记帐币种表示的尾差”的自动科目。</span><span class="sxs-lookup"><span data-stu-id="c19f2-151">If the cash discount administration setting is Specific, or if the setting is Unspecific and the applicable cash discount is posted in a different legal entity from the overpayment, the automatic account for Customer cash discount, Vendor cash discount, or Penny difference in accounting currency is used.</span></span> <span data-ttu-id="c19f2-152">您可以在**自动交易记录帐户**页上指定这些科目。</span><span class="sxs-lookup"><span data-stu-id="c19f2-152">You can specify these accounts on the **Accounts for automatic transactions** page.</span></span>
-   <span data-ttu-id="c19f2-153">如果现金折扣管理设置为“非特定”，并且在与超额支付相同的法人中（付款法人和发票的法人相同）过帐现金折扣，则调整现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="c19f2-153">If the cash discount administration setting is Unspecific and the cash discount is posted in the same legal entity as the overpayment (the legal entity of the payment and the legal entity of the invoice are the same), the cash discount account is adjusted.</span></span> <span data-ttu-id="c19f2-154">例如，如果金额为 100.00 的发票（且具有 3.00 的可用现金折扣）使用金额为 98.00 的付款结算，则为 1.00 调整现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="c19f2-154">For example, if an invoice for 100.00 with an available cash discount of 3.00 is settled with a payment for 98.00, the cash discount account is adjusted for 1.00.</span></span> <span data-ttu-id="c19f2-155">折扣净额是 2.00。</span><span class="sxs-lookup"><span data-stu-id="c19f2-155">The net discount amount is 2.00.</span></span>
-   <span data-ttu-id="c19f2-156">如果现金折扣管理设置为“非特定”，在与超额支付相同的法人中过帐现金折扣，并且用具有现金折扣的多张发票结算超额支付或支付不足，则调整最后一张发票的现金折扣帐户。</span><span class="sxs-lookup"><span data-stu-id="c19f2-156">If the cash discount administration setting is Unspecific, the cash discount is posted in the same legal entity as the overpayment, and the overpayment or underpayment is settled with multiple invoices with cash discounts, the cash discount account for the last invoice is adjusted.</span></span>

<span data-ttu-id="c19f2-157">如果现金折扣管理选择为“非特定”，则不指定的付款结算规则只适用于以下情况中：</span><span class="sxs-lookup"><span data-stu-id="c19f2-157">If the cash discount administration selection is Unspecific, unspecific payment settlement rules apply only in the following situations:</span></span>
-   <span data-ttu-id="c19f2-158">存在超额支付。</span><span class="sxs-lookup"><span data-stu-id="c19f2-158">There is an overpayment.</span></span>
-   <span data-ttu-id="c19f2-159">使用具有现金折扣的一张或多张发票结算超额支付。</span><span class="sxs-lookup"><span data-stu-id="c19f2-159">The overpayment is settled with one or more invoices that has a cash discount.</span></span>
-   <span data-ttu-id="c19f2-160">现金折扣在与该超额支付相同的法人中过帐。</span><span class="sxs-lookup"><span data-stu-id="c19f2-160">The cash discount is posted in the same legal entity as the overpayment.</span></span>

<span data-ttu-id="c19f2-161">在所有其他情况下，超额支付或支付不足过帐到“客户现金折扣”、“供应商现金折扣”或“以记帐币种表示的尾差”的自动科目。</span><span class="sxs-lookup"><span data-stu-id="c19f2-161">In all other situations, overpayments or underpayments are posted to the automatic account for Customer cash discount, Vendor cash discount, or Penny difference in accounting currency.</span></span>

## <a name="sales-tax"></a><span data-ttu-id="c19f2-162">增值税</span><span class="sxs-lookup"><span data-stu-id="c19f2-162">Sales tax</span></span>
<span data-ttu-id="c19f2-163">增值税交易记录保留在最初过帐它们的法人中。</span><span class="sxs-lookup"><span data-stu-id="c19f2-163">Sales tax transactions remain in the legal entity where they were originally posted.</span></span> 

<span data-ttu-id="c19f2-164">如果已经为某一预付款过帐了增值税，则跨公司结算将冲销预付款法人中针对预付款的增值税。</span><span class="sxs-lookup"><span data-stu-id="c19f2-164">If sales tax was posted for a prepayment, the cross-company settlement reverses the sales tax on the prepayment in the legal entity of the prepayment.</span></span> <span data-ttu-id="c19f2-165">在税发票的法人保留在发票的法人中。</span><span class="sxs-lookup"><span data-stu-id="c19f2-165">The taxes in the legal entity of the invoice remain in the legal entity of the invoice.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="c19f2-166">财务维度</span><span class="sxs-lookup"><span data-stu-id="c19f2-166">Financial dimensions</span></span>
<span data-ttu-id="c19f2-167">对于客户付款，付款法人中的应收和应付交易记录使用根据要结算的付款为应收账款汇总科目指定的财务维度。</span><span class="sxs-lookup"><span data-stu-id="c19f2-167">For customer payments, the due-to and due-from transactions in the legal entity of the payment use the financial dimensions that are specified for the accounts receivable summary account from the payment that is being settled.</span></span> <span data-ttu-id="c19f2-168">在发票的法人中，应收和应付交易记录使用根据要结算的发票为应收账款汇总科目指定的财务维度。</span><span class="sxs-lookup"><span data-stu-id="c19f2-168">In the legal entity of the invoice, due-to and due-from transactions use the financial dimensions that are specified for the accounts receivable summary account from the invoice that is being settled.</span></span> 

<span data-ttu-id="c19f2-169">对于供应商付款，付款法人中的应收和应付交易记录使用根据要结算的付款为应付账款汇总科目指定的财务维度。</span><span class="sxs-lookup"><span data-stu-id="c19f2-169">For vendor payments, the due-to and due-from transactions in the legal entity of the payment use the financial dimensions that are specified for the accounts payable summary account from the payment that is being settled.</span></span> <span data-ttu-id="c19f2-170">在发票的法人中，应收和应付交易记录使用根据要结算的发票为应付账款汇总科目指定的财务维度。</span><span class="sxs-lookup"><span data-stu-id="c19f2-170">In the legal entity of the invoice, due-to and due-from transactions use the financial dimensions that are specified for the accounts payable summary account from the invoice that is being settled.</span></span>

## <a name="withholding-tax"></a><span data-ttu-id="c19f2-171">预缴税金</span><span class="sxs-lookup"><span data-stu-id="c19f2-171">Withholding tax</span></span>
<span data-ttu-id="c19f2-172">与发票关联的供应商帐户用于确定是否应计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="c19f2-172">The vendor account that is associated with the invoice is used to determine whether withholding tax should be calculated.</span></span> <span data-ttu-id="c19f2-173">如果预缴税金如果适用，则在与发票关联的法人中计算。</span><span class="sxs-lookup"><span data-stu-id="c19f2-173">If withholding tax applies, it is calculated in the legal entity that is associated with the invoice.</span></span> <span data-ttu-id="c19f2-174">如果使用不同币种法人，则使用来自与发票关联的法人的汇率。</span><span class="sxs-lookup"><span data-stu-id="c19f2-174">If the legal entities use different currencies, the exchange rate from the legal entity that is associated with the invoice is used.</span></span>
