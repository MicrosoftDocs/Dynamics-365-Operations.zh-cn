---
title: 采取的折扣大于供应商付款的计算折扣
description: 本文向您展示为超过发票上最初可用折扣的金额执行现金折扣的情况。 如果组织履行协议，供应商支付发票上的较小金额，可能发生此情况。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843257"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="390c8-104">采取的折扣大于供应商付款的计算折扣</span><span class="sxs-lookup"><span data-stu-id="390c8-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="390c8-105">本文向您展示为超过发票上最初可用折扣的金额执行现金折扣的情况。</span><span class="sxs-lookup"><span data-stu-id="390c8-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="390c8-106">如果组织履行协议，供应商支付发票上的较小金额，可能发生此情况。</span><span class="sxs-lookup"><span data-stu-id="390c8-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="390c8-107">如果七天内支付发票，供应商 3051 将给予 Fabrikam 4% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="390c8-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="390c8-108">April 在 6 月 29 日为发票输入 1,000.00。</span><span class="sxs-lookup"><span data-stu-id="390c8-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="390c8-109">供应商让 April 执行对此发票可用的 60.00 的折扣，而不是默认折扣 40.00。</span><span class="sxs-lookup"><span data-stu-id="390c8-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="390c8-110">通过使用应付账款付款日记帐，April 记录一次性付款。</span><span class="sxs-lookup"><span data-stu-id="390c8-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="390c8-111">她为付款输入供应商，然后打开**结算交易记录**页。</span><span class="sxs-lookup"><span data-stu-id="390c8-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="390c8-112">她标记发票并在**现金折扣金额**字段中将值更改为 **60.00**。</span><span class="sxs-lookup"><span data-stu-id="390c8-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="390c8-113">标记</span><span class="sxs-lookup"><span data-stu-id="390c8-113">Mark</span></span>     | <span data-ttu-id="390c8-114">使用现金折扣</span><span class="sxs-lookup"><span data-stu-id="390c8-114">Use cash discount</span></span> | <span data-ttu-id="390c8-115">凭证</span><span class="sxs-lookup"><span data-stu-id="390c8-115">Voucher</span></span>   | <span data-ttu-id="390c8-116">帐户</span><span class="sxs-lookup"><span data-stu-id="390c8-116">Account</span></span> | <span data-ttu-id="390c8-117">日期</span><span class="sxs-lookup"><span data-stu-id="390c8-117">Date</span></span>      | <span data-ttu-id="390c8-118">到期日期</span><span class="sxs-lookup"><span data-stu-id="390c8-118">Due date</span></span>  | <span data-ttu-id="390c8-119">开票</span><span class="sxs-lookup"><span data-stu-id="390c8-119">Invoice</span></span> | <span data-ttu-id="390c8-120">交易记录币种金额</span><span class="sxs-lookup"><span data-stu-id="390c8-120">Amount in transaction currency</span></span> | <span data-ttu-id="390c8-121">货币</span><span class="sxs-lookup"><span data-stu-id="390c8-121">Currency</span></span> | <span data-ttu-id="390c8-122">要结算的金额</span><span class="sxs-lookup"><span data-stu-id="390c8-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="390c8-123">已选择</span><span class="sxs-lookup"><span data-stu-id="390c8-123">Selected</span></span> | <span data-ttu-id="390c8-124">标准</span><span class="sxs-lookup"><span data-stu-id="390c8-124">Normal</span></span>            | <span data-ttu-id="390c8-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="390c8-125">Inv-10040</span></span> | <span data-ttu-id="390c8-126">3051</span><span class="sxs-lookup"><span data-stu-id="390c8-126">3051</span></span>    | <span data-ttu-id="390c8-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="390c8-127">6/29/2015</span></span> | <span data-ttu-id="390c8-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="390c8-128">7/29/2015</span></span> | <span data-ttu-id="390c8-129">10040</span><span class="sxs-lookup"><span data-stu-id="390c8-129">10040</span></span>   | <span data-ttu-id="390c8-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="390c8-130">1,000.00</span></span>                       | <span data-ttu-id="390c8-131">美元</span><span class="sxs-lookup"><span data-stu-id="390c8-131">USD</span></span>      | <span data-ttu-id="390c8-132">940.00</span><span class="sxs-lookup"><span data-stu-id="390c8-132">940.00</span></span>           |

<span data-ttu-id="390c8-133">折扣信息显示在**结算交易记录**页的底部。</span><span class="sxs-lookup"><span data-stu-id="390c8-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="390c8-134">现金折扣日期</span><span class="sxs-lookup"><span data-stu-id="390c8-134">Cash discount date</span></span>           | <span data-ttu-id="390c8-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="390c8-135">7/12/2015</span></span> |
| <span data-ttu-id="390c8-136">现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="390c8-136">Cash discount amount</span></span>         | <span data-ttu-id="390c8-137">60.00</span><span class="sxs-lookup"><span data-stu-id="390c8-137">60.00</span></span>     |
| <span data-ttu-id="390c8-138">使用现金折扣</span><span class="sxs-lookup"><span data-stu-id="390c8-138">Use cash discount</span></span>            | <span data-ttu-id="390c8-139">标准</span><span class="sxs-lookup"><span data-stu-id="390c8-139">Normal</span></span>    |
| <span data-ttu-id="390c8-140">提取了现金折扣</span><span class="sxs-lookup"><span data-stu-id="390c8-140">Cash discount taken</span></span>          | <span data-ttu-id="390c8-141">0.00</span><span class="sxs-lookup"><span data-stu-id="390c8-141">0.00</span></span>      |
| <span data-ttu-id="390c8-142">要提取的现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="390c8-142">Cash discount amount to take</span></span> | <span data-ttu-id="390c8-143">60.00</span><span class="sxs-lookup"><span data-stu-id="390c8-143">60.00</span></span>     |

<span data-ttu-id="390c8-144">April 过帐付款日志。</span><span class="sxs-lookup"><span data-stu-id="390c8-144">April posts the payment journal.</span></span> <span data-ttu-id="390c8-145">使用付款 940.00 和 60.00 折扣完全结算发票。</span><span class="sxs-lookup"><span data-stu-id="390c8-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



