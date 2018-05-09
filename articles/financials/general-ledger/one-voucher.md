---
title: "一个凭证"
description: "财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的一个凭证让您可以在单个凭证的上下文中输入多个子分类帐交易记录。"
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 54da64f4407d2fca9bd48e2014ff327640a4d5aa
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="one-voucher"></a><span data-ttu-id="b0301-103">一个凭证</span><span class="sxs-lookup"><span data-stu-id="b0301-103">One voucher</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  <span data-ttu-id="b0301-104">此功能在 Dynamics 365 for Finance and Operations 版本 8.0 中提供，将于 2018 年春季的发布中推出。</span><span class="sxs-lookup"><span data-stu-id="b0301-104">This functionality will be available in Dynamics 365 for Finance and Operations version 8.0, which will be available in the Spring '18 release.</span></span>   

<a name="what-is-one-voucher"></a><span data-ttu-id="b0301-105">什么是“一个凭证”？</span><span class="sxs-lookup"><span data-stu-id="b0301-105">What is "One voucher"?</span></span>
======================

<span data-ttu-id="b0301-106">财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的这个现有功能让您可以在单个凭证的上下文中输入多个子分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="b0301-106">The existing functionality for financial journals (general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="b0301-107">我们将此功能称为“一个凭证”。</span><span class="sxs-lookup"><span data-stu-id="b0301-107">We refer to this functionality as "One voucher."</span></span> <span data-ttu-id="b0301-108">可以使用以下方法之一来创建“一个凭证”：</span><span class="sxs-lookup"><span data-stu-id="b0301-108">You can create One voucher by using one of the following methods:</span></span>

-   <span data-ttu-id="b0301-109">设置日记帐名称（**总帐** \> **日记帐设置** \> **日记帐名称**），以便**新凭证**字段设置为**仅一个凭证号**。</span><span class="sxs-lookup"><span data-stu-id="b0301-109">Set up the journal name (**General ledger** \> **Journal setup** \>**Journal names**) so that the **New voucher** field is set to **One voucher number only**.</span></span> <span data-ttu-id="b0301-110">\* 您添加到日记帐的各行现在都包括在同一凭证中。</span><span class="sxs-lookup"><span data-stu-id="b0301-110">\* Every line that you add to the journal is now included on the same voucher.</span></span> <span data-ttu-id="b0301-111">由于每一行添加到同一个凭证，凭证可以作为多行凭证、同一行上的科目/对方科目或组合输入。</span><span class="sxs-lookup"><span data-stu-id="b0301-111">Because every line is added to the same voucher, the voucher can be entered as a multiline voucher, as an account/offset account on the same line, or as a combination.</span></span>

<span data-ttu-id="b0301-112">[![单行](./media/same-line.png)](./media/same-line.png)</span><span class="sxs-lookup"><span data-stu-id="b0301-112">[![Single line](./media/same-line.png)](./media/same-line.png)</span></span>
 
> [!IMPORTANT] 
> *  <span data-ttu-id="b0301-113">请注意，“一个凭证”的定义中不包含设置为**仅一个凭证号**的日记帐名称，而用户则输入仅包含日记帐科目类型的凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-113">Note that the definition of ‘One voucher’ does NOT include journal names that are set up as **One voucher number** only and the user then enters a voucher which only includes Ledger account types.</span></span>  <span data-ttu-id="b0301-114">在本文中，“一个凭证”意味着有一个凭证包含多个供应商、客户、银行、固定资产或项目。</span><span class="sxs-lookup"><span data-stu-id="b0301-114">In this document, ‘One voucher’ means that there is one voucher that contains more than one vendor, customer, bank, fixed asset, or project.</span></span> 

-   <span data-ttu-id="b0301-115">输入没有对方科目的多行凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-115">Enter a multiline voucher where there is no offset account.</span></span>

<span data-ttu-id="b0301-116">[![多行凭证](./media/Multi-line.png)](./media/Multi-line.png)</span><span class="sxs-lookup"><span data-stu-id="b0301-116">[![Multiline voucher](./media/Multi-line.png)](./media/Multi-line.png)</span></span>

-   <span data-ttu-id="b0301-117">输入科目和对方科目都包含子分类帐科目类型（如供应商/供应商、客户/客户、供应商/客户或银行/银行）的凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-117">Enter a voucher where both the account and the offset account contain a subledger account type, such as vendor/vendor, Customer/customer, vendor/customer, or bank/bank.</span></span>

<span data-ttu-id="b0301-118">[![子分类帐凭证](./media/subledger.png)](./media/subledger.png)</span><span class="sxs-lookup"><span data-stu-id="b0301-118">[![Subledger voucher](./media/subledger.png)](./media/subledger.png)</span></span>

<a name="issues-with-one-voucher"></a><span data-ttu-id="b0301-119">一个凭证存在的问题</span><span class="sxs-lookup"><span data-stu-id="b0301-119">Issues with One voucher</span></span>
=======================

<span data-ttu-id="b0301-120">“一个凭证”功能会在结算、纳税计算、子分类帐与总帐的对帐、财务报告等期间导致问题。</span><span class="sxs-lookup"><span data-stu-id="b0301-120">The One voucher functionality causes issues during settlement, tax calculation, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="b0301-121">（例如，有关结算期间可能发生的问题的详细信息，请参阅[具有多个客户或供应商记录的单个凭证](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records)。）为了正确工作和报告，这些流程和报告需要交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="b0301-121">(For example, for more information about issues that can occur during settlement, see [Single voucher with multiple customer or vendor records](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) To work and report correctly, these processes and reports require transaction details.</span></span> <span data-ttu-id="b0301-122">尽管根据您的组织的设置，某些可能方案仍能正确工作，但当在一个凭证中输入多个交易记录时通常会有问题。</span><span class="sxs-lookup"><span data-stu-id="b0301-122">Although some scenarios might still work correctly, based on your organization's setup, there are often issues when multiple transactions are entered in one voucher.</span></span>

<span data-ttu-id="b0301-123">例如，您过帐以下多行凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-123">For example, you post the following multiline voucher.</span></span>

<span data-ttu-id="b0301-124">[![示例](./media/example.png)](./media/example.png)</span><span class="sxs-lookup"><span data-stu-id="b0301-124">[![Example](./media/example.png)](./media/example.png)</span></span>

<span data-ttu-id="b0301-125">然后您在**财务见解**工作区生成**按供应商分类的费用**报表。</span><span class="sxs-lookup"><span data-stu-id="b0301-125">You then generate the **Expenses by vendor** report in the **Financial Insights** workspace.</span></span> <span data-ttu-id="b0301-126">供应商组和随后的供应商下的报表组支出帐户余额。</span><span class="sxs-lookup"><span data-stu-id="b0301-126">The report groups expense account balances under vendor group and then vendor.</span></span> <span data-ttu-id="b0301-127">当生成报表时，系统不能确定哪些供应商组/供应商发生了 250.00 费用。</span><span class="sxs-lookup"><span data-stu-id="b0301-127">When generating the report, the system can't determine which vendor groups/vendors incurred the expense of 250.00.</span></span> <span data-ttu-id="b0301-128">因为交易记录明细缺少，系统假定所有 250.00 是由在凭证中找到的第一个供应商产生。</span><span class="sxs-lookup"><span data-stu-id="b0301-128">Because transaction details are missing, the system assumes the whole 250.00 was incurred by the first vendor found in the voucher.</span></span> <span data-ttu-id="b0301-129">250.00（包含在主科目 600120 的余额中）然后显示在该供应商组/供应商下。</span><span class="sxs-lookup"><span data-stu-id="b0301-129">The 250.00, which is included in the balance for main account 600120, is then shown under that vendor group/vendor.</span></span> <span data-ttu-id="b0301-130">凭证中的第一个供应商很有可能不是正确的供应商，因此，报表不正确。</span><span class="sxs-lookup"><span data-stu-id="b0301-130">It’s very likely that the first vendor in the voucher was not the correct vendor, so the report is incorrect.</span></span>

<span data-ttu-id="b0301-131">[![支出](./media/expenses.png)](./media/expenses.png)</span><span class="sxs-lookup"><span data-stu-id="b0301-131">[![Expenses](./media/expenses.png)](./media/expenses.png)</span></span>

<a name="the-future-of-one-voucher"></a><span data-ttu-id="b0301-132">一个凭证的未来</span><span class="sxs-lookup"><span data-stu-id="b0301-132">The future of One voucher</span></span>
=========================

<span data-ttu-id="b0301-133">由于之前所说的问题，“一个凭证”功能将被废弃。</span><span class="sxs-lookup"><span data-stu-id="b0301-133">Because of the issues that were stated earlier, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="b0301-134">但是，因为存在依赖此功能的功能空白，此功能不会一次全部废弃。</span><span class="sxs-lookup"><span data-stu-id="b0301-134">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at once.</span></span> <span data-ttu-id="b0301-135">我们将使用以下计划：</span><span class="sxs-lookup"><span data-stu-id="b0301-135">Instead, we will use the following schedule:</span></span> 

- <span data-ttu-id="b0301-136">**2018 年春季发布** – 此功能将通过总帐参数默认关闭。</span><span class="sxs-lookup"><span data-stu-id="b0301-136">**Spring 2018 release** – The functionality will be turned off by default through a General ledger parameter.</span></span> <span data-ttu-id="b0301-137">但是，如果您的组织有本主题后面列出的业务方案空白的方案，您可以打开此功能。</span><span class="sxs-lookup"><span data-stu-id="b0301-137">However, you can turn the functionality on if your organization has a scenario that falls in the business scenario gaps that are listed later in this topic.</span></span>

  -   <span data-ttu-id="b0301-138">如果客户的业务方案不需要一个凭证，则不要打开此功能。</span><span class="sxs-lookup"><span data-stu-id="b0301-138">If a customer has a business scenario that doesn't require One voucher, don't turn the functionality on.</span></span> <span data-ttu-id="b0301-139">如果使用此功能，即使存在另一种解决方案，我们也不会修复本主题后面确定的区域的 "bug"。</span><span class="sxs-lookup"><span data-stu-id="b0301-139">We won't fix "bugs" in the areas that were identified later in this topic if this functionality is used even though another solution exists.</span></span>

  -   <span data-ttu-id="b0301-140">除非需要使用一个凭证来填补其中一个功能空白，否则请停止使用此功能来集成到 Microsoft Dynamics 365 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="b0301-140">Stop using One voucher for integrations into Microsoft Dynamics 365 Finance and Operations, unless the functionality is required for one of the functional gaps.</span></span>

- <span data-ttu-id="b0301-141">**2018 年秋季及以后发布** – 将填补此功能空白。</span><span class="sxs-lookup"><span data-stu-id="b0301-141">**Fall 2018 and later releases** – The functional gaps will be filled.</span></span> <span data-ttu-id="b0301-142">在填补功能空白后，一个凭证功能将永久关闭。</span><span class="sxs-lookup"><span data-stu-id="b0301-142">After the functional gaps are filled, the One voucher functionality will be permanently turned off.</span></span>

- > [!IMPORTANT]
  > <span data-ttu-id="b0301-143">请注意，日记帐名称设置中尚未移除**仅一个凭证号**选项。</span><span class="sxs-lookup"><span data-stu-id="b0301-143">Please note that the **One voucher number only** option has NOT been removed from the Journal name setup.</span></span>  <span data-ttu-id="b0301-144">凭证仅包含会计科目类型时，仍然支持此选项。</span><span class="sxs-lookup"><span data-stu-id="b0301-144">This option is still supported when the voucher only contains Ledger account types.</span></span>  <span data-ttu-id="b0301-145">客户在使用此设置时应小心谨慎，因为如果使用**仅一个凭证号**，但随之输入多个客户、供应商、银行、固定资产或项目，则该凭证将不过帐。</span><span class="sxs-lookup"><span data-stu-id="b0301-145">Customers must be careful when using this setting because the voucher will not post if they use **One voucher number only** but then enter more than one customer, vendor, bank, fixed asset, or project.</span></span>  <span data-ttu-id="b0301-146">不过，客户仍然可以在包含“供应商/银行”科目类型的单个凭证内输入子分类帐科目类型，如付款。</span><span class="sxs-lookup"><span data-stu-id="b0301-146">Also, customers can still enter a mix of subledger account types, such as a payment within a single voucher that contains account types of Vendor/Bank.</span></span>  

<a name="why-use-one-voucher"></a><span data-ttu-id="b0301-147">为何使用一个凭证？</span><span class="sxs-lookup"><span data-stu-id="b0301-147">Why use One voucher?</span></span>
====================

<span data-ttu-id="b0301-148">基于与客户的对话，我们汇编了客户使用一个凭证功能或使用原因的以下场景列表。</span><span class="sxs-lookup"><span data-stu-id="b0301-148">Based on conversations with customers, we have compiled the following list of scenarios where customers use the One voucher functionality or reasons why they use it.</span></span> <span data-ttu-id="b0301-149">这些业务要求中有一些只能使用一个凭证满足。</span><span class="sxs-lookup"><span data-stu-id="b0301-149">Some of these business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="b0301-150">但是，对于很多场景，替代方案即可以满足同一业务要求。</span><span class="sxs-lookup"><span data-stu-id="b0301-150">However, for many scenarios, alternatives can meet the same business requirements.</span></span>

<a name="scenarios-that-require-one-voucher"></a><span data-ttu-id="b0301-151">需要一个凭证的场景</span><span class="sxs-lookup"><span data-stu-id="b0301-151">Scenarios that require One voucher</span></span>
----------------------------------

<span data-ttu-id="b0301-152">以下场景只能使用一个凭证功能完成。</span><span class="sxs-lookup"><span data-stu-id="b0301-152">The following scenarios can be accomplished only by using the One voucher functionality.</span></span> <span data-ttu-id="b0301-153">这些功能空白将通过 2018 年秋季及以后发布的其他功能填补。</span><span class="sxs-lookup"><span data-stu-id="b0301-153">These functional gaps will be filled through other features in the Fall 2018 and later releases.</span></span>

-   <span data-ttu-id="b0301-154">**将汇总窗体中的供应商或客户付款过帐到银行帐户**</span><span class="sxs-lookup"><span data-stu-id="b0301-154">**Post vendor or customer payments in summary form to a bank account**</span></span>

    -   <span data-ttu-id="b0301-155">组织将供应商和金额列表传达给银行，银行使用此列表代表组织向供应商付款。</span><span class="sxs-lookup"><span data-stu-id="b0301-155">An organization communicates a list of vendors and amounts to its bank, and the bank uses this list to pay the vendors on the organization's behalf.</span></span> <span data-ttu-id="b0301-156">银行通过银行帐户的单次提款形式过帐付款总额。</span><span class="sxs-lookup"><span data-stu-id="b0301-156">The bank posts the sum of the payments as a single withdrawal on the bank account.</span></span>

>   <span data-ttu-id="b0301-157">仅通过一个凭证支持供应商付款的汇总。</span><span class="sxs-lookup"><span data-stu-id="b0301-157">Summarization of vendor payments is supported only through One voucher.</span></span> <span data-ttu-id="b0301-158">每个供应商作为单独一行输入以维护应付帐款子分类帐的明细，但所有付款的汇总金额是对银行帐户的一个行的冲销。</span><span class="sxs-lookup"><span data-stu-id="b0301-158">Each vendor is entered as a separate line to maintain detail in the Accounts payable subledger, but the summarized amount for all the payments is offset to a single line for the bank account.</span></span> <span data-ttu-id="b0301-159">因此，提款在银行子分类帐中显示为单个汇总金额。</span><span class="sxs-lookup"><span data-stu-id="b0301-159">Therefore, the withdrawal is shown as a single summarized amount in the bank subledger.</span></span>

-   <span data-ttu-id="b0301-160">组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。</span><span class="sxs-lookup"><span data-stu-id="b0301-160">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

>   <span data-ttu-id="b0301-161">客户付款的汇总通常通过存款功能来支持。</span><span class="sxs-lookup"><span data-stu-id="b0301-161">Summarization of customer payments is typically supported through the deposit functionality.</span></span> <span data-ttu-id="b0301-162">但是，如果您在付款方式中使用“过渡”，此场景只通过一个凭证来支持。</span><span class="sxs-lookup"><span data-stu-id="b0301-162">However, if you're using "bridging" on the method of payment, this scenario is supported only through One voucher.</span></span> <span data-ttu-id="b0301-163">客户付款的输入方式与所述的供应商付款汇总相同。</span><span class="sxs-lookup"><span data-stu-id="b0301-163">The customer payments are entered in the same manner that is described for vendor payment summarization.</span></span>

-   <span data-ttu-id="b0301-164">**用于分组业务事件交易记录的机制**</span><span class="sxs-lookup"><span data-stu-id="b0301-164">**Mechanism to group transactions from a business event**</span></span>

    -   <span data-ttu-id="b0301-165">组织有触发多个交易的单个业务事件。</span><span class="sxs-lookup"><span data-stu-id="b0301-165">An organization has a single business event that triggers multiple transactions.</span></span> <span data-ttu-id="b0301-166">不过，会计部门希望同时查看会计条目以提高可审计性。</span><span class="sxs-lookup"><span data-stu-id="b0301-166">However, the Accounting department wants to view the accounting entries together for better auditability.</span></span>

>   <span data-ttu-id="b0301-167">如果组织必须同时查看业务事件的会计条目，则必须使用一个凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-167">If an organization must view the accounting entries from a business event together, it must use One voucher.</span></span> 

- <span data-ttu-id="b0301-168">**特定于国家/地区的功能**</span><span class="sxs-lookup"><span data-stu-id="b0301-168">**Country-specific features**</span></span>

  -   <span data-ttu-id="b0301-169">波兰的欧共体统一单证 (SAD) 功能当前要求使用单一凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-169">The Single Administrative Document (SAD) feature for Poland currently requires that a single voucher be used.</span></span> <span data-ttu-id="b0301-170">在分组选项可用于此功能前，您必须继续使用“一个凭证”功能。</span><span class="sxs-lookup"><span data-stu-id="b0301-170">Until a grouping option is available for this feature, you must continue to use the One voucher functionality.</span></span> <span data-ttu-id="b0301-171">可能还有其他一些特定于国家/地区的功能需要“一个凭证”功能。</span><span class="sxs-lookup"><span data-stu-id="b0301-171">There may be additional country-specific features that require the One voucher functionality.</span></span>

- <span data-ttu-id="b0301-172">**在多个“行”有税款的客户预付款付款日记帐**</span><span class="sxs-lookup"><span data-stu-id="b0301-172">**Customer prepayment payment journal that has taxes on multiple "lines"**</span></span>

  -   <span data-ttu-id="b0301-173">客户进行订单的预付款，并且订单的行具有必须为预付款记录的不同税。</span><span class="sxs-lookup"><span data-stu-id="b0301-173">A customer makes a prepayment for an order, and the lines of the order have different taxes that must be recorded for the prepayment.</span></span> <span data-ttu-id="b0301-174">预付款客户付款是一个模拟订单行的交易记录，因此，相应的税可为每一行的金额记录。</span><span class="sxs-lookup"><span data-stu-id="b0301-174">The prepayment customer payment is one transaction that simulates the lines of the order, so that the appropriate tax can be recorded for the amount on each line.</span></span>

<span data-ttu-id="b0301-175">在此场景中，因为此交易记录模拟客户订单的行，单个凭证中的客户为同一客户。</span><span class="sxs-lookup"><span data-stu-id="b0301-175">In this scenario, the customers in the single voucher are the same customer, because the transaction simulates the lines of a customer order.</span></span> <span data-ttu-id="b0301-176">预付款必须在单个凭证中输入，因为税金计算必须在客户支付的单个付款的行中进行。</span><span class="sxs-lookup"><span data-stu-id="b0301-176">The prepayment must be entered in a single voucher, because the tax calculation must be made on the "lines" of the single payment that the customer made.</span></span>

-   <span data-ttu-id="b0301-177">**固定资产维护：采纳折旧、拆分资产、计算处置折旧**</span><span class="sxs-lookup"><span data-stu-id="b0301-177">**Fixed asset maintenance: Catch-up depreciation, split asset, calculate depreciation on disposal**</span></span>

<span data-ttu-id="b0301-178">以下固定资产交易记录还在单个凭证中创建多个交易记录：</span><span class="sxs-lookup"><span data-stu-id="b0301-178">The following fixed asset transactions also create multiple transactions within a single voucher:</span></span>
-   <span data-ttu-id="b0301-179">对资产进行其他购置，以及计算“采纳”折旧。</span><span class="sxs-lookup"><span data-stu-id="b0301-179">An additional acquisition is made on an asset and ‘catch-up’ depreciation is calculated.</span></span>
-   <span data-ttu-id="b0301-180">拆分资产。</span><span class="sxs-lookup"><span data-stu-id="b0301-180">An asset is split.</span></span>
-   <span data-ttu-id="b0301-181">计算处置折旧的参数启用，然后处置资产。</span><span class="sxs-lookup"><span data-stu-id="b0301-181">A parameter to calculate depreciation on disposal is enabled and then the asset is disposed.</span></span>

<a name="scenarios-that-dont-require-one-voucher"></a><span data-ttu-id="b0301-182">不需要一个凭证的场景</span><span class="sxs-lookup"><span data-stu-id="b0301-182">Scenarios that don't require One voucher</span></span>
----------------------------------------

<span data-ttu-id="b0301-183">以下场景可以通过其他方法完成，不应使用一个凭证。</span><span class="sxs-lookup"><span data-stu-id="b0301-183">The following scenarios can be accomplished through other means and should not use One voucher.</span></span>

-   <span data-ttu-id="b0301-184">**将汇总窗体中的客户付款过帐到银行帐户**</span><span class="sxs-lookup"><span data-stu-id="b0301-184">**Post customer payments in summary form to the bank account**</span></span>

<span data-ttu-id="b0301-185">组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。</span><span class="sxs-lookup"><span data-stu-id="b0301-185">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="b0301-186">不在付款方式中使用过渡时，通过存款功能支持客户付款的汇总。</span><span class="sxs-lookup"><span data-stu-id="b0301-186">Summarization of customer payments is supported through the deposit  functionality when bridging isn't used on the method of payment.</span></span>

-   <span data-ttu-id="b0301-187">**净额结算**</span><span class="sxs-lookup"><span data-stu-id="b0301-187">**Netting**</span></span>

<span data-ttu-id="b0301-188">在净额结算中，因为供应商和客户是同一方，供应商和客户的余额根据彼此进行净额结算。</span><span class="sxs-lookup"><span data-stu-id="b0301-188">In netting, the balances for a vendor and customer are netted against each other because the vendor and customer are the same party.</span></span> <span data-ttu-id="b0301-189">此方法可以最小化组织和客户/供应商当事方之间的货币交换。</span><span class="sxs-lookup"><span data-stu-id="b0301-189">This approach minimizes the exchange of money between an organization and the customer/vendor party.</span></span>

<span data-ttu-id="b0301-190">净额结算可以通过在单独凭证中输入增加和减少，并过帐冲销以清算会计科目来完成。</span><span class="sxs-lookup"><span data-stu-id="b0301-190">Netting can be accomplished by entering the increase and decrease in separate vouchers, and posting the offset to a clearing ledger account.</span></span>

-   <span data-ttu-id="b0301-191">**汇总过帐到总帐**</span><span class="sxs-lookup"><span data-stu-id="b0301-191">**Post in summary to the general ledger**</span></span>

<span data-ttu-id="b0301-192">组织通常想要汇总过帐总帐以最小化数据量。</span><span class="sxs-lookup"><span data-stu-id="b0301-192">Organizations often want to post to the general ledger in summary to minimize the amount of data.</span></span> <span data-ttu-id="b0301-193">但是，组织通常仍需要维护交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="b0301-193">However, the organizations typically still require that the transaction detail be maintained.</span></span> <span data-ttu-id="b0301-194">在通过单个凭证完成汇总过帐时，交易记录明细未知且无法维护。</span><span class="sxs-lookup"><span data-stu-id="b0301-194">When posting is done in summary through a single voucher, the transaction detail isn't known and can't be maintained.</span></span>

   -   <span data-ttu-id="b0301-195">因为交易记录明细当前不能维护，我们建议不使用一个凭证进行汇总过帐。</span><span class="sxs-lookup"><span data-stu-id="b0301-195">Because the transaction detail currently can't be maintained, we recommend that One voucher not be used to post in summary.</span></span>
   -   <span data-ttu-id="b0301-196">删除一个凭证支持后，我们可以在日记帐中实现原始凭证和会计框架。</span><span class="sxs-lookup"><span data-stu-id="b0301-196">After support for One voucher is removed, we can implement the Source document and Accounting frameworks into the journals.</span></span> <span data-ttu-id="b0301-197">这些框架然后将维护交易记录明细并支持汇总到总帐。</span><span class="sxs-lookup"><span data-stu-id="b0301-197">These frameworks, will then maintain the transaction detail and support summarization into the general ledger.</span></span>

-   <span data-ttu-id="b0301-198">**将多项未过帐付款结算到同一发票**</span><span class="sxs-lookup"><span data-stu-id="b0301-198">**Settle multiple unposted payments to the same invoice**</span></span>

<span data-ttu-id="b0301-199">此场景通常在客户可以使用多种付款方式支付采购的零售组织中遇到。</span><span class="sxs-lookup"><span data-stu-id="b0301-199">This scenario is typically found in retail organizations where customers can use multiple methods of payment to pay for purchases.</span></span> <span data-ttu-id="b0301-200">在此场景中，组织必须可以记录多个未过帐付款并对照客户发票进行结算。</span><span class="sxs-lookup"><span data-stu-id="b0301-200">In this scenario, the organization must be able to record multiple unposted payments and settle them against the customer invoice.</span></span>

<span data-ttu-id="b0301-201">Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月）中添加的新功能支持对照单个发票结算多个未过帐的付款。</span><span class="sxs-lookup"><span data-stu-id="b0301-201">A new feature that was added in Microsoft Dynamics 365 for Operations version 1611 (November 2016) enables multiple unposted payments to be settled against a single invoice.</span></span> <span data-ttu-id="b0301-202">不必再在单个凭证中输入多个客户付款。</span><span class="sxs-lookup"><span data-stu-id="b0301-202">Multiple customer payments no longer have to be entered in a single voucher.</span></span>

-   <span data-ttu-id="b0301-203">**导入银行对帐单交易记录**</span><span class="sxs-lookup"><span data-stu-id="b0301-203">**Import bank statement transactions**</span></span>

<span data-ttu-id="b0301-204">银行经常代表组织支付和接收付款，这些交易记录通过从银行收到的文件记录在 Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="b0301-204">Banks often pay and receive payments on an organization's behalf, and these transactions are recorded in Finance and Operations through a file that is received from the bank.</span></span> <span data-ttu-id="b0301-205">组织通常希望在文件中使用银行对帐单编号将这些交易记录分组到一起。</span><span class="sxs-lookup"><span data-stu-id="b0301-205">Organizations often want to group together those transactions by using the bank statement number in the file.</span></span> <span data-ttu-id="b0301-206">由于每个交易记录都在银行对帐单中详细显示，银行子分类帐中不需要进行汇总。</span><span class="sxs-lookup"><span data-stu-id="b0301-206">Because each transaction is shown in detail on the bank statement, no summarization is required in the bank subledger.</span></span>

<span data-ttu-id="b0301-207">交易记录可以使用日记帐中的其他字段分组，例如日记帐批处理号或单据编号。</span><span class="sxs-lookup"><span data-stu-id="b0301-207">Transactions can be grouped by using other fields on the journal, such as the journal batch number itself or the document number.</span></span>

-   <span data-ttu-id="b0301-208">**转移余额**</span><span class="sxs-lookup"><span data-stu-id="b0301-208">**Transfer balances**</span></span>

<span data-ttu-id="b0301-209">组织可能必须将一个供应商的余额转账给其他供应商，或者由于错误，或者因为其他供应商接收了负债。</span><span class="sxs-lookup"><span data-stu-id="b0301-209">An organization might have to transfer a balance from one vendor to another vendor, either because of a mistake or because another vendor has taken over the liability.</span></span> <span data-ttu-id="b0301-210">此类型转账对于如客户和银行帐户等科目类型也会发生。</span><span class="sxs-lookup"><span data-stu-id="b0301-210">Transfers of this type also occur for account types such as customers and bank accounts.</span></span>

<span data-ttu-id="b0301-211">将余额从一个帐户（供应商、客户、银行帐户等）转账到其他帐户可以通过单独的凭证完成，并且可以过帐冲销来清算会计科目。</span><span class="sxs-lookup"><span data-stu-id="b0301-211">Balance transfers from one account (vendor, customer, bank account, and so on) to another account can be done through separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="b0301-212">**输入期初余额**</span><span class="sxs-lookup"><span data-stu-id="b0301-212">**Enter beginning balances**</span></span>

<span data-ttu-id="b0301-213">组织通常作为一个凭证交易记录输入子分类帐科目（供应商、客户、固定资产等）的期初余额。</span><span class="sxs-lookup"><span data-stu-id="b0301-213">Organizations often enter beginning balances for subledger accounts (vendors, customers, fixed assets, and so on) as one voucher transaction.</span></span> <span data-ttu-id="b0301-214">每个子分类帐科目的期初余额可以输入为单独的凭证，并且可以过帐冲销来清算会计科目。</span><span class="sxs-lookup"><span data-stu-id="b0301-214">Beginning balances for each subledger account can be entered as separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="b0301-215">**更正过帐的客户或供应商单据的会计条目**</span><span class="sxs-lookup"><span data-stu-id="b0301-215">**Correct the accounting entry of a posted customer or vendor document**</span></span>

<span data-ttu-id="b0301-216">组织可能必须更正已过帐发票的会计条目的应收帐款或应付帐款会计科目，但该发票不能通过其他机制冲销或更正。</span><span class="sxs-lookup"><span data-stu-id="b0301-216">An organization might have to correct the Accounts receivable or Accounts payable ledger account for an accounting entry of a posted invoice, but that invoice can't be reversed or corrected through another mechanism.</span></span>

<span data-ttu-id="b0301-217">如果必须对应收帐款或应付帐款会计科目进行更正，必须直接对该会计科目进行调整。</span><span class="sxs-lookup"><span data-stu-id="b0301-217">If a correction must be made to the accounts receivable or accounts payable ledger account, an adjustment must be made directly to the ledger account.</span></span> <span data-ttu-id="b0301-218">调整不能由通过供应商或客户的过帐进行。</span><span class="sxs-lookup"><span data-stu-id="b0301-218">The adjustment can't be made by posting through the vendor or customer.</span></span> <span data-ttu-id="b0301-219">此方法要求调整在“停机”期间进行，以便会计科目可以暂时允许手动输入。</span><span class="sxs-lookup"><span data-stu-id="b0301-219">This approach requires that the adjustment be made during a "down time," so that the ledger account can temporarily allow manual entry.</span></span>

-   <span data-ttu-id="b0301-220">**“系统允许使用”**</span><span class="sxs-lookup"><span data-stu-id="b0301-220">**"The system allows it"**</span></span>

<span data-ttu-id="b0301-221">组织使用“一个凭证”功能经常只是因为系统允许他们使用，而不了解影响。</span><span class="sxs-lookup"><span data-stu-id="b0301-221">Organizations often use the One voucher functionality merely because the system lets them use it, without understanding the implications.</span></span>

