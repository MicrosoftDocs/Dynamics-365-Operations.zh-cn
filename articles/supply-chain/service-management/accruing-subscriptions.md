---
title: 应计预订
description: 使用服务预订，您可以在费用交易记录开票日期后的期间中手动计入收入。
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebd65655db56ee1169f24dbc79fbfb5130f06a5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978813"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="51db9-103">应计预订</span><span class="sxs-lookup"><span data-stu-id="51db9-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="51db9-104">使用服务预订，您可以在费用交易记录开票日期后的期间中手动计入收入。</span><span class="sxs-lookup"><span data-stu-id="51db9-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="51db9-105">为您为预订费用设置的发票期间创建应计期间，并且应计期间基于预订的期间代码。</span><span class="sxs-lookup"><span data-stu-id="51db9-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="51db9-106">您可以计入或冲销应计收入。</span><span class="sxs-lookup"><span data-stu-id="51db9-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="51db9-107">贷方金额冲销应计</span><span class="sxs-lookup"><span data-stu-id="51db9-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="51db9-108">如果您贷记已开票的预订金额，则可以使用两种方法冲销应计金额：</span><span class="sxs-lookup"><span data-stu-id="51db9-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="51db9-109">在创建交易记录的贷方通知单方案之前，您可以逐个冲销每个应计收入交易记录。</span><span class="sxs-lookup"><span data-stu-id="51db9-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="51db9-110">此方法是手动方法。</span><span class="sxs-lookup"><span data-stu-id="51db9-110">This is the manual method.</span></span> <span data-ttu-id="51db9-111">手动</span><span class="sxs-lookup"><span data-stu-id="51db9-111">(manual)</span></span>

  - <span data-ttu-id="51db9-112">您可以具有在过帐贷方通知单的日期或在应计的原始过帐日期冲销的应计金额。</span><span class="sxs-lookup"><span data-stu-id="51db9-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="51db9-113">有关详细信息，请参阅[预订参数（窗体）](https://technet.microsoft.com/library/aa619615.aspx)。</span><span class="sxs-lookup"><span data-stu-id="51db9-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="51db9-114">设置需求</span><span class="sxs-lookup"><span data-stu-id="51db9-114">Setup requirements</span></span>

<span data-ttu-id="51db9-115">若要应计收入，请确保满足以下数据要求：</span><span class="sxs-lookup"><span data-stu-id="51db9-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="51db9-116">帐户设置</span><span class="sxs-lookup"><span data-stu-id="51db9-116">Account setup</span></span>

<span data-ttu-id="51db9-117">必须在**项目**模块中设置 **WIP - 预订**和**应计收入 - 预订**科目。</span><span class="sxs-lookup"><span data-stu-id="51db9-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="51db9-118">在您过帐应计收入时，**WIP - 预订**科目使用应计金额借记，而**应计收入 - 预订**科目使用应计金额贷记。</span><span class="sxs-lookup"><span data-stu-id="51db9-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="51db9-119">为预订收入应计设置帐户</span><span class="sxs-lookup"><span data-stu-id="51db9-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="51db9-120">单击**项目管理与核算** \> **设置** \> **过帐** \> **分类帐记帐设置**。</span><span class="sxs-lookup"><span data-stu-id="51db9-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="51db9-121">单击**收入科目**选项卡中，选择 **WIP - 预订**或**应计收入 - 预订**设置科目。</span><span class="sxs-lookup"><span data-stu-id="51db9-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="51db9-122">预订组设置</span><span class="sxs-lookup"><span data-stu-id="51db9-122">Subscription group setup</span></span>

<span data-ttu-id="51db9-123">为了能够为预订应计收入，必须选中**应计收入**复选框。</span><span class="sxs-lookup"><span data-stu-id="51db9-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="51db9-124">这在附加到预订组的**预订组**窗体中找到。</span><span class="sxs-lookup"><span data-stu-id="51db9-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="51db9-125">单击**服务管理** \> **设置** \> **服务预订** \> **预订组**。</span><span class="sxs-lookup"><span data-stu-id="51db9-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="51db9-126">针对预订组启用收入应计</span><span class="sxs-lookup"><span data-stu-id="51db9-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="51db9-127">单击**服务管理** \> **设置** \> **服务预订** \> **预订组**。</span><span class="sxs-lookup"><span data-stu-id="51db9-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="51db9-128">期间</span><span class="sxs-lookup"><span data-stu-id="51db9-128">Periods</span></span>

<span data-ttu-id="51db9-129">您必须设置开票期间代码。</span><span class="sxs-lookup"><span data-stu-id="51db9-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="51db9-130">除非您想在您用于开票的同一时间间隔内应计收入，否则，还必须设置应计期间。</span><span class="sxs-lookup"><span data-stu-id="51db9-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="51db9-131">下表提供为每个开票期设置应计期间的概览:</span><span class="sxs-lookup"><span data-stu-id="51db9-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51db9-132">开票期</span><span class="sxs-lookup"><span data-stu-id="51db9-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="51db9-133">应计期间</span><span class="sxs-lookup"><span data-stu-id="51db9-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51db9-134"><strong>年</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="51db9-135"><strong>年</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-136"><strong>季度</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-137"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-138"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51db9-139"><strong>季度</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="51db9-140"><strong>季度</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-141"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-142"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51db9-143"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="51db9-144"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="51db9-145"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51db9-146"><strong>周</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="51db9-147"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51db9-148"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="51db9-149"><strong>天</strong></span><span class="sxs-lookup"><span data-stu-id="51db9-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="51db9-150">设置开票期间是整个预订组设置的一部分。</span><span class="sxs-lookup"><span data-stu-id="51db9-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="51db9-151">您可以决定是否也要设置预订组的应计期间。</span><span class="sxs-lookup"><span data-stu-id="51db9-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="51db9-152">如果您设置预订组的应计期间，在**期间代码**字段提供此期间。</span><span class="sxs-lookup"><span data-stu-id="51db9-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="51db9-153">当您应计预订收入时，此字段在**应计预订收入**窗体中找到。</span><span class="sxs-lookup"><span data-stu-id="51db9-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="51db9-154">但是，应计期间是与预订组有关的可选信息。</span><span class="sxs-lookup"><span data-stu-id="51db9-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="51db9-155">可使用以下路径打开<STRONG>应计预订收入</STRONG>窗体。</span><span class="sxs-lookup"><span data-stu-id="51db9-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="51db9-156">单击<STRONG>服务管理</STRONG> &gt; <STRONG>定期</STRONG> &gt; <STRONG>服务预订</STRONG> &gt; <STRONG>应计预订收入</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="51db9-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="51db9-157">交易</span><span class="sxs-lookup"><span data-stu-id="51db9-157">Transactions</span></span>

<span data-ttu-id="51db9-158">在您过帐应计收入时，您可以控制创建分录的数量。</span><span class="sxs-lookup"><span data-stu-id="51db9-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="51db9-159">在预订时，如果分类帐交易记录应创建为合计或每行，则定义。</span><span class="sxs-lookup"><span data-stu-id="51db9-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="51db9-160">指定要为应计交易记录显示的过帐明细的级别</span><span class="sxs-lookup"><span data-stu-id="51db9-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="51db9-161">单击**项目管理与核算** \> **设置** \> **项目管理与核算参数**。</span><span class="sxs-lookup"><span data-stu-id="51db9-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="51db9-162">在**财务**选项卡的**发票**字段中，选择**总计**或**行**。</span><span class="sxs-lookup"><span data-stu-id="51db9-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="51db9-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="51db9-163">See also</span></span>

[<span data-ttu-id="51db9-164">应计预订收入</span><span class="sxs-lookup"><span data-stu-id="51db9-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


