---
title: 在线财务合并
description: 此主题介绍总帐中的在线财务合并。
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: b25d52524d1b115a7513a73eafa1aef44e25562d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212293"
---
# <a name="online-financial-consolidations"></a><span data-ttu-id="a6c58-103">在线财务合并</span><span class="sxs-lookup"><span data-stu-id="a6c58-103">Online financial consolidations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6c58-104">此主题介绍总帐中的在线财务合并。</span><span class="sxs-lookup"><span data-stu-id="a6c58-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="a6c58-105">阅读此主题之前，务必阅读[财务合并和货币折算概述](financial-consolidations-currency-translation.md)主题。</span><span class="sxs-lookup"><span data-stu-id="a6c58-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation overview](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="a6c58-106">完成设置后，在 **[在线] 合并** 页中输入合并的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a6c58-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="a6c58-107">完成后，可单击 **确定** 或 **批处理** 处理合并。</span><span class="sxs-lookup"><span data-stu-id="a6c58-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="a6c58-108">条件</span><span class="sxs-lookup"><span data-stu-id="a6c58-108">Criteria</span></span>
<span data-ttu-id="a6c58-109">在 **[在线] 合并** 页的 **条件** 选项卡上，定义合并的金额、期间和数据类型。</span><span class="sxs-lookup"><span data-stu-id="a6c58-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="a6c58-110">![“条件”选项卡](./media/criteria-consolidate-online.png "“条件”选项卡")</span><span class="sxs-lookup"><span data-stu-id="a6c58-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="a6c58-111">下面是此选项卡上的各字段的说明：</span><span class="sxs-lookup"><span data-stu-id="a6c58-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="a6c58-112">**说明** – 输入要合并的期间的精确说明。</span><span class="sxs-lookup"><span data-stu-id="a6c58-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="a6c58-113">**主科目** – 此部分中的字段用于定义将处理的主科目。</span><span class="sxs-lookup"><span data-stu-id="a6c58-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="a6c58-114">**从** 和 **到** – 指定要处理的科目范围。</span><span class="sxs-lookup"><span data-stu-id="a6c58-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="a6c58-115">如果将这些字段保留为空，将把所有公司的所有科目移到合并公司。</span><span class="sxs-lookup"><span data-stu-id="a6c58-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="a6c58-116">因此，如果要合并四个公司，每个公司有一个不同的会计科目表，将在合并公司中创建所有四个公司的所有科目。</span><span class="sxs-lookup"><span data-stu-id="a6c58-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="a6c58-117">**使用合并科目** – 如果将此选项设置为 **是**，**选择合并科目的来源** 字段将可用。</span><span class="sxs-lookup"><span data-stu-id="a6c58-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="a6c58-118">在此字段中，选择应将所有科目合并到 **主科目** 页中设置的合并科目，还是要从一个合并科目组选择科目。</span><span class="sxs-lookup"><span data-stu-id="a6c58-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="a6c58-119">**合并科目组** – 选择要用于合并的主科目映射的组。</span><span class="sxs-lookup"><span data-stu-id="a6c58-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="a6c58-120">**合并期间** – 此部分中的字段用于定义合并期间。</span><span class="sxs-lookup"><span data-stu-id="a6c58-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="a6c58-121">**从** 和 **到** – 指定合并的日期范围。</span><span class="sxs-lookup"><span data-stu-id="a6c58-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="a6c58-122">如果将这些字段留空，将为公司的分类帐日历中定义的所有期间处理合并。</span><span class="sxs-lookup"><span data-stu-id="a6c58-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="a6c58-123">我们建议您不要将这些字段留空。</span><span class="sxs-lookup"><span data-stu-id="a6c58-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="a6c58-124">**包括实际金额** – 如果将此选项设置为 **是**，将合并实际数据。</span><span class="sxs-lookup"><span data-stu-id="a6c58-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="a6c58-125">**包括预算金额** – 如果将此选项设置为 **是**，将合并预算登记的数据。</span><span class="sxs-lookup"><span data-stu-id="a6c58-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="a6c58-126">**在合并过程中重新生成余额** – 建议不要将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a6c58-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="a6c58-127">而是以单独的批处理作业的形式重新生成余额。</span><span class="sxs-lookup"><span data-stu-id="a6c58-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="a6c58-128">**预算模型** – 如果已选择合并预算数据，请使用此部分中的选项定义预算模型。</span><span class="sxs-lookup"><span data-stu-id="a6c58-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="a6c58-129">**从** 和 **到** – 指定要使用的模型范围。</span><span class="sxs-lookup"><span data-stu-id="a6c58-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="a6c58-130">**预算汇率类型** – 选择要用于对预算数据进行货币折算的预算汇率类型。</span><span class="sxs-lookup"><span data-stu-id="a6c58-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="a6c58-131">财务维度</span><span class="sxs-lookup"><span data-stu-id="a6c58-131">Financial dimensions</span></span>
<span data-ttu-id="a6c58-132">在 **财务维度** 选项卡上，定义合并公司中应包含的维度。</span><span class="sxs-lookup"><span data-stu-id="a6c58-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="a6c58-133">若要选择维度，请将 **说明** 字段设置为 **维度**，然后定义合并公司中的维度顺序。</span><span class="sxs-lookup"><span data-stu-id="a6c58-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="a6c58-134">![“财务维度”选项卡](./media/financial-dimensions-cons.png "“财务维度”选项卡")</span><span class="sxs-lookup"><span data-stu-id="a6c58-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="a6c58-135">无论定义哪种顺序，**主科目** 始终是第一个科目段。</span><span class="sxs-lookup"><span data-stu-id="a6c58-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="a6c58-136">法人</span><span class="sxs-lookup"><span data-stu-id="a6c58-136">Legal entities</span></span>
<span data-ttu-id="a6c58-137">在 **法人** 选项卡上，定义合并公司中应包含的公司。</span><span class="sxs-lookup"><span data-stu-id="a6c58-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="a6c58-138">也可以定义这些公司的所有权百分比。</span><span class="sxs-lookup"><span data-stu-id="a6c58-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="a6c58-139">如果指定的所有权低于 100%，将把指定的这个百分比汇总到合并公司。</span><span class="sxs-lookup"><span data-stu-id="a6c58-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="a6c58-140">对于任何折算差额，**折算差额的科目类型** 字段用于从 **自动交易记录科目** 页中的设置选择主科目。</span><span class="sxs-lookup"><span data-stu-id="a6c58-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="a6c58-141">![“法人”选项卡](./media/legal-entities-cons.png "“法人”选项卡")</span><span class="sxs-lookup"><span data-stu-id="a6c58-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="a6c58-142">![自动交易记录帐户页面](./media/accounts-for-automatic-cons.png "自动交易记录帐户页面")</span><span class="sxs-lookup"><span data-stu-id="a6c58-142">![Accounts for automatic transactions page](./media/accounts-for-automatic-cons.png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="a6c58-143">清除</span><span class="sxs-lookup"><span data-stu-id="a6c58-143">Elimination</span></span>
<span data-ttu-id="a6c58-144">在 **清除** 选项卡上，有三个用于处理清除的选项：</span><span class="sxs-lookup"><span data-stu-id="a6c58-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="a6c58-145">设置清除规则，然后在 **方案选项** 字段中选择 **仅方案**。</span><span class="sxs-lookup"><span data-stu-id="a6c58-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="a6c58-146">此选项将在合并过程中处理清除，但是不会在一个步骤中进行所有过帐。</span><span class="sxs-lookup"><span data-stu-id="a6c58-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="a6c58-147">可以在以后过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="a6c58-147">You can post the journal later.</span></span>
- <span data-ttu-id="a6c58-148">设置清除规则，然后在 **方案选项** 字段中选择 **仅过帐**。</span><span class="sxs-lookup"><span data-stu-id="a6c58-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="a6c58-149">此选项将在合并过程中处理清除，并将在一个步骤中进行所有过帐。</span><span class="sxs-lookup"><span data-stu-id="a6c58-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="a6c58-150">通过使用清除日记帐与合并过程分开运行清除方案。</span><span class="sxs-lookup"><span data-stu-id="a6c58-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="a6c58-151">![“清除”选项卡](./media/elimination-cons-onl.png "“清除”选项卡")</span><span class="sxs-lookup"><span data-stu-id="a6c58-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="a6c58-152">有关清除的详细信息，请参阅[清除规则](./elimination-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c58-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="a6c58-153">货币折算</span><span class="sxs-lookup"><span data-stu-id="a6c58-153">Currency translation</span></span>
<span data-ttu-id="a6c58-154">在 **货币折算** 选项卡中，可定义法人、科目和汇率类型，以及汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="a6c58-155">**应用来自以下对象的汇率** 字段中有三个选项：</span><span class="sxs-lookup"><span data-stu-id="a6c58-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="a6c58-156">**合并日期** – 将把合并的日期用于获取汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="a6c58-157">此汇率等同于即期汇率或月底汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="a6c58-158">将看到汇率的预览，但是不能进行编辑。</span><span class="sxs-lookup"><span data-stu-id="a6c58-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="a6c58-159">**交易记录日期**  – 每个交易记录的日期将用于选择汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="a6c58-160">此选项最常用于固定资产，通常称为历史汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="a6c58-161">不能查看此汇率的预览，因为科目范围的各交易记录有大量汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="a6c58-162">**用户定义的汇率** – 选择此选项之后，可以输入所需汇率。</span><span class="sxs-lookup"><span data-stu-id="a6c58-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="a6c58-163">此选项可能对于平均汇率很有用，如果要针对固定汇率进行合并，也可能很有用。</span><span class="sxs-lookup"><span data-stu-id="a6c58-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="a6c58-164">![“货币折算”选项卡](./media/currency-translation-cons-online.png "“货币折算”选项卡")</span><span class="sxs-lookup"><span data-stu-id="a6c58-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6c58-165">其他资源</span><span class="sxs-lookup"><span data-stu-id="a6c58-165">Additional resources</span></span>

<span data-ttu-id="a6c58-166">有关合并和货币折算的详细信息，请参阅此主题的父主题，即[财务合并和货币折算概述](./financial-consolidations-currency-translation.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c58-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation overview](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="a6c58-167">有关可以生成财务报表的方案的信息，请参阅[生成合并的财务报表](./generating-consolidated-financial-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c58-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]