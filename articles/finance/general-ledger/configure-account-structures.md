---
title: 配置科目结构
description: 此主题提供有关科目结构和财务维度的信息。
author: aprilolson
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7565dac61546ba87f5bf4605d3c6beceef7ac980
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821881"
---
# <a name="configure-account-structures"></a><span data-ttu-id="99441-103">配置科目结构</span><span class="sxs-lookup"><span data-stu-id="99441-103">Configure account structures</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="99441-104">科目结构使用主科目和财务维度创建一组规则，用于在输入科目编号时确定所用顺序和值。</span><span class="sxs-lookup"><span data-stu-id="99441-104">Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</span></span> <span data-ttu-id="99441-105">可根据企业的需要设置任意数量的科目结构。</span><span class="sxs-lookup"><span data-stu-id="99441-105">You can set up as many account structures as you need for your business.</span></span> <span data-ttu-id="99441-106">将把科目结构分配给公司的日记帐设置，以便共享。</span><span class="sxs-lookup"><span data-stu-id="99441-106">The account structures are assigned to a company’s ledger setup, so they can be shared.</span></span>

<span data-ttu-id="99441-107">创建科目结构时，最大科目段数为 11。</span><span class="sxs-lookup"><span data-stu-id="99441-107">When creating an account structure, the maximum number of segments is 11.</span></span> <span data-ttu-id="99441-108">如果需要的科目段超过此数量，请彻底评估您的设置和需求，因为这会影响用户体验。</span><span class="sxs-lookup"><span data-stu-id="99441-108">If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</span></span> <span data-ttu-id="99441-109">考虑科目段在申报方案中是否使用层次结构派生，而不是在数据录入期间或通过使用用户定义的字段派生。</span><span class="sxs-lookup"><span data-stu-id="99441-109">Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</span></span> <span data-ttu-id="99441-110">例如，如果要按位置申报，但是您可以通过部门或成本中心识别位置，则不需要将位置设置为财务维度。</span><span class="sxs-lookup"><span data-stu-id="99441-110">For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</span></span> <span data-ttu-id="99441-111">如果在评估后的确认定需要的科目段数超过 11 个，则可使用高级规则添加更多科目段。</span><span class="sxs-lookup"><span data-stu-id="99441-111">If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</span></span>

<span data-ttu-id="99441-112">科目结构需要主科目。</span><span class="sxs-lookup"><span data-stu-id="99441-112">Account structures require the main account.</span></span> <span data-ttu-id="99441-113">主科目不需要是结构中的第一个科目段，但的确可用于在录入科目编号时确定使用的是哪个科目结构。</span><span class="sxs-lookup"><span data-stu-id="99441-113">The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</span></span> <span data-ttu-id="99441-114">因此，只有分配给日记帐的一个结构中可以有主科目值，以免重合。</span><span class="sxs-lookup"><span data-stu-id="99441-114">Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</span></span> <span data-ttu-id="99441-115">识别了科目结构之后，将筛选允许值列表以引导用户仅选择有效的维度值，从而日记帐录入错误的可能性。</span><span class="sxs-lookup"><span data-stu-id="99441-115">After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</span></span>

> [!NOTE] 
> <span data-ttu-id="99441-116">如果计划针对财务维度编制预算，则该财务维度需要是科目结构的一部分。</span><span class="sxs-lookup"><span data-stu-id="99441-116">If you plan to budget against a financial dimension, it will need to be part of an account structure.</span></span> <span data-ttu-id="99441-117">编制预算现在不使用高级规则。</span><span class="sxs-lookup"><span data-stu-id="99441-117">Budgeting does not currently utilize advanced rules.</span></span>

## <a name="example"></a><span data-ttu-id="99441-118">示例</span><span class="sxs-lookup"><span data-stu-id="99441-118">Example</span></span>
<span data-ttu-id="99441-119">为了说明有关设置科目结构的最佳实践，假设一家公司希望在科目和业务单位财务维度级别跟踪自己的资产负债表科目 (100000..399999)。</span><span class="sxs-lookup"><span data-stu-id="99441-119">To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</span></span> <span data-ttu-id="99441-120">对于收入科目和支出科目 (400000..999999)，该公司跟踪财务维度“业务单位”、“部门”和“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="99441-120">For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</span></span> <span data-ttu-id="99441-121">如果他们开展销售，也希望跟踪客户。</span><span class="sxs-lookup"><span data-stu-id="99441-121">If they make a sale, they also like to track Customer.</span></span> <span data-ttu-id="99441-122">如果使用此方案，建议为该公司的日记帐指定两个科目结构 - 一个用于资产负债表科目，一个用于损益科目。</span><span class="sxs-lookup"><span data-stu-id="99441-122">Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</span></span> <span data-ttu-id="99441-123">若要优化用户体验和验证，“客户”应该是仅当使用了销售科目时财神爷的高级规则。</span><span class="sxs-lookup"><span data-stu-id="99441-123">To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</span></span>

<span data-ttu-id="99441-124">**资产负债表科目结构**</span><span class="sxs-lookup"><span data-stu-id="99441-124">**Balance sheet account structure**</span></span>

|<span data-ttu-id="99441-125">主科目</span><span class="sxs-lookup"><span data-stu-id="99441-125">Main account</span></span>          | <span data-ttu-id="99441-126">业务单位</span><span class="sxs-lookup"><span data-stu-id="99441-126">Business unit</span></span>    |
|----------------------|-----------|
|<span data-ttu-id="99441-127">100000..399999</span><span class="sxs-lookup"><span data-stu-id="99441-127">100000..399999</span></span> | <span data-ttu-id="99441-128">\*;” “</span><span class="sxs-lookup"><span data-stu-id="99441-128">\*;” “</span></span>|

<span data-ttu-id="99441-129">**损益科目结构**</span><span class="sxs-lookup"><span data-stu-id="99441-129">**Profit and loss account structure**</span></span>

|<span data-ttu-id="99441-130">主科目</span><span class="sxs-lookup"><span data-stu-id="99441-130">Main account</span></span>          | <span data-ttu-id="99441-131">业务单位</span><span class="sxs-lookup"><span data-stu-id="99441-131">Business unit</span></span>    |<span data-ttu-id="99441-132">部门</span><span class="sxs-lookup"><span data-stu-id="99441-132">Department</span></span>          | <span data-ttu-id="99441-133">成本中心</span><span class="sxs-lookup"><span data-stu-id="99441-133">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="99441-134">400000..999999</span><span class="sxs-lookup"><span data-stu-id="99441-134">400000..999999</span></span> | <span data-ttu-id="99441-135">\*;” “</span><span class="sxs-lookup"><span data-stu-id="99441-135">\*;” “</span></span>|<span data-ttu-id="99441-136">\*;” “</span><span class="sxs-lookup"><span data-stu-id="99441-136">\*;” “</span></span>|<span data-ttu-id="99441-137">\*;” “</span><span class="sxs-lookup"><span data-stu-id="99441-137">\*;” “</span></span>|<span data-ttu-id="99441-138">\*;” “</span><span class="sxs-lookup"><span data-stu-id="99441-138">\*;” “</span></span>|

<span data-ttu-id="99441-139">**用于添加客户的高级规则**</span><span class="sxs-lookup"><span data-stu-id="99441-139">**Advanced rule for adding a Customer**</span></span>

<span data-ttu-id="99441-140">条件：主科目介于 400000 与 499999 之间时，添加客户。</span><span class="sxs-lookup"><span data-stu-id="99441-140">Criteria: Where Main account is between 400000 and 499999, then add customer.</span></span> <span data-ttu-id="99441-141">不能将其保留为空。</span><span class="sxs-lookup"><span data-stu-id="99441-141">It cannot be left blank.</span></span>

|<span data-ttu-id="99441-142">客户</span><span class="sxs-lookup"><span data-stu-id="99441-142">Customer</span></span>         |
|-----------------|
|* |

<span data-ttu-id="99441-143">在这个简化的示例中，允许所有值和空白，所以使用了 \* 和 “ “。</span><span class="sxs-lookup"><span data-stu-id="99441-143">In this simplified example, all values and blank are allowed so \* and “ “ are used.</span></span>

## <a name="segments-and-allowed-values"></a><span data-ttu-id="99441-144">段落和允许的值</span><span class="sxs-lookup"><span data-stu-id="99441-144">Segments and allowed values</span></span>
<span data-ttu-id="99441-145">**科目段** 和 **允许的值详细信息** 部分提供了网格式体验，用于输入过帐期间验证时要遵循的规则。</span><span class="sxs-lookup"><span data-stu-id="99441-145">The **Segments** and **Allowed values details** section provides a grid like experience for entering the rules that will be followed on validation during posting.</span></span> <span data-ttu-id="99441-146">可直接在网格中的单元格内键入，从 Excel 导入，或使用 **允许的值详细信息** 部分引导您完成。</span><span class="sxs-lookup"><span data-stu-id="99441-146">You can type directly in the cells in the grid, import it from Excel, or use the **Allowed value details** section to guide you through it.</span></span>

<span data-ttu-id="99441-147">**允许的值详细信息** 部分可引导您使用开头为、介于、包含等各种 **运算符** 创建条件。</span><span class="sxs-lookup"><span data-stu-id="99441-147">The **Allowed value details** section guides you through creating criteria using **Operators** such as begins with, is between, includes, and many others.</span></span>

<span data-ttu-id="99441-148">[![允许值](./media/account.png)](./media/account.png)</span><span class="sxs-lookup"><span data-stu-id="99441-148">[![Allow values](./media/account.png)](./media/account.png)</span></span> 

<span data-ttu-id="99441-149">在根据科目结构设置没有其他潜在值可供选择时，将把允许的值设置为日记帐或会计分配录入页中的默认值。</span><span class="sxs-lookup"><span data-stu-id="99441-149">Allowed values will default onto a journal or accounting distribution entry page when there are no other possible values to select according to the account structure setup.</span></span>

<span data-ttu-id="99441-150">下面是 **损益科目结构** 的示例。</span><span class="sxs-lookup"><span data-stu-id="99441-150">Here's an example of the **Profit and loss account structure**.</span></span>

|<span data-ttu-id="99441-151">主科目</span><span class="sxs-lookup"><span data-stu-id="99441-151">Main account</span></span>          | <span data-ttu-id="99441-152">业务单位</span><span class="sxs-lookup"><span data-stu-id="99441-152">Business unit</span></span>    |<span data-ttu-id="99441-153">部门</span><span class="sxs-lookup"><span data-stu-id="99441-153">Department</span></span>          | <span data-ttu-id="99441-154">成本中心</span><span class="sxs-lookup"><span data-stu-id="99441-154">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="99441-155">400000..999999</span><span class="sxs-lookup"><span data-stu-id="99441-155">400000..999999</span></span> | <span data-ttu-id="99441-156">002</span><span class="sxs-lookup"><span data-stu-id="99441-156">002</span></span> | <span data-ttu-id="99441-157">022</span><span class="sxs-lookup"><span data-stu-id="99441-157">022</span></span> | <span data-ttu-id="99441-158">014</span><span class="sxs-lookup"><span data-stu-id="99441-158">014</span></span> |

<span data-ttu-id="99441-159">输入日记帐和在损益范围内选择科目时，选择业务单位“002”将导致把值 022 和 014 设置为科目控件上的默认值。</span><span class="sxs-lookup"><span data-stu-id="99441-159">When entering a journal and selecting an account in the profit and loss range, selecting business unit '002' will cause values 022 and 014 to be the default on the account control.</span></span> <span data-ttu-id="99441-160">还将在会计分配页中发生以下行为。</span><span class="sxs-lookup"><span data-stu-id="99441-160">This behavior will also occur with the accounting distribution page.</span></span> 

## <a name="more-than-7-criteria-needed"></a><span data-ttu-id="99441-161">需要 7 个以上的条件</span><span class="sxs-lookup"><span data-stu-id="99441-161">More than 7 criteria needed</span></span>

<span data-ttu-id="99441-162">如果需要的条件超过 7 个，则可在下一行中继续添加条件。</span><span class="sxs-lookup"><span data-stu-id="99441-162">If you have more than 7 criteria that are needed, you can continue adding them on the next line.</span></span> <span data-ttu-id="99441-163">您将发现在 **允许的值详细信息** 部分中工作时，输入了第七个条件之后，**+新添** 添加将不再处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="99441-163">You will notice when working in the **Allowed value details** section that the **+Add new** criteria is nt longer active after the seventh criteria is entered.</span></span> <span data-ttu-id="99441-164">原因很多，例如：</span><span class="sxs-lookup"><span data-stu-id="99441-164">This is due to many factors such as:</span></span> 
 - <span data-ttu-id="99441-165">列宽</span><span class="sxs-lookup"><span data-stu-id="99441-165">Column width</span></span> 
 - <span data-ttu-id="99441-166">数据的存储方式</span><span class="sxs-lookup"><span data-stu-id="99441-166">How the data is stored</span></span> 
 - <span data-ttu-id="99441-167">**允许的值详细信息** 控件的性能</span><span class="sxs-lookup"><span data-stu-id="99441-167">Performance of the **Allowed value details** control</span></span>
 - <span data-ttu-id="99441-168">可用性</span><span class="sxs-lookup"><span data-stu-id="99441-168">Usability</span></span>  
 
<span data-ttu-id="99441-169">若要继续添加更多添加，请单击 **在科目段中复制** 和 **允许的值部分**。</span><span class="sxs-lookup"><span data-stu-id="99441-169">To continue to add additional criteria, click **Duplicate in the Segment** and **Allowed values section**.</span></span> <span data-ttu-id="99441-170">这样就会把条件复制到新行中。</span><span class="sxs-lookup"><span data-stu-id="99441-170">This will copy the criteria to a new line.</span></span> <span data-ttu-id="99441-171">然后可以再次键入或修改 **允许的值详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="99441-171">You can then type over or modify the **Allowed value details** section.</span></span>

## <a name="best-practices"></a><span data-ttu-id="99441-172">最佳实践</span><span class="sxs-lookup"><span data-stu-id="99441-172">Best practices</span></span>
<span data-ttu-id="99441-173">设置科目结构时，可以遵循一些最佳实践。</span><span class="sxs-lookup"><span data-stu-id="99441-173">When setting up your account structures there are some best practices you can follow.</span></span> <span data-ttu-id="99441-174">但是，这只是指导，所以在通盘讨论中应考虑业务、成长计划和维持计划。</span><span class="sxs-lookup"><span data-stu-id="99441-174">However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</span></span>

- <span data-ttu-id="99441-175">让主科目成为科目结构的第一项或尽量靠近科目结构前面，这样用户就可以在录入科目时获得最佳的引导式体验。</span><span class="sxs-lookup"><span data-stu-id="99441-175">Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</span></span>

- <span data-ttu-id="99441-176">尽量重复使用科目结构，以减少法人中的维护。</span><span class="sxs-lookup"><span data-stu-id="99441-176">Reuse account structures as much as possible to reduce maintenance across your legal entities.</span></span>

- <span data-ttu-id="99441-177">对于法人中的变型，请考虑使用高级规则，以便重复使用科目结构。</span><span class="sxs-lookup"><span data-stu-id="99441-177">For variations across legal entities, consider using advanced rules so that account structures can be reused.</span></span>

- <span data-ttu-id="99441-178">定义允许的值时，请尽量使用范围和通配符。</span><span class="sxs-lookup"><span data-stu-id="99441-178">When defining allowed values, use ranges and wildcards as much as possible.</span></span> <span data-ttu-id="99441-179">这样在此配置下不仅可以在不进行维护的情况下增长和变化，而且系统还可以更理想地运行。</span><span class="sxs-lookup"><span data-stu-id="99441-179">This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</span></span>

- <span data-ttu-id="99441-180">请不要只是为科目结构中的每个科目段放一个星号，然后单纯地依赖高级规则。</span><span class="sxs-lookup"><span data-stu-id="99441-180">Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</span></span> <span data-ttu-id="99441-181">这样可能很难管理，往往会在维护期间导致用户错误，从而让系统无法过帐。</span><span class="sxs-lookup"><span data-stu-id="99441-181">This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</span></span>

## <a name="account-structure-activation"></a><span data-ttu-id="99441-182">科目结构启用</span><span class="sxs-lookup"><span data-stu-id="99441-182">Account structure activation</span></span>
<span data-ttu-id="99441-183">如果对科目结构的新设置或更改感到满意，必须将其激活。</span><span class="sxs-lookup"><span data-stu-id="99441-183">When you are satifisfied with your new setup or a change to an account structure, you must activate it.</span></span> <span data-ttu-id="99441-184">如果为日记帐分配了科目结构，此项激活可能需要运行很长一段时间，因为必须将系统中的所有未过帐交易记录同步到新结构中。</span><span class="sxs-lookup"><span data-stu-id="99441-184">If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</span></span> <span data-ttu-id="99441-185">科目结构的变化不影响已过帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="99441-185">Posted transactions are not impacted with account structure changes.</span></span>

<span data-ttu-id="99441-186">有关详细信息，请参阅[计划您的会计科目表](plan-chart-of-accounts.md)、[财务维度](financial-dimensions.md)和[输入科目和维度组合（分段式录入控件）](enter-account-dimension-combinations-segmented-entry-control.md)。</span><span class="sxs-lookup"><span data-stu-id="99441-186">For more information, see [Plan your chart of accounts](plan-chart-of-accounts.md), [Financial dimensions](financial-dimensions.md) and [Enter account and dimension combinations (segmented entry control)](enter-account-dimension-combinations-segmented-entry-control.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]