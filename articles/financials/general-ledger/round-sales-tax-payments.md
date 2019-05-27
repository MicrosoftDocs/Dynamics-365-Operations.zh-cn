---
title: 销售税付款和舍入规则
description: 文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间舍入销售税余额。
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531849"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="33f54-103">销售税付款和舍入规则</span><span class="sxs-lookup"><span data-stu-id="33f54-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33f54-104">文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间舍入销售税余额。</span><span class="sxs-lookup"><span data-stu-id="33f54-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="33f54-105">销售税需要定期申报和缴纳给税务主管机构。</span><span class="sxs-lookup"><span data-stu-id="33f54-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="33f54-106">这可以通过在“销售税”页运行结算和过帐销售税流程完成。</span><span class="sxs-lookup"><span data-stu-id="33f54-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="33f54-107">期间销售税将对照销售税帐户结算，销售税余额将过帐到销售税结算帐户。</span><span class="sxs-lookup"><span data-stu-id="33f54-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="33f54-108">销售税余额，在销售增值税结算帐户过帐，可以通过在“销售税”页设置舍入规则来按照税务主管机构的要求舍入。</span><span class="sxs-lookup"><span data-stu-id="33f54-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="33f54-109">舍入差额过帐到销售税舍入帐户，在“总帐”的“自动交易记录帐户”字段中选择。</span><span class="sxs-lookup"><span data-stu-id="33f54-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="33f54-110">以下示例说明销售税主管机构的舍入规则如何工作。</span><span class="sxs-lookup"><span data-stu-id="33f54-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="33f54-111">示例</span><span class="sxs-lookup"><span data-stu-id="33f54-111">Examples</span></span>

<span data-ttu-id="33f54-112">期间的总销售税显示贷方余额 -98,765.43。</span><span class="sxs-lookup"><span data-stu-id="33f54-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="33f54-113">法人征收了的增值税超过其支付的金额。</span><span class="sxs-lookup"><span data-stu-id="33f54-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="33f54-114">因此，该法人欠税务主管机构款项。</span><span class="sxs-lookup"><span data-stu-id="33f54-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="33f54-115">该法人想要使用将该余额化整为最接近的 1.00 的化整方法。</span><span class="sxs-lookup"><span data-stu-id="33f54-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="33f54-116">负责增值税帐户的用户执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="33f54-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="33f54-117">单击“税”&gt;“间接税”&gt;“销售税”&gt;“销售税主管机构”。</span><span class="sxs-lookup"><span data-stu-id="33f54-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="33f54-118">在“常规”快速选项卡上，选择“舍入形式”字段中的“标准”。</span><span class="sxs-lookup"><span data-stu-id="33f54-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="33f54-119">在“舍入”字段中，输入 1.00。</span><span class="sxs-lookup"><span data-stu-id="33f54-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="33f54-120">在向税务主管机构支付销售税时，打开“结算和过帐销售税”页。</span><span class="sxs-lookup"><span data-stu-id="33f54-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="33f54-121">（单击“税”&gt;“申报”&gt;“销售税”&gt;“结算和过帐销售税”。）</span><span class="sxs-lookup"><span data-stu-id="33f54-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="33f54-122">在销售税结算帐户中，将应交税额 98,765.43 舍入到 98,765。</span><span class="sxs-lookup"><span data-stu-id="33f54-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="33f54-123">下表显示通过使用用于“销售税主管机构”页中的“舍入形式”字段的舍方法，如何将 98,765.43 的金额舍入。</span><span class="sxs-lookup"><span data-stu-id="33f54-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="33f54-124">舍入形式选项</span><span class="sxs-lookup"><span data-stu-id="33f54-124">Rounding form option</span></span>                | <span data-ttu-id="33f54-125">舍入值 = 0.01</span><span class="sxs-lookup"><span data-stu-id="33f54-125">Round-off value = 0.01</span></span> | <span data-ttu-id="33f54-126">舍入值 = 0.10</span><span class="sxs-lookup"><span data-stu-id="33f54-126">Round-off value = 0.10</span></span> | <span data-ttu-id="33f54-127">舍入值 = 1.00</span><span class="sxs-lookup"><span data-stu-id="33f54-127">Round-off value = 1.00</span></span> | <span data-ttu-id="33f54-128">舍入值 = 100.00</span><span class="sxs-lookup"><span data-stu-id="33f54-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="33f54-129">标准</span><span class="sxs-lookup"><span data-stu-id="33f54-129">Normal</span></span>                              | <span data-ttu-id="33f54-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="33f54-130">98,765.43</span></span>              | <span data-ttu-id="33f54-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="33f54-131">98,765.40</span></span>              | <span data-ttu-id="33f54-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="33f54-132">98,765.00</span></span>              | <span data-ttu-id="33f54-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="33f54-133">98,800.00</span></span>                |
| <span data-ttu-id="33f54-134">舍尾</span><span class="sxs-lookup"><span data-stu-id="33f54-134">Downward</span></span>                            | <span data-ttu-id="33f54-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="33f54-135">98,765.43</span></span>              | <span data-ttu-id="33f54-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="33f54-136">98,765.40</span></span>              | <span data-ttu-id="33f54-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="33f54-137">98,765.00</span></span>              | <span data-ttu-id="33f54-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="33f54-138">98,700.00</span></span>                |
| <span data-ttu-id="33f54-139">进位</span><span class="sxs-lookup"><span data-stu-id="33f54-139">Rounding-up</span></span>                         | <span data-ttu-id="33f54-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="33f54-140">98,765.43</span></span>              | <span data-ttu-id="33f54-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="33f54-141">98,765.50</span></span>              | <span data-ttu-id="33f54-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="33f54-142">98,766.00</span></span>              | <span data-ttu-id="33f54-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="33f54-143">98,800.00</span></span>                |
| <span data-ttu-id="33f54-144">对自身有利，对于贷方余额</span><span class="sxs-lookup"><span data-stu-id="33f54-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="33f54-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="33f54-145">98,765.43</span></span>              | <span data-ttu-id="33f54-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="33f54-146">98,765.40</span></span>              | <span data-ttu-id="33f54-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="33f54-147">98,765.00</span></span>              | <span data-ttu-id="33f54-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="33f54-148">98,700.00</span></span>                |
| <span data-ttu-id="33f54-149">对自身有利，对于借方余额</span><span class="sxs-lookup"><span data-stu-id="33f54-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="33f54-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="33f54-150">98,765.43</span></span>              | <span data-ttu-id="33f54-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="33f54-151">98,765.50</span></span>              | <span data-ttu-id="33f54-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="33f54-152">98,766.00</span></span>              | <span data-ttu-id="33f54-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="33f54-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="33f54-154">根本不舍入，因为化整为 0.00</span><span class="sxs-lookup"><span data-stu-id="33f54-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="33f54-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="33f54-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="33f54-156">正常舍入，舍入精度为 0.01</span><span class="sxs-lookup"><span data-stu-id="33f54-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="33f54-157">舍入</span><span class="sxs-lookup"><span data-stu-id="33f54-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="33f54-158">计算流程</span><span class="sxs-lookup"><span data-stu-id="33f54-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="33f54-159">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="33f54-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="33f54-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="33f54-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="33f54-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="33f54-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="33f54-162">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="33f54-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="33f54-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="33f54-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="33f54-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="33f54-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="33f54-165">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="33f54-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="33f54-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="33f54-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="33f54-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="33f54-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="33f54-168">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="33f54-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="33f54-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="33f54-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="33f54-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="33f54-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="33f54-171">如果您选择“对自身有利”，则舍入始终对法人有利。</span><span class="sxs-lookup"><span data-stu-id="33f54-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="33f54-172">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="33f54-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="33f54-173">销售税概览</span><span class="sxs-lookup"><span data-stu-id="33f54-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="33f54-174">创建销售税支付</span><span class="sxs-lookup"><span data-stu-id="33f54-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="33f54-175">在单据中创建销售交易记录</span><span class="sxs-lookup"><span data-stu-id="33f54-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="33f54-176">查看已过帐的销售税交易记录</span><span class="sxs-lookup"><span data-stu-id="33f54-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="33f54-177">舍入功能</span><span class="sxs-lookup"><span data-stu-id="33f54-177">round Function</span></span>](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


