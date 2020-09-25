---
title: 库存值存储报表
description: 本主题说明如何运行库存值存储报表并以数字方式提供输出，可以是 Microsoft Dynamics 365 Supply Chain Management 中的交互式页面，也可以是多种格式中任何一种的导出文档。
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759560"
---
# <a name="inventory-value-storage-report"></a><span data-ttu-id="45c00-103">库存值存储报表</span><span class="sxs-lookup"><span data-stu-id="45c00-103">Inventory value storage report</span></span>

<span data-ttu-id="45c00-104">本主题说明如何运行**库存值存储**报表并以数字方式提供输出，可以是 Microsoft Dynamics 365 Supply Chain Management 中的交互式页面，也可以是多种格式中任何一种的导出文档。</span><span class="sxs-lookup"><span data-stu-id="45c00-104">This topic explains how to run an **Inventory value storage** report and make the output available digitally, either as an interactive page in Microsoft Dynamics 365 Supply Chain Management or as an exported document in any of several formats.</span></span>

<span data-ttu-id="45c00-105">在浏览器中查看此报表时，将根据您已配置的布局动态调整列和聚合余额。</span><span class="sxs-lookup"><span data-stu-id="45c00-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on the layout that you've configured.</span></span> <span data-ttu-id="45c00-106">可以对结果排序，进行过滤，以及向下钻取到数据中，等等。</span><span class="sxs-lookup"><span data-stu-id="45c00-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="45c00-107">报告结果存储在**库存值**数据实体中。</span><span class="sxs-lookup"><span data-stu-id="45c00-107">Report results are stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="45c00-108">因此，您可以筛选结果并将其导出为逗号分隔值 (CSV) 或 Microsoft Excel 格式等格式。</span><span class="sxs-lookup"><span data-stu-id="45c00-108">Therefore, you can filter and export the results to a format such as comma-separated values (CSV) or Microsoft Excel format.</span></span>

<span data-ttu-id="45c00-109">当输出包含许多行时，**库存值存储**报表会很有用。</span><span class="sxs-lookup"><span data-stu-id="45c00-109">The **Inventory value storage** report is helpful when the output contains many lines.</span></span> <span data-ttu-id="45c00-110">例如，您有 50,000 件商品，并且已创建 300 家商店作为仓库。</span><span class="sxs-lookup"><span data-stu-id="45c00-110">For example, you have 50,000 items, and 300 stores have been created as warehouses.</span></span> <span data-ttu-id="45c00-111">在这种情况下，如果您按物料、站点和仓库请求库存期末余额，输出将包含许多行。</span><span class="sxs-lookup"><span data-stu-id="45c00-111">In this case, if you request inventory ending balances by item, site, and warehouse, the output will contain many lines.</span></span>

> [!NOTE]
> <span data-ttu-id="45c00-112">此报表将不包括报表布局中定义的小计。</span><span class="sxs-lookup"><span data-stu-id="45c00-112">The report won't include subtotals that are defined in the report layout.</span></span> <span data-ttu-id="45c00-113">即使在报表布局中定义了总帐余额，也不会将其包括在内。</span><span class="sxs-lookup"><span data-stu-id="45c00-113">It also won't include general ledger balances, even when they are defined in the report layout.</span></span> <span data-ttu-id="45c00-114">总帐对帐必须使用试算平衡表进行。</span><span class="sxs-lookup"><span data-stu-id="45c00-114">Reconciliation to the general ledger must be done by using trial balances.</span></span>

## <a name="turn-on-the-inventory-value-storage-feature"></a><span data-ttu-id="45c00-115">打开库存值存储功能</span><span class="sxs-lookup"><span data-stu-id="45c00-115">Turn on the Inventory value storage feature</span></span>

<span data-ttu-id="45c00-116">您必须先在系统中打开此功能，然后才能够生成**库存值存储**报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-116">Before you can generate an **Inventory value storage** report, you must turn on the feature in your system.</span></span> <span data-ttu-id="45c00-117">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="45c00-117">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="45c00-118">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="45c00-118">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="45c00-119">**模块** – 成本管理</span><span class="sxs-lookup"><span data-stu-id="45c00-119">**Module** – Cost management</span></span>
- <span data-ttu-id="45c00-120">**功能名称** – 库存值存储</span><span class="sxs-lookup"><span data-stu-id="45c00-120">**Feature name** – Inventory value storage</span></span>

## <a name="generate-an-inventory-value-storage-report"></a><span data-ttu-id="45c00-121">生成库存值存储报表</span><span class="sxs-lookup"><span data-stu-id="45c00-121">Generate an Inventory value storage report</span></span>

<span data-ttu-id="45c00-122">请执行以下步骤生成并存储**库存值存储**报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-122">Follow these steps to generate and store an **Inventory value storage** report.</span></span>

1. <span data-ttu-id="45c00-123">转到**成本管理 \> 查询和报表 \> 库存值报表存储**。</span><span class="sxs-lookup"><span data-stu-id="45c00-123">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="45c00-124">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="45c00-124">Select **New**.</span></span>
1. <span data-ttu-id="45c00-125">在显示的**库存值**对话框中，设置以下值以定义报表中包括哪些记录：</span><span class="sxs-lookup"><span data-stu-id="45c00-125">In the **Inventory value** dialog box that appears, set the following values to define which records are included in your report:</span></span>

    - <span data-ttu-id="45c00-126">在**参数**快速选项卡上，输入报表的唯一名称，然后使用**日期间隔**部分的字段来定义报表中包括哪些记录。</span><span class="sxs-lookup"><span data-stu-id="45c00-126">On the **Parameters** FastTab, enter a unique name for the report, and use the fields in the **Date interval** section to define which records are included in the report.</span></span> <span data-ttu-id="45c00-127">要定义日期间隔，您可以在**日期间隔代码**字段中选择预设范围（相对于报表生成日期），也可以在**开始日期**和**结束日期**字段中选择特定日期。</span><span class="sxs-lookup"><span data-stu-id="45c00-127">To define the date interval, you can either select a preset range (relative to the report generation date) in the **Date interval code** field, or select specific dates in the **From date** and **To date** fields.</span></span>
    - <span data-ttu-id="45c00-128">在**要包括的记录**快速选项卡上，设置筛选器和约束以定义要在报表中包括的数据。</span><span class="sxs-lookup"><span data-stu-id="45c00-128">On the **Records to include** FastTab, set up filters and constraints to define which data is included in the report.</span></span>
    - <span data-ttu-id="45c00-129">在**在后台运行**快速选项卡上，指定生成报表的方式、时间和频率。</span><span class="sxs-lookup"><span data-stu-id="45c00-129">On the **Run in the background** FastTab, specify how, when, and how often the report is generated.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45c00-130">此报表始终作为批处理作业的一部分运行。</span><span class="sxs-lookup"><span data-stu-id="45c00-130">This report is always run as part of a batch job.</span></span>

1. <span data-ttu-id="45c00-131">选择**确定**应用设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="45c00-131">Select **OK** to apply your settings and close the dialog box.</span></span>

<span data-ttu-id="45c00-132">批处理作业完成后，报表将在**库存价值报表存储**页面上列出。</span><span class="sxs-lookup"><span data-stu-id="45c00-132">After the batch job is completed, the report will be listed on the **Inventory value report storage** page.</span></span> <span data-ttu-id="45c00-133">可能必须刷新页面才能查看报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-133">You might have to refresh the page to see the report.</span></span>

## <a name="explore-an-inventory-value-storage-report"></a><span data-ttu-id="45c00-134">浏览库存值存储报表</span><span class="sxs-lookup"><span data-stu-id="45c00-134">Explore an Inventory value storage report</span></span>

<span data-ttu-id="45c00-135">生成报表后，您可以按照以下步骤随时查看和浏览报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-135">After you've generated a report, you can view and explore it at any time by following these steps.</span></span>

1. <span data-ttu-id="45c00-136">转到**成本管理 \> 查询和报表 \> 库存值报表存储**。</span><span class="sxs-lookup"><span data-stu-id="45c00-136">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="45c00-137">在列表中选择一个报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-137">Select a report in the list.</span></span>
1. <span data-ttu-id="45c00-138">选择**查看详细信息**显示报表内容。</span><span class="sxs-lookup"><span data-stu-id="45c00-138">Select **View details** to show the report content.</span></span>
1. <span data-ttu-id="45c00-139">通过执行以下任何一个步骤来浏览报表：</span><span class="sxs-lookup"><span data-stu-id="45c00-139">Explore the report by following any of these steps:</span></span>

    - <span data-ttu-id="45c00-140">对于 Supply Chain Management 中的大多数标准页面，您可以选择几乎任何列标题，来按该列中的值对网格进行排序或筛选。</span><span class="sxs-lookup"><span data-stu-id="45c00-140">As for most standard pages in Supply Chain Management, you can select almost any column heading to sort or filter the grid by the values in that column.</span></span>
    - <span data-ttu-id="45c00-141">使用**筛选**字段按几个可用列中任何一列的任何值筛选报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-141">Use the **Filter** field to filter the report by any value in any of several available columns.</span></span>
    - <span data-ttu-id="45c00-142">使用查看菜单（位于**筛选**字段上方）保存和加载您喜欢的排序和筛选选项组合。</span><span class="sxs-lookup"><span data-stu-id="45c00-142">Use the view menu (above the **Filter** field) to save and load your favorite combinations of sort and filter options.</span></span>

## <a name="export-an-inventory-value-storage-report"></a><span data-ttu-id="45c00-143">导出库存值存储报表</span><span class="sxs-lookup"><span data-stu-id="45c00-143">Export an Inventory value storage report</span></span>

<span data-ttu-id="45c00-144">生成的所有报表都存储在**库存值**数据实体中。</span><span class="sxs-lookup"><span data-stu-id="45c00-144">Every report that you generate is stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="45c00-145">可使用 Supply Chain Management 的标准数据管理功能将此实体中的数据导出到任何支持的数据格式，如 CSV 或 Excel 格式。</span><span class="sxs-lookup"><span data-stu-id="45c00-145">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, such as CSV or Excel format.</span></span>

<span data-ttu-id="45c00-146">以下示例显示了如何导出**库存值报表**报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-146">The following example shows how to export an **Inventory value report** report.</span></span>

1. <span data-ttu-id="45c00-147">转到**系统管理 \> 工作区 \> 数据管理**。</span><span class="sxs-lookup"><span data-stu-id="45c00-147">Go to **System administration \> Workspaces \> Data management**.</span></span>
1. <span data-ttu-id="45c00-148">在**导入/导出**部分，选择**导出**磁贴。</span><span class="sxs-lookup"><span data-stu-id="45c00-148">In the **Import / Export** section, select the **Export** tile.</span></span> 
1. <span data-ttu-id="45c00-149">在出现的**导出**页面上，设置导出作业。</span><span class="sxs-lookup"><span data-stu-id="45c00-149">On the **Export** page that appears, you will set up the export job.</span></span> <span data-ttu-id="45c00-150">首先输入作业的组名称。</span><span class="sxs-lookup"><span data-stu-id="45c00-150">First enter a group name for the job.</span></span>
1. <span data-ttu-id="45c00-151">在**选定实体**部分，选择**添加实体**。</span><span class="sxs-lookup"><span data-stu-id="45c00-151">In the **Selected entities** section, select **Add entity**.</span></span>
1. <span data-ttu-id="45c00-152">在出现的对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="45c00-152">In the dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="45c00-153">**实体名称** – 选择**库存值**。</span><span class="sxs-lookup"><span data-stu-id="45c00-153">**Entity name** – Select **Inventory value**.</span></span>
    - <span data-ttu-id="45c00-154">**目标数据格式** – 选择数据要导出的格式。</span><span class="sxs-lookup"><span data-stu-id="45c00-154">**Target data format** – Select the format to export data to.</span></span>

1. <span data-ttu-id="45c00-155">选择**添加**添加新行，然后选择**关闭**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="45c00-155">Select **Add** to add the new row, and then select **Close** to close the dialog box.</span></span>
1. <span data-ttu-id="45c00-156">通常一次导出一个报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-156">Usually, you will export one report at a time.</span></span> <span data-ttu-id="45c00-157">要导出单个报表，为您刚刚添加到**查询**对话框的行设置一个筛选器。</span><span class="sxs-lookup"><span data-stu-id="45c00-157">To export a single report, set up a filter for the row that you just added to the **Inquiry** dialog box.</span></span> <span data-ttu-id="45c00-158">通过这种方式，您可以定义**库存值**实体中的哪个报表包含在导出中。</span><span class="sxs-lookup"><span data-stu-id="45c00-158">In this way, you can define which report from the **Inventory value** entity is included in your export.</span></span> <span data-ttu-id="45c00-159">按照以下步骤设置以下筛选选项以导出单个报表：</span><span class="sxs-lookup"><span data-stu-id="45c00-159">Follow these steps to set the following filter options to export a single report:</span></span>

    1. <span data-ttu-id="45c00-160">在**范围**选项卡中，选择**添加**添加行。</span><span class="sxs-lookup"><span data-stu-id="45c00-160">On the **Range** tab, select **Add** to add a row.</span></span>
    2. <span data-ttu-id="45c00-161">将**表**字段设置为**库存值**。</span><span class="sxs-lookup"><span data-stu-id="45c00-161">Set the **Table** field to **Inventory value**.</span></span>
    3. <span data-ttu-id="45c00-162">将**派生表**字段设置为**库存值**。</span><span class="sxs-lookup"><span data-stu-id="45c00-162">Set the **Derived table** field to **Inventory value**.</span></span>
    4. <span data-ttu-id="45c00-163">将**字段**字段设置为要充当筛选依据的字段。</span><span class="sxs-lookup"><span data-stu-id="45c00-163">Set the **Field** field to the field that you want to filter by.</span></span> <span data-ttu-id="45c00-164">通常，您将使用**执行名称**字段和/或**执行时间**字段。</span><span class="sxs-lookup"><span data-stu-id="45c00-164">Usually, you will use the **Execution name** field and/or the **Execution time** field.</span></span>
    5. <span data-ttu-id="45c00-165">将**条件**字段设置为要在所选字段中查找的值。</span><span class="sxs-lookup"><span data-stu-id="45c00-165">Set the **Criteria** field to the value that you want to look for in the selected field.</span></span> <span data-ttu-id="45c00-166">（如果您在上一步中选择了**执行名称**字段，此值将成为报表的名称。</span><span class="sxs-lookup"><span data-stu-id="45c00-166">(If you selected the **Execution name** field in the previous step, this value will be the name of the report.</span></span> <span data-ttu-id="45c00-167">如果您选择了**执行时间**字段，它将是生成报表的时间。）</span><span class="sxs-lookup"><span data-stu-id="45c00-167">If you selected the **Execution time** field, it will be the time when the report was generated.)</span></span>
    6. <span data-ttu-id="45c00-168">根据需要向**范围**选项卡添加更多行，直到唯一确定了要查找的报表。</span><span class="sxs-lookup"><span data-stu-id="45c00-168">Add more rows to the **Range** tab as you require, until you've uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="45c00-169">选择**确定**保存设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="45c00-169">Select **OK** to save your settings and close the dialog box.</span></span>
1. <span data-ttu-id="45c00-170">选择**保存**则保存导出设置。</span><span class="sxs-lookup"><span data-stu-id="45c00-170">Select **Save** to save your export setup.</span></span>
1. <span data-ttu-id="45c00-171">在**导出选项**选项卡上，选择**立即导出**生成导出文件。</span><span class="sxs-lookup"><span data-stu-id="45c00-171">On the **Export options** tab, select **Export now** to generate the export file.</span></span>
1. <span data-ttu-id="45c00-172">在出现的**执行摘要**页上，您可以查看导出作业的状态和导出的实体的列表。</span><span class="sxs-lookup"><span data-stu-id="45c00-172">On the **Execution summary** page that appears, you can view the status of your export job and a list of the entities that were exported.</span></span> <span data-ttu-id="45c00-173">在**实体处理状态**部分，选择列表中的**库存值**实体，然后选择**下载文件**下载从该实体导出的数据。</span><span class="sxs-lookup"><span data-stu-id="45c00-173">In the **Entity processing status** section, select the **Inventory value** entity in the list, and then select **Download file** to download the data that was exported from that entity.</span></span>

<span data-ttu-id="45c00-174">有关如何使用数据管理导出数据的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。</span><span class="sxs-lookup"><span data-stu-id="45c00-174">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
