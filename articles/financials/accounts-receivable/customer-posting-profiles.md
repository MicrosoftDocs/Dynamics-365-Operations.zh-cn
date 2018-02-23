---
title: "客户过帐模板"
description: "客户过帐模板控制将客户交易记录过帐到总帐。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: d0795a9cb1839c45cf264b0d0f7cffacdc01ea9d
ms.contentlocale: zh-cn
ms.lasthandoff: 02/23/2018

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="c2016-103">客户过帐模板</span><span class="sxs-lookup"><span data-stu-id="c2016-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c2016-104">客户过帐模板控制将客户交易记录过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="c2016-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="c2016-105">客户过帐模板</span><span class="sxs-lookup"><span data-stu-id="c2016-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="c2016-106">客户过帐模板能让您将总帐科目和文档设置分配给所有客户、一组客户或单个客户。</span><span class="sxs-lookup"><span data-stu-id="c2016-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="c2016-107">这些设置将在您创建销售订单、普通发票、现金付款、催款单、利息单和注销时使用。</span><span class="sxs-lookup"><span data-stu-id="c2016-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="c2016-108">对于某些交易记录，您可以选择不同于在此页面中为交易记录设置的模板的其他过帐模板，并且您选择的过帐模板优先。</span><span class="sxs-lookup"><span data-stu-id="c2016-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="c2016-109">默认过帐模板是在“应收账款参数”页上的“分类帐”和“销售税”快速选项卡中定义的。</span><span class="sxs-lookup"><span data-stu-id="c2016-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="c2016-110">然后，默认过帐模板自动包括到新文档的标题中，在那里您可以根据需要将其更改为不同的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="c2016-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="c2016-111">您还可以将过帐定义与“交易记录过帐定义”页中的交易记录过帐类型关联。</span><span class="sxs-lookup"><span data-stu-id="c2016-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="c2016-112">过帐定义控制到总帐的客户交易记录过帐，而不是过帐模板。</span><span class="sxs-lookup"><span data-stu-id="c2016-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="c2016-113">创建过帐模板</span><span class="sxs-lookup"><span data-stu-id="c2016-113">Creating a posting profile</span></span>
<span data-ttu-id="c2016-114">指定在使用所选过帐模板对交易记录进行过帐时所使用的会计科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="c2016-115">为所选的过帐模板选择帐户编码；只要可能，还选择帐户/组编号。</span><span class="sxs-lookup"><span data-stu-id="c2016-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="c2016-116">在过帐过程中，定位每个交易记录的最合适过帐模板的方法是搜索针对性最强的帐户编码、帐号或组编号组合，其优先级如下：</span><span class="sxs-lookup"><span data-stu-id="c2016-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="c2016-117">**“帐户编码”**字段值</span><span class="sxs-lookup"><span data-stu-id="c2016-117">**Account code** field value</span></span> | <span data-ttu-id="c2016-118">**“帐户/组编号”**字段值</span><span class="sxs-lookup"><span data-stu-id="c2016-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="c2016-119">搜索优先级</span><span class="sxs-lookup"><span data-stu-id="c2016-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="c2016-120">**表**</span><span class="sxs-lookup"><span data-stu-id="c2016-120">**Table**</span></span>                    | <span data-ttu-id="c2016-121">特定的客户帐户</span><span class="sxs-lookup"><span data-stu-id="c2016-121">Specific customer account</span></span>                       | <span data-ttu-id="c2016-122">1</span><span class="sxs-lookup"><span data-stu-id="c2016-122">1</span></span>               |
| <span data-ttu-id="c2016-123">**组**</span><span class="sxs-lookup"><span data-stu-id="c2016-123">**Group**</span></span>                    | <span data-ttu-id="c2016-124">分配到客户的客户组</span><span class="sxs-lookup"><span data-stu-id="c2016-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="c2016-125">2</span><span class="sxs-lookup"><span data-stu-id="c2016-125">2</span></span>               |
| <span data-ttu-id="c2016-126">**全部**</span><span class="sxs-lookup"><span data-stu-id="c2016-126">**All**</span></span>                      | <span data-ttu-id="c2016-127">空白</span><span class="sxs-lookup"><span data-stu-id="c2016-127">Blank</span></span>                                           | <span data-ttu-id="c2016-128">3</span><span class="sxs-lookup"><span data-stu-id="c2016-128">3</span></span>               |

<span data-ttu-id="c2016-129">如果您希望所有客户交易记录具有相同的过帐模板，请在“帐户编码”字段中使用“全部”，从而仅建立一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="c2016-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="c2016-130">指定以下值设置您的过帐模板：</span><span class="sxs-lookup"><span data-stu-id="c2016-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c2016-131">字段</span><span class="sxs-lookup"><span data-stu-id="c2016-131">Field</span></span></th>
<th><span data-ttu-id="c2016-132">描述</span><span class="sxs-lookup"><span data-stu-id="c2016-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2016-133"><strong>过帐模板</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="c2016-134">输入过帐模板的代码。</span><span class="sxs-lookup"><span data-stu-id="c2016-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="c2016-135">例如，您可以创建两个过帐模板以便用本国币种获取客户余额的一个科目，用外币获取客户余额的另一个科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="c2016-136">您可以对本国币种调用一个科目，对外币调用另一个科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2016-137"><strong>描述</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="c2016-138">输入过帐模板的描述。</span><span class="sxs-lookup"><span data-stu-id="c2016-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="c2016-139">这仅用于当您在该页面中查看过帐模板时，更好地标识它。</span><span class="sxs-lookup"><span data-stu-id="c2016-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2016-140"><strong>帐户编码</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="c2016-141">指定该过帐模板是应用于单个客户、一组客户还是所有客户：</span><span class="sxs-lookup"><span data-stu-id="c2016-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="c2016-142"><strong>表</strong> – 过帐模板应用于单个客户。</span><span class="sxs-lookup"><span data-stu-id="c2016-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="c2016-143">在“帐户/组编号”字段中选择客户帐户。</span><span class="sxs-lookup"><span data-stu-id="c2016-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="c2016-144"><strong>组</strong> – 过帐模板应用于客户组。</span><span class="sxs-lookup"><span data-stu-id="c2016-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="c2016-145">在“帐户/组编号”字段中选择客户组。</span><span class="sxs-lookup"><span data-stu-id="c2016-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="c2016-146"><strong>全部</strong> – 过帐模板应用于所有客户。</span><span class="sxs-lookup"><span data-stu-id="c2016-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="c2016-147">将“帐户/组编号”字段留空。</span><span class="sxs-lookup"><span data-stu-id="c2016-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2016-148"><strong>帐户/组编号</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="c2016-149">如果在“帐户编码”字段中选择了“表”，请选择与该过帐模板相关的客户的帐号。</span><span class="sxs-lookup"><span data-stu-id="c2016-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="c2016-150">如果选择了“组”，请选择客户组。</span><span class="sxs-lookup"><span data-stu-id="c2016-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="c2016-151">如果选择“全部”，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="c2016-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2016-152"><strong>汇总科目</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="c2016-153">选择将用作与该过帐模板相关的客户的客户汇总科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2016-154"><strong>结算科目</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="c2016-155">选择用于现金流量预测的流动性会计科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="c2016-156">此字段只有在启用现金流量预测时才出现。</span><span class="sxs-lookup"><span data-stu-id="c2016-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2016-157"><strong>销售税预付款</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="c2016-158">选择预付款的销售税帐户。</span><span class="sxs-lookup"><span data-stu-id="c2016-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c2016-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="注意</span><span class="sxs-lookup"><span data-stu-id="c2016-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="c2016-160"><strong>注释</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2016-161">使用“应收账款参数”页指定在将付款标记为预付款过帐模板时使用的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="c2016-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2016-162"><strong>折扣负债科目</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="c2016-163">选择折扣负债科目。</span><span class="sxs-lookup"><span data-stu-id="c2016-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2016-164"><strong>催款单序列</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="c2016-165">选择的催款单序列的标识，以用于过帐模板分配到的客户。</span><span class="sxs-lookup"><span data-stu-id="c2016-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2016-166"><strong>利息代码</strong></span><span class="sxs-lookup"><span data-stu-id="c2016-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="c2016-167">选择利息代码，以用于为过帐模板分配到的客户计算利息。</span><span class="sxs-lookup"><span data-stu-id="c2016-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="c2016-168">**表限制**</span><span class="sxs-lookup"><span data-stu-id="c2016-168">**Table restrictions**</span></span>

<span data-ttu-id="c2016-169">对于具有所选过帐模板的交易记录，指定交易记录是否将自动结算、是否计算利息、是否签发催款单。</span><span class="sxs-lookup"><span data-stu-id="c2016-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="c2016-170">您还可以选择对具有所选过帐模板的交易记录进行结算时所使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="c2016-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="c2016-171">指定以下值设置您的过帐模板：</span><span class="sxs-lookup"><span data-stu-id="c2016-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="c2016-172">字段</span><span class="sxs-lookup"><span data-stu-id="c2016-172">Field</span></span>                 | <span data-ttu-id="c2016-173">描述</span><span class="sxs-lookup"><span data-stu-id="c2016-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2016-174">**结算**</span><span class="sxs-lookup"><span data-stu-id="c2016-174">**Settlement**</span></span>        | <span data-ttu-id="c2016-175">选择此开关可启用具有此过帐模板的交易记录的自动结算。</span><span class="sxs-lookup"><span data-stu-id="c2016-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="c2016-176">如果清除此开关，您必须通过使用“结算未结交易记录”页或“输入客户付款”页来手动结算交易记录。</span><span class="sxs-lookup"><span data-stu-id="c2016-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="c2016-177">**兴趣**</span><span class="sxs-lookup"><span data-stu-id="c2016-177">**Interest**</span></span>          | <span data-ttu-id="c2016-178">如果利息应对使用此模板的客户帐户的未清余额进行计算，则选择此开关。</span><span class="sxs-lookup"><span data-stu-id="c2016-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="c2016-179">如果清除此开关，将不为这些客户计算利息。</span><span class="sxs-lookup"><span data-stu-id="c2016-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="c2016-180">**催款单**</span><span class="sxs-lookup"><span data-stu-id="c2016-180">**Collection letter**</span></span> | <span data-ttu-id="c2016-181">如果催款单应为使用此模板的客户帐户而生成，则选择此开关。</span><span class="sxs-lookup"><span data-stu-id="c2016-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="c2016-182">如果清除此开关，将不为这些客户生成催款单。</span><span class="sxs-lookup"><span data-stu-id="c2016-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="c2016-183">**关闭**</span><span class="sxs-lookup"><span data-stu-id="c2016-183">**Close**</span></span>             | <span data-ttu-id="c2016-184">选择在您关闭具有此过帐模板的交易记录时希望更改为的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="c2016-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="c2016-185">在完全结算某一交易记录后，该交易记录被视为已关闭。</span><span class="sxs-lookup"><span data-stu-id="c2016-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="c2016-186">有关详细信息，请参阅[客户付款概览](../cash-bank-management/tasks/customer-payment-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c2016-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


