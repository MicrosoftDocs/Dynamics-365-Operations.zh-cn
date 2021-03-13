---
title: ER 配置格式以执行盘点和合计（第 3 部分 - 使用计算生成输出）
description: 本主题介绍如何配置电子报告格式以基于已经生成的文本输出的数据执行盘点和合计。 （第 3 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092964"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="ccf3f-104">ER 配置格式以执行盘点和合计（第 3 部分 - 使用计算生成输出）</span><span class="sxs-lookup"><span data-stu-id="ccf3f-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccf3f-105">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ccf3f-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ccf3f-107">必须首先完成“ER 配置格式以执行盘点和合计（第 2 部分：配置计算）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="ccf3f-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="ccf3f-109">配置此报表以使用盘点和合计信息</span><span class="sxs-lookup"><span data-stu-id="ccf3f-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="ccf3f-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ccf3f-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ccf3f-112">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ccf3f-113">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ccf3f-114">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ccf3f-115">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-115">Click Designer.</span></span>
7. <span data-ttu-id="ccf3f-116">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="ccf3f-117">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="ccf3f-118">添加新数据源以获取记忆的块列表。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="ccf3f-119">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="ccf3f-120">在“名称”字段中，键入“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="ccf3f-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="ccf3f-121">$BlocksList</span></span>  
11. <span data-ttu-id="ccf3f-122">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-122">Click Edit formula.</span></span>
12. <span data-ttu-id="ccf3f-123">在此该树中，选择“数据收集函数\COLLECTEDLIST”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="ccf3f-124">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-124">Click Add function.</span></span>
14. <span data-ttu-id="ccf3f-125">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-125">Click Add data source.</span></span>
15. <span data-ttu-id="ccf3f-126">在“公式”字段中，输入“COLLECTEDLIST('$BlockName',”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="ccf3f-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ccf3f-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="ccf3f-128">在“公式”字段中，输入“COLLECTEDLIST('$BlockName', "\*")”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="ccf3f-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="ccf3f-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="ccf3f-130">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-130">Click Save.</span></span>
    * <span data-ttu-id="ccf3f-131">模式“\*”表示所有块都包含在此记录的列表中。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="ccf3f-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-132">Close the page.</span></span>
19. <span data-ttu-id="ccf3f-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-133">Click OK.</span></span>
20. <span data-ttu-id="ccf3f-134">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-134">Click the Format tab.</span></span>
21. <span data-ttu-id="ccf3f-135">在树结构中，选择“内部统计\数据”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="ccf3f-136">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ccf3f-137">在树中，选择“文本\序列”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="ccf3f-138">在“名称”字段中，键入“按块的合计”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="ccf3f-139">按块的总计</span><span class="sxs-lookup"><span data-stu-id="ccf3f-139">Totals by blocks</span></span>  
25. <span data-ttu-id="ccf3f-140">在"特殊字符"字段中，选择“换行 - Windows (CR LF)”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="ccf3f-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-141">Click OK.</span></span>
27. <span data-ttu-id="ccf3f-142">在树中，选择“内部统计\数据\按块的合计”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="ccf3f-143">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="ccf3f-144">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="ccf3f-145">在“名称”字段中，键入“块代码”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="ccf3f-146">块代码</span><span class="sxs-lookup"><span data-stu-id="ccf3f-146">Block code</span></span>  
31. <span data-ttu-id="ccf3f-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-147">Click OK.</span></span>
32. <span data-ttu-id="ccf3f-148">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-148">Click Add String.</span></span>
33. <span data-ttu-id="ccf3f-149">在“名称”字段中，键入“行合计”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="ccf3f-150">行合计</span><span class="sxs-lookup"><span data-stu-id="ccf3f-150">Lines counting</span></span>  
34. <span data-ttu-id="ccf3f-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-151">Click OK.</span></span>
35. <span data-ttu-id="ccf3f-152">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-152">Click Add String.</span></span>
36. <span data-ttu-id="ccf3f-153">在“名称”字段中，键入“总金额”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="ccf3f-154">总数</span><span class="sxs-lookup"><span data-stu-id="ccf3f-154">Total amount</span></span>  
37. <span data-ttu-id="ccf3f-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-155">Click OK.</span></span>
38. <span data-ttu-id="ccf3f-156">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="ccf3f-157">在树中，选择“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="ccf3f-158">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-158">Click Bind.</span></span>
    * <span data-ttu-id="ccf3f-159">为记忆的每个块创建汇总行。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="ccf3f-160">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-160">Click the Format tab.</span></span>
42. <span data-ttu-id="ccf3f-161">在树中，选择“内部统计\数据\按块的合计\块代码”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="ccf3f-162">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="ccf3f-163">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-163">Click Edit formula.</span></span>
45. <span data-ttu-id="ccf3f-164">在“公式”字段中，输如""块 id: " & '"。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="ccf3f-165">"块 id: " &</span><span class="sxs-lookup"><span data-stu-id="ccf3f-165">"Block id: " &</span></span>  
46. <span data-ttu-id="ccf3f-166">在树中，展开“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="ccf3f-167">在树中，选择“$BlocksList\值”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="ccf3f-168">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-168">Click Add data source.</span></span>
49. <span data-ttu-id="ccf3f-169">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-169">Click Save.</span></span>
50. <span data-ttu-id="ccf3f-170">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-170">Close the page.</span></span>
51. <span data-ttu-id="ccf3f-171">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-171">Click the Format tab.</span></span>
52. <span data-ttu-id="ccf3f-172">在树中，选择“内部统计\数据\按块的合计\行合计”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="ccf3f-173">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="ccf3f-174">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-174">Click Edit formula.</span></span>
    * <span data-ttu-id="ccf3f-175">为此报表中的每个块的行数创建输出。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="ccf3f-176">在“公式”字段中，输入“"此块中的行数: " & ”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="ccf3f-177">"此块中的行数: " &</span><span class="sxs-lookup"><span data-stu-id="ccf3f-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="ccf3f-178">在“公式”字段中，输入“"此块中的行数: & TEXT(”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="ccf3f-179">"此块中的行数: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="ccf3f-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="ccf3f-180">在此该树中，选择“数据收集函数\COUNTIFS”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="ccf3f-181">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-181">Click Add function.</span></span>
59. <span data-ttu-id="ccf3f-182">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-182">Click Add data source.</span></span>
60. <span data-ttu-id="ccf3f-183">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', ”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="ccf3f-184">"此块中的行数: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ccf3f-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="ccf3f-185">在树中，展开“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="ccf3f-186">在树中，选择“$BlocksList\值”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="ccf3f-187">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-187">Click Add data source.</span></span>
64. <span data-ttu-id="ccf3f-188">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="ccf3f-189">"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="ccf3f-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="ccf3f-190">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="ccf3f-191">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-191">Click Add data source.</span></span>
67. <span data-ttu-id="ccf3f-192">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="ccf3f-193">"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="ccf3f-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="ccf3f-194">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-194">Click Save.</span></span>
69. <span data-ttu-id="ccf3f-195">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-195">Close the page.</span></span>
70. <span data-ttu-id="ccf3f-196">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-196">Click the Format tab.</span></span>
71. <span data-ttu-id="ccf3f-197">在树中，选择“内部统计\数据\按块的合计\总金额”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="ccf3f-198">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="ccf3f-199">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-199">Click Edit formula.</span></span>
    * <span data-ttu-id="ccf3f-200">创建将为此报表中的每个块的开票金额总和的输出。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="ccf3f-201">在“公式”字段中，输入“"开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="ccf3f-202">"开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="ccf3f-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="ccf3f-203">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-203">Click Save.</span></span>
76. <span data-ttu-id="ccf3f-204">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-204">Close the page.</span></span>
77. <span data-ttu-id="ccf3f-205">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-205">Click Save.</span></span>
78. <span data-ttu-id="ccf3f-206">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ccf3f-206">Close the page.</span></span>

