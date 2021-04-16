---
title: 预订销售价
description: 在您创建某一预订时，销售价将从在“销售价(预订)”窗体中创建的销售价设置中导出。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4b02af0a535e67818751c437482c3663524474
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817405"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="2635e-103">预订销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2635e-104">在您创建某一预订时，销售价将从在 **销售价(预订)** 窗体中创建的销售价设置中导出。</span><span class="sxs-lookup"><span data-stu-id="2635e-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="2635e-105">在 **销售价(预订)** 窗体中，您可以为特定的预订创建销售价，或者可以创建更广泛应用的销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="2635e-106">对于要应用于某一预订的销售价，预订的期间代码和币种必须与期间代码和该销售价的币种相同。</span><span class="sxs-lookup"><span data-stu-id="2635e-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="2635e-107">如果预订和销售价的期间代码和币种完全相同，则将基于在下表中列出的优先级选择预订销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="2635e-108">表中的空电池表示空字段，X 表示值等于从其生成交易记录的预订中的值。</span><span class="sxs-lookup"><span data-stu-id="2635e-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2635e-109">优先级 </span><span class="sxs-lookup"><span data-stu-id="2635e-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="2635e-110"><strong>类别</strong></span><span class="sxs-lookup"><span data-stu-id="2635e-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="2635e-111"><strong>项目 ID</strong></span><span class="sxs-lookup"><span data-stu-id="2635e-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="2635e-112"><strong>预订</strong></span><span class="sxs-lookup"><span data-stu-id="2635e-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="2635e-113"><strong>销售币种</strong></span><span class="sxs-lookup"><span data-stu-id="2635e-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="2635e-114"><strong>期间代码</strong></span><span class="sxs-lookup"><span data-stu-id="2635e-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-115">1</span><span class="sxs-lookup"><span data-stu-id="2635e-115">1</span></span></p></td>
<td><p><span data-ttu-id="2635e-116">X</span><span class="sxs-lookup"><span data-stu-id="2635e-116">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-117">X</span><span class="sxs-lookup"><span data-stu-id="2635e-117">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-118">X</span><span class="sxs-lookup"><span data-stu-id="2635e-118">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-119">X</span><span class="sxs-lookup"><span data-stu-id="2635e-119">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-120">X</span><span class="sxs-lookup"><span data-stu-id="2635e-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-121">2</span><span class="sxs-lookup"><span data-stu-id="2635e-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-122">X</span><span class="sxs-lookup"><span data-stu-id="2635e-122">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-123">X</span><span class="sxs-lookup"><span data-stu-id="2635e-123">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-124">X</span><span class="sxs-lookup"><span data-stu-id="2635e-124">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-125">X</span><span class="sxs-lookup"><span data-stu-id="2635e-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2635e-126">3</span><span class="sxs-lookup"><span data-stu-id="2635e-126">3</span></span></p></td>
<td><p><span data-ttu-id="2635e-127">X</span><span class="sxs-lookup"><span data-stu-id="2635e-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-128">X</span><span class="sxs-lookup"><span data-stu-id="2635e-128">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-129">X</span><span class="sxs-lookup"><span data-stu-id="2635e-129">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-130">X</span><span class="sxs-lookup"><span data-stu-id="2635e-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-131">4</span><span class="sxs-lookup"><span data-stu-id="2635e-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-132">X</span><span class="sxs-lookup"><span data-stu-id="2635e-132">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-133">X</span><span class="sxs-lookup"><span data-stu-id="2635e-133">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-134">X</span><span class="sxs-lookup"><span data-stu-id="2635e-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2635e-135">5</span><span class="sxs-lookup"><span data-stu-id="2635e-135">5</span></span></p></td>
<td><p><span data-ttu-id="2635e-136">X</span><span class="sxs-lookup"><span data-stu-id="2635e-136">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-137">X</span><span class="sxs-lookup"><span data-stu-id="2635e-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-138">X</span><span class="sxs-lookup"><span data-stu-id="2635e-138">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-139">X</span><span class="sxs-lookup"><span data-stu-id="2635e-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-140">6</span><span class="sxs-lookup"><span data-stu-id="2635e-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-141">X</span><span class="sxs-lookup"><span data-stu-id="2635e-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-142">X</span><span class="sxs-lookup"><span data-stu-id="2635e-142">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-143">X</span><span class="sxs-lookup"><span data-stu-id="2635e-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2635e-144">7</span><span class="sxs-lookup"><span data-stu-id="2635e-144">7</span></span></p></td>
<td><p><span data-ttu-id="2635e-145">X</span><span class="sxs-lookup"><span data-stu-id="2635e-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-146">X</span><span class="sxs-lookup"><span data-stu-id="2635e-146">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-147">X</span><span class="sxs-lookup"><span data-stu-id="2635e-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-148">8</span><span class="sxs-lookup"><span data-stu-id="2635e-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2635e-149">X</span><span class="sxs-lookup"><span data-stu-id="2635e-149">X</span></span></p></td>
<td><p><span data-ttu-id="2635e-150">X</span><span class="sxs-lookup"><span data-stu-id="2635e-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-151">在创建预订费用时，具有最高详细级别的销售价（如上表中所述）将选作预订销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="2635e-152">对预订销售价进行更新并编制索引</span><span class="sxs-lookup"><span data-stu-id="2635e-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="2635e-153">您可以通过更新基价或指数，更新预订销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="2635e-154">您可以按百分比更新，或者更新为新值。</span><span class="sxs-lookup"><span data-stu-id="2635e-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="2635e-155">预订费用销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-155">Subscription fee sales prices</span></span>

<span data-ttu-id="2635e-156">在您创建预订费用时，销售价将基于预订的销售价设置。</span><span class="sxs-lookup"><span data-stu-id="2635e-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="2635e-157">您可以通过预订价格设置来使用基价，或者可以创建指数形式的销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="2635e-158">示例</span><span class="sxs-lookup"><span data-stu-id="2635e-158">Example</span></span>

<span data-ttu-id="2635e-159">您想要为新项目 9030 设置 EUR 500 的预订销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="2635e-160">在 **销售价(预订)** 窗体中，可按照下表所示创建预订销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2635e-161">生效日期</span><span class="sxs-lookup"><span data-stu-id="2635e-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2635e-162">类别</span><span class="sxs-lookup"><span data-stu-id="2635e-162">Category</span></span></p></th>
<th><p><span data-ttu-id="2635e-163">项目</span><span class="sxs-lookup"><span data-stu-id="2635e-163">Project</span></span></p></th>
<th><p><span data-ttu-id="2635e-164">预订</span><span class="sxs-lookup"><span data-stu-id="2635e-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2635e-165">期间代码</span><span class="sxs-lookup"><span data-stu-id="2635e-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="2635e-166">销售币种</span><span class="sxs-lookup"><span data-stu-id="2635e-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2635e-167">销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="2635e-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2635e-169">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2635e-170">月</span><span class="sxs-lookup"><span data-stu-id="2635e-170">Month</span></span></p></td>
<td><p><span data-ttu-id="2635e-171">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-172">500</span><span class="sxs-lookup"><span data-stu-id="2635e-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-173">请注意，**类别** 字段和 **预订** 字段为空。</span><span class="sxs-lookup"><span data-stu-id="2635e-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="2635e-174">然后，您创建以下预订。</span><span class="sxs-lookup"><span data-stu-id="2635e-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2635e-175">服务预订</span><span class="sxs-lookup"><span data-stu-id="2635e-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2635e-176">项目</span><span class="sxs-lookup"><span data-stu-id="2635e-176">Project</span></span></p></th>
<th><p><span data-ttu-id="2635e-177">预订组</span><span class="sxs-lookup"><span data-stu-id="2635e-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="2635e-178">类别</span><span class="sxs-lookup"><span data-stu-id="2635e-178">Category</span></span></p></th>
<th><p><span data-ttu-id="2635e-179">币种</span><span class="sxs-lookup"><span data-stu-id="2635e-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="2635e-180">期间代码</span><span class="sxs-lookup"><span data-stu-id="2635e-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="2635e-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-182">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-182">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="2635e-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2635e-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2635e-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2635e-185">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-186">每月</span><span class="sxs-lookup"><span data-stu-id="2635e-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="2635e-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-188">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-188">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="2635e-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2635e-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2635e-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2635e-191">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-192">每月</span><span class="sxs-lookup"><span data-stu-id="2635e-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-193">现在，您为预订组 Sub1 中的两个预订都创建了预订费用：</span><span class="sxs-lookup"><span data-stu-id="2635e-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="2635e-194">单击 **服务管理** \> **设置** \> **服务预订** \> **预订组**。</span><span class="sxs-lookup"><span data-stu-id="2635e-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="2635e-195">在 **预订组** 窗体中，单击 **功能** \> **创建预订费用**。</span><span class="sxs-lookup"><span data-stu-id="2635e-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="2635e-196">在 **创建预订费用** 窗体中，输入相应信息。</span><span class="sxs-lookup"><span data-stu-id="2635e-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="2635e-197">有关详细信息，请参阅[创建预订费用交易记录](create-subscription-fee-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="2635e-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="2635e-198">为两个预订创建具有 EUR 500 销售价的费用，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="2635e-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="2635e-199">项目日期</span><span class="sxs-lookup"><span data-stu-id="2635e-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="2635e-200">服务预订</span><span class="sxs-lookup"><span data-stu-id="2635e-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2635e-201">项目</span><span class="sxs-lookup"><span data-stu-id="2635e-201">Project</span></span></p></th>
<th><p><span data-ttu-id="2635e-202">类别</span><span class="sxs-lookup"><span data-stu-id="2635e-202">Category</span></span></p></th>
<th><p><span data-ttu-id="2635e-203">开始日期</span><span class="sxs-lookup"><span data-stu-id="2635e-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="2635e-204">结束日期</span><span class="sxs-lookup"><span data-stu-id="2635e-204">End date</span></span></p></th>
<th><p><span data-ttu-id="2635e-205">销售币种</span><span class="sxs-lookup"><span data-stu-id="2635e-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2635e-206">销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="2635e-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2635e-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="2635e-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-209">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-209">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2635e-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2635e-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-213">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-214">500</span><span class="sxs-lookup"><span data-stu-id="2635e-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="2635e-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2635e-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="2635e-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-217">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-217">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2635e-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2635e-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-221">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-222">500</span><span class="sxs-lookup"><span data-stu-id="2635e-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-223">以后，您决定要为项目 9030 的类别 SubCat1 指定销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="2635e-224">因此，您创建一个新的销售价行，该行具有针对项目 9030 和费用类别 SubCat1 的组合的 EUR 550 的销售价。</span><span class="sxs-lookup"><span data-stu-id="2635e-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="2635e-225">现在项目 9030 存在两个预订销售价行，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="2635e-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2635e-226">生效日期</span><span class="sxs-lookup"><span data-stu-id="2635e-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2635e-227">类别</span><span class="sxs-lookup"><span data-stu-id="2635e-227">Category</span></span></p></th>
<th><p><span data-ttu-id="2635e-228">项目</span><span class="sxs-lookup"><span data-stu-id="2635e-228">Project</span></span></p></th>
<th><p><span data-ttu-id="2635e-229">预订</span><span class="sxs-lookup"><span data-stu-id="2635e-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2635e-230">期间代码</span><span class="sxs-lookup"><span data-stu-id="2635e-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="2635e-231">货币</span><span class="sxs-lookup"><span data-stu-id="2635e-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="2635e-232">销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2635e-234">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2635e-235">月</span><span class="sxs-lookup"><span data-stu-id="2635e-235">Month</span></span></p></td>
<td><p><span data-ttu-id="2635e-236">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-237">500</span><span class="sxs-lookup"><span data-stu-id="2635e-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2635e-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2635e-240">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2635e-241">月</span><span class="sxs-lookup"><span data-stu-id="2635e-241">Month</span></span></p></td>
<td><p><span data-ttu-id="2635e-242">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-243">550</span><span class="sxs-lookup"><span data-stu-id="2635e-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-244">您重复执行上述过程，以便为预订组 Sub1 中的两个预订都创建预订费用。</span><span class="sxs-lookup"><span data-stu-id="2635e-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="2635e-245">下表显示为每个预订创建的附加到该预订组的交易记录。</span><span class="sxs-lookup"><span data-stu-id="2635e-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="2635e-246">项目日期</span><span class="sxs-lookup"><span data-stu-id="2635e-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="2635e-247">预订</span><span class="sxs-lookup"><span data-stu-id="2635e-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2635e-248">项目</span><span class="sxs-lookup"><span data-stu-id="2635e-248">Project</span></span></p></th>
<th><p><span data-ttu-id="2635e-249">类别</span><span class="sxs-lookup"><span data-stu-id="2635e-249">Category</span></span></p></th>
<th><p><span data-ttu-id="2635e-250">开始日期</span><span class="sxs-lookup"><span data-stu-id="2635e-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="2635e-251">结束日期</span><span class="sxs-lookup"><span data-stu-id="2635e-251">End date</span></span></p></th>
<th><p><span data-ttu-id="2635e-252">销售币种</span><span class="sxs-lookup"><span data-stu-id="2635e-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2635e-253">销售价</span><span class="sxs-lookup"><span data-stu-id="2635e-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2635e-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="2635e-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="2635e-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="2635e-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-256">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-256">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2635e-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2635e-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="2635e-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2635e-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="2635e-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2635e-260">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-261">550</span><span class="sxs-lookup"><span data-stu-id="2635e-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2635e-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="2635e-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="2635e-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="2635e-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2635e-264">9030</span><span class="sxs-lookup"><span data-stu-id="2635e-264">9030</span></span></p></td>
<td><p><span data-ttu-id="2635e-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2635e-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2635e-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="2635e-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2635e-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="2635e-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2635e-268">欧元</span><span class="sxs-lookup"><span data-stu-id="2635e-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="2635e-269">500</span><span class="sxs-lookup"><span data-stu-id="2635e-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2635e-270">在预订 00020\_135 的第一个交易记录中，EUR 550 的销售价从为特定项目和类别的组合设置的预订销售价中导出。</span><span class="sxs-lookup"><span data-stu-id="2635e-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="2635e-271">在预订 00021\_135 的第二个交易记录中，EUR 500 的销售价用作项目预订销售价，因为不存在为项目 9030 和类别 SubCat2 的组合设置的价格。</span><span class="sxs-lookup"><span data-stu-id="2635e-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="2635e-272">请参阅</span><span class="sxs-lookup"><span data-stu-id="2635e-272">See also</span></span>

[<span data-ttu-id="2635e-273">对预订销售价进行更新并编制索引</span><span class="sxs-lookup"><span data-stu-id="2635e-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]