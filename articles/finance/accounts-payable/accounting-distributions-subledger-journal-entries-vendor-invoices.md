---
title: 会计分配和供应商发票的日记帐条目
description: 会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0ad3124963dda33f44cf8ba6e6bb466029b2651
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252185"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="516b4-104">会计分配和供应商发票的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="516b4-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="516b4-105">会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。</span><span class="sxs-lookup"><span data-stu-id="516b4-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="516b4-106">普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="516b4-107">会计分配</span><span class="sxs-lookup"><span data-stu-id="516b4-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="516b4-108">您可以使用“供应商发票”页中的以下按钮查看和修改普通发票的每笔金额的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="516b4-109">**分摊金额**– 查看和修改单独行和任何子行的会计分配，例如税金或费用。</span><span class="sxs-lookup"><span data-stu-id="516b4-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="516b4-110">您还可以直接从“销售税交易记录”页或“费用交易记录”页查看和修改子行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="516b4-111">修改普通发票抬头金额，如费用或币种化整金额。</span><span class="sxs-lookup"><span data-stu-id="516b4-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="516b4-112">修改供应商发票行金额。</span><span class="sxs-lookup"><span data-stu-id="516b4-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="516b4-113">**查看分配** – 查看文档中所有行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="516b4-114">您无法从此视图修改会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="516b4-115">查看标题和单行金额。</span><span class="sxs-lookup"><span data-stu-id="516b4-115">View header and line amounts.</span></span>

<span data-ttu-id="516b4-116">如果供应商发票参考采购订单，才能拆分和修改包含一个物料未库存行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="516b4-117">如果供应商发票行不参考采购订单行，还可以删除会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="516b4-118">您不能拆分或删除费用、税和单行折扣行。</span><span class="sxs-lookup"><span data-stu-id="516b4-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="516b4-119">您可以修改会计科目，不过，您不能更改金额或百分比。</span><span class="sxs-lookup"><span data-stu-id="516b4-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="516b4-120">如果父行包含贮存的物料和拆分的会计分配，将自动拆分该子行以与父行的财务维度匹配。</span><span class="sxs-lookup"><span data-stu-id="516b4-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="516b4-121">无法进一步拆分或删除子行的会计分配，但根据子行的设置，您可能能够为子行的会计分配修改会计科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="516b4-122">分配金额</span><span class="sxs-lookup"><span data-stu-id="516b4-122">Distributing amounts</span></span>
<span data-ttu-id="516b4-123">当您输入普通发票时，每笔金额将按如下分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="516b4-124">供应商发票行的类型</span><span class="sxs-lookup"><span data-stu-id="516b4-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="516b4-125">优先级顺序确定默认主科目显示的位置。</span><span class="sxs-lookup"><span data-stu-id="516b4-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="516b4-126">优先级顺序确定显示的默认财务维度</span><span class="sxs-lookup"><span data-stu-id="516b4-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="516b4-127">贮存的产品</span><span class="sxs-lookup"><span data-stu-id="516b4-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-128">采购订单行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-129">当在“过帐”页选择“产品采购支出”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-130">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-131">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-132">采购类别或未库存的物料</span><span class="sxs-lookup"><span data-stu-id="516b4-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-133">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-134">当在“过帐”页选择“支出中的采购支出”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-135">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-136">如果主科目是分配帐户，则使用分配帐户定义中的默认值。</span><span class="sxs-lookup"><span data-stu-id="516b4-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="516b4-137">在普通发票行使用默认的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="516b4-138">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-139">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="516b4-140">固定资产</span><span class="sxs-lookup"><span data-stu-id="516b4-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-141">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-142">如果在“供应商发票”窗体中的“交易记录类型”字段中的“购置”，在“固定资产过帐模板”页中选择“购置”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="516b4-143">如果在“交易记录类型”字段中选择“购置调整”，在“固定资产过帐模板”页中选择“购置调整”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-144">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-145">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-146">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-147">项目定义在供应商发票行</span><span class="sxs-lookup"><span data-stu-id="516b4-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-148">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-149">如果在“项目组”页的“过帐成本 - 物料”字段中选择了“余额”，在“分类帐记帐设置”页中选择“成本”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="516b4-150">如果在“项目组”页的“过帐成本 - 物料”字段中选择了“损益”，在“分类帐记帐设置”页中选择“成本 - 物料”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-151">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="516b4-152">单行折扣</span><span class="sxs-lookup"><span data-stu-id="516b4-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-153">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-154">在“过帐”页中选择“折扣”时的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="516b4-155">如果没有在过帐模版上、采购订单行上延伸价格的会计分配中定义主折扣科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-156">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-157">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-158">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-159">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-160">在采购订单行的“价格和折扣”选项卡上输入的采购费用</span><span class="sxs-lookup"><span data-stu-id="516b4-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-161">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-162">采购订单行延伸价格的会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-163">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-164">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="516b4-165">行费用</span><span class="sxs-lookup"><span data-stu-id="516b4-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-166">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-167">如果在“费用代码”窗体中的“借方类型”字段中选择了“会计科目”，“费用代码”页的“借方科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="516b4-168">如果在“费用代码”窗体中的“借方类型”字段中选择“物料”，延伸价格的会计分配为采购订单行。</span><span class="sxs-lookup"><span data-stu-id="516b4-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-169">如果在“费用代码”窗体中的“借方类型”字段中选择了“客户/供应商”，“费用代码”页的“贷方科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-170">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-171">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-172">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-173">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-174">满足以下条件的税金：</span><span class="sxs-lookup"><span data-stu-id="516b4-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="516b4-175">在“总帐参数”页中选择“应用美国税务规则”选项。</span><span class="sxs-lookup"><span data-stu-id="516b4-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="516b4-176">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-177">查看费用的延伸价格或会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-178">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-179">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-180">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="516b4-181">满足以下条件的税金：</span><span class="sxs-lookup"><span data-stu-id="516b4-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="516b4-182">在“总帐参数”页中清除“应用美国税务规则”选项。</span><span class="sxs-lookup"><span data-stu-id="516b4-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="516b4-183">在“销售税组”页清除销售税组的“销项税”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="516b4-184">如果税额应退，“分类帐记帐组”页的“应收销售税”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="516b4-185">如果增值税金额不应退，费用的延伸价格或会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-186">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-187">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-188">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-189">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-190">满足以下条件的税金：</span><span class="sxs-lookup"><span data-stu-id="516b4-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="516b4-191">在“总帐参数”页中清除“应用美国税务规则”选项。</span><span class="sxs-lookup"><span data-stu-id="516b4-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="516b4-192">在“销售税组”页选择销售税组的“销项税”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="516b4-193">如果税额应退，“分类帐记帐组”页的“应收销售税”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="516b4-194">如果税额不应退，“分类帐记帐组”页的“销项税支出”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-195">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-196">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-197">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-198">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="516b4-199">标题费用</span><span class="sxs-lookup"><span data-stu-id="516b4-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-200">如果在“费用代码”窗体中的“借方类型”字段中选择了“会计科目”，“费用代码”页的“借方科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="516b4-201">如果在“费用代码”窗体中的“借方类型”字段中选择了“客户/供应商”，“费用代码”页的“贷方科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-202">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-203">如果主科目是分配帐户，则使用分配帐户定义中的默认值。</span><span class="sxs-lookup"><span data-stu-id="516b4-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="516b4-204">使用供应商发票抬头的财务维度值默认模板。</span><span class="sxs-lookup"><span data-stu-id="516b4-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="516b4-205">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-206">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="516b4-207">标题折扣</span><span class="sxs-lookup"><span data-stu-id="516b4-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="516b4-208">“自动交易记录帐户”页中“供应商发票折扣过帐类型”的“主科目”字段。</span><span class="sxs-lookup"><span data-stu-id="516b4-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="516b4-209">如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</span><span class="sxs-lookup"><span data-stu-id="516b4-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="516b4-210">用于供应商发票行的总价使用来自会计分配的财务维度。</span><span class="sxs-lookup"><span data-stu-id="516b4-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-211">使用来自采购订单行的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="516b4-212">使用“会计科目表”页中主科目中的默认财务维度值。</span><span class="sxs-lookup"><span data-stu-id="516b4-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="516b4-213">分配税</span><span class="sxs-lookup"><span data-stu-id="516b4-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="516b4-214">无法在计算税金之前创建税金会计分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="516b4-215">若要计算增值税，必须完成“供应商发票”页中的以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="516b4-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="516b4-216">查看发票合计。</span><span class="sxs-lookup"><span data-stu-id="516b4-216">View the invoice total.</span></span>
-   <span data-ttu-id="516b4-217">查看增值税。</span><span class="sxs-lookup"><span data-stu-id="516b4-217">View the sales tax.</span></span>
-   <span data-ttu-id="516b4-218">– 查看子分类日记帐。</span><span class="sxs-lookup"><span data-stu-id="516b4-218">View the subledger journal.</span></span>
-   <span data-ttu-id="516b4-219">完成供应商发票的会计查看分配。</span><span class="sxs-lookup"><span data-stu-id="516b4-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="516b4-220">处于暂挂状态的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="516b4-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="516b4-221">过帐供应商发票。</span><span class="sxs-lookup"><span data-stu-id="516b4-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="516b4-222">供应商发票的子分类日志</span><span class="sxs-lookup"><span data-stu-id="516b4-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="516b4-223">将普通发票过帐前，您可以查看发票的完整的会计条目，包括借方和贷方，以验证发票已过帐到正确的帐户。</span><span class="sxs-lookup"><span data-stu-id="516b4-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="516b4-224">完整的会计条目的此视图称作子分类日记帐。</span><span class="sxs-lookup"><span data-stu-id="516b4-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="516b4-225">如果子分类日记帐条目不正确，在预览后，分录普通发票前，您无法修改子分类日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="516b4-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="516b4-226">相反，您必须修改会计分配或过帐模板。</span><span class="sxs-lookup"><span data-stu-id="516b4-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="516b4-227">会计分配用于定义会计条目、借方或贷方的这一侧。</span><span class="sxs-lookup"><span data-stu-id="516b4-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="516b4-228">抵销子分类日记帐科目分录从过帐模板创建，如从客户帐户或税金。</span><span class="sxs-lookup"><span data-stu-id="516b4-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]