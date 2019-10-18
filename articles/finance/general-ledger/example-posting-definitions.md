---
title: 过帐定义
description: 本文提供示例以显示如何将过帐定义用于采购订单保留款和预算拨款。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b78a40d3bac5794a66d0ea743f11a27cfacf4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186616"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="ed91e-103">过帐定义示例</span><span class="sxs-lookup"><span data-stu-id="ed91e-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed91e-104">本文提供示例以显示如何将过帐定义用于采购订单保留款和预算拨款。</span><span class="sxs-lookup"><span data-stu-id="ed91e-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="ed91e-105">在阅读此主题前，您应该熟悉过帐定义和交易记录过帐定义。</span><span class="sxs-lookup"><span data-stu-id="ed91e-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="ed91e-106">有关信息，请参阅[过帐定义](posting-definitions.md)。</span><span class="sxs-lookup"><span data-stu-id="ed91e-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="ed91e-107">以下示例可以在**过帐定义**页设置。</span><span class="sxs-lookup"><span data-stu-id="ed91e-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="ed91e-108">每个示例都包含以下部分：</span><span class="sxs-lookup"><span data-stu-id="ed91e-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="ed91e-109">过帐定义 – 匹配条件</span><span class="sxs-lookup"><span data-stu-id="ed91e-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="ed91e-110">过帐定义 – 生成的条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="ed91e-111">包含科目、维度值和金额的交易记录</span><span class="sxs-lookup"><span data-stu-id="ed91e-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="ed91e-112">从过帐定义生成的分类帐条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed91e-113">交易记录上的过帐定义和维度值在**匹配条件**窗格中的帐户和维度值之间发生匹配时，为过帐定义基于**生成的条目**窗格生成分类帐条目。</span><span class="sxs-lookup"><span data-stu-id="ed91e-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="ed91e-114">若要将过帐定义与特定的交易记录类型关联，请使用**交易记录过帐定义**页。</span><span class="sxs-lookup"><span data-stu-id="ed91e-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="ed91e-115">在您将过账定义与某一交易记录类型关联并在**总帐参数**页中选择**使用过帐定义**后，所选交易记录类型的所有交易记录都必须使用过账定义。</span><span class="sxs-lookup"><span data-stu-id="ed91e-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="ed91e-116">示例：采购订单保留款</span><span class="sxs-lookup"><span data-stu-id="ed91e-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="ed91e-117">在您通过在**总帐参数**页选择**启用保留款流程**后，过帐定义必须用于将保留款记录到应预留的所有帐户的总帐。</span><span class="sxs-lookup"><span data-stu-id="ed91e-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="ed91e-118">在大多数情况下，所有支出帐户都预留在资产负债表。</span><span class="sxs-lookup"><span data-stu-id="ed91e-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="ed91e-119">保留款的过帐定义为**过帐定义**页的**采购**模块设置。</span><span class="sxs-lookup"><span data-stu-id="ed91e-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ed91e-120">然后，在**交易记录过帐定义**页的**采购**区域，您可以选择**采购订单**交易记录类型以将过帐定义与采购订单关联。</span><span class="sxs-lookup"><span data-stu-id="ed91e-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="ed91e-121">在凭证上的每个唯一维度中，采购订单保留款的所有凭证交易记录都必须平衡（即借方必须与贷项相等）。</span><span class="sxs-lookup"><span data-stu-id="ed91e-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ed91e-122">过帐定义 – 匹配条件</span><span class="sxs-lookup"><span data-stu-id="ed91e-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ed91e-123">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-123">Account structure</span></span>       | <span data-ttu-id="ed91e-124">匹配帐号</span><span class="sxs-lookup"><span data-stu-id="ed91e-124">Match account number</span></span> | <span data-ttu-id="ed91e-125">优先级 </span><span class="sxs-lookup"><span data-stu-id="ed91e-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ed91e-126">科目结构 - P&L</span><span class="sxs-lookup"><span data-stu-id="ed91e-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ed91e-127">1</span><span class="sxs-lookup"><span data-stu-id="ed91e-127">1</span></span>        |

<span data-ttu-id="ed91e-128"><em>\**匹配帐号</em>* 字段中的空值意味着定义的科目结构中的所有匹配的科目都是匹配规则的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed91e-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ed91e-129">过帐定义 – 生成的条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ed91e-130">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-130">Account structure</span></span> | <span data-ttu-id="ed91e-131">生成的帐号</span><span class="sxs-lookup"><span data-stu-id="ed91e-131">Generated account number</span></span>                    | <span data-ttu-id="ed91e-132">生成的借方/贷方</span><span class="sxs-lookup"><span data-stu-id="ed91e-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="ed91e-133">余额</span><span class="sxs-lookup"><span data-stu-id="ed91e-133">Balance</span></span>           | <span data-ttu-id="ed91e-134">300143 - -（保留款帐户）</span><span class="sxs-lookup"><span data-stu-id="ed91e-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="ed91e-135">相同</span><span class="sxs-lookup"><span data-stu-id="ed91e-135">Same</span></span>                   |
| <span data-ttu-id="ed91e-136">余额</span><span class="sxs-lookup"><span data-stu-id="ed91e-136">Balance</span></span>           | <span data-ttu-id="ed91e-137">300144 - -（保留款帐户的预留）</span><span class="sxs-lookup"><span data-stu-id="ed91e-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="ed91e-138">平衡</span><span class="sxs-lookup"><span data-stu-id="ed91e-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ed91e-139">包含科目、维度值和金额的交易记录</span><span class="sxs-lookup"><span data-stu-id="ed91e-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ed91e-140">帐户和维度值来自您为采购订单行输入的会计分配，或者来自基于对供应商、物料、类别和维度模板的默认设置自动生成的帐户和维度。</span><span class="sxs-lookup"><span data-stu-id="ed91e-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="ed91e-141">帐户 + 维度</span><span class="sxs-lookup"><span data-stu-id="ed91e-141">Account + dimensions</span></span>           | <span data-ttu-id="ed91e-142">借记卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-142">Debit</span></span>  | <span data-ttu-id="ed91e-143">信用卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-143">Credit</span></span> | <span data-ttu-id="ed91e-144">注释</span><span class="sxs-lookup"><span data-stu-id="ed91e-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed91e-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed91e-146">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ed91e-147">从过帐定义生成的分类帐条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed91e-148">创建生成的分类帐条目记录保留款。</span><span class="sxs-lookup"><span data-stu-id="ed91e-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="ed91e-149">帐户 + 维度</span><span class="sxs-lookup"><span data-stu-id="ed91e-149">Account + dimensions</span></span>           | <span data-ttu-id="ed91e-150">借记卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-150">Debit</span></span>  | <span data-ttu-id="ed91e-151">信用卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-151">Credit</span></span> | <span data-ttu-id="ed91e-152">注释</span><span class="sxs-lookup"><span data-stu-id="ed91e-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed91e-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed91e-154">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-154">250.00</span></span> |        |         |
| <span data-ttu-id="ed91e-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ed91e-156">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-156">250.00</span></span> |         |

<span data-ttu-id="ed91e-157">在此示例中，所有科目都是科目结构的一部分 - P&L 与过账定义条件匹配。</span><span class="sxs-lookup"><span data-stu-id="ed91e-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ed91e-158">因此，在对 606500-OU\_1-OU\_3566-Training 进行评估时，在过帐定义的**生成的条目**窗格中定义的科目创建生成的条目。</span><span class="sxs-lookup"><span data-stu-id="ed91e-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="ed91e-159">示例：预算拨款</span><span class="sxs-lookup"><span data-stu-id="ed91e-159">Example: Budget appropriations</span></span>
<span data-ttu-id="ed91e-160">在您通过在**总帐参数**页中选择**启用预算拨款**时，过帐定义必须用于记录总帐的预算登记条目。</span><span class="sxs-lookup"><span data-stu-id="ed91e-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="ed91e-161">在预算控制配置有效并打开时，过帐定义和交易记录过帐定义可用于支持将拨款、版本、转移、项目、固定资产及供应和需求预测条目记录到总帐。</span><span class="sxs-lookup"><span data-stu-id="ed91e-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="ed91e-162">若要为具有**原始预算**预算类型且已启用拨款的预算登记条目设置过帐定义，在**过帐定义**页选择**预算**模块。</span><span class="sxs-lookup"><span data-stu-id="ed91e-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ed91e-163">然后，在**交易记录过帐定义**页的**预算**区域，您可以使用预算代码将过帐定义与具有**原始预算**预算类型的预算登记条目关联。</span><span class="sxs-lookup"><span data-stu-id="ed91e-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="ed91e-164">在启用预算拨款和过帐定义时，为预算控件记录登记条目并将其记录在总帐中。</span><span class="sxs-lookup"><span data-stu-id="ed91e-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ed91e-165">过帐定义 – 匹配条件</span><span class="sxs-lookup"><span data-stu-id="ed91e-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ed91e-166">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-166">Account structure</span></span>       | <span data-ttu-id="ed91e-167">匹配帐号</span><span class="sxs-lookup"><span data-stu-id="ed91e-167">Match account number</span></span> | <span data-ttu-id="ed91e-168">优先级 </span><span class="sxs-lookup"><span data-stu-id="ed91e-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ed91e-169">科目结构 - P&L</span><span class="sxs-lookup"><span data-stu-id="ed91e-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ed91e-170">1</span><span class="sxs-lookup"><span data-stu-id="ed91e-170">1</span></span>        |

<span data-ttu-id="ed91e-171"><em>\**匹配帐号</em>* 字段中的空值意味着定义的科目结构中的所有匹配的科目都是匹配规则的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed91e-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ed91e-172">过帐定义 – 生成的条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ed91e-173">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-173">Account structure</span></span> | <span data-ttu-id="ed91e-174">生成的帐号</span><span class="sxs-lookup"><span data-stu-id="ed91e-174">Generated account number</span></span>              | <span data-ttu-id="ed91e-175">生成的借方/贷方</span><span class="sxs-lookup"><span data-stu-id="ed91e-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="ed91e-176">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-176">Account structure</span></span> | <span data-ttu-id="ed91e-177">300145 - -（估计的收入帐户）</span><span class="sxs-lookup"><span data-stu-id="ed91e-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="ed91e-178">相同</span><span class="sxs-lookup"><span data-stu-id="ed91e-178">Same</span></span>                   |
| <span data-ttu-id="ed91e-179">科目结构</span><span class="sxs-lookup"><span data-stu-id="ed91e-179">Account structure</span></span> | <span data-ttu-id="ed91e-180">300146 - -（拨款帐户）</span><span class="sxs-lookup"><span data-stu-id="ed91e-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="ed91e-181">平衡</span><span class="sxs-lookup"><span data-stu-id="ed91e-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ed91e-182">包含科目、维度值和金额的交易记录</span><span class="sxs-lookup"><span data-stu-id="ed91e-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ed91e-183">您在**预算登记分录**页中输入该帐户、维度值和的预算科目分录金额。</span><span class="sxs-lookup"><span data-stu-id="ed91e-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="ed91e-184">帐户 + 维度</span><span class="sxs-lookup"><span data-stu-id="ed91e-184">Account + dimensions</span></span>           | <span data-ttu-id="ed91e-185">借记卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-185">Debit</span></span> | <span data-ttu-id="ed91e-186">信用卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-186">Credit</span></span> | <span data-ttu-id="ed91e-187">注释</span><span class="sxs-lookup"><span data-stu-id="ed91e-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="ed91e-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="ed91e-189">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ed91e-190">从过帐定义生成的分类帐条目</span><span class="sxs-lookup"><span data-stu-id="ed91e-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed91e-191">创建生成的分类帐条目将原始预算记录进每个维度。</span><span class="sxs-lookup"><span data-stu-id="ed91e-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="ed91e-192">帐户 + 维度</span><span class="sxs-lookup"><span data-stu-id="ed91e-192">Account + dimensions</span></span>           | <span data-ttu-id="ed91e-193">借记卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-193">Debit</span></span>  | <span data-ttu-id="ed91e-194">信用卡</span><span class="sxs-lookup"><span data-stu-id="ed91e-194">Credit</span></span> | <span data-ttu-id="ed91e-195">注释</span><span class="sxs-lookup"><span data-stu-id="ed91e-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed91e-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ed91e-197">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-197">250.00</span></span> |         |
| <span data-ttu-id="ed91e-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="ed91e-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed91e-199">250.00</span><span class="sxs-lookup"><span data-stu-id="ed91e-199">250.00</span></span> |        |         |

<span data-ttu-id="ed91e-200">在此示例中，所有科目都是科目结构的一部分 - P&L 与过账定义条件匹配。</span><span class="sxs-lookup"><span data-stu-id="ed91e-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ed91e-201">因此，在对 606400-OU\_1-OU\_3566-Training 进行评估时，创建生成的分类帐条目。</span><span class="sxs-lookup"><span data-stu-id="ed91e-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





