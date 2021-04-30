---
title: 销售税付款和化整规则
description: 文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间化整销售税余额。
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97f1a30c541a302755826bb8f77205bc060ec159
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897178"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="c66df-103">销售税付款和化整规则</span><span class="sxs-lookup"><span data-stu-id="c66df-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c66df-104">文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间化整销售税余额。</span><span class="sxs-lookup"><span data-stu-id="c66df-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="c66df-105">销售税需要定期申报和缴纳给税务主管机构。</span><span class="sxs-lookup"><span data-stu-id="c66df-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="c66df-106">这可以通过在“销售税”页运行结算和过帐销售税流程完成。</span><span class="sxs-lookup"><span data-stu-id="c66df-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="c66df-107">期间销售税将对照销售税帐户结算，销售税余额将过帐到销售税结算帐户。</span><span class="sxs-lookup"><span data-stu-id="c66df-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="c66df-108">销售税余额，在销售增值税结算帐户过帐，可以通过在“销售税”页设置化整规则来按照税务主管机构的要求化整。</span><span class="sxs-lookup"><span data-stu-id="c66df-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="c66df-109">化整差额过帐到销售税化整帐户，在“总帐”的“自动交易记录帐户”字段中选择。</span><span class="sxs-lookup"><span data-stu-id="c66df-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="c66df-110">以下示例说明销售税主管机构的化整规则如何工作。</span><span class="sxs-lookup"><span data-stu-id="c66df-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="c66df-111">示例</span><span class="sxs-lookup"><span data-stu-id="c66df-111">Examples</span></span>

<span data-ttu-id="c66df-112">期间的总销售税显示贷方余额 -98,765.43。</span><span class="sxs-lookup"><span data-stu-id="c66df-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="c66df-113">法人征收了的增值税超过其支付的金额。</span><span class="sxs-lookup"><span data-stu-id="c66df-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="c66df-114">因此，该法人欠税务主管机构款项。</span><span class="sxs-lookup"><span data-stu-id="c66df-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="c66df-115">该法人想要使用将该余额化整为最接近的 1.00 的化整方法。</span><span class="sxs-lookup"><span data-stu-id="c66df-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="c66df-116">负责增值税帐户的用户执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c66df-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="c66df-117">单击 **纳税** > **间接税** > **销售税** > **销售税主管机构**。</span><span class="sxs-lookup"><span data-stu-id="c66df-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="c66df-118">在 **常规** 快速选项卡上，在 **舍入形式** 字段中选择 **标准**。</span><span class="sxs-lookup"><span data-stu-id="c66df-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="c66df-119">在 **舍入** 字段中，输入 1.00。</span><span class="sxs-lookup"><span data-stu-id="c66df-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="c66df-120">在向税务主管机构支付销售税时，转到 **纳税** > **申报** > **销售税** > **结算和过帐销售税**。</span><span class="sxs-lookup"><span data-stu-id="c66df-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="c66df-121">在销售税结算帐户中，您可以看到应交税额 **98,765.43** 已舍入到 **98,765**。</span><span class="sxs-lookup"><span data-stu-id="c66df-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="c66df-122">下表显示通过使用用于 **销售税主管机构** 页中的 **舍入形式** 字段的舍入方法，如何将 98,765.43 的金额舍入。</span><span class="sxs-lookup"><span data-stu-id="c66df-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="c66df-123">如果舍入值设置为 0.00，则：</span><span class="sxs-lookup"><span data-stu-id="c66df-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="c66df-124">对于普通舍入，舍入行为与 **舍入 = 0.01** 相同。</span><span class="sxs-lookup"><span data-stu-id="c66df-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="c66df-125">对于 **舍入形式选项**，**舍尾**、**进位** 和 **对自身有利**，其行为与 **舍入 = 1.00** 相同。</span><span class="sxs-lookup"><span data-stu-id="c66df-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="c66df-126">化整形式选项</span><span class="sxs-lookup"><span data-stu-id="c66df-126">Rounding form option</span></span>                | <span data-ttu-id="c66df-127">化整值 = 0.01</span><span class="sxs-lookup"><span data-stu-id="c66df-127">Round-off value = 0.01</span></span> | <span data-ttu-id="c66df-128">化整值 = 0.10</span><span class="sxs-lookup"><span data-stu-id="c66df-128">Round-off value = 0.10</span></span> | <span data-ttu-id="c66df-129">化整值 = 1.00</span><span class="sxs-lookup"><span data-stu-id="c66df-129">Round-off value = 1.00</span></span> | <span data-ttu-id="c66df-130">化整值 = 100.00</span><span class="sxs-lookup"><span data-stu-id="c66df-130">Round-off value = 100.00</span></span> | <span data-ttu-id="c66df-131">化整值 = 0.00</span><span class="sxs-lookup"><span data-stu-id="c66df-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="c66df-132">标准</span><span class="sxs-lookup"><span data-stu-id="c66df-132">Normal</span></span>                              | <span data-ttu-id="c66df-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-133">98,765.43</span></span>              | <span data-ttu-id="c66df-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c66df-134">98,765.40</span></span>              | <span data-ttu-id="c66df-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c66df-135">98,765.00</span></span>              | <span data-ttu-id="c66df-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c66df-136">98,800.00</span></span>                | <span data-ttu-id="c66df-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-137">98,765.43</span></span>                |
| <span data-ttu-id="c66df-138">舍尾</span><span class="sxs-lookup"><span data-stu-id="c66df-138">Downward</span></span>                            | <span data-ttu-id="c66df-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-139">98,765.43</span></span>              | <span data-ttu-id="c66df-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c66df-140">98,765.40</span></span>              | <span data-ttu-id="c66df-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c66df-141">98,765.00</span></span>              | <span data-ttu-id="c66df-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="c66df-142">98,700.00</span></span>                | <span data-ttu-id="c66df-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c66df-143">98,765.00</span></span>                |
| <span data-ttu-id="c66df-144">进位</span><span class="sxs-lookup"><span data-stu-id="c66df-144">Rounding-up</span></span>                         | <span data-ttu-id="c66df-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-145">98,765.43</span></span>              | <span data-ttu-id="c66df-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="c66df-146">98,765.50</span></span>              | <span data-ttu-id="c66df-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c66df-147">98,766.00</span></span>              | <span data-ttu-id="c66df-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c66df-148">98,800.00</span></span>                | <span data-ttu-id="c66df-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c66df-149">98,766.00</span></span>                |
| <span data-ttu-id="c66df-150">对自身有利，对于贷方余额</span><span class="sxs-lookup"><span data-stu-id="c66df-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="c66df-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-151">98,765.43</span></span>              | <span data-ttu-id="c66df-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c66df-152">98,765.40</span></span>              | <span data-ttu-id="c66df-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c66df-153">98,765.00</span></span>              | <span data-ttu-id="c66df-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="c66df-154">98,700.00</span></span>                | <span data-ttu-id="c66df-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c66df-155">98,765.00</span></span>                |
| <span data-ttu-id="c66df-156">对自身有利，对于借方余额</span><span class="sxs-lookup"><span data-stu-id="c66df-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="c66df-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c66df-157">98,765.43</span></span>              | <span data-ttu-id="c66df-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="c66df-158">98,765.50</span></span>              | <span data-ttu-id="c66df-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c66df-159">98,766.00</span></span>              | <span data-ttu-id="c66df-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c66df-160">98,800.00</span></span>                | <span data-ttu-id="c66df-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c66df-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="c66df-162">正常化整，化整精度为 0.01</span><span class="sxs-lookup"><span data-stu-id="c66df-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="c66df-163">舍入</span><span class="sxs-lookup"><span data-stu-id="c66df-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="c66df-164">计算流程</span><span class="sxs-lookup"><span data-stu-id="c66df-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="c66df-165">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="c66df-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="c66df-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="c66df-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="c66df-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="c66df-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="c66df-168">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="c66df-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="c66df-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="c66df-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="c66df-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="c66df-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="c66df-171">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="c66df-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="c66df-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="c66df-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="c66df-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="c66df-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="c66df-174">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="c66df-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="c66df-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="c66df-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="c66df-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="c66df-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="c66df-177">如果您选择“对自身有利”，则化整始终对法人有利。</span><span class="sxs-lookup"><span data-stu-id="c66df-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="c66df-178">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c66df-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="c66df-179">销售税概览</span><span class="sxs-lookup"><span data-stu-id="c66df-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="c66df-180">创建销售税支付</span><span class="sxs-lookup"><span data-stu-id="c66df-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="c66df-181">在单据中创建销售税交易记录</span><span class="sxs-lookup"><span data-stu-id="c66df-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="c66df-182">查看已过帐的销售税交易记录</span><span class="sxs-lookup"><span data-stu-id="c66df-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- <span data-ttu-id="c66df-183">[化整功能](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="c66df-183">[round Function](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
