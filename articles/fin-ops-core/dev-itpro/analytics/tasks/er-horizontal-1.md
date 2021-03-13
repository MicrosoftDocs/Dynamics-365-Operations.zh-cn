---
title: ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分 - 设计格式）
description: 本主题介绍如何配置电子报告 (ER) 格式以将报表生成为 OPENXML 工作表 (Excel) 文件。 （第 1 部分）
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3281f3059562fd34f9ccb71a6a11f64bf664008
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093493"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="04660-104">ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分 - 设计格式）</span><span class="sxs-lookup"><span data-stu-id="04660-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04660-105">下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。</span><span class="sxs-lookup"><span data-stu-id="04660-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="04660-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="04660-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="04660-107">若要完成这些步骤，首先必须完成下面的三个任务指南：</span><span class="sxs-lookup"><span data-stu-id="04660-107">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="04660-108">ER 创建一个配置提供程序，并标记其为当前运行的</span><span class="sxs-lookup"><span data-stu-id="04660-108">"ER Create a configuration provider and mark it as active"</span></span>

<span data-ttu-id="04660-109">“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”</span><span class="sxs-lookup"><span data-stu-id="04660-109">"ER Use financial dimensions as a data source (Part 1: Design data model)"</span></span>

<span data-ttu-id="04660-110">“ER 将财务维度用作数据源（第 2 部分：模型映射）”</span><span class="sxs-lookup"><span data-stu-id="04660-110">"ER Use financial dimensions as a data source (Part 2: Model mapping)"</span></span>

<span data-ttu-id="04660-111">您还必须下载和保存模板的本地副本，示例报表可以在这里找到：[Financial Dimensions Web 服务示例报表](https://go.microsoft.com/fwlink/?linkid=862266)。</span><span class="sxs-lookup"><span data-stu-id="04660-111">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="04660-112">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="04660-112">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="04660-113">创建新报表配置</span><span class="sxs-lookup"><span data-stu-id="04660-113">Create a new report configuration</span></span>
1. <span data-ttu-id="04660-114">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="04660-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="04660-115">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="04660-115">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="04660-116">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="04660-116">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="04660-117">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="04660-117">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="04660-118">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="04660-118">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="04660-119">在”名称“字段中，键入”包含可水平扩展范围的示例报表“。</span><span class="sxs-lookup"><span data-stu-id="04660-119">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="04660-120">包含可水平扩展范围的示例报表</span><span class="sxs-lookup"><span data-stu-id="04660-120">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="04660-121">在”描述“字段中，键入”通过动态添加列创建 Excel 输出“。</span><span class="sxs-lookup"><span data-stu-id="04660-121">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="04660-122">通过动态添加列创建 Excel 输出</span><span class="sxs-lookup"><span data-stu-id="04660-122">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="04660-123">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="04660-123">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="04660-124">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="04660-124">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="04660-125">设计报表格式</span><span class="sxs-lookup"><span data-stu-id="04660-125">Design the report format</span></span>
1. <span data-ttu-id="04660-126">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="04660-126">Click Designer.</span></span>
2. <span data-ttu-id="04660-127">开启”显示详细信息“切换按钮。</span><span class="sxs-lookup"><span data-stu-id="04660-127">Turn on the 'Show details' toggle button.</span></span>
3. <span data-ttu-id="04660-128">在“操作”窗格上，单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="04660-128">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="04660-129">单击“从 Excel 导入”。</span><span class="sxs-lookup"><span data-stu-id="04660-129">Click Import from Excel.</span></span>
5. <span data-ttu-id="04660-130">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="04660-130">Click Attachments.</span></span>
    * <span data-ttu-id="04660-131">导入报表的模板。</span><span class="sxs-lookup"><span data-stu-id="04660-131">Import the report's template.</span></span> <span data-ttu-id="04660-132">使用为其下载的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="04660-132">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="04660-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="04660-133">Click New.</span></span>
7. <span data-ttu-id="04660-134">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="04660-134">Click File.</span></span>
8. <span data-ttu-id="04660-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="04660-135">Close the page.</span></span>
9. <span data-ttu-id="04660-136">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="04660-136">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="04660-137">选择下载的模板。</span><span class="sxs-lookup"><span data-stu-id="04660-137">Select the downloaded template.</span></span>  
10. <span data-ttu-id="04660-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04660-138">Click OK.</span></span>
    * <span data-ttu-id="04660-139">添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。</span><span class="sxs-lookup"><span data-stu-id="04660-139">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="04660-140">每个列的每个单元格表示一个财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="04660-140">Each cell for every column will represent a single financial dimension's name.</span></span>  
11. <span data-ttu-id="04660-141">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="04660-141">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="04660-142">在树中，选择“Excel\范围”。</span><span class="sxs-lookup"><span data-stu-id="04660-142">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="04660-143">在“Excel 范围”字段中，键入“DimNames”。</span><span class="sxs-lookup"><span data-stu-id="04660-143">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="04660-144">DimNames</span><span class="sxs-lookup"><span data-stu-id="04660-144">DimNames</span></span>  
14. <span data-ttu-id="04660-145">在“复制方向”字段中，选择“水平”。</span><span class="sxs-lookup"><span data-stu-id="04660-145">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="04660-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04660-146">Click OK.</span></span>
16. <span data-ttu-id="04660-147">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-147">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="04660-148">单击“上移”。</span><span class="sxs-lookup"><span data-stu-id="04660-148">Click Move up.</span></span>
18. <span data-ttu-id="04660-149">在树中，选择“Excel = "SampleFinDimWsReport"\Cell<DimNames>”。</span><span class="sxs-lookup"><span data-stu-id="04660-149">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="04660-150">单击“剪切”。</span><span class="sxs-lookup"><span data-stu-id="04660-150">Click Cut.</span></span>
20. <span data-ttu-id="04660-151">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-151">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="04660-152">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="04660-152">Click Paste.</span></span>
22. <span data-ttu-id="04660-153">在树中，展开“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="04660-154">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="04660-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="04660-155">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="04660-155">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="04660-156">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="04660-156">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="04660-157">添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。</span><span class="sxs-lookup"><span data-stu-id="04660-157">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="04660-158">每个列的每个单元格表示报告的每个交易的一个财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="04660-158">Each cell for every column will represent a single financial dimension's value for each reporting transaction.</span></span>  
26. <span data-ttu-id="04660-159">单击“添加范围”。</span><span class="sxs-lookup"><span data-stu-id="04660-159">Click Add Range.</span></span>
27. <span data-ttu-id="04660-160">在“Excel 范围”字段中，键入“DimValues”。</span><span class="sxs-lookup"><span data-stu-id="04660-160">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="04660-161">DimValues</span><span class="sxs-lookup"><span data-stu-id="04660-161">DimValues</span></span>  
28. <span data-ttu-id="04660-162">在“复制方向”字段中，选择“水平”。</span><span class="sxs-lookup"><span data-stu-id="04660-162">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="04660-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04660-163">Click OK.</span></span>
30. <span data-ttu-id="04660-164">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>”。</span><span class="sxs-lookup"><span data-stu-id="04660-164">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="04660-165">单击“剪切”。</span><span class="sxs-lookup"><span data-stu-id="04660-165">Click Cut.</span></span>
32. <span data-ttu-id="04660-166">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-166">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="04660-167">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="04660-167">Click Paste.</span></span>
34. <span data-ttu-id="04660-168">在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-168">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="04660-169">将格式元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="04660-169">Map format elements to data sources</span></span>
1. <span data-ttu-id="04660-170">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="04660-170">Click the Mapping tab.</span></span>
2. <span data-ttu-id="04660-171">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="04660-171">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="04660-172">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="04660-173">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="04660-174">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="04660-175">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>”。</span><span class="sxs-lookup"><span data-stu-id="04660-175">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="04660-176">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-176">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="04660-177">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-177">Click Bind.</span></span>
9. <span data-ttu-id="04660-178">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-178">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="04660-179">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="04660-180">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-180">Click Bind.</span></span>
12. <span data-ttu-id="04660-181">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>”。</span><span class="sxs-lookup"><span data-stu-id="04660-181">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="04660-182">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="04660-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="04660-183">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-183">Click Bind.</span></span>
15. <span data-ttu-id="04660-184">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>”。</span><span class="sxs-lookup"><span data-stu-id="04660-184">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="04660-185">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="04660-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="04660-186">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-186">Click Bind.</span></span>
18. <span data-ttu-id="04660-187">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>”。</span><span class="sxs-lookup"><span data-stu-id="04660-187">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="04660-188">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-188">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="04660-189">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-189">Click Bind.</span></span>
21. <span data-ttu-id="04660-190">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>”。</span><span class="sxs-lookup"><span data-stu-id="04660-190">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="04660-191">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="04660-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="04660-192">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-192">Click Bind.</span></span>
24. <span data-ttu-id="04660-193">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>”。</span><span class="sxs-lookup"><span data-stu-id="04660-193">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="04660-194">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="04660-195">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-195">Click Bind.</span></span>
27. <span data-ttu-id="04660-196">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>”。</span><span class="sxs-lookup"><span data-stu-id="04660-196">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="04660-197">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="04660-198">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-198">Click Bind.</span></span>
30. <span data-ttu-id="04660-199">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="04660-199">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="04660-200">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="04660-201">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-201">Click Bind.</span></span>
33. <span data-ttu-id="04660-202">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>”。</span><span class="sxs-lookup"><span data-stu-id="04660-202">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="04660-203">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="04660-204">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-204">Click Bind.</span></span>
36. <span data-ttu-id="04660-205">在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。</span><span class="sxs-lookup"><span data-stu-id="04660-205">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="04660-206">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="04660-207">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-207">Click Bind.</span></span>
39. <span data-ttu-id="04660-208">在树中，展开“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-208">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="04660-209">在树中，选择“模型: 数据模型财务维度示例模型\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-209">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="04660-210">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>”。</span><span class="sxs-lookup"><span data-stu-id="04660-210">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="04660-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-211">Click Bind.</span></span>
43. <span data-ttu-id="04660-212">在树中，选择“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="04660-212">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="04660-213">在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。</span><span class="sxs-lookup"><span data-stu-id="04660-213">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="04660-214">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-214">Click Bind.</span></span>
46. <span data-ttu-id="04660-215">在树中，选择“Excel = "SampleFinDimWsReport"\Cell<CompanyName>”。</span><span class="sxs-lookup"><span data-stu-id="04660-215">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="04660-216">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="04660-216">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="04660-217">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="04660-217">Click Bind.</span></span>
49. <span data-ttu-id="04660-218">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04660-218">Click Save.</span></span>
50. <span data-ttu-id="04660-219">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="04660-219">Close the page.</span></span>

