---
title: "转换记帐或申报币种"
description: 
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 363543f8befacbf2e1b3ab28e6b9f14a5caf3c10
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a><span data-ttu-id="a38d4-102">转换记帐或申报币种</span><span class="sxs-lookup"><span data-stu-id="a38d4-102">Convert accounting or reporting currencies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a38d4-103">必须更改该记帐币种或申报币种的公司有两个选项。</span><span class="sxs-lookup"><span data-stu-id="a38d4-103">A company that must change its accounting currency or reporting currency has two options.</span></span> <span data-ttu-id="a38d4-104">第一个选项是创建一个新公司并全新开始。</span><span class="sxs-lookup"><span data-stu-id="a38d4-104">The first option is to create a new company and start fresh.</span></span> <span data-ttu-id="a38d4-105">第二个选项是运行记帐和申报币种转换流程。</span><span class="sxs-lookup"><span data-stu-id="a38d4-105">The second option is to run the accounting and reporting currency conversion process.</span></span> <span data-ttu-id="a38d4-106">这是一个运行时间很长的流程，会更改系统中的每个交易记录。</span><span class="sxs-lookup"><span data-stu-id="a38d4-106">This is a very long-running process that changes every transaction in the system.</span></span> <span data-ttu-id="a38d4-107">在流程可以运行之前，必须进行某些设置。</span><span class="sxs-lookup"><span data-stu-id="a38d4-107">Some setup is also required before the process can be run.</span></span>

## <a name="preparing-the-legal-entity-for-currency-conversion"></a><span data-ttu-id="a38d4-108">为币种转换准备法人</span><span class="sxs-lookup"><span data-stu-id="a38d4-108">Preparing the legal entity for currency conversion</span></span>
<span data-ttu-id="a38d4-109">在可以转换法人的币种之前，您必须为客户和供应商帐户恢复所有外币重估金额，然后关闭上个会计年度。</span><span class="sxs-lookup"><span data-stu-id="a38d4-109">Before you can convert the legal entity’s currency, you must revert any foreign currency revaluation amounts for customer and vendor accounts, and close the previous fiscal years.</span></span> <span data-ttu-id="a38d4-110">您还必须为转换准备数据库，然后对要进行币种转换的法人的帐户做出所需的更改。</span><span class="sxs-lookup"><span data-stu-id="a38d4-110">You must also prepare the database for the conversion, and then make the required changes to the legal entity’s account that is undergoing the currency conversion.</span></span> <span data-ttu-id="a38d4-111">在您完成了币种转换后，您必须完成一些附加程序。</span><span class="sxs-lookup"><span data-stu-id="a38d4-111">After you have completed a currency conversion, you must complete some additional procedures.</span></span> <span data-ttu-id="a38d4-112">您必须对账已转换金额中的舍入尾差、重新计算业务统计数据、分录分类账交易记录、限制对转换工具的访问并为客户和供应商账户重估外币金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-112">You must reconcile rounding differences in converted amounts, recalculate business statistics, journalize the ledger transactions, limit access to the conversion tool, and revalue foreign currency amounts for customer and vendor accounts.</span></span>

## <a name="setting-up-accounts-for-automatic-transactions"></a><span data-ttu-id="a38d4-113">为自动交易记录设置帐户</span><span class="sxs-lookup"><span data-stu-id="a38d4-113">Setting up accounts for automatic transactions</span></span>
<span data-ttu-id="a38d4-114">在币种转换流程中，损益或尾差会过帐到在**“自动交易记录帐户”**页上定义的帐户。</span><span class="sxs-lookup"><span data-stu-id="a38d4-114">During the currency conversion process, gains or losses, or penny differences, are posted to the accounts that are defined on the **Accounts for automatic transactions** page.</span></span> <span data-ttu-id="a38d4-115">在转换流程运行前，主科目必须分配到以下类型的交易记录：</span><span class="sxs-lookup"><span data-stu-id="a38d4-115">Main accounts must be assigned to the following types of transaction before the conversion process is run:</span></span>

-   <span data-ttu-id="a38d4-116">记帐币种折算收益</span><span class="sxs-lookup"><span data-stu-id="a38d4-116">Accounting currency conversion gain</span></span>
-   <span data-ttu-id="a38d4-117">记帐币种折算损失</span><span class="sxs-lookup"><span data-stu-id="a38d4-117">Accounting currency conversion loss</span></span>
-   <span data-ttu-id="a38d4-118">以记帐币种表示的尾差</span><span class="sxs-lookup"><span data-stu-id="a38d4-118">Penny difference in accounting currency</span></span>
-   <span data-ttu-id="a38d4-119">以申报币种表示的尾差</span><span class="sxs-lookup"><span data-stu-id="a38d4-119">Penny difference in reporting currency</span></span>
-   <span data-ttu-id="a38d4-120">年结</span><span class="sxs-lookup"><span data-stu-id="a38d4-120">Year-end result</span></span>

## <a name="posting-rounding-differences-and-sum-recalculations"></a><span data-ttu-id="a38d4-121">过帐舍入尾差和合计重新计算</span><span class="sxs-lookup"><span data-stu-id="a38d4-121">Posting rounding differences and sum recalculations</span></span>
<span data-ttu-id="a38d4-122">以下信息说明化整时可能发生的差异：</span><span class="sxs-lookup"><span data-stu-id="a38d4-122">The following information explains where differences in rounding might occur:</span></span>

-   <span data-ttu-id="a38d4-123">如果产品价格已转换为 0（零），将生成一份报告，其中显示在转换前的产品编号、模块类型、价格和单位。</span><span class="sxs-lookup"><span data-stu-id="a38d4-123">If product prices have been converted to 0 (zero), a report is generated that shows the product number, module type, price before the conversion, and unit.</span></span>
-   <span data-ttu-id="a38d4-124">增值税和总帐之间的化整差额过帐到普通记帐日志。</span><span class="sxs-lookup"><span data-stu-id="a38d4-124">Rounding differences between sales tax and the general ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="a38d4-125">重新计算重估外币金额、客户和供应商交易记录金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-125">Foreign currency revaluation amounts are recalculated, and customer and vendor transaction amounts are recalculated.</span></span>
-   <span data-ttu-id="a38d4-126">为每个客户和供应商交易记录的化整差额创建客户和供应商结算记录。</span><span class="sxs-lookup"><span data-stu-id="a38d4-126">Customer and vendor settlement records are created for rounding differences for each customer and vendor transaction.</span></span>
-   <span data-ttu-id="a38d4-127">将客户和供应商的舍入差额过账至普通记账日志。</span><span class="sxs-lookup"><span data-stu-id="a38d4-127">Rounding differences for customers and vendors are posted to the general journal.</span></span>
-   <span data-ttu-id="a38d4-128">重新计算在已关帐库存交易记录中的已结算的成本金额和成本调整金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-128">Settled cost amounts and cost adjustment amounts in closed inventory transactions are recalculated.</span></span>
-   <span data-ttu-id="a38d4-129">将库存管理中的舍入差额过帐到普通记帐日志。</span><span class="sxs-lookup"><span data-stu-id="a38d4-129">Rounding differences in Inventory management are posted to the general journal.</span></span>
-   <span data-ttu-id="a38d4-130">重新计算现有库存量。</span><span class="sxs-lookup"><span data-stu-id="a38d4-130">On-hand inventory is recalculated.</span></span>
-   <span data-ttu-id="a38d4-131">重新计算在分类帐日志中的总金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-131">Total amounts in ledger journals are recalculated.</span></span>
-   <span data-ttu-id="a38d4-132">重新计算分类帐结算单。</span><span class="sxs-lookup"><span data-stu-id="a38d4-132">Ledger closing sheets are recalculated.</span></span>
-   <span data-ttu-id="a38d4-133">重新计算帐户余额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-133">Ledger balances are recalculated.</span></span>
-   <span data-ttu-id="a38d4-134">将在总帐中的舍入差额过帐到普通记帐日志。</span><span class="sxs-lookup"><span data-stu-id="a38d4-134">Rounding differences in General ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="a38d4-135">重新计算未结的分录。</span><span class="sxs-lookup"><span data-stu-id="a38d4-135">Opening ledger transactions are recalculated.</span></span>
-   <span data-ttu-id="a38d4-136">计算在帐户余额中的最终余额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-136">The final amount in the ledger balances is calculated.</span></span>

<span data-ttu-id="a38d4-137">如果您转换新的分类帐会计币种，在重新计算总金额或过帐舍入差额期间产生错误时，必须关闭“**日记帐记帐币种转换**”页。</span><span class="sxs-lookup"><span data-stu-id="a38d4-137">If you're converting to a new ledger accounting currency, and an error occurs during the recalculation of total amounts or the posting of rounding differences, you must close the **Ledger accounting currency conversion** page.</span></span> <span data-ttu-id="a38d4-138">然后总金额会重新计算，并且舍入差额将过帐。</span><span class="sxs-lookup"><span data-stu-id="a38d4-138">The total amounts are then recalculated, and the rounding differences are posted.</span></span>

## <a name="processing-the-currency-conversion"></a><span data-ttu-id="a38d4-139">处理币种转换</span><span class="sxs-lookup"><span data-stu-id="a38d4-139">Processing the currency conversion</span></span>
<span data-ttu-id="a38d4-140">当您开始转换币种转换流程时，所有用户都必须从系统退出。</span><span class="sxs-lookup"><span data-stu-id="a38d4-140">When you start the currency conversion process, all users must be signed out of the system.</span></span> <span data-ttu-id="a38d4-141">您必须定义新的分类帐或申报币种和汇率。</span><span class="sxs-lookup"><span data-stu-id="a38d4-141">You must define the new ledger or reporting currency, and the exchange rates.</span></span> <span data-ttu-id="a38d4-142">当您单击**“确定”**时，该流程会运行并更新系统中的每个交易记录。</span><span class="sxs-lookup"><span data-stu-id="a38d4-142">When you click **OK**, the process runs and updates every transaction in the system.</span></span> <span data-ttu-id="a38d4-143">币种转换是很长的流程。</span><span class="sxs-lookup"><span data-stu-id="a38d4-143">Currency conversion is a very long process.</span></span> <span data-ttu-id="a38d4-144">当完成时，您将看到记帐或申报币种在**“分类帐”**页上已更新。</span><span class="sxs-lookup"><span data-stu-id="a38d4-144">When it's completed, you will see that the accounting or reporting currency is updated on the **Ledger** page.</span></span>

## <a name="completing-the-currency-conversion"></a><span data-ttu-id="a38d4-145">完成币种转换</span><span class="sxs-lookup"><span data-stu-id="a38d4-145">Completing the currency conversion</span></span>
<span data-ttu-id="a38d4-146">币种转换后，您必须重新生成所有对账报告以确保所有转换金额都是正确的。</span><span class="sxs-lookup"><span data-stu-id="a38d4-146">After the currency conversion, you must generate all reconciliation reports again to make sure that all converted amounts are correct.</span></span>

-   <span data-ttu-id="a38d4-147">如果分类账记账币种的转换导致了舍入尾差，则将不会通过使用发生舍入尾差的凭证过账这些差额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-147">If the conversion of the ledger accounting currency causes rounding differences, these differences aren't posted by using the voucher where the rounding difference occurred.</span></span> <span data-ttu-id="a38d4-148">相反，将通过为转换过账输入的凭证过账这些差额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-148">Instead, the differences are posted by using the voucher that was entered for the conversion postings.</span></span> <span data-ttu-id="a38d4-149">转换后，按凭证和日期检查的所有报告将包括这些舍入尾差。</span><span class="sxs-lookup"><span data-stu-id="a38d4-149">After the conversion, all reports that check by voucher and date include these rounding differences.</span></span> <span data-ttu-id="a38d4-150">此行为是正确的，并且可以忽略。</span><span class="sxs-lookup"><span data-stu-id="a38d4-150">This behavior is correct and can be ignored.</span></span>
-   <span data-ttu-id="a38d4-151">如果客户和供应商的对帐报表在合计行上显示差异金额，并且在转换前不存在任何差异金额，则必须过帐此差异金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-151">If the customer and vendor reconciliation reports display a difference amount on the total line, and no difference amount existed before the conversion, this difference amount must be posted.</span></span> <span data-ttu-id="a38d4-152">该科目是客户和供应商的汇总科目。</span><span class="sxs-lookup"><span data-stu-id="a38d4-152">The account is the summary account for customers and vendors.</span></span> <span data-ttu-id="a38d4-153">对方科目是针对转换损失或转换收益的会计科目。</span><span class="sxs-lookup"><span data-stu-id="a38d4-153">The offset account is the ledger account for conversion loss or conversion profit.</span></span>

<span data-ttu-id="a38d4-154">当所有分录日志均已删除时，您可以将分录记入日志。</span><span class="sxs-lookup"><span data-stu-id="a38d4-154">When all ledger transaction journals have been deleted, you can journalize the ledger transactions.</span></span> <span data-ttu-id="a38d4-155">单击“**总帐**”&gt;“**定期**”&gt;“**日记帐**”&gt;“**日记帐分录**”。</span><span class="sxs-lookup"><span data-stu-id="a38d4-155">Click **General ledger** &gt; **Periodic** &gt; **Journals** &gt; **Journalizing**.</span></span> <span data-ttu-id="a38d4-156">如果需要重估，您可以在转换币种后重估外币金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-156">You can revalue foreign currency amounts after the currency conversion, if revaluation is required.</span></span> <span data-ttu-id="a38d4-157">您通过为重估选择**“方法”**字段中的**“标准”**，重估外币金额。</span><span class="sxs-lookup"><span data-stu-id="a38d4-157">You revalue foreign currency amounts by selecting **Standard** in the **Method** field for the revaluation.</span></span>

<span data-ttu-id="a38d4-158">有关详细信息，请参阅[将过帐的日记帐条目记入日记帐](tasks/journalize-posted-journal-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="a38d4-158">For more information, see [Journalize posted journal entries](tasks/journalize-posted-journal-entries.md).</span></span>

