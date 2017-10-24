--- 
title: "设置增值税分类帐记帐组"
description: "将计算销售税，并过帐到分类帐过帐组中指定的主科目。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10386719e925e53e26c7e547b29a72873a4d000d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a><span data-ttu-id="91d79-103">设置增值税分类帐记帐组</span><span class="sxs-lookup"><span data-stu-id="91d79-103">Set up ledger posting groups for sales tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91d79-104">将计算销售税，并过帐到分类帐过帐组中指定的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-104">Sales tax is calculated and posted to main accounts that are specified in the Ledger posting groups.</span></span> <span data-ttu-id="91d79-105">分类帐过帐组将分配给每个销售税代码。</span><span class="sxs-lookup"><span data-stu-id="91d79-105">Ledger posting groups are attached to each sales tax code.</span></span> <span data-ttu-id="91d79-106">您可以为每个销售税代码设置单独的分类帐过帐组，将一个分类帐过帐组用于所有销售税代码，或者可以将多个分类帐过帐组分配给销售税代码。</span><span class="sxs-lookup"><span data-stu-id="91d79-106">You can set up individual ledger posting groups for each sales tax code, use one ledger posting group for all sales tax codes or assign multiple ledger posting groups to the sales tax codes.</span></span> <span data-ttu-id="91d79-107">此记录使用 DEMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="91d79-107">This recording uses the DEMF demo company.</span></span> 

1. <span data-ttu-id="91d79-108">转到“纳税”>“设置”>“销售税”>“分类帐过帐组”。</span><span class="sxs-lookup"><span data-stu-id="91d79-108">Go to Tax > Setup > Sales tax > Ledger posting groups.</span></span>
2. <span data-ttu-id="91d79-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91d79-109">Click New.</span></span>
3. <span data-ttu-id="91d79-110">在“分类帐过帐组”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d79-110">In the Ledger posting group field, type a value.</span></span>
4. <span data-ttu-id="91d79-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d79-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="91d79-112">在“应付销售税”字段中，选择应付给税务主管机构的输出销售税的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-112">In the Sales tax payable field, select the main account for outgoing sales taxes that are payable to the tax authority.</span></span>
    * <span data-ttu-id="91d79-113">在您销售应纳税商品和服务时，将代表税务主管机构收取销售税。</span><span class="sxs-lookup"><span data-stu-id="91d79-113">Sales taxes are collected on behalf of the tax authority when you sell taxable goods and services.</span></span>  
6. <span data-ttu-id="91d79-114">在“应收销售税”字段中，选择可从税务主管机构接收的所得税的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-114">In the Sales tax receivable filed, select the main account for incoming taxes that are received from the tax authority.</span></span>
    * <span data-ttu-id="91d79-115">在您购买应纳税商品和服务时，供应商代表税务主管机构收取税费。</span><span class="sxs-lookup"><span data-stu-id="91d79-115">Vendors collect taxes on behalf of the tax authority when you buy taxable goods and services.</span></span> <span data-ttu-id="91d79-116">如果在总帐参数页面选择“应用销售税纳税规则”选项，此字段不可用。</span><span class="sxs-lookup"><span data-stu-id="91d79-116">This field is not available if the Apply sales tax taxation rules option is selected in the General ledger parameters page.</span></span> <span data-ttu-id="91d79-117">而是将支付给供应商的销售税作为采购项借记到相同的帐户。</span><span class="sxs-lookup"><span data-stu-id="91d79-117">Instead, sales taxes that are paid to vendors are debited to the same account as the purchase.</span></span>   
7. <span data-ttu-id="91d79-118">在“销项税费用”字段，选择作为欧盟反向收费 GST/HST，供应商未向税务主管机构申报或报告的可扣除销项税过帐的主计科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-118">In the Use tax expense field, select  the main account for posting deductible Use taxes that are not claimed or reported to the tax authority by vendors as part of EU reverse charge GST/HST.</span></span>
    * <span data-ttu-id="91d79-119">需要为在交易记录中使用的销售税组的销售税代码选择“销项税”选项。</span><span class="sxs-lookup"><span data-stu-id="91d79-119">The Use tax option needs to be selected for the Sales tax code in the Sales tax group that is used in the transaction.</span></span>  <span data-ttu-id="91d79-120">如果在总帐参数页面选择“应用销售税纳税规则”选项，此字段不可用。</span><span class="sxs-lookup"><span data-stu-id="91d79-120">This field is not be available if the Apply sales tax taxation rules option is selected in the General ledger parameters page.</span></span>   
8. <span data-ttu-id="91d79-121">在“应付销项税”字段中，选择应付给税务主管机构的所得销项税过帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-121">In the Use tax payable field, select the main account for posting incoming Use taxes that are payable to tax authorities.</span></span>
    * <span data-ttu-id="91d79-122">需要在销售税组中的销售税代码中选择“销项税”选项，以过帐销项税。</span><span class="sxs-lookup"><span data-stu-id="91d79-122">The Use tax option needs to be selected in the Sales tax code in the Sales tax group to post Use tax.</span></span> <span data-ttu-id="91d79-123">如果在总帐参数中选择“应用销售税纳税规则”选项，抵销项过帐到交易记录的费用帐户。</span><span class="sxs-lookup"><span data-stu-id="91d79-123">If Apply sales tax taxation rules option is selected in General ledger parameters, the offset is posted to the transaction’s expense account.</span></span>   
9. <span data-ttu-id="91d79-124">在“结算帐户”字段中，选择将过帐应付销项税指定的会计科目的净余额以及“应收销售税”字段的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-124">In the Settlement account field, select the main account  that the net balance of the ledger accounts specified in the Use tax payable and Sales tax receivable fields will be posted.</span></span>
    * <span data-ttu-id="91d79-125">在运行销售税结算和过帐时，将创建余额。</span><span class="sxs-lookup"><span data-stu-id="91d79-125">The balance will be created when the Sales tax settle and post job is ran.</span></span>  <span data-ttu-id="91d79-126">如果结算期间的税务主管机构与供应商帐户相关，余额将过帐到供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="91d79-126">If the Tax authority for the settlement period is associated with a vendor account, the balance is posted to the vendor account instead.</span></span>   
10. <span data-ttu-id="91d79-127">在“供应商现金折扣”字段中，选择主科目，以过帐与此分类帐记帐组相关的销售税代码的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="91d79-127">In the Vendor cash discount field, select the main account to post cash discount for Sales tax codes associated with this Ledger posting group.</span></span>
    * <span data-ttu-id="91d79-128">此为可选项，如果未输入科目，将使用在现金折扣代码的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-128">This is optional and if no account is entered,  the main account on Cash discount codes will be used.</span></span> <span data-ttu-id="91d79-129">如果使用销售税组中的“冲销现金折扣的销售税”选项，每个分类帐过帐组使用不同的帐户会很有帮助。</span><span class="sxs-lookup"><span data-stu-id="91d79-129">It can be useful to use different accounts per Ledger posting group if using the reverse sales tax on cash discount option on Sales tax groups.</span></span>  
11. <span data-ttu-id="91d79-130">在“客户折扣”字段中，选择主科目，以过帐与此分类帐过帐组相关的销售税代码的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="91d79-130">In the Customer case discount field, select the main account to post cash discount for Sales tax codes associated with this Ledger posting group.</span></span>
    * <span data-ttu-id="91d79-131">此为可选项，如果未输入科目，将使用现金折扣代码的主科目。</span><span class="sxs-lookup"><span data-stu-id="91d79-131">This is optional and if no account is entered, the main account on the Cash discount codes will be used.</span></span> <span data-ttu-id="91d79-132">如果使用销售税组中的“冲销现金折扣的销售税”选项，每个分类帐过帐组使用不同的帐户会很有帮助。</span><span class="sxs-lookup"><span data-stu-id="91d79-132">It can be useful to use different accounts per Ledger posting group if using the reverse sales tax on cash discount option on Sales tax groups.</span></span>  
12. <span data-ttu-id="91d79-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="91d79-133">Click Save.</span></span>

