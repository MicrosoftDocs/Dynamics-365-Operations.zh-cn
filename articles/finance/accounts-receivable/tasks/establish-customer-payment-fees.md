---
title: 设定客户付款费用
description: 为客户付款创建付款费用。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6475671002379d84519df05a0198a17ac000677
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440745"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="6a04f-103">设定客户付款费用</span><span class="sxs-lookup"><span data-stu-id="6a04f-103">Establish customer payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a04f-104">为客户付款创建付款费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="6a04f-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="6a04f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6a04f-106">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 付款设置 > 付款费用**。</span><span class="sxs-lookup"><span data-stu-id="6a04f-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Payment fee**.</span></span>
2. <span data-ttu-id="6a04f-107">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6a04f-107">Click **New**.</span></span>
3. <span data-ttu-id="6a04f-108">在 **费用 ID** 字段中，输入一个“费用 ID”。</span><span class="sxs-lookup"><span data-stu-id="6a04f-108">In the **Fee ID** field, enter a Fee ID.</span></span> <span data-ttu-id="6a04f-109">“费用 ID”将显示在付款日记帐中，以便您足够清晰地了解所评估的费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="6a04f-110">在 **名称** 字段中，输入一个费用名称。</span><span class="sxs-lookup"><span data-stu-id="6a04f-110">In the **Name** field, enter a fee name.</span></span>
5. <span data-ttu-id="6a04f-111">在 **费用描述** 字段，输入一个费用描述。</span><span class="sxs-lookup"><span data-stu-id="6a04f-111">In the **Fee description** field, enter a description for the fee.</span></span>
6. <span data-ttu-id="6a04f-112">在 **费用** 字段中，选择费用是向“客户”或“会计”帐户收取。</span><span class="sxs-lookup"><span data-stu-id="6a04f-112">In the **Charge** field, select whether the fee will be charged to the Customer or a Ledger account.</span></span> <span data-ttu-id="6a04f-113">如果评估费用的是客户，则选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="6a04f-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="6a04f-114">如果费用作为您组织的一项开支进行评估，请选择“分类帐”。</span><span class="sxs-lookup"><span data-stu-id="6a04f-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="6a04f-115">对于此任务，选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="6a04f-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="6a04f-116">在 **日记帐类型** 字段中，选择可使用此付款费用的日记帐类型。</span><span class="sxs-lookup"><span data-stu-id="6a04f-116">In the **Journal type** field, select the type of journal that can use this payment fee.</span></span> <span data-ttu-id="6a04f-117">如果这些费用用于客户付款，则日记帐类型将是“客户付款”。</span><span class="sxs-lookup"><span data-stu-id="6a04f-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="6a04f-118">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6a04f-118">Click **Save**.</span></span>
9. <span data-ttu-id="6a04f-119">单击 **付款费用设置**。</span><span class="sxs-lookup"><span data-stu-id="6a04f-119">Click **Payment fee setup**.</span></span> <span data-ttu-id="6a04f-120">“付款费用设置”用于定义付款费用评估时间的条件。</span><span class="sxs-lookup"><span data-stu-id="6a04f-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="6a04f-121">例如，若银行帐户是 USMF 工序且付款方式为支票时，您可以定义将会计算费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="6a04f-122">在 **分组** 字段中，选择“表单”、“组”或“所有物料”以定义评估此费用的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="6a04f-122">In the **Groupings** field, select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span> <span data-ttu-id="6a04f-123">若您选择“全部”，则所有的银行帐户都将评估此项费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="6a04f-124">若您选择“表单”，将只有您所选的银行帐户可以评估此项费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="6a04f-125">如果选择了“组”，则只有所选银行组中的银行帐户才可评估此费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="6a04f-126">在 **银行关系** 字段中，选择银行组或银行帐户。</span><span class="sxs-lookup"><span data-stu-id="6a04f-126">In the **Bank relation** field, select either a bank group or a bank account.</span></span> <span data-ttu-id="6a04f-127">如果您选择了“表单”，则查找操作将显示银行帐户。</span><span class="sxs-lookup"><span data-stu-id="6a04f-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="6a04f-128">如果您选择了“组”，则查找操作将显示银行组。</span><span class="sxs-lookup"><span data-stu-id="6a04f-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="6a04f-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6a04f-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6a04f-130">在 **付款方式** 字段中，选择用于估计此费用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="6a04f-130">In the **Method of payment** field, select the Method of payment for which this fee will be assessed.</span></span> <span data-ttu-id="6a04f-131">例如，如果客户使用支票付款，而不是电子付款，您需要向您的客户评估费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="6a04f-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6a04f-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6a04f-133">如果相关，在 **付款币种** 字段中输入一种付款币种。</span><span class="sxs-lookup"><span data-stu-id="6a04f-133">If relevant, in the **Payment currency** field, enter a payment currency.</span></span> <span data-ttu-id="6a04f-134">付款币种用于是否评估费用的附加条件。</span><span class="sxs-lookup"><span data-stu-id="6a04f-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="6a04f-135">例如，通常情况下采用欧元交易，所以当贵银行收取以 USD 为单位的币种付款时，便会收取附加费用。</span><span class="sxs-lookup"><span data-stu-id="6a04f-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="6a04f-136">选择费用是否为百分比、金额或间隔。</span><span class="sxs-lookup"><span data-stu-id="6a04f-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="6a04f-137">在 **百分比/金额** 字段中，输入费用的百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="6a04f-137">In the **Percentage/Amount field**, enter either percentage or amount of the fee.</span></span> <span data-ttu-id="6a04f-138">如果“百分比/金额”字段为“百分比”，则在该处输入的值将是一个百分比。</span><span class="sxs-lookup"><span data-stu-id="6a04f-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="6a04f-139">如果“百分比/金额”字段为“金额”，则在该处输入的值应为金额。</span><span class="sxs-lookup"><span data-stu-id="6a04f-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="6a04f-140">如果“百分比/金额”字段为“间隔”，则使用“间隔选项卡”定义等级。</span><span class="sxs-lookup"><span data-stu-id="6a04f-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="6a04f-141">在 **费用币种** 字段中，选择费用的币种。</span><span class="sxs-lookup"><span data-stu-id="6a04f-141">In the **Fee currency** field, select the currency of the fee.</span></span> <span data-ttu-id="6a04f-142">此为费用支付币种。</span><span class="sxs-lookup"><span data-stu-id="6a04f-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="6a04f-143">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6a04f-143">Click **Save**.</span></span>

