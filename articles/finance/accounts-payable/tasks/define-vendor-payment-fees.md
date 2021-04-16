---
title: 定义供应商付款费用
description: 设置供应商付款费用。
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0871e0889b078c08e4bcbd86bf749bcfe39463
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837247"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="44b4b-103">定义供应商付款费用</span><span class="sxs-lookup"><span data-stu-id="44b4b-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44b4b-104">设置供应商付款费用。</span><span class="sxs-lookup"><span data-stu-id="44b4b-104">Set up vendor payment fees.</span></span> <span data-ttu-id="44b4b-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="44b4b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="44b4b-106">转到“应付帐款”>“付款设置”>“付款费用”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="44b4b-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-107">Click New.</span></span>
3. <span data-ttu-id="44b4b-108">在“费用 ID”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="44b4b-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="44b4b-109">“费用 ID”应描述何时使用此费用，如“EFT_Fee”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="44b4b-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="44b4b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="44b4b-111">在“费用描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="44b4b-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="44b4b-112">添加描述以提供何时评估费用的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="44b4b-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="44b4b-113">在“支付”字段中，选择“供应商”或“分类帐”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="44b4b-114">当向贵组织支付该费用时，请使用“分类帐”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="44b4b-115">当评估供应商费用时，请使用供应商。</span><span class="sxs-lookup"><span data-stu-id="44b4b-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="44b4b-116">在费用支付位置输入一个主要帐号。</span><span class="sxs-lookup"><span data-stu-id="44b4b-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="44b4b-117">只有在费用选项中选择“分类帐”时，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="44b4b-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="44b4b-118">选择可供该费用使用的日记帐。</span><span class="sxs-lookup"><span data-stu-id="44b4b-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="44b4b-119">对于供应商付款费用，您可以选择“供应商支付”日记帐。</span><span class="sxs-lookup"><span data-stu-id="44b4b-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="44b4b-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-120">Click Save.</span></span>
10. <span data-ttu-id="44b4b-121">单击“付款费用”设置。</span><span class="sxs-lookup"><span data-stu-id="44b4b-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="44b4b-122">继续在“付款费用”设置中，定义何时将该费用设置为所选日记帐的默认项。</span><span class="sxs-lookup"><span data-stu-id="44b4b-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="44b4b-123">选择“表单”、“组”或“所有”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="44b4b-124">“表单”用于选择一个单一的银行帐户，“组”用于选择一个银行组，“所有”是将此费用设置应用于所有银行帐户。</span><span class="sxs-lookup"><span data-stu-id="44b4b-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="44b4b-125">选择某一银行组或某一银行帐户。</span><span class="sxs-lookup"><span data-stu-id="44b4b-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="44b4b-126">如果您选择的为“组”，查找操作将显示银行组；如果您选择的为“表单”，查找操作将显示银行帐号。</span><span class="sxs-lookup"><span data-stu-id="44b4b-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="44b4b-127">选择用于评估该费用时的付款方式。</span><span class="sxs-lookup"><span data-stu-id="44b4b-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="44b4b-128">选择当前付款方式的“付款说明”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="44b4b-129">电子资金转帐付款方式应遵循“付款说明”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="44b4b-130">选择费用是为百分比、金额或间隔。</span><span class="sxs-lookup"><span data-stu-id="44b4b-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="44b4b-131">输入费用的百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="44b4b-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="44b4b-132">如果“费用”为百分比，则输入百分比。</span><span class="sxs-lookup"><span data-stu-id="44b4b-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="44b4b-133">如果“费用”为金额，则输入该费用金额。</span><span class="sxs-lookup"><span data-stu-id="44b4b-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="44b4b-134">如果“费用”为间隔，则使用“间隔选项卡”定义分层费用。</span><span class="sxs-lookup"><span data-stu-id="44b4b-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="44b4b-135">在“费用币种”字段中，选择评估费用的币种。</span><span class="sxs-lookup"><span data-stu-id="44b4b-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="44b4b-136">该币种用于费用。</span><span class="sxs-lookup"><span data-stu-id="44b4b-136">This currency is for the fee.</span></span> <span data-ttu-id="44b4b-137">付款币种用于定义，基于付款的币种，应何时评估支出规则。</span><span class="sxs-lookup"><span data-stu-id="44b4b-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="44b4b-138">例如，当使用欧元付款时，您选择的银行可能会收取费用，但对于其他付款将不会评估费用。</span><span class="sxs-lookup"><span data-stu-id="44b4b-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="44b4b-139">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="44b4b-139">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]