---
title: 网格功能
description: 本主题介绍网格控件的几个强大功能。 必须启用新的网格功能才能访问这些功能。
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0fd0e15ea88e9f5f34d8dff82606a8d26616a16d
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260452"
---
# <a name="grid-capabilities"></a><span data-ttu-id="ebcf7-104">网格功能</span><span class="sxs-lookup"><span data-stu-id="ebcf7-104">Grid capabilities</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ebcf7-105">新的网格控件提供了许多有用而强大的功能，可用于提高用户生产率、构造更有趣的数据视图并获得有意义的数据见解。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-105">The new grid control provides a number of useful and powerful capabilities that can be used to enhance user productivity, construct more interesting views of your data, and get meaningful insights into your data.</span></span> <span data-ttu-id="ebcf7-106">本文将介绍以下功能：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-106">This article will cover the following capabilities:</span></span> 

-  <span data-ttu-id="ebcf7-107">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="ebcf7-107">Calculating totals</span></span>
-  <span data-ttu-id="ebcf7-108">分组数据</span><span class="sxs-lookup"><span data-stu-id="ebcf7-108">Grouping data</span></span>
-  <span data-ttu-id="ebcf7-109">先于系统键入</span><span class="sxs-lookup"><span data-stu-id="ebcf7-109">Typing ahead of the system</span></span>
-  <span data-ttu-id="ebcf7-110">评估数学表达式</span><span class="sxs-lookup"><span data-stu-id="ebcf7-110">Evaluating math expressions</span></span> 

## <a name="calculating-totals"></a><span data-ttu-id="ebcf7-111">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="ebcf7-111">Calculating totals</span></span>
<span data-ttu-id="ebcf7-112">在 Finance and Operations 应用中，用户可以在网格中数字列的底部查看总计。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-112">In Finance and Operations apps, users have the ability to see totals at the bottom of numeric columns in grids.</span></span> <span data-ttu-id="ebcf7-113">这些总计显示在网格底部的页脚部分。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-113">These totals are shown in a footer section at the bottom of the grid.</span></span> 

### <a name="showing-the-grid-footer"></a><span data-ttu-id="ebcf7-114">显示网格页脚</span><span class="sxs-lookup"><span data-stu-id="ebcf7-114">Showing the grid footer</span></span>
<span data-ttu-id="ebcf7-115">下面是 Finance and Operations 应用中每个选项卡式网格底部的页脚区域。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-115">There is a footer area at the bottom of every tabular grid in Finance and Operations apps.</span></span> <span data-ttu-id="ebcf7-116">此页脚可显示与网格中显示的数据有关的宝贵信息。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-116">The footer can show valuable information that is related to the data that appears in the grid.</span></span> <span data-ttu-id="ebcf7-117">下面是这些信息的一些示例：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-117">Here are some examples of this information:</span></span>

- <span data-ttu-id="ebcf7-118">表中选定的行数（当选择多个记录时）</span><span class="sxs-lookup"><span data-stu-id="ebcf7-118">The number of selected rows in the table (when more than one record is selected)</span></span>
- <span data-ttu-id="ebcf7-119">已配置数字列底部的总计</span><span class="sxs-lookup"><span data-stu-id="ebcf7-119">Grand totals at the bottom of configured, numeric columns</span></span>
- <span data-ttu-id="ebcf7-120">数据集中的行数</span><span class="sxs-lookup"><span data-stu-id="ebcf7-120">The number of rows in the dataset</span></span> 

<span data-ttu-id="ebcf7-121">默认情况下，此页脚为隐藏状态，但可以轻松打开。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-121">This footer is hidden by default, but can be easily turned on.</span></span> <span data-ttu-id="ebcf7-122">要显示网格的页脚，右键单击网格中的列标题，然后选择**显示页脚**选项。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-122">To show the footer for a grid, right-click on a column header in the grid and select the **Show footer** option.</span></span> <span data-ttu-id="ebcf7-123">在为特定网格打开页脚后，该设置将被记住，直到用户选择隐藏页脚为止，可以通过右键单击列标题并选择**隐藏页脚**来隐藏。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-123">Once the footer has been turned on for a particular grid, that setting will be remembered until the user opts to hide the footer, which can be done by right-clicking on a column header and selecting **Hide footer**.</span></span>  <span data-ttu-id="ebcf7-124">请注意，**显示页脚/隐藏页脚**操作的位置预计在以后的更新中会重新放置。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-124">Note the placement of the **Show footer/Hide footer** action is expected to be re-located in a future update.</span></span> 

### <a name="specifying-columns-with-totals"></a><span data-ttu-id="ebcf7-125">指定包含总计的列</span><span class="sxs-lookup"><span data-stu-id="ebcf7-125">Specifying columns with totals</span></span>
<span data-ttu-id="ebcf7-126">当前，默认情况下，没有列会被配置为显示总计。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-126">Currently, no columns will be configured to show totals by default.</span></span> <span data-ttu-id="ebcf7-127">而是将此视为一次性设置活动，类似于调整网格中列的宽度。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-127">Instead, this is considered a one-time setup activity, similar to adjusting the widths of columns in grids.</span></span> <span data-ttu-id="ebcf7-128">指定要查看某列的总计后，该设置将在您下次访问页面时被记住。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-128">Once you specify that you want to see totals for a column, that setting will be remembered the next time you visit the page.</span></span>  

<span data-ttu-id="ebcf7-129">有两种方法可以配置列以显示总计：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-129">There are two ways to configure a column to show a total:</span></span> 

- <span data-ttu-id="ebcf7-130">在您想查看总计的列中右键单击，然后选择**计算此列总计**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-130">Right-click in the column that you want to see a total for, and then select **Total this column**.</span></span> <span data-ttu-id="ebcf7-131">此操作将导致发生三个事件：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-131">This action causes three events to occur:</span></span>

    1. <span data-ttu-id="ebcf7-132">显示页脚。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-132">The footer becomes visible.</span></span> 
    2. <span data-ttu-id="ebcf7-133">保存您查看此列总计的首选项。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-133">Your preference for seeing a total for this column is saved.</span></span> 
    3. <span data-ttu-id="ebcf7-134">将启动此列以及您之前配置为查看总计的其他任何列的总计计算。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-134">A calculation of totals is initiated for this column and any other columns that you previously configured to see totals for.</span></span> <span data-ttu-id="ebcf7-135">何时需要显示总计取决于要计算其总计的数据集的大小。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-135">The time that is required to show a total depends on the size of the dataset that you're totaling.</span></span>

- <span data-ttu-id="ebcf7-136">页脚显示后，选择要查看其总计的列底部页脚区域中的**显示总计**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-136">After the footer is visible, select **Show total** in the footer area at the bottom of the column that you want to see a total for.</span></span> <span data-ttu-id="ebcf7-137">如果没有配置的列，**显示总计**按钮将对所有数字列可用。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-137">If there are no configured columns, the **Show total** button will be available for all numeric columns.</span></span> 

    <span data-ttu-id="ebcf7-138">在为总计配置了至少一列后，**显示总计**按钮将仅在悬停或聚焦时可用。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-138">After at least one column is configured for totals, the **Show total** buttons will be available only on hover or focus.</span></span> <span data-ttu-id="ebcf7-139">选择**显示总计**这一操作仅保存有关在此列中查看总计的首选项，因此将来访问此页面时间应用此首选项。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-139">The action of selecting **Show total** just saves your preference for seeing a total in this column, so that the preference is applied during future visits to the page.</span></span> <span data-ttu-id="ebcf7-140">在页脚中，此状态由列中显示的破折号表示。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-140">In the footer, this state is indicated by a dash that appears in the column.</span></span> <span data-ttu-id="ebcf7-141">（或者，如果数据集足够小，将立即显示总计。）</span><span class="sxs-lookup"><span data-stu-id="ebcf7-141">(Alternatively, if the dataset is small enough, a total is immediately shown.)</span></span>

<span data-ttu-id="ebcf7-142">如果您输入有误，并且不想再查看特定列中的总计，右键单击该列，然后选择**隐藏总计**或选择该列页脚中的**隐藏总计**按钮。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-142">If you make a mistake and no longer want to see a total in a particular column, right-click on the column and select **Hide total** or select the **Hide total** button in the footer in that column.</span></span> <span data-ttu-id="ebcf7-143">此首选项也将被保存以供将来访问该页面时使用。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-143">This preference will also be saved for future visits to the page.</span></span> 

### <a name="calculating-totals"></a><span data-ttu-id="ebcf7-144">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="ebcf7-144">Calculating totals</span></span>
<span data-ttu-id="ebcf7-145">当您进入页脚可见且已为总计配置了列的页面时，总计可能会显示在页脚中，也可能不会显示。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-145">When you come to a page with the footer visible and columns already configured for totals, totals may or may not be shown in the footer.</span></span> <span data-ttu-id="ebcf7-146">此行为取决于页面上数据集的大小。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-146">The behavior is dependent on the size of the dataset on the page.</span></span> <span data-ttu-id="ebcf7-147">如果数据集足够小，则会自动显示总计以及数据集中的行数。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-147">If the dataset is sufficiently small, totals will be shown automatically, along with the number of rows in the dataset.</span></span> <span data-ttu-id="ebcf7-148">如果您在为总计配置的列下的页脚中有破折号，则说明数据集太大，系统无法立即显示总计，因此需要执行明确操作来计算总计。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-148">If there are dashes in the footer under the columns you configured for totals, then the dataset is too large for the system to show totals immediately, and an explicit action is needed to calculate the totals.</span></span> <span data-ttu-id="ebcf7-149">若要执行此操作，单击页脚中的**计算**按钮，或右键单击要计算总计的列，然后选择**计算此列总计**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-149">To do this, click the **Calculate** button in the footer, or right-click on a column you want a total for and select **Total this column**.</span></span>  

<span data-ttu-id="ebcf7-150">如果计算时间过长，可以选择**取消**按钮取消运算。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-150">If the calculation is taking too long, you can cancel the operation by selecting the **Cancel** button.</span></span> <span data-ttu-id="ebcf7-151">但是，有时数据集太大而无法计算总数（组织施加的限制），而是会通知您进一步筛选数据。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-151">Sometimes, however, the dataset will be too large to calculate totals (a limit imposed by your organization), and you will instead be notified to filter your data more.</span></span>

<span data-ttu-id="ebcf7-152">总计将在您更新、删除或创建数据集中的行时自动更新。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-152">Totals will update automatically as you update, delete, or create rows in the dataset.</span></span>  

## <a name="grouping-data"></a><span data-ttu-id="ebcf7-153">分组数据</span><span class="sxs-lookup"><span data-stu-id="ebcf7-153">Grouping data</span></span>
<span data-ttu-id="ebcf7-154">业务用户通常需要执行专门的数据分析。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-154">Business users often need to perform ad-hoc analysis of data.</span></span> <span data-ttu-id="ebcf7-155">尽管可以通过将数据导出到 Microsoft Excel 并使用数据透视表来完成此操作，但表格式网格中的**分组**功能允许用户在 Finance and Operations 应用中以有趣的方式组织其数据。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-155">While this can be done by exporting data to Microsoft Excel and using pivot tables, the **Grouping** capability in tabular grids allows users to organize their data in interesting ways within Finance and Operations apps.</span></span> <span data-ttu-id="ebcf7-156">随着此功能扩展**总计**功能，**分组**还允许您通过在组级别提供小计来获得有意义的数据见解。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-156">As this feature extends the **Totals** feature, **Grouping** also allows you to get meaningful insights into the data by providing subtotals at the group level.</span></span>

<span data-ttu-id="ebcf7-157">要使用此功能，右键单击分组所基于的列，然后选择**按此列分组**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-157">To use this feature, right-click on the column you wish to group by, and select **Group by this column**.</span></span> <span data-ttu-id="ebcf7-158">此操作将按所选列对数据进行排序，将新的“按列分组”添加到网格的开头，并在每个组的开头插入“标题行”。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-158">This action will sort the data by the selected column, add a new Group by column to the beginning to the grid, and insert "header rows" at the beginning of each group.</span></span> <span data-ttu-id="ebcf7-159">这些标题行提供有关每个组的以下信息：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-159">These header rows provide the following information about each group:</span></span> 
-  <span data-ttu-id="ebcf7-160">组的数据值</span><span class="sxs-lookup"><span data-stu-id="ebcf7-160">Data value for the group</span></span> 
-  <span data-ttu-id="ebcf7-161">列标签（在支持多级分组之后，此信息特别有用。）</span><span class="sxs-lookup"><span data-stu-id="ebcf7-161">Column label (This information will be especially useful after multiple levels of grouping are supported.)</span></span>
-  <span data-ttu-id="ebcf7-162">该组中的数据行数</span><span class="sxs-lookup"><span data-stu-id="ebcf7-162">Number of data rows in this group</span></span>
-  <span data-ttu-id="ebcf7-163">配置为显示总计的所有列的小计</span><span class="sxs-lookup"><span data-stu-id="ebcf7-163">Subtotals for any column configured to show totals</span></span>

<span data-ttu-id="ebcf7-164">启用[保存的视图](saved-views.md)后，可以通过个性化将分组保存为视图的一部分，以便下次访问页面时快速访问。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-164">With [Saved views](saved-views.md) enabled, this grouping can be saved by personalization as part of a view for quick access the next time you visit the page.</span></span>  

<span data-ttu-id="ebcf7-165">如果您选择另一列的**按此列分组**，原始分组将被替换，因为带平台更新 33 的版本 10.0.9 仅支持一级分组。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-165">If you select **Group by this column** for a different column, the original grouping is replaced, because only one level of grouping is supported in version 10.0.9 with Platform update 33.</span></span>

<span data-ttu-id="ebcf7-166">要撤消网格中的分组，右键单击分组列，然后选择**取消分组**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-166">To undo grouping in a grid, right-click on the grouping column and select **Ungroup**.</span></span>  


## <a name="evaluating-math-expressions"></a><span data-ttu-id="ebcf7-167">评估数学表达式</span><span class="sxs-lookup"><span data-stu-id="ebcf7-167">Evaluating math expressions</span></span>
<span data-ttu-id="ebcf7-168">随着生产力的迅速提高，用户可以在网格中的数值列内输入数学公式。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-168">As a productivity booster, users can enter mathematical formulas in numeric cells in a grid.</span></span> <span data-ttu-id="ebcf7-169">不必在系统外的应用内进行计算。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-169">They don't have to do the calculation in an app outside the system.</span></span> <span data-ttu-id="ebcf7-170">例如，如果输入 **=15\*4**，然后按 **Tab** 键离开字段，系统将计算该表达式，并保存该字段的值 **60**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-170">For example, if you enter **=15\*4** and then press the **Tab** key to move out of the field, the system will evaluate the expression and save a value of **60** for the field.</span></span>

<span data-ttu-id="ebcf7-171">要使系统将值识别为表达式，请将值以等号 (**=**) 开头。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-171">To make the system recognize a value as an expression, start the value with an equal sign (**=**).</span></span> <span data-ttu-id="ebcf7-172">有关受支持的运算符和语法的详细信息，请参阅[支持的数学符号](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols)。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-172">For more information about the supported operators and syntax, see [Supported math symbols](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ebcf7-173">常见问题</span><span class="sxs-lookup"><span data-stu-id="ebcf7-173">Frequently asked questions</span></span>
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a><span data-ttu-id="ebcf7-174">如何在我的环境中启用新的网格控件？</span><span class="sxs-lookup"><span data-stu-id="ebcf7-174">How do I enable the new grid control in my environment?</span></span> 

<span data-ttu-id="ebcf7-175">**10.0.9/平台更新 33 及更高版本** 在任何环境中，**新网格控件**功能均可直接在功能管理中使用。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-175">**10.0.9 / Platform update 33 and later** The **New grid control** feature is available directly in Feature management in any environment.</span></span> <span data-ttu-id="ebcf7-176">与其他公共预览功能一样，在生产环境中启用此功能取决于[补充使用条款协议](https://go.microsoft.com/fwlink/?linkid=2105274)。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-176">Like other public preview features, enabling this feature in production is subject to the [Supplemental Terms of Use Agreement](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>  

<span data-ttu-id="ebcf7-177">**10.0.8/平台更新 32 及 10.0.7/平台更新 31** 可以在第 1 层（开发/测试）和第 2 层（沙盒）环境中启用**新网格控件**功能，以便按照以下步骤进行其他测试和设计更改。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-177">**10.0.8 / Platform update 32 and 10.0.7 / Platform update 31** The **New grid control** feature can be enabled in Tier 1 (Dev/Test) and Tier 2 (Sandbox) environments in order to provide additional testing and design changes by following the steps below.</span></span>

1.  <span data-ttu-id="ebcf7-178">**启用外部测试版**：执行以下 SQL 语句：</span><span class="sxs-lookup"><span data-stu-id="ebcf7-178">**Enable the flight**: Execute the following SQL statement:</span></span> 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. <span data-ttu-id="ebcf7-179">**重置 IIS**，用于清空静态外部测试缓存。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-179">**Reset IIS** to flush the static flighting cache.</span></span> 

3.  <span data-ttu-id="ebcf7-180">**查找功能**：转到**功能管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-180">**Find the feature**: Go to the **Feature management** workspace.</span></span> <span data-ttu-id="ebcf7-181">如果所有功能列表中不显示**新网格控件**，请选择**检查更新**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-181">If **New grid control** does not appear in the list of all features, select **Check for updates**.</span></span>   

4.  <span data-ttu-id="ebcf7-182">**启用功能**：在功能列表中找到**新网格控件**功能，然后选择详细信息窗格上的**立即启用**。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-182">**Enable the feature**: Find the **New grid control** feature in the list of features, and select **Enable now** on the details pane.</span></span> <span data-ttu-id="ebcf7-183">请注意，必须刷新浏览器。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-183">Note that a browser refresh is required.</span></span> 

<span data-ttu-id="ebcf7-184">所有后续用户会话都将从启用新网格控件开始。</span><span class="sxs-lookup"><span data-stu-id="ebcf7-184">All subsequent user sessions will start with the new grid control enabled.</span></span>
