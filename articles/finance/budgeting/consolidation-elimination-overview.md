---
title: 合并和清除概览
description: 本文提供有关合并和清除流程的一般信息。 它包含对一些常见问题的回答。
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9eb1440a67ae96f2a456bcee07515841f205bd2a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827402"
---
# <a name="consolidation-and-elimination-overview"></a><span data-ttu-id="3bd9b-104">合并和清除概览</span><span class="sxs-lookup"><span data-stu-id="3bd9b-104">Consolidation and elimination overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bd9b-105">本文提供有关合并和清除流程的一般信息。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-105">This article provides general information about the consolidation and elimination process.</span></span> <span data-ttu-id="3bd9b-106">它包含对一些常见问题的回答。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-106">It includes answers to some frequently asked questions.</span></span>

<span data-ttu-id="3bd9b-107">在您合并数据时，若干子公司的财务结果合并到一个合并公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-107">When you consolidate data, the financial results for multiple subsidiary companies are combined into results for a single, consolidated company.</span></span> <span data-ttu-id="3bd9b-108">子公司可以在不同的版本或系统中，它们可能不是完全所有，并且可能使用不同币种。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-108">Subsidiaries might be on different versions or systems, they might not be fully owned, and they might use different currencies.</span></span> <span data-ttu-id="3bd9b-109">合并数据具有多个选项：</span><span class="sxs-lookup"><span data-stu-id="3bd9b-109">There are multiple options for consolidating data:</span></span>

-   <span data-ttu-id="3bd9b-110">**联机合并** – 此选项按所选科目和维度合并每日余额，并且在合并公司中存储它们。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-110">**Consolidate online** – This option consolidates daily balances by the selected accounts and dimensions, and stores them in a consolidation company.</span></span>
-   <span data-ttu-id="3bd9b-111">**财务报表** – 此选项可以合并交易记录和余额，可以在任何时间生成。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-111">**Financial reporting** – This option enables consolidation of transactions and balances, and can be generated at any time.</span></span> <span data-ttu-id="3bd9b-112">可以创建层次结构的多个级别，并且可以查看多个申报币种。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-112">Multiple levels of hierarchies can be created, and multiple reporting currencies can be viewed.</span></span>
-   <span data-ttu-id="3bd9b-113">**与导入合并** – 此选项导入余额到合并公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-113">**Consolidate with import** – This option imports balances into a consolidation company.</span></span>
-   <span data-ttu-id="3bd9b-114">**导出公司余额** – 此选项提供公司余额的导出文件。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-114">**Export company balances** – This option provides an export file of company balances.</span></span> <span data-ttu-id="3bd9b-115">该文件然后可以导入到其他实例或系统。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-115">The file can then be imported into other instances or systems.</span></span> <span data-ttu-id="3bd9b-116">财务报表还可以用于将余额导出到 Microsoft Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-116">Financial reporting can also be used to export the balances to a Microsoft Excel file.</span></span>

<span data-ttu-id="3bd9b-117">清除可以通过多种方式报告：</span><span class="sxs-lookup"><span data-stu-id="3bd9b-117">Eliminations can be reported in multiple ways:</span></span>

-   <span data-ttu-id="3bd9b-118">清除规则可以在系统中进行设置，然后在合并流程中或通过清除方案处理。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-118">Elimination rules can be set up in the system, and then processed during the consolidation process or through an elimination proposal.</span></span> <span data-ttu-id="3bd9b-119">规则可过帐到在法人设置中选择了 **用于财务清除过程** 的所有公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-119">The rules can be posted to any company that has **Use for financial elimination process** selected in the legal entity setup.</span></span>
-   <span data-ttu-id="3bd9b-120">一个单独公司可以创建，并可用于手动确定和过帐清除交易记录。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-120">A separate company can be created and used to manually determine and post elimination transactions.</span></span> <span data-ttu-id="3bd9b-121">此公司可以在合并流程或在财务报表中使用。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-121">This company can be used in the consolidation process or in financial reporting.</span></span>
-   <span data-ttu-id="3bd9b-122">用于确定内部公司活动的科目和财务维度可以在财务报表的行定义或列定义中筛选，并可使用完整深化功能。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-122">The accounts and financial dimensions that are used to determine intercompany activity can be filtered on a row definition or column definition in Financial reporting, and full drill-down capabilities can be used.</span></span> <span data-ttu-id="3bd9b-123">计算的列或行然后可用于从合并的合计中删除科目和财务维度。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-123">A calculated column or row can then be used to remove the accounts and financial dimensions from the consolidated total.</span></span>

<span data-ttu-id="3bd9b-124">有很多合并方案，并且每个方法可以通过不同方式处理方案。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-124">There are many consolidation scenarios, and each method can handle the scenarios in different ways.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3bd9b-125">常见问题</span><span class="sxs-lookup"><span data-stu-id="3bd9b-125">Frequently asked questions</span></span>
1.  <span data-ttu-id="3bd9b-126">我想要在数据库中过帐清除。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-126">I prefer to post eliminations in a database.</span></span> <span data-ttu-id="3bd9b-127">我应该使用哪些选项？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-127">What are my options?</span></span>

<span data-ttu-id="3bd9b-128">您有多个选项。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-128">You have multiple options.</span></span> <span data-ttu-id="3bd9b-129">您可以使用 **联机合并** 选项，并且在流程中包括清除或将其作为方案。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-129">You can use the **Consolidate online** option, and include eliminations during the process or as a proposal.</span></span> <span data-ttu-id="3bd9b-130">交易记录将在合并公司中过帐。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-130">The transactions will be posted in the consolidation company.</span></span> <span data-ttu-id="3bd9b-131">或者，您可以有一个在其中手动创建清除的单独公司，然后在财务报表或在合并流程中使用该公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-131">Alternatively, you can have a separate company that you manually create the eliminations in, and then use that company in Financial reporting or in the consolidation process.</span></span>

2.  <span data-ttu-id="3bd9b-132">我们需要我们的合并结果以多种申报币种显示。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-132">We need our consolidated results in multiple reporting currencies.</span></span>

<span data-ttu-id="3bd9b-133">**财务报表** 选项有无限制的申报币种。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-133">The **Financial reporting** option has unlimited reporting currencies.</span></span> <span data-ttu-id="3bd9b-134">数据在报表生成期间，基于在主科目中设置的汇率类型和币种转换方法转换。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-134">The data is translated during report generation, based on the exchange rate type and currency translation method that are set on the main account.</span></span> <span data-ttu-id="3bd9b-135">但是，由于 **联机合并** 选项只有一个申报币种，如果您使用该选项，每一申报币种都需要一个合同公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-135">However, because the **Consolidate online** option has only one reporting currency, a consolidated company is required for each reporting currency if you use that option.</span></span> <span data-ttu-id="3bd9b-136">**财务报表** 选项是建议的方法。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-136">The **Financial reporting** option is the recommended method.</span></span>

3.  <span data-ttu-id="3bd9b-137">我想查看每个公司的交易记录级的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-137">I want to see transaction-level detail for each company.</span></span>

<span data-ttu-id="3bd9b-138">**财务报表** 选项是解决方法，因为可以查看报表结构树定义中包括的任意数量公司的交易记录级的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-138">The **Financial reporting** option is the solution, because transaction-level detail can be viewed for as many companies as are included in the reporting tree definition.</span></span>

4.  <span data-ttu-id="3bd9b-139">我们使用预算计划或预算控制，并且必须合并它。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-139">We are using budget planning or budget control, and it must be consolidated.</span></span>

<span data-ttu-id="3bd9b-140">**财务报表** 选项是合并所有预算计划或预算控制数据的解决方法。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-140">The **Financial reporting** option is the solution to consolidate any budget planning or budget control data.</span></span>

5.  <span data-ttu-id="3bd9b-141">我们的子公司遍布世界各地，我们有多个会计科目表。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-141">Our subsidiaries are spread throughout the world, and we have multiple charts of accounts.</span></span> <span data-ttu-id="3bd9b-142">什么是我们合并数据的最佳方法？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-142">What is the best method for consolidating our data?</span></span>

<span data-ttu-id="3bd9b-143">在您必须处理多个会计科目表时，您有多个选项。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-143">You have multiple options when you must handle multiple charts of accounts.</span></span> <span data-ttu-id="3bd9b-144">您可以使用 **联机合并** 选项，然后选择使用在主科目中定义的合并帐户或合并帐户组。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-144">You can use the **Consolidate online** option, and then choose to use either the consolidation  account that is defined on the main account or a consolidation account group.</span></span> <span data-ttu-id="3bd9b-145">您还可以使用 **财务报表** 选项，包括指向行定义中个财务维度的多个链接并映射科目。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-145">You can also use the **Financial reporting** option, include multiple links to the financial dimensions in the row definition, and map the accounts.</span></span>

6.  <span data-ttu-id="3bd9b-146">我们需要多个级别的合并。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-146">We require multiple levels of consolidation.</span></span> <span data-ttu-id="3bd9b-147">换言之，我们首先将我们所有的欧洲子公司合并到英镑 (GBP)。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-147">In other words, we first consolidate all our European subsidiaries to the British pound (GBP).</span></span> <span data-ttu-id="3bd9b-148">我们然后获取该数据并将合并金额转换为美元。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-148">We then take that data and translate the consolidated amount to US dollars.</span></span> <span data-ttu-id="3bd9b-149">我们如何完成此任务？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-149">How can we do this?</span></span>

<span data-ttu-id="3bd9b-150">在需要多个级别的合并，并且每个级别使用不同的币种时，必须使用 **联机合并** 选项。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-150">When multiple levels of consolidation are required, and different currencies are used at each level, you must use the **Consolidate online** option.</span></span> <span data-ttu-id="3bd9b-151">必须创建多个具有不同会计和申报币种的合并公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-151">Multiple consolidation companies must be created that differ in their accounting and reporting currencies.</span></span> <span data-ttu-id="3bd9b-152">然后必须多次运行合并。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-152">The consolidation must then be run multiple times.</span></span> <span data-ttu-id="3bd9b-153">**财务报表** 选项始终会将每个源公司的记帐币种转换为所选币种。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-153">The **Financial reporting** option always translates from each source company's accounting currency to the selected currency.</span></span>

7.  <span data-ttu-id="3bd9b-154">我们在不同系统中有子公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-154">We have subsidiaries on a different system.</span></span> <span data-ttu-id="3bd9b-155">我们如何合并它们？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-155">How can we consolidate them?</span></span>

<span data-ttu-id="3bd9b-156">使用 **与导入合并** 选项将余额导入到合并公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-156">Use the **Consolidate with import** option to bring the balances into a consolidation company.</span></span>

8.  <span data-ttu-id="3bd9b-157">我们的某些子公司不是完全所有。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-157">Some of our subsidiaries are not fully owned.</span></span> <span data-ttu-id="3bd9b-158">什么是我们合并它们的最佳方法？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-158">What is the best method for consolidating them?</span></span>

<span data-ttu-id="3bd9b-159">您有多个选项可用于部分所有的子公司。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-159">You have multiple options for partially owned subsidiaries.</span></span> <span data-ttu-id="3bd9b-160">通过使用 **财务报表** 选项，您可以定义报表结构树定义和所有权。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-160">By using the **Financial reporting** option, you can define a reporting tree definition and the ownership.</span></span> <span data-ttu-id="3bd9b-161">您还可以使用计算出的行或列表示部分所拥有的金额。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-161">You can also use a calculated row or column to represent the partially owned amount.</span></span> <span data-ttu-id="3bd9b-162">您甚至可以在报表中将少数股权显示为其自己的行。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-162">You can even show the minority interest as its own row on a report.</span></span> <span data-ttu-id="3bd9b-163">您还可以使用 **联机合并** 选项。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-163">You can also use the **Consolidate online** option.</span></span> <span data-ttu-id="3bd9b-164">**法人** 选项卡具有 **所有权** 列，在其中您可以定义母公司拥有的百分比。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-164">The **Legal entities** tab has an **Ownership** column, where you can define the percentage that is owned by the parent company.</span></span>

9.  <span data-ttu-id="3bd9b-165">我们的组织必须按业务单位显示合并或想要使用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-165">Our organization must show consolidations by business unit or wants to use the organization hierarchies.</span></span>

<span data-ttu-id="3bd9b-166">**财务报表** 选项是解决方法。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-166">The **Financial reporting** option is the solution.</span></span> <span data-ttu-id="3bd9b-167">具有法人或财务维度的组织层次结构可以在财务报表中报告。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-167">Organization hierarchies that have legal entities or financial dimensions in them can be reported on in Financial reporting.</span></span> <span data-ttu-id="3bd9b-168">您还可以通过使用有法人和维度值组合的报表结构树定义创建您自己的多级别层次结构。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-168">You can also create your own multilevel hierarchies by using a reporting tree definition that has a combination of legal entities and dimension values.</span></span>

10. <span data-ttu-id="3bd9b-169">我们具有多个系统实例。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-169">We have more than one instance of the system.</span></span>

<span data-ttu-id="3bd9b-170">通过使用 **导出公司余额** 选项从一个实例导出，然后使用其他实例的 **与导入合并** 选项，可以合并数据。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-170">By using the **Export company balances** option to export from one instance and then using the **Consolidate with import** option on the other instance, you can consolidate the data.</span></span>

11. <span data-ttu-id="3bd9b-171">我能否对状态为 **草稿** 的预算执行合并？</span><span class="sxs-lookup"><span data-stu-id="3bd9b-171">Can I do a Consolidation with my budget in **DRAFT** status?</span></span> 
            
<span data-ttu-id="3bd9b-172">您无法在合并公司中处理或完成预算。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-172">You won't be able to process or complete your budgets in the consolidation company.</span></span> <span data-ttu-id="3bd9b-173">我们建议使用 Financial Reporting 来合并草案预算。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-173">We recommended using Financial Reporting to consolidate draft budgets.</span></span>

<span data-ttu-id="3bd9b-174">有关详细信息，请参阅[合并公司中的币种重估](../general-ledger/currency-revaluation-consolidation-company.md)。</span><span class="sxs-lookup"><span data-stu-id="3bd9b-174">For more information, see [Currency revaluation in a consolidation company](../general-ledger/currency-revaluation-consolidation-company.md).</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]