---
title: 预算概览
description: 几乎每家使用 Microsoft Dynamics 365 for Finance and Operations 中的财务功能的公司都必须可以创建预算与实际的报表、 本文说明要在 Finance and Operations 中创建预算或从第三方程序加载预算所需的最低配置。
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01b7970119b9abb26570c19162e159dd05496168
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559729"
---
# <a name="budgeting-overview"></a><span data-ttu-id="20d3d-104">预算编制概览</span><span class="sxs-lookup"><span data-stu-id="20d3d-104">Budgeting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20d3d-105">几乎每家使用 Microsoft Dynamics 365 for Finance and Operations 中的财务功能的公司都必须可以创建预算与实际的报表、</span><span class="sxs-lookup"><span data-stu-id="20d3d-105">Almost every company that uses Financials functionality in Microsoft Dynamics 365 for Finance and Operations will have to be able to create reports of budget vs. actuals.</span></span> <span data-ttu-id="20d3d-106">本文说明要在 Finance and Operations 中创建预算或从第三方程序加载预算所需的最低配置。</span><span class="sxs-lookup"><span data-stu-id="20d3d-106">This article explains the minimum configuration that is required in order to create budgets in Finance and Operations or load them from a third-party program.</span></span>

<a name="overview"></a><span data-ttu-id="20d3d-107">概览</span><span class="sxs-lookup"><span data-stu-id="20d3d-107">Overview</span></span>
--------

<span data-ttu-id="20d3d-108">法人的已审核预算保留在一个名为 *“预算登记分录”* 的文档中。</span><span class="sxs-lookup"><span data-stu-id="20d3d-108">The approved budget for a legal entity is maintained in a document that is known as a *budget register entry*.</span></span> <span data-ttu-id="20d3d-109">预算登记分录文档中的行称作*预算科目*分录，它们包含财务维度信息、日期和已审核预算的金额。</span><span class="sxs-lookup"><span data-stu-id="20d3d-109">The lines in a budget register entry document are known as *budget account* entries, and contain financial dimension information, dates, and the amounts of the approved budget.</span></span> <span data-ttu-id="20d3d-110">预算登记分录文档与基本财务报表和查询页（其中，将比较分类帐实际金额与预算金额）集成。</span><span class="sxs-lookup"><span data-stu-id="20d3d-110">The budget register entry document is integrated with basic financial reports and inquiry pages where ledger actual amounts are compared to budget amounts.</span></span> 

<span data-ttu-id="20d3d-111">可通过多种方法在 Finance and Operations 中创建预算登记分录：</span><span class="sxs-lookup"><span data-stu-id="20d3d-111">There are multiple methods for creating budget register entries in Finance and Operations:</span></span>

-   <span data-ttu-id="20d3d-112">在**预算登记分录**页上手动输入文档信息。</span><span class="sxs-lookup"><span data-stu-id="20d3d-112">Manually enter the document information on the **Budget register entries** page.</span></span>
-   <span data-ttu-id="20d3d-113">使用可通过单击**预算登记分录**页上的**在 Excel 中打开**按钮打开的 Microsoft Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="20d3d-113">Use the Microsoft Excel template that you can open by clicking the **Open in Excel** button on the **Budget register entries** page.</span></span>
-   <span data-ttu-id="20d3d-114">使用数据管理中的**预算科目分录**数据实体导入预算登记分录。</span><span class="sxs-lookup"><span data-stu-id="20d3d-114">Use the **Budget Account Entries** data entity in Data management to import budget register entries.</span></span> <span data-ttu-id="20d3d-115">当您必须将多个预算科目分录导入系统中时，应考虑使用此方法并启用**基于集的** **处理** 参数。</span><span class="sxs-lookup"><span data-stu-id="20d3d-115">You should consider using this method and turning on the **Set based** \*\*processing \*\*parameter when you must import many budget account entries into the system.</span></span>
-   <span data-ttu-id="20d3d-116">如果公司使用预算计划功能来准备预算数据，您可以使用**生成预算登记分录**定期流程。</span><span class="sxs-lookup"><span data-stu-id="20d3d-116">If the company uses Budget planning functionality to prepare budget data, you can use the **Generate budget register entry** periodic process.</span></span>

<span data-ttu-id="20d3d-117">在更新预算余额后，预算登记分录将视为已完成。</span><span class="sxs-lookup"><span data-stu-id="20d3d-117">The budget register entry is considered completed when the budget balances have been updated.</span></span> <span data-ttu-id="20d3d-118">在**预算登记分录**页上，单击所选预算登记分录或多个分录的**更新预算余额**。</span><span class="sxs-lookup"><span data-stu-id="20d3d-118">On the **Budget register entries** page, click **Update budget balances** for a selected budget register entry or multiple entries.</span></span> <span data-ttu-id="20d3d-119">在更新预算余额后，预算登记分录的状态将变为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="20d3d-119">After you update the budget balances, the status of the budget register entry changes to **Completed**.</span></span> <span data-ttu-id="20d3d-120">无法重新打开已完成的预算登记分录以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="20d3d-120">Completed budget register entry can't be re-opened for edits.</span></span> <span data-ttu-id="20d3d-121">因此，如果必须调整预算数据，您必须创建新的预算登记分录，而不是更正已完成的预算登记分录中的数据。</span><span class="sxs-lookup"><span data-stu-id="20d3d-121">Therefore, if the budget data must be adjusted, you must create a new budget register entry instead of correcting data in the completed budget register entry.</span></span>

## <a name="configuration"></a><span data-ttu-id="20d3d-122">配置</span><span class="sxs-lookup"><span data-stu-id="20d3d-122">Configuration</span></span>
<span data-ttu-id="20d3d-123">在配置预算编制时，从**预算编制参数**页上开始。</span><span class="sxs-lookup"><span data-stu-id="20d3d-123">When you configure budgeting, start on the **Budgeting parameters** page.</span></span> <span data-ttu-id="20d3d-124">在此页上，您必须定义预算日记帐、预算登记分录的编号规则和工作区中的默认行为。</span><span class="sxs-lookup"><span data-stu-id="20d3d-124">On this page, you must define the budget journal, the number sequence for budget register entries, and the default behavior in the workspaces.</span></span>

<span data-ttu-id="20d3d-125">接下来，如果存在根据预算类型（例如，转移或修订）控制预算登记分录的审核的策略，则必须在**预算编制工作流**页上创建预算登记分录工作流。</span><span class="sxs-lookup"><span data-stu-id="20d3d-125">Next, if there are policies that govern the approval of budget register entries, based on budget type (for example, transfers or revisions), you must create budget register entry workflows on the **Budgeting workflows** page.</span></span> <span data-ttu-id="20d3d-126">如果存在允许转移而无需工作流审核的方案，您可以定义预算转移规则以支持这些方案。</span><span class="sxs-lookup"><span data-stu-id="20d3d-126">If there are scenarios where transfers might be allowed without workflow approval, you can define budget transfer rules to support those scenarios.</span></span> 

<span data-ttu-id="20d3d-127">在**预算编制维度**页上，您必须根据会计科目表中使用的维度来选择用于预算编制的财务维度。</span><span class="sxs-lookup"><span data-stu-id="20d3d-127">On the **Budgeting dimensions** page, you must select the financial dimensions that are used for budgeting, based on the dimensions that are used in the chart of accounts.</span></span> <span data-ttu-id="20d3d-128">您可以选择所有或部分财务维度来进行预算编制。</span><span class="sxs-lookup"><span data-stu-id="20d3d-128">You can select all financial dimensions or a subset of them for budgeting.</span></span>

<span data-ttu-id="20d3d-129">定义与所有或部分预算对应的 *预算模型*。</span><span class="sxs-lookup"><span data-stu-id="20d3d-129">Define a \*budget model \*that corresponds to all or some of the budgets.</span></span> <span data-ttu-id="20d3d-130">您可以将单个预算模型用于所有预算登记分录。</span><span class="sxs-lookup"><span data-stu-id="20d3d-130">You can use a single budget model for all budget register entries.</span></span> <span data-ttu-id="20d3d-131">或者，您可以根据预算类型、地理位置或其他预算分类方式来创建单独的模型。</span><span class="sxs-lookup"><span data-stu-id="20d3d-131">Alternatively, you can create separate models that are based on the budget type, the geographical location, or some other way that a budget can be classified.</span></span> 

> [!NOTE] 
> <span data-ttu-id="20d3d-132">如果使用预算控制，则只能将一个预算模型与一个特定的预算周期跨度关联。</span><span class="sxs-lookup"><span data-stu-id="20d3d-132">If budget control is used, you can associate only one budget model with a specific budget cycle time span.</span></span> 

<span data-ttu-id="20d3d-133">创建用于标识要记录的预算交易记录类型和任何相关工作流的 *“预算代码”*。</span><span class="sxs-lookup"><span data-stu-id="20d3d-133">Create *budget codes* that identify the type of budget transactions to record and any related workflow.</span></span> <span data-ttu-id="20d3d-134">预算代码可支持以下预算类型：</span><span class="sxs-lookup"><span data-stu-id="20d3d-134">Budget codes can support the following budget types:</span></span>

-   <span data-ttu-id="20d3d-135">原始预算</span><span class="sxs-lookup"><span data-stu-id="20d3d-135">Original budget</span></span>
-   <span data-ttu-id="20d3d-136">转移</span><span class="sxs-lookup"><span data-stu-id="20d3d-136">Transfer</span></span>
-   <span data-ttu-id="20d3d-137">修订</span><span class="sxs-lookup"><span data-stu-id="20d3d-137">Revision</span></span>
-   <span data-ttu-id="20d3d-138">保留款</span><span class="sxs-lookup"><span data-stu-id="20d3d-138">Encumbrance</span></span>
-   <span data-ttu-id="20d3d-139">预留款</span><span class="sxs-lookup"><span data-stu-id="20d3d-139">Pre-encumbrance</span></span>
-   <span data-ttu-id="20d3d-140">结转预算</span><span class="sxs-lookup"><span data-stu-id="20d3d-140">Carry-forward budget</span></span>

<span data-ttu-id="20d3d-141">利用预算代码，您可以获得整个预算周期内的已审核的预算修改的审计线索。</span><span class="sxs-lookup"><span data-stu-id="20d3d-141">Budget codes let you have an audit trail of approved budget modifications throughout the course of the budget cycle.</span></span> <span data-ttu-id="20d3d-142">如果工作流与预算代码关联，则将为使用该预算代码的所有预算登记分录启用工作流，并且必须先完成工作流步骤，之后预算登记分录才能达到**已完成**阶段。</span><span class="sxs-lookup"><span data-stu-id="20d3d-142">If a workflow is associated with a budget code, the workflow will be enabled for all budget register entries that use that budget code, and workflow steps must be completed before the budget register entry can reach the **Completed** stage.</span></span>  

<span data-ttu-id="20d3d-143">您还可以选择性地设置*预算转移规则*。</span><span class="sxs-lookup"><span data-stu-id="20d3d-143">You can also optionally set up *budget transfer rules*.</span></span> <span data-ttu-id="20d3d-144">要使用预算转移规则，请选择**预算参数**页上的**使用预算转移规则**。</span><span class="sxs-lookup"><span data-stu-id="20d3d-144">To use budget transfer rules, select **Use rules for budget transfers** on the **Budget parameters** page.</span></span> <span data-ttu-id="20d3d-145">在使用预算转移规则时，如果用户使用**转移**类型的预算代码创建文档，则在违反预算转移规则的情况下，将不会更新预算余额。</span><span class="sxs-lookup"><span data-stu-id="20d3d-145">When budget transfer rules are used, if a user creates a document by using a budget code of the **Transfer** type, budget balances won't be updated if the budget transfer rules are violated.</span></span> <span data-ttu-id="20d3d-146">例如，您可以允许预算转移文档（其中，费用预算在销售和市场营销部门的主科目之间转移），但可以禁止在该部门转入或转出预算，除非已允许针对该类型的预算科目分录的工作流审核。</span><span class="sxs-lookup"><span data-stu-id="20d3d-146">For example, you can allow budget transfer documents where the expense budget is transferred between the main accounts for the Sales and Marketing department, but can prohibit budget from being transferred from or to that department unless workflow approval has been granted for that type of budget account entry.</span></span>

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a><span data-ttu-id="20d3d-147">使用工作区和查询页来跟踪预算和实际值</span><span class="sxs-lookup"><span data-stu-id="20d3d-147">Using workspaces and inquiry pages to track budget vs. actuals</span></span>
<span data-ttu-id="20d3d-148">预算经理可以在**分类帐预算和预测**工作区中检查预算的当前状态。</span><span class="sxs-lookup"><span data-stu-id="20d3d-148">The budget manager can review the current state of a budget in the **Ledger budgets and forecasts** workspace.</span></span> <span data-ttu-id="20d3d-149">**高于预算的费用**和**低于预算的收入**选项卡可让您快速了解财务维度组合，其中预算目标未达到或正在接近限额。</span><span class="sxs-lookup"><span data-stu-id="20d3d-149">The **Expense over budget** and **Revenue under budget** tabs provide a quick view of the financial dimension combinations where budget targets aren't being met or are approaching the threshold.</span></span> <span data-ttu-id="20d3d-150">您可以通过单击**配置我的工作区**来个性化这些选项卡上使用的预算限额百分比和财务维度集。</span><span class="sxs-lookup"><span data-stu-id="20d3d-150">You can personalize the budget threshold percentage and financial dimension sets that are used on those tabs by clicking **Configure my workspace**.</span></span> <span data-ttu-id="20d3d-151">您可以单击**部门经理**查看负责已在这些选项卡上选定的特定财务维度组合的工作人员。</span><span class="sxs-lookup"><span data-stu-id="20d3d-151">You can click **Unit managers** to see the workers who are responsible for specific financial dimension combinations that are selected on those tabs.</span></span> <span data-ttu-id="20d3d-152">例如，如果您发现运营部门的费用预算将超出预算限额，您可轻松找到并联系运营部门经理以讨论此问题。</span><span class="sxs-lookup"><span data-stu-id="20d3d-152">For example, if you see that the expense budget of the Operations department is going over the budget threshold, you can easily find and contact the Operations department manager to discuss the issue.</span></span> 

> [!NOTE] 
> <span data-ttu-id="20d3d-153">**组织单位**页上的**部门经理**字段确定哪些经理支持特定财务维度组合。</span><span class="sxs-lookup"><span data-stu-id="20d3d-153">The **Department manager** field on the **Organization Units** page determines which managers support specific financial dimension combinations.</span></span> <span data-ttu-id="20d3d-154">单击选项卡底部的**查看更多**可打开**预算与实际**查询页，以查看有关预算金额与实际金额的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="20d3d-154">Click **See more** at the bottom of the tab to open the **Budget vs actuals** inquiry page for more details about budget amounts versus actual amounts.</span></span> 

<span data-ttu-id="20d3d-155">**实际值与预算**查询页可让您深入了解预算金额与实际金额的详细信息。</span><span class="sxs-lookup"><span data-stu-id="20d3d-155">The **Actual vs budget** inquiry page lets you drill into the details of the budget versus actual amounts.</span></span> <span data-ttu-id="20d3d-156">在该查询页上选择一行，然后单击**期间余额**可查看分布在各个会计期间的预算金额和实际金额。</span><span class="sxs-lookup"><span data-stu-id="20d3d-156">Select a line on the inquiry page, and then click **Period balances** to see budget and actual amounts spread across fiscal periods.</span></span> <span data-ttu-id="20d3d-157">**预算科目分录**页可让您深入了解预算登记分录中的预算金额的详细信息。</span><span class="sxs-lookup"><span data-stu-id="20d3d-157">The **Budget account entries** page provides drill-through to the details of the budget amount in budget register entries.</span></span> <span data-ttu-id="20d3d-158">**普通日记帐分录**页打开包含在计算的**实际**金额中的分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="20d3d-158">The **General journal entries** page opens the ledger transactions that are included in the calculated **Actuals** amount.</span></span> 

<span data-ttu-id="20d3d-159">使用预算计划编制功能的公司可以在**分类帐预算和预测**工作区中创建和使用*预算预测*。</span><span class="sxs-lookup"><span data-stu-id="20d3d-159">A company that is using Budget planning functionality can create and use *budget forecasts* in the **Ledger budgets and forecasts** workspace.</span></span>



