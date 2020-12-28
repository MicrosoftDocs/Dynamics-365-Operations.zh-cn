---
title: Excel 的预算计划模板
description: 此主题描述如何创建可用于预算计划的 Microsoft Excel 模板。
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 471c719a8e6de0ebe6fcdad0ae222453db841c87
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440880"
---
# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="9a356-103">Excel 的预算计划模板</span><span class="sxs-lookup"><span data-stu-id="9a356-103">Budget planning templates for Excel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a356-104">此主题描述如何创建可用于预算计划的 Microsoft Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="9a356-105">此主题显示如何使用标准演示数据集和 Admin 用户登录创建可用于预算计划的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="9a356-106">有关预算计划的详细信息，请参阅[预算计划概览](budget-planning-overview-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="9a356-106">For more information about budget planning, see [Budget planning overview](budget-planning-overview-configuration.md).</span></span> <span data-ttu-id="9a356-107">也可以按照[预算计划](budget-plan.md)教程了解基本模块配置和使用原则。</span><span class="sxs-lookup"><span data-stu-id="9a356-107">You can also follow the [Budget planning](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="9a356-108">使用预算计划文档布局生成工作表</span><span class="sxs-lookup"><span data-stu-id="9a356-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="9a356-109">可使用一种或多种布局查看和编辑预算计划文档。</span><span class="sxs-lookup"><span data-stu-id="9a356-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="9a356-110">每种布局可以有一个关联预算计划文档模板，用于使用 Excel 工作表查看和编辑预算计划数据。</span><span class="sxs-lookup"><span data-stu-id="9a356-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="9a356-111">在此主题中，将使用现有布局配置生成预算计划文档模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="9a356-112">打开 **预算计划列表**（**预算编制** &gt; **预算计划**）。</span><span class="sxs-lookup"><span data-stu-id="9a356-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="9a356-113">单击 **新建** 创建新的预算计划文档。</span><span class="sxs-lookup"><span data-stu-id="9a356-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="9a356-114">[![预算计划列表](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="9a356-115">使用 **添加** 行选项添加行。</span><span class="sxs-lookup"><span data-stu-id="9a356-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="9a356-116">单击 **布局** 查看预算计划文档布局配置。</span><span class="sxs-lookup"><span data-stu-id="9a356-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="9a356-117">[![添加预算计划](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="9a356-118">可以检查布局配置并根据需要调整。</span><span class="sxs-lookup"><span data-stu-id="9a356-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="9a356-119">转至 **模板** &gt; **生成**，为该布局生成一个 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="9a356-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="9a356-120">生成模板之后，转至 **模板** &gt; **查看** 以打开并检查预算计划文档模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="9a356-121">可将该 Excel 文件保存到本地驱动器。</span><span class="sxs-lookup"><span data-stu-id="9a356-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="9a356-122">[![另存为](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="9a356-123">为预算计划文档布局关联 Excel 模板之后，不能编辑该布局。</span><span class="sxs-lookup"><span data-stu-id="9a356-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="9a356-124">若要修改此布局，请删除关联的 Excel 模板文件并重新生成。</span><span class="sxs-lookup"><span data-stu-id="9a356-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="9a356-125">若要让布局中的字段和工作表中的字段保持同步，需执行此操作。</span><span class="sxs-lookup"><span data-stu-id="9a356-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="9a356-126">该 Excel 模板中将包含预算计划文档模板中的所有元素，其中的 **在工作表中可用** 列设置为 True。</span><span class="sxs-lookup"><span data-stu-id="9a356-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="9a356-127">Excel 模板中不允许重叠元素。</span><span class="sxs-lookup"><span data-stu-id="9a356-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="9a356-128">例如，如果布局中包含 Request Q1、Request Q2、Request Q3 和 Request Q4 列，以及表示所有 4 个季度列总和的请求总计列，则只能在 Excel 模板中使用季度列或总计列。</span><span class="sxs-lookup"><span data-stu-id="9a356-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="9a356-129">更新期间，此 Excel 文件不能更新重叠列，因为表中的数据可能超出日期范围，因此不精确。</span><span class="sxs-lookup"><span data-stu-id="9a356-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

> [!NOTE] 
> <span data-ttu-id="9a356-130">若要避免使用 Excel 查看和编辑预算计划数据时可能出现问题，应使用相同用户登录 Microsoft Dynamics 365 Finance 和 Microsoft Dynamics Office 加载项数据连接器。</span><span class="sxs-lookup"><span data-stu-id="9a356-130">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 Finance and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="9a356-131">为预算计划文档模板添加标题</span><span class="sxs-lookup"><span data-stu-id="9a356-131">Add a header to budget plan document template</span></span>
<span data-ttu-id="9a356-132">若要添加标题信息，请选择 Excel 文件中的首行，然后插入空行。</span><span class="sxs-lookup"><span data-stu-id="9a356-132">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="9a356-133">单击 **数据连接器** 中的 **设计** 向 Excel 文件添加标题字段。</span><span class="sxs-lookup"><span data-stu-id="9a356-133">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="9a356-134">在 **设计** 选项卡中，单击 **添加** 字段，然后选择 **BudgetPlanHeader** 作为实体数据源。</span><span class="sxs-lookup"><span data-stu-id="9a356-134">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="9a356-135">将光标指向 Excel 文件中的所需位置。</span><span class="sxs-lookup"><span data-stu-id="9a356-135">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="9a356-136">单击 **添加标签** 向所选位置添加字段标签。</span><span class="sxs-lookup"><span data-stu-id="9a356-136">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="9a356-137">选择 **添加值** 向所选位置添加值字段。</span><span class="sxs-lookup"><span data-stu-id="9a356-137">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="9a356-138">单击 **确定** 关闭该设计器。</span><span class="sxs-lookup"><span data-stu-id="9a356-138">Click **Done** to close the designer.</span></span>

## <a name="select-add-valuemediabpt7png"></a><span data-ttu-id="9a356-139">[![选择“添加值”](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-139">[![Select Add Value](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="9a356-140">向预算计划文档模板表添加计算列</span><span class="sxs-lookup"><span data-stu-id="9a356-140">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="9a356-141">接下来，将把计算列添加到生成的预算计划文档模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-141">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="9a356-142">一个 **请求总计** 列，用于计算 Request Q1 到 Request Q4 列之和，以及一个 **调整** 列，用于按预定义的系数重新计算 **请求总数** 列。</span><span class="sxs-lookup"><span data-stu-id="9a356-142">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="9a356-143">单击 **数据连接器** 中的 **设计** 向表添加列。</span><span class="sxs-lookup"><span data-stu-id="9a356-143">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="9a356-144">单击 **BudgetPlanWorksheet** 数据源旁边的 **编辑** 开始添加列。</span><span class="sxs-lookup"><span data-stu-id="9a356-144">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="9a356-145">[![开始添加列](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-145">[![Start adding columns](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="9a356-146">所选字段组将显示模板中的可用列。</span><span class="sxs-lookup"><span data-stu-id="9a356-146">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="9a356-147">单击 **公式** 添加新列。</span><span class="sxs-lookup"><span data-stu-id="9a356-147">Click **Formula** to add a new column.</span></span> <span data-ttu-id="9a356-148">为新列命名，然后将公式粘贴到 **公式** 字段中。</span><span class="sxs-lookup"><span data-stu-id="9a356-148">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="9a356-149">单击 **更新** 以插入该列。</span><span class="sxs-lookup"><span data-stu-id="9a356-149">Click **Update** to insert the column.</span></span>

<span data-ttu-id="9a356-150">[![添加和插入列](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-150">[![Add and insert column](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="9a356-151">若要定义公式，请在电子表格中创建公式，然后将其复制到 **设计** 窗口中。</span><span class="sxs-lookup"><span data-stu-id="9a356-151">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="9a356-152">Finance and Operations 绑定表通常命名为“AXTable1”。</span><span class="sxs-lookup"><span data-stu-id="9a356-152">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="9a356-153">例如，若要计算电子表格中的 Request Q1 到 Request Q4 列之和，则公式 = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\]。</span><span class="sxs-lookup"><span data-stu-id="9a356-153">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="9a356-154">重复此步骤以插入 **调整** 列。</span><span class="sxs-lookup"><span data-stu-id="9a356-154">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="9a356-155">为此列使用公式 = AxTable1\[Total request\]\*$I$1。</span><span class="sxs-lookup"><span data-stu-id="9a356-155">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="9a356-156">这将提取单元格 I1 中的值并乘以 **请求总数** 列中的值，以计算调整金额。</span><span class="sxs-lookup"><span data-stu-id="9a356-156">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="9a356-157">保存然后关闭该 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="9a356-157">Save and close the Excel file.</span></span> <span data-ttu-id="9a356-158">在 **布局** 中，单击 **模板 &gt; 上传**，上传要已保存的用于预算计划的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="9a356-158">In **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="9a356-159">[![上载 Excel 模板](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-159">[![Upload Excel template](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="9a356-160">关闭 **布局** 滑块。</span><span class="sxs-lookup"><span data-stu-id="9a356-160">Close the **Layouts** slider.</span></span> <span data-ttu-id="9a356-161">在 **预算计划** 文档中，单击 **工作表**，以便在 Excel 中查看和编辑文档。</span><span class="sxs-lookup"><span data-stu-id="9a356-161">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="9a356-162">请注意，此预算计划工作表是使用调整后的 Excel 模板创建的，并使用在前面的步骤中定义的公式更新计算列。</span><span class="sxs-lookup"><span data-stu-id="9a356-162">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="9a356-163">[![在 Excel 中查看和编辑文档](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-163">[![View and edit document in Excel](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="9a356-164">有关如何创建预算计划模板的提示和技巧</span><span class="sxs-lookup"><span data-stu-id="9a356-164">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="9a356-165">是否可以为预算计划模板添加和使用更多数据源？</span><span class="sxs-lookup"><span data-stu-id="9a356-165">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="9a356-166">可以，可以使用 **设计** 菜单向 Excel 模板中的同一个或其他工作表添加更多实体。</span><span class="sxs-lookup"><span data-stu-id="9a356-166">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="9a356-167">例如，可以添加 **BudgetPlanProposedProject** 数据源，以便在 Excel 中处理预算计划数据的同时，创建和维护一列建议的项目。</span><span class="sxs-lookup"><span data-stu-id="9a356-167">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="9a356-168">请注意，包含大量数据源可能影响 Excel 工作簿的性能。</span><span class="sxs-lookup"><span data-stu-id="9a356-168">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="9a356-169">可使用 **数据连接器** 中的 **筛选器** 选项向更多数据源添加所需筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a356-169">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="9a356-170">是否可以在数据连接器中对其他用户隐藏“设计”选项？</span><span class="sxs-lookup"><span data-stu-id="9a356-170">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="9a356-171">可以，请打开 **数据连接器** 选项，以便对其他用户隐藏 **设计** 选项。</span><span class="sxs-lookup"><span data-stu-id="9a356-171">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="9a356-172">[![打开“数据连接器”选项](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-172">[![Open Data Connector options](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="9a356-173">展开 **数据连接器选项** 并清除 **启用设计** 复选框。</span><span class="sxs-lookup"><span data-stu-id="9a356-173">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="9a356-174">这将在 **数据连接器** 中隐藏 **设计** 选项。</span><span class="sxs-lookup"><span data-stu-id="9a356-174">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="9a356-175">[![在数据连接器中隐藏“设计”选项](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-175">[![Hide Design option from Data connector](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="9a356-176">是否可以阻止用户在处理数据时意外关闭数据连接器？</span><span class="sxs-lookup"><span data-stu-id="9a356-176">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="9a356-177">我们建议锁定模板，以防用户将其关闭。</span><span class="sxs-lookup"><span data-stu-id="9a356-177">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="9a356-178">若要开启锁定，请单击 **数据连接器**；将在右上角显示一个箭头。</span><span class="sxs-lookup"><span data-stu-id="9a356-178">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="9a356-179">[![开启锁定](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-179">[![Turn on the lock](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="9a356-180">单击箭头以再显示一个菜单。</span><span class="sxs-lookup"><span data-stu-id="9a356-180">Click the arrow for an additional menu.</span></span> <span data-ttu-id="9a356-181">选择 **锁定**。</span><span class="sxs-lookup"><span data-stu-id="9a356-181">Select **Lock**.</span></span>

### <a name="select-lockmediabpt16png"></a><span data-ttu-id="9a356-182">[![选择锁定](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="9a356-182">[![Select Lock](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="9a356-183">是否可以在我的预算计划模板中使用其他 Excel 功能，如单元格格式、颜色、条件格式和图表？</span><span class="sxs-lookup"><span data-stu-id="9a356-183">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="9a356-184">可以，预算计划模板中支持大多数标准的 Excel 功能。</span><span class="sxs-lookup"><span data-stu-id="9a356-184">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="9a356-185">我们建议使用颜色编码，以便用户区分只读列和可编辑列。</span><span class="sxs-lookup"><span data-stu-id="9a356-185">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="9a356-186">可使用条件格式突出显示预算的问题区域。</span><span class="sxs-lookup"><span data-stu-id="9a356-186">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="9a356-187">可通过使用标准 Excel 公式在表上方轻松表示列总计。</span><span class="sxs-lookup"><span data-stu-id="9a356-187">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="9a356-188">还可以为预算数据的更多分组和可视化创建和使用透视表和图表。</span><span class="sxs-lookup"><span data-stu-id="9a356-188">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="9a356-189">在 **数据** 选项卡上的 **连接** 组中，单击 **全部刷新**，然后单击 **连接属性**。</span><span class="sxs-lookup"><span data-stu-id="9a356-189">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="9a356-190">单击 **用法** 选项卡。在 **刷新** 下，选中 **打开文件时刷新数据** 复选框。</span><span class="sxs-lookup"><span data-stu-id="9a356-190">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 



