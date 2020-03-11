---
title: 比较物料价格存储报表
description: 了解如何生成比较物料价格存储报表，然后浏览和/或导出结果。
author: AndersGirke
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 80e376db3616af27d94ee55480cd2f56441db93b
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2020
ms.locfileid: "3072107"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="64cba-103">比较物料价格存储报表</span><span class="sxs-lookup"><span data-stu-id="64cba-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64cba-104">本主题说明如何运行**比较物料价格存储**报表并以数字方式提供输出，可以是 Dynamics 365 Supply Chain Management 中的交互式页面，也可以是多种格式中任何一种的导出文档。</span><span class="sxs-lookup"><span data-stu-id="64cba-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="64cba-105">在浏览器中查看此报表时，将根据配置的布局动态调整列和聚合余额。</span><span class="sxs-lookup"><span data-stu-id="64cba-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="64cba-106">可以对结果排序，进行过滤，以及向下钻取到数据中，等等。</span><span class="sxs-lookup"><span data-stu-id="64cba-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="64cba-107">报告结果存储在**比较物料价格**数据实体中，可用于过滤结果并将其导出为 CSV 或 Microsoft Excel 之类格式。</span><span class="sxs-lookup"><span data-stu-id="64cba-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="64cba-108">如果输出中包含多行，**比较物料价格存储**报表非常有用。</span><span class="sxs-lookup"><span data-stu-id="64cba-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="64cba-109">例如，如果成本计算版本中有 40,000 个以上的物料的物料价格未决，则输出将包含多行。</span><span class="sxs-lookup"><span data-stu-id="64cba-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="64cba-110">启用比较物料价格存储</span><span class="sxs-lookup"><span data-stu-id="64cba-110">Enable compare item prices storage</span></span>

<span data-ttu-id="64cba-111">此功能只有在系统中启用了之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="64cba-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="64cba-112">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态，并在需要时启用。</span><span class="sxs-lookup"><span data-stu-id="64cba-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="64cba-113">此功能在此处列出为：</span><span class="sxs-lookup"><span data-stu-id="64cba-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="64cba-114">**模块** - 成本管理</span><span class="sxs-lookup"><span data-stu-id="64cba-114">**Module** - Cost management</span></span>
- <span data-ttu-id="64cba-115">**功能名称** - 比较物料价格存储</span><span class="sxs-lookup"><span data-stu-id="64cba-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="64cba-116">生成比较物料价格存储报表</span><span class="sxs-lookup"><span data-stu-id="64cba-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="64cba-117">请执行以下步骤生成并存储**比较物料价格存储**报表：</span><span class="sxs-lookup"><span data-stu-id="64cba-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="64cba-118">转到**成本管理 > 查询和报表 > 预先确定的成本报表 > 比较物料价格存储**。</span><span class="sxs-lookup"><span data-stu-id="64cba-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="64cba-119">选择**新建**打开**比较物料价格**窗格。</span><span class="sxs-lookup"><span data-stu-id="64cba-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="64cba-120">设置以下选项以定义要在报表中比较的价格：</span><span class="sxs-lookup"><span data-stu-id="64cba-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="64cba-121">在**参数**快速选项卡上，为报表提供唯一**名称**，并使用**要比较的未决价格**和**用于比较的价格**部分中的字段定义要比较的价格和日期。</span><span class="sxs-lookup"><span data-stu-id="64cba-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="64cba-122">在**要包括的记录**快速选项卡上，设置筛选器和约束以定义要在报表中包括的数据。</span><span class="sxs-lookup"><span data-stu-id="64cba-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="64cba-123">在**在后台运行**快速选项卡上，设置报表的生成方式、时间和频率。</span><span class="sxs-lookup"><span data-stu-id="64cba-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="64cba-124">此报告始终作为批处理作业的一部分执行。</span><span class="sxs-lookup"><span data-stu-id="64cba-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="64cba-125">选择**确定**应用设置并关闭窗格。</span><span class="sxs-lookup"><span data-stu-id="64cba-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="64cba-126">批处理作业完成后，它将列在**比较物料价格存储**页中。</span><span class="sxs-lookup"><span data-stu-id="64cba-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="64cba-127">您可能需要刷新页面才能查看此报表。</span><span class="sxs-lookup"><span data-stu-id="64cba-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="64cba-128">浏览比较物料价格存储报表</span><span class="sxs-lookup"><span data-stu-id="64cba-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="64cba-129">生成报表后，随时可以查看和浏览报表，如下所示：</span><span class="sxs-lookup"><span data-stu-id="64cba-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="64cba-130">转到**成本管理 > 查询和报表 > 预先确定的成本报表 > 比较物料价格存储**。</span><span class="sxs-lookup"><span data-stu-id="64cba-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="64cba-131">从列表中选择报表。</span><span class="sxs-lookup"><span data-stu-id="64cba-131">Select a report from the list.</span></span>

1. <span data-ttu-id="64cba-132">执行以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="64cba-132">Do one of the following:</span></span>

    - <span data-ttu-id="64cba-133">选择**概览**获取报表结果的概览。</span><span class="sxs-lookup"><span data-stu-id="64cba-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="64cba-134">选择**查看详细信息**获取更详细的报表视图</span><span class="sxs-lookup"><span data-stu-id="64cba-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="64cba-135">所选视图打开之后，可执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="64cba-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="64cba-136">选择几乎任何标题以按照该列中的值对表进行排序或筛选，就像在 Supply Chain Management 中对大多数标准窗体的处理一样。</span><span class="sxs-lookup"><span data-stu-id="64cba-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="64cba-137">请注意，不能对**单价净额变化百分比**列进行排序或筛选，因为这是计算字段。</span><span class="sxs-lookup"><span data-stu-id="64cba-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="64cba-138">选择**维度显示**打开一个窗格，可在其中选择窗体中要包含哪些维度列。</span><span class="sxs-lookup"><span data-stu-id="64cba-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="64cba-139">如果要保存这些设置，以便保留到下次打开报表时，请将**保存设置**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="64cba-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="64cba-140">选择**确定**应用设置并关闭。</span><span class="sxs-lookup"><span data-stu-id="64cba-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="64cba-141">选择窗体中的任何行，然后选择**查看详细信息**查看有关所选物料的详细信息。</span><span class="sxs-lookup"><span data-stu-id="64cba-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="64cba-142">您将可以从此处向下钻取到数据。</span><span class="sxs-lookup"><span data-stu-id="64cba-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="64cba-143">选择窗体中的任何行，然后选择**查看对比图**查看结果的交互式图形表示，因为它们与您的所选物料有关。</span><span class="sxs-lookup"><span data-stu-id="64cba-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="64cba-144">可以通过选择图表中的各种图形元素和图例浏览这些结果。</span><span class="sxs-lookup"><span data-stu-id="64cba-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="64cba-145">选择窗体中的任何行，然后选择**查看计算详细信息**查看有关与所选物料相关的计算的详细信息。</span><span class="sxs-lookup"><span data-stu-id="64cba-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="64cba-146">您将可以从此处向下钻取到数据。</span><span class="sxs-lookup"><span data-stu-id="64cba-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="64cba-147">导出比较物料价格存储报表</span><span class="sxs-lookup"><span data-stu-id="64cba-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="64cba-148">生成的所有报表都存储在**比较物料价格**数据实体中。</span><span class="sxs-lookup"><span data-stu-id="64cba-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="64cba-149">可使用 Supply Chain Management 的标准数据管理功能将此实体中的数据导出到任何支持的数据格式，包括 CSV 或 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="64cba-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="64cba-150">下面是如何导出**比较物料价格存储**报表的示例：</span><span class="sxs-lookup"><span data-stu-id="64cba-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="64cba-151">转到**系统管理 > 工作区 > 数据管理**。</span><span class="sxs-lookup"><span data-stu-id="64cba-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="64cba-152">选择**数据管理**部分中的**导出**按钮。</span><span class="sxs-lookup"><span data-stu-id="64cba-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="64cba-153">将打开**导出**页面，用于设置导出作业。</span><span class="sxs-lookup"><span data-stu-id="64cba-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="64cba-154">首先为作业提供**组名称**。</span><span class="sxs-lookup"><span data-stu-id="64cba-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="64cba-155">在**选定实体**部分中，选择**添加实体**打开一个对话框，可在其中设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="64cba-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="64cba-156">**实体名称** - 选择**比较物料价格**。</span><span class="sxs-lookup"><span data-stu-id="64cba-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="64cba-157">**目标数据格式** - 选择要导出到的格式。</span><span class="sxs-lookup"><span data-stu-id="64cba-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="64cba-158">选择**添加**添加新行，然后选择**关闭**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="64cba-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="64cba-159">通常一次导出一个报表。</span><span class="sxs-lookup"><span data-stu-id="64cba-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="64cba-160">方法是，为刚才添加到**查询**窗格中的行设置**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="64cba-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="64cba-161">这样就可以定义导出中要包含**比较物料价格**实体中的哪些报表。</span><span class="sxs-lookup"><span data-stu-id="64cba-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="64cba-162">设置以下筛选选项以导出单个报表：</span><span class="sxs-lookup"><span data-stu-id="64cba-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="64cba-163">在**范围**选项卡中，选择**添加**添加新行。</span><span class="sxs-lookup"><span data-stu-id="64cba-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="64cba-164">将**表**设置为**比较物料价格**。</span><span class="sxs-lookup"><span data-stu-id="64cba-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="64cba-165">将**派生表**设置为**比较物料价格**。</span><span class="sxs-lookup"><span data-stu-id="64cba-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="64cba-166">将**字段**设置为要充当筛选依据的字段。</span><span class="sxs-lookup"><span data-stu-id="64cba-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="64cba-167">通常使用**执行名称**或**执行时间**。</span><span class="sxs-lookup"><span data-stu-id="64cba-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="64cba-168">将**条件**设置为要查找的所选字段中的值（报表的名称或生成时间）。</span><span class="sxs-lookup"><span data-stu-id="64cba-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="64cba-169">如有必要，向**范围**表添加更多行，直到唯一确定了要查找的报表。</span><span class="sxs-lookup"><span data-stu-id="64cba-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="64cba-170">选择**确定**保存设置并关闭。</span><span class="sxs-lookup"><span data-stu-id="64cba-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="64cba-171">选择**保存**则保存导出设置。</span><span class="sxs-lookup"><span data-stu-id="64cba-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="64cba-172">打开**导出选项**选项卡，然后选择**立即导出**生成导出文件。</span><span class="sxs-lookup"><span data-stu-id="64cba-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="64cba-173">将打开**执行摘要**页，可在其中查看导出作业的状态和导出的实体的列表。</span><span class="sxs-lookup"><span data-stu-id="64cba-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="64cba-174">选择**实体处理状态**区域中列出的**比较物料价格**实体，然后选择**下载文件**下载从该实体导出的数据。</span><span class="sxs-lookup"><span data-stu-id="64cba-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="64cba-175">有关如何使用数据管理导出数据的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。</span><span class="sxs-lookup"><span data-stu-id="64cba-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
