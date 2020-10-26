---
title: 缩减天数示例
description: 缩减天数示例。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975648"
---
# <a name="reduction-days-example"></a><span data-ttu-id="b5e2e-103">缩减天数示例</span><span class="sxs-lookup"><span data-stu-id="b5e2e-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b5e2e-104">您已经为客户的维护预订创建了预订交易记录，如下表中所述。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5e2e-105">开始日期</span><span class="sxs-lookup"><span data-stu-id="b5e2e-105">From date</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-106">结束日期</span><span class="sxs-lookup"><span data-stu-id="b5e2e-106">To date</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-107">预订</span><span class="sxs-lookup"><span data-stu-id="b5e2e-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-108">预订类型</span><span class="sxs-lookup"><span data-stu-id="b5e2e-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-109">项目</span><span class="sxs-lookup"><span data-stu-id="b5e2e-109">Project</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-110">类别</span><span class="sxs-lookup"><span data-stu-id="b5e2e-110">Category</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-111">销售币种</span><span class="sxs-lookup"><span data-stu-id="b5e2e-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-112">销售价</span><span class="sxs-lookup"><span data-stu-id="b5e2e-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e2e-113">2011 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="b5e2e-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-114">2011 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b5e2e-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="b5e2e-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-116"><strong>常规</strong></span><span class="sxs-lookup"><span data-stu-id="b5e2e-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e2e-117">9013</span><span class="sxs-lookup"><span data-stu-id="b5e2e-117">9013</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b5e2e-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-119">欧元</span><span class="sxs-lookup"><span data-stu-id="b5e2e-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-120">200.00</span><span class="sxs-lookup"><span data-stu-id="b5e2e-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5e2e-121">客户报告不需要两天（3 月 10 日和 3 月 11 日）的服务覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="b5e2e-122">您同意缩减这两天的预订。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="b5e2e-123">您如下表中所述，创建类型为**缩减天数**的新交易记录。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5e2e-124">开始日期</span><span class="sxs-lookup"><span data-stu-id="b5e2e-124">From date</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-125">结束日期</span><span class="sxs-lookup"><span data-stu-id="b5e2e-125">To date</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-126">预订</span><span class="sxs-lookup"><span data-stu-id="b5e2e-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-127">预订类型</span><span class="sxs-lookup"><span data-stu-id="b5e2e-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-128">项目</span><span class="sxs-lookup"><span data-stu-id="b5e2e-128">Project</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-129">类别</span><span class="sxs-lookup"><span data-stu-id="b5e2e-129">Category</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-130">销售币种</span><span class="sxs-lookup"><span data-stu-id="b5e2e-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b5e2e-131">销售价</span><span class="sxs-lookup"><span data-stu-id="b5e2e-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e2e-132">2011 年 3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b5e2e-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-133">2011 年 3 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b5e2e-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="b5e2e-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-135"><strong>缩减天数</strong></span><span class="sxs-lookup"><span data-stu-id="b5e2e-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e2e-136">9013</span><span class="sxs-lookup"><span data-stu-id="b5e2e-136">9013</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b5e2e-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-138">欧元</span><span class="sxs-lookup"><span data-stu-id="b5e2e-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="b5e2e-139">-12.90</span><span class="sxs-lookup"><span data-stu-id="b5e2e-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5e2e-140">在给 2011 年 3 月的交易记录开票时，EUR 200 的销售价将减少 EUR 12.90。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="b5e2e-141">因此，预测交易记录的应计费金额是 EUR 187.10，并且按 EUR 187.10 的合计对这两个交易记录开票。</span><span class="sxs-lookup"><span data-stu-id="b5e2e-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5e2e-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5e2e-142">See also</span></span>

[<span data-ttu-id="b5e2e-143">缩减预订费用天数</span><span class="sxs-lookup"><span data-stu-id="b5e2e-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


