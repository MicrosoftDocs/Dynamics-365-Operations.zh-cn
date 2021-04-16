---
title: 保函
description: 本文提供有关保函的信息。 在保函中，如果银行客户之一拖欠某人员的付款或合同，银行同意向该人员支付特定金额。
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b561f64cc08a82b349b7cd8659c1e6559c9fa15
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815804"
---
# <a name="letters-of-guarantee"></a><span data-ttu-id="f48b7-104">保函</span><span class="sxs-lookup"><span data-stu-id="f48b7-104">Letters of guarantee</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f48b7-105">本文提供有关保函的信息。</span><span class="sxs-lookup"><span data-stu-id="f48b7-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="f48b7-106">在保函中，如果银行客户之一拖欠某人员的付款或合同，银行同意向该人员支付特定金额。</span><span class="sxs-lookup"><span data-stu-id="f48b7-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="f48b7-107">信用保证书是由银行（保人）支付金钱到某人（受益人）的协议，如果银行的客户（主要的）在付款或合同默认为受益人。</span><span class="sxs-lookup"><span data-stu-id="f48b7-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="f48b7-108">保函是不可转移的。</span><span class="sxs-lookup"><span data-stu-id="f48b7-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="f48b7-109">它们仅适用于协议中指定的受益人。</span><span class="sxs-lookup"><span data-stu-id="f48b7-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="f48b7-110">依据协议持续时间，主要客户可以请求增减信用保证书的值。</span><span class="sxs-lookup"><span data-stu-id="f48b7-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="f48b7-111">若要结算信用保证书，受益人必须在到期日期之前提交原始信用保证书和通知主要客户默认的银行。</span><span class="sxs-lookup"><span data-stu-id="f48b7-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="f48b7-112">根据保函条款，银行然后由于受益人的帐户支付金额。</span><span class="sxs-lookup"><span data-stu-id="f48b7-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="f48b7-113">银行预留付款的百分比作为毛利。</span><span class="sxs-lookup"><span data-stu-id="f48b7-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="f48b7-114">百分比在协议条款审核并指定。</span><span class="sxs-lookup"><span data-stu-id="f48b7-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="f48b7-115">您可以创建代码跟踪保函的用途。</span><span class="sxs-lookup"><span data-stu-id="f48b7-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="f48b7-116">当保函取消时，您还可以指定可与保函关联的原因。</span><span class="sxs-lookup"><span data-stu-id="f48b7-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="f48b7-117">您可以在 **付款目的代码** 和 **银行原因** 页查看目的代码和银行原因。</span><span class="sxs-lookup"><span data-stu-id="f48b7-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="f48b7-118">您可以使用 **保函** 页完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="f48b7-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="f48b7-119">创建正确的分类帐条目并消除手动输入。</span><span class="sxs-lookup"><span data-stu-id="f48b7-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="f48b7-120">记录所有货币性和非货币性交易记录和跟踪保函余额。</span><span class="sxs-lookup"><span data-stu-id="f48b7-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="f48b7-121">记录和跟踪保函状态和到期。</span><span class="sxs-lookup"><span data-stu-id="f48b7-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="f48b7-122">生成列出了各个持有信用保证书的银行的报表。</span><span class="sxs-lookup"><span data-stu-id="f48b7-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="f48b7-123">下表介绍了您可以在保函中执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f48b7-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="f48b7-124">行为</span><span class="sxs-lookup"><span data-stu-id="f48b7-124">Action</span></span>              | <span data-ttu-id="f48b7-125">用途</span><span class="sxs-lookup"><span data-stu-id="f48b7-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48b7-126">提交至银行</span><span class="sxs-lookup"><span data-stu-id="f48b7-126">Submit to bank</span></span>      | <span data-ttu-id="f48b7-127">提交信用保证书申请给银行。</span><span class="sxs-lookup"><span data-stu-id="f48b7-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="f48b7-128">从银行收到</span><span class="sxs-lookup"><span data-stu-id="f48b7-128">Receive from bank</span></span>   | <span data-ttu-id="f48b7-129">在银行同意已提交的申请后，从银行托收信用保证书。</span><span class="sxs-lookup"><span data-stu-id="f48b7-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="f48b7-130">给予受益人</span><span class="sxs-lookup"><span data-stu-id="f48b7-130">Give to beneficiary</span></span> | <span data-ttu-id="f48b7-131">在您从银行收到信用保证书后，提供信用保证书给受益人。</span><span class="sxs-lookup"><span data-stu-id="f48b7-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="f48b7-132">增加值</span><span class="sxs-lookup"><span data-stu-id="f48b7-132">Increase value</span></span>      | <span data-ttu-id="f48b7-133">如果同意受益人和主要审核，则增加货币值。</span><span class="sxs-lookup"><span data-stu-id="f48b7-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="f48b7-134">减少值</span><span class="sxs-lookup"><span data-stu-id="f48b7-134">Decrease value</span></span>      | <span data-ttu-id="f48b7-135">如果同意受益人和主要审核，则减少货币值。</span><span class="sxs-lookup"><span data-stu-id="f48b7-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="f48b7-136">扩展</span><span class="sxs-lookup"><span data-stu-id="f48b7-136">Extend</span></span>              | <span data-ttu-id="f48b7-137">在您提供信用保证书给受益人后，如果需要扩展，扩展有效期。</span><span class="sxs-lookup"><span data-stu-id="f48b7-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="f48b7-138">取消</span><span class="sxs-lookup"><span data-stu-id="f48b7-138">Cancel</span></span>              | <span data-ttu-id="f48b7-139">在保函请求的用途不再适用时，取消协议。</span><span class="sxs-lookup"><span data-stu-id="f48b7-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="f48b7-140">清偿</span><span class="sxs-lookup"><span data-stu-id="f48b7-140">Liquidate</span></span>           | <span data-ttu-id="f48b7-141">在受益人显示信用保证书到银行后，清除信用保证书。</span><span class="sxs-lookup"><span data-stu-id="f48b7-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="f48b7-142">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="f48b7-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="f48b7-143">保函交易记录</span><span class="sxs-lookup"><span data-stu-id="f48b7-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="f48b7-144">设置保函的银行设施和过帐模板</span><span class="sxs-lookup"><span data-stu-id="f48b7-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]