---
title: 客户帐龄分析表
description: 客户帐龄分析表显示应收客户余额，按日期间隔或帐龄期间排序。
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974853"
---
# <a name="customer-aging-report"></a><span data-ttu-id="7b49e-103">客户帐龄分析表</span><span class="sxs-lookup"><span data-stu-id="7b49e-103">Customer aging report</span></span> 

<span data-ttu-id="7b49e-104">**客户帐龄**分析表显示应收客户余额，按日期间隔或帐龄期间排序。</span><span class="sxs-lookup"><span data-stu-id="7b49e-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="7b49e-105">生成此分析表时，显示下列默认参数。</span><span class="sxs-lookup"><span data-stu-id="7b49e-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="7b49e-106">可使用这些参数筛选将在分析表中显示的数据。</span><span class="sxs-lookup"><span data-stu-id="7b49e-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="7b49e-107">有关详细信息，请参阅[设置收款](set-up-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="7b49e-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b49e-108">字段</span><span class="sxs-lookup"><span data-stu-id="7b49e-108">Field</span></span></p></th>
<th><p><span data-ttu-id="7b49e-109">说明</span><span class="sxs-lookup"><span data-stu-id="7b49e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-110"><strong>计费分类</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-111">选择要包括到分析表中的一个或多个计费分类。</span><span class="sxs-lookup"><span data-stu-id="7b49e-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="7b49e-112">**注意：** 只有选择了<STRONG>公共部门</STRONG> Configuration Key 后，此控制才可用。</span><span class="sxs-lookup"><span data-stu-id="7b49e-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-113"><strong>包括没有计费分类的交易记录</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-114">如果选中此复选框，则未获分配计费分类的所有交易都将显示在分析表上。</span><span class="sxs-lookup"><span data-stu-id="7b49e-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="7b49e-115">**注意：** 只有选择了<STRONG>公共部门</STRONG> Configuration Key 后，此控制才可用。</span><span class="sxs-lookup"><span data-stu-id="7b49e-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-116"><strong>帐龄截至日期</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-117">输入当前帐龄时段使用的日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-118"><strong>截至该天余额</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-119">输入要查看客户余额的日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="7b49e-120">这也称作交易的截止日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-121"><strong>开始日期</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-122">输入要包括在分析表中的第一个期间间隔或帐龄期间内的日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-123"><strong>条件</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-124">选择分析表基于的日期类型。</span><span class="sxs-lookup"><span data-stu-id="7b49e-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="7b49e-125"><strong>交易日期</strong> – 交易的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="7b49e-126">例如，这可能是用于计算截止日期所依据的发票日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="7b49e-127"><strong>截止日期</strong> – 付款期限中规定的交易的截止日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="7b49e-128"><strong>单据日期</strong> – 计算截止日期所依据的用户定义的单据日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-129"><strong>帐龄期间定义</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-130">选择帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="7b49e-130">Select an aging period definition.</span></span> <span data-ttu-id="7b49e-131">如果您选择帐龄期间定义，则不使用<strong>间隔</strong>字段。</span><span class="sxs-lookup"><span data-stu-id="7b49e-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="7b49e-132">具有六个以上帐龄期间的帐龄期间定义不可在打印的分析表上使用。</span><span class="sxs-lookup"><span data-stu-id="7b49e-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="7b49e-133">**注意：** 您可以在<STRONG>帐龄期间定义</STRONG>页面上设置帐龄期间。</span><span class="sxs-lookup"><span data-stu-id="7b49e-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-134"><strong>打印帐龄期间描述</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-135">选择<strong>是</strong>以在分析表中每个帐龄期间列的顶部包括帐龄期间描述。</span><span class="sxs-lookup"><span data-stu-id="7b49e-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="7b49e-136">选择<strong>否</strong>以打印分析表，而无需列标题。</span><span class="sxs-lookup"><span data-stu-id="7b49e-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-137"><strong>间期</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-138">通过输入每个期间中的天或月单位数来定义要使用的期间。</span><span class="sxs-lookup"><span data-stu-id="7b49e-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="7b49e-139">例如，若要按周查看帐龄信息，请在此字段中输入 7 并在<strong>天/月</strong>字段中选择<strong>天</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b49e-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="7b49e-140">**注意：** 只有当您未选择帐龄期间定义时，才能使用在此字段中输入的信息。</span><span class="sxs-lookup"><span data-stu-id="7b49e-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="7b49e-141">否则，在帐龄期间定义上定义打印方向。</span><span class="sxs-lookup"><span data-stu-id="7b49e-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-142"><strong>天/月</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-143">选择单位<strong>天</strong>或<strong>月</strong>，它用于定义<strong>间隔</strong>字段中的期间。</span><span class="sxs-lookup"><span data-stu-id="7b49e-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-144"><strong>打印方向</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-145">选择是否计算余额，是为过去还是将来期间打印帐龄分析表。</span><span class="sxs-lookup"><span data-stu-id="7b49e-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="7b49e-146">相对于<strong>余额截止日期</strong>字段中选择的日期评估日期。</span><span class="sxs-lookup"><span data-stu-id="7b49e-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="7b49e-147">选择<strong>倒推</strong>以显示过去期间的信息。</span><span class="sxs-lookup"><span data-stu-id="7b49e-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="7b49e-148">选择<strong>正推</strong>以显示将来期间的信息。</span><span class="sxs-lookup"><span data-stu-id="7b49e-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="7b49e-149">**注意：** 只有当您未选择帐龄期间定义时，才能使用在此字段中输入的信息。</span><span class="sxs-lookup"><span data-stu-id="7b49e-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-150"><strong>明细</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-151">选择以列出在分析表上显示的余额所涉及的交易。</span><span class="sxs-lookup"><span data-stu-id="7b49e-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-152"><strong>包括以交易记录币种表示的金额</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-153">选择以包括除以记帐币种表示的金额之外，还包括以交易币种表示的金额。</span><span class="sxs-lookup"><span data-stu-id="7b49e-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="7b49e-154">如果未选中此复选框，则分析表上的金额仅以记帐币种显示。</span><span class="sxs-lookup"><span data-stu-id="7b49e-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-155"><strong>负数余额</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-156">选择以包括余额为负数的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="7b49e-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b49e-157"><strong>排除零余额科目</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-158">选择以排除余额为零的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="7b49e-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b49e-159"><strong>付款定位</strong></span><span class="sxs-lookup"><span data-stu-id="7b49e-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="7b49e-160">选择以显示尚未结算的付款。</span><span class="sxs-lookup"><span data-stu-id="7b49e-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="7b49e-161">这些都显示在分析表的第一列中。</span><span class="sxs-lookup"><span data-stu-id="7b49e-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

