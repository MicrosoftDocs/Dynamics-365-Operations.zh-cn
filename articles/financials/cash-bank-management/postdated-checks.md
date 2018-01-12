---
title: "远期支票"
description: "本文提供有关 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中远期支票的支持的信息。 远期支票是签发用于在将来时间进行付款和收款的支票。 因此，支票在指定日期前不能兑现。"
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 68d3029f750e2f2feb5912bbb64bfe105b9d9718
ms.contentlocale: zh-cn
ms.lasthandoff: 01/12/2018

---

# <a name="postdated-checks"></a><span data-ttu-id="b58b8-105">远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b58b8-106">本文提供有关 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中远期支票的支持的信息。</span><span class="sxs-lookup"><span data-stu-id="b58b8-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="b58b8-107">远期支票是签发用于在将来时间进行付款和收款的支票。</span><span class="sxs-lookup"><span data-stu-id="b58b8-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="b58b8-108">因此，支票在指定日期前不能兑现。</span><span class="sxs-lookup"><span data-stu-id="b58b8-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="b58b8-109">Microsoft Dynamics 365 for Finance and Operations 支持应收账款和应付账款中远期支票的完整管理周期，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="b58b8-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b58b8-110">方案</span><span class="sxs-lookup"><span data-stu-id="b58b8-110">Scenario</span></span></th>
<th><span data-ttu-id="b58b8-111">明细</span><span class="sxs-lookup"><span data-stu-id="b58b8-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b58b8-112">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="b58b8-113">您必须设置新的付款方式，并为已签发支票、收到的支票和预缴税金的结算帐户指定付款流程。</span><span class="sxs-lookup"><span data-stu-id="b58b8-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b58b8-114">为供应商登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="b58b8-115">登记您向供应商签发的远期支票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b58b8-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="b58b8-116">在过帐付款时，识别供应商负债，不过，银行帐户不是贷方。</span><span class="sxs-lookup"><span data-stu-id="b58b8-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="b58b8-117">相反，结算帐户用于此目的。</span><span class="sxs-lookup"><span data-stu-id="b58b8-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b58b8-118">为客户登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="b58b8-119">登记您从客户处接收的远期支票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b58b8-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="b58b8-120">在过帐付款时，应收客户是贷方，但银行帐户不是借方。</span><span class="sxs-lookup"><span data-stu-id="b58b8-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="b58b8-121">相反，结算帐户用于此目的。</span><span class="sxs-lookup"><span data-stu-id="b58b8-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b58b8-122">为客户或供应商登记和过帐更换远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="b58b8-123">如果您给供应商或从客户处收到的原始支票已丢失或损坏，您可以签发替代远期支票给供应商。</span><span class="sxs-lookup"><span data-stu-id="b58b8-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="b58b8-124">当您登记该支票的详细信息后，提供参考给该原始支票并指示新支票是原始支票的替代。</span><span class="sxs-lookup"><span data-stu-id="b58b8-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="b58b8-125">您也可以过账替代支票。</span><span class="sxs-lookup"><span data-stu-id="b58b8-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b58b8-126">将客户远期支票转移到供应商</span><span class="sxs-lookup"><span data-stu-id="b58b8-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="b58b8-127">当您从客户处接收了一张远期发票时，您可以将该支票作为付款转移到供应商。</span><span class="sxs-lookup"><span data-stu-id="b58b8-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b58b8-128">结算客户或供应商的远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="b58b8-129">当支票最后到期时，结算过帐到客户或供应商的过渡帐户的远期支票。</span><span class="sxs-lookup"><span data-stu-id="b58b8-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="b58b8-130">在结算支票时，银行根据之前使用的结算帐户为最后借方或贷方。</span><span class="sxs-lookup"><span data-stu-id="b58b8-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b58b8-131">取消供应商的远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="b58b8-132">您可以在以下情况下取消已过帐的远期支票: - 银行退回了支票。</span><span class="sxs-lookup"><span data-stu-id="b58b8-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="b58b8-133">- 该支票被应用于不正确的发票。</span><span class="sxs-lookup"><span data-stu-id="b58b8-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="b58b8-134">- 现金支付是针对发票而存在的。</span><span class="sxs-lookup"><span data-stu-id="b58b8-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b58b8-135">停止远期支票付款</span><span class="sxs-lookup"><span data-stu-id="b58b8-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="b58b8-136">您可以停止对签发给供应商的远期支票的付款，原因可以是资金不足、与供应商的协议更改、供应商提供残次货物或货物返还给了供应商等。</span><span class="sxs-lookup"><span data-stu-id="b58b8-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="b58b8-137">您只能停止未清算的支票上的付款。</span><span class="sxs-lookup"><span data-stu-id="b58b8-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b58b8-138">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="b58b8-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="b58b8-139">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="b58b8-140">为客户登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="b58b8-141">结算客户的远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="b58b8-142">为供应商登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="b58b8-143">结算供应商的远期支票</span><span class="sxs-lookup"><span data-stu-id="b58b8-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




