---
title: "预算计划与其他模块的集成"
description: "预算计划可以从多个不同资源生成。 所有资源的周期性流程的基本元素相同。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: f63297b35f989f99236547514463eb2d4206797b
ms.contentlocale: zh-cn
ms.lasthandoff: 06/30/2017


---

# <a name="budget-planning-integration-with-other-modules"></a><span data-ttu-id="2bcc9-104">预算计划与其他模块的集成</span><span class="sxs-lookup"><span data-stu-id="2bcc9-104">Budget planning integration with other modules</span></span>

[!include[banner](../includes/banner.md)]




<a name="periodic-processes-for-generating-budget-plans"></a><span data-ttu-id="2bcc9-105">生成预算计划的周期性流程</span><span class="sxs-lookup"><span data-stu-id="2bcc9-105">Periodic processes for generating budget plans</span></span>
----------------------------------------------

<span data-ttu-id="2bcc9-106">预算计划可以从以下资源生成：</span><span class="sxs-lookup"><span data-stu-id="2bcc9-106">Budget plans can be generated from the following resources:</span></span>

-   <span data-ttu-id="2bcc9-107">总帐交易记录</span><span class="sxs-lookup"><span data-stu-id="2bcc9-107">General ledger transactions</span></span>
-   <span data-ttu-id="2bcc9-108">固定资产</span><span class="sxs-lookup"><span data-stu-id="2bcc9-108">Fixed assets</span></span>
-   <span data-ttu-id="2bcc9-109">预测位置</span><span class="sxs-lookup"><span data-stu-id="2bcc9-109">Forecast positions</span></span>
-   <span data-ttu-id="2bcc9-110">项目预测</span><span class="sxs-lookup"><span data-stu-id="2bcc9-110">Project forecasts</span></span>
-   <span data-ttu-id="2bcc9-111">供应预测</span><span class="sxs-lookup"><span data-stu-id="2bcc9-111">Supply forecasts</span></span>
-   <span data-ttu-id="2bcc9-112">需求预测</span><span class="sxs-lookup"><span data-stu-id="2bcc9-112">Demand forecasts</span></span>
-   <span data-ttu-id="2bcc9-113">预算登记分录</span><span class="sxs-lookup"><span data-stu-id="2bcc9-113">Budget register entries</span></span>
-   <span data-ttu-id="2bcc9-114">其他预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-114">Other budget plans</span></span>

<span data-ttu-id="2bcc9-115">所有流程的周期性流程的基本元素相同。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-115">The basic elements of the periodic process are the same for all the processes.</span></span> <span data-ttu-id="2bcc9-116">选项卡可以定义数据源、目标（预算计划）属性和在后台作为批处理运行流程的选项。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-116">Tabs let you define the source of the data, the target (budget plan) attributes, and options to run the process in the background as a batch process.</span></span> <span data-ttu-id="2bcc9-117">本文章的后面部分介绍在每个流程中可能不明显的物料。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-117">Later sections of this article describe items that might not be apparent in each process.</span></span>

### <a name="actions"></a><span data-ttu-id="2bcc9-118">行为</span><span class="sxs-lookup"><span data-stu-id="2bcc9-118">Actions</span></span>

<span data-ttu-id="2bcc9-119">对于每个生成流程，有三个操作可用：</span><span class="sxs-lookup"><span data-stu-id="2bcc9-119">For each generation process, three actions are available:</span></span>

-   <span data-ttu-id="2bcc9-120">**创建新的预算计划**创建具有在**目标**部分选择的属性的新计划。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-120">**Create a new budget plan** creates a new plan that has the attributes that are selected in the **Target **section.</span></span> <span data-ttu-id="2bcc9-121">这些属性不必是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-121">These attributes don't have to be unique.</span></span> <span data-ttu-id="2bcc9-122">因此，两个计划可以具有相同的名称和其他值。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-122">Therefore, two plans can have the same name and other values.</span></span>
-   <span data-ttu-id="2bcc9-123">**更换现有预算计划方案**删除所选预算计划方案中目标预算计划的所有数据，并创建使用所选源数据的新行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-123">**Replace the existing budget plan scenario** deletes all data in the target budget plan in the selected budget plan scenario and creates new lines that use the selected source data.</span></span>
-   <span data-ttu-id="2bcc9-124">**更新现有预算计划方案并追加新数据**更新与源行匹配的目标计划中的现有行和添加新数据的新行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-124">**Update the existing budget plan scenario, and append new data** updates existing lines in the target plan that match the source lines and adds new lines for new data.</span></span> <span data-ttu-id="2bcc9-125">匹配基于会计科目、日期、预算类和各个其他字段。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-125">The matching is based on the ledger account, date, budget class, and various other fields.</span></span> <span data-ttu-id="2bcc9-126">例如，当您从预测职位生成预算计划时，该职位编号是一个重要字段。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-126">For example, when you generate budget plans from forecast positions, the position number is an important field.</span></span> <span data-ttu-id="2bcc9-127">具有与该源职位编号匹配的职位编号的所有行将使用来自该源的新行替换。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-127">All lines that have a position number that matches the source position number are replaced with the new lines from the source.</span></span>

### <a name="source"></a><span data-ttu-id="2bcc9-128">来源</span><span class="sxs-lookup"><span data-stu-id="2bcc9-128">Source</span></span>

<span data-ttu-id="2bcc9-129">对于所有流程，**源**选项卡可以通过使用**筛选器**按钮筛选数据。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-129">For all processes, the **Source** tab lets you filter data by using the **Filter** button.</span></span> <span data-ttu-id="2bcc9-130">默认情况下，特定字段添加到每个流程的筛选器。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-130">By default, specific fields are added to the filter for each process.</span></span> <span data-ttu-id="2bcc9-131">例如，对于流程**从总帐生成预算计划**，**会计科目**和**主科目**类别可用，并且在生成页显示。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-131">For example, for the **Generate budget plan from general ledger** process, the **Ledger account** and **Main account** categories are available, and appear on the generation page.</span></span> <span data-ttu-id="2bcc9-132">您添加到筛选器的所有字段也将添加到此页，以及您添加的任何条件。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-132">Any fields that you add to the filter are also added to the page, together with with any criteria that you add.</span></span>

### <a name="target"></a><span data-ttu-id="2bcc9-133">目标</span><span class="sxs-lookup"><span data-stu-id="2bcc9-133">Target</span></span>

<span data-ttu-id="2bcc9-134">**目标**选项卡上的**历史**选项允许您在预算计划中使用源数据的日期作为生效日期。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-134">The **Historical** option on the **Target** tab lets you use the dates from the source data as the effective date in the budget plan.</span></span> <span data-ttu-id="2bcc9-135">通常，生效日期必须在计划的预算周期中。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-135">Typically, the effective date must be within the plan’s budget cycle.</span></span> <span data-ttu-id="2bcc9-136">当您将**历史**选项设置为**是**时，使用源的日期（甚至年份），以便您可以使用过去数据作为比较的基础。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-136">When you set the **Historical** option to **Yes**, the date (even the year) of the source is used, so that you can use past data as a basis for comparison.</span></span> <span data-ttu-id="2bcc9-137">您不能修改预算计划的历史数据，计划设置为已审核的工作流状态。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-137">You can't modify historical data in the budget plan, and the plan is set to an approved workflow status.</span></span> <span data-ttu-id="2bcc9-138">但是，如果您在计划有必需更改的其他方案，您可以重置状态。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-138">However, you can reset the status if you must other scenarios in the plan require changes.</span></span>

<span data-ttu-id="2bcc9-139">该页顶部的**聚合总计**字段还确定要使用的日期。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-139">The **Aggregate total by** field at the top of the page also determines the date that is used.</span></span> <span data-ttu-id="2bcc9-140">此字段合计金额，并且可以选择将生效日期设置为会计年度或会计期间的第一天。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-140">This field totals amounts, and optionally sets the effective date to the first day of the fiscal year or fiscal period.</span></span> 

<span data-ttu-id="2bcc9-141">**目标**选项卡上的很多字段将变为可编辑或只读，具体取决于您选择的操作。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-141">Many of the fields on the **Target** tab become editable or read-only, depending on the action that you select.</span></span> <span data-ttu-id="2bcc9-142">在您将创建新预算计划更改为更新现有计划时，**预算计划名称**字段将变为不可用，与选择现有计划相关的字段将变为可用。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-142">When you change from creating a new budget plan to updating an existing plan, the **Budget plan name** field becomes unavailable, and the fields that are related to selecting an existing plan become available.</span></span> <span data-ttu-id="2bcc9-143">在**目标**选项卡和 **源** 选项卡上，**分类帐**字段始终不可用，因为此值由所选预算计划流程确定。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-143">On both the **Target** tab and the **Source **tab, the **Ledger** field is always unavailable, because the value is determined by the selected budget planning process.</span></span> 

<span data-ttu-id="2bcc9-144">**预算类**字段可以将预算计划行设置为支出交易记录或收入交易记录。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-144">The **Budget class** field lets you set the budget plan lines as either expense transactions or revenue transactions.</span></span> <span data-ttu-id="2bcc9-145">通常，收入交易记录是会计科目的贷方，因此存储为负金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-145">Usually, revenue transactions are credits to a ledger account and are therefore stored as negative amounts.</span></span> <span data-ttu-id="2bcc9-146">通常，这些交易记录在预算计划中同时显示为负金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-146">Typically, these transactions also appear as negative amounts in the budget plan.</span></span> <span data-ttu-id="2bcc9-147">不过，通过在计划布局中作为字段添加预算类，您可以启用收入显示为正金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-147">However, by adding the budget class as a field in the plan layout, you can enable revenue to appear as positive amounts.</span></span>

### <a name="generation-rules"></a><span data-ttu-id="2bcc9-148">生成规则</span><span class="sxs-lookup"><span data-stu-id="2bcc9-148">Generation rules</span></span>

<span data-ttu-id="2bcc9-149">三个字段提供其他功能：**系数**、**最小值**和**舍入****规则**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-149">Three fields provide additional functionality: **Factor**, **Minimum**, and **Rounding** **rule**.</span></span> 

<span data-ttu-id="2bcc9-150">**系数**字段中的值乘以源金额来设置预算计划中的金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-150">The value in the **Factor** field is multiplied by the source amount to set the amount in the budget plan.</span></span> <span data-ttu-id="2bcc9-151">然后在您创建预算计划行时，您可以进行调整。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-151">You can then make adjustments when you create budget plan lines.</span></span> <span data-ttu-id="2bcc9-152">例如，可以为提高 3% 输入 **1.03**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-152">For example, you can enter **1.03** for a 3 percent increase.</span></span> <span data-ttu-id="2bcc9-153">系数必须为正数。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-153">The factor must be a positive number.</span></span> 

<span data-ttu-id="2bcc9-154">**最小值**字段可以设置创建预算计划行的阈值金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-154">The **Minimum** field lets you set the threshold amount for creating a budget plan line.</span></span> <span data-ttu-id="2bcc9-155">如果源金额少于此数字，预算计划行不创建。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-155">If the source amount is less than this number, the budget plan line isn't created.</span></span> <span data-ttu-id="2bcc9-156">值 **0.00**  允许所有金额，但不限制行是否为正金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-156">A value of **0.00** allows all amounts but doesn't limit lines to positive amounts.</span></span> <span data-ttu-id="2bcc9-157">（没有值限制行必须为正金额。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-157">(No value limits lines to positive amounts.</span></span> <span data-ttu-id="2bcc9-158">负金额始终包括在内并且通常表示贷方条目）。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-158">Negative amounts are always included and usually represent credit entries.)</span></span>

<span data-ttu-id="2bcc9-159">**舍入规则**字段可以设置创建的预算计划行的精度。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-159">The **Rounding rule** field lets you set the precision of the budget plan lines that are created.</span></span> <span data-ttu-id="2bcc9-160">您可以将金额舍入到最接近的货币的 1.00、10.00、100.00，依此类推。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-160">You can round amounts to the nearest 1.00, 10.00, 100.00, and so on, of currency.</span></span>

## <a name="notes-for-specific-processes"></a><span data-ttu-id="2bcc9-161">特定流程的注释</span><span class="sxs-lookup"><span data-stu-id="2bcc9-161">Notes for specific processes</span></span>
### <a name="generate-budget-plan-from-general-ledger"></a><span data-ttu-id="2bcc9-162">从总帐生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-162">Generate budget plan from general ledger</span></span>

<span data-ttu-id="2bcc9-163">在您从总帐数据创建预算计划时，如果将**历史**选项设置为**否**，则必须将**聚合总计**字段设置为**会计年度**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-163">When you create a budget plan from general ledger data, you must set the **Aggregate total by** field to **Fiscal year** if the **Historical** option is set to **No**.</span></span> <span data-ttu-id="2bcc9-164">源中的期间和日期可能与目标中日期的期间不匹配。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-164">The periods and dates in the source might not match the periods in dates in the target.</span></span> <span data-ttu-id="2bcc9-165">由于流程没有可靠的方式映射这些值，您必须限制流程到年份的第一天。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-165">Because the process has no reliable way to map these values, you must limit the process to the first of the year.</span></span> 

<span data-ttu-id="2bcc9-166">在目标中，**预算类**字段设置为**支出**或**收入**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-166">In the target, the **Budget class** field is set to either **Expense** or **Revenue**.</span></span> <span data-ttu-id="2bcc9-167">此设置用于在行上的主科目不是**收入**或**支出**类型时，选择创建的行的**预算类型**属性。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-167">This setting is used to select the **Budget type** attribute for lines that are created, when the main account on a line isn't of the **Revenue** or **Expense** type.</span></span>

### <a name="generate-budget-plan-from-fixed-assets"></a><span data-ttu-id="2bcc9-168">从固定资产生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-168">Generate budget plan from fixed assets</span></span>

<span data-ttu-id="2bcc9-169">**从固定资产生成预算计划**流程不具有按期间或天聚合的选项。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-169">The **Generate budget plan from fixed assets** process has no option for aggregating by period or day.</span></span> <span data-ttu-id="2bcc9-170">还不存在将计划设置为历史的选项。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-170">There is also no option for setting the plan as historical.</span></span> <span data-ttu-id="2bcc9-171">您可以使用此周期性流程在预算计划中包括固定资产的计划交易记录。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-171">You can use this periodic process to include projected transactions for fixed assets in your budget planning.</span></span>

### <a name="generate-budget-plan-from-forecast-positions"></a><span data-ttu-id="2bcc9-172">从预测职位生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-172">Generate budget plan from forecast positions</span></span>

<span data-ttu-id="2bcc9-173">**从预测职位生成预算计划**流程将源预测职位分配到预算计划行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-173">The **Generate budget plan from forecast positions** process assigns the source forecast position to the budget plan line.</span></span> <span data-ttu-id="2bcc9-174">您可以通过在预算计划布局中作为行添加预测职位或通过使用**预算计划行**查询来查看职位。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-174">You can view the position by adding the forecast position as a row in the budget plan layout or by using the **Budget plan lines** inquiry.</span></span> <span data-ttu-id="2bcc9-175">如果您不希望将预测职位分配到预算计划行，则将**在预算计划行中包含职位**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-175">If you don't want the forecast position to be assigned to budget plan lines, set the **Include position in budget plan line** option to **No**.</span></span>

<span data-ttu-id="2bcc9-176">预算计划中的行按会计科目和职位聚合。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-176">Lines in the budget plan are aggregated by ledger account and position.</span></span> <span data-ttu-id="2bcc9-177">但是，您可以排除职位编号，以使行只按会计科目聚合。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-177">However, you can exclude the position number, so that lines are aggregated by ledger account only.</span></span> <span data-ttu-id="2bcc9-178">在**目标**选项卡上，将**在预算计划行中包含职位**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-178">On the **Target** tab, set the **Include position in budget plan** option to **No**.</span></span>

<span data-ttu-id="2bcc9-179">在**预算计划 FTE 方案**字段中，可以选择在预算计划中包括全职等价的数量 (FTE) 的方案。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-179">In the **Budget plan FTE scenario** field, you can select a scenario to include the number of full-time equivalents (FTEs) in the budget plan.</span></span> <span data-ttu-id="2bcc9-180">此字段限制为在目标预算计划的布局中包括的数量类型方案。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-180">This field is limited to quantity-type scenarios that are included in the layout of the target budget plan.</span></span> <span data-ttu-id="2bcc9-181">如果您选择了一个 FTE 方案，还必须选择 FTE 主科目。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-181">If you select an FTE scenario, you must also select an FTE main account.</span></span> <span data-ttu-id="2bcc9-182">此科目用于创建数量预算计划行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-182">This account is used to create the quantity budget plan lines.</span></span> 

<span data-ttu-id="2bcc9-183">在源中选择的预算计划流程和预算计划方案设置目标方案预算计划流程和方案。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-183">The budget planning process and budget plan scenario that are selected in the source set the target scenario budget planning process and scenario.</span></span> <span data-ttu-id="2bcc9-184">由于这些属性分配给预测职位，它们必须与预算计划匹配。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-184">Because these attributes are assigned to forecast positions, they must match the budget plan.</span></span> <span data-ttu-id="2bcc9-185">因此，这些属性不能在目标中修改。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-185">Therefore, these attributes can't be modified on the target.</span></span>

### <a name="generate-budget-plan-from-project-forecasts"></a><span data-ttu-id="2bcc9-186">从项目预测生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-186">Generate budget plan from project forecasts</span></span>

<span data-ttu-id="2bcc9-187">**从项目预测生成预算计划**流程，如同**从预测职位生成预算计划**流程，具有在数量方案中包括项目数量（工时、支出和物料）的选项。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-187">The **Generate budget plan from project forecasts** process, like the **Generate budget plan from forecast positions** process, has an option to include project quantities (hours, expenses, and items) in a quantity scenario.</span></span> <span data-ttu-id="2bcc9-188">这两个流程在预算计划布局中还有类似的列筛选器。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-188">The two process also have similar filters for the columns in the budget plan layout.</span></span> 

<span data-ttu-id="2bcc9-189">在**源**选项卡上，**包括报表**部分的三个选项确定创建哪些预算计划行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-189">On the **Source** tab, three options in the **Include statement** section determine which budget plan lines are created.</span></span> <span data-ttu-id="2bcc9-190">这些选项与在您直接从项目预测创建预算登记分录时可用的选项相同。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-190">These options are the same as the options that are available when you create budget register entries directly from project forecasts.</span></span> <span data-ttu-id="2bcc9-191">将**损益**选项设置为**是**以创建成本行和收入行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-191">Set the **Profit and loss** option to **Yes** to create lines for costs and for revenues.</span></span> <span data-ttu-id="2bcc9-192">将 **WIP** 选项设置为**是**以创建在制品条目。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-192">Set the **WIP** option to **Yes** to create work in process entries.</span></span> <span data-ttu-id="2bcc9-193">将**工资分配**选项设置为**是**以创建工时交易记录的工资对方科目的行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-193">Set the **Payroll allocation** option to **Yes** to create lines for the payroll offset accounts for hour transactions.</span></span> 

<span data-ttu-id="2bcc9-194">没有**预算类**字段，因为预算类（**支出**或**收入**）由源确定。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-194">There is no **Budget class** field, because the budget class (**Expense** or **Revenue**) is determined by the source.</span></span> 

<span data-ttu-id="2bcc9-195">您可以选择包含项目预算金额的预测模型，这样可将项目预算用作源。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-195">You can use project budgets as a source by selecting the forecast model that contains the project budget amounts.</span></span> <span data-ttu-id="2bcc9-196">请记住项目预算在通过审核时创建项目预测条目。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-196">Remember that project budgets create project forecast entries as they are approved.</span></span>

<span data-ttu-id="2bcc9-197">若要只为预算计划行选择成本或收入，请使用筛选器来选择**预算更新：金额类型 = 成本**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-197">To select only costs or revenues for budget plan lines, use the filter to select **Budget updates: Amount type = Cost**.</span></span> <span data-ttu-id="2bcc9-198">若要只选择一种预测类型，则使用筛选器来选择**预算更新：交易记录类型 = *xxx***。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-198">To select only one type of forecast, use the filter to select **Budget updates: Transaction type = *xxx***.</span></span> 

<span data-ttu-id="2bcc9-199">只有一个预测模型可用于生成预算计划方案。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-199">Only one forecast model can be used to generate a budget plan scenario.</span></span> <span data-ttu-id="2bcc9-200">如果运行一个预测模型的流程，然后执行更新并尝试指定另一个模型，那么当应用相同项目和会计科目时，第一个模型将被覆盖。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-200">If you run the process for one forecast model, and then do an update and try to specify another model, the first model will be overwritten if the same project and ledger accounts apply.</span></span> <span data-ttu-id="2bcc9-201">若要从多个预测模型生成预算计划方案，请生成到不同的预算计划方案并使用分配选项将这些方案一起添加到另一个方案。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-201">To generate a budget plan scenario from more than one forecast model, generate into different budget plan scenarios, and use allocation options to add them together in another scenario.</span></span> 

<span data-ttu-id="2bcc9-202">**从项目预测生成预算计划**流程还将源项目分配到预算计划行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-202">The **Generate budget plan from project forecasts** process also assigns the source project to the budget plan line.</span></span>

### <a name="generate-budget-plan-from-supply-forecast"></a><span data-ttu-id="2bcc9-203">从供应预测生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-203">Generate budget plan from supply forecast</span></span>

<span data-ttu-id="2bcc9-204">**从供应预测生成预算计划**流程中的源筛选器选项在**将采购预算转移到分类帐**功能中的选项之后建模，因为该流程和该功能之间有相似之处。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-204">The source filter options in the **Generate budget plan from supply forecast** process were modeled after options in the **Transfer purchase budget to ledger** function, because of similarities between the process and the function.</span></span>

### <a name="generate-budget-plan-from-demand-forecast"></a><span data-ttu-id="2bcc9-205">从需求预测生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-205">Generate budget plan from demand forecast</span></span>

<span data-ttu-id="2bcc9-206">对于**从需求预测生成预算计划**流程，可以将**销售订单**选项设置为**是**以在预算计划中生成收入行，将**消耗**设置为**是**以创建支出行，或将两个选项同时设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-206">For the **Generate budget plan from demand forecast** process, you can set the **Sales order** option to **Yes** to generate revenue lines in the budget plan, set the **Consumption** to **Yes** to create expense lines, or set both options to **Yes**.</span></span>

### <a name="generate-budget-plan-from-budget-register-entries"></a><span data-ttu-id="2bcc9-207">从预算登记分录生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-207">Generate budget plan from budget register entries</span></span>

<span data-ttu-id="2bcc9-208">对于**从预算登记分录生成预算计划**流程，源必须指定一个子模型、一个预算代码和一个条目编号。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-208">For the **Generate budget plan from budget register entries** process, the source must specify one submodel, one budget code, and one entry number.</span></span> <span data-ttu-id="2bcc9-209">换言之，一次只能为一个预算登记分录创建预算计划行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-209">In other words, you can create budget plan lines for only one budget register entry at a time.</span></span> <span data-ttu-id="2bcc9-210">您可以通过为每个源条目运行一次此流程来使用相同预算计划中的其他条目。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-210">You can use additional entries in the same budget plan by running the process one time for each source entry.</span></span>

### <a name="generate-budget-plan-from-budget-plan"></a><span data-ttu-id="2bcc9-211">从预算计划生成预算计划</span><span class="sxs-lookup"><span data-stu-id="2bcc9-211">Generate budget plan from budget plan</span></span>

<span data-ttu-id="2bcc9-212">对于**从预算计划生成预算计划**流程，**目标**选项卡上的其他选项设置可以分配新的财务维度。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-212">For the **Generate budget plan from budget plan** process, an additional set of options on the **Target** tab lets you assign new financial dimensions.</span></span> <span data-ttu-id="2bcc9-213">如果选择了财务维度，则该值将为所有预算计划行使用。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-213">If a financial dimension is selected, that value will be used for all budget plan lines.</span></span> <span data-ttu-id="2bcc9-214">因此，您可以使用一个预算计划作为其他预算计划的基础，不过，还可以分配不同部门或成本中心到新预算计划（举例）。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-214">Therefore, you can use one budget plan as the basis for other budget plans, but can also assign, for example, a different department or cost center to the new budget plans.</span></span>

## <a name="looking-back-from-the-budget-plan"></a><span data-ttu-id="2bcc9-215">从预算计划回顾</span><span class="sxs-lookup"><span data-stu-id="2bcc9-215">Looking back from the budget plan</span></span>
### <a name="budget-plans-by-dimension-set-inquiry"></a><span data-ttu-id="2bcc9-216">按维度集排列的预算计划查询</span><span class="sxs-lookup"><span data-stu-id="2bcc9-216">Budget plans by dimension set inquiry</span></span>

<span data-ttu-id="2bcc9-217">**按维度集排列的预算计划**查询包括让您运行查询以帮助确定预算计划数据源的若干选项。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-217">The **Budget plans by dimension set** inquiry includes several options that let you run a query to help identify the source of the budget plan data.</span></span> 

<span data-ttu-id="2bcc9-218">选择某一行并单击**预算计划行**按钮运行**预算计划行**查询。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-218">Select a line and click the **Budget plan lines** button to run the **Budget plan lines** query.</span></span> <span data-ttu-id="2bcc9-219">结果为所选行的维度值进行筛选。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-219">The results are filtered for the dimension values of the selected line.</span></span> <span data-ttu-id="2bcc9-220">然后可以应用附加参数。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-220">You can then apply additional parameters.</span></span> 

<span data-ttu-id="2bcc9-221">使用**供应预测**和**需求预测**按钮运行这些查询。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-221">Use the **Supply forecast** and **Demand forecast** buttons run these queries.</span></span> <span data-ttu-id="2bcc9-222">在这两种情况下，查询搜索可能创建了预算计划行的预测行。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-222">In both cases, the query searches for forecast lines that could have created the budget plan lines.</span></span> 

<span data-ttu-id="2bcc9-223">其他可用的报表包括**按预算计划预测职位**报表。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-223">Additional reports that are available include the **Forecast positions by budget plan** report.</span></span> <span data-ttu-id="2bcc9-224">当您要确定职位是否正确地分配到预算计划时，此报表尤其有用。</span><span class="sxs-lookup"><span data-stu-id="2bcc9-224">This report is especially useful when you want to determine whether a position has been correctly allocated to budget plans.</span></span>




