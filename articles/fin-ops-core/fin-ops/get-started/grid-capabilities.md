---
title: 网格功能
description: 本主题介绍网格控件的几个强大功能。 必须启用新的网格功能才能访问这些功能。
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019651"
---
# <a name="grid-capabilites"></a><span data-ttu-id="0996f-104">网格功能</span><span class="sxs-lookup"><span data-stu-id="0996f-104">Grid capabilites</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0996f-105">新的网格控件提供了许多有用而强大的功能，可用于提高用户生产率、构造更有趣的数据视图并获得有意义的数据见解。</span><span class="sxs-lookup"><span data-stu-id="0996f-105">The new grid control provides a number of useful and powerful capabilities that can be used to enhance user productivity, construct more interesting views of your data, and get meaningful insights into your data.</span></span> <span data-ttu-id="0996f-106">本文将介绍以下功能：</span><span class="sxs-lookup"><span data-stu-id="0996f-106">This article will cover the following capabilities:</span></span> 

-  <span data-ttu-id="0996f-107">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="0996f-107">Calculating totals</span></span>
-  <span data-ttu-id="0996f-108">分组数据</span><span class="sxs-lookup"><span data-stu-id="0996f-108">Grouping data</span></span>
-  <span data-ttu-id="0996f-109">先于系统键入</span><span class="sxs-lookup"><span data-stu-id="0996f-109">Typing ahead of the system</span></span>
-  <span data-ttu-id="0996f-110">评估数学表达式</span><span class="sxs-lookup"><span data-stu-id="0996f-110">Evaluating math expressions</span></span> 

## <a name="calculating-totals"></a><span data-ttu-id="0996f-111">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="0996f-111">Calculating totals</span></span>
<span data-ttu-id="0996f-112">在 Finance and Operations 应用中，用户可以在网格中数字列的底部查看总计。</span><span class="sxs-lookup"><span data-stu-id="0996f-112">In Finance and Operations apps, users have the ability to see totals at the bottom of numeric columns in grids.</span></span> <span data-ttu-id="0996f-113">这些总计显示在网格底部的页脚部分。</span><span class="sxs-lookup"><span data-stu-id="0996f-113">These totals are shown in a footer section at the bottom of the grid.</span></span> 

### <a name="showing-the-grid-footer"></a><span data-ttu-id="0996f-114">显示网格页脚</span><span class="sxs-lookup"><span data-stu-id="0996f-114">Showing the grid footer</span></span>
<span data-ttu-id="0996f-115">Finance and Operations 应用中的每个表格式网格在其底部都有一个页脚区域，可以显示与所显示数据相关的有价值信息。</span><span class="sxs-lookup"><span data-stu-id="0996f-115">Every tabular grid in the Finance and Operations apps has a footer area at the bottom of the grid that can show valuable information related to the data being displayed.</span></span> <span data-ttu-id="0996f-116">这些信息包括：</span><span class="sxs-lookup"><span data-stu-id="0996f-116">This information includes:</span></span> 
-  <span data-ttu-id="0996f-117">表中选定的行数（当选择多个记录时）</span><span class="sxs-lookup"><span data-stu-id="0996f-117">The number of selected rows in the table (when more than one record is selected)</span></span>
-  <span data-ttu-id="0996f-118">已配置数字列底部的总计</span><span class="sxs-lookup"><span data-stu-id="0996f-118">Grand totals at the bottom of configured numeric columns</span></span>
-  <span data-ttu-id="0996f-119">数据集中的行数</span><span class="sxs-lookup"><span data-stu-id="0996f-119">The number of rows in the dataset</span></span> 

<span data-ttu-id="0996f-120">默认情况下，此页脚为隐藏状态，但可以轻松打开。</span><span class="sxs-lookup"><span data-stu-id="0996f-120">This footer is hidden by default, but can be easily turned on.</span></span> <span data-ttu-id="0996f-121">要显示网格的页脚，右键单击网格中的列标题，然后选择**显示页脚**选项。</span><span class="sxs-lookup"><span data-stu-id="0996f-121">To show the footer for a grid, right-click on a column header in the grid and select the **Show footer** option.</span></span> <span data-ttu-id="0996f-122">在为特定网格打开页脚后，该设置将被记住，直到用户选择隐藏页脚为止，可以通过右键单击列标题并选择**隐藏页脚**来隐藏。</span><span class="sxs-lookup"><span data-stu-id="0996f-122">Once the footer has been turned on for a particular grid, that setting will be remembered until the user opts to hide the footer, which can be done by right-clicking on a column header and selecting **Hide footer**.</span></span>  <span data-ttu-id="0996f-123">请注意，**显示页脚/隐藏页脚**操作的位置预计在以后的更新中会重新放置。</span><span class="sxs-lookup"><span data-stu-id="0996f-123">Note the placement of the **Show footer/Hide footer** action is expected to be re-located in a future update.</span></span> 

### <a name="specifying-columns-with-totals"></a><span data-ttu-id="0996f-124">指定包含总计的列</span><span class="sxs-lookup"><span data-stu-id="0996f-124">Specifying columns with totals</span></span>
<span data-ttu-id="0996f-125">当前，默认情况下，没有列会被配置为显示总计。</span><span class="sxs-lookup"><span data-stu-id="0996f-125">Currently, no columns will be configured to show totals by default.</span></span> <span data-ttu-id="0996f-126">而是将此视为一次性设置活动，类似于调整网格中列的宽度。</span><span class="sxs-lookup"><span data-stu-id="0996f-126">Instead, this is considered a one-time setup activity, similar to adjusting the widths of columns in grids.</span></span> <span data-ttu-id="0996f-127">指定要查看某列的总计后，该设置将在您下次访问页面时被记住。</span><span class="sxs-lookup"><span data-stu-id="0996f-127">Once you specify that you want to see totals for a column, that setting will be remembered the next time you visit the page.</span></span>  

<span data-ttu-id="0996f-128">有两种方法可以配置列以显示总计：</span><span class="sxs-lookup"><span data-stu-id="0996f-128">There are two ways to configure a column to show a total:</span></span> 
1.  <span data-ttu-id="0996f-129">右键单击您想查看总计的列，然后选择**计算此列总计**。</span><span class="sxs-lookup"><span data-stu-id="0996f-129">Right-click on the column you are interested in seeing a total for and select **Total this column**.</span></span> <span data-ttu-id="0996f-130">此操作将完成三件事。</span><span class="sxs-lookup"><span data-stu-id="0996f-130">This action will do three things.</span></span> <span data-ttu-id="0996f-131">首先，将使页脚可见。</span><span class="sxs-lookup"><span data-stu-id="0996f-131">First, it will make the footer visible.</span></span> <span data-ttu-id="0996f-132">其次，将保存您在此列上查看总计的首选项。</span><span class="sxs-lookup"><span data-stu-id="0996f-132">Second, it will save your preference for seeing a total on this column.</span></span> <span data-ttu-id="0996f-133">第三，此操作将启动此列以及您之前配置为查看总计的其他任何列的总计计算。</span><span class="sxs-lookup"><span data-stu-id="0996f-133">Third, this action will initiate a totals calculation for this column and any others you’ve previously configured to see totals.</span></span> <span data-ttu-id="0996f-134">显示总计所需的时间与您要计算总计的数据集的大小直接相关。</span><span class="sxs-lookup"><span data-stu-id="0996f-134">The time it takes for a total to be shown is directly related to the size of the dataset you are totalling.</span></span>  

2.  <span data-ttu-id="0996f-135">显示页脚后，您也可以在您希望查看总计的列底部的页脚区域中单击**显示总计**按钮。</span><span class="sxs-lookup"><span data-stu-id="0996f-135">Once the footer has been shown, you can alternatively click on the **Show total** button in the footer region at the bottom of the column you are interested in seeing a total for.</span></span> <span data-ttu-id="0996f-136">如果没有配置的列，**显示总计**按钮将对所有数字列可见。</span><span class="sxs-lookup"><span data-stu-id="0996f-136">If there are no configured columns, then the **Show total** button will be visible for all numeric columns.</span></span> <span data-ttu-id="0996f-137">在为总计配置了至少一列后，**显示总计**按钮将仅在悬停或聚焦时可用。</span><span class="sxs-lookup"><span data-stu-id="0996f-137">Once there is at least one column configured for totals, the **Show total** buttons will only be available on hover or focus.</span></span> <span data-ttu-id="0996f-138">此操作只是保存您的首选项，以便在以后访问此页面时在此列中查看总计，此状态由页脚中此列中出现的破折号指示（如果数据集足够小，总计将立即显示）。</span><span class="sxs-lookup"><span data-stu-id="0996f-138">This action simply saves your preference for seeing a total in this column for future visits to this page, and this state is indicated by the dash that appears in this column in the footer (or a total will show immediately if the dataset is sufficiently small).</span></span>

<span data-ttu-id="0996f-139">如果您输入有误，并且不想再查看特定列中的总计，右键单击该列，然后选择**隐藏总计**或选择该列页脚中的**隐藏总计**按钮。</span><span class="sxs-lookup"><span data-stu-id="0996f-139">If you make a mistake and no longer want to see a total in a particular column, right-click on the column and select **Hide total** or select the **Hide total** button in the footer in that column.</span></span> <span data-ttu-id="0996f-140">此首选项也将被保存以供将来访问该页面时使用。</span><span class="sxs-lookup"><span data-stu-id="0996f-140">This preference will also be saved for future visits to the page.</span></span> 

### <a name="calculating-totals"></a><span data-ttu-id="0996f-141">正在计算合计</span><span class="sxs-lookup"><span data-stu-id="0996f-141">Calculating totals</span></span>
<span data-ttu-id="0996f-142">当您进入页脚可见且已为总计配置了列的页面时，总计可能会显示在页脚中，也可能不会显示。</span><span class="sxs-lookup"><span data-stu-id="0996f-142">When you come to a page with the footer visible and columns already configured for totals, totals may or may not be shown in the footer.</span></span> <span data-ttu-id="0996f-143">此行为取决于页面上数据集的大小。</span><span class="sxs-lookup"><span data-stu-id="0996f-143">The behavior is dependent on the size of the dataset on the page.</span></span> <span data-ttu-id="0996f-144">如果数据集足够小，则会自动显示总计以及数据集中的行数。</span><span class="sxs-lookup"><span data-stu-id="0996f-144">If the dataset is sufficiently small, totals will be shown automatically, along with the number of rows in the dataset.</span></span> <span data-ttu-id="0996f-145">如果您在为总计配置的列下的页脚中有破折号，则说明数据集太大，系统无法立即显示总计，因此需要执行明确操作来计算总计。</span><span class="sxs-lookup"><span data-stu-id="0996f-145">If there are dashes in the footer under the columns you configured for totals, then the dataset is too large for the system to show totals immediately, and an explicit action is needed to calculate the totals.</span></span> <span data-ttu-id="0996f-146">若要执行此操作，单击页脚中的**计算**按钮，或右键单击要计算总计的列，然后选择**计算此列总计**。</span><span class="sxs-lookup"><span data-stu-id="0996f-146">To do this, click the **Calculate** button in the footer, or right-click on a column you want a total for and select **Total this column**.</span></span>  

<span data-ttu-id="0996f-147">如果计算时间过长，可以选择**取消**按钮取消运算。</span><span class="sxs-lookup"><span data-stu-id="0996f-147">If the calculation is taking too long, you can cancel the operation by selecting the **Cancel** button.</span></span> <span data-ttu-id="0996f-148">但是，有时数据集太大而无法计算总数（组织施加的限制），而是会通知您进一步筛选数据。</span><span class="sxs-lookup"><span data-stu-id="0996f-148">Sometimes, however, the dataset will be too large to calculate totals (a limit imposed by your organization), and you will instead be notified to filter your data more.</span></span>

<span data-ttu-id="0996f-149">总计将在您更新、删除或创建数据集中的行时自动更新。</span><span class="sxs-lookup"><span data-stu-id="0996f-149">Totals will update automatically as you update, delete, or create rows in the dataset.</span></span>  

## <a name="grouping-data"></a><span data-ttu-id="0996f-150">分组数据</span><span class="sxs-lookup"><span data-stu-id="0996f-150">Grouping data</span></span>
<span data-ttu-id="0996f-151">业务用户通常需要执行专门的数据分析。</span><span class="sxs-lookup"><span data-stu-id="0996f-151">Business users often need to perform ad-hoc analysis of data.</span></span> <span data-ttu-id="0996f-152">尽管可以通过将数据导出到 Microsoft Excel 并使用数据透视表来完成此操作，但表格式网格中的**分组**功能允许用户在 Finance and Operations 应用中以有趣的方式组织其数据。</span><span class="sxs-lookup"><span data-stu-id="0996f-152">While this can be done by exporting data to Microsoft Excel and using pivot tables, the **Grouping** capability in tabular grids allows users to organize their data in interesting ways within Finance and Operations apps.</span></span> <span data-ttu-id="0996f-153">随着此功能扩展**总计**功能，**分组**还允许您通过在组级别提供小计来获得有意义的数据见解。</span><span class="sxs-lookup"><span data-stu-id="0996f-153">As this feature extends the **Totals** feature, **Grouping** also allows you to get meaningful insights into the data by providing subtotals at the group level.</span></span>

<span data-ttu-id="0996f-154">要使用此功能，右键单击分组所基于的列，然后选择**按此列分组**。</span><span class="sxs-lookup"><span data-stu-id="0996f-154">To use this feature, right-click on the column you wish to group by, and select **Group by this column**.</span></span> <span data-ttu-id="0996f-155">此操作将按所选列对数据进行排序，将新的“按列分组”添加到网格的开头，并在每个组的开头插入“标题行”。</span><span class="sxs-lookup"><span data-stu-id="0996f-155">This action will sort the data by the selected column, add a new Group by column to the beginning to the grid, and insert “header rows” at the beginning of each group.</span></span> <span data-ttu-id="0996f-156">这些标题行提供有关每个组的以下信息：</span><span class="sxs-lookup"><span data-stu-id="0996f-156">These header rows provide the following information about each group:</span></span> 
-  <span data-ttu-id="0996f-157">组的数据值</span><span class="sxs-lookup"><span data-stu-id="0996f-157">Data value for the group</span></span> 
-  <span data-ttu-id="0996f-158">列标签。</span><span class="sxs-lookup"><span data-stu-id="0996f-158">Column label.</span></span> <span data-ttu-id="0996f-159">在支持多级分组后，这会特别有用。</span><span class="sxs-lookup"><span data-stu-id="0996f-159">This will be particularly useful once multiple levels of grouping is supported.</span></span>  
-  <span data-ttu-id="0996f-160">该组中的数据行数</span><span class="sxs-lookup"><span data-stu-id="0996f-160">Number of data rows in this group</span></span>
-  <span data-ttu-id="0996f-161">配置为显示总计的所有列的小计</span><span class="sxs-lookup"><span data-stu-id="0996f-161">Subtotals for any column configured to show totals</span></span>

<span data-ttu-id="0996f-162">启用[保存的视图](saved-views.md)后，可以通过个性化将分组保存为视图的一部分，以便下次访问页面时快速访问。</span><span class="sxs-lookup"><span data-stu-id="0996f-162">With [Saved views](saved-views.md) enabled, this grouping can be saved by personalization as part of a view for quick access the next time you visit the page.</span></span>  

<span data-ttu-id="0996f-163">如果您在另一列上选择**按此列分组**，原始分组将被替换，因为 10.0.9/平台更新 33 仅支持分组级别。</span><span class="sxs-lookup"><span data-stu-id="0996f-163">If you select **Group by this column** on a different column, the original grouping will be replaced, as only level of grouping is supported in 10.0.9 / Platform update 33.</span></span>

<span data-ttu-id="0996f-164">要撤消网格中的分组，右键单击分组列，然后选择**取消分组**。</span><span class="sxs-lookup"><span data-stu-id="0996f-164">To undo grouping in a grid, right-click on the grouping column and select **Ungroup**.</span></span>  


## <a name="evaluating-math-expressions"></a><span data-ttu-id="0996f-165">评估数学表达式</span><span class="sxs-lookup"><span data-stu-id="0996f-165">Evaluating math expressions</span></span>
<span data-ttu-id="0996f-166">作为提高工作效率的工具，用户可以在网格内的数字单元格中输入数学公式，而不必在系统外部的应用中进行计算。</span><span class="sxs-lookup"><span data-stu-id="0996f-166">As a productivity booster, user can enter mathematical formulae into numeric cells in a grid, instead of having to do the calculation in an app outside the system.</span></span> <span data-ttu-id="0996f-167">例如，您可以输入 **=15\*4** 并离开该字段。</span><span class="sxs-lookup"><span data-stu-id="0996f-167">For example, you can enter **=15\*4** and tab out of the field.</span></span> <span data-ttu-id="0996f-168">系统将评估表达式并为该字段保存值“60”。</span><span class="sxs-lookup"><span data-stu-id="0996f-168">The system will evaluate the expression and save a value of “60” for the field.</span></span>

<span data-ttu-id="0996f-169">要使系统将值识别为表达式，请将值以等号 (**=**) 开头。</span><span class="sxs-lookup"><span data-stu-id="0996f-169">To make the system recognize a value as an expression, start the value with an equal sign (**=**).</span></span> <span data-ttu-id="0996f-170">有关受支持的运算符和语法的更多详细信息，请参阅[支持的数学符号](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols)。</span><span class="sxs-lookup"><span data-stu-id="0996f-170">For more details on the supported operators and syntax, see [Supported math symbols](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).</span></span>  
