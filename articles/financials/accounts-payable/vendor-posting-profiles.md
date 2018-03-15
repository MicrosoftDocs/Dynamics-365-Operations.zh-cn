---
title: "供应商过帐模板"
description: "供应商过帐模板控制将供应商交易记录过帐到总帐。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 8d9a27ecb99265674211a5ec768fe55040b8f5fe
ms.contentlocale: zh-cn
ms.lasthandoff: 02/23/2018

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="bbebe-103">供应商过帐模板</span><span class="sxs-lookup"><span data-stu-id="bbebe-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bbebe-104">供应商过帐模板控制将供应商交易记录过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="bbebe-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="bbebe-105">供应商过帐模板</span><span class="sxs-lookup"><span data-stu-id="bbebe-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="bbebe-106">供应商过帐模板能让您将总帐科目和文档设置分配给所有供应商、一组供应商或单个供应商。</span><span class="sxs-lookup"><span data-stu-id="bbebe-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="bbebe-107">这些设置将在您创建采购订单、供应商发票和现金付款时使用。</span><span class="sxs-lookup"><span data-stu-id="bbebe-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="bbebe-108">对于某些交易记录，您可以选择不同于在此页面中为交易记录设置的模板的其他过帐模板，并且您选择的过帐模板优先。</span><span class="sxs-lookup"><span data-stu-id="bbebe-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="bbebe-109">默认过帐模板是在“应付账款参数”页上的“分类帐”和“销售税”快速选项卡中定义的。</span><span class="sxs-lookup"><span data-stu-id="bbebe-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="bbebe-110">然后，默认过帐模板自动包括到新文档的标题中，在那里您可以根据需要将其更改为不同的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="bbebe-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="bbebe-111">您还可以将过帐定义与“交易记录过帐定义”页中的交易记录过帐类型关联。</span><span class="sxs-lookup"><span data-stu-id="bbebe-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="bbebe-112">过帐定义控制到总帐的供应商交易记录过帐，而不是过帐模板。</span><span class="sxs-lookup"><span data-stu-id="bbebe-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="bbebe-113">创建过帐模板</span><span class="sxs-lookup"><span data-stu-id="bbebe-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="bbebe-114">**设置**</span><span class="sxs-lookup"><span data-stu-id="bbebe-114">**Setup**</span></span>

<span data-ttu-id="bbebe-115">指定在使用所选过帐模板对交易记录进行过帐时所使用的会计科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="bbebe-116">为所选的过帐模板选择帐户编码；只要可能，还选择帐户/组编号。</span><span class="sxs-lookup"><span data-stu-id="bbebe-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="bbebe-117">在过帐过程中，定位每个交易记录的最合适过帐模板的方法是搜索针对性最强的帐户编码、帐号或组编号组合，其优先级如下：</span><span class="sxs-lookup"><span data-stu-id="bbebe-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="bbebe-118">**“帐户编码”**字段值</span><span class="sxs-lookup"><span data-stu-id="bbebe-118">**Account code** field value</span></span> | <span data-ttu-id="bbebe-119">**“帐户/组编号”**字段值</span><span class="sxs-lookup"><span data-stu-id="bbebe-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="bbebe-120">搜索优先级</span><span class="sxs-lookup"><span data-stu-id="bbebe-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="bbebe-121">**表**</span><span class="sxs-lookup"><span data-stu-id="bbebe-121">**Table**</span></span>                    | <span data-ttu-id="bbebe-122">特定供应商帐户</span><span class="sxs-lookup"><span data-stu-id="bbebe-122">Specific vendor account</span></span>                     | <span data-ttu-id="bbebe-123">1</span><span class="sxs-lookup"><span data-stu-id="bbebe-123">1</span></span>               |
| <span data-ttu-id="bbebe-124">**组**</span><span class="sxs-lookup"><span data-stu-id="bbebe-124">**Group**</span></span>                    | <span data-ttu-id="bbebe-125">分配给供应商的供应商组</span><span class="sxs-lookup"><span data-stu-id="bbebe-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="bbebe-126">2</span><span class="sxs-lookup"><span data-stu-id="bbebe-126">2</span></span>               |
| <span data-ttu-id="bbebe-127">**全部**</span><span class="sxs-lookup"><span data-stu-id="bbebe-127">**All**</span></span>                      | <span data-ttu-id="bbebe-128">空白</span><span class="sxs-lookup"><span data-stu-id="bbebe-128">Blank</span></span>                                       | <span data-ttu-id="bbebe-129">3</span><span class="sxs-lookup"><span data-stu-id="bbebe-129">3</span></span>               |

<span data-ttu-id="bbebe-130">如果您希望所有供应商交易记录具有相同的过帐模板，请在“帐户编码”字段中使用“全部”，从而仅建立一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="bbebe-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="bbebe-131">指定以下值设置您的过帐模板：</span><span class="sxs-lookup"><span data-stu-id="bbebe-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bbebe-132">字段</span><span class="sxs-lookup"><span data-stu-id="bbebe-132">Field</span></span></th>
<th><span data-ttu-id="bbebe-133">描述</span><span class="sxs-lookup"><span data-stu-id="bbebe-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbebe-134"><strong>过帐模板</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="bbebe-135">输入过帐模板的代码。</span><span class="sxs-lookup"><span data-stu-id="bbebe-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="bbebe-136">例如，您可以创建两个过帐模板以便用本国币种获取供应商余额的一个科目，用外币获取供应商余额的另一个科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="bbebe-137">您可以对本国币种调用一个科目，对外币调用另一个科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbebe-138"><strong>描述</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="bbebe-139">输入过帐模板的描述。</span><span class="sxs-lookup"><span data-stu-id="bbebe-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbebe-140"><strong>帐户编码</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="bbebe-141">指定过帐模板是应用于特定供应商、一组供应商还是所有供应商：</span><span class="sxs-lookup"><span data-stu-id="bbebe-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="bbebe-142"><strong>表</strong> – 过帐模板应用于单个供应商。</span><span class="sxs-lookup"><span data-stu-id="bbebe-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="bbebe-143">在“帐户/组编号”字段中选择供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="bbebe-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="bbebe-144"><strong>组</strong> – 过帐模板应用于供应商组。</span><span class="sxs-lookup"><span data-stu-id="bbebe-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="bbebe-145">在“帐户/组编号”字段中选择供应商组。</span><span class="sxs-lookup"><span data-stu-id="bbebe-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="bbebe-146"><strong>全部</strong> – 过帐模板应用于所有供应商。</span><span class="sxs-lookup"><span data-stu-id="bbebe-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="bbebe-147">将“帐户/组编号”字段留空。</span><span class="sxs-lookup"><span data-stu-id="bbebe-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbebe-148"><strong>帐户/组编号</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="bbebe-149">如果在“帐户编码”字段中选择了“表”，请选择与该过帐模板相关的供应商的帐号。</span><span class="sxs-lookup"><span data-stu-id="bbebe-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="bbebe-150">如果选择“组”，则选择一个供应商组。</span><span class="sxs-lookup"><span data-stu-id="bbebe-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="bbebe-151">如果选择“全部”，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="bbebe-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbebe-152"><strong>汇总科目</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="bbebe-153">选择将用作该过帐模板所关联到的供应商的汇总科目的会计科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bbebe-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="注意</span><span class="sxs-lookup"><span data-stu-id="bbebe-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="bbebe-155"><strong>注释</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbebe-156">如果“使用过帐定义”开关在“总帐参数”页中处于选定状态，则会使用供应商发票的交易记录过帐定义，而不是汇总科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbebe-157"><strong>结算科目</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="bbebe-158">选择用于现金流量预测的流动性会计科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="bbebe-159">只有启用现金流量预测时，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="bbebe-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbebe-160"><strong>销售税预付款</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="bbebe-161">选择预付款的销售税帐户。</span><span class="sxs-lookup"><span data-stu-id="bbebe-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bbebe-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="注意</span><span class="sxs-lookup"><span data-stu-id="bbebe-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="bbebe-163"><strong>注释</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbebe-164">在付款标记为预付款时使用的过帐模板在“应付账款参数”页的“分类帐和销售税”区域中的“具有预付款日记帐凭证的过帐模板”字段中处于选定状态。</span><span class="sxs-lookup"><span data-stu-id="bbebe-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbebe-165"><strong>到达</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="bbebe-166">选择有关未审核的供应商发票信息过帐到的会计科目编号。</span><span class="sxs-lookup"><span data-stu-id="bbebe-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="bbebe-167">在发票登记簿日记帐中输入此信息。</span><span class="sxs-lookup"><span data-stu-id="bbebe-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="bbebe-168">例如，在发票登记簿中接收供应商发票时，用户输入与发票有关的最基本信息。</span><span class="sxs-lookup"><span data-stu-id="bbebe-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="bbebe-169">在过帐发票登记簿时，交易记录被过帐到在此处输入的科目以及“对方科目”字段中的科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="bbebe-170">在审核发票时，债务将从“到达”科目转移到供应商汇总科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbebe-171"><strong>对方科目</strong></span><span class="sxs-lookup"><span data-stu-id="bbebe-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="bbebe-172">选择用于抵消通过发票登记簿更新的未核准供应商发票的会计科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="bbebe-173">对方科目充当过帐到到达科目的交易记录的对方科目。</span><span class="sxs-lookup"><span data-stu-id="bbebe-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="bbebe-174">因此，该科目包含还未审核的供应商采购。</span><span class="sxs-lookup"><span data-stu-id="bbebe-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="bbebe-175">**表限制**</span><span class="sxs-lookup"><span data-stu-id="bbebe-175">**Table restrictions**</span></span>

<span data-ttu-id="bbebe-176">对于具有所选过帐模板的交易记录，指定交易记录是否将自动结算、是否计算利息、是否签发催款单。</span><span class="sxs-lookup"><span data-stu-id="bbebe-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="bbebe-177">您还可以选择对具有所选过帐模板的交易记录进行结算时所使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="bbebe-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="bbebe-178">指定以下值设置您的过帐模板：</span><span class="sxs-lookup"><span data-stu-id="bbebe-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="bbebe-179">字段</span><span class="sxs-lookup"><span data-stu-id="bbebe-179">Field</span></span>          | <span data-ttu-id="bbebe-180">描述</span><span class="sxs-lookup"><span data-stu-id="bbebe-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbebe-181">**结算**</span><span class="sxs-lookup"><span data-stu-id="bbebe-181">**Settlement**</span></span> | <span data-ttu-id="bbebe-182">选择此选项可启用具有此过帐模板的交易记录的自动结算。</span><span class="sxs-lookup"><span data-stu-id="bbebe-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="bbebe-183">如果清除此选项，您必须通过使用“结算未结交易记录”页来手动结算交易记录。</span><span class="sxs-lookup"><span data-stu-id="bbebe-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="bbebe-184">**取消**</span><span class="sxs-lookup"><span data-stu-id="bbebe-184">**Cancel**</span></span>     | <span data-ttu-id="bbebe-185">如果您希望能够取消具有此过帐模板的交易记录，请选择此选项。</span><span class="sxs-lookup"><span data-stu-id="bbebe-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="bbebe-186">**关闭**</span><span class="sxs-lookup"><span data-stu-id="bbebe-186">**Close**</span></span>      | <span data-ttu-id="bbebe-187">选择在您关闭具有此过帐模板的交易记录时希望更改为的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="bbebe-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="bbebe-188">在完全结算某一交易记录后，该交易记录被视为已关闭。</span><span class="sxs-lookup"><span data-stu-id="bbebe-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






