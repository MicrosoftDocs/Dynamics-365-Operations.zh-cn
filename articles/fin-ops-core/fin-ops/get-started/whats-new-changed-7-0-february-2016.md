---
title: Dynamics AX 7.0（2016 年 2 月）中的新增功能和更改内容
description: 本文介绍了 Microsoft Dynamics AX 7.0 中的新功能和更改的功能。 此版本包含平台和应用程序功能，于 2016 年 2 月发布。
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57e88285c29d13001d5c5586ec4ad8674973f256
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176721"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a><span data-ttu-id="2cf09-104">Dynamics AX 7.0（2016 年 2 月）中的新增功能和更改内容</span><span class="sxs-lookup"><span data-stu-id="2cf09-104">What's new or changed in Dynamics AX 7.0 (February 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cf09-105">本文介绍了 Microsoft Dynamics AX 7.0 中的新功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-105">This article describes features that are either new or changed in Microsoft Dynamics AX 7.0.</span></span> <span data-ttu-id="2cf09-106">此版本包含平台和应用程序功能，于 2016 年 2 月发布。</span><span class="sxs-lookup"><span data-stu-id="2cf09-106">This version contains both platform and application features and was released in February 2016.</span></span>

## <a name="cost-management"></a><span data-ttu-id="2cf09-107">成本管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-107">Cost management</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-108">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-108">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-109">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-109">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-110">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-110">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-111">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-111">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-112">可快速概览库存余额、在制品 (WIP) 库存余额，以及针对所选会计年度的库存流入量和流出量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-112">Get a quick overview of the inventory balance, the work in progress (WIP) inventory balance, and what the inventory inflow and outflow have been for the selected fiscal year.</span></span></td>
<td><span data-ttu-id="2cf09-113">不适用</span><span class="sxs-lookup"><span data-stu-id="2cf09-113">Not applicable</span></span></td>
<td><span data-ttu-id="2cf09-114"><strong>成本管理</strong>工作区包含一个部分，在其中提供了所选会计期间的库存报表和 WIP 库存报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-114">The <strong>Cost administration</strong> workspace contains a section where the inventory statement or WIP inventory statement is presented for the selected fiscal period.</span></span> <span data-ttu-id="2cf09-115">此报表基于数据集缓存，该缓存在默认情况下每 24 小时更新一次。</span><span class="sxs-lookup"><span data-stu-id="2cf09-115">The statement is based on a data set cache that, by default, is updated every 24 hours.</span></span> <span data-ttu-id="2cf09-116">可以配置数据集缓存，以使用户可以手动更新它以实时报告。</span><span class="sxs-lookup"><span data-stu-id="2cf09-116">The data set cache can be configured so that users can manually update it for real-time reporting.</span></span> <span data-ttu-id="2cf09-117"><strong>成本管理</strong>工作区中的<strong>数据刷新状态卡</strong>在最后一次更新缓存时显示。</span><span class="sxs-lookup"><span data-stu-id="2cf09-117">The <strong>Data refresh status card</strong> in the <strong>Cost administration</strong> workspace shows when the cache was last updated.</span></span></td>
<td><span data-ttu-id="2cf09-118">成本总监有兴趣知道库存或 WIP 库存报表余额是随着时间的推移增加还是减少。</span><span class="sxs-lookup"><span data-stu-id="2cf09-118">Cost controllers are interested in knowing whether the inventory or WIP inventory statement balance increases or decreases over time.</span></span> <span data-ttu-id="2cf09-119">通过对报表中的操作事件进行分类，成本总监可以概览库存如何流动。</span><span class="sxs-lookup"><span data-stu-id="2cf09-119">By classifying operational events in the statement, the cost controller can get an overview of how inventory is flowing.</span></span> <span data-ttu-id="2cf09-120">如果库存或 WIP 库存是按标准成本评估的，则还可以查看登记的整体差异。</span><span class="sxs-lookup"><span data-stu-id="2cf09-120">If inventory or WIP inventory is evaluated by standard costs, the overall variance registered can also be seen.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-121">使用<strong>成本管理</strong>模块。</span><span class="sxs-lookup"><span data-stu-id="2cf09-121">Use the <strong>Cost management</strong> module.</span></span></td>
<td><span data-ttu-id="2cf09-122">不适用</span><span class="sxs-lookup"><span data-stu-id="2cf09-122">Not applicable</span></span></td>
<td><span data-ttu-id="2cf09-123">成本管理是作为域区域引入的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-123">Cost management is introduced as a domain area.</span></span> <span data-ttu-id="2cf09-124">成本相关的配置和见解分散在整个库存管理、生产控制和应付账款中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-124">Cost-related configuration and insight were scattered throughout Inventory management, Production control, and Accounts Payable.</span></span></td>
<td><span data-ttu-id="2cf09-125">由于与成本管理关联的所有任务集中在一个模块中，因此更容易让成本总监维护系统。</span><span class="sxs-lookup"><span data-stu-id="2cf09-125">Because all the tasks that are related to cost management are centralized in one module, it will be easier for cost controllers to maintain the system.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-126">与库存会计和生产会计相关的过帐类型已更新。</span><span class="sxs-lookup"><span data-stu-id="2cf09-126">The posting types that are related to inventory accounting and production accounting have been updated.</span></span></td>
<td><span data-ttu-id="2cf09-127"><strong>InventPosting</strong>、<strong>资源</strong>、<strong>ResourceGroup</strong> 和 <strong>ProductionGroup</strong> 窗体中的标签始终不与实际使用的 <strong>LedgerPostingType</strong> 标签一致。</span><span class="sxs-lookup"><span data-stu-id="2cf09-127">The labels in the <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong>, and <strong>ProductionGroup</strong> forms aren't always aligned with the <strong>LedgerPostingType</strong> labels that are actually used.</span></span> <span data-ttu-id="2cf09-128">了解标签中使用的术语并不容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-128">It's not easy to understand the terminology that is used in the labels.</span></span></td>
<td><span data-ttu-id="2cf09-129">这些标签已经更新，因此<strong>InventPosting</strong>、<strong>资源</strong>、<strong>ResourceGroup</strong>和<strong>ProductionGroup</strong>页上的标签始终与实际<strong>LedgerPostingType</strong>标签匹配。</span><span class="sxs-lookup"><span data-stu-id="2cf09-129">The labels have been updated so that labels on the <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong>, and <strong>ProductionGroup</strong> pages match the actual <strong>LedgerPostingType</strong> labels.</span></span> <span data-ttu-id="2cf09-130">还需重命名所有标签，以便标签与操作事件匹配。</span><span class="sxs-lookup"><span data-stu-id="2cf09-130">All the labels have also been renamed so that the labels match the operational events.</span></span> <span data-ttu-id="2cf09-131">请注意，未更改实际过帐逻辑。</span><span class="sxs-lookup"><span data-stu-id="2cf09-131">Note that the actual posting logic hasn't been changed.</span></span></td>
<td><span data-ttu-id="2cf09-132">配置系统更加简单，因为新的标签与使用此过帐类型的操作事件有关。</span><span class="sxs-lookup"><span data-stu-id="2cf09-132">It's easier to configure the system, because the new labels are related to the operational events that use this posting type.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-133">在 Microsoft Excel 或成本计算版本中导出/导入采购价、成本或销售价。</span><span class="sxs-lookup"><span data-stu-id="2cf09-133">Import/export the purchase price, cost, or sales price from Microsoft Excel into or from a costing version.</span></span></td>
<td><span data-ttu-id="2cf09-134">您无法将价格或成本正确导入到成本计算版本，因为数据模型需要 InventDim ID。</span><span class="sxs-lookup"><span data-stu-id="2cf09-134">You can't correctly import prices or costs into a costing version, because the data model requires an InventDim ID.</span></span></td>
<td><span data-ttu-id="2cf09-135">引入数据实体后可以执行导入或导出功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-135">The introduction of data entities makes it possible to implement an import/export feature.</span></span> <span data-ttu-id="2cf09-136">此功能允许用户将价格或成本导入/导出到成本计算版本中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-136">This feature lets users import/export prices or costs into a costing version.</span></span>
<ul>
<li><span data-ttu-id="2cf09-137">导入从采购部门获得的下一年采购价的完整列表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-137">Import a full list of next year's purchase prices that is obtained from the Purchasing department.</span></span></li>
<li><span data-ttu-id="2cf09-138">通过一个操作将成本和标准销售价从总部推送到一个或多个销售公司。</span><span class="sxs-lookup"><span data-stu-id="2cf09-138">Push costs and standard sales prices from headquarters to one or more sales companies in one operation.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-139">它可以在成本总监维护系统时为其节省大量时间，尤其是当他们必须为下一会计年度维护预先确定的成本时。</span><span class="sxs-lookup"><span data-stu-id="2cf09-139">It can save the cost controllers a significant amount of time when they maintain the system, especially when they must maintain predetermined costs for the next fiscal year.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-140">可快速概览成本对象的库存余额和平均单位成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-140">Get a quick overview of the inventory balance and average unit cost of a cost object.</span></span></td>
<td><span data-ttu-id="2cf09-141">用户必须打开现有量窗体并选择反映成本对象的库存维度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-141">The user must open the on-hand form and select the inventory dimensions that reflect the cost object.</span></span> <span data-ttu-id="2cf09-142">因此，用户必须知道为特定产品的财务库存标记了哪些库存维度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-142">Therefore, the user must know which inventory dimensions were marked for financial inventory for the specific product.</span></span></td>
<td><span data-ttu-id="2cf09-143">引入了新的<strong>成本对象</strong>页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-143">A new <strong>Cost object</strong> page is introduced.</span></span> <span data-ttu-id="2cf09-144">默认情况下，此页显示与产品相关的所有成本对象。</span><span class="sxs-lookup"><span data-stu-id="2cf09-144">By default, this page shows all cost objects that are related to the product.</span></span> <span data-ttu-id="2cf09-145">此页显示每个成本对象的当前库存数量、值和平均单位成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-145">The page shows the current inventory quantity, value, and average unit cost per cost object.</span></span></td>
<td><span data-ttu-id="2cf09-146">它消除一些复杂性，使得更容易当一名成本总监。</span><span class="sxs-lookup"><span data-stu-id="2cf09-146">It removes some of the complexity and makes it easier to be a cost controller.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-147">在库存控制期间使用新<strong>成本条目</strong>页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-147">Use the new <strong>Cost entries</strong> page during inventory control.</span></span></td>
<td><span data-ttu-id="2cf09-148">对登记的库存交易记录和相关的结算进行库存控制会很复杂，因为相同的交易记录可以是实际的或财务的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-148">It can be complicated to perform inventory control on registered inventory transactions and related settlements, because the same transactions can be physical or financial.</span></span></td>
<td><span data-ttu-id="2cf09-149"><strong>成本条目</strong>页提供一个新的方式来查看库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-149">The <strong>Cost entries</strong> page offers a new way to view inventory transactions.</span></span>
<ul>
<li><span data-ttu-id="2cf09-150">交易记录按时间顺序显示。</span><span class="sxs-lookup"><span data-stu-id="2cf09-150">Transactions are shown in a chronological order.</span></span></li>
<li><span data-ttu-id="2cf09-151">仅包括对成本有贡献的交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-151">Only transactions that contribute to costs are included.</span></span></li>
<li><span data-ttu-id="2cf09-152">没有实际成本或财务成本的概念。</span><span class="sxs-lookup"><span data-stu-id="2cf09-152">There is no notion of physical costs or financial cost.</span></span></li>
<li><span data-ttu-id="2cf09-153">没有实际数量或财务数量的概念。</span><span class="sxs-lookup"><span data-stu-id="2cf09-153">There is no notion of physical quantity or financial quantity.</span></span></li>
<li><span data-ttu-id="2cf09-154">成本增量添加。</span><span class="sxs-lookup"><span data-stu-id="2cf09-154">The costs are added incrementally.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-155">当成本总监必须在交易记录级别执行库存控制时，它可以使他们节省大量时间。</span><span class="sxs-lookup"><span data-stu-id="2cf09-155">It can save cost controllers a significant amount of time when they must perform inventory control at the transaction level.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-156">使用新的<strong>生产 WIP 报表</strong>对话框可以查看特定产品的累计成本的汇总视图。</span><span class="sxs-lookup"><span data-stu-id="2cf09-156">Use the new <strong>Production WIP statement</strong> dialog box to see a summarized view of accumulated costs for a specific product.</span></span></td>
<td><span data-ttu-id="2cf09-157">不适用</span><span class="sxs-lookup"><span data-stu-id="2cf09-157">Not applicable</span></span></td>
<td><span data-ttu-id="2cf09-158">WIP 报表显示特定生产订单的 WIP 余额汇总，它们已按组分类到相应的成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-158">The WIP statement shows a summarized WIP balance of the specific production order, grouped into appropriate cost classifications.</span></span> <span data-ttu-id="2cf09-159">图表按时间顺序显示操作过帐如何影响 WIP 余额。</span><span class="sxs-lookup"><span data-stu-id="2cf09-159">A chart shows, in chronological order, how operational postings have affected the WIP balance.</span></span></td>
<td><span data-ttu-id="2cf09-160">当成本总监需要了解特定生产订单的当前 WIP 余额，或该订单已消耗的物料数量时，上述报表可以为他们节省大量时间。</span><span class="sxs-lookup"><span data-stu-id="2cf09-160">It can save cost controllers a significant amount of time when they need to know what the current WIP balance is on a specific production order, or how much material has been consumed on the order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-161">使用在生产订单上引入的“查看成本比较”功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-161">Use the View cost comparison feature that has been introduced on production orders.</span></span> <span data-ttu-id="2cf09-162">此功能便于比较与生产订单相关的成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-162">The feature makes it easier to compare costs that are related to a production order.</span></span></td>
<td><span data-ttu-id="2cf09-163">用户可以仅比较估计成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-163">The user can compare only estimated costs and realized costs.</span></span> <span data-ttu-id="2cf09-164">此操作可以在最低级别下完成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-164">The comparison can be done at the lowest level.</span></span></td>
<td><span data-ttu-id="2cf09-165">成本比较功能允许成本总监比较以下数据：</span><span class="sxs-lookup"><span data-stu-id="2cf09-165">The cost comparison feature lets cost controllers compare the following data:</span></span>
<ul>
<li><span data-ttu-id="2cf09-166">有效成本和估计成本 = 计划差异</span><span class="sxs-lookup"><span data-stu-id="2cf09-166">Active cost versus Estimated cost = Planning variance</span></span></li>
<li><span data-ttu-id="2cf09-167">估计成本和实际成本 = 生产差异</span><span class="sxs-lookup"><span data-stu-id="2cf09-167">Estimated cost versus Realized cost = Production variance</span></span></li>
<li><span data-ttu-id="2cf09-168">计划差异 + 生产差异 = 合计差异</span><span class="sxs-lookup"><span data-stu-id="2cf09-168">Planning variance + Production variance = Total variance</span></span></li>
</ul>
<span data-ttu-id="2cf09-169">此功能单独运行，与分配给已生产物料的成本计算方法无关。</span><span class="sxs-lookup"><span data-stu-id="2cf09-169">This feature works independently of costing methods that are assigned to the produced item.</span></span> <span data-ttu-id="2cf09-170">默认情况下，图表按成本组类型显示成本比较。</span><span class="sxs-lookup"><span data-stu-id="2cf09-170">By default, a chart shows the cost comparison by cost group type.</span></span> <span data-ttu-id="2cf09-171">该图表允许用户深入到更详细的级别。</span><span class="sxs-lookup"><span data-stu-id="2cf09-171">The chart lets users drill into more detailed levels.</span></span></td>
<td><span data-ttu-id="2cf09-172">成本总监或生产经理可通过图表分析生产差异的来源，以及导致差异的原因。</span><span class="sxs-lookup"><span data-stu-id="2cf09-172">It lets cost controllers or production managers analyze where the production variances come from, and what causes them.</span></span></td>
</tr>
</tbody>
</table>

## <a name="developer"></a><span data-ttu-id="2cf09-173">开发人员</span><span class="sxs-lookup"><span data-stu-id="2cf09-173">Developer</span></span>

| <span data-ttu-id="2cf09-174">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-174">What can you do?</span></span> | <span data-ttu-id="2cf09-175">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-175">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-176">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-176">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-177">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-177">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-178">在云中创建可从许多设备访问的基于 Web 的解决方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-178">Create web-based solutions in the cloud that are accessible on many devices.</span></span> | <span data-ttu-id="2cf09-179">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-179">Not available</span></span> | <span data-ttu-id="2cf09-180">Dynamics AX 的当前版本是以新的基于 Web 的客户端和客户端框架为基础的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-180">The current version of Dynamics AX is based on a new web-based client and client framework.</span></span> | <span data-ttu-id="2cf09-181">您可以为您的最终用户提供代下一解决方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-181">You can provide next-generation solutions to your end users.</span></span> |
| <span data-ttu-id="2cf09-182">使用 Microsoft Visual Studio 开发解决方法。</span><span class="sxs-lookup"><span data-stu-id="2cf09-182">Use Microsoft Visual Studio to develop your solutions.</span></span> | <span data-ttu-id="2cf09-183">Microsoft MorphX 是主要开发环境，但某些开发在 Visual Studio 中进行。</span><span class="sxs-lookup"><span data-stu-id="2cf09-183">Microsoft MorphX is the main development environment, but some development occurs in Visual Studio.</span></span> | <span data-ttu-id="2cf09-184">Visual Studio 是纯开发环境。</span><span class="sxs-lookup"><span data-stu-id="2cf09-184">Visual Studio is the only development environment.</span></span> | <span data-ttu-id="2cf09-185">它保留熟悉的 Dynamics AX 2012 概念，使它们无缝满足 Visual Studio 框架和范例。</span><span class="sxs-lookup"><span data-stu-id="2cf09-185">It keeps familiar Dynamics AX 2012 concepts, and seamlessly adapts them to the Visual Studio framework and paradigms.</span></span> <span data-ttu-id="2cf09-186">它启用与其他 .NET 语言和项目的标准互操作性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-186">It enables standard interoperability with other .NET languages and projects.</span></span> |
| <span data-ttu-id="2cf09-187">为所有功能编译公共中间语言 (CIL)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-187">Compile Common Intermediate Language (CIL) for all features.</span></span> | <span data-ttu-id="2cf09-188">X++ 编译成 p 代码。</span><span class="sxs-lookup"><span data-stu-id="2cf09-188">X++ is compiled to p-code.</span></span> | <span data-ttu-id="2cf09-189">全新的 X++ 编译器为所有功能生成 CIL。</span><span class="sxs-lookup"><span data-stu-id="2cf09-189">The brand-new X++ compiler generates CIL for all features.</span></span> <span data-ttu-id="2cf09-190">CIL 与其他基于 .NET 的语言所使用的中间语言相同。</span><span class="sxs-lookup"><span data-stu-id="2cf09-190">CIL is the same intermediate language that is used by other .NET-based languages.</span></span> | <span data-ttu-id="2cf09-191">CIL 更快，可以高效地引用托管动态链接库 (DLL) 中的类，并且可以在 .NET 实用程序的大型工具库上运行。</span><span class="sxs-lookup"><span data-stu-id="2cf09-191">CIL is faster, can efficiently reference classes in managed dynamic-link libraries (DLLs), and can run on a large tool base of .NET utilities.</span></span> |
| <span data-ttu-id="2cf09-192">在 Microsoft Dynamics AX 客户端嵌入商业智能 (BI) 报表和可视化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-192">Embed business intelligence (BI) reports and visualizations in the Microsoft Dynamics AX client.</span></span> | <span data-ttu-id="2cf09-193">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-193">Not available</span></span> | <span data-ttu-id="2cf09-194">创建高度直观且可变的可视化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-194">Create highly-intuitive and fluid visualizations.</span></span> | <span data-ttu-id="2cf09-195">它提供基于 BI 的决策见解。</span><span class="sxs-lookup"><span data-stu-id="2cf09-195">It provides decision-making insights that are based on BI.</span></span> |
| <span data-ttu-id="2cf09-196">与 Microsoft Office 集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-196">Integrate with Microsoft Office.</span></span> | <span data-ttu-id="2cf09-197">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-197">Not available</span></span> | <span data-ttu-id="2cf09-198">新增功能包括 Excel Data Connector 应用程序、**工作簿设计器**页、“导出 API”和文档管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-198">New capabilities include the Excel Data Connector app, **Workbook Designer** page, Export API, and Document management.</span></span> | <span data-ttu-id="2cf09-199">您可以为您的最终用户创建工作效率解决方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-199">You can create productivity solutions for your end users.</span></span> |
| <span data-ttu-id="2cf09-200">自动化生成、测试和部署。</span><span class="sxs-lookup"><span data-stu-id="2cf09-200">Automate build, test, and deploy.</span></span> | <span data-ttu-id="2cf09-201">部分可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-201">Partially available</span></span> | <span data-ttu-id="2cf09-202">通过使用 Developer 和 Build VM 部署开发人员拓扑结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-202">Deploy the Developer topology by using Developer and Build VM.</span></span> <span data-ttu-id="2cf09-203">自动配置“构建虚拟机”以从 Visual Studio Online (VSO) 发现、构建模块并运行测试。</span><span class="sxs-lookup"><span data-stu-id="2cf09-203">Auto-configure Build VM to discover, build modules from Visual Studio Online (VSO), and run tests.</span></span> <span data-ttu-id="2cf09-204">支持 C\# 和 X++ 模块编译和引用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-204">C\# and X++ module compilation and references are supported.</span></span> | <span data-ttu-id="2cf09-205">它通过减少测试和验证的成本和工作，提高开发人员的工作效率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-205">It increases developer productivity by reducing cost and effort for testing and validations.</span></span> |
| <span data-ttu-id="2cf09-206">通过覆盖和扩展进行自定义。</span><span class="sxs-lookup"><span data-stu-id="2cf09-206">Customize with overlayering and extensions.</span></span> | <span data-ttu-id="2cf09-207">扩展不可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-207">Extensions aren't available.</span></span> | <span data-ttu-id="2cf09-208">Dynamics AX 的当前版本具有一个新的自定义模型。</span><span class="sxs-lookup"><span data-stu-id="2cf09-208">The current version of Dynamics AX has a new customization model.</span></span> | <span data-ttu-id="2cf09-209">您可以自定义由 Microsoft 或第三方 Microsoft 合作伙伴交付的模型元素的源代码和元数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-209">You can customize source code and metadata of model elements that are shipped by Microsoft or third-party Microsoft partners.</span></span> |
| <span data-ttu-id="2cf09-210">通过使用 X++ 和一个现代 Web 框架，生成新控件和 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="2cf09-210">Build new controls and UI elements by using X++ and a modern web framework.</span></span> | <span data-ttu-id="2cf09-211">自定义控件依赖于外部框架，例如 Microsoft ActiveX 和 Windows Presentation Foundation (WPF)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-211">Custom controls rely on external frameworks such as Microsoft ActiveX and Windows Presentation Foundation (WPF).</span></span> | <span data-ttu-id="2cf09-212">在当前版本中生成控件更容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-212">It's easier to build controls in the current version.</span></span> <span data-ttu-id="2cf09-213">X++ 框架可用于应用程序行为和业务逻辑，基于 HTML/JavaScript 的客户端允许现代化的可视化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-213">The X++ framework can be used for application behavior and business logic, and an HTML/JavaScript-based client allows for modern visualizations.</span></span> | <span data-ttu-id="2cf09-214">您的控件可以设计为外观和行为类似于 Dynamics AX 现成 (OOB) 控件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-214">Your controls can be designed to look and behave just like the Dynamics AX out-of-box (OOB) controls.</span></span> |
| <span data-ttu-id="2cf09-215">通过使用新工具，评估和优化性能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-215">Evaluate and tune performance by using new tools.</span></span> | <span data-ttu-id="2cf09-216">PerfSDK、数据扩展工具包、跟踪分析器 Web 应用程序和 PerfTimer 不可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-216">PerfSDK, Data Expansion Toolkit, Trace Parser WEb app, and PerfTimer aren't available.</span></span> | <span data-ttu-id="2cf09-217">PerfSDK、数据扩展工具包、跟踪分析器 Web 应用程序和 PerfTimer 是新的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-217">PerfSDK, Data Expansion Toolkit, Trace Parser Web app, and PerfTimer are new.</span></span> | <span data-ttu-id="2cf09-218">软件开发配套件 (SDK) 能让您在单用户以及多用户（如果适用）中测试和验证所有关键业务流程的性能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-218">The software development kit (SDK) lets you test and validate all critical business processes for performance in a single-user and, if applicable, multi-user test run.</span></span> <span data-ttu-id="2cf09-219">数据扩展工具包能让您正确展开必须让主数据和交易记录数据正确展开的所有性能测试。</span><span class="sxs-lookup"><span data-stu-id="2cf09-219">The Data Expansion Toolkit lets you correctly expand all performance tests that must have master data and transactional data correctly expanded.</span></span> <span data-ttu-id="2cf09-220">跟踪分析器能让您验证单用户性能测试或多用户运行。</span><span class="sxs-lookup"><span data-stu-id="2cf09-220">The Trace Parser lets you validate a single-user performance test or a multi-user run.</span></span> <span data-ttu-id="2cf09-221">PerfTimer 能让您查看任何查询或任何特定方法调用是否导致性能问题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-221">The PerfTimer lets you see whether any query or any specific method call is causing a performance issue.</span></span> <span data-ttu-id="2cf09-222">因此，您无需执行跟踪和详细分析所有内容。</span><span class="sxs-lookup"><span data-stu-id="2cf09-222">Therefore, you don't have to take a trace and analyze everything in detail.</span></span> |
| <span data-ttu-id="2cf09-223">通过使用 OData 公开可更新的视图。</span><span class="sxs-lookup"><span data-stu-id="2cf09-223">Expose updatable view by using OData.</span></span> | <span data-ttu-id="2cf09-224">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-224">Not available</span></span> | <span data-ttu-id="2cf09-225">Dynamics AX 的当前版本引入公共 OData 服务终结点，它允许在多种类型的客户端上以一致的方式访问 Dynamics AX 数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-225">The current version of Dynamics AX introduces a public OData service endpoint that enables access to Dynamics AX data in a consistent way across a broad range of clients.</span></span> | <span data-ttu-id="2cf09-226">通过使用 HTTP 堆栈协议，您的解决方案可以与 RESTful 服务交互，以可发现方式共享数据，并可启用广泛的集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-226">Your solutions can interact with RESTful services, share data in a discoverable way, and enable broad integration by using the HTTP stack protocol.</span></span> |
| <span data-ttu-id="2cf09-227">利用 Business Connector 编写业务逻辑和支持集成方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-227">Take advantage of the business connector to author business logic and support integration scenarios.</span></span> | <span data-ttu-id="2cf09-228">可使用 Business Connector 从受管代码调用 X++ 代码。</span><span class="sxs-lookup"><span data-stu-id="2cf09-228">The business connector is available to call into X++ code from managed code.</span></span> <span data-ttu-id="2cf09-229">我们建议您仅将 Business Connector 用于编写 C\# 的业务逻辑，不用于集成方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-229">We recommend that you use the business connector only to author business logic in C\#, not for integration scenarios.</span></span> | <span data-ttu-id="2cf09-230">不再支持 Business Connector。</span><span class="sxs-lookup"><span data-stu-id="2cf09-230">The business connector is no longer supported.</span></span> <span data-ttu-id="2cf09-231">只有 X++ 已编译成托管代码才会提供编写要求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-231">The authoring requirement is provided by the fact that X++ is compiled into managed code.</span></span> <span data-ttu-id="2cf09-232">因此，互操作更容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-232">Therefore, interop is easier.</span></span> <span data-ttu-id="2cf09-233">通过使用 OData，满足集成方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-233">The integration scenarios are met by using OData.</span></span> | <span data-ttu-id="2cf09-234">今后您不能使用 Business Connector。</span><span class="sxs-lookup"><span data-stu-id="2cf09-234">You can't use the business connector going forward.</span></span> |
| <span data-ttu-id="2cf09-235">在实际数据库字段和扩展数据类型 (EDT) 上选择标度（即小数位数）。</span><span class="sxs-lookup"><span data-stu-id="2cf09-235">Choose scale (that is, the number of decimal places) on real database fields and extended data types (EDTs).</span></span> | <span data-ttu-id="2cf09-236">标度 16 是默认标度，不能被开发人员更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-236">Scale 16 is the default scale and can't be changed by the developer.</span></span> | <span data-ttu-id="2cf09-237">EDT 和字段现在由一个标度属性，可应用于单个字段和 EDT。</span><span class="sxs-lookup"><span data-stu-id="2cf09-237">EDTs and fields now have a scale property that can be applied to the individual field and EDT.</span></span> <span data-ttu-id="2cf09-238">默认值设置为 6，而不是 16。</span><span class="sxs-lookup"><span data-stu-id="2cf09-238">The default is set to 6, not 16.</span></span> | <span data-ttu-id="2cf09-239">在使用较小标度时，NCCI 表（SQL 中的内存中支持）的性能提高好几个数量级。</span><span class="sxs-lookup"><span data-stu-id="2cf09-239">Performance with NCCI tables (in-memory support in SQL) is faster by orders of magnitude when a smaller scale is used.</span></span> <span data-ttu-id="2cf09-240">根据各个字段的使用需求，更改标度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-240">Change the scale as your use of the individual fields requires.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="2cf09-241">财务管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-241">Financial management</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-242">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-242">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-243">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-243">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-244">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-244">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-245">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-245">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-246">将科目结构导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="2cf09-246">Export account structures to Microsoft Excel.</span></span></td>
<td><span data-ttu-id="2cf09-247">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-247">Not available</span></span></td>
<td><span data-ttu-id="2cf09-248">您现在可选择科目结构并将它导出到 Excel。</span><span class="sxs-lookup"><span data-stu-id="2cf09-248">You can now select an account structure and export it to Excel.</span></span></td>
<td><span data-ttu-id="2cf09-249">许多客户请求能够将科目结构导出到 Excel 以便更容易筛选。</span><span class="sxs-lookup"><span data-stu-id="2cf09-249">Many customers have requested the ability to export account structures to Excel for easier filtering.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-250">查看与单个页面上的科目结构关联的分类帐和高级规则结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-250">View ledgers and advanced rule structures that are associated with an account structure on a single page.</span></span></td>
<td> <span data-ttu-id="2cf09-251">用户必须导航到多个窗体以查看使用的分类帐和科目结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-251">The user must navigate to multiple forms to see the ledger and the account structure that are used.</span></span></td>
<td><span data-ttu-id="2cf09-252">FactBox 已添加到科目结构页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-252">FactBoxes have been added to the account structure page.</span></span></td>
<td><span data-ttu-id="2cf09-253">当定义并编辑科目结构时，对重要信息的访问更容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-253">It's easier to access important information when account structures are defined and edited.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-254">查看与单个页面的会计科目表关联的分类帐。</span><span class="sxs-lookup"><span data-stu-id="2cf09-254">View ledgers that are associated with a chart of accounts on a single page.</span></span></td>
<td><span data-ttu-id="2cf09-255">用户必须导航到每个公司并打开分类帐窗体以查看分配给分类帐的会计科目表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-255">The user must navigate to each company and open the ledger form to see the chart of account that is assigned to the ledger.</span></span></td>
<td><span data-ttu-id="2cf09-256">FactBox 已添加到<strong>会计科目表</strong>页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-256">FactBoxes have been added to the <strong>Chart of accounts</strong> page.</span></span></td>
<td> <span data-ttu-id="2cf09-257">当定义并分配会计科目表时，对重要信息的访问更容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-257">It's easier to access important information when a chart of accounts is defined and assigned.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-258">查看<strong>试算平衡表</strong>列表页上的单独列中的结算单调整和期末交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-258">View closing sheet adjustments and closing transactions in separate columns on the <strong>Trial balance</strong> list page.</span></span></td>
<td><span data-ttu-id="2cf09-259">用户在单个列中查看这两种类型的交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-259">The user sees both types of transactions in a single column.</span></span></td>
<td><span data-ttu-id="2cf09-260">一个附加参数已添加到<strong>试算平衡表</strong>列表页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-260">An additional parameter has been added to the <strong>Trial balance</strong> list page.</span></span></td>
<td><span data-ttu-id="2cf09-261">它允许对数据进行更简明的分析，也是某些国家/地区的管制报表所必需的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-261">It allows for more concise analysis of data and is also required for regulatory reporting in some countries/regions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-262">使用新<strong>全球普通日记帐</strong>页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-262">Use the new <strong>Global general journal</strong> page.</span></span></td>
<td><span data-ttu-id="2cf09-263">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-263">Not available</span></span></td>
<td><span data-ttu-id="2cf09-264">新<strong>全球普通日记帐</strong>页可以输入普通日记帐。</span><span class="sxs-lookup"><span data-stu-id="2cf09-264">New <strong>Global general journal</strong> page to enter general journals.</span></span> <span data-ttu-id="2cf09-265">此页面的权限添加到<strong>会计师</strong>角色。</span><span class="sxs-lookup"><span data-stu-id="2cf09-265">Privileges for this page are added to the <strong>Accountant</strong> role.</span></span></td>
<td><span data-ttu-id="2cf09-266">使共享服务会计师无需退出该窗体或者切换公司上下文即可跨公司输入普通日记帐。</span><span class="sxs-lookup"><span data-stu-id="2cf09-266">Makes it possible for a shared service accountant to enter general journals across companies without having to leave the form or to switch company context.</span></span></td>
</tr> 
<tr>
<td><span data-ttu-id="2cf09-267">使用新<strong>会计源管理器</strong>页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-267">Use the new <strong>Accounting source explorer</strong> page.</span></span></td>
<td><span data-ttu-id="2cf09-268">通过 Dynamics AX 2012 R3 CU10 提供。</span><span class="sxs-lookup"><span data-stu-id="2cf09-268">Available from Dynamics AX 2012 R3 CU10.</span></span></td>
<td><span data-ttu-id="2cf09-269">新<strong>会计源资源管理器</strong>页面和操作可以从<strong>试算平衡表</strong>列表页和<strong>凭证交易记录</strong>页导入到那里。</span><span class="sxs-lookup"><span data-stu-id="2cf09-269">New <strong>Accounting source explorer</strong> page and actions to navigate there from the <strong>Trial balance</strong> list page and the <strong>Voucher transactions</strong> page.</span></span></td>
<td><span data-ttu-id="2cf09-270">可查看总账中的试算平衡表或会计条目或特别分析的最详细的源信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-270">Makes it possible view the most detailed information about the source for a trial balance or an accounting entry in general ledger, or for ad-hoc analysis.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-271">添加其他过帐层。</span><span class="sxs-lookup"><span data-stu-id="2cf09-271">Add additional posting layers.</span></span></td>
<td><span data-ttu-id="2cf09-272">添加其他过帐层属于开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-272">Adding additional posting layers was a developer experience.</span></span></td>
<td><span data-ttu-id="2cf09-273">目前有十个过帐层。</span><span class="sxs-lookup"><span data-stu-id="2cf09-273">Ten posting layers are now available.</span></span></td>
<td><span data-ttu-id="2cf09-274">大多数客户将添加其他过帐层。</span><span class="sxs-lookup"><span data-stu-id="2cf09-274">Most customers add additional posting layers.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-275">使用相关凭证选项。</span><span class="sxs-lookup"><span data-stu-id="2cf09-275">Use the Related voucher option.</span></span></td>
<td><span data-ttu-id="2cf09-276">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-276">Not available</span></span></td>
<td><span data-ttu-id="2cf09-277">相关凭证选项仅供用户在过帐公司内部交易记录时查看对方公司的凭证。</span><span class="sxs-lookup"><span data-stu-id="2cf09-277">The Related voucher option is available for users to see the voucher in the offset company when posting intercompany transactions.</span></span> <span data-ttu-id="2cf09-278">从相关凭证中，用户可以单击详细信息并快速跳转到对方公司凭证。</span><span class="sxs-lookup"><span data-stu-id="2cf09-278">From the related vouchers users can click on the details and quickly jump to the offset company voucher.</span></span></td>
<td><span data-ttu-id="2cf09-279">在过帐公司内部交易记录时，用户无法看到或跟踪在对方公司过帐的凭证。</span><span class="sxs-lookup"><span data-stu-id="2cf09-279">When posting intercompany transactions, users had no visibility or tracing to the voucher that was posted in the offset company.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-280">财务期间批量关闭</span><span class="sxs-lookup"><span data-stu-id="2cf09-280">Mass financial period close</span></span></td>
<td><span data-ttu-id="2cf09-281">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-281">Not available</span></span></td>
<td><span data-ttu-id="2cf09-282">用户可以更新模块访问，并可以一次更改多个公司的期间状态。</span><span class="sxs-lookup"><span data-stu-id="2cf09-282">Users are able to update the module access and change the period status for multiple companies at one time.</span></span></td>
<td><span data-ttu-id="2cf09-283">在使用该功能之前，用户必须更改登录哪些公司，导航到分类帐日历窗体并手动更新模块访问和期间状态。</span><span class="sxs-lookup"><span data-stu-id="2cf09-283">Prior to the feature, users had to change what company they were logged in, navigate to the ledger calendar form and manually update the module access and period status.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-284">有 Oanda 支持的汇率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-284">Have exchange rates powered by Oanda.</span></span></td>
<td><span data-ttu-id="2cf09-285">配置要从 Oanda 导入的汇率提供商属于开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-285">Configuring the exchange rate provider to import rates from Oanda was a developer experience.</span></span></td>
<td><span data-ttu-id="2cf09-286">如果用户有一个 Oanda 密钥，他们可以在配置汇率提供商时输入它。</span><span class="sxs-lookup"><span data-stu-id="2cf09-286">If users have a key for Oanda they can enter it when configuring the exchange rate provider.</span></span></td>
<td><span data-ttu-id="2cf09-287">用户可以通过获得 Oanda 支持的定期导入的汇率来利用现成功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-287">Users can take advantage of out-of-the box functionality by having exchange rates powered by Oanda imported in on a scheduled basis.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-288">基于维度、属性、日期以及方案筛选财务报表 (Management Reporter)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-288">Filter financial reports (Management Reporter) based on dimensions, attributes, dates, and scenarios.</span></span></td>
<td> <span data-ttu-id="2cf09-289">Management Reporter 报表的所有筛选都是通过报表的设计处理的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-289">All filtering of Management Reporter reports is handled through the design of the report.</span></span> <span data-ttu-id="2cf09-290">例如，如果具有查看权限的用户想要查看不同日期的报表，则报表设计器必须进行修改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-290">For example, if a user who has viewing privileges wants to view a report for a different date, a report designer must make the modification.</span></span></td>
<td><span data-ttu-id="2cf09-291">已经添加了报表选项，因此，用户在查看报表时，可以应用不同的筛选器。</span><span class="sxs-lookup"><span data-stu-id="2cf09-291">Report options have been added, so that different filters can be applied when a user is viewing a report.</span></span> <span data-ttu-id="2cf09-292">然后基于这些筛选器生成新报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-292">A new report is then generated based on those filters.</span></span></td>
<td><span data-ttu-id="2cf09-293">财务报表的客户可以针对维度、日期、属性和方案应用不同的筛选器，而不要求更新报表设计。</span><span class="sxs-lookup"><span data-stu-id="2cf09-293">Consumers of financial reports can apply different filters for dimensions, dates, attributes, and scenarios without requiring updates to report designs.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-294">在 Microsoft Dynamics AX 客户端中查看财务报表 (Management Reporter)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-294">View financial reports (Management Reporter) within the Microsoft Dynamics AX client.</span></span></td>
<td><span data-ttu-id="2cf09-295">单独的 Web 客户端用于查看 Management Reporter 报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-295">A separate web client was used to view Management Reporter reports.</span></span></td>
<td><span data-ttu-id="2cf09-296">所有财务报表均可以在 Dynamics AX 客户端访问到。</span><span class="sxs-lookup"><span data-stu-id="2cf09-296">All financial reports can be accessed in the Dynamics AX client.</span></span> <span data-ttu-id="2cf09-297">用户选择要查看的报表，报表将在客户端中显示。</span><span class="sxs-lookup"><span data-stu-id="2cf09-297">The user selects a report to view, and the report is displayed in the client.</span></span></td>
<td><span data-ttu-id="2cf09-298">您现在可以查看财务报表，而不必访问不同的客户端/应用程序。</span><span class="sxs-lookup"><span data-stu-id="2cf09-298">You can now view financial reports without having to access a different client/application.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-299">从 Microsoft Dynamics AX 客户端打印财务报表 (Management Reporter)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-299">Print financial reports (Management Reporter) from the Microsoft Dynamics AX client.</span></span></td>
<td><span data-ttu-id="2cf09-300">打印报表将使用浏览器的打印选项进行打印，但只打印用户可以在屏幕上看到的内容。</span><span class="sxs-lookup"><span data-stu-id="2cf09-300">Printing a report would use the browser's print options for printing and only prints what the user can see on the screen.</span></span></td>
<td><span data-ttu-id="2cf09-301">通过使用 Dynamics AX 客户端财务报表中的打印选项，用户可以选择报表的详细级别和页面设置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-301">The user can choose the detail level and page setup for a report by using the Print option in the financial report in the Dynamics AX client.</span></span></td>
<td><span data-ttu-id="2cf09-302">打印的报表按用户期望而不是打印网页的方式打印。</span><span class="sxs-lookup"><span data-stu-id="2cf09-302">Printed reports print in the way users expect instead of printing a web page.</span></span></td>
</tr><tr>
<td><span data-ttu-id="2cf09-303">通过使用“监控财务业绩”Power BI 内容分析财务数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-303">Analyze financial data by using the "Monitor financial performance" Power BI content.</span></span></td>
<td><span data-ttu-id="2cf09-304">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-304">Not available</span></span></td>
<td><span data-ttu-id="2cf09-305">在 PowerBI.com 上，选择<strong>获取数据</strong>，然后选择 <strong>Dynamics AX – 财务绩效</strong>内容包。</span><span class="sxs-lookup"><span data-stu-id="2cf09-305">On PowerBI.com, select <strong>Get Data</strong>, and then select the <strong>Dynamics AX – Financial performance</strong> content pack.</span></span> <span data-ttu-id="2cf09-306">输入您的 Dynamics AX 终结点的 URL 以查看反映在仪表板中的数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-306">Enter the URL for your Dynamics AX endpoint to see your data reflected in the dashboard.</span></span></td>
<td><span data-ttu-id="2cf09-307">通过三到四次单击，组织可以部署一个包含重要财务数据的 Power BI 仪表板。</span><span class="sxs-lookup"><span data-stu-id="2cf09-307">In three to four clicks, organizations can deploy a Power BI dashboard that contains important financial data.</span></span> <span data-ttu-id="2cf09-308">内容可由组织个性化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-308">Content can be personalized by the organization.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-309">跟踪财务期间结帐流程。</span><span class="sxs-lookup"><span data-stu-id="2cf09-309">Track financial period closing processes.</span></span></td>
<td><span data-ttu-id="2cf09-310">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-310">Not available</span></span></td>
<td><span data-ttu-id="2cf09-311">通过使用财务期间结帐配置，可以创建结帐模板和计划。</span><span class="sxs-lookup"><span data-stu-id="2cf09-311">Closing templates and schedules can be created by using the Financial period close configuration.</span></span> <span data-ttu-id="2cf09-312">使用<strong>财务期间结帐</strong>工作区可跨多个公司跟踪结帐计划的进度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-312">Use the <strong>Financial period close</strong> workspace to track the progress of closing schedules across multiple companies.</span></span></td>
<td><span data-ttu-id="2cf09-313">此工作区消除用于定义、计划和沟通结帐活动的手动系统。</span><span class="sxs-lookup"><span data-stu-id="2cf09-313">This workspace eliminates manual systems to define, schedule, and communicate close activities.</span></span> <span data-ttu-id="2cf09-314">因此，结帐天数会减少。</span><span class="sxs-lookup"><span data-stu-id="2cf09-314">Therefore, the number of days to close is reduced.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-315">使用<strong>分类帐预算和预测</strong>工作区和附加的查询窗体，监控预算值与实际值，创建分类帐预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-315">Monitor budget versus actuals, and create ledger forecasts by using the <strong>Ledger budgets and forecasts</strong> workspace and additional inquiry forms.</span></span></td>
<td><span data-ttu-id="2cf09-316">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-316">Not available</span></span></td>
<td> <span data-ttu-id="2cf09-317">该工作区可以通过 Dynamics AX 仪表板访问。</span><span class="sxs-lookup"><span data-stu-id="2cf09-317">The workspace can be accessed through the Dynamics AX dashboard.</span></span> <span data-ttu-id="2cf09-318">包含指向若干新查询页的链接：<strong>实际和预算汇总</strong>、<strong>预算控制统计汇总</strong>、<strong>预算登记簿条目</strong>和<strong>预算计划</strong>。</span><span class="sxs-lookup"><span data-stu-id="2cf09-318">It includes links to several new inquiry pages: <strong>Actuals vs. budget summary</strong>, <strong>Budget control statistic summary</strong>, <strong>Budget register entries</strong>, and <strong>Budget plans</strong>.</span></span></td>
<td><span data-ttu-id="2cf09-319">新的查询页便于您输入预算信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-319">New inquiry pages enable easy access to budget information.</span></span> <span data-ttu-id="2cf09-320">该工作区将所有预算维护和监控任务组合到一个地方，便于预算经理或会计经理使用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-320">The workspace combines all budget maintenance and monitoring tasks in one place that is easy for budget managers or accounting managers to use.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-321">为预算计划和预测创建布局。</span><span class="sxs-lookup"><span data-stu-id="2cf09-321">Create layouts for budget plans and forecasts.</span></span></td>
<td><span data-ttu-id="2cf09-322"><strong>预算计划</strong>文档显示为一个行列表，其中各行具有财务维度组合的生效日期和金额。</span><span class="sxs-lookup"><span data-stu-id="2cf09-322">The <strong>Budget plan</strong> document is viewed as a list of lines that have effective dates and amounts for combinations of financial dimensions.</span></span> <span data-ttu-id="2cf09-323">用户必须创建和使用 Excel 模板查看数据透视表中的预算计划数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-323">The user must create and use Excel templates to view budget plan data in a PivotTable.</span></span></td>
<td><span data-ttu-id="2cf09-324">无限数量的布局可用于预算计划和预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-324">An unlimited number of layouts is available for budget plans and forecasts.</span></span> <span data-ttu-id="2cf09-325">您可以将所选的财务维度、用户定义的列和其他行属性（例如注释、项目和资产）组合到布局中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-325">You can combine selected financial dimensions, user-defined columns, and other row attributes (such as comments, projects, and assets) in the layout.</span></span> <span data-ttu-id="2cf09-326">用户可以通过使用任何所选的格式，在运行中切换预算计划文档的布局和编辑数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-326">Users can switch the layout for the budget plan document on the fly and edit data by using any selected layout.</span></span> <span data-ttu-id="2cf09-327">通过清除方案约束和使用布局定义在预算计划文档的每个阶段可以查看和编辑哪些数据，可简化预算计划的配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-327">The configuration of budget planning is simplified by eliminating scenario constraints and using layouts to define which data can be viewed and edited in each stage of the budget plan document.</span></span></td>
<td><span data-ttu-id="2cf09-328">它能让您通过使用 Excel 和 Dynamics AX 客户端，灵活地创建和编辑预算计划。</span><span class="sxs-lookup"><span data-stu-id="2cf09-328">It gives the flexibility to create and edit budget plans by using both Excel and the Dynamics AX client.</span></span> <span data-ttu-id="2cf09-329">通过使用预算计划布局设置可以生成 Excel 工作簿模板。</span><span class="sxs-lookup"><span data-stu-id="2cf09-329">Templates for Excel workbooks can be generated by using the Budget plan layout setup.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-330">通过使用<strong>未结明细表</strong>报表（其中包括逾期天数）中的信息，打印<strong>供应商发票交易记录</strong>报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-330">Print the <strong>Vendor Invoice Transactions</strong> report by using information from the <strong>Detailed Due Day List</strong> report, which includes the days past due.</span></span></td>
<td><span data-ttu-id="2cf09-331">您必须首先打印两个不同报表：<strong>未结明细表</strong>和<strong>供应商发票交易记录</strong>。</span><span class="sxs-lookup"><span data-stu-id="2cf09-331">You must print two different reports: <strong>Detailed Due Day List</strong> and <strong>Vendor Invoice Transactions</strong>.</span></span></td>
<td><span data-ttu-id="2cf09-332">有关这两个报表的信息已合并到<strong>供应商发票交易记录</strong>报表中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-332">The information on the two reports has been consolidated into the <strong>Vendor Invoice Transactions</strong> report.</span></span> <span data-ttu-id="2cf09-333"><strong>未结明细表</strong>报表已弃用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-333">The <strong>Detailed Due Day List</strong> report was deprecated.</span></span></td>
<td><span data-ttu-id="2cf09-334">有了它，就不必打印两个独立但相关的报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-334">It eliminates the need to print two separate but related reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-335">直接以 PDF 格式生成管制报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-335">Generate regulatory reports directly in PDF format.</span></span></td>
<td><span data-ttu-id="2cf09-336">您必须首先以一种格式生成一个管制报表，然后将其导出到 PDF 格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-336">You must first generate a regulatory report in one format and then export it to PDF format.</span></span></td>
<td><span data-ttu-id="2cf09-337">PDF 格式是管制报表的默认格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-337">The PDF format is the default format for regulatory reports.</span></span></td>
<td><span data-ttu-id="2cf09-338">它在计算机监视器和打印的纸质副本上提供统一的显示体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-338">It provides a unified display experience on both the computer monitor and a printed paper copy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-339">作为批处理运行销售税结算流程。</span><span class="sxs-lookup"><span data-stu-id="2cf09-339">Run the sales tax settlement process as a batch process.</span></span></td>
<td><span data-ttu-id="2cf09-340">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-340">Not available</span></span></td>
<td><span data-ttu-id="2cf09-341">在<strong>销售税结算期间</strong>页上，您可以指定结算流程应以批处理模式运行。</span><span class="sxs-lookup"><span data-stu-id="2cf09-341">On the <strong>Sales tax settlement period</strong> page, you can specify that the settlement process should be run in batch mode.</span></span></td>
<td><span data-ttu-id="2cf09-342">对于有很多涉税交易记录的期间，结算流程可能非常耗时，而作为批处理进程在后台运行该进程可能更好。</span><span class="sxs-lookup"><span data-stu-id="2cf09-342">For periods that have many tax transactions, the settlement process can be time consuming, and it might be better to run the process in the background as a batch process.</span></span></td>
</tr>
</tbody>
</table>

## <a name="foundation"></a><span data-ttu-id="2cf09-343">基础</span><span class="sxs-lookup"><span data-stu-id="2cf09-343">Foundation</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-344">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-344">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-345">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-345">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-346">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-346">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-347">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-347">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-348">随时随地访问客户端。</span><span class="sxs-lookup"><span data-stu-id="2cf09-348">Access the client anytime, anywhere.</span></span></td>
<td><span data-ttu-id="2cf09-349">AX 2012 桌面客户端提供全套窗体，但它只能在运行 Microsoft Windows 的计算机上运行并要求安装。</span><span class="sxs-lookup"><span data-stu-id="2cf09-349">The AX 2012 desktop client provides a full set of forms, but it can run only on computers that run Microsoft Windows and requires installation.</span></span> <span data-ttu-id="2cf09-350">终端服务器通常与桌面客户端一起使用，来启用通过广域网 (WAN) 的访问。</span><span class="sxs-lookup"><span data-stu-id="2cf09-350">Terminal Server is often used with the desktop client to enable access over a wide area network (WAN).</span></span> <span data-ttu-id="2cf09-351">企业门户 Web 客户端提供更少的窗体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-351">The Enterprise Portal web client provides a reduced set of forms.</span></span></td>
<td><span data-ttu-id="2cf09-352">这两个 AX 2012 客户端已经被单个的、基于标准的 Web 客户端替换了，该客户端连同企业门户客户端一起提供全套桌面客户端功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-352">The two AX 2012 clients have been replaced by a single, standards-based web client that provides the full set of functionality of the desktop client together with the reach of the Enterprise Portal client.</span></span></td>
<td><span data-ttu-id="2cf09-353">它防止开发工作在两个 UI 平台之间被拆分。</span><span class="sxs-lookup"><span data-stu-id="2cf09-353">It prevents development efforts from being split between two UI platforms.</span></span> <span data-ttu-id="2cf09-354">通过使用标准 Web 界面，它消除了对终端服务器的需要。</span><span class="sxs-lookup"><span data-stu-id="2cf09-354">By using standard web interfaces, it eliminates the need for Terminal Server.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-355">通过使用新的任务录制器，更有工作效率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-355">Be productive by using the new Task recorder.</span></span></td>
<td><span data-ttu-id="2cf09-356">AX 2012 任务录制器需要直接访问应用程序对象服务器 (AOS) 计算机的权限和提高的权限，不提供编辑选项。</span><span class="sxs-lookup"><span data-stu-id="2cf09-356">The AX 2012 Task recorder requires direct access to an Application Object Server (AOS) computer and elevated privileges, and provides no editing options.</span></span></td>
<td><span data-ttu-id="2cf09-357">新任务录制器可以直接从 Web 客户端使用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-357">The new Task recorder can be used directly from the web client.</span></span> <span data-ttu-id="2cf09-358">对任务录制器的访问不要求管理员权限。</span><span class="sxs-lookup"><span data-stu-id="2cf09-358">Access to Task recorder doesn't require admin privileges.</span></span> <span data-ttu-id="2cf09-359">记录的步骤可以在记录的同时实时查看，引入了新的编辑选项卡，而且除了现有业务流程建模器 (BPM) 方案，任务录制器还支持更多方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-359">Recorded steps can be viewed live as you record, new editing options have been introduced, and Task recorder supports more scenarios in addition to existing Business process modeler (BPM) scenarios.</span></span></td>
<td><span data-ttu-id="2cf09-360">新任务录制器提供简化的体验，并在 Dynamics AX 中提供新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-360">The new Task recorder provides a streamlined experience and powers new capabilities in Dynamics AX.</span></span> <span data-ttu-id="2cf09-361">其中某些功能立即可用，而未来会推出更多功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-361">Some of these capabilities are available now, and more will follow in the future.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-362">通过工作区帮助用户更好地了解其即将到来的工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-362">Help users better understand their upcoming work with workspaces.</span></span></td>
<td><span data-ttu-id="2cf09-363">角色中心提供与在企业或组织中的用户的工作职能的有关信息的概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-363">Role centers provide an overview of information that pertains to a user's job function in the business or organization.</span></span></td>
<td><span data-ttu-id="2cf09-364">工作区是 Dynamics AX 中的新概念，旨在作为替换角色中心的主要方式以导航到任务和特定页面。</span><span class="sxs-lookup"><span data-stu-id="2cf09-364">Workspaces are a new concept in Dynamics AX that are meant to replace role centers as the primary way to navigate to tasks and specific pages.</span></span> <span data-ttu-id="2cf09-365">它们提供了业务活动的一页概览，并帮助用户了解当前状态、即将到来的工作负荷，以及流程或用户的表现。</span><span class="sxs-lookup"><span data-stu-id="2cf09-365">They provide a one-page overview of a business activity and help users to understand the current status, the upcoming workload, and the performance of the process or user.</span></span> <span data-ttu-id="2cf09-366">工作区比 AX 2012 角色中心更细化，用户可能可以访问多个工作区。</span><span class="sxs-lookup"><span data-stu-id="2cf09-366">Workspaces are more granular than AX 2012 role centers, and a user may have access to multiple workspaces.</span></span></td>
<td><span data-ttu-id="2cf09-367">工作区旨在提高用户生产效率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-367">Workspaces are meant to increase user productivity.</span></span> <span data-ttu-id="2cf09-368">开发人员需要为产品支持的每个重大“活动”创建工作区。</span><span class="sxs-lookup"><span data-stu-id="2cf09-368">Developers will need to create a workspace for every significant "activity" supported in the product.</span></span> <span data-ttu-id="2cf09-369">AX 2012 的传统角色中心通常会被 Dynamics AX 的当前版本的多个工作区替换。</span><span class="sxs-lookup"><span data-stu-id="2cf09-369">A legacy role center from AX 2012 will typically be replaced by multiple workspaces in the current version of Dynamics AX.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-370">使窗体响应浏览器视区或设备大小。</span><span class="sxs-lookup"><span data-stu-id="2cf09-370">Make forms responsive to browser viewport or device size.</span></span></td>
<td><span data-ttu-id="2cf09-371">在 AX 2012 中，窗体内容使用列严格布置，整个窗体高度/宽度很大程度上基于窗体上的控件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-371">In AX 2012, form content was rigidly laid out using columns, and the overall form height/width was largely determined based on the controls on the form.</span></span></td>
<td><span data-ttu-id="2cf09-372">切换到最新的 Dynamics AX 中的 Web，窗体尺寸现在基于浏览器视区大小或设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-372">With the shift to the web in the latest Dynamics AX, a form's dimensions are now based on the browser viewport size or device.</span></span> <span data-ttu-id="2cf09-373">控件和布局参数已修改或添加以更好地响应视区大小的变化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-373">Controls and layout parameters have been modified or added to better respond to changes in viewport size.</span></span></td>
<td><span data-ttu-id="2cf09-374">窗体内容需要更快地响应，以最佳方式利用可用的浏览器或设备的高度/宽度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-374">Form content needs to be more responsive to optimally utilize the available height/width of the browser or device.</span></span> <span data-ttu-id="2cf09-375">实现响应能力可能需要以窗体进行建模的方法更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-375">Achieving responsiveness may require changes in the way a form is modeled.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-376">将模式用于增强窗体的开发经验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-376">Use patterns for an enhanced form development experience.</span></span></td>
<td><span data-ttu-id="2cf09-377">窗体模板是基于窗体样式作为 AX 2012 中窗体开发的起点提供。</span><span class="sxs-lookup"><span data-stu-id="2cf09-377">Form templates were available as starting points for form development in AX 2012 based on a form style.</span></span> <span data-ttu-id="2cf09-378">窗体样式检查器（可选附加项）提供窗体如何源自其相应模板的信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-378">The Form Style Checker, an optional add-in, provided information on how a form deviated from its corresponding template.</span></span></td>
<td><span data-ttu-id="2cf09-379">在当前版本中的 Dynamics AX 中，引入了窗体模式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-379">In the current version of Dynamics AX, form patterns have been introduced.</span></span> <span data-ttu-id="2cf09-380">窗体模式代表紧密地集成到开发体验的窗体模板和窗体样式检查器的组合。</span><span class="sxs-lookup"><span data-stu-id="2cf09-380">Form patterns represent a combination of form templates and the Form Style Checker tightly integrated into the development experience.</span></span> <span data-ttu-id="2cf09-381">模式已在窗体级别（如 AX 2012）定义，其他子模式现已在组和选项卡页级别提供。</span><span class="sxs-lookup"><span data-stu-id="2cf09-381">Patterns have been defined at the form level (like AX 2012) with additional subpatterns now available at the group and tab page level.</span></span></td>
<td><span data-ttu-id="2cf09-382">遵守模式的窗体有许多好处，包括更加一致的用户界面、更简单的开发体验、更简单的窗体升级路径和增强的窗体布局响应性信心。</span><span class="sxs-lookup"><span data-stu-id="2cf09-382">Forms that adhere to patterns have many benefits including a more consistent user interface, a simpler development experience, easier form upgrade path, and increased confidence in form layout responsiveness.</span></span></td>
</tr>
</tbody>
</table>

## <a name="help"></a><span data-ttu-id="2cf09-383">帮助</span><span class="sxs-lookup"><span data-stu-id="2cf09-383">Help</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-384">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-384">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-385">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-385">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-386">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-386">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-387">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-387">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-388">通过单击<strong>帮助</strong>，访问引导式程序帮助（任务指南）和概念主题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-388">Access guided procedural Help (task guides) and conceptual topics by clicking <strong>Help</strong>.</span></span></td>
<td><span data-ttu-id="2cf09-389">AX 2012 帮助系统指向本地 Web 服务器上存储的 HTML 主题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-389">The AX 2012 Help system points to HTML topics that are stored on a local web server.</span></span> <span data-ttu-id="2cf09-390">客户和合作伙伴可以创建自己的帮助。</span><span class="sxs-lookup"><span data-stu-id="2cf09-390">Customers and partners can create their own Help.</span></span></td>
<td><span data-ttu-id="2cf09-391">Dynamics AX 的当前版本中的帮助系统显示在 Microsoft Dynamics Lifecycle Services (LCS) BPM 中存储的任务指南。</span><span class="sxs-lookup"><span data-stu-id="2cf09-391">The Help system in the current version of Dynamics AX displays task guides that are stored in Microsoft Dynamics Lifecycle Services (LCS) BPM.</span></span> <span data-ttu-id="2cf09-392">该帮助系统还显示 Microsoft 文档站点中的主题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-392">The Help system also displays topics from the Microsoft docs site.</span></span> <span data-ttu-id="2cf09-393">有关详细信息，请参阅 <a href="help-overview.md" data-raw-source="[Dynamics AX Help - Getting Started](help-overview.md)">Dynamics AX 帮助 - 入门</a>和<a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides available (February 2016)](new-task-guides-available-february-2016.md)">新推出的任务指南（2016 年 2 月）</a>.</span><span class="sxs-lookup"><span data-stu-id="2cf09-393">For more information, see <a href="help-overview.md" data-raw-source="[Dynamics AX Help - Getting Started](help-overview.md)">Dynamics AX Help - Getting Started</a> and <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides available (February 2016)](new-task-guides-available-february-2016.md)">New task guides available (February 2016)</a>.</span></span></td>
<td><span data-ttu-id="2cf09-394">任务指南提供引导、交互式的体验，带领您完成任务或业务流程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="2cf09-394">Task guides provide a guided, interactive experience that leads you through the steps of a task or business process.</span></span> <span data-ttu-id="2cf09-395">您可以下载和自定义 Microsoft 提供的任务指南。</span><span class="sxs-lookup"><span data-stu-id="2cf09-395">You can download and customize the task guides that Microsoft provides.</span></span> <span data-ttu-id="2cf09-396">本主题提供了更快、更灵活的方式来创建、交付和更新产品文档。</span><span class="sxs-lookup"><span data-stu-id="2cf09-396">The topic provides a faster and more flexible way to create, deliver, and update product documentation.</span></span> <span data-ttu-id="2cf09-397">因此，它有助于确保您有权访问最新技术信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-397">Therefore, it helps guarantee that you have access to the latest technical information.</span></span></td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a><span data-ttu-id="2cf09-398">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-398">Human capital management</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-399">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-399">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-400">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-400">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-401">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-401">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-402">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-402">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-403">在完成课程时将技能和证书传送给课程参与者。</span><span class="sxs-lookup"><span data-stu-id="2cf09-403">Transfer skills and certificates to class participants upon course completion.</span></span></td>
<td><span data-ttu-id="2cf09-404">这是手动流程。</span><span class="sxs-lookup"><span data-stu-id="2cf09-404">This is a manual process.</span></span></td>
<td><span data-ttu-id="2cf09-405">课程完成时会提供一个新选项，以便使用新的技能和证书更新参与者的记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-405">When a course is completed, a new option becomes available to update a participant's records with the new skills and certificates.</span></span></td>
<td><span data-ttu-id="2cf09-406">它提供了新的、有效的方式来更新员工记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-406">It provides a new and efficient way to update employee records.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-407">快速验证雇用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-407">Quickly verify employment.</span></span></td>
<td><span data-ttu-id="2cf09-408">这是手动流程。</span><span class="sxs-lookup"><span data-stu-id="2cf09-408">This is a manual process.</span></span></td>
<td><span data-ttu-id="2cf09-409">您的人力资源部门可以通过使用工作区或员工页，快速验证雇用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-409">Your HR department can quickly verify employment by using a workspace or the employee page.</span></span></td>
<td><span data-ttu-id="2cf09-410">您的人力资源部门不再需要访问多个页面来验证开始日期、经理、在职月数以及薪酬数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-410">Your HR department no longer has to access multiple pages to verify the start date, manager, months in the position, and compensation data.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-411">让员工查看、更新和删除系统中的信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-411">Let employees view, update, and delete information in the system.</span></span></td>
<td><span data-ttu-id="2cf09-412">可用，但只有有限的查看和更新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-412">Available, but with limited view and update capabilities.</span></span></td>
<td><span data-ttu-id="2cf09-413">此功能已启用，可让员工和合同工查看多种个人数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-413">This feature is enabled, and lets employees and contractors view a wide range of personal data.</span></span> <span data-ttu-id="2cf09-414">或者，当创建、更新或删除信息时，可以使用工作流。</span><span class="sxs-lookup"><span data-stu-id="2cf09-414">Optionally, a workflow can be used when information is created, updated, or deleted.</span></span></td>
<td><span data-ttu-id="2cf09-415">它允许员工控制自己的信息，无论信息否与更新地址或联系人信息、申请工作、参与调查问卷或更新图像有关。</span><span class="sxs-lookup"><span data-stu-id="2cf09-415">It lets employees take control of their information, whether that involves updating address or contact information, applying for a job, taking a questionnaire, or updating their image.</span></span> <span data-ttu-id="2cf09-416">在启用工作流时，根据您的业务流程，信息可以由审核人审批或自动审批。</span><span class="sxs-lookup"><span data-stu-id="2cf09-416">When a workflow is enabled, information can be reviewed by an approver or automatically approved, based on your business processes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-417">允许经理查看或编辑员工信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-417">Let managers view or edit employee information.</span></span></td>
<td><span data-ttu-id="2cf09-418">可用，但只有有限的查看和更新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-418">Available, but with limited view and update capabilities.</span></span></td>
<td><span data-ttu-id="2cf09-419">根据配置设置和安全性，经理可以查看或编辑员工信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-419">Depending on configuration settings and security, managers can view or edit employee information.</span></span></td>
<td><span data-ttu-id="2cf09-420">它允许经理访问重要员工数据，因此，他们可以针对资源、绩效和员工发展作出更好的决策。</span><span class="sxs-lookup"><span data-stu-id="2cf09-420">It lets managers access important employee data, so that they can make better decisions about resourcing, performance, and employee development.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-421">利用经理自助服务功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-421">Take advantage of manager self-service functionality.</span></span></td>
<td><span data-ttu-id="2cf09-422">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-422">Not available</span></span></td>
<td><span data-ttu-id="2cf09-423">经理现在可以提交新雇佣（员工和承包商）、转岗和终止（结束雇用）请求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-423">Managers can now submit requests for new hires (employees and contractors), transfers and termination (ending employment).</span></span> <span data-ttu-id="2cf09-424">经理还可以请求一个新职位、扩展职位持续时间，或请求职位更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-424">Managers can also request a new position, extend a positions duration, or request position changes.</span></span></td>
<td><span data-ttu-id="2cf09-425">这些方案以前只向人力资源公开。</span><span class="sxs-lookup"><span data-stu-id="2cf09-425">These scenarios were previously only exposed to Human Resources.</span></span> <span data-ttu-id="2cf09-426">启用这些方案在组织中为经理提供功能强大的工具。</span><span class="sxs-lookup"><span data-stu-id="2cf09-426">Enabling these scenarios provides powerful tools to managers in an organization.</span></span> <span data-ttu-id="2cf09-427">可以启用可选工作流，以提供适当级别的审查和审核。</span><span class="sxs-lookup"><span data-stu-id="2cf09-427">Optional workflows can be enabled to provide the right level of review and approvals.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-428">访问薪酬处理的结果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-428">Access the results of compensation processing.</span></span></td>
<td><span data-ttu-id="2cf09-429">结果仅在处理时可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-429">Results are available only at the time of processing.</span></span></td>
<td><span data-ttu-id="2cf09-430">在运行流程后，现在可以随时访问薪酬处理结果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-430">Compensation processing results can now be accessed at any point after the process has been run.</span></span></td>
<td><span data-ttu-id="2cf09-431">它可卓越地审核流程和流程的结果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-431">It provides an excellent audit of the process and the outcome of the process.</span></span> <span data-ttu-id="2cf09-432">它还在员工记录更新之前提供数据的全面概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-432">It also provides a comprehensive view of the data before employee records are updated.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-433">访问福利处理的结果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-433">Access the results of benefit processing.</span></span></td>
<td><span data-ttu-id="2cf09-434">结果仅在处理时可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-434">Results are available only at the time of processing.</span></span></td>
<td><span data-ttu-id="2cf09-435">在运行流程后，现在可以随时访问福利处理结果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-435">Benefits processing results can now be accessed at any point after the process has been run.</span></span></td>
<td><span data-ttu-id="2cf09-436">它提供福利登记和成本变化所更新的数据的全面概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-436">It provides a comprehensive view of the data that is updated by benefit enrollment and cost changes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-437">查看“有效日期”时间线更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-437">View "Date Effective" timeline changes.</span></span></td>
<td><span data-ttu-id="2cf09-438">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-438">Not available</span></span></td>
<td><span data-ttu-id="2cf09-439">这一比较工具可用于员工、职位和工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-439">This comparison tool is available for employees, positions, and jobs.</span></span> <span data-ttu-id="2cf09-440">它提供了从记录的一个版本到另一个版本的更改的全面概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-440">It provides a comprehensive view of changes from one version of a record to another.</span></span></td>
<td><span data-ttu-id="2cf09-441">在您查看随时间推移发生的员工、职位和工作记录更改时，它为您节省时间。</span><span class="sxs-lookup"><span data-stu-id="2cf09-441">It saves you time when you view changes that have occurred over time to employees, positions, and job records.</span></span> <span data-ttu-id="2cf09-442">它能让您随着时间的推移快速比较记录的两个版本，或者所有记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-442">It lets you quickly compare two versions of a record, or all records, over time.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-443">按公司查看员工。</span><span class="sxs-lookup"><span data-stu-id="2cf09-443">View employees by company.</span></span></td>
<td><span data-ttu-id="2cf09-444">这是通过筛选执行的手动流程。</span><span class="sxs-lookup"><span data-stu-id="2cf09-444">This is a manual process that is performed through filtering.</span></span></td>
<td><span data-ttu-id="2cf09-445">员工和合同工列表按您登录的公司自动筛选。</span><span class="sxs-lookup"><span data-stu-id="2cf09-445">Employee and contractor lists are automatically filtered by the company that you're logged on to.</span></span></td>
<td><span data-ttu-id="2cf09-446">它提供了在登录到的公司中就职的员工的筛选视图。</span><span class="sxs-lookup"><span data-stu-id="2cf09-446">It provides a filtered view of employees who are employed in the logged-on company.</span></span> <span data-ttu-id="2cf09-447">对于所有员工和合同工的未筛选视图，工作人员列表仍可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-447">For an unfiltered view of all employees and contractors, the worker list is still available.</span></span> <span data-ttu-id="2cf09-448">在 Dynamics AX 的当前版本中，系统不基于在列表中选定的员工更改公司。</span><span class="sxs-lookup"><span data-stu-id="2cf09-448">In the current version of Dynamics AX, the system doesn't change company based on the employee that is selected in the list.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-449">更新课程参与者列表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-449">Update the course participants list.</span></span></td>
<td><span data-ttu-id="2cf09-450">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-450">Not available</span></span></td>
<td><span data-ttu-id="2cf09-451">可以从参与者列表中删除课程参与者。</span><span class="sxs-lookup"><span data-stu-id="2cf09-451">Course participants can be removed from the participants list.</span></span></td>
<td><span data-ttu-id="2cf09-452">它提供了一个简单的方式来更新错误登记的课程参与者。</span><span class="sxs-lookup"><span data-stu-id="2cf09-452">It provides an easy way to update course participants who registered by mistake.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-453">按组管理薪酬事件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-453">Manage compensation events in a group.</span></span></td>
<td><span data-ttu-id="2cf09-454">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-454">Not available</span></span></td>
<td><span data-ttu-id="2cf09-455">此功能简化处理员工的薪酬更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-455">This feature streamlines the processing of compensation changes for employees.</span></span></td>
<td><span data-ttu-id="2cf09-456">它提供一个简单、简化的流程来通过薪酬工作区和相关页面更新员工记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-456">It provides a simple, streamlined process for updating employee records through the compensation workspace and related pages.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a><span data-ttu-id="2cf09-457">库存管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-457">Inventory management</span></span>

<span data-ttu-id="2cf09-458">未添加新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-458">No new features have been added.</span></span>

## <a name="localization"></a><span data-ttu-id="2cf09-459">本地化</span><span class="sxs-lookup"><span data-stu-id="2cf09-459">Localization</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-460">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-460">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-461">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-461">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-462">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-462">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-463">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-463">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-464">配置并生成电子文档以满足不同国家/地区的法规要求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-464">Configure and generate electronic documents to meet the legal requirements in various countries/regions.</span></span></td>
<td><span data-ttu-id="2cf09-465">电子文档是以 X++ 格式硬编码的，或者作为可扩展样式表语言转换 (XSLT) 硬编码的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-465">Electronic documents are hard-coded in X++ or as Extensible Stylesheet Language Transformations (XSLTs).</span></span> <span data-ttu-id="2cf09-466">所有格式调整都需要开发工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-466">Any format adjustments require development efforts.</span></span> <span data-ttu-id="2cf09-467">对数据和格式的访问未隔离。</span><span class="sxs-lookup"><span data-stu-id="2cf09-467">Access to data and formatting aren't isolated.</span></span> <span data-ttu-id="2cf09-468">已调整的格式部署要求覆盖该现有格式的新的 Microsoft Dynamics AX 修补程序包。</span><span class="sxs-lookup"><span data-stu-id="2cf09-468">An adjusted format deployment requires a new Microsoft Dynamics AX hotfix package that overrides the existing format.</span></span> <span data-ttu-id="2cf09-469">每个格式的自定义修改都必须手动导入新 Microsoft Dynamics AX 修补程序包的源代码中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-469">Custom modifications of each format must be manually ported to the source code of a new Microsoft Dynamics AX hotfix package.</span></span></td>
<td><span data-ttu-id="2cf09-470">电子申报 (ER) 是一个新工具，用于配置和生成针对业务用户而不是开发人员的电子文档。</span><span class="sxs-lookup"><span data-stu-id="2cf09-470">Electronic Reporting (ER) is a new tool for configuring and generating electronic documents that target a business user instead of a developer.</span></span> <span data-ttu-id="2cf09-471">ER 能让您将域特定的且独立于 Microsoft Dynamics AX 数据库的数据模型设置为文档格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="2cf09-471">ER lets you set up data models that are domain-specific and independent of the Microsoft Dynamics AX database as data sources for document formats.</span></span> <span data-ttu-id="2cf09-472">业务用户可以基于这些域特定的数据模型来配置格式（例如，对于付款、内部统计报告或税金报表）。</span><span class="sxs-lookup"><span data-stu-id="2cf09-472">A business user can configure the formats, based on these domain-specific data models (for example, for payments, Intrastat reports, or tax reports).</span></span> <span data-ttu-id="2cf09-473">用户通过使用类似于 Excel 的一种简单、直观的工具来配置格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-473">The user configures the formats by using simple visual tools that are similar to Excel.</span></span> <span data-ttu-id="2cf09-474">ER 当前支持生成文本、XML 和 Excel 格式的电子文档。</span><span class="sxs-lookup"><span data-stu-id="2cf09-474">ER currently supports the generation of electronic documents in text, XML, and Excel formats.</span></span> <span data-ttu-id="2cf09-475">这些文档可以同时生成并打包到到 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-475">These documents can be generated simultaneously and packed into zip files.</span></span> <span data-ttu-id="2cf09-476">支持模型和格式数据版本控制。</span><span class="sxs-lookup"><span data-stu-id="2cf09-476">Data models and formats support versioning.</span></span> <span data-ttu-id="2cf09-477">格式版本可以具有有效期间。</span><span class="sxs-lookup"><span data-stu-id="2cf09-477">Format versions can have effective periods.</span></span> <span data-ttu-id="2cf09-478">每个数据模型或格式版本都存储在单独的配置中，并通过 LCS 分发给合作伙伴和客户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-478">Each data model or format version is stored in a separate configuration and distributed to partners and customers through LCS.</span></span> <span data-ttu-id="2cf09-479">合作伙伴和客户可以自定义 Microsoft 数据模型和格式，或者创建自己的数据模型和格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-479">Partners and customers can customize Microsoft data models and formats, or create their own.</span></span> <span data-ttu-id="2cf09-480">ER 将合作伙伴和客户配置更改保存为 Microsoft 配置的增量，以便简化到 Microsoft 配置的新版本的升级。</span><span class="sxs-lookup"><span data-stu-id="2cf09-480">ER saves partner and customer configuration changes as deltas to Microsoft configurations, which simplifies upgrades to new versions of Microsoft configurations.</span></span> <span data-ttu-id="2cf09-481">通过使用 LCS，合作伙伴还可以与其他合作伙伴和客户共享数据模型和格式配置，其他合作伙伴和客户可以自定义和共享它们。</span><span class="sxs-lookup"><span data-stu-id="2cf09-481">By using LCS, partners can also share their data model and format configurations with other partners and customers, who can customize and share them.</span></span> <span data-ttu-id="2cf09-482">增量自定义和简易升级通过整个自定义链受支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-482">Delta customization and easy upgrade are supported through the whole customization chain.</span></span></td>
<td><span data-ttu-id="2cf09-483">ER 简化电子文档格式的创建、维护和升级，以便符合不同国家/地区的法规要求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-483">ER simplifies the creation, maintenance, and upgrade of electronic document formats to meet legal requirements in various countries/regions.</span></span> <span data-ttu-id="2cf09-484">ER 使创建或更改电子文档格式的流程更快、更容易。</span><span class="sxs-lookup"><span data-stu-id="2cf09-484">ER makes the process of creating or changing electronic document formats faster and easier.</span></span> <span data-ttu-id="2cf09-485">这些更改可以由业务用户而不是开发人员完成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-485">These changes can be made by business users instead of developers.</span></span> <span data-ttu-id="2cf09-486">ER 使合作伙伴和客户更快、更容易将格式自定义升级到由 Microsoft 或其他合作伙伴发布的新版本格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-486">ER makes it faster and easier for partners and customers to upgrade their format customizations to new versions of formats that are released by Microsoft or other partners.</span></span> <span data-ttu-id="2cf09-487">ER 提供一种常见方式（通过 LCS）让 Microsoft 和合作伙伴将电子文档配置分发给其他合作伙伴和客户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-487">ER provides one common way (through LCS) for Microsoft and partners to distribute electronic document configurations to other partners and customers.</span></span> <span data-ttu-id="2cf09-488">ER 还使合作伙伴和客户更容易特定业务需求自定义、升级和分发电子文档格式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-488">ER also makes it easier for partners and customers to customize, upgrade, and distribute electronic document formats for their specific business requirements.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-489">(MEX) 生成墨西哥增值税 (VAT) 管制报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-489">(MEX) Generate Mexican value-added tax (VAT) regulatory reports.</span></span></td>
<td><span data-ttu-id="2cf09-490">您必须通过使用未实现的销售增值税功能来生成<strong>销售和采购增值税</strong>报表，因此，用户可以基于状态来识别属于已实现部分和未实现部分的交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-490">You must generate <strong>Sales and Purchases VAT</strong> reports by using the unrealized VAT functionality, so that users can identify transactions that belong to the realized and unrealized sections based on the status.</span></span></td>
<td><span data-ttu-id="2cf09-491"><strong>销售和采购增值税</strong>报表已经修改，现在仅通过未实现和已实现销售税代码的定义的特定结算期间来考虑特殊增值税功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-491"><strong>Sales and Purchases VAT</strong> reports were modified and now consider the conditional tax feature only by using specific settlement periods for the definition of unrealized and realized sales tax codes.</span></span></td>
<td><span data-ttu-id="2cf09-492">需要更改销售税代码的配置，然后用户才能正确生成这些报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-492">Changes in the configuration of sales tax codes are required before users can generate these reports correctly.</span></span> <span data-ttu-id="2cf09-493">需要特殊增值税功能，并且，用户必须配置单独的结算期间、未实现的已实现的，从而在相关部分区域识别交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-493">A conditional sales tax feature is required, and the user must configure separate settlement periods, unrealized and realized, to identify the transactions in the related section areas.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-494">(JPN) 管理日本固定资产加速折旧申报文档。</span><span class="sxs-lookup"><span data-stu-id="2cf09-494">(JPN) Manage the Japanese fixed asset accelerated depreciation declaration document.</span></span></td>
<td><span data-ttu-id="2cf09-495">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-495">Not available</span></span></td>
<td><span data-ttu-id="2cf09-496">重要申报信息集中存储在一个文档中，以便更好地维护。</span><span class="sxs-lookup"><span data-stu-id="2cf09-496">Important declaration information is centrally stored in a single document for better maintenance.</span></span></td>
<td><span data-ttu-id="2cf09-497">在审核和其他审查期间，文档符合性和管理简便性可帮助减少问题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-497">Document compliance and ease of management help reduce issues during audits and other reviews.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-498">(JPN) 验证银行帐户上的 JBA 字符。</span><span class="sxs-lookup"><span data-stu-id="2cf09-498">(JPN) Verify JBA characters on the bank account.</span></span></td>
<td><span data-ttu-id="2cf09-499">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-499">Not available</span></span></td>
<td><span data-ttu-id="2cf09-500">您可以验证假名字段是否仅包含 JBA 银行格式允许的字符。</span><span class="sxs-lookup"><span data-stu-id="2cf09-500">You can verify that kana name fields contain only the characters that are permitted by the JBA bank format.</span></span></td>
<td><span data-ttu-id="2cf09-501">由于无效字符，它可帮助在生成付款文档时减少对用户的干扰。</span><span class="sxs-lookup"><span data-stu-id="2cf09-501">It helps reduce interruptions to users during payment file generation because of invalid characters.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-502">(JPN) 在会计年度结束时跟进日本固定资产尾差。</span><span class="sxs-lookup"><span data-stu-id="2cf09-502">(JPN) Catch up the Japan fixed asset penny difference at the end of the fiscal year.</span></span></td>
<td><span data-ttu-id="2cf09-503">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-503">Not available</span></span></td>
<td><span data-ttu-id="2cf09-504">在<strong>固定资产参数</strong>页上，您可以选择在会计期间或会计年度结束时跟进。</span><span class="sxs-lookup"><span data-stu-id="2cf09-504">On the <strong>Fixed asset parameters</strong> page, you can choose to catch up at the end of the fiscal period or the fiscal year.</span></span></td>
<td><span data-ttu-id="2cf09-505">它提供更大的灵活性来符合当地风俗。</span><span class="sxs-lookup"><span data-stu-id="2cf09-505">It provides more flexibility to match local practices.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-506">(JPN) 生成日本公司纳税申报追加表 16 系列（按固定资产主要类型汇总的金额）。</span><span class="sxs-lookup"><span data-stu-id="2cf09-506">(JPN) Generate the Japanese Corporate Tax Declaration Appended Tables 16 series at a summarized amount by fixed asset major type.</span></span></td>
<td><span data-ttu-id="2cf09-507">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-507">Not available</span></span></td>
<td><span data-ttu-id="2cf09-508">在固定资产的价值模型上，您可以选择按主要类型汇总。</span><span class="sxs-lookup"><span data-stu-id="2cf09-508">On the value models of a fixed asset, you can choose to summarize by major type.</span></span> <span data-ttu-id="2cf09-509">默认情况下，此功能用于新创建的固定资产。</span><span class="sxs-lookup"><span data-stu-id="2cf09-509">By default, this functionality is used for newly created fixed assets.</span></span></td>
<td><span data-ttu-id="2cf09-510">对于具有数以千计固定资产的大型公司，汇总报表极大地减少生成报表的规模。</span><span class="sxs-lookup"><span data-stu-id="2cf09-510">For large corporations that have thousands of fixed assets, the summarized reports greatly reduce the size of the report that is generated.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-511">(JPN) 从下一会计年度开始针对日本固定资产分配特殊折旧准备金。</span><span class="sxs-lookup"><span data-stu-id="2cf09-511">(JPN) Start to allocate Special depreciation reserve from the next fiscal year for Japan fixed assets.</span></span></td>
<td><span data-ttu-id="2cf09-512">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-512">Not available</span></span></td>
<td><span data-ttu-id="2cf09-513">在具有相应的特别折旧模板的固定资产价值模型上，您可以选择从下一会计期间或下一会计年度开始分配。</span><span class="sxs-lookup"><span data-stu-id="2cf09-513">On the value models of a fixed asset that has an appropriate extraordinary depreciation profile, you can choose to start allocation from the next fiscal period or the next fiscal year.</span></span></td>
<td><span data-ttu-id="2cf09-514">它提供更大的灵活性来符合当地风俗。</span><span class="sxs-lookup"><span data-stu-id="2cf09-514">It provides more flexibility to match local practices.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-515">(JPN) 生成包括修订税率的日本消费税报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-515">(JPN) Generate a Japan consumption tax report that includes the revised tax rates.</span></span></td>
<td><span data-ttu-id="2cf09-516">消费税报表可用于 5% 的税率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-516">The consumption tax report is available for a tax rate of 5 percent.</span></span></td>
<td><span data-ttu-id="2cf09-517">消费税报表包含一个用于修订税率（例如，8%）的部分。</span><span class="sxs-lookup"><span data-stu-id="2cf09-517">The consumption tax report contains a section for the revised tax rate (for example, 8 percent).</span></span></td>
<td><span data-ttu-id="2cf09-518">布局是由政府新公布的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-518">The layout was newly announced by the government.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-519">(EU) 为欧盟销售清单配置舍入设置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-519">(EU) Configure rounding settings for EU sales list.</span></span></td>
<td><span data-ttu-id="2cf09-520">各个国家/地区的欧盟销售清单报告的舍入设置是硬编码，使用 X ++ 或可扩展样式表语言转换 (XSLT)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-520">Rounding settings for the EU sales list reporting for various countries/regions are hard-coded in X++ or in Extensible Stylesheet Language Transformations (XSLTs).</span></span></td>
<td><span data-ttu-id="2cf09-521">舍入设置添加到外贸参数。</span><span class="sxs-lookup"><span data-stu-id="2cf09-521">Rounding settings are added to Foreign trade parameters.</span></span> <span data-ttu-id="2cf09-522">您可以为小于舍入精度的金额配置舍入精度、舍入方法、输出精度和行为。</span><span class="sxs-lookup"><span data-stu-id="2cf09-522">You can configure rounding precision, rounding method, output precision, and the behavior for amounts smaller than the rounding precision.</span></span></td>
<td><span data-ttu-id="2cf09-523">这将统一并简化欧盟销售清单报告的配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-523">This unifies and simplifies the configuration of the EU sales list reporting.</span></span> <span data-ttu-id="2cf09-524">舍入设置的调整不再需要开发工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-524">Adjustment of rounding settings no longer requires development efforts.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-525">(EU) 配置冲销费用适用性规则。</span><span class="sxs-lookup"><span data-stu-id="2cf09-525">(EU) Configure reverse charge applicability rules.</span></span></td>
<td><span data-ttu-id="2cf09-526">冲销费用适用规则被硬编码为国内冲销费用方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-526">Reverse charge applicability rules are hard-coded for the domestic reverse charge scenario.</span></span> <span data-ttu-id="2cf09-527">适用性阈值可以为每个物料组设置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-527">The applicability threshold can be set up per item group.</span></span> <span data-ttu-id="2cf09-528">该功能仅可用于英国。</span><span class="sxs-lookup"><span data-stu-id="2cf09-528">The functionality is available to Great Britain only.</span></span></td>
<td><span data-ttu-id="2cf09-529">您可以配置每个文档类型（采购/销售订单、供应商发票、普通发票等）的冲销费用适用规则，以及组合物料、物料组和采购/销售类别的冲销费用组。</span><span class="sxs-lookup"><span data-stu-id="2cf09-529">You can configure reverse charge applicability rules per document type (purchase/sales order, vendor invoice, free text invoice, etc.) and a reverse charge group that combines items, items groups, and purchase/sales categories.</span></span> <span data-ttu-id="2cf09-530">适用规则具有有效日期。</span><span class="sxs-lookup"><span data-stu-id="2cf09-530">The applicability rules are date effective.</span></span> <span data-ttu-id="2cf09-531">您还可以将销售税组中的单个销售税代码标记为适用于冲销费用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-531">You can also mark individual sales tax codes in sales tax groups as applicable for reverse charge.</span></span> <span data-ttu-id="2cf09-532">销售发票报表进行调整来表示应用冲销费用的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-532">The sales invoice report is adjusted to represent details of the applied reverse charge.</span></span> <span data-ttu-id="2cf09-533">此功能可用于所有国家/地区。</span><span class="sxs-lookup"><span data-stu-id="2cf09-533">The functionality is available to all European countries/regions.</span></span></td>
<td><span data-ttu-id="2cf09-534">此更改将统一冲销费用适用规则的配置，并支持欧洲国家/地区的国内冲销费用法规的采用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-534">This change unifies the configuration of the reverse charge applicability rules and supports the adoption of the domestic reverse charge regulations by European countries/regions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-535">(DE) 生成德国审计文件 - GDPdUGoBD</span><span class="sxs-lookup"><span data-stu-id="2cf09-535">(DE) Generate the German audit file - GDPdUGoBD</span></span></td>
<td><span data-ttu-id="2cf09-536">用户可以设置包含使用德国审计机构和监管机构接受的格式导出的财务数据的表的定义。</span><span class="sxs-lookup"><span data-stu-id="2cf09-536">Users can set up definition of tables containing financial data to be exported in a format accepted by German auditors and authorities.</span></span></td>
<td><span data-ttu-id="2cf09-537">此功能已作为电子申报配置实现。</span><span class="sxs-lookup"><span data-stu-id="2cf09-537">The feature has been implemented as an electronic reporting configuration.</span></span> <span data-ttu-id="2cf09-538">该功能可用于德国和奥地利。</span><span class="sxs-lookup"><span data-stu-id="2cf09-538">The functionality is available to Germany and Austria.</span></span></td>
<td><span data-ttu-id="2cf09-539">这一更改为用户提供数据格式、转换的更多可能性，还提供了所有来自电子申报配置生命周期管理的优点，如轻松配置汇率、版本控制等。</span><span class="sxs-lookup"><span data-stu-id="2cf09-539">This change gives user much more possibilities in data formatting, transformations, and also provides all the benefits coming from electronic reporting configuration lifecycle management, like easy configuration exchange, versioning, etc.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-540">(FR) 具有组合计科目的余额表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-540">(FR) Balance list with group total accounts report.</span></span></td>
<td><span data-ttu-id="2cf09-541">具有组合计科目的余额表作为 SSRS 报表 (LedgerAccountSum_FR) 实现。</span><span class="sxs-lookup"><span data-stu-id="2cf09-541">Balance list with group total accounts report is implemented as SSRS report (LedgerAccountSum_FR).</span></span></td>
<td><span data-ttu-id="2cf09-542">具有组合计科目的余额表作为 LCS 资产库本地化财务报表文件夹中提供的管理报表器报表实现。</span><span class="sxs-lookup"><span data-stu-id="2cf09-542">Balance list with group total accounts report is implemented as Management Reporter report available in LCS Asset library localized financial reports folder.</span></span></td>
<td><span data-ttu-id="2cf09-543">这使用户能够通过在管理报表器中使用财务报表来获取自定义项的所有优点和自由。</span><span class="sxs-lookup"><span data-stu-id="2cf09-543">This allows users to get all the benefits and freedom in customizations from using financial reports in Management Reporter.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-544">(EU) 付款的付款通知报、出席单和控制表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-544">(EU) Payment advice, Attending note and Control reports for payments.</span></span></td>
<td><span data-ttu-id="2cf09-545">所有这些报表已实现，为 SSRS 报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-545">All those reports are implemented and SSRS reports.</span></span></td>
<td><span data-ttu-id="2cf09-546">这些报表已实现为 Open XML 模板，用于 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="2cf09-546">These reports have been implemented as Open XML templates to be used in Microsoft Excel.</span></span></td>
<td><span data-ttu-id="2cf09-547">电子支付配置包含付款文件格式设置和模板。</span><span class="sxs-lookup"><span data-stu-id="2cf09-547">Electronic payment configurations contain payment file format setup and templates.</span></span> <span data-ttu-id="2cf09-548">这使用户能够通过使用电子申报来获取报表自定义的所有优点和自由。</span><span class="sxs-lookup"><span data-stu-id="2cf09-548">This allows users to get all the benefits and freedom in report customizations from using Electronic reporting.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-549">(EU) 为内部统计配置舍入设置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-549">(EU) Configure rounding settings for Intrastat.</span></span></td>
<td><span data-ttu-id="2cf09-550">各个国家/地区的内部统计报告的舍入设置是硬编码，使用 X ++ 或可扩展样式表语言转换 (XSLT)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-550">Rounding settings for the Intrastat reporting for various countries/regions are hard-coded in X++ or in Extensible Stylesheet Language Transformations (XSLTs).</span></span></td>
<td><span data-ttu-id="2cf09-551">舍入设置添加到外贸参数。</span><span class="sxs-lookup"><span data-stu-id="2cf09-551">Rounding settings are added to foreign trade parameters.</span></span> <span data-ttu-id="2cf09-552">您可以为小于舍入精度的金额配置舍入精度、舍入方法、输出精度和行为。</span><span class="sxs-lookup"><span data-stu-id="2cf09-552">You can configure rounding precision, rounding method, output precision, and the behavior for amounts smaller than the rounding precision.</span></span></td>
<td><span data-ttu-id="2cf09-553">这将统一并简化内部统计报告的配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-553">This unifies and simplifies the configuration of the Intrastat reporting.</span></span> <span data-ttu-id="2cf09-554">舍入设置的调整不再需要开发工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-554">Adjustment of rounding settings no longer requires development efforts.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-555">(EU) 设置类别层次结构中的内部统计商品代码。</span><span class="sxs-lookup"><span data-stu-id="2cf09-555">(EU) Set up Intrastat commodity codes in category hierarchies.</span></span></td>
<span data-ttu-id="2cf09-556">u</span><span class="sxs-lookup"><span data-stu-id="2cf09-556">u</span></span><td><span data-ttu-id="2cf09-557">内部统计商品代码是一个单独的列表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-557">Intrastat commodity codes is a separate list.</span></span> <span data-ttu-id="2cf09-558">虽然存在商品代码类型的类别层次结构，这些商品代码无法在 Retail HQent 和销售类别中被视为默认设置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-558">While there is category hierarchy of type Commodity code, these commodity codes could be defaulted in Retail HQent and sales categories.</span></span></td>
<td><span data-ttu-id="2cf09-559">单独的内部统计商品代码列表与商品代码类型的产品层次结构合并。</span><span class="sxs-lookup"><span data-stu-id="2cf09-559">Separate list of Intrastat commodity codes are merged with product hierarchy of type Commodity code.</span></span></td>
<td><span data-ttu-id="2cf09-560">这将统一将商品代码分配给销售和采购单据中已发布产品和类别的方法。</span><span class="sxs-lookup"><span data-stu-id="2cf09-560">This unifies the approach for assigning commodity codes to released products and categories in sales and purchase documents.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-561">(EU) 通过使用单位转换设置报告内部统计的其他单位的数量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-561">(EU) Report quantity in additional units for Intrastat by using unit conversion setting.</span></span></td>
<td><span data-ttu-id="2cf09-562">内部统计商品代码有一个文本字段，以标识其他单位，<strong>产品</strong>卡有一个字段来标识其他单位（千克）的数量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-562">Intrastat commodity code has a text field to identify additional units, and the <strong>Product</strong> card has a field to identify the quantity of additional units in kilograms.</span></span></td>
<td><span data-ttu-id="2cf09-563">用于内部统计商品代码的其他单位从“单位”列表中选择。</span><span class="sxs-lookup"><span data-stu-id="2cf09-563">Additional units for Intrastat commodity code is chosen from the list of Units.</span></span> <span data-ttu-id="2cf09-564">通过单位转换设置计算其他计价单位的数量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-564">The quantity of additional units is calculated through unit conversion settings.</span></span></td>
<td><span data-ttu-id="2cf09-565">这将统一将交易记录单位重新计算为其他单位的方法。</span><span class="sxs-lookup"><span data-stu-id="2cf09-565">This unifies the approach for recalculation from units of transaction to additional units.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-566">(EU) 将默认运输方法分配到交货方式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-566">(EU) Assign default transport method to mode of delivery.</span></span></td>
<td><span data-ttu-id="2cf09-567">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-567">Not available</span></span></td>
<td><span data-ttu-id="2cf09-568">将默认运输方法字段添加到交货方式。</span><span class="sxs-lookup"><span data-stu-id="2cf09-568">A field for default transport method is added to the Mode of delivery.</span></span></td>
<td><span data-ttu-id="2cf09-569">这简化了内部统计报告的准备的工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-569">This simplifies the preparation of Intrastat reporting.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-570">(EU) 标记发布的产品不要在内部统计中报告。</span><span class="sxs-lookup"><span data-stu-id="2cf09-570">(EU) Mark released product not to be reported in Intrastat.</span></span></td>
<td><span data-ttu-id="2cf09-571">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-571">Not available</span></span></td>
<td><span data-ttu-id="2cf09-572">从内部统计报告中排除物料的选项被添加到已发布产品。</span><span class="sxs-lookup"><span data-stu-id="2cf09-572">An option to exclude the item from Intrastat reporting is added to released product.</span></span></td>
<td><span data-ttu-id="2cf09-573">这简化了内部统计报告的准备的工作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-573">This simplifies the preparation of Intrastat reporting.</span></span></td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a><span data-ttu-id="2cf09-574">制造</span><span class="sxs-lookup"><span data-stu-id="2cf09-574">Manufacturing</span></span>

| <span data-ttu-id="2cf09-575">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-575">What can you do?</span></span> | <span data-ttu-id="2cf09-576">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-576">Dynamics AX 2012</span></span> |
|------------------|------------------|
| <span data-ttu-id="2cf09-577">在单独的页面上针对生产订单执行物料可用性检查，该页面可从**生产车间管理**工作区中打开。</span><span class="sxs-lookup"><span data-stu-id="2cf09-577">Perform a check of material availability for production orders on a separate page that is opened from the **Production floor management** workspace.</span></span> | <span data-ttu-id="2cf09-578">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-578">Not available</span></span> |
| <span data-ttu-id="2cf09-579">通过使用新的**作业卡设备**页，启动并报告生产作业的进度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-579">Start and report progress on production jobs by using the new **Job card device** page.</span></span> | <span data-ttu-id="2cf09-580">**工作登记**窗体主要面向大型终端屏幕，UI 通常通过鼠标单击即可访问。</span><span class="sxs-lookup"><span data-stu-id="2cf09-580">The **Job registration** form is primarily targeted at large terminal screens, and the UI is typically accessed via mouse clicks.</span></span> |

## <a name="master-planning-and-forecasting"></a><span data-ttu-id="2cf09-581">主计划和预测</span><span class="sxs-lookup"><span data-stu-id="2cf09-581">Master planning and forecasting</span></span>

| <span data-ttu-id="2cf09-582">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-582">What can you do?</span></span> | <span data-ttu-id="2cf09-583">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-583">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-584">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-584">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-585">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-585">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-586">如果销售订单或生产订单没有做好按计划日期交货的准备，则将警告用户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-586">Warn the user if a sales order or production order isn't ready for delivery by the scheduled date.</span></span> | <span data-ttu-id="2cf09-587">由主计划创建的警告叫做*预期消息*。</span><span class="sxs-lookup"><span data-stu-id="2cf09-587">The warnings that are created by master planning are called *futures messages*.</span></span> <span data-ttu-id="2cf09-588">*预期*是两个当事方之间的合同，用于按照今天议定的价格（*预期价格*）采购或销售资产，但交货和付款在未来的时间点（*交货日期*）发生。</span><span class="sxs-lookup"><span data-stu-id="2cf09-588">*Futures* is a contract between two parties to buy or sell an asset for a price that is agreed upon today (the *futures price*), although delivery and payment occur at a future point (the *delivery date*).</span></span> | <span data-ttu-id="2cf09-589">*预期消息*和*将来日期*各自重命名了*计算的延迟*和*延期的日期*。</span><span class="sxs-lookup"><span data-stu-id="2cf09-589">*Futures messages* and *futures dates* have been renamed *calculated delays* and *delayed dates*, respectively.</span></span> | <span data-ttu-id="2cf09-590">AX 2012 中使用的术语不准确，导致不正确的翻译。</span><span class="sxs-lookup"><span data-stu-id="2cf09-590">The terminology that is used in AX 2012 was inaccurate and led to incorrect translations.</span></span> |
| <span data-ttu-id="2cf09-591">用户可以快速了解主计划运行的状态、紧急计划订单和导致延迟的计划订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-591">Gain quick insight into the status of a master planning run, urgent planned orders, and planned orders that cause delays.</span></span> | <span data-ttu-id="2cf09-592">该信息可用，但分散在多个窗体中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-592">The information is available, but it's scattered across multiple forms.</span></span> | <span data-ttu-id="2cf09-593">**主计划**工作区提供有关上次主计划运行何时完成、是否发生任何错误、紧急计划订单是什么、以及哪个计划订单导致延迟的概览信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-593">The **Master planning** workspace offers at-a-glance information about when the last master planning run was completed, whether any errors occurred, what the urgent planned orders are, and which planned orders cause delays.</span></span> | <span data-ttu-id="2cf09-594">您可从工作区提供的概览中获益。</span><span class="sxs-lookup"><span data-stu-id="2cf09-594">You benefit from the overview that the workspace provides.</span></span> <span data-ttu-id="2cf09-595">相关信息组合起来，可引导主计划和帮助提高生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-595">Relevant information is put together to guide master planning and help improve productivity.</span></span> |
| <span data-ttu-id="2cf09-596">使用 Excel 更新需求预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-596">Use Excel to update demand forecasts.</span></span> | <span data-ttu-id="2cf09-597">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-597">Not available</span></span> | <span data-ttu-id="2cf09-598">当您输入需求预测、进行更新和删除需求预测时，可以利用与 Excel 的无缝集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-598">You can take advantage of seamless integration with Excel when you enter demand forecasts, make updates, and delete demand forecasts.</span></span> | <span data-ttu-id="2cf09-599">它有助于提高效率和生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-599">It helps increase efficiency and productivity.</span></span> |
| <span data-ttu-id="2cf09-600">根据历史交易记录数据来估计未来需求并创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-600">Estimate future demand and create demand forecasts, based on historical transaction data.</span></span> | <span data-ttu-id="2cf09-601">在 Microsoft Dynamics AX 2012 R3 中，Microsoft SQL Server 分析服务中的预测模型用于创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-601">In Microsoft Dynamics AX 2012 R3, the forecast models in Microsoft SQL Server Analysis Service are used to create demand forecast predictions.</span></span> | <span data-ttu-id="2cf09-602">利用 Microsoft Azure 机器学习云服务的功能和可扩展性来估计未来需求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-602">Estimate future demand by using the power and extensibility of a Microsoft Azure Machine Learning cloud service.</span></span> <span data-ttu-id="2cf09-603">它易于使用和扩展机器学习中的预测模型以满足客户要求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-603">It's easy to use and extend the forecast models in Machine Learning to meet customer requirements.</span></span> <span data-ttu-id="2cf09-604">该服务执行最符合模型选择，并提供可用于计算预测的准确性 (KPI) 的关键绩效指标 (KPI)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-604">The service performs best-match model selection and offers key performance indicators (KPIs) that can be used to calculate forecast accuracy.</span></span> | <span data-ttu-id="2cf09-605">通过使用机器学习技术，生成更准确的预测。</span><span class="sxs-lookup"><span data-stu-id="2cf09-605">Generate more accurate forecasts by using the Machine Learning techniques.</span></span> |
| <span data-ttu-id="2cf09-606">基于主计划运行中的相关操作的可视概览，优化订单日期和数量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-606">Optimize the order date and quantity, based on a visual overview of related actions from the master planning run.</span></span> | <span data-ttu-id="2cf09-607">操作图表概览可用，但会显示所有相关操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-607">The overview of actions chart is available but shows all the related actions.</span></span> <span data-ttu-id="2cf09-608">当应用操作时，操作将立即从视图中消失。</span><span class="sxs-lookup"><span data-stu-id="2cf09-608">When actions are applied, they immediately disappear from the view.</span></span> | <span data-ttu-id="2cf09-609">操作图表提供更好的概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-609">The actions chart provides a better overview.</span></span> <span data-ttu-id="2cf09-610">它包含可用于仅显示已应用操作和直接相关操作的选项。</span><span class="sxs-lookup"><span data-stu-id="2cf09-610">It includes options that let you show only applied actions and directly related actions.</span></span> <span data-ttu-id="2cf09-611">当应用操作时，操作将灰显，但仍显示。</span><span class="sxs-lookup"><span data-stu-id="2cf09-611">When actions are applied, they appear dimmed but are still shown.</span></span> <span data-ttu-id="2cf09-612">因此，概览仍保留。</span><span class="sxs-lookup"><span data-stu-id="2cf09-612">Therefore, the overview is retained.</span></span> <span data-ttu-id="2cf09-613">附加信息添加到操作图表，以在一页上显示数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-613">Additional information is added to the actions chart to display the data on one page.</span></span> | <span data-ttu-id="2cf09-614">您会生产力增强中获益，因为您只侧重于相关操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-614">You benefit from productivity improvement, because you focus only on the relevant actions.</span></span> |

## <a name="procurement-and-sourcing"></a><span data-ttu-id="2cf09-615">采购</span><span class="sxs-lookup"><span data-stu-id="2cf09-615">Procurement and sourcing</span></span>

| <span data-ttu-id="2cf09-616">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-616">What can you do?</span></span> | <span data-ttu-id="2cf09-617">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-617">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-618">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-618">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-619">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-619">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-620">使用**采购订单准备**工作区可快速了解正在准备的采购订单的状态。</span><span class="sxs-lookup"><span data-stu-id="2cf09-620">Use the **Purchase order preparation** workspace to gain quick insight into the status of purchase orders that are being prepared.</span></span> | <span data-ttu-id="2cf09-621">不支持</span><span class="sxs-lookup"><span data-stu-id="2cf09-621">Not supported</span></span> | <span data-ttu-id="2cf09-622">**采购订单准备**工作区提供订单的概览，从订单作为草稿被创建并被跟踪时起，历经工作流审核状态，直到确认。</span><span class="sxs-lookup"><span data-stu-id="2cf09-622">The **Purchase order preparation** workspace provides an overview of orders from the time when they are created as a draft and traced, through workflow approval states, and onward toward confirmation.</span></span> | <span data-ttu-id="2cf09-623">您的采购部门不必再寻求多个页面的信息，而是现在从该工作区提供的概览中获益。</span><span class="sxs-lookup"><span data-stu-id="2cf09-623">Your purchasing department no longer has to seek information from multiple pages but now benefits from the overview that the workspace provides.</span></span> |
| <span data-ttu-id="2cf09-624">使用**采购订单收货和跟进**工作区快速了解正在等待收货的采购订单，以帮助跟进。</span><span class="sxs-lookup"><span data-stu-id="2cf09-624">Use the **Purchase order receipt and follow-up** workspace to gain quick insight into purchase orders that are pending receipt, to help with follow-up.</span></span> | <span data-ttu-id="2cf09-625">不支持</span><span class="sxs-lookup"><span data-stu-id="2cf09-625">Not supported</span></span> | <span data-ttu-id="2cf09-626">**采购订单收货和跟进**工作区提供等待收货或装运的已确认采购订单的概览。</span><span class="sxs-lookup"><span data-stu-id="2cf09-626">The **Purchase order receipt and follow-up** workspace provides an overview of confirmed purchase orders that have pending receipts or shipments.</span></span> <span data-ttu-id="2cf09-627">该工作区包括过期收货和等待收货的列表，用以帮助供应商进行主动审核和跟进。</span><span class="sxs-lookup"><span data-stu-id="2cf09-627">The workspace includes lists of post-due receipts and pending receipts to help with proactive review and follow-up by the supplier.</span></span> <span data-ttu-id="2cf09-628">该工作区还列出已在仓库中发生其到达登记的采购订单，以帮助确保收货得以过帐。</span><span class="sxs-lookup"><span data-stu-id="2cf09-628">The workspace also lists purchase orders that arrival registration has occurred for in the warehouse, to help guarantee that the receipt is posted.</span></span> <span data-ttu-id="2cf09-629">尚未装运的采购订单退货也可用，以供审核。</span><span class="sxs-lookup"><span data-stu-id="2cf09-629">Purchase order returns that haven't yet been shipped are also available for review.</span></span> | <span data-ttu-id="2cf09-630">您的采购部门会从科该工作区提供的概览中获益。</span><span class="sxs-lookup"><span data-stu-id="2cf09-630">Your purchasing department benefits from the overview that the workspace provides.</span></span> <span data-ttu-id="2cf09-631">相关信息组合起来，可引导跟进和帮助提高生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-631">Relevant information is put together to guide follow-up and help improve productivity.</span></span> |
| <span data-ttu-id="2cf09-632">向在 Dynamics AX 客户端中承载的供应商门户发送采购订单以供确认。</span><span class="sxs-lookup"><span data-stu-id="2cf09-632">Send purchase orders for confirmation to a vendor portal hosted in the Dynamics AX client.</span></span> <span data-ttu-id="2cf09-633">允许供应商确认或拒绝。</span><span class="sxs-lookup"><span data-stu-id="2cf09-633">Let the vendor confirm or reject.</span></span> | <span data-ttu-id="2cf09-634">不支持</span><span class="sxs-lookup"><span data-stu-id="2cf09-634">Not supported</span></span> | <span data-ttu-id="2cf09-635">供应商门户界面允许供应商接收采购订单以便确认或拒绝。</span><span class="sxs-lookup"><span data-stu-id="2cf09-635">The vendor portal interface allows vendors to receive purchase orders to be confirmed or rejected.</span></span> <span data-ttu-id="2cf09-636">它还允许供应商概览帐户的所有已确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-636">It also allows the vendor to have an overview of all the confirmed purchase orders for an account.</span></span> <span data-ttu-id="2cf09-637">采购代理可以发送采购订单以请求供应商确认。</span><span class="sxs-lookup"><span data-stu-id="2cf09-637">The purchasing agent can send a purchase order requesting a confirmation from the vendor.</span></span> <span data-ttu-id="2cf09-638">供应商必须是 Dynamics AX 中的一个登记 Microsoft Azure Active Directory (Azure AD) 用户，供应商的联系人有专用的安全角色。</span><span class="sxs-lookup"><span data-stu-id="2cf09-638">The vendor needs to be a registered Microsoft Azure Active Directory (Azure AD) user in Dynamics AX, a contact person for the vendor, and have a dedicated security role.</span></span> | <span data-ttu-id="2cf09-639">您的采购部门从减少书面工作和手动在采购订单上跟踪响应（因为他们直接进入系统）中获益。</span><span class="sxs-lookup"><span data-stu-id="2cf09-639">Your purchasing department benefits from reduced paper work and manually tracking responses on purchase orders, as they flow directly into the system.</span></span> <span data-ttu-id="2cf09-640">具有一个事实来源可减少客户和供应商之间的误解。</span><span class="sxs-lookup"><span data-stu-id="2cf09-640">Having one source of truth reduces misunderstandings between customer and vendor.</span></span> |

## <a name="projects"></a><span data-ttu-id="2cf09-641">项目</span><span class="sxs-lookup"><span data-stu-id="2cf09-641">Projects</span></span>

| <span data-ttu-id="2cf09-642">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-642">What can you do?</span></span> | <span data-ttu-id="2cf09-643">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-643">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-644">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-644">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-645">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-645">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-646">预订工作人员作为项目的资源。</span><span class="sxs-lookup"><span data-stu-id="2cf09-646">Book workers as resources on projects.</span></span> | <span data-ttu-id="2cf09-647">类似于资源，除了资源之外，工作人员是直接在项目中预订的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-647">Similar to resources, workers are booked directly on projects in addition to resources.</span></span> | <span data-ttu-id="2cf09-648">用于存储制造和生产资源的工作中心表现在可用于预订工作人员作为项目的资源。</span><span class="sxs-lookup"><span data-stu-id="2cf09-648">The Work center table where resources for manufacturing and production are stored can now be used to book workers as resources on a project.</span></span> | <span data-ttu-id="2cf09-649">在您预订项目时，您只需预订资源。</span><span class="sxs-lookup"><span data-stu-id="2cf09-649">When you book projects, you only have to book resources.</span></span> |

## <a name="retail-sales-marketing-and-customer-service"></a><span data-ttu-id="2cf09-650">零售销售、市场营销和客户服务</span><span class="sxs-lookup"><span data-stu-id="2cf09-650">Retail sales, marketing, and customer service</span></span>

### <a name="retail-hq"></a><span data-ttu-id="2cf09-651">Retail HQ</span><span class="sxs-lookup"><span data-stu-id="2cf09-651">Retail HQ</span></span>

<span data-ttu-id="2cf09-652">Microsoft Azure 承载的 Retail HQ 能让您通过 Web 客户端集中管理和全面了解商务运营的各个方面。</span><span class="sxs-lookup"><span data-stu-id="2cf09-652">Microsoft Azure-hosted Retail HQ offers centralized management of and complete visibility into all aspects of commerce operations through a web client.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-653">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-653">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-654">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-654">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-655">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-655">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-656">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-656">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-657">执行促销操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-657">Perform merchandizing operations.</span></span></td>
<td><span data-ttu-id="2cf09-658">用户必须访问多个窗体来管理此数据：</span><span class="sxs-lookup"><span data-stu-id="2cf09-658">Users must access multiple forms to manage this data:</span></span>
<ul>
<li><span data-ttu-id="2cf09-659">类别管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-659">Category management</span></span></li>
<li><span data-ttu-id="2cf09-660">产品管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-660">Product management</span></span></li>
<li><span data-ttu-id="2cf09-661">渠道产品属性</span><span class="sxs-lookup"><span data-stu-id="2cf09-661">Channel product attributes</span></span></li>
<li><span data-ttu-id="2cf09-662">分类</span><span class="sxs-lookup"><span data-stu-id="2cf09-662">Assortments</span></span></li>
<li><span data-ttu-id="2cf09-663">目录管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-663">Catalog management</span></span></li>
<li><span data-ttu-id="2cf09-664">配套件</span><span class="sxs-lookup"><span data-stu-id="2cf09-664">Kits</span></span></li>
<li><span data-ttu-id="2cf09-665">价格 &amp; 折扣</span><span class="sxs-lookup"><span data-stu-id="2cf09-665">Prices &amp; discounts</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-666"><strong>类别和产品管理</strong>工作区启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-666">The <strong>Category and product management</strong> workspace enables the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-667">分类管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-667">Assortment management.</span></span></li>
<li><span data-ttu-id="2cf09-668">分类生命周期跟踪。</span><span class="sxs-lookup"><span data-stu-id="2cf09-668">Assortment lifecycle tracking.</span></span></li>
<li><span data-ttu-id="2cf09-669">已发布产品管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-669">Released products management.</span></span></li>
</ul>
<span data-ttu-id="2cf09-670"><strong>价格和折扣管理</strong>工作区启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-670">The <strong>Prices and discounts management workspace</strong> enables the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-671">给定渠道和类别的价格和折扣管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-671">Price and discount management for a given channel and category.</span></span></li>
<li><span data-ttu-id="2cf09-672">类别价格规则管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-672">Category price rule management.</span></span></li>
<li><span data-ttu-id="2cf09-673">价格和折扣优先级，用于让您向价格组和折扣分配优先级，因此，您可以控制应用它们的顺序。</span><span class="sxs-lookup"><span data-stu-id="2cf09-673">Price and discount priorities, which let you assign priorities to price groups and discounts, so that you can control the order that they are applied in.</span></span></li>
<li><span data-ttu-id="2cf09-674">隶属关系和类别折扣管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-674">Affiliation and catalog discount management.</span></span></li>
</ul>
<span data-ttu-id="2cf09-675"><strong>类别管理</strong>工作区启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-675">The <strong>Catalog management</strong> workspace enables the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-676">有效目录的汇总。</span><span class="sxs-lookup"><span data-stu-id="2cf09-676">Summary of active catalogs.</span></span></li>
<li><span data-ttu-id="2cf09-677">单个地点中的目录生命周期跟踪。</span><span class="sxs-lookup"><span data-stu-id="2cf09-677">Catalog lifecycle tracking in a single location.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2cf09-678">工作区通过让工作人员集中管理与促销角色相关的任务和操作，提高工作人员的效率和生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-678">Workspaces improve the efficiency and productivity of workers by letting them centrally manage their tasks and actions that are related to the merchandizing role.</span></span></li>
<li><span data-ttu-id="2cf09-679">价格和折扣优先级功能让客户能够更多地控制如何使用价格和折扣。</span><span class="sxs-lookup"><span data-stu-id="2cf09-679">The price and discount priorities feature gives customers more control over how prices and discounts are used.</span></span> <span data-ttu-id="2cf09-680">此功能还启用新方案，即更高的商店价格战胜标准价格。</span><span class="sxs-lookup"><span data-stu-id="2cf09-680">The feature also enables new scenarios where higher store prices win over standard prices.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-681">管理零售渠道部署和操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-681">Manage retail channel deployments and operations.</span></span></td>
<td><span data-ttu-id="2cf09-682">用户必须访问多个窗体来执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="2cf09-682">The user must access multiple forms to perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2cf09-683">创建和配置新渠道和相关实体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-683">Create and configure new channels and related entities.</span></span></li>
<li><span data-ttu-id="2cf09-684">管理每日商店活动。</span><span class="sxs-lookup"><span data-stu-id="2cf09-684">Manage daily store activities.</span></span></li>
<li><span data-ttu-id="2cf09-685">在 Microsoft Dynamics AX 中处理零售交易记录，生成零售报表，并更新 Microsoft Dynamics AX 库存和财务信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-685">Process retail transactions in Microsoft Dynamics AX, generate retail statements, and update Microsoft Dynamics AX inventory and financials.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="2cf09-686"><strong>渠道部署</strong>工作区能让您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="2cf09-686"><strong>Channel deployment</strong> workspace lets you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2cf09-687">创建新渠道和相关实体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-687">Create new channels and related entities.</span></span></li>
<li><span data-ttu-id="2cf09-688">跟踪零售商店配置的进度。</span><span class="sxs-lookup"><span data-stu-id="2cf09-688">Track the progress of retail store configuration.</span></span></li>
<li><span data-ttu-id="2cf09-689">执行所需的步骤以完成任务，或提供信息以完成任务。</span><span class="sxs-lookup"><span data-stu-id="2cf09-689">Take the required steps to complete a task, or provide information to complete the task.</span></span></li>
<li><span data-ttu-id="2cf09-690">跟踪设备的状态，直接在商店中验证并下载 Retail Modern POS (MPOS) 程序安装。</span><span class="sxs-lookup"><span data-stu-id="2cf09-690">Track the status of devices, and directly validate and download the Retail Modern POS (MPOS) program installation in stores.</span></span></li>
<li><span data-ttu-id="2cf09-691">访问所有相关页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-691">Access all related pages.</span></span></li>
</ul><span data-ttu-id="2cf09-692">
<strong>零售商店管理</strong>工作区能让您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="2cf09-692">
<strong>Retail store management</strong> workspace lets you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2cf09-693">管理工作人员和工作人员的销售点 (POS) 权限。</span><span class="sxs-lookup"><span data-stu-id="2cf09-693">Manage workers and the workers' point of sale (POS) permissions.</span></span></li>
<li><span data-ttu-id="2cf09-694">跟踪给定商店或商店组的班次状态。</span><span class="sxs-lookup"><span data-stu-id="2cf09-694">Track shift status for a given store or group of stores.</span></span></li>
<li><span data-ttu-id="2cf09-695">在商店中直接验证和下载 MPOS 程序安装。</span><span class="sxs-lookup"><span data-stu-id="2cf09-695">Directly validate and download the MPOS program installation in stores.</span></span></li>
<li><span data-ttu-id="2cf09-696">打印报表和访问相关页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-696">Print reports and access related pages.</span></span></li>
</ul><span data-ttu-id="2cf09-697">
<strong>零售商店财务</strong>工作区能让您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="2cf09-697">
<strong>Retail store financials</strong> workspace lets you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2cf09-698">创建、计算和过帐给定渠道的报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-698">Create, calculate, and post statements for a given channel.</span></span></li>
<li><span data-ttu-id="2cf09-699">安排批处理作业以更新库存，并且计算和过帐报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-699">Schedule batch jobs to update inventory, and calculate and post statements.</span></span></li>
<li><span data-ttu-id="2cf09-700">跟踪未结报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-700">Track open statements.</span></span></li>
<li><span data-ttu-id="2cf09-701">跟踪给定商店或商店组的班次状态。</span><span class="sxs-lookup"><span data-stu-id="2cf09-701">Track shift status for a given store or group of stores.</span></span></li>
<li><span data-ttu-id="2cf09-702">打印报表和快速访问所有相关页。</span><span class="sxs-lookup"><span data-stu-id="2cf09-702">Print reports and quickly access all related pages.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-703">工作区通过让工作人员集中管理与渠道部署、商店管理和财务相关的大多数任务和操作，提高工作人员的效率和生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-703">Workspaces improve the efficiency and productivity of workers by letting them centrally manage most of their tasks and actions that are related to channel deployment, store management, and financials.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-704">管理零售 IT 运营。 </span><span class="sxs-lookup"><span data-stu-id="2cf09-704">Manage retail IT operations.</span></span></td>
<td><span data-ttu-id="2cf09-705">用户必须访问多个窗体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-705">The user must access multiple forms.</span></span></td>
<td><span data-ttu-id="2cf09-706"><strong>零售 IT</strong> 工作区针对给定渠道在单个位置启用 Commerce Data Exchange 查询，因此，您可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="2cf09-706">The <strong>Retail IT</strong> workspace enables Commerce Data Exchange inquiries in a single place for a given channel, so that you can perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2cf09-707">下载会话。</span><span class="sxs-lookup"><span data-stu-id="2cf09-707">Download sessions.</span></span></li>
<li><span data-ttu-id="2cf09-708">上载会话。</span><span class="sxs-lookup"><span data-stu-id="2cf09-708">Upload sessions.</span></span></li>
<li><span data-ttu-id="2cf09-709">跟踪失败会话，并且重新启动或运行它们。</span><span class="sxs-lookup"><span data-stu-id="2cf09-709">Track failed sessions, and re-initiate or run them again.</span></span></li>
<li><span data-ttu-id="2cf09-710">查看或运行即将发生的作业。</span><span class="sxs-lookup"><span data-stu-id="2cf09-710">View or run upcoming jobs.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-711">工作区通过让工作人员集中管理与零售 IT 运营相关的任务和操作，提高工作人员的效率和生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-711">Workspaces improve the efficiency and productivity of workers by letting them centrally manage their tasks and actions that are related to retail IT operations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-712">使用数据实体导出/导入数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-712">Import/export data by using data entities.</span></span></td>
<td><span data-ttu-id="2cf09-713">AX 2012 支持通过数据导入/导出框架迁移现成 Microsoft Dynamics 零售管理系统 (RMS)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-713">AX 2012 supports out-of-box Microsoft Dynamics Retail Management System (RMS) migration through the Data Import/Export framework.</span></span></td>
<td><span data-ttu-id="2cf09-714">零售数据实体已扩展，可支持与零售有关的所有主数据和引用数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-714">Retail data entities have been expanded to support all master and reference data that is related to retail.</span></span> <span data-ttu-id="2cf09-715">还有在整个 Dynamics AX 解决方案中对数据实体提供增强的支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-715">There is also enhanced support for data entities across the entire Dynamics AX solution.</span></span></td>
<td><span data-ttu-id="2cf09-716">数据实体允许客户执行元数据驱动的数据导入和导出。</span><span class="sxs-lookup"><span data-stu-id="2cf09-716">Data entities lets customers do metadata-driven import and export of data.</span></span> <span data-ttu-id="2cf09-717">OData 实体还允许客户将 Dynamics AX 与第三方程序集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-717">OData entities also let customers integrate Dynamics AX with third-party programs.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-718">通过使用来自 Dynamics Microsoft AX 和 POS 客户端的 BI 报表，执行智能分析。</span><span class="sxs-lookup"><span data-stu-id="2cf09-718">Perform intelligent analytics by using BI reports from Dynamics Microsoft AX and the POS client.</span></span></td>
<td><span data-ttu-id="2cf09-719">超过 25 个后端办公室报表以及 5 个渠道侧报表可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-719">More than 25 back-office reports and five channel-side reports are available.</span></span></td>
<td><span data-ttu-id="2cf09-720">超过 30 个后端办公室报表以及 10 个渠道侧报表可用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-720">More than 30 back-office reports and 10 channel-side reports are available.</span></span></td>
<td><span data-ttu-id="2cf09-721">这些报表允许客户有更多 BI 来预测趋势，发现见解和以持续绩效高峰运营。</span><span class="sxs-lookup"><span data-stu-id="2cf09-721">These reports let customers have more BI to predict trends, uncover insights, and operate at continual peak performance.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-722">通过使用“监控 Retail Channel performance”Power BI 内容来分析零售渠道销售数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-722">Analyze retail channel sales data by using the "Monitor Retail Channel performance" Power BI content.</span></span></td>
<td><span data-ttu-id="2cf09-723">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-723">Not available</span></span></td>
<td><span data-ttu-id="2cf09-724">在 PowerBI.com 上，选择<strong>获取数据</strong>，然后选择 <strong>Dynamics AX – 零售渠道绩效</strong>内容包。</span><span class="sxs-lookup"><span data-stu-id="2cf09-724">On PowerBI.com, select <strong>Get Data</strong>, and then select the <strong>Dynamics AX – Retail Channel performance</strong> content pack.</span></span> <span data-ttu-id="2cf09-725">输入您的 Dynamics AX 终结点的 URL 以查看反映在仪表板中的数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-725">Enter the URL for your Dynamics AX endpoint to see your data reflected in the dashboard.</span></span></td>
<td><span data-ttu-id="2cf09-726">通过三到四次单击，组织可以部署一个包含重要财务数据的 Power BI 仪表板。</span><span class="sxs-lookup"><span data-stu-id="2cf09-726">In three to four clicks, organizations can deploy a Power BI dashboard that contains important financial data.</span></span> <span data-ttu-id="2cf09-727">内容可由组织个性化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-727">Content can be personalized by the organization.</span></span> <span data-ttu-id="2cf09-728">此外，用户可以将 Power BI 仪表板磁贴嵌入到其在 Dynamics AX 中的个性化工作区，因此，用户随后可以快速查看分析信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-728">Additionally, users can embed Power BI dashboard tiles into their personalized workspaces in Dynamics AX, so that they can then see analytical information at a glance.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-729">配置用户权限。</span><span class="sxs-lookup"><span data-stu-id="2cf09-729">Configure consumer permissions.</span></span></td>
<td><span data-ttu-id="2cf09-730">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-730">Not available</span></span></td>
<td><span data-ttu-id="2cf09-731">客户可以选择 POS 操作是否可用于客户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-731">Customers can choose whether POS operations can be available to consumers.</span></span> <span data-ttu-id="2cf09-732">Retail Server 使用权限来进行应用程序编程接口 (API) 调用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-732">Retail Server uses permissions for application programming interface (API) calls.</span></span></td>
<td><span data-ttu-id="2cf09-733">它能让用户配置用户级权限。</span><span class="sxs-lookup"><span data-stu-id="2cf09-733">It provides the ability to configure consumer-level permissions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-734">管理和验证实体配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-734">Manage and validate entity configurations.</span></span></td>
<td><span data-ttu-id="2cf09-735">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-735">Not available</span></span></td>
<td><span data-ttu-id="2cf09-736">配置管理器和验证器功能启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-736">The configuration manager and validator feature enables the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-737">批量配置数据上载</span><span class="sxs-lookup"><span data-stu-id="2cf09-737">Bulk configuration data upload</span></span></li>
<li><span data-ttu-id="2cf09-738">业务实体验证</span><span class="sxs-lookup"><span data-stu-id="2cf09-738">Business entity validation</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-739">它能让用户引导配置，以及验证配置的状态和各种配置元素的完整性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-739">It provides the ability to bootstrap the configuration, and to validate the status and completeness of the configuration for the various configuration elements.</span></span></td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a><span data-ttu-id="2cf09-740">Retail 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="2cf09-740">Retail Hardware Station</span></span>

| <span data-ttu-id="2cf09-741">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-741">What can you do?</span></span> | <span data-ttu-id="2cf09-742">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-742">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-743">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-743">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-744">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-744">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-745">使 POS 设备能连接到外围设备，例如打印机、银箱或付款设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-745">Enable POS devices to connect to peripherals such as printers, cash drawers, or payment devices.</span></span> | <span data-ttu-id="2cf09-746">MPOS 硬件配置文件用于指定要使用的设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-746">The MPOS hardware profile is used to specify the devices that are used.</span></span> | <span data-ttu-id="2cf09-747">一个添加的硬件配置文件支持更多不同硬件，从一个工作站到下一个工作站。</span><span class="sxs-lookup"><span data-stu-id="2cf09-747">An added hardware profile supports more diverse hardware from one station to the next.</span></span> <span data-ttu-id="2cf09-748">在处理电子资金转帐 (EFT) 交易记录时，新的硬件工作站配置文件对每个硬件工作站都支持一个唯一的终端 ID。</span><span class="sxs-lookup"><span data-stu-id="2cf09-748">A new Hardware Station profile supports a unique terminal ID for each Hardware Station when electronic funds transfer (EFT) transactions are processed.</span></span> <span data-ttu-id="2cf09-749">EFT 支持已合并到硬件工作站，以减少 EFT 付款处理中 MPOS 的涉及。</span><span class="sxs-lookup"><span data-stu-id="2cf09-749">EFT support has been merged into hardware station to reduce the involvement of MPOS in EFT payment processing.</span></span> | <span data-ttu-id="2cf09-750">它为实现提供更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-750">It provides greater flexibility for implementations.</span></span> <span data-ttu-id="2cf09-751">它还提供增强的安全性和减少的信用卡数据暴露。</span><span class="sxs-lookup"><span data-stu-id="2cf09-751">It also provides enhanced security and reduced exposure to credit card data.</span></span> |

### <a name="retail-server-and-data-management"></a><span data-ttu-id="2cf09-752">Retail Server 和数据管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-752">Retail Server and data management</span></span>

<span data-ttu-id="2cf09-753">Retail Server 和数据管理允许客户和企业跨在线、商店内和呼叫中心渠道创建 omni 渠道购物体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-753">Retail Server and data management lets consumers and enterprises create an omni-channel shopping experience across online, in-store, and call center channels.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-754">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-754">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-755">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-755">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-756">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-756">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-757">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-757">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-758">连接到 Commerce Runtime (CRT) 数据库，其中使用 CRT 服务存储渠道的业务数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-758">Connect to a commerce runtime (CRT) database that stores business data for the channel by using CRT services.</span></span></td>
<td><span data-ttu-id="2cf09-759">支持 OData V3。</span><span class="sxs-lookup"><span data-stu-id="2cf09-759">OData V3 is supported.</span></span></td>
<td><span data-ttu-id="2cf09-760">支持 OData V4。</span><span class="sxs-lookup"><span data-stu-id="2cf09-760">OData V4 is supported.</span></span></td>
<td><span data-ttu-id="2cf09-761">它帮助客户紧跟 OData 条件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-761">It helps the customer stay current with OData standards.</span></span> <span data-ttu-id="2cf09-762">它还通过跨商店内、移动和在线渠道集成销售，创建可靠的 omni 渠道体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-762">It also creates a robust omni-channel experience by integrating sales across in-store, mobile, and online channels.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-763">支持零售服务作为可托管服务组。</span><span class="sxs-lookup"><span data-stu-id="2cf09-763">Support Retail services as a hostable set of services.</span></span></td>
<td><span data-ttu-id="2cf09-764">电子商务 API 不通过 Retail Server 受支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-764">The E-commerce API isn't supported through Retail Server.</span></span></td>
<td><span data-ttu-id="2cf09-765">电子商务 API 现在通过 Retail Server 可用，用以支持联机方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-765">The E-commerce API is now available through Retail Server to support online scenarios.</span></span></td>
<td><span data-ttu-id="2cf09-766">它提供承载的且可扩展的电子商务服务，可以和第三方联机商店一起使用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-766">It provides hosted and scalable e-commerce services that can be used with third-party online stores.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-767">通过使用 Commerce Data Exchange，在 Microsoft Dynamics AX 后端办公室和渠道之间移动数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-767">Move data between the Microsoft Dynamics AX back office and channels by using Commerce Data Exchange.</span></span></td>
<td><span data-ttu-id="2cf09-768">Commerce Data Exchange 是一种在 Microsoft Dynamics AX 和零售渠道（例如，在线商店或实体商店）之间传送数据的系统。</span><span class="sxs-lookup"><span data-stu-id="2cf09-768">Commerce Data Exchange is a system that transfers data between Microsoft Dynamics AX and retail channels, such as online stores or brick-and-mortar stores.</span></span> <span data-ttu-id="2cf09-769">有关详细信息，请参阅<a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>。</span><span class="sxs-lookup"><span data-stu-id="2cf09-769">For more information, see <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</span></span></td>
<td><span data-ttu-id="2cf09-770">与 Microsoft Dynamics AX 2012 CU8 之间有功能对等性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-770">There is functional parity with Microsoft Dynamics AX 2012 CU8.</span></span> <span data-ttu-id="2cf09-771">不过，请注意以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="2cf09-771">However, note the following details:</span></span>
<ul>
<li><span data-ttu-id="2cf09-772">Commerce Data Exchange 针对云重新进行了设计。</span><span class="sxs-lookup"><span data-stu-id="2cf09-772">Commerce Data Exchange has been re-engineered for the cloud.</span></span></li>
<li><span data-ttu-id="2cf09-773">异步服务使用直接数据库访问权限来访问渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="2cf09-773">Async service uses direct database access to the channel database.</span></span></li>
<li><span data-ttu-id="2cf09-774">Commerce Data Exchange：实时服务是作为 Microsoft Dynamics AX 自定义服务承载的。</span><span class="sxs-lookup"><span data-stu-id="2cf09-774">Commerce Data Exchange: Real-time Service is hosted as a Microsoft Dynamics AX custom service.</span></span></li>
<li><span data-ttu-id="2cf09-775">MPOS 管理脱机数据库和 Retail Server 之间的同步。</span><span class="sxs-lookup"><span data-stu-id="2cf09-775">MPOS manages synchronization between offline databases and Retail Server.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-776">Commerce Data Exchange 针对云平台重新进行了设计。</span><span class="sxs-lookup"><span data-stu-id="2cf09-776">Commerce Data Exchange has been re-engineered for the cloud platform.</span></span> <span data-ttu-id="2cf09-777">它继续管理 Microsoft Dynamics AX 和零售渠道（例如，在线商店或实体商店）之间的数据传送。</span><span class="sxs-lookup"><span data-stu-id="2cf09-777">It continues to manage the transfer of data between Microsoft Dynamics AX and retail channels, such as online stores or brick-and-mortar stores.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-778">通过使用付款 SDK，支持即插即用、半集成的跨渠道付款处理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-778">Support plug and play, semi-integrated cross-channel payment processing by using the payment SDK.</span></span></td>
<td><span data-ttu-id="2cf09-779">AX 2012 提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-779">AX 2012 provides the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-780">支持所有通道：POS、电子商务和呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="2cf09-780">Support for all channels: POS, e-commerce, and call center.</span></span></li>
<li><span data-ttu-id="2cf09-781">支持卡存在和卡不存在。</span><span class="sxs-lookup"><span data-stu-id="2cf09-781">Support for card present and card not present.</span></span></li>
<li><span data-ttu-id="2cf09-782">接受付款的页面。</span><span class="sxs-lookup"><span data-stu-id="2cf09-782">Page for accepting payment.</span></span></li>
<li><span data-ttu-id="2cf09-783">作为 Retail SDK 中的示例代码对 LS5300 和 MX925 提供外围支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-783">Peripheral support for LS5300 and MX925 as sample code in the Retail SDK.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-784">Dynamics AX 的当前版本支持所有现有 Microsoft Dynamics AX for Retail 2012 信用卡/借记卡功能和四种新的改进。</span><span class="sxs-lookup"><span data-stu-id="2cf09-784">The current version of Dynamics AX supports all existing Microsoft Dynamics AX for Retail 2012 credit/debit card features and four new enhancements.</span></span></td>
<td><span data-ttu-id="2cf09-785">它允许客户处理付款的信用卡/借记卡交易记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-785">It lets the customer process credit/debit card transactions for payments.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-786">通过使用 Microsoft 帐户 (Microsoft Azure Active Directory (Azure AD)) 启用设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-786">Activate devices by using a Microsoft account (Microsoft Azure Active Directory (Azure AD)).</span></span></td>
<td><span data-ttu-id="2cf09-787">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-787">Not available</span></span></td>
<td><span data-ttu-id="2cf09-788">提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-788">The following functionality is provided:</span></span>
<ul>
<li><span data-ttu-id="2cf09-789">针对云环境通过基于 Azure AD 的激活增强了安全性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-789">Enhanced security by Azure AD-based activation for the cloud.</span></span></li>
<li><span data-ttu-id="2cf09-790">针对令牌管理增强了安全性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-790">Enhanced security for token management.</span></span></li>
<li><span data-ttu-id="2cf09-791">改进了激活过程中的可靠性、故障排除和错误消息传送</span><span class="sxs-lookup"><span data-stu-id="2cf09-791">Improved reliability, troubleshooting, and error messaging during activation</span></span></li>
<li><span data-ttu-id="2cf09-792">简化了与激活有关的 IT 管理任务。</span><span class="sxs-lookup"><span data-stu-id="2cf09-792">Simplified IT administration tasks that are related to activation.</span></span></li>
<li><span data-ttu-id="2cf09-793">重新访了威胁模型并修复了安全问题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-793">Revisited threat model and fixed security issues.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-794">它提供了以下优点：</span><span class="sxs-lookup"><span data-stu-id="2cf09-794">It provides the following benefits:</span></span>
<ul>
<li><span data-ttu-id="2cf09-795">通过 Azure AD 和设备令牌/ID（使用令牌的 RS 调用，用户特定的应用程序存储）增强了安全性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-795">Security is enhanced through Azure AD and device token/ID (RS calls that use a token, user-specific app storage).</span></span></li>
<li><span data-ttu-id="2cf09-796">该停止对 MPOS（传统设备）的未授权远程使用。</span><span class="sxs-lookup"><span data-stu-id="2cf09-796">It stops unauthorized remote use of MPOS (brick device).</span></span></li>
<li><span data-ttu-id="2cf09-797">它出于 PCI 符合性目的跟踪 MPOS 设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-797">It tracks MPOS devices for PCI-compliance purposes.</span></span></li>
<li><span data-ttu-id="2cf09-798">它使用设备令牌映射具有企业实体的物理设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-798">It maps physical devices with a business entity (register) by using a device token.</span></span></li>
<li><span data-ttu-id="2cf09-799">它初始化顺畅 MPOS 功能的设置（编号规则和硬件配置文件），作为 MPOS 的第一个接触点。</span><span class="sxs-lookup"><span data-stu-id="2cf09-799">It initializes settings for smooth MPOS functionality (number sequences and hardware profiles) as the first touch point of MPOS.</span></span></li>
<li><span data-ttu-id="2cf09-800">它报告来自总部的设备信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-800">It reports device information from headquarters.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-801">通过媒体库管理富媒体内容的编写和服务。</span><span class="sxs-lookup"><span data-stu-id="2cf09-801">Manage rich media content for authoring and serving through Media Gallery.</span></span></td>
<td><span data-ttu-id="2cf09-802">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-802">Not available</span></span></td>
<td><ul>
<li><span data-ttu-id="2cf09-803">支持图像上载，并且可以针对外部承载的和 Retail 承载的图像在媒体库中进行查看、管理和删除。</span><span class="sxs-lookup"><span data-stu-id="2cf09-803">Support image upload, and also view, manage, and delete, from Media Gallery for both externally-hosted and Retail-hosted images.</span></span></li>
<li><span data-ttu-id="2cf09-804">通过链接库中的图像和从桌面上载图像，支持从实体页（<strong>产品</strong>、<strong>目录</strong>等）上载和查看图像。</span><span class="sxs-lookup"><span data-stu-id="2cf09-804">Support image upload and view from entity pages (<strong>Products</strong>, <strong>Catalogs</strong>, and so on) by linking an image from the gallery and uploading an image from the desktop.</span></span></li>
<li><span data-ttu-id="2cf09-805">优化图像以达到缩略图、自定义大小和原始效果。</span><span class="sxs-lookup"><span data-stu-id="2cf09-805">Optimize the images for thumbnail, custom size, and original.</span></span></li>
<li><span data-ttu-id="2cf09-806">通过对批量关联使用模板和后台作业，批量链接实体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-806">Bulk link entities by using a template and background jobs for bulk association.</span></span></li>
<li><span data-ttu-id="2cf09-807">Microsoft Excel 集成覆盖命名约定和预定义路径的属性组限制。</span><span class="sxs-lookup"><span data-stu-id="2cf09-807">Microsoft Excel integration overwrites the attribute group limitation of naming conventions and predefined paths.</span></span></li>
<li><span data-ttu-id="2cf09-808">支持将脱机图像和安全图像用于个人可识别信息 (PII) 内容，例如 Retail 承载的员工和客户图像。</span><span class="sxs-lookup"><span data-stu-id="2cf09-808">Support offline images and secure images for personally identifiable information (PII) content, such as Retail-hosted employee and customer images.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2cf09-809">它解决围绕外部承载的图像的痛点，因此，您可以避免反复执行某些步骤，并且可以在单个位置进行管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-809">It addresses pain points around externally-hosted images, so that you can avoid going back and forth, and instead manage in a single place.</span></span></li>
<li><span data-ttu-id="2cf09-810">它通过媒体库为上载的和外部承载的图像提供强大的内容管理，并且提供筛选以帮助您查找图像。</span><span class="sxs-lookup"><span data-stu-id="2cf09-810">It provides powerful content management through Media Gallery for uploaded and externally-hosted images, and also provides filtering to help you find images.</span></span></li>
<li><span data-ttu-id="2cf09-811">它能让您轻松地在外部承载的图像和实体（例如产品和类别）之间创建批量关联。</span><span class="sxs-lookup"><span data-stu-id="2cf09-811">It lets you easily create bulk associations between externally-hosted images and entities such as products and catalogs.</span></span></li>
<li><span data-ttu-id="2cf09-812">它为图像支持 Retail 承载的存储，为简易更新支持 Excel 集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-812">It supports Retail-hosted storage for images, and Excel integration for easy updates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a><span data-ttu-id="2cf09-813">富客户体验</span><span class="sxs-lookup"><span data-stu-id="2cf09-813">Rich clientele experience</span></span>

<span data-ttu-id="2cf09-814">Retail 随时随地在任何设备上提供沉浸式移动体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-814">Retail offers immersive mobile experiences anywhere, any time, and on any device.</span></span> <span data-ttu-id="2cf09-815">此功能在所有通道中启用增强的购物和商店体验。</span><span class="sxs-lookup"><span data-stu-id="2cf09-815">This functionality enables enhanced shopping and store experiences across all channels.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-816">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-816">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-817">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-817">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-818">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-818">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-819">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-819">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-820">通过使用一个直观、触摸友好、丰富的沉浸式用户体验，来搜索、浏览、查找或扫描产品、将产品添加到购物车、接受付款，以及签出。</span><span class="sxs-lookup"><span data-stu-id="2cf09-820">Search, browse, look up, or scan products, add products to a cart, accept payment, and check out by using an intuitive, touch-friendly, rich and immersive user experience on MPOS.</span></span></td>
<td><span data-ttu-id="2cf09-821">AX 2012 启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-821">AX 2012 enables the following features:</span></span>
<ul>
<li><span data-ttu-id="2cf09-822">执行销售、退货和取消。</span><span class="sxs-lookup"><span data-stu-id="2cf09-822">Perform sales, returns, and voids.</span></span></li>
<li><span data-ttu-id="2cf09-823">创建、修改和领取客户订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-823">Create, modify, and pick up customer orders.</span></span></li>
<li><span data-ttu-id="2cf09-824">执行班次和银箱操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-824">Perform shift and drawer operations.</span></span></li>
<li><span data-ttu-id="2cf09-825">领取和接收订单，以及执行存货盘点。</span><span class="sxs-lookup"><span data-stu-id="2cf09-825">Pick and receive orders, and perform stock counts.</span></span></li>
<li><span data-ttu-id="2cf09-826">查看商店内报表。</span><span class="sxs-lookup"><span data-stu-id="2cf09-826">View in-store reports.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-827">提供与 AX 2012 MPOS 之间的功能对等性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-827">Functional parity with AX 2012 MPOS is provided.</span></span> <span data-ttu-id="2cf09-828">这包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-828">This includes the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-829">跨商店/渠道进行客户查找。</span><span class="sxs-lookup"><span data-stu-id="2cf09-829">Customer lookup across stores/channels.</span></span></li>
<li><span data-ttu-id="2cf09-830">能够创建客户订单，而无需访问实时服务。</span><span class="sxs-lookup"><span data-stu-id="2cf09-830">The ability to create customer orders without accessing Real-time Service.</span></span></li>
<li><span data-ttu-id="2cf09-831">改进了设备激活工作流、状态和错误消息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-831">Improved device activation workflows, status, and error messages.</span></span></li>
<li><span data-ttu-id="2cf09-832">进行了延伸性改进（例如过帐前触发和活动支持）以改进自定义。</span><span class="sxs-lookup"><span data-stu-id="2cf09-832">Extensibility improvements, such as pre-post triggers and activity support to improve customization.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-833">销售人员可以通过在商店中的任何位置使用移动设备，来处理销售交易记录和客户订单，并执行日常运营和库存管理。</span><span class="sxs-lookup"><span data-stu-id="2cf09-833">Sales staff can process sales transactions and customer orders, and perform daily operations and inventory management, by using mobile devices anywhere in the store.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-834">通过 Cloud POS 将 POS 作为 Web 应用程序启动。</span><span class="sxs-lookup"><span data-stu-id="2cf09-834">Start POS as a web app via Cloud POS.</span></span></td>
<td><span data-ttu-id="2cf09-835">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-835">Not available</span></span></td>
<td><span data-ttu-id="2cf09-836">提供与 MPOS 之间的功能对等性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-836">Functional parity with MPOS is provided.</span></span> <span data-ttu-id="2cf09-837">这包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-837">This includes the following functionality:</span></span>
<ul>
<li><span data-ttu-id="2cf09-838">通过使用 AAD 进行设备激活</span><span class="sxs-lookup"><span data-stu-id="2cf09-838">Device activation by using AAD</span></span></li>
<li><span data-ttu-id="2cf09-839">响应性强的布局设计</span><span class="sxs-lookup"><span data-stu-id="2cf09-839">Responsive layout design</span></span></li>
<li><span data-ttu-id="2cf09-840">支持 Edge、Internet Explorer 和 Chrome 浏览器。</span><span class="sxs-lookup"><span data-stu-id="2cf09-840">Support for Edge, Internet Explorer and Chrome browsers.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-841">它提供了一个 Web 应用程序 POS，其具有与 MPOS 兼容的功能，并且可以在多个平台和 Web 浏览器中使用而没有配置成本。</span><span class="sxs-lookup"><span data-stu-id="2cf09-841">It provides a web app POS that has functionality that is compatible with MPOS, and that can be used across platforms and browsers at no deployment cost.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-842">与内容管理系统集成，以创建 omni 渠道电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="2cf09-842">Integrate with content management systems to create an omni-channel e-Commerce website.</span></span></td>
<td><span data-ttu-id="2cf09-843">支持 Microsoft SharePoint 和第三方店面。</span><span class="sxs-lookup"><span data-stu-id="2cf09-843">Microsoft SharePoint and third-party storefronts are supported.</span></span></td>
<td><span data-ttu-id="2cf09-844">提供一个电子商务平台，以支持第三方店面。</span><span class="sxs-lookup"><span data-stu-id="2cf09-844">An e-Commerce platform is provided that supports third-party storefronts.</span></span> <span data-ttu-id="2cf09-845">该平台包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-845">The platform includes the following features:</span></span>
<ul>
<li><span data-ttu-id="2cf09-846">一个丰富的用户 API。</span><span class="sxs-lookup"><span data-stu-id="2cf09-846">A rich consumer API.</span></span></li>
<li><span data-ttu-id="2cf09-847">面向任何第三方开放式 ID 提供商的身份验证集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-847">Authentication integration to any third-party open ID providers.</span></span></li>
<li><span data-ttu-id="2cf09-848">付款集成。</span><span class="sxs-lookup"><span data-stu-id="2cf09-848">Payment integration.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-849">客户现在可灵活地使用其选择的内容管理系统。</span><span class="sxs-lookup"><span data-stu-id="2cf09-849">Customers now have the flexibility to use the content management system of their choice.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-850">通过邮件订单目录来瞄准客户，并通过快速订单条目、协助销售和使用呼叫中心的履行来简化操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-850">Target customers via mail order catalogs, and streamline operations through fast order entry, assisted sales, and fulfillment by using Call Center.</span></span></td>
<td><ul>
<li><span data-ttu-id="2cf09-851">呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="2cf09-851">Call Center channel</span></span></li>
<li><span data-ttu-id="2cf09-852">邮件订单目录</span><span class="sxs-lookup"><span data-stu-id="2cf09-852">Mail order catalogs</span></span></li>
<li><span data-ttu-id="2cf09-853">快速订单条目和协助销售</span><span class="sxs-lookup"><span data-stu-id="2cf09-853">Fast order entry and assisted sale</span></span></li>
<li><span data-ttu-id="2cf09-854">改进的订单履行</span><span class="sxs-lookup"><span data-stu-id="2cf09-854">Enhanced order fulfillment</span></span></li>
<li><span data-ttu-id="2cf09-855">客户服务</span><span class="sxs-lookup"><span data-stu-id="2cf09-855">Customer service</span></span></li>
<li><span data-ttu-id="2cf09-856">集成的定价和促销/折扣</span><span class="sxs-lookup"><span data-stu-id="2cf09-856">Integrated pricing and promotions/discounts</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-857">提供与 AX 2012 呼叫中心之间的功能对等性，但价格覆盖除外。</span><span class="sxs-lookup"><span data-stu-id="2cf09-857">Feature parity with the AX 2012 Call Center solution is available, with the exception of price overrides.</span></span></td>
<td><span data-ttu-id="2cf09-858">呼叫中心是一种类型的零售渠道，它能让工作人员通过电话接受来自客户的订单和创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-858">Call centers are a type of retail channel that lets workers take orders from customers over the phone and create sales orders.</span></span></td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a><span data-ttu-id="2cf09-859">商业要素</span><span class="sxs-lookup"><span data-stu-id="2cf09-859">Commerce essentials</span></span>

<span data-ttu-id="2cf09-860">侧重于零售和商务的配置选项可帮助简化特定于零售的配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-860">A retail and commerce-focused configuration option helps streamline retail-specific deployments.</span></span>

| <span data-ttu-id="2cf09-861">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-861">What can you do?</span></span> | <span data-ttu-id="2cf09-862">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-862">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-863">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-863">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-864">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-864">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-865">使用商业要素仪表板。</span><span class="sxs-lookup"><span data-stu-id="2cf09-865">Use the Commerce essentials dashboard.</span></span> | <span data-ttu-id="2cf09-866">提供一个区域页，其带有指向菜单项的链接。</span><span class="sxs-lookup"><span data-stu-id="2cf09-866">An area page with links to menu items is available.</span></span> | <span data-ttu-id="2cf09-867">商业要素仪表板提供指向常用任务的链接，包括指向工作区、Power BI Web 控件、收藏夹、最近查看页面和当前工作项的链接。</span><span class="sxs-lookup"><span data-stu-id="2cf09-867">The Commerce essentials dashboard provides links to frequent tasks, including links to workspaces, the Power BI web control, favorites, recent pages, and current work items.</span></span> | <span data-ttu-id="2cf09-868">增强的仪表板能让工作人员提高效率并提供一个灵活的起点以适用于任何特定于零售的任务。</span><span class="sxs-lookup"><span data-stu-id="2cf09-868">The enhanced dashboard empowers workers by making them more efficient and providing a flexible starting point for any retail-specific task.</span></span> |
| <span data-ttu-id="2cf09-869">使用数据实体访问帐户更改。</span><span class="sxs-lookup"><span data-stu-id="2cf09-869">Use data entities to access account changes.</span></span> | <span data-ttu-id="2cf09-870">帐户更改导出到文件系统上的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="2cf09-870">Account changes are exported to a folder on the file system.</span></span> | <span data-ttu-id="2cf09-871">帐户更改可通过数据实体获得。</span><span class="sxs-lookup"><span data-stu-id="2cf09-871">Account changes are accessible through data entities.</span></span> | <span data-ttu-id="2cf09-872">在不同系统之间移动数据时，此功能提供更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-872">This feature provides greater flexibility when moving data between disparate systems.</span></span> <span data-ttu-id="2cf09-873">此功能还可通过 OData 应用程序增强。</span><span class="sxs-lookup"><span data-stu-id="2cf09-873">This feature can be enhanced through OData applications, as well.</span></span> |
| <span data-ttu-id="2cf09-874">使用 Cloud POS 和 MPOS。</span><span class="sxs-lookup"><span data-stu-id="2cf09-874">Use Cloud POS and MPOS.</span></span> | <span data-ttu-id="2cf09-875">只支持现成的 Enterprise POS (EPOS)。</span><span class="sxs-lookup"><span data-stu-id="2cf09-875">Only Enterprise POS (EPOS) is supported out-of-the-box.</span></span> | <span data-ttu-id="2cf09-876">MPOS 和 Cloud POS 替换 EPOS 客户端。</span><span class="sxs-lookup"><span data-stu-id="2cf09-876">MPOS and Cloud POS replace the EPOS client.</span></span> <span data-ttu-id="2cf09-877">默认情况下，电子商务渠道也将添加到商业要素。</span><span class="sxs-lookup"><span data-stu-id="2cf09-877">The e-Commerce channel has also been added to Commerce essentials by default.</span></span> | <span data-ttu-id="2cf09-878">此功能通过可迅速部署的销售终端客户端启用更好的现成渠道支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-878">This feature enables greater out-of-box channel support with rapidly deployable point-of-sale clients.</span></span> |
| <span data-ttu-id="2cf09-879">实施和维护两层体系结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-879">Implement and maintain two-tier architecture.</span></span> | <span data-ttu-id="2cf09-880">数据导出/导入框架能让您在 AX 2012 和第三方系统之间移动数据。</span><span class="sxs-lookup"><span data-stu-id="2cf09-880">The Data import/export framework provides the ability to move data between AX 2012 and third-party systems.</span></span> | <span data-ttu-id="2cf09-881">创建了数据实体可提高对两层体系结构的支持。</span><span class="sxs-lookup"><span data-stu-id="2cf09-881">Data entities created to enhance support for two-tier architecture.</span></span> | <span data-ttu-id="2cf09-882">数据实体和 OData 应用程序提供一个抽象层，使两层方案更易于实施和维护。</span><span class="sxs-lookup"><span data-stu-id="2cf09-882">Data entities and OData applications provide an abstraction layer to make two-tier scenarios easier to implement and maintain.</span></span> |
| <span data-ttu-id="2cf09-883">简化窗体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-883">Simplify forms.</span></span> | <span data-ttu-id="2cf09-884">需要自定义代码，用以简化 UI。</span><span class="sxs-lookup"><span data-stu-id="2cf09-884">Custom code is required to simplify the UI.</span></span> | <span data-ttu-id="2cf09-885">窗体和菜单扩展提供标准化的 UI 简化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-885">Form and menu extensions provide standardized UI simplification.</span></span> | <span data-ttu-id="2cf09-886">此功能提供更方便快捷的方式来基于零售商的需要优化窗体。</span><span class="sxs-lookup"><span data-stu-id="2cf09-886">This feature provides a faster and easier way to fine-tune forms based on retailer's needs.</span></span> |

### <a name="pos-task-recorder"></a><span data-ttu-id="2cf09-887">POS 任务录制器</span><span class="sxs-lookup"><span data-stu-id="2cf09-887">POS Task recorder</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-888">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-888">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-889">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-889">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-890">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-890">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-891">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-891">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-892">为 Modern POS 创建和共享任务指南和文档。</span><span class="sxs-lookup"><span data-stu-id="2cf09-892">Create and share task guides and documents for Modern POS.</span></span></td>
<td><span data-ttu-id="2cf09-893">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-893">Not available</span></span></td>
<td><span data-ttu-id="2cf09-894">MPOS 任务录制器支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-894">The MPOS Task recorder supports the following features:</span></span>
<ul>
<li><span data-ttu-id="2cf09-895">为在 MPOS 中执行的多种任务创建任务记录。</span><span class="sxs-lookup"><span data-stu-id="2cf09-895">Create task recordings for various tasks that are performed in MPOS.</span></span></li>
<li><span data-ttu-id="2cf09-896">生成一个文档，其中包含步骤和屏幕快照，并将该文档与业务流程模型中的节点关联。</span><span class="sxs-lookup"><span data-stu-id="2cf09-896">Generate a document that includes steps and screenshots, and associate it with a node in the business process model.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-897">合作伙伴和独立软件供应商 (ISV) 可以自定义 MPOS 并提供支持文档以培训其用户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-897">Partners and independent software vendors (ISVs) can customize MPOS and provide supporting documents to train their users.</span></span></td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a><span data-ttu-id="2cf09-898">可扩展性</span><span class="sxs-lookup"><span data-stu-id="2cf09-898">Extensibility</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-899">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-899">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-900">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-900">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-901">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-901">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-902">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-902">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-903">跨 HQ、呼叫中心、电子商务和 POS 支持可扩展的且可轻松部署的 Retail 组件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-903">Support an extensible and easily deployable Retail components across HQ, Call Center, e-Commerce, and the POS.</span></span></td>
<td><span data-ttu-id="2cf09-904">可使用 Retail SDK 扩展组件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-904">The components can be extended by using the Retail SDK.</span></span> <span data-ttu-id="2cf09-905">不支持包装和部署功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-905">No packaging and deployment capabilities are supported.</span></span></td>
<td><span data-ttu-id="2cf09-906">跨各种组件对可扩展性挂接进行了改进，从而更好地支持代码隔离和可用性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-906">Extensibility hooks are improved across the various components to better support code isolation and serviceability.</span></span> <span data-ttu-id="2cf09-907">下面是包括的某些功能：</span><span class="sxs-lookup"><span data-stu-id="2cf09-907">Here are some of the features that are included:</span></span>
<ul>
<li><span data-ttu-id="2cf09-908">工作流、活动和操作。</span><span class="sxs-lookup"><span data-stu-id="2cf09-908">Workflow, activity, and operation.</span></span></li>
<li><span data-ttu-id="2cf09-909">能让您轻松扩展工作流的前触发器和后触发器。</span><span class="sxs-lookup"><span data-stu-id="2cf09-909">Pre-triggers and post-triggers that let you easily extend a workflow.</span></span></li>
<li><span data-ttu-id="2cf09-910">应用程序和操作触发器。</span><span class="sxs-lookup"><span data-stu-id="2cf09-910">Application and operation triggers.</span></span></li>
</ul>
<span data-ttu-id="2cf09-911">此外，还提供一个框架，能让您通过使用 MSBuild 来创建和包装这些组件，然后通过 Microsoft Dynamics Lifecycle Services (LCS) 无缝部署您的自定义项。</span><span class="sxs-lookup"><span data-stu-id="2cf09-911">Additionally, a framework is available that lets you build and package these components by using MSBuild, and then seamlessly deploy your customization through Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="2cf09-912">基于运营的垂直市场和地理位置，零售商有非常具体的要求。</span><span class="sxs-lookup"><span data-stu-id="2cf09-912">Retailers have very specific requirements based on verticals and geographies of operation.</span></span> <span data-ttu-id="2cf09-913">通过提供易于扩展的平台，我们跨多个垂直市场提供可用性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-913">By providing an easily extensible platform, we enable usage across verticals and markets.</span></span> <span data-ttu-id="2cf09-914">由于 Retail 还具有非常分散的体系结构，因此无缝部署的能力会极大提高生产率。</span><span class="sxs-lookup"><span data-stu-id="2cf09-914">Because Retail also has a very distributed architecture, the ability to seamlessly deploy greatly improves productivity.</span></span></td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a><span data-ttu-id="2cf09-915">生命周期管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-915">Lifecycle management</span></span>

<span data-ttu-id="2cf09-916">Lifecycle Services (LCS) 提供一系列服务，可供客户和合作伙伴用来管理系统的生命周期，从注册到日常运营。</span><span class="sxs-lookup"><span data-stu-id="2cf09-916">Lifecycle Services (LCS) provides a set of services that customers and partners can use to manage the lifecycle of the system from sign-up to daily operations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-917">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-917">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-918">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-918">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-919">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-919">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-920">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-920">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-921">通过云部署服务来管理程序。</span><span class="sxs-lookup"><span data-stu-id="2cf09-921">Manage the program via cloud deployment services.</span></span></td>
<td><span data-ttu-id="2cf09-922">不可用</span><span class="sxs-lookup"><span data-stu-id="2cf09-922">Not available</span></span></td>
<td><span data-ttu-id="2cf09-923">以下拓扑结构可以部署到云中：</span><span class="sxs-lookup"><span data-stu-id="2cf09-923">The following topologies can be deployed to the cloud:</span></span>
<ul>
<li><span data-ttu-id="2cf09-924">Retail 一盒试用拓扑。</span><span class="sxs-lookup"><span data-stu-id="2cf09-924">Retail one-box trial topology.</span></span></li>
<li><span data-ttu-id="2cf09-925">Retail 多盒高可用性拓扑结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-925">Retail multi-box high-availability topology.</span></span></li>
<li><span data-ttu-id="2cf09-926">采用 Retail SDK 的开发人员拓扑结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-926">Developer topology with the Retail SDK.</span></span></li>
</ul>
<span data-ttu-id="2cf09-927">通过自助服务安装可获得改进的“低触摸”客户端组件安装：</span><span class="sxs-lookup"><span data-stu-id="2cf09-927">There is an improved "low-touch" client component installation via self-service installation:</span></span>
<ul>
<li><span data-ttu-id="2cf09-928">Retail Modern POS。</span><span class="sxs-lookup"><span data-stu-id="2cf09-928">Retail Modern POS.</span></span></li>
<li><span data-ttu-id="2cf09-929">Retail Hardware Station。</span><span class="sxs-lookup"><span data-stu-id="2cf09-929">Retail Hardware Station.</span></span></li>
<li><span data-ttu-id="2cf09-930">通过自助服务安装支持自定义包的上载和分配。</span><span class="sxs-lookup"><span data-stu-id="2cf09-930">Support for the upload and distribution of customized packages through self-service installation.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-931">云部署服务提供以下优点：</span><span class="sxs-lookup"><span data-stu-id="2cf09-931">The cloud deployment services provide the following benefits:</span></span>
<ul>
<li><span data-ttu-id="2cf09-932">显著减少了部署工作量和 Retail HQ 组件的复杂性。</span><span class="sxs-lookup"><span data-stu-id="2cf09-932">Significantly reduced deployment effort and complexity for Retail HQ components.</span></span></li>
<li><span data-ttu-id="2cf09-933">本地部署到 Microsoft Azure 公有云。</span><span class="sxs-lookup"><span data-stu-id="2cf09-933">Native deployment to the Microsoft Azure public cloud.</span></span></li>
<li><span data-ttu-id="2cf09-934">改进了商店内组件的自助服务安装，使配置更简便更直观</span><span class="sxs-lookup"><span data-stu-id="2cf09-934">Improved self-service installation of in-store components to make configuration easier and more intuitive</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-935">监控系统的运行状况，并且诊断错误和问题。</span><span class="sxs-lookup"><span data-stu-id="2cf09-935">Monitor the health of the system, and diagnose errors and issues.</span></span></td>
<td><span data-ttu-id="2cf09-936">此功能需要适用于 <a href="https://www.microsoft.com/download/details.aspx?id=42636">Microsoft Dynamics AX 2012 R3 CU8 Retail 的 System Center 2012 管理包</a>。</span><span class="sxs-lookup"><span data-stu-id="2cf09-936">This functionality requires <a href="https://www.microsoft.com/download/details.aspx?id=42636">System Center 2012 Management Pack for Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</span></span></td>
<td><span data-ttu-id="2cf09-937">现在可以通过 LCS 中的<strong>运营见解</strong>仪表板来监控和诊断 Retail 组件。</span><span class="sxs-lookup"><span data-stu-id="2cf09-937">Monitoring and diagnostics for Retail components is now available through the <strong>Operational Insights</strong> dashboard in LCS.</span></span></td>
<td><span data-ttu-id="2cf09-938"><strong>运营见解</strong>仪表板是一个基于云的监控门户，有了它便不再需要安装 System Center Operations Manager (SCOM) 基础结构。</span><span class="sxs-lookup"><span data-stu-id="2cf09-938">The <strong>Operational Insights</strong> dashboard is a cloud-based monitoring portal that replaces the need to install the System Center Operations Manager (SCOM) infrastructure.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2cf09-939">通过使用自助服务，创建、配置、下载并安装 Retail Hardware Station 和设备。</span><span class="sxs-lookup"><span data-stu-id="2cf09-939">Create, configure, download, and install Retail Hardware Station and devices by using self-service.</span></span></td>
<td><span data-ttu-id="2cf09-940">通过使用安装包装器和企业门户，用户可以基于定义的拓扑结构，对特定计算机上需要的所有组件执行自动化安装和配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-940">By using the installation packager and Enterprise Portal, a user can perform an automated installation and configuration of all components that are required on a particular computer, based on a defined topology.</span></span></td>
<td><span data-ttu-id="2cf09-941">因为只有两个安装程序包，一个用于 MPOS 客户端，另一个用于 Retail Hardware Station 组件，因此自助服务减少了在每个级别安装这些客户端组件所需的工作量。</span><span class="sxs-lookup"><span data-stu-id="2cf09-941">Because there are only two installation packages, one for the MPOS client and the other for the Retail Hardware Station component, self-service has reduced the amount of work that is required at every level to install these client components.</span></span></td>
<td><span data-ttu-id="2cf09-942">自助服务旨在最大限度地减少要求，并且更便于用户进行安装。</span><span class="sxs-lookup"><span data-stu-id="2cf09-942">Self-service aims to minimize requirements and make it easier for a user to perform an installation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="sales"></a><span data-ttu-id="2cf09-943">销售额</span><span class="sxs-lookup"><span data-stu-id="2cf09-943">Sales</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf09-944">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-944">What can you do?</span></span></th>
<th><span data-ttu-id="2cf09-945">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-945">Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="2cf09-946">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-946">Dynamics AX 7.0</span></span></th>
<th><span data-ttu-id="2cf09-947">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-947">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf09-948">在您向客户承诺订单时，可快速概览交货备选方案。</span><span class="sxs-lookup"><span data-stu-id="2cf09-948">Get a quick overview of delivery alternatives when you promise orders to customers.</span></span></td>
<td><span data-ttu-id="2cf09-949">当有产品可用性约束，而且客户在订单上请求的一个或多个产品的交货日期不能满足时，订单承诺任务就成为挑战。</span><span class="sxs-lookup"><span data-stu-id="2cf09-949">When there are product availability constraints, and the customer's requested delivery date for one or more products on the order can't be met, the order promising task becomes a challenge.</span></span> <span data-ttu-id="2cf09-950">若要查找可以抵消可用性和装运时间问题的备选方案，以便客户请求的日期可以满足，或为客户提供可以接受和信任的发货解决方案，则订单处理人员可能必须打开多个窗体，每个窗体都仅提供一部分必需信息。</span><span class="sxs-lookup"><span data-stu-id="2cf09-950">To find alternatives that can offset availability and shipping time issues so that the customer's requested date can be met, or to offer customers a delivery solution that they can accept and trust, the order processor might have to open several forms, each of which offers only a subset of the required information.</span></span> <span data-ttu-id="2cf09-951">具体而言，一个窗体显示跨站点的现有数量，另一个窗体显示内部公司设置的现有数量，第三个窗体能让用户一次一个站点/款式地计算最早可用日期，第四个窗体显示供应订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-951">More specifically, one form shows on-hand quantity across sites, another form shows on-hand quantity in the intercompany setting, a third form lets users calculate the earliest available date for one site/variant at a time, and a fourth form shows supply orders.</span></span> <span data-ttu-id="2cf09-952">因此，用户不认为自己考虑了所有相关选项，而不是仅选择了一个眼前的但次优的解决方法。</span><span class="sxs-lookup"><span data-stu-id="2cf09-952">Therefore, users don't feel confident that they have considered all the relevant options instead of just choosing an immediate but suboptimal solution.</span></span> <span data-ttu-id="2cf09-953">用户也不觉得有效，因为在订单承诺流程期间在他们打开和关闭多个页面以及组合见解和选项时发生了许多中断。</span><span class="sxs-lookup"><span data-stu-id="2cf09-953">Users also don't feel effective, because numerous interruptions occur during the order promising flow as they open and close multiple pages, and combine the insights and options.</span></span></td>
<td><span data-ttu-id="2cf09-954">基于交货日期计算的现有算法，<strong>交货备选方案</strong>页提供订单承诺的新用户体验：</span><span class="sxs-lookup"><span data-stu-id="2cf09-954">Based on the existing algorithms for delivery date calculation, the <strong>Delivery alternatives </strong>page offers a new user experience for order promising:</span></span>
<ul>
<li><span data-ttu-id="2cf09-955">它将多个窗体中的相关信息合并到一个空间。</span><span class="sxs-lookup"><span data-stu-id="2cf09-955">It consolidates relevant information from multiple forms into one space.</span></span></li>
<li><span data-ttu-id="2cf09-956">它基于用户可以从中选择的最快交货（最早可用日期）条件，提供“现成的”备选交货包，例如站点/仓库/款式/运输方式组合。</span><span class="sxs-lookup"><span data-stu-id="2cf09-956">It offers "ready-made" alternative delivery packages, such as a combination site/warehousing/variant/transport mode, based on the fastest delivery (earliest available date) criterion that the user can choose from.</span></span></li>
<li><span data-ttu-id="2cf09-957">它能让用户从模拟界面选择选项并将其转移到销售订单行。</span><span class="sxs-lookup"><span data-stu-id="2cf09-957">It lets the user select options from the simulation interface and transfer them to the sales order line.</span></span></li>
</ul></td>
<td><span data-ttu-id="2cf09-958">想要在致力于库存优化策略的同时提供高质量客户服务的公司，必须能够可靠而有竞争力地承诺订单。</span><span class="sxs-lookup"><span data-stu-id="2cf09-958">Companies that aspire to provide high customer service while committing to an inventory optimization strategy must be able to promise orders reliably and competitively.</span></span> <span data-ttu-id="2cf09-959">毕竟，其客户自己的业务需要产品按时上市。</span><span class="sxs-lookup"><span data-stu-id="2cf09-959">After all, their customers' own business requires that products be available on time.</span></span> <span data-ttu-id="2cf09-960"><strong>交货备选方案</strong>任务页通过在一个交互式位置标识和建议最佳备选订单交货日期，使得订单承诺任务更快速、简便和系统化。</span><span class="sxs-lookup"><span data-stu-id="2cf09-960">The <strong>Delivery alternatives</strong> task page makes the order promising task quicker, easier, and more systematic by identifying and recommending the best alternative order delivery dates in one interactive place.</span></span></td>
</tr>
</tbody>
</table>

## <a name="service-management"></a><span data-ttu-id="2cf09-961">服务管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-961">Service management</span></span>

<span data-ttu-id="2cf09-962">未添加新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-962">No new features have been added.</span></span>

## <a name="transportation-management"></a><span data-ttu-id="2cf09-963">运输管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-963">Transportation management</span></span>

<span data-ttu-id="2cf09-964">未添加新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-964">No new features have been added.</span></span>

## <a name="travel-and-expense"></a><span data-ttu-id="2cf09-965">出差和支出</span><span class="sxs-lookup"><span data-stu-id="2cf09-965">Travel and expense</span></span>

<span data-ttu-id="2cf09-966">未添加新功能。</span><span class="sxs-lookup"><span data-stu-id="2cf09-966">No new features have been added.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="2cf09-967">仓库管理</span><span class="sxs-lookup"><span data-stu-id="2cf09-967">Warehouse management</span></span>

| <span data-ttu-id="2cf09-968">您能怎么做？</span><span class="sxs-lookup"><span data-stu-id="2cf09-968">What can you do?</span></span> | <span data-ttu-id="2cf09-969">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2cf09-969">Dynamics AX 2012</span></span> | <span data-ttu-id="2cf09-970">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="2cf09-970">Dynamics AX 7.0</span></span> | <span data-ttu-id="2cf09-971">为什么如此重要</span><span class="sxs-lookup"><span data-stu-id="2cf09-971">Why is this important?</span></span> |
|------------------|------------------|-----------------|------------------------|
| <span data-ttu-id="2cf09-972">下载、安装和配置仓库移动设备门户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-972">Download, install, and configure the Warehouse Mobile Devices portal.</span></span> | <span data-ttu-id="2cf09-973">您可以通过一个标准设置，在 Microsoft Dynamics AX 安装过程中下载、安装和配置该门户。</span><span class="sxs-lookup"><span data-stu-id="2cf09-973">You can download, install, and configure the portal during the Microsoft Dynamics AX installation process, through a standard setup.</span></span> <span data-ttu-id="2cf09-974">它专用于自驱动的本地部署和配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-974">It's designed for self-driven on-premises deployment and configuration.</span></span> | <span data-ttu-id="2cf09-975">您可以在仓库管理中通过菜单项下载独立安装程序。</span><span class="sxs-lookup"><span data-stu-id="2cf09-975">You can download a stand-alone installer through a menu item in Warehouse management.</span></span> <span data-ttu-id="2cf09-976">它专用于自驱动的本地部署和配置。</span><span class="sxs-lookup"><span data-stu-id="2cf09-976">It's designed for self-driven on-premises deployment and configuration.</span></span> | <span data-ttu-id="2cf09-977">在您设置移动设备功能时，您必须在本地安装并配置仓库移动设备门户，并在云中与 Dynamics AX 连接。</span><span class="sxs-lookup"><span data-stu-id="2cf09-977">When you're setting up the mobile device functionality, you must install and configure the Warehouse Mobile Devices Portal locally and get a connection to Dynamics AX in the cloud.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2cf09-978">其他资源</span><span class="sxs-lookup"><span data-stu-id="2cf09-978">Additional resources</span></span>

[<span data-ttu-id="2cf09-979">新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="2cf09-979">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="2cf09-980">新任务指南可用（2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="2cf09-980">New task guides available (February 2016)</span></span>](new-task-guides-available-february-2016.md)
