---
title: "会计分配和普通发票的子分类日记帐条目"
description: "会计分配用于定义将如何对账金额，例如将如何对账普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对账的每笔金额都将具有一个或多个会计分配。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d13fbd98597fc8138bfb4d549608d75f790e0e52
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="b05b6-104">会计分配和普通发票的子分类日记帐条目</span><span class="sxs-lookup"><span data-stu-id="b05b6-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b05b6-105">会计分配用于定义将如何对账金额，例如将如何对账普通发票中的收入、税金或费用。</span><span class="sxs-lookup"><span data-stu-id="b05b6-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="b05b6-106">普通发票已记入日记帐时，必须对账的每笔金额都将具有一个或多个会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="b05b6-107">会计分配</span><span class="sxs-lookup"><span data-stu-id="b05b6-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="b05b6-108">您可以使用“普通发票”页中的以下按钮查看和更改普通发票的每笔金额的会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="b05b6-109">**分摊金额** — 查看和更改单独行和任何子行的会计分配，例如税金或费用。</span><span class="sxs-lookup"><span data-stu-id="b05b6-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="b05b6-110">您还可以直接从“销售税交易记录”页或“费用交易记录”页查看和更改子行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="b05b6-111">更改普通发票抬头金额，如费用或币种整金额。</span><span class="sxs-lookup"><span data-stu-id="b05b6-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="b05b6-112">更改普通发票行金额。</span><span class="sxs-lookup"><span data-stu-id="b05b6-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="b05b6-113">**“查看分配”** - 查看文档中所有行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="b05b6-114">您无法从此视图更改会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="b05b6-115">查看标题和单行金额。</span><span class="sxs-lookup"><span data-stu-id="b05b6-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="b05b6-116">分配金额</span><span class="sxs-lookup"><span data-stu-id="b05b6-116">Distributing amounts</span></span>
<span data-ttu-id="b05b6-117">当您输入普通发票时，每笔金额将按如下分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b05b6-118">货币金额的类型</span><span class="sxs-lookup"><span data-stu-id="b05b6-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="b05b6-119">主科目显示的位置。</span><span class="sxs-lookup"><span data-stu-id="b05b6-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="b05b6-120">优先级顺序确定显示的默认财务维度</span><span class="sxs-lookup"><span data-stu-id="b05b6-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b05b6-121">普通发票行</span><span class="sxs-lookup"><span data-stu-id="b05b6-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="b05b6-122">普通发票行的会计科目。</span><span class="sxs-lookup"><span data-stu-id="b05b6-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b05b6-123">如果主科目是分配帐户，则使用分配账户定义中的默认值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b05b6-124">如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</span><span class="sxs-lookup"><span data-stu-id="b05b6-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-125">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-126">使用“会计科目表”页中会计科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b05b6-127">固定资产编号和价值模型组合的普通发票行</span><span class="sxs-lookup"><span data-stu-id="b05b6-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b05b6-128"><strong>注意</strong></span><span class="sxs-lookup"><span data-stu-id="b05b6-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b05b6-129">普通发票行的主科目将为固定资产处置科目。</span><span class="sxs-lookup"><span data-stu-id="b05b6-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="b05b6-130">普通发票行的会计科目。</span><span class="sxs-lookup"><span data-stu-id="b05b6-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b05b6-131">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-132">使用“会计科目表”页中会计科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b05b6-133">普通发票折扣金额</span><span class="sxs-lookup"><span data-stu-id="b05b6-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="b05b6-134">“现金折扣”页面上的“客户折扣的主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="b05b6-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b05b6-135">如果主科目是分配帐户，则使用分配账户定义中的默认值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b05b6-136">如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</span><span class="sxs-lookup"><span data-stu-id="b05b6-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-137">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-138">使用“会计科目表”页中会计科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b05b6-139">普通发票销售税总额</span><span class="sxs-lookup"><span data-stu-id="b05b6-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="b05b6-140">“分类帐记帐组”页中的“应付销售税”字段。</span><span class="sxs-lookup"><span data-stu-id="b05b6-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b05b6-141">使用普通发票单行金额或费用行金额的分配中定义的财务维度。</span><span class="sxs-lookup"><span data-stu-id="b05b6-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="b05b6-142">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-143">使用“会计科目表”页中会计科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b05b6-144">普通发票费用行金额</span><span class="sxs-lookup"><span data-stu-id="b05b6-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="b05b6-145">“费用代码”页中的“贷方科目”字段。</span><span class="sxs-lookup"><span data-stu-id="b05b6-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b05b6-146">如果主科目是分配帐户，则使用分配账户定义中的默认值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b05b6-147">如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</span><span class="sxs-lookup"><span data-stu-id="b05b6-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-148">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b05b6-149">使用“会计科目表”页中会计科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="b05b6-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="b05b6-150">分配税</span><span class="sxs-lookup"><span data-stu-id="b05b6-150">Distributing taxes</span></span>
<span data-ttu-id="b05b6-151">无法在计算税金之前创建税金会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="b05b6-152">若要计算增值税，必须完成“普通发票”窗体中的以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="b05b6-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="b05b6-153">查看增值税。</span><span class="sxs-lookup"><span data-stu-id="b05b6-153">View the sales tax.</span></span>
-   <span data-ttu-id="b05b6-154">查看发票合计。</span><span class="sxs-lookup"><span data-stu-id="b05b6-154">View the invoice total.</span></span>
-   <span data-ttu-id="b05b6-155">查看现金流。</span><span class="sxs-lookup"><span data-stu-id="b05b6-155">View the cash flow.</span></span>
-   <span data-ttu-id="b05b6-156">查看整个普通发票的会计分配。</span><span class="sxs-lookup"><span data-stu-id="b05b6-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="b05b6-157">– 查看子分类日记账。</span><span class="sxs-lookup"><span data-stu-id="b05b6-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="b05b6-158">普通发票的子分类日记帐</span><span class="sxs-lookup"><span data-stu-id="b05b6-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="b05b6-159">将普通发票过帐前，您可以查看发票的完整的会计条目，包括借方和贷方，以验证发票已过帐到正确的账户。</span><span class="sxs-lookup"><span data-stu-id="b05b6-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="b05b6-160">完整的会计条目的此视图称作子分类日记账。</span><span class="sxs-lookup"><span data-stu-id="b05b6-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="b05b6-161">如果子分类日记帐条目不正确，在预览后，分录普通发票前，您无法更改子分类日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="b05b6-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="b05b6-162">相反，您必须更改会计分配或过帐模板。</span><span class="sxs-lookup"><span data-stu-id="b05b6-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="b05b6-163">会计分配用于定义会计条目、借方或贷方的这一侧。</span><span class="sxs-lookup"><span data-stu-id="b05b6-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="b05b6-164">抵销子分类日记帐科目分录从过帐模板创建，如从客户帐户或税金。</span><span class="sxs-lookup"><span data-stu-id="b05b6-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>




