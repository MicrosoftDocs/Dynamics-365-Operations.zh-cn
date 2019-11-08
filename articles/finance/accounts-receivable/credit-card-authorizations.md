---
title: 信用卡设置、授权和捕获
description: 本文提供 Microsoft Dynamics 365 Finance 中的信用卡授权的概览。 其中包含有关如何设置付款服务，添加信用卡到销售订单和取消授权的信息。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de35934e8bdb160f68f68dab118997d0141bf29
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570394"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="430f2-104">信用卡设置、授权和捕获</span><span class="sxs-lookup"><span data-stu-id="430f2-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="430f2-105">本文提供 Microsoft Dynamics 365 Finance 中的信用卡授权的概览。</span><span class="sxs-lookup"><span data-stu-id="430f2-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="430f2-106">其中包含有关如何设置付款服务，添加信用卡到销售订单和取消授权的信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="430f2-107">设置信用卡付款服务</span><span class="sxs-lookup"><span data-stu-id="430f2-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="430f2-108">若要使用信用卡，您必须设置并激活付款服务页的付款服务。</span><span class="sxs-lookup"><span data-stu-id="430f2-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="430f2-109">付款服务充当您的法人和处理客户信用卡费用的银行之间的桥梁。</span><span class="sxs-lookup"><span data-stu-id="430f2-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="430f2-110">您必须使用在“付款连接器”字段中列出的信用卡提供商，并在该提供商那里设置帐户。</span><span class="sxs-lookup"><span data-stu-id="430f2-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="430f2-111">然后必须在“付款服务”页设置其他选项，在“信用卡类型”页上设置信用卡类型为 American Express、Discover、MasterCard 和 Discover，并激活提供商为默认提供商。</span><span class="sxs-lookup"><span data-stu-id="430f2-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="430f2-112">您还必须按照下面的步骤完成您的设置：</span><span class="sxs-lookup"><span data-stu-id="430f2-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="430f2-113">在“应收账款参数”页，指定用于信用卡授权的参数。</span><span class="sxs-lookup"><span data-stu-id="430f2-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="430f2-114">在“付款期限”页，设置信用卡的付款期限。</span><span class="sxs-lookup"><span data-stu-id="430f2-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="430f2-115">在“付款类型”字段中，选择“信用卡”。</span><span class="sxs-lookup"><span data-stu-id="430f2-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="430f2-116">在“客户信用卡”页，输入客户的信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="430f2-117">添加新的信用卡</span><span class="sxs-lookup"><span data-stu-id="430f2-117">Adding a new credit card</span></span>
<span data-ttu-id="430f2-118">通过使用“客户”、“设置”、“信用卡”在“客户”页创建新的信用卡记录。</span><span class="sxs-lookup"><span data-stu-id="430f2-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="430f2-119">在“销售订单”页输入销售订单时，还可以通过使用“管理”、“客户”、“信用卡”、“登记”创建信用卡记录。</span><span class="sxs-lookup"><span data-stu-id="430f2-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="430f2-120">将信用卡添加到销售订单</span><span class="sxs-lookup"><span data-stu-id="430f2-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="430f2-121">您可以添加信用卡到销售订单，方法是通过在“销售订单”页的“价格和折扣”快速选项卡上的信用卡查找中选择信用卡。</span><span class="sxs-lookup"><span data-stu-id="430f2-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="430f2-122">若要开始授权流程，在“操作窗格”，在“管理”选项卡上，选择“信用卡和授权”。</span><span class="sxs-lookup"><span data-stu-id="430f2-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="430f2-123">授权信用卡</span><span class="sxs-lookup"><span data-stu-id="430f2-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="430f2-124">在对某一信用卡进行授权时，验证信用卡号和持卡人的名字，并且确认可用的信用卡余额。</span><span class="sxs-lookup"><span data-stu-id="430f2-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="430f2-125">或者，验证卡验证值和持卡人的地址。</span><span class="sxs-lookup"><span data-stu-id="430f2-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="430f2-126">然后，从该客户的可用信用卡余额中减去发票金额。</span><span class="sxs-lookup"><span data-stu-id="430f2-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="430f2-127">付款服务将发送信用卡已核准或拒绝的信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="430f2-128">在给销售订单开票时，按发票金额对信用卡计费（已捕获）。</span><span class="sxs-lookup"><span data-stu-id="430f2-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="430f2-129">卡验证值</span><span class="sxs-lookup"><span data-stu-id="430f2-129">Card verification value</span></span>

<span data-ttu-id="430f2-130">您可以要求卡验证值，此值有时候称作卡的安全代码。</span><span class="sxs-lookup"><span data-stu-id="430f2-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="430f2-131">对于美国运通，这是一个四位数值。</span><span class="sxs-lookup"><span data-stu-id="430f2-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="430f2-132">对于 Discover、MasterCard 和 Visa，它是一个三位数字的值。</span><span class="sxs-lookup"><span data-stu-id="430f2-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="430f2-133">地址验证</span><span class="sxs-lookup"><span data-stu-id="430f2-133">Address verification</span></span>

<span data-ttu-id="430f2-134">地址验证信息始终发送到付款提供商。</span><span class="sxs-lookup"><span data-stu-id="430f2-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="430f2-135">您可以决定交易记录需要的信息量以接受交易记录。</span><span class="sxs-lookup"><span data-stu-id="430f2-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="430f2-136">请确保向您的提供商确定其是否可以接受此信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="430f2-137">这是地址验证的选项：</span><span class="sxs-lookup"><span data-stu-id="430f2-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="430f2-138">**始终接受交易记录** – 无论地址验证结果，接受交易记录。</span><span class="sxs-lookup"><span data-stu-id="430f2-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="430f2-139">**帐户持有人** – 将交易记录的持卡人的姓名与公司信息进行比较。</span><span class="sxs-lookup"><span data-stu-id="430f2-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="430f2-140">**帐单地址** – 将交易记录的持卡人姓名和帐单地址与信用卡公司的信息进行比较。</span><span class="sxs-lookup"><span data-stu-id="430f2-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="430f2-141">**帐单邮政编码** – 将交易记录的持卡人姓名、帐单地址和邮政编码与信用卡公司的信息进行比较。</span><span class="sxs-lookup"><span data-stu-id="430f2-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="430f2-142">数据支持</span><span class="sxs-lookup"><span data-stu-id="430f2-142">Data support</span></span>
<span data-ttu-id="430f2-143">对于支持的每个信用卡类型，您可以指定数据支持的级别。</span><span class="sxs-lookup"><span data-stu-id="430f2-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="430f2-144">级别控制将交易记录的多少信息转移到付款服务。</span><span class="sxs-lookup"><span data-stu-id="430f2-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="430f2-145">请确保向您的提供商确定其是否可以提供此信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="430f2-146">这是数据支持级别的选项：</span><span class="sxs-lookup"><span data-stu-id="430f2-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="430f2-147">**级别 1** – 转移交易记录日期、交易记录金额和描述。</span><span class="sxs-lookup"><span data-stu-id="430f2-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="430f2-148">**级别 2** – 转移所有级别 1 信息，以及装运和商人地址和税务信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="430f2-149">**级别 3** – 转移所有级别 2 信息，以及订单行信息。</span><span class="sxs-lookup"><span data-stu-id="430f2-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="430f2-150">部分付款</span><span class="sxs-lookup"><span data-stu-id="430f2-150">Partial payments</span></span>
<span data-ttu-id="430f2-151">如果发送部分订单，捕获部分订单的金额，并且授权关闭，该授权针对整个订单的金额</span><span class="sxs-lookup"><span data-stu-id="430f2-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="430f2-152">然后，新的权限针对尚未装运订单的余额提交。</span><span class="sxs-lookup"><span data-stu-id="430f2-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="430f2-153">取消授权</span><span class="sxs-lookup"><span data-stu-id="430f2-153">Voiding an authorization</span></span>
<span data-ttu-id="430f2-154">若要取消信用卡授权，您可以将付款方法更改为没有“信用卡类型”的其他方法。</span><span class="sxs-lookup"><span data-stu-id="430f2-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>





