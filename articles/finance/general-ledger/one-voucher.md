---
title: 一个凭证
description: 财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的一个凭证让您可以在单个凭证的上下文中输入多个子分类帐交易记录。
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 2b755dcfbcdf41ada0302fc04f527ce7c309f4bb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186386"
---
# <a name="one-voucher"></a><span data-ttu-id="79cea-103">一个凭证</span><span class="sxs-lookup"><span data-stu-id="79cea-103">One voucher</span></span>

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a><span data-ttu-id="79cea-104">什么是“一个凭证”？</span><span class="sxs-lookup"><span data-stu-id="79cea-104">What is One voucher?</span></span>

<span data-ttu-id="79cea-105">财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的这个现有功能让您可以在单个凭证的上下文中输入多个子分类帐交易记录（客户、供应商、固定资产、项目和银行）。</span><span class="sxs-lookup"><span data-stu-id="79cea-105">The existing functionality for financial journals (the general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions (customer, vendor, fixed assets, project, and bank) in the context of a single voucher.</span></span> <span data-ttu-id="79cea-106">Microsoft 将此功能称为*一个凭证*。</span><span class="sxs-lookup"><span data-stu-id="79cea-106">Microsoft refers to this functionality as *One voucher*.</span></span> <span data-ttu-id="79cea-107">可以使用以下方法之一来创建一个凭证：</span><span class="sxs-lookup"><span data-stu-id="79cea-107">You can create a single voucher by using one of the following methods:</span></span>

- <span data-ttu-id="79cea-108">设置日记帐名称（**总帐** \> **日记帐设置** \> **日记帐名称**），以便**新凭证**字段设置为**仅一个凭证号**。</span><span class="sxs-lookup"><span data-stu-id="79cea-108">Set up the journal name (**General ledger** \> **Journal setup** \> **Journal names**) so that the **New voucher** field is set to **One voucher number only**.</span></span> <span data-ttu-id="79cea-109">您添加到日记帐的各行现在都包括在同一凭证中。</span><span class="sxs-lookup"><span data-stu-id="79cea-109">Every line that you add to the journal is now included in the same voucher.</span></span> <span data-ttu-id="79cea-110">因此，凭证可以作为多行凭证、同一行上的科目/对方科目或组合输入。</span><span class="sxs-lookup"><span data-stu-id="79cea-110">Therefore, the voucher can be entered as a multiline voucher, as an account/offset account on the same line, or as a combination.</span></span>

    <span data-ttu-id="79cea-111">[![单行](./media/same-line.png)](./media/same-line.png)</span><span class="sxs-lookup"><span data-stu-id="79cea-111">[![Single line](./media/same-line.png)](./media/same-line.png)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="79cea-112">“一个凭证”的定义**不**包括日记帐名称设置为**仅一个凭证号**，但用户随后输入仅包含会计科目类型的凭证的情况。</span><span class="sxs-lookup"><span data-stu-id="79cea-112">The definition of One voucher does **not** cover cases where journal names are set up as **One voucher number only**, but the user then enters a voucher that includes only ledger account types.</span></span> <span data-ttu-id="79cea-113">在本主题中，“一个凭证”意味着有单个凭证包含多个供应商、客户、银行、固定资产或项目。</span><span class="sxs-lookup"><span data-stu-id="79cea-113">In this topic, One voucher means that there is a single voucher that contains more than one vendor, customer, bank, fixed asset, or project.</span></span>

- <span data-ttu-id="79cea-114">输入没有对方科目的多行凭证。</span><span class="sxs-lookup"><span data-stu-id="79cea-114">Enter a multiline voucher where there is no offset account.</span></span>

    <span data-ttu-id="79cea-115">[![多行凭证](./media/Multi-line.png)](./media/Multi-line.png)</span><span class="sxs-lookup"><span data-stu-id="79cea-115">[![Multiline voucher](./media/Multi-line.png)](./media/Multi-line.png)</span></span>

- <span data-ttu-id="79cea-116">输入科目和对方科目都包含子分类帐科目类型（如**供应商**/**供应商**、**客户**/**客户**、**供应商**/**客户**或**银行**/**银行**）的凭证。</span><span class="sxs-lookup"><span data-stu-id="79cea-116">Enter a voucher where both the account and the offset account contain a subledger account type, such as **Vendor**/**Vendor**, **Customer**/**Customer**, **Vendor**/**Customer**, or **Bank**/**Bank**.</span></span>

    <span data-ttu-id="79cea-117">[![子分类帐凭证](./media/subledger.png)](./media/subledger.png)</span><span class="sxs-lookup"><span data-stu-id="79cea-117">[![Subledger voucher](./media/subledger.png)](./media/subledger.png)</span></span>

## <a name="issues-with-one-voucher"></a><span data-ttu-id="79cea-118">一个凭证存在的问题</span><span class="sxs-lookup"><span data-stu-id="79cea-118">Issues with One voucher</span></span>

<span data-ttu-id="79cea-119">“一个凭证”功能会在结算、纳税计算、交易记录冲销、子分类帐与总帐的对帐、财务报告等期间导致问题。</span><span class="sxs-lookup"><span data-stu-id="79cea-119">The One voucher functionality causes issues during settlement, tax calculation, transaction reversal, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="79cea-120">（有关结算期间可能发生的问题的详细信息，请参阅如[具有多个客户或供应商记录的单个凭证](https://docs.microsoft.com/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records)。）为了正确工作和报告，这些流程和报告需要交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="79cea-120">(For more information about issues that can occur during settlement, see, for example, [Single voucher with multiple customer or vendor records](https://docs.microsoft.com/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) To work and report correctly, these processes and reports require transaction details.</span></span> <span data-ttu-id="79cea-121">尽管取决于您的组织的设置，某些可能方案仍能正确工作，但当在一个凭证中输入多个交易记录时通常会有问题。</span><span class="sxs-lookup"><span data-stu-id="79cea-121">Although some scenarios might still work correctly, depending on your organization's setup, there are often issues when multiple transactions are entered in one voucher.</span></span>

<span data-ttu-id="79cea-122">例如，您过帐以下多行凭证。</span><span class="sxs-lookup"><span data-stu-id="79cea-122">For example, you post the following multiline voucher.</span></span>

<span data-ttu-id="79cea-123">[![示例](./media/example.png)](./media/example.png)</span><span class="sxs-lookup"><span data-stu-id="79cea-123">[![Example](./media/example.png)](./media/example.png)</span></span>

<span data-ttu-id="79cea-124">然后您在**财务见解**工作区生成**按供应商分类的费用**报表。</span><span class="sxs-lookup"><span data-stu-id="79cea-124">You then generate the **Expenses by vendor** report in the **Financial Insights** workspace.</span></span> <span data-ttu-id="79cea-125">在此报表中，支出帐户余额按供应商组然后按供应商分组。</span><span class="sxs-lookup"><span data-stu-id="79cea-125">On this report, expense account balances are grouped by vendor group and then vendor.</span></span> <span data-ttu-id="79cea-126">当生成报表时，系统不能确定哪些供应商组/供应商发生了 250.00 费用。</span><span class="sxs-lookup"><span data-stu-id="79cea-126">When the report is generated, the system can't determine which vendor groups/vendors incurred the expense of 250.00.</span></span> <span data-ttu-id="79cea-127">因为交易记录明细缺少，系统假定所有 250.00 费用是由在凭证中找到的第一个供应商产生。</span><span class="sxs-lookup"><span data-stu-id="79cea-127">Because transaction details are missing, the system assumes that the whole 250.00 expense was incurred by the first vendor that is found in the voucher.</span></span> <span data-ttu-id="79cea-128">因此，250.00 费用（包含在主科目 600120 的余额中）显示在该供应商组/供应商下。</span><span class="sxs-lookup"><span data-stu-id="79cea-128">Therefore, the 250.00 expense, which is included in the balance for main account 600120, is shown under that vendor group/vendor.</span></span> <span data-ttu-id="79cea-129">但是，凭证中的第一个供应商很有可能不是正确的供应商。</span><span class="sxs-lookup"><span data-stu-id="79cea-129">However, it's very likely that the first vendor in the voucher isn't the correct vendor.</span></span> <span data-ttu-id="79cea-130">因此，报表可能不正确。</span><span class="sxs-lookup"><span data-stu-id="79cea-130">Therefore, the report is probably incorrect.</span></span>

<span data-ttu-id="79cea-131">[![支出](./media/expenses.png)](./media/expenses.png)</span><span class="sxs-lookup"><span data-stu-id="79cea-131">[![Expenses](./media/expenses.png)](./media/expenses.png)</span></span>

## <a name="the-future-of-one-voucher"></a><span data-ttu-id="79cea-132">一个凭证的未来</span><span class="sxs-lookup"><span data-stu-id="79cea-132">The future of One voucher</span></span>

<span data-ttu-id="79cea-133">由于之前所提到的问题，“一个凭证”功能将被废弃。</span><span class="sxs-lookup"><span data-stu-id="79cea-133">Because of the issues that were mentioned earlier, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="79cea-134">但是，因为存在依赖此功能的功能空白，此功能不会一次全部废弃。</span><span class="sxs-lookup"><span data-stu-id="79cea-134">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at one time.</span></span> <span data-ttu-id="79cea-135">而是使用以下计划：</span><span class="sxs-lookup"><span data-stu-id="79cea-135">Instead, the following schedule will be used:</span></span>

- <span data-ttu-id="79cea-136">**2018 年春季发布** – 默认情况下，该功能将通过**总帐参数**页的**常规**选项卡上的**一个凭证可以允许多个交易记录**参数默认关闭。</span><span class="sxs-lookup"><span data-stu-id="79cea-136">**Spring 2018 release** – By default, the functionality will be turned off by default through the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="79cea-137">但是，如果您的组织有属于本主题后面列出的功能空白之一的方案，您可以打开此功能。</span><span class="sxs-lookup"><span data-stu-id="79cea-137">However, you can turn the functionality on if your organization has a scenario that falls into one of the functional gaps that are listed later in this topic.</span></span>

    - <span data-ttu-id="79cea-138">如果客户的业务方案不需要一个凭证，他们不应打开此功能。</span><span class="sxs-lookup"><span data-stu-id="79cea-138">If customers have a business scenario that doesn't require One voucher, they shouldn't turn the functionality on.</span></span> <span data-ttu-id="79cea-139">如果使用此功能，即使存在另一种解决方案，Microsoft 也不会修复本主题后面确定的区域的 "bug"。</span><span class="sxs-lookup"><span data-stu-id="79cea-139">Microsoft won't fix "bugs" in the areas that are identified later in this topic if this functionality is used even though another solution exists.</span></span>
    - <span data-ttu-id="79cea-140">除非需要使用一个凭证来填补其中一个功能空白，否则请停止使用此功能来集成。</span><span class="sxs-lookup"><span data-stu-id="79cea-140">Stop using One voucher for integrations, unless you need the functionality for one of the functional gaps.</span></span>

- <span data-ttu-id="79cea-141">**以后发布** – 将填补所有功能空白。</span><span class="sxs-lookup"><span data-stu-id="79cea-141">**Later releases** – All functional gaps will be filled.</span></span> <span data-ttu-id="79cea-142">**在填补功能空白并提供新功能后，在关闭“一个凭证”之前至少还会留有一年时间**，因为客户和独立软件供应商 (ISV) 必须有足够的时间来对新功能作出反应。</span><span class="sxs-lookup"><span data-stu-id="79cea-142">**After the functional gaps are filled and new features are delivered, it will be at least one year before the One voucher functionality is permanently turned off**, because customers and independent software vendors (ISVs) must have enough time to react to the new functionality.</span></span> <span data-ttu-id="79cea-143">例如，他们可能必须更新其业务流程、实体和集成。</span><span class="sxs-lookup"><span data-stu-id="79cea-143">For example, they might have to update their business processes, entities, and integrations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79cea-144">日记帐名称设置中尚**未**移除**仅一个凭证号**选项。</span><span class="sxs-lookup"><span data-stu-id="79cea-144">The **One voucher number only** option has **not** been removed from the Journal name setup.</span></span> <span data-ttu-id="79cea-145">凭证仅包含会计科目类型时，仍然支持此选项。</span><span class="sxs-lookup"><span data-stu-id="79cea-145">This option is still supported when the voucher contains only ledger account types.</span></span> <span data-ttu-id="79cea-146">客户在使用此设置时应小心谨慎，因为如果使用**仅一个凭证号**选项，但随之输入多个客户、供应商、银行、固定资产或项目，则该凭证将不过帐。</span><span class="sxs-lookup"><span data-stu-id="79cea-146">Customers must be careful when they use this setting, because the voucher won't be posted if they use the **One voucher number only** option but then enter more than one customer, vendor, bank, fixed asset, or project.</span></span> <span data-ttu-id="79cea-147">而且，客户仍然可以在包含**供应商**/**银行**科目类型的单个凭证内输入子分类帐科目类型，如付款。</span><span class="sxs-lookup"><span data-stu-id="79cea-147">Additionally, customers can still enter a mix of subledger account types, such as a payment in a single voucher that contains the **Vendor**/**Bank** account types.</span></span>

## <a name="why-use-one-voucher"></a><span data-ttu-id="79cea-148">为何使用一个凭证？</span><span class="sxs-lookup"><span data-stu-id="79cea-148">Why use One voucher?</span></span>

<span data-ttu-id="79cea-149">基于与客户的对话，Microsoft 汇编了客户使用一个凭证功能或使用原因的以下场景列表。</span><span class="sxs-lookup"><span data-stu-id="79cea-149">Based on conversations with customers, Microsoft has compiled the following list of scenarios where customers use the One voucher functionality or reasons why they use it.</span></span> <span data-ttu-id="79cea-150">这些业务要求中有一些只能使用一个凭证满足。</span><span class="sxs-lookup"><span data-stu-id="79cea-150">Some of these business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="79cea-151">但是，对于很多场景，替代方案即可以满足同一业务要求。</span><span class="sxs-lookup"><span data-stu-id="79cea-151">However, for many scenarios, alternatives can meet the same business requirements.</span></span>

### <a name="scenarios-that-require-one-voucher"></a><span data-ttu-id="79cea-152">需要一个凭证的场景</span><span class="sxs-lookup"><span data-stu-id="79cea-152">Scenarios that require One voucher</span></span>

<span data-ttu-id="79cea-153">以下场景只能使用一个凭证功能完成。</span><span class="sxs-lookup"><span data-stu-id="79cea-153">The following scenarios can be accomplished only by using the One voucher functionality.</span></span> <span data-ttu-id="79cea-154">如果您的组织遇到这些场景案中的任何一个，您必须启用要在凭证中输入的多个交易记录，方法是更改**总帐参数**页上**一个凭证可以允许多个交易记录**参数的设置。。</span><span class="sxs-lookup"><span data-stu-id="79cea-154">If your organization has any of these scenarios, you must enable multiple transactions to be entered in a voucher by changing the setting of the **Allow multiple transactions within one voucher** parameter on the **General ledger parameters** page.</span></span> <span data-ttu-id="79cea-155">这些功能空白将通过以后发布的其他功能填补。</span><span class="sxs-lookup"><span data-stu-id="79cea-155">These functional gaps will be filled through other features in later releases.</span></span>

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a><span data-ttu-id="79cea-156">将汇总窗体中的供应商或客户付款过帐到银行帐户</span><span class="sxs-lookup"><span data-stu-id="79cea-156">Post vendor or customer payments in summary form to a bank account</span></span>

<span data-ttu-id="79cea-157">**场景**组织将供应商和金额列表传达给银行，银行使用此列表代表组织向供应商付款。</span><span class="sxs-lookup"><span data-stu-id="79cea-157">**Scenario** An organization communicates a list of vendors and amounts to its bank, and the bank uses this list to pay the vendors on the organization's behalf.</span></span> <span data-ttu-id="79cea-158">银行通过银行帐户的单次提款形式过帐付款总额。</span><span class="sxs-lookup"><span data-stu-id="79cea-158">The bank posts the sum of the payments as a single withdrawal on the bank account.</span></span>

<span data-ttu-id="79cea-159">仅通过一个凭证支持供应商付款的汇总。</span><span class="sxs-lookup"><span data-stu-id="79cea-159">Summarization of vendor payments is supported only through One voucher.</span></span> <span data-ttu-id="79cea-160">每个供应商输入为一个单独行以在应付帐款子分类帐中维护详细信息。</span><span class="sxs-lookup"><span data-stu-id="79cea-160">Each vendor is entered as a separate line to maintain details in the Accounts payable subledger.</span></span> <span data-ttu-id="79cea-161">不过，所有付款的汇总金额将冲销到银行帐户的一个行。</span><span class="sxs-lookup"><span data-stu-id="79cea-161">However, the summarized amount for all the payments is offset to a single line for the bank account.</span></span> <span data-ttu-id="79cea-162">因此，提款在银行子分类帐中显示为单个汇总金额。</span><span class="sxs-lookup"><span data-stu-id="79cea-162">Therefore, the withdrawal is shown as a single summarized amount in the bank subledger.</span></span>

<span data-ttu-id="79cea-163">**场景**组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。</span><span class="sxs-lookup"><span data-stu-id="79cea-163">**Scenario** An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="79cea-164">客户付款的汇总通常通过存款功能来支持。</span><span class="sxs-lookup"><span data-stu-id="79cea-164">Summarization of customer payments is typically supported through the deposit functionality.</span></span> <span data-ttu-id="79cea-165">但是，如果您在付款方式中使用“过渡”，此场景只通过一个凭证来支持。</span><span class="sxs-lookup"><span data-stu-id="79cea-165">However, if you're using "bridging" on the method of payment, this scenario is supported only through One voucher.</span></span> <span data-ttu-id="79cea-166">客户付款的输入方式与所述的供应商付款汇总相同。</span><span class="sxs-lookup"><span data-stu-id="79cea-166">The customer payments are entered in the same manner that is described for vendor payment summarization.</span></span>

### <a name="mechanism-to-group-transactions-from-a-business-event"></a><span data-ttu-id="79cea-167">用于分组业务事件交易记录的机制</span><span class="sxs-lookup"><span data-stu-id="79cea-167">Mechanism to group transactions from a business event</span></span>

<span data-ttu-id="79cea-168">**场景**组织有触发多个交易的单个业务事件。</span><span class="sxs-lookup"><span data-stu-id="79cea-168">**Scenario** An organization has a single business event that triggers multiple transactions.</span></span> <span data-ttu-id="79cea-169">不过，会计部门希望同时查看会计条目以提高可审计性。</span><span class="sxs-lookup"><span data-stu-id="79cea-169">However, the Accounting department wants to view the accounting entries together for better auditability.</span></span>

<span data-ttu-id="79cea-170">如果组织必须同时查看业务事件的会计条目，则必须使用一个凭证。</span><span class="sxs-lookup"><span data-stu-id="79cea-170">If an organization must view the accounting entries from a business event together, it must use One voucher.</span></span> 

### <a name="country-specific-features"></a><span data-ttu-id="79cea-171">特定于国家/地区的功能</span><span class="sxs-lookup"><span data-stu-id="79cea-171">Country-specific features</span></span>

<span data-ttu-id="79cea-172">**场景**波兰的欧共体统一单证 (SAD) 功能当前要求使用单一凭证。</span><span class="sxs-lookup"><span data-stu-id="79cea-172">**Scenario** The Single Administrative Document (SAD) feature for Poland currently requires that a single voucher be used.</span></span> <span data-ttu-id="79cea-173">在分组选项可用于此功能前，您必须继续使用“一个凭证”功能。</span><span class="sxs-lookup"><span data-stu-id="79cea-173">Until a grouping option is available for this feature, you must continue to use the One voucher functionality.</span></span> <span data-ttu-id="79cea-174">可能还有其他一些特定于国家/地区的功能需要“一个凭证”功能。</span><span class="sxs-lookup"><span data-stu-id="79cea-174">There may be additional country-specific features that require the One voucher functionality.</span></span>

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a><span data-ttu-id="79cea-175">在多个“行”有税款的客户预付款付款日记帐</span><span class="sxs-lookup"><span data-stu-id="79cea-175">Customer prepayment payment journal that has taxes on multiple "lines"</span></span>

<span data-ttu-id="79cea-176">在此场景中，因为此交易记录模拟客户订单的行，单个凭证中的客户为同一客户。</span><span class="sxs-lookup"><span data-stu-id="79cea-176">In this scenario, the customers in the single voucher are the same customer, because the transaction simulates the lines of a customer order.</span></span> <span data-ttu-id="79cea-177">预付款必须在单个凭证中输入，因为税金计算必须在客户支付的单个付款的行中进行。</span><span class="sxs-lookup"><span data-stu-id="79cea-177">The prepayment must be entered in a single voucher, because the tax calculation must be made on the "lines" of the single payment that the customer made.</span></span>

### <a name="customer-reimbursement"></a><span data-ttu-id="79cea-178">客户偿还</span><span class="sxs-lookup"><span data-stu-id="79cea-178">Customer reimbursement</span></span>

<span data-ttu-id="79cea-179">**场景**客户进行订单的预付款，并且订单的行具有必须为预付款记录的不同税。</span><span class="sxs-lookup"><span data-stu-id="79cea-179">**Scenario** A customer makes a prepayment for an order, and the lines of the order have different taxes that must be recorded for the prepayment.</span></span> <span data-ttu-id="79cea-180">预付款客户付款是一个模拟订单行的交易记录，因此，相应的税可为每一行的金额记录。</span><span class="sxs-lookup"><span data-stu-id="79cea-180">The prepayment customer payment is one transaction that simulates the lines of the order, so that the appropriate tax can be recorded for the amount on each line.</span></span>

<span data-ttu-id="79cea-181">如果“偿还”定期任务从应收帐款模块运行，它将创建将余额从客户移至供应商的交易记录。</span><span class="sxs-lookup"><span data-stu-id="79cea-181">If the Reimbursement periodic task is run from the Accounts receivable module, it creates a transaction to move the balance from a customer to a vendor.</span></span> <span data-ttu-id="79cea-182">对于此场景，“一个凭证”必须用于偿还客户。</span><span class="sxs-lookup"><span data-stu-id="79cea-182">For this scenario, One voucher must be used to reimburse the customer.</span></span>

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a><span data-ttu-id="79cea-183">固定资产维护：采纳折旧、拆分资产、计算处置折旧</span><span class="sxs-lookup"><span data-stu-id="79cea-183">Fixed asset maintenance: Catch-up depreciation, split asset, calculate depreciation on disposal</span></span>
<span data-ttu-id="79cea-184">以下固定资产交易记录还在单个凭证中创建多个交易记录：</span><span class="sxs-lookup"><span data-stu-id="79cea-184">The following fixed asset transactions also create multiple transactions in a single voucher:</span></span>

- <span data-ttu-id="79cea-185">对资产进行其他购置，以及计算“采纳”折旧。</span><span class="sxs-lookup"><span data-stu-id="79cea-185">An additional acquisition is made on an asset, and "catch-up" depreciation is calculated.</span></span>
- <span data-ttu-id="79cea-186">拆分资产。</span><span class="sxs-lookup"><span data-stu-id="79cea-186">An asset is split.</span></span>
- <span data-ttu-id="79cea-187">计算处置折旧的参数打开，然后处置资产。</span><span class="sxs-lookup"><span data-stu-id="79cea-187">A parameter to calculate depreciation on disposal is turned on, and then the asset is disposed of.</span></span>
- <span data-ttu-id="79cea-188">资产的服务日期在购置日期之前。</span><span class="sxs-lookup"><span data-stu-id="79cea-188">An asset's service date is before the acquisition date.</span></span> <span data-ttu-id="79cea-189">因此，折旧调整将过帐。</span><span class="sxs-lookup"><span data-stu-id="79cea-189">Therefore, a depreciation adjustment is posted.</span></span>

### <a name="bills-of-exchange-and-promissory-notes"></a><span data-ttu-id="79cea-190"> 汇票和本票</span><span class="sxs-lookup"><span data-stu-id="79cea-190">Bills of exchange and promissory notes</span></span>
<span data-ttu-id="79cea-191">汇票和本票需要使用“一个凭证”，因为交易记录根据付款状态将客户或供应商余额从一个应收帐款/应付帐款会计科目移至另一个。</span><span class="sxs-lookup"><span data-stu-id="79cea-191">Bills of exchange and promissory notes require that One voucher be used, because the transactions move the customer or vendor balance from one Accounts receivable/Accounts payable ledger account to another, based on the state of the payment.</span></span>

## <a name="scenarios-that-dont-require-one-voucher"></a><span data-ttu-id="79cea-192">不需要一个凭证的场景</span><span class="sxs-lookup"><span data-stu-id="79cea-192">Scenarios that don't require One voucher</span></span>

<span data-ttu-id="79cea-193">以下场景可以通过其他方法完成，不应使用“一个凭证”功能。</span><span class="sxs-lookup"><span data-stu-id="79cea-193">The following scenarios can be accomplished through other means and should not use the One voucher functionality.</span></span>

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a><span data-ttu-id="79cea-194">将汇总窗体中的客户付款过帐到银行帐户</span><span class="sxs-lookup"><span data-stu-id="79cea-194">Post customer payments in summary form to the bank account</span></span>

<span data-ttu-id="79cea-195">组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。</span><span class="sxs-lookup"><span data-stu-id="79cea-195">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="79cea-196">不在付款方式中使用“过渡”时，通过存款功能支持客户付款的汇总。</span><span class="sxs-lookup"><span data-stu-id="79cea-196">Summarization of customer payments is supported through the deposit functionality when "bridging" isn't used on the method of payment.</span></span>

### <a name="netting"></a><span data-ttu-id="79cea-197">净额结算</span><span class="sxs-lookup"><span data-stu-id="79cea-197">Netting</span></span>

<span data-ttu-id="79cea-198">在净额结算中，因为供应商和客户是同一方，供应商和客户的余额根据彼此进行净额结算。</span><span class="sxs-lookup"><span data-stu-id="79cea-198">In netting, the balances for a vendor and customer are netted against each other, because the vendor and customer are the same party.</span></span> <span data-ttu-id="79cea-199">此方法可以最小化组织和客户/供应商当事方之间的货币交换。</span><span class="sxs-lookup"><span data-stu-id="79cea-199">This approach minimizes the exchange of money between an organization and the customer/vendor party.</span></span>

<span data-ttu-id="79cea-200">净额结算可以通过在单独凭证中输入增加和减少，然后过帐冲销以清算会计科目来完成。</span><span class="sxs-lookup"><span data-stu-id="79cea-200">Netting can be accomplished by entering the increase and decrease in separate vouchers, and then posting the offset to a clearing ledger account.</span></span>

### <a name="post-in-summary-to-the-general-ledger"></a><span data-ttu-id="79cea-201">汇总过帐到总帐</span><span class="sxs-lookup"><span data-stu-id="79cea-201">Post in summary to the general ledger</span></span>

<span data-ttu-id="79cea-202">组织通常想要过帐到汇总窗体中的总帐以最小化数据量。</span><span class="sxs-lookup"><span data-stu-id="79cea-202">Organizations often want to post to the general ledger in summary form to minimize the amount of data.</span></span> <span data-ttu-id="79cea-203">但是，这些组织通常仍需要维护交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="79cea-203">However, those organizations typically still require that the transaction details be maintained.</span></span> <span data-ttu-id="79cea-204">在通过单个凭证在汇总窗体中完成过帐时，交易记录明细未知且无法维护。</span><span class="sxs-lookup"><span data-stu-id="79cea-204">When posting is done in summary form through a single voucher, the transaction details aren't known and can't be maintained.</span></span>

- <span data-ttu-id="79cea-205">因为交易记录明细当前不能维护，我们建议组织**不要**使用“一个凭证”在汇总窗体中过帐。</span><span class="sxs-lookup"><span data-stu-id="79cea-205">Because the transaction details currently can't be maintained, we recommend that organization **not** use One voucher to post in summary form.</span></span>
- <span data-ttu-id="79cea-206">删除一个凭证支持后，原始凭证和会计框架可以在日记帐中实现。</span><span class="sxs-lookup"><span data-stu-id="79cea-206">After support for One voucher is removed, the Source document and Accounting frameworks can be implemented in the journals.</span></span> <span data-ttu-id="79cea-207">这些框架然后将维护交易记录明细并支持汇总到总帐。</span><span class="sxs-lookup"><span data-stu-id="79cea-207">These frameworks will then maintain the transaction details and support summarization into the general ledger.</span></span>


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a><span data-ttu-id="79cea-208">将多项未过帐付款结算到同一发票</span><span class="sxs-lookup"><span data-stu-id="79cea-208">Settle multiple unposted payments to the same invoice</span></span>

<span data-ttu-id="79cea-209">此场景通常在客户可以使用多种付款方式支付采购的零售组织中遇到。</span><span class="sxs-lookup"><span data-stu-id="79cea-209">This scenario is typically found in retail organizations where customers can use multiple methods of payment to pay for purchases.</span></span> <span data-ttu-id="79cea-210">在此场景中，组织必须可以记录多个未过帐付款并对照客户发票进行结算。</span><span class="sxs-lookup"><span data-stu-id="79cea-210">In this scenario, the organization must be able to record multiple unposted payments and settle them against the customer invoice.</span></span>

<span data-ttu-id="79cea-211">Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月）中添加的新功能支持对照单个发票结算多个未过帐的付款。</span><span class="sxs-lookup"><span data-stu-id="79cea-211">A new feature that was added in Microsoft Dynamics 365 for Operations version 1611 (November 2016) enables multiple unposted payments to be settled against a single invoice.</span></span> <span data-ttu-id="79cea-212">不必再在单个凭证中输入多个客户付款。</span><span class="sxs-lookup"><span data-stu-id="79cea-212">Multiple customer payments no longer have to be entered in a single voucher.</span></span>

### <a name="import-bank-statement-transactions"></a><span data-ttu-id="79cea-213">导入银行对帐单交易记录</span><span class="sxs-lookup"><span data-stu-id="79cea-213">Import bank statement transactions</span></span>

<span data-ttu-id="79cea-214">银行经常代表组织支付和接收付款，这些交易记录通过从银行收到的文件记录在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="79cea-214">Banks often pay and receive payments on an organization's behalf, and those transactions are recorded in Finance through a file that is received from the bank.</span></span> <span data-ttu-id="79cea-215">组织通常希望在文件中使用银行对帐单编号将这些交易记录分组到一起。</span><span class="sxs-lookup"><span data-stu-id="79cea-215">Organizations often want to group together those transactions by using the bank statement number in the file.</span></span> <span data-ttu-id="79cea-216">由于每个交易记录都在银行对帐单中详细显示，银行子分类帐中不需要进行汇总。</span><span class="sxs-lookup"><span data-stu-id="79cea-216">Because each transaction is shown in detail on the bank statement, no summarization is required in the bank subledger.</span></span>

<span data-ttu-id="79cea-217">交易记录可以使用日记帐中的其他字段分组，例如日记帐批处理号或单据编号。</span><span class="sxs-lookup"><span data-stu-id="79cea-217">Transactions can be grouped by using other fields on the journal, such as the journal batch number itself or the document number.</span></span>


### <a name="transfer-balances"></a><span data-ttu-id="79cea-218">转移余额</span><span class="sxs-lookup"><span data-stu-id="79cea-218">Transfer balances</span></span>

<span data-ttu-id="79cea-219">组织可能必须将一个供应商的余额转账给其他供应商，或者由于错误，或者因为其他供应商接收了负债。</span><span class="sxs-lookup"><span data-stu-id="79cea-219">An organization might have to transfer a balance from one vendor to another vendor, either because of a mistake or because another vendor has taken over the liability.</span></span> <span data-ttu-id="79cea-220">此类型转账对于如**客户**和**银行**等科目类型也会发生。</span><span class="sxs-lookup"><span data-stu-id="79cea-220">Transfers of this type also occur for account types such as **Customer** and **Bank**.</span></span>

<span data-ttu-id="79cea-221">将余额从一个帐户（供应商、客户、银行等）转账到其他帐户可以通过单独的凭证完成，并且可以过帐冲销来清算会计科目。</span><span class="sxs-lookup"><span data-stu-id="79cea-221">Balance transfers from one account (vendor, customer, bank, and so on) to another account can be done through separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

### <a name="enter-beginning-balances"></a><span data-ttu-id="79cea-222">输入期初余额</span><span class="sxs-lookup"><span data-stu-id="79cea-222">Enter beginning balances</span></span>

<span data-ttu-id="79cea-223">组织通常作为一个凭证交易记录输入子分类帐科目（供应商、客户、固定资产等）的期初余额。</span><span class="sxs-lookup"><span data-stu-id="79cea-223">Organizations often enter beginning balances for subledger accounts (vendors, customers, fixed assets, and so on) as one voucher transaction.</span></span> <span data-ttu-id="79cea-224">每个子分类帐科目的期初余额可以输入为单独的凭证，并且可以过帐冲销来清算会计科目。</span><span class="sxs-lookup"><span data-stu-id="79cea-224">Beginning balances for each subledger account can be entered as separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a><span data-ttu-id="79cea-225">更正过帐的客户或供应商单据的会计条目</span><span class="sxs-lookup"><span data-stu-id="79cea-225">Correct the accounting entry of a posted customer or vendor document</span></span>

<span data-ttu-id="79cea-226">组织可能必须更正已过帐发票的会计条目的应收帐款或应付帐款会计科目，但该发票不能通过其他机制冲销或更正。</span><span class="sxs-lookup"><span data-stu-id="79cea-226">An organization might have to correct the Accounts receivable or Accounts payable ledger account for an accounting entry of a posted invoice, but that invoice can't be reversed or corrected through another mechanism.</span></span>

<span data-ttu-id="79cea-227">如果必须对应收帐款或应付帐款会计科目进行更正，必须直接对该会计科目进行调整。</span><span class="sxs-lookup"><span data-stu-id="79cea-227">If a correction must be made to the Accounts receivable or Accounts payable ledger account, an adjustment must be made directly to the ledger account.</span></span> <span data-ttu-id="79cea-228">调整不能由通过供应商或客户的过帐进行。</span><span class="sxs-lookup"><span data-stu-id="79cea-228">The adjustment can't be made by posting through the vendor or customer.</span></span> <span data-ttu-id="79cea-229">此方法要求调整在“停机”期间进行，以便会计科目可以暂时允许手动输入。</span><span class="sxs-lookup"><span data-stu-id="79cea-229">This approach requires that the adjustment be made during a "down time," so that the ledger account can temporarily allow manual entry.</span></span>

### <a name="the-system-allows-it"></a><span data-ttu-id="79cea-230">系统允许使用</span><span class="sxs-lookup"><span data-stu-id="79cea-230">"The system allows it"</span></span>

<span data-ttu-id="79cea-231">组织使用“一个凭证”功能经常只是因为系统允许他们使用，而不了解影响。</span><span class="sxs-lookup"><span data-stu-id="79cea-231">Organizations often use the One voucher functionality merely because the system lets them use it, without understanding the implications.</span></span>
