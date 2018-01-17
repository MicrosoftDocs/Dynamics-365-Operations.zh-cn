---
title: "设置汇票"
description: "此主题描述设置汇票的步骤。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 9b051c9a32a026af0680314f6821c251ada51d40
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-bills-of-exchange"></a><span data-ttu-id="338ef-103">设置汇票</span><span class="sxs-lookup"><span data-stu-id="338ef-103">Set up bills of exchange</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="338ef-104">此主题描述设置汇票的步骤。</span><span class="sxs-lookup"><span data-stu-id="338ef-104">This topic describes the steps for setting up bills of exchange.</span></span>

<span data-ttu-id="338ef-105">汇票是来自客户的手写或电子形式的订单，它指定其他方（通常是银行）应向公司支付指示的金额。</span><span class="sxs-lookup"><span data-stu-id="338ef-105">A bill of exchange is a written or electronic order from a customer that specifies that another party, usually a bank, should pay a stated amount to the company.</span></span> <span data-ttu-id="338ef-106">在您使用汇票作为针对销售订单发票或普通发票的付款时，您贷记该客户帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-106">When you use a bill of exchange as payment for a sales order invoice or free text invoice, you credit the customer account.</span></span> <span data-ttu-id="338ef-107">该贷记由汇票担保，直到客户向银行支付汇票。</span><span class="sxs-lookup"><span data-stu-id="338ef-107">That credit is secured by the bill of exchange until the customer pays the bill of exchange to the bank.</span></span> <span data-ttu-id="338ef-108">您通常将在到期日期通过汇票结算发票。</span><span class="sxs-lookup"><span data-stu-id="338ef-108">Typically, you will settle the invoice with the bill of exchange on the due date.</span></span> <span data-ttu-id="338ef-109">在您收到来自承兑汇票的银行的通知后，就可以关闭该汇票。</span><span class="sxs-lookup"><span data-stu-id="338ef-109">When you receive notification from your bank that the bill of exchange has been honored, you can close the bill of exchange.</span></span> <span data-ttu-id="338ef-110">您可以在以下时间之一通过您的银行支取汇票：</span><span class="sxs-lookup"><span data-stu-id="338ef-110">You can draw a bill of exchange through your bank at either of the following times:</span></span>

-   <span data-ttu-id="338ef-111">到期日期。</span><span class="sxs-lookup"><span data-stu-id="338ef-111">On the due date.</span></span> <span data-ttu-id="338ef-112">此方法也称作“托收汇款”。</span><span class="sxs-lookup"><span data-stu-id="338ef-112">This approach is known as remit for collection.</span></span>
-   <span data-ttu-id="338ef-113">在到期日期前，通常在为客户设置的付款期限指定的折扣日期。</span><span class="sxs-lookup"><span data-stu-id="338ef-113">Before the due date, typically on the discount date that is specified in the terms of payment that are set up for the customer.</span></span> <span data-ttu-id="338ef-114">当您过账交易记录时，将折扣金额过账到支出科目。</span><span class="sxs-lookup"><span data-stu-id="338ef-114">When you post the transaction, the discount amount is posted to an expense account.</span></span> <span data-ttu-id="338ef-115">剩余金额时之于您的负债（直到银行从客户接收了付款）。</span><span class="sxs-lookup"><span data-stu-id="338ef-115">The remaining amount is a liability to you until the bank receives payment from the customer.</span></span> <span data-ttu-id="338ef-116">此方法也称作“折扣汇款”。</span><span class="sxs-lookup"><span data-stu-id="338ef-116">This approach is known as remit for discount.</span></span>

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a><span data-ttu-id="338ef-117">设置汇票的过帐模板</span><span class="sxs-lookup"><span data-stu-id="338ef-117">Set up posting profiles for bills of exchange</span></span>
<span data-ttu-id="338ef-118">使用**客户过帐模板**页面设置过帐模板，以便用于汇票、拒付的汇票、托收汇款和折扣汇款。</span><span class="sxs-lookup"><span data-stu-id="338ef-118">Use the **Customer posting profiles** page to set up posting profiles that you can use with bills of exchange, protest bills of exchange, remittances for collection, and remittances for discount.</span></span> <span data-ttu-id="338ef-119">在**汇总科目**字段中，选择要将汇票金额过帐到的汇总科目。</span><span class="sxs-lookup"><span data-stu-id="338ef-119">In the **Summary account** field, select the summary account to post bill of exchange amounts to.</span></span> <span data-ttu-id="338ef-120">根据汇款交易记录的类型借记或贷记此账户：</span><span class="sxs-lookup"><span data-stu-id="338ef-120">This account is debited or credited, depending on the type of bill of exchange transaction:</span></span>
-   <span data-ttu-id="338ef-121">对于汇票，在过帐汇票时借记此帐户，在过帐折扣汇款或托收汇款时贷记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-121">For bills of exchange, this account is debited when a bill of exchange is posted, and it's credited when a remittance for discount or a remittance for collection is posted.</span></span>
-   <span data-ttu-id="338ef-122">对于拒付汇票，在过帐拒付汇票时借记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-122">For protest bills of exchange, this account is debited when a protest bill of exchange is posted.</span></span>
-   <span data-ttu-id="338ef-123">对于托收汇款，在过帐托收汇款时借记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-123">For remittances for collection, this account is debited when a remittance for collection is posted.</span></span>
-   <span data-ttu-id="338ef-124">对于折扣汇款，在过帐折扣汇款时借记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-124">For remittances for discount, this account is debited when a remittance for discount is posted.</span></span>

<span data-ttu-id="338ef-125">在**结算科目**字段中，选择要将汇票金额过帐到的现金帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-125">In the **Settle account** field, select the cash account to post bill of exchange amounts to.</span></span> <span data-ttu-id="338ef-126">在结算汇票时借记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-126">This account is debited when a bill of exchange is settled.</span></span> <span data-ttu-id="338ef-127">在**销售税预付款**字段中，选择在汇票用于预付时要将增值税金额过帐到的汇总科目。</span><span class="sxs-lookup"><span data-stu-id="338ef-127">In the **Sales tax prepayments** field, select the summary account to post sales tax amounts to when bills of exchange are used for prepayments.</span></span> <span data-ttu-id="338ef-128">在**折扣负债科目**段中，选择您要将折旧汇款的折扣金额过账到的账户。</span><span class="sxs-lookup"><span data-stu-id="338ef-128">In the **Liabilities for discount account** field, select the account to post the discount amount for remittances for discount to.</span></span> <span data-ttu-id="338ef-129">在过帐折扣汇款时贷记此帐户。</span><span class="sxs-lookup"><span data-stu-id="338ef-129">This account is credited when a remittance for discount is posted.</span></span>

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a><span data-ttu-id="338ef-130">为汇票设置应收账款参数</span><span class="sxs-lookup"><span data-stu-id="338ef-130">Set up Accounts receivable parameters for bills of exchange</span></span>
<span data-ttu-id="338ef-131">在**应收账款参数**页，在**分类帐和销售税**选项卡上输入汇票的默认过帐模板。在**编号规则**选项卡上定义编号规则。设置汇票的日记帐名称</span><span class="sxs-lookup"><span data-stu-id="338ef-131">On the **Accounts receivable parameters** page, the default posting profiles for bills of exchange are entered on the **Ledger and sales tax** tab. Number sequences are defined on the **Number sequences** tab. Set up journal names for bills of exchange</span></span>
------------------------------------------

<span data-ttu-id="338ef-132">在**日记帐名称**页面中，至少创建五个要用于汇票的日志名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-132">On the **Journals names** page, create at least five journal names to use for bills of exchange.</span></span> <span data-ttu-id="338ef-133">下面是日记帐类型：</span><span class="sxs-lookup"><span data-stu-id="338ef-133">Here are the journal types:</span></span>
-   <span data-ttu-id="338ef-134">**客户签发汇票** – 为签发汇票日记帐创建日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-134">**Customer draw bill of exchange** – Create a journal name for the Draw bill of exchange journal.</span></span>
-   <span data-ttu-id="338ef-135">**客户拒付汇票** – 为拒付汇票日记帐创建日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-135">**Customer protest bill of exchange** – Create a journal name for the Protest bill of exchange journal.</span></span>
-   <span data-ttu-id="338ef-136">**客户重新签发汇票** – 为重新签发汇票日记帐创建日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-136">**Customer redraw bill of exchange** – Create a journal name for the Redraw bill of exchange journal.</span></span>
-   <span data-ttu-id="338ef-137">**客户银行汇款** – 为汇款日记帐创建日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-137">**Customer bank remittance** – Create a journal name for the Remittance journal.</span></span>
-   <span data-ttu-id="338ef-138">**客户结算汇票** – 为结算汇票日记帐创建日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="338ef-138">**Customer settle bill of exchange** – Create a journal name for the Settle bill of exchange journal.</span></span>

<span data-ttu-id="338ef-139">在每个汇票日记帐的日记帐凭证页上，在**汇票**选项卡上输入有关汇票的信息。在过帐汇票日志行后，可以在**汇票日记帐查询**页面和**汇票统计信息**页面中看到这些行。</span><span class="sxs-lookup"><span data-stu-id="338ef-139">On the journal voucher page for each bill of exchange journal, enter information about the bill of exchange on the **Bill of exchange** tab. After the bill of exchange journal lines are posted, you can view them on the **Bill of exchange journal inquiry** page and the **Bills of exchange statistics** page.</span></span>
<span data-ttu-id="338ef-140">设置汇票的付款方式</span><span class="sxs-lookup"><span data-stu-id="338ef-140">Set up methods of payment for bills of exchange</span></span>
-----------------------------------------------

<span data-ttu-id="338ef-141">在**付款方式**页面中，为汇票至少设置一种付款方式。</span><span class="sxs-lookup"><span data-stu-id="338ef-141">On the **Methods of payment** page, set up at least one method of payment for bills of exchange.</span></span> <span data-ttu-id="338ef-142">如果您与多家银行有业务往来，则设置的付款方式应该与每家银行需要的汇票汇款格式相符。</span><span class="sxs-lookup"><span data-stu-id="338ef-142">If you do business with more than one bank, set up a method of payment that corresponds to the remittance format that each bank requires for bills of exchange.</span></span>
<span data-ttu-id="338ef-143">设置汇票的付款费用</span><span class="sxs-lookup"><span data-stu-id="338ef-143">Set up payment fees for bills of exchange</span></span>
-----------------------------------------

<span data-ttu-id="338ef-144">汇款付款是与客户付款收取过程有关的费用。</span><span class="sxs-lookup"><span data-stu-id="338ef-144">A payment fee is a charge that is associated with the process of collecting payments from customers.</span></span> <span data-ttu-id="338ef-145">每个付款费用可以与多个付款费用设置行关联。</span><span class="sxs-lookup"><span data-stu-id="338ef-145">Multiple payment fee setup lines can be associated each payment fee.</span></span> <span data-ttu-id="338ef-146">可使用设置行可以控制如何计算付款费用的默认金额。</span><span class="sxs-lookup"><span data-stu-id="338ef-146">You can use setup lines to control how default amounts for payment fees are calculated.</span></span> <span data-ttu-id="338ef-147">例如，您可以针对付款方法、付款说明、币种和时段创建设置行。</span><span class="sxs-lookup"><span data-stu-id="338ef-147">For example, you can create setup lines for methods of payment, payment specifications, currencies, and time periods.</span></span> <span data-ttu-id="338ef-148">也可以为基于日期间隔的百分比或金额创建设置行。</span><span class="sxs-lookup"><span data-stu-id="338ef-148">You can also create setup lines for a percentage or amount that is based on day intervals.</span></span> <span data-ttu-id="338ef-149">例如，可以设置基于逾期时间长度的利息百分比。</span><span class="sxs-lookup"><span data-stu-id="338ef-149">For example, you can set up an interest percentage that is based on the length of time a payment is overdue.</span></span> <span data-ttu-id="338ef-150">如果银行为不同的汇款类型（例如**征收**或**折扣**）收取不同的费用，则为各汇款类型设置单独的付款费用行。</span><span class="sxs-lookup"><span data-stu-id="338ef-150">If the bank charges different fees for different remittance types, such as **Collection** or **Discount**, set up a separate payment fee line for each remittance type.</span></span>
<span data-ttu-id="338ef-151">为银行汇款文件设置汇款费用</span><span class="sxs-lookup"><span data-stu-id="338ef-151">Set up remittance fees for bank remittance files</span></span>
------------------------------------------------

<span data-ttu-id="338ef-152">在**银行帐户**页面中，您可以设置银行向生成的每个汇款文件收取的汇款费用。</span><span class="sxs-lookup"><span data-stu-id="338ef-152">On the **Bank accounts** page, you can set up remittance fees that a bank charges for each remittance file that is generated.</span></span> <span data-ttu-id="338ef-153">在汇款已确认并且实收费用额已知时，过帐汇款费用。</span><span class="sxs-lookup"><span data-stu-id="338ef-153">The remittance fees are posted when the remittance has been confirmed and the realized fee amounts are known.</span></span> <span data-ttu-id="338ef-154">汇款费用不同于付款费用，后者将从客户收取并且附加到日志行。</span><span class="sxs-lookup"><span data-stu-id="338ef-154">Remittance fees differ from payment fees, which are collected from customers and attached to journal lines.</span></span>
<span data-ttu-id="338ef-155">设置汇票的单据版式</span><span class="sxs-lookup"><span data-stu-id="338ef-155">Set up document layouts for bills of exchange</span></span>
---------------------------------------------

<span data-ttu-id="338ef-156">在**银行帐户**页面中，单击**设置**，然后指定将为其生成打印的汇票单据的各个银行帐户所需的单据版式。</span><span class="sxs-lookup"><span data-stu-id="338ef-156">On the **Bank accounts** page, click **Set up**, and specify the document layout that is required for each bank account that you will generate printed bills of exchange documents for.</span></span>
<span data-ttu-id="338ef-157">为汇票设置客户</span><span class="sxs-lookup"><span data-stu-id="338ef-157">Set up customers for bills of exchange</span></span>
--------------------------------------

<span data-ttu-id="338ef-158">在**客户**页面中的**付款默认值**选项卡上，对于同意通过使用汇票支付的每个客户，您可以设置汇票的默认付款方式。</span><span class="sxs-lookup"><span data-stu-id="338ef-158">On the **Customers** page, for each customer who has agreed to pay by using a bill of exchange, you can set up a default method of payment for bills of exchange on the **Payment defaults** tab.</span></span>






