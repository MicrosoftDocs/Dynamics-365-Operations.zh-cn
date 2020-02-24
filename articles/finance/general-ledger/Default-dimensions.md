---
title: 财务维度和过帐
description: 在计划和设置会计科目表时，必须考虑过帐单据或日记帐时，各组件如何协同工作。 这些组件包括科目结构、高级规则和平衡与固定维度。 本主题介绍各组件的定义及其协同工作方式。
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0e2b98bde04b221730413bcd7ddd028074b19d47
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030937"
---
# <a name="financial-dimensions-and-posting"></a><span data-ttu-id="70d31-105">财务维度和过帐</span><span class="sxs-lookup"><span data-stu-id="70d31-105">Financial dimensions and posting</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70d31-106">在计划和设置会计科目表时，必须考虑过帐单据或日记帐时，各组件如何协同工作。</span><span class="sxs-lookup"><span data-stu-id="70d31-106">When you plan and set up your chart of accounts, you must consider how the various components will work together when you post a document or journal.</span></span> <span data-ttu-id="70d31-107">这些组件包括科目结构、高级规则和平衡与固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-107">These components include account structures, advanced rules, and balancing and fixed dimensions.</span></span> <span data-ttu-id="70d31-108">本主题介绍各组件的定义及其协同工作方式。</span><span class="sxs-lookup"><span data-stu-id="70d31-108">This topic explains what each component is and how the components work together.</span></span>

## <a name="chart-of-accounts-and-financial-dimension-components"></a><span data-ttu-id="70d31-109">会计科目表和财务维度组件</span><span class="sxs-lookup"><span data-stu-id="70d31-109">Chart of accounts and financial dimension components</span></span>

<span data-ttu-id="70d31-110">基于规则的丰富系统用于定义主科目和财务维度值的有效组合。</span><span class="sxs-lookup"><span data-stu-id="70d31-110">A rich, rule-based system is used to define valid combinations of main accounts and financial dimension values.</span></span> <span data-ttu-id="70d31-111">此部分简介各组件的功能及其位置。</span><span class="sxs-lookup"><span data-stu-id="70d31-111">This section gives a brief overview of the functionality of each component and explains where you can find the component.</span></span>

### <a name="account-structures"></a><span data-ttu-id="70d31-112">科目结构</span><span class="sxs-lookup"><span data-stu-id="70d31-112">Account structures</span></span>

<span data-ttu-id="70d31-113">设置分类帐时，需要科目结构。</span><span class="sxs-lookup"><span data-stu-id="70d31-113">An account structure is required when you set up your ledger.</span></span> <span data-ttu-id="70d31-114">必须至少定义和启用一个科目结构，并且必须将其分配给分类帐。</span><span class="sxs-lookup"><span data-stu-id="70d31-114">You must define and activate at least one account structure, and you must assign it to the ledger.</span></span> <span data-ttu-id="70d31-115">科目结构中必须包含主科目。</span><span class="sxs-lookup"><span data-stu-id="70d31-115">The account structure must have the main account in it.</span></span> <span data-ttu-id="70d31-116">可以定义最适合业务的细分市场顺序。</span><span class="sxs-lookup"><span data-stu-id="70d31-116">You can define the order of segments that works best for the business.</span></span> <span data-ttu-id="70d31-117">定义主科目后，系统可以确定所用科目结构。</span><span class="sxs-lookup"><span data-stu-id="70d31-117">After the main account is defined, the system can determine the account structure that is used.</span></span> <span data-ttu-id="70d31-118">通过将主科目放在结构的首位或靠前位置，可以帮助限制值，还可以帮助系统将已知的最后一个有效值作为默认值应用。</span><span class="sxs-lookup"><span data-stu-id="70d31-118">By putting the main account first or near the front of a structure, you can help limit the values and also help the system apply the last known valid value as a default value.</span></span> <span data-ttu-id="70d31-119">科目结构中还可以有最多 10 个财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-119">You can have up to 10 additional financial dimensions in the account structure.</span></span> <span data-ttu-id="70d31-120">科目结构定义哪些维度值在与其他值的组合中有效。</span><span class="sxs-lookup"><span data-stu-id="70d31-120">The account structure defines which dimension values are valid in combination with other values.</span></span> <span data-ttu-id="70d31-121">还定义是否必须输入维度值。</span><span class="sxs-lookup"><span data-stu-id="70d31-121">it also defines whether dimension values must be entered.</span></span>

### <a name="advanced-rules"></a><span data-ttu-id="70d31-122">高级规则</span><span class="sxs-lookup"><span data-stu-id="70d31-122">Advanced rules</span></span>

<span data-ttu-id="70d31-123">设置会计科目表时，高级规则是可选组件。</span><span class="sxs-lookup"><span data-stu-id="70d31-123">Advanced rules are an optional component when you set up the chart of accounts.</span></span> <span data-ttu-id="70d31-124">可以根据需要向科目结构添加任意数量的高级规则。</span><span class="sxs-lookup"><span data-stu-id="70d31-124">You can add as many advanced rules as you want to an account structure.</span></span> <span data-ttu-id="70d31-125">高级规则通常用于处理满足特定条件时必须跟踪更多财务维度的场景。</span><span class="sxs-lookup"><span data-stu-id="70d31-125">Advanced rules are often used to handle scenarios where additional financial dimensions must be tracked when specific criteria are met.</span></span> <span data-ttu-id="70d31-126">例如，如果使用路费科目，可能需要跟踪更多信息，如员工出差参加的活动。</span><span class="sxs-lookup"><span data-stu-id="70d31-126">For example, if you use a Travel expense account, you might want to track additional information, such as the event that the employee is traveling for.</span></span> <span data-ttu-id="70d31-127">如果有多个高级规则，则基于其名称按字母顺序应用。</span><span class="sxs-lookup"><span data-stu-id="70d31-127">If there are multiple advanced rules, they are applied in alphabetical order, based on the names of the rules.</span></span> <span data-ttu-id="70d31-128">只能将规则添加的细分市场应用到科目结构的细分市场后。</span><span class="sxs-lookup"><span data-stu-id="70d31-128">The segments that a rule adds can be applied only after the segments of the account structure.</span></span>

### <a name="balancing-dimension"></a><span data-ttu-id="70d31-129">平衡维度</span><span class="sxs-lookup"><span data-stu-id="70d31-129">Balancing dimension</span></span>

<span data-ttu-id="70d31-130">可以选择定义平衡财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-130">You can optionally define a balancing financial dimension.</span></span> <span data-ttu-id="70d31-131">在**分类帐**页中，可以定义应平衡的财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-131">On the **Ledger** page, you can define the financial dimension that should be balanced.</span></span> <span data-ttu-id="70d31-132">然后，只要将交易过帐到该财务维度，系统都将自动创建条目并过帐，以便平衡该财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-132">Then, whenever transactions are posted to that financial dimension, the system automatically creates and posts entries to make the financial dimension balanced.</span></span>

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a><span data-ttu-id="70d31-133">主科目中的默认/固定财务维度</span><span class="sxs-lookup"><span data-stu-id="70d31-133">Default/fixed financial dimensions on the main account</span></span>

<span data-ttu-id="70d31-134">默认维度来自各种位置，如主记录（如客户或供应商记录）、单据抬头和主科目。</span><span class="sxs-lookup"><span data-stu-id="70d31-134">Default dimensions come from various places, such as master records (for example, customer or vendor records), document headers, and the main account.</span></span> <span data-ttu-id="70d31-135">本主题重点介绍主科目中按法人分类的默认维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-135">This topic focuses on default dimensions on the main account by legal entity.</span></span> <span data-ttu-id="70d31-136">可以为分类帐的所有科目结构中使用的各财务维度定义主科目具有**非固定**还是**固定**值。</span><span class="sxs-lookup"><span data-stu-id="70d31-136">You can define whether a main account has a **Not fixed** or **Fixed** value for each financial dimension that is used across all account structures for the ledger.</span></span> <span data-ttu-id="70d31-137">如果财务维度**非固定**，则使用默认值，但不能改写该值。</span><span class="sxs-lookup"><span data-stu-id="70d31-137">If a financial dimension is **Not fixed**, it uses a default value, but that value can be overwritten.</span></span> <span data-ttu-id="70d31-138">此行为适用于系统中的所有默认值，即使来自主记录的默认值也不例外。</span><span class="sxs-lookup"><span data-stu-id="70d31-138">This behavior applies to all default values in the system, even default values that come from master records.</span></span> <span data-ttu-id="70d31-139">如果财务维度设置为**固定**值，无论该值与默认值来自同一位置还是用户输入的。都将始终应用该值。</span><span class="sxs-lookup"><span data-stu-id="70d31-139">If a financial dimension is set to a **Fixed** value, that value is always applied, regardless of whether it came from somewhere as a default value or the user entered it.</span></span>

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a><span data-ttu-id="70d31-140">过帐期间默认维度的应用顺序</span><span class="sxs-lookup"><span data-stu-id="70d31-140">Order in which default dimensions are applied during posting</span></span>

<span data-ttu-id="70d31-141">大家经常好奇各种组件的运行顺序。</span><span class="sxs-lookup"><span data-stu-id="70d31-141">People often have questions about the order that the various components run in.</span></span> <span data-ttu-id="70d31-142">请务必了解默认维度的应用顺序，因为此行为影响你设置时采用的方法。</span><span class="sxs-lookup"><span data-stu-id="70d31-142">It's very important that you understand the order that default dimensions are applied in, because this behavior affects the approach that you take to setup.</span></span>

> [!NOTE]
> <span data-ttu-id="70d31-143">此信息仅适用于应用程序中默认维度的应用。</span><span class="sxs-lookup"><span data-stu-id="70d31-143">This information applies only to the application of default dimensions in the application.</span></span> <span data-ttu-id="70d31-144">如果通过使用 Microsoft Excel 或数据管理 Framework 导入数据，则行为不同。</span><span class="sxs-lookup"><span data-stu-id="70d31-144">If you import data by using Microsoft Excel or the Data Management Framework, the behavior differs.</span></span>

### <a name="example-1"></a><span data-ttu-id="70d31-145">示例 1</span><span class="sxs-lookup"><span data-stu-id="70d31-145">Example 1</span></span>

<span data-ttu-id="70d31-146">**科目结构**</span><span class="sxs-lookup"><span data-stu-id="70d31-146">**Account structure**</span></span>

| <span data-ttu-id="70d31-147">主科目</span><span class="sxs-lookup"><span data-stu-id="70d31-147">Main account</span></span>            | <span data-ttu-id="70d31-148">业务单位</span><span class="sxs-lookup"><span data-stu-id="70d31-148">Business unit</span></span>           | <span data-ttu-id="70d31-149">部门</span><span class="sxs-lookup"><span data-stu-id="70d31-149">Department</span></span>              | <span data-ttu-id="70d31-150">成本中心</span><span class="sxs-lookup"><span data-stu-id="70d31-150">Cost center</span></span>             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| <span data-ttu-id="70d31-151">允许所有值。</span><span class="sxs-lookup"><span data-stu-id="70d31-151">All values are allowed.</span></span> | <span data-ttu-id="70d31-152">允许所有值。</span><span class="sxs-lookup"><span data-stu-id="70d31-152">All values are allowed.</span></span> | <span data-ttu-id="70d31-153">允许所有值。</span><span class="sxs-lookup"><span data-stu-id="70d31-153">All values are allowed.</span></span> | <span data-ttu-id="70d31-154">允许所有值。</span><span class="sxs-lookup"><span data-stu-id="70d31-154">All values are allowed.</span></span> |

<span data-ttu-id="70d31-155">**主科目**</span><span class="sxs-lookup"><span data-stu-id="70d31-155">**Main account**</span></span>

| <span data-ttu-id="70d31-156">主科目</span><span class="sxs-lookup"><span data-stu-id="70d31-156">Main account</span></span> | <span data-ttu-id="70d31-157">姓名</span><span class="sxs-lookup"><span data-stu-id="70d31-157">Name</span></span>          | <span data-ttu-id="70d31-158">法人</span><span class="sxs-lookup"><span data-stu-id="70d31-158">Legal entity</span></span> | <span data-ttu-id="70d31-159">部门</span><span class="sxs-lookup"><span data-stu-id="70d31-159">Department</span></span>                                 |
|--------------|---------------|--------------|--------------------------------------------|
| <span data-ttu-id="70d31-160">401100</span><span class="sxs-lookup"><span data-stu-id="70d31-160">401100</span></span>       | <span data-ttu-id="70d31-161">产品销售</span><span class="sxs-lookup"><span data-stu-id="70d31-161">Product Sales</span></span> | <span data-ttu-id="70d31-162">USMF</span><span class="sxs-lookup"><span data-stu-id="70d31-162">USMF</span></span>         | <span data-ttu-id="70d31-163">固定 - 022 销售和市场营销部门</span><span class="sxs-lookup"><span data-stu-id="70d31-163">Fixed – 022 Sales and Marketing department</span></span> |

<span data-ttu-id="70d31-164">下图显示主科目 401100 中设置的默认固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-164">The following illustration shows the fixed default dimension that is set on main account 401100.</span></span>

<span data-ttu-id="70d31-165">[![默认财务维度](./media/default-dimensions.png)](./media/default-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-165">[![Default financial dimensions](./media/default-dimensions.png)](./media/default-dimensions.png)</span></span>

<span data-ttu-id="70d31-166">在这个非常基础的示例中，将输入一个普通日记帐，其中的部门维度设置为使用默认值 **023**（操作）。</span><span class="sxs-lookup"><span data-stu-id="70d31-166">For this very basic example, we will enter a general journal where the Department dimension is set to use the default value **023** (Operations).</span></span> <span data-ttu-id="70d31-167">将输入一个会计科目并过帐。</span><span class="sxs-lookup"><span data-stu-id="70d31-167">We will enter and post a ledger account.</span></span> <span data-ttu-id="70d31-168">下图显示总帐标题中的默认财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-168">The following illustration shows the default financial dimension on the general ledger header.</span></span>

<span data-ttu-id="70d31-169">[![普通日记帐](./media/general-journal.png)](./media/general-journal.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-169">[![General journals](./media/general-journal.png)](./media/general-journal.png)</span></span>

<span data-ttu-id="70d31-170">该日记帐标题中的默认维度将导致在销售科目行中默认应用部门 023。</span><span class="sxs-lookup"><span data-stu-id="70d31-170">The default dimension on the journal header will cause department 023 to be applied by default on the sales account line.</span></span> <span data-ttu-id="70d31-171">下图显示普通日记帐行，其中应用了来自标题的默认维度值 **023**。</span><span class="sxs-lookup"><span data-stu-id="70d31-171">The following illustration shows the general journal line, where the **023** default dimension value from the header is applied.</span></span>

<span data-ttu-id="70d31-172">[![日志凭证](./media/journal-voucher.png)](./media/journal-voucher.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-172">[![Journal voucher](./media/journal-voucher.png)](./media/journal-voucher.png)</span></span>

<span data-ttu-id="70d31-173">但是，过帐该行时，将应用固定维度，并将该行过帐到部门 022。</span><span class="sxs-lookup"><span data-stu-id="70d31-173">However, when the line is posted, the fixed dimension is applied, and the line is posted to department 022.</span></span> <span data-ttu-id="70d31-174">下图显示过帐的凭证，其中为销售科目应用了固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-174">The following illustration shows the posted voucher, where the fixed dimension is applied for the sales account.</span></span>

<span data-ttu-id="70d31-175">[![凭证交易记录](./media/voucher-transactions.png)](./media/voucher-transactions.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-175">[![Voucher transactions](./media/voucher-transactions.png)](./media/voucher-transactions.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="70d31-176">示例 2</span><span class="sxs-lookup"><span data-stu-id="70d31-176">Example 2</span></span>

<span data-ttu-id="70d31-177">此示例使用与第一个示例相同的设置。</span><span class="sxs-lookup"><span data-stu-id="70d31-177">This example uses the same setup as the first example.</span></span> <span data-ttu-id="70d31-178">但是，将再添加一个组件，并将部门维度用作平衡维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-178">However, we will add a second component and use the Department dimension as a balancing dimension.</span></span> <span data-ttu-id="70d31-179">在下图中，**部门**设置为 USMF 分类帐的平衡财务维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-179">In the following illustration, **Department** is set as the balancing financial dimension for the USMF ledger.</span></span>

<span data-ttu-id="70d31-180">[![分类帐](./media/ledger.png)](./media/ledger.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-180">[![Ledger](./media/ledger.png)](./media/ledger.png)</span></span>

<span data-ttu-id="70d31-181">使用相同的日记帐标题设置并过帐同一个交易时，将首先应用固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-181">When the same journal header setup is used, and the same transaction is posted, the fixed dimension is applied first.</span></span> <span data-ttu-id="70d31-182">然后应用平衡逻辑以帮助确保每个部门都有一个平衡的条目。</span><span class="sxs-lookup"><span data-stu-id="70d31-182">Then the balancing logic is applied to help guarantee that every department has a balanced entry.</span></span> <span data-ttu-id="70d31-183">下图显示应用固定维度后包含平衡条目的凭证交易。</span><span class="sxs-lookup"><span data-stu-id="70d31-183">The following illustration shows voucher transactions that include the balancing entry after the fixed dimension is applied.</span></span>

<span data-ttu-id="70d31-184">[![凭证交易记录](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-184">[![Voucher transactions](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)</span></span>

### <a name="example-3"></a><span data-ttu-id="70d31-185">示例 3</span><span class="sxs-lookup"><span data-stu-id="70d31-185">Example 3</span></span>

<span data-ttu-id="70d31-186">在此示例中，我们将添加一条高级规则。</span><span class="sxs-lookup"><span data-stu-id="70d31-186">In this example, we will add an advanced rule.</span></span> <span data-ttu-id="70d31-187">这条高级规则指定，如果使用销售科目 401100 和部门 022（销售和市场营销），系统应再跟踪一个名称为“客户”的细分市场。</span><span class="sxs-lookup"><span data-stu-id="70d31-187">The advanced rule specifies that if sales account 401100 and department 022 (Sales and Marketing) are used, the system should track an additional segment that is named Customer.</span></span>

<span data-ttu-id="70d31-188">因为顺序，此示例非常重要。</span><span class="sxs-lookup"><span data-stu-id="70d31-188">This example is important because of the order.</span></span> <span data-ttu-id="70d31-189">科目结构在输入主科目后确定。</span><span class="sxs-lookup"><span data-stu-id="70d31-189">The account structure is determined after the main account is entered.</span></span> <span data-ttu-id="70d31-190">如果希望设置科目结构，系统可以确定主科目、业务单位、部门和成本中心相关。</span><span class="sxs-lookup"><span data-stu-id="70d31-190">If you refer to the account structure setup, the system can determine that the main account, business unit, department, and cost center are relevant.</span></span> <span data-ttu-id="70d31-191">此时尚未触发高级规则，因为过帐期间为日记帐凭证应用默认维度之前，不应用固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-191">At this point, the advanced rule hasn't been triggered, because fixed dimensions aren't applied until default dimensions have been applied for the journal voucher during posting.</span></span> <span data-ttu-id="70d31-192">在下图中，无“客户”细分市场，因为尚未满足高级规则的条件。</span><span class="sxs-lookup"><span data-stu-id="70d31-192">In the following illustration, the Customer segment isn't present, because the criteria for the advanced rule haven't been met.</span></span>

<span data-ttu-id="70d31-193">[![会计科目](./media/drop-down.png)](./media/drop-down.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-193">[![Ledger account](./media/drop-down.png)](./media/drop-down.png)</span></span>

<span data-ttu-id="70d31-194">过帐将失败，因为流程结束时应用了固定维度。</span><span class="sxs-lookup"><span data-stu-id="70d31-194">The posting won't be successful, because the fixed dimension was applied at the end of the process.</span></span> <span data-ttu-id="70d31-195">维度验证确定如果主科目为 401100 且部门为 022，则需要“科目”细分市场。</span><span class="sxs-lookup"><span data-stu-id="70d31-195">Dimension validation determines that the Customer segment is required if the main account is 401100 and the department is 022.</span></span> <span data-ttu-id="70d31-196">验证错误导致不能执行过帐。</span><span class="sxs-lookup"><span data-stu-id="70d31-196">Posting can't occur because of the validation error.</span></span> <span data-ttu-id="70d31-197">下图显示维度验证确定“客户”为必需的细分市场后显示的消息。</span><span class="sxs-lookup"><span data-stu-id="70d31-197">The following illustration shows the message that appears after dimension validation determines that Customer is a required segment.</span></span>

<span data-ttu-id="70d31-198">[![消息详细信息](./media/message.png)](./media/message.png)</span><span class="sxs-lookup"><span data-stu-id="70d31-198">[![Message details](./media/message.png)](./media/message.png)</span></span>

<span data-ttu-id="70d31-199">在此示例中，必须覆盖默认值，这样才会触发高级规则，并且可以输入“客户”细分市场。</span><span class="sxs-lookup"><span data-stu-id="70d31-199">In this example, you must overwrite the default value so that the advanced rule is triggered and you can enter the Customer segment.</span></span> <span data-ttu-id="70d31-200">但是，此解决方案并非始终可行，一些用户甚至不会注意到过帐规则。</span><span class="sxs-lookup"><span data-stu-id="70d31-200">However, this solution isn't always possible, and some users aren't even aware of the posting rules.</span></span> <span data-ttu-id="70d31-201">因此，设置会计科目表时务必了解默认维度的应用顺序。</span><span class="sxs-lookup"><span data-stu-id="70d31-201">Therefore, it's important that you understand the order that default dimensions are applied in when you set up your chart of accounts.</span></span>

<span data-ttu-id="70d31-202">若要实现此示例中的目标，可通过多种方法更改配置。</span><span class="sxs-lookup"><span data-stu-id="70d31-202">To achieve what you want in this example, you can change the configuration in several ways.</span></span> <span data-ttu-id="70d31-203">例如，可为销售科目创建新的科目结构，并在该结构中加入“科目”细分市场。</span><span class="sxs-lookup"><span data-stu-id="70d31-203">For example, you can create a new account structure for sales accounts and include the Customer segment in the structure.</span></span> <span data-ttu-id="70d31-204">还可以在现有科目结构中添加更多行，并指定主科目和有效的部门值。</span><span class="sxs-lookup"><span data-stu-id="70d31-204">You can also add more rows in an existing account structure, and specify the main account and valid department values.</span></span> <span data-ttu-id="70d31-205">然后，在额外的客户结构中，可以发现包含“客户”细分市场的单独销售科目科目结构非常有用。</span><span class="sxs-lookup"><span data-stu-id="70d31-205">Then, in the additional customer structure, you might find it useful to have a separate account structure of sales accounts where the Customer segment is present.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70d31-206">其他资源</span><span class="sxs-lookup"><span data-stu-id="70d31-206">Additional resources</span></span> 

<span data-ttu-id="70d31-207">下面的部分资源涉及我们的软件的早期版本。</span><span class="sxs-lookup"><span data-stu-id="70d31-207">Some of the following resources refer to an earlier version of our software.</span></span> <span data-ttu-id="70d31-208">但是，许多有关默认维度的应用的信息和许多概念在早期版本中是一样的，这些参考材料仍然有效。</span><span class="sxs-lookup"><span data-stu-id="70d31-208">However, much of the information about the application of default dimensions and many of the concepts are the same in the earlier version, and the references are still valid.</span></span>

[<span data-ttu-id="70d31-209">单位间核算的平衡日记帐</span><span class="sxs-lookup"><span data-stu-id="70d31-209">Balanced journals for interunit accounting</span></span>](example-balanced-journals-interunit-accounting.md)

[<span data-ttu-id="70d31-210">计划您的会计科目表</span><span class="sxs-lookup"><span data-stu-id="70d31-210">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md) 

<span data-ttu-id="70d31-211">[“在 AX 2012 中计划会计科目表”博客](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) - 此链接是由七个部分组成的系列中的第一部分。</span><span class="sxs-lookup"><span data-stu-id="70d31-211">[Planning your chart of accounts in AX 2012 blog](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – This link goes to part 1 of a seven-part series.</span></span>

[<span data-ttu-id="70d31-212">会计分配中的维度默认设置</span><span class="sxs-lookup"><span data-stu-id="70d31-212">Dimension defaulting in accounting distributions</span></span>](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[<span data-ttu-id="70d31-213">维度框架中的维度默认设置</span><span class="sxs-lookup"><span data-stu-id="70d31-213">Dimension defaulting in Dimensions framework</span></span>](https://docs.microsoft.com/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)
