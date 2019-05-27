---
title: ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分 - 设计格式）
description: 下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f0481a09e2ff4ae06fc53011067050c3373d6bc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544464"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1-design-format"></a><span data-ttu-id="95e40-103">ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分：设计格式）</span><span class="sxs-lookup"><span data-stu-id="95e40-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95e40-104">下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。</span><span class="sxs-lookup"><span data-stu-id="95e40-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="95e40-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="95e40-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="95e40-106">若要完成这些步骤，首先必须完成下面的三个任务指南：</span><span class="sxs-lookup"><span data-stu-id="95e40-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="95e40-107">“ER 创建一个配置提供程序，并标记其为当前运行的”</span><span class="sxs-lookup"><span data-stu-id="95e40-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="95e40-108">“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”</span><span class="sxs-lookup"><span data-stu-id="95e40-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="95e40-109">“ER 将财务维度用作数据源（第 2 部分：模型映射）”</span><span class="sxs-lookup"><span data-stu-id="95e40-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="95e40-110">您还必须下载和保存模板的本地副本，示例报表可以在这里找到：[Financial Dimensions Web 服务示例报表](https://go.microsoft.com/fwlink/?linkid=862266)。</span><span class="sxs-lookup"><span data-stu-id="95e40-110">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="95e40-111">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="95e40-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="95e40-112">创建新报表配置</span><span class="sxs-lookup"><span data-stu-id="95e40-112">Create a new report configuration</span></span>
1. <span data-ttu-id="95e40-113">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="95e40-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="95e40-114">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="95e40-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="95e40-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="95e40-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="95e40-116">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="95e40-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="95e40-117">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="95e40-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="95e40-118">在”名称“字段中，键入”包含可水平扩展范围的示例报表“。</span><span class="sxs-lookup"><span data-stu-id="95e40-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="95e40-119">包含可水平扩展范围的示例报表</span><span class="sxs-lookup"><span data-stu-id="95e40-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="95e40-120">在”描述“字段中，键入”通过动态添加列创建 Excel 输出“。</span><span class="sxs-lookup"><span data-stu-id="95e40-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="95e40-121">通过动态添加列创建 Excel 输出</span><span class="sxs-lookup"><span data-stu-id="95e40-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="95e40-122">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="95e40-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="95e40-123">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="95e40-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="95e40-124">设计报表格式</span><span class="sxs-lookup"><span data-stu-id="95e40-124">Design the report format</span></span>
1. <span data-ttu-id="95e40-125">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="95e40-125">Click Designer.</span></span>
2. <span data-ttu-id="95e40-126">开启”显示详细信息“切换按钮。</span><span class="sxs-lookup"><span data-stu-id="95e40-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="95e40-127">在“操作”窗格上，单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="95e40-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="95e40-128">单击“从 Excel 导入”。</span><span class="sxs-lookup"><span data-stu-id="95e40-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="95e40-129">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="95e40-129">Click Attachments.</span></span>
    * <span data-ttu-id="95e40-130">导入报表的模板。</span><span class="sxs-lookup"><span data-stu-id="95e40-130">Import the report’s template.</span></span> <span data-ttu-id="95e40-131">使用为其下载的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="95e40-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="95e40-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="95e40-132">Click New.</span></span>
7. <span data-ttu-id="95e40-133">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="95e40-133">Click File.</span></span>
8. <span data-ttu-id="95e40-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="95e40-134">Close the page.</span></span>
9. <span data-ttu-id="95e40-135">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="95e40-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="95e40-136">选择下载的模板。</span><span class="sxs-lookup"><span data-stu-id="95e40-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="95e40-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-137">Click OK.</span></span>
    * <span data-ttu-id="95e40-138">添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。</span><span class="sxs-lookup"><span data-stu-id="95e40-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="95e40-139">每个列的每个单元格表示一个财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="95e40-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="95e40-140">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="95e40-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="95e40-141">在树中，选择“Excel\范围”。</span><span class="sxs-lookup"><span data-stu-id="95e40-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="95e40-142">在“Excel 范围”字段中，键入“DimNames”。</span><span class="sxs-lookup"><span data-stu-id="95e40-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="95e40-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="95e40-143">DimNames</span></span>  
14. <span data-ttu-id="95e40-144">在“复制方向”字段中，选择“水平”。</span><span class="sxs-lookup"><span data-stu-id="95e40-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="95e40-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-145">Click OK.</span></span>
16. <span data-ttu-id="95e40-146">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="95e40-147">单击“上移”。</span><span class="sxs-lookup"><span data-stu-id="95e40-147">Click Move up.</span></span>
18. <span data-ttu-id="95e40-148">在树中，选择“Excel = "SampleFinDimWsReport"\Cell<DimNames>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="95e40-149">单击“剪切”。</span><span class="sxs-lookup"><span data-stu-id="95e40-149">Click Cut.</span></span>
20. <span data-ttu-id="95e40-150">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="95e40-151">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="95e40-151">Click Paste.</span></span>
22. <span data-ttu-id="95e40-152">在树中，展开“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="95e40-153">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="95e40-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="95e40-154">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="95e40-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="95e40-155">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="95e40-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="95e40-156">添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。</span><span class="sxs-lookup"><span data-stu-id="95e40-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="95e40-157">每个列的每个单元格表示报告的每个交易的一个财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="95e40-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="95e40-158">单击“添加范围”。</span><span class="sxs-lookup"><span data-stu-id="95e40-158">Click Add Range.</span></span>
27. <span data-ttu-id="95e40-159">在“Excel 范围”字段中，键入“DimValues”。</span><span class="sxs-lookup"><span data-stu-id="95e40-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="95e40-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="95e40-160">DimValues</span></span>  
28. <span data-ttu-id="95e40-161">在“复制方向”字段中，选择“水平”。</span><span class="sxs-lookup"><span data-stu-id="95e40-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="95e40-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-162">Click OK.</span></span>
30. <span data-ttu-id="95e40-163">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="95e40-164">单击“剪切”。</span><span class="sxs-lookup"><span data-stu-id="95e40-164">Click Cut.</span></span>
32. <span data-ttu-id="95e40-165">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="95e40-166">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="95e40-166">Click Paste.</span></span>
34. <span data-ttu-id="95e40-167">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="95e40-168">将格式元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="95e40-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="95e40-169">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="95e40-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="95e40-170">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="95e40-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="95e40-171">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="95e40-172">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="95e40-173">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="95e40-174">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="95e40-175">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="95e40-176">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-176">Click Bind.</span></span>
9. <span data-ttu-id="95e40-177">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="95e40-178">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="95e40-179">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-179">Click Bind.</span></span>
12. <span data-ttu-id="95e40-180">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="95e40-181">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="95e40-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="95e40-182">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-182">Click Bind.</span></span>
15. <span data-ttu-id="95e40-183">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="95e40-184">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="95e40-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="95e40-185">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-185">Click Bind.</span></span>
18. <span data-ttu-id="95e40-186">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="95e40-187">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="95e40-188">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-188">Click Bind.</span></span>
21. <span data-ttu-id="95e40-189">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="95e40-190">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="95e40-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="95e40-191">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-191">Click Bind.</span></span>
24. <span data-ttu-id="95e40-192">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="95e40-193">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="95e40-194">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-194">Click Bind.</span></span>
27. <span data-ttu-id="95e40-195">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="95e40-196">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="95e40-197">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-197">Click Bind.</span></span>
30. <span data-ttu-id="95e40-198">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="95e40-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="95e40-199">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="95e40-200">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-200">Click Bind.</span></span>
33. <span data-ttu-id="95e40-201">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="95e40-202">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="95e40-203">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-203">Click Bind.</span></span>
36. <span data-ttu-id="95e40-204">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="95e40-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="95e40-205">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="95e40-206">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-206">Click Bind.</span></span>
39. <span data-ttu-id="95e40-207">在树中，展开“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="95e40-208">在树中，选择“模型: 数据模型财务维度示例模型\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="95e40-209">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="95e40-210">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-210">Click Bind.</span></span>
43. <span data-ttu-id="95e40-211">在树中，选择“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="95e40-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="95e40-212">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="95e40-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="95e40-213">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-213">Click Bind.</span></span>
46. <span data-ttu-id="95e40-214">在树中，选择“Excel = "SampleFinDimWsReport"\Cell<CompanyName>”。</span><span class="sxs-lookup"><span data-stu-id="95e40-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="95e40-215">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="95e40-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="95e40-216">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="95e40-216">Click Bind.</span></span>
49. <span data-ttu-id="95e40-217">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="95e40-217">Click Save.</span></span>
50. <span data-ttu-id="95e40-218">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="95e40-218">Close the page.</span></span>

