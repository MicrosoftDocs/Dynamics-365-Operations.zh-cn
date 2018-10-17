--- 
title: "ER 配置格式以执行盘点和合计（第 3 部分 - 使用计算生成输出）"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="d7cb4-103">ER 配置格式以执行盘点和合计（第 3 部分：使用计算生成输出）</span><span class="sxs-lookup"><span data-stu-id="d7cb4-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7cb4-104">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="d7cb4-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d7cb4-106">必须首先完成“ER 配置格式以执行盘点和合计（第 2 部分：配置计算）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="d7cb4-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="d7cb4-108">配置此报表以使用盘点和合计信息</span><span class="sxs-lookup"><span data-stu-id="d7cb4-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="d7cb4-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d7cb4-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d7cb4-111">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="d7cb4-112">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="d7cb4-113">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="d7cb4-114">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-114">Click Designer.</span></span>
7. <span data-ttu-id="d7cb4-115">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="d7cb4-116">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="d7cb4-117">添加新数据源以获取记忆的块列表。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="d7cb4-118">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="d7cb4-119">在“名称”字段中，键入“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="d7cb4-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="d7cb4-120">$BlocksList</span></span>  
11. <span data-ttu-id="d7cb4-121">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-121">Click Edit formula.</span></span>
12. <span data-ttu-id="d7cb4-122">在此该树中，选择“数据收集函数\COLLECTEDLIST”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="d7cb4-123">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-123">Click Add function.</span></span>
14. <span data-ttu-id="d7cb4-124">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-124">Click Add data source.</span></span>
15. <span data-ttu-id="d7cb4-125">在“公式”字段中，输入“COLLECTEDLIST('$BlockName',”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="d7cb4-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="d7cb4-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="d7cb4-127">在“公式”字段中，输入“COLLECTEDLIST('$BlockName', "\*")”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="d7cb4-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="d7cb4-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="d7cb4-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-129">Click Save.</span></span>
    * <span data-ttu-id="d7cb4-130">模式“\*”表示所有块都包含在此记录的列表中。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="d7cb4-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-131">Close the page.</span></span>
19. <span data-ttu-id="d7cb4-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-132">Click OK.</span></span>
20. <span data-ttu-id="d7cb4-133">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-133">Click the Format tab.</span></span>
21. <span data-ttu-id="d7cb4-134">在树结构中，选择“内部统计\数据”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="d7cb4-135">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="d7cb4-136">在树中，选择“文本\序列”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="d7cb4-137">在“名称”字段中，键入“按块的合计”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="d7cb4-138">按块的总计</span><span class="sxs-lookup"><span data-stu-id="d7cb4-138">Totals by blocks</span></span>  
25. <span data-ttu-id="d7cb4-139">在"特殊字符"字段中，选择“换行 - Windows (CR LF)”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="d7cb4-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-140">Click OK.</span></span>
27. <span data-ttu-id="d7cb4-141">在树中，选择“内部统计\数据\按块的合计”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="d7cb4-142">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="d7cb4-143">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="d7cb4-144">在“名称”字段中，键入“块代码”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="d7cb4-145">块代码</span><span class="sxs-lookup"><span data-stu-id="d7cb4-145">Block code</span></span>  
31. <span data-ttu-id="d7cb4-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-146">Click OK.</span></span>
32. <span data-ttu-id="d7cb4-147">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-147">Click Add String.</span></span>
33. <span data-ttu-id="d7cb4-148">在“名称”字段中，键入“行合计”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="d7cb4-149">行合计</span><span class="sxs-lookup"><span data-stu-id="d7cb4-149">Lines counting</span></span>  
34. <span data-ttu-id="d7cb4-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-150">Click OK.</span></span>
35. <span data-ttu-id="d7cb4-151">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-151">Click Add String.</span></span>
36. <span data-ttu-id="d7cb4-152">在“名称”字段中，键入“总金额”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="d7cb4-153">总数</span><span class="sxs-lookup"><span data-stu-id="d7cb4-153">Total amount</span></span>  
37. <span data-ttu-id="d7cb4-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-154">Click OK.</span></span>
38. <span data-ttu-id="d7cb4-155">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="d7cb4-156">在树中，选择“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="d7cb4-157">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-157">Click Bind.</span></span>
    * <span data-ttu-id="d7cb4-158">为记忆的每个块创建汇总行。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="d7cb4-159">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-159">Click the Format tab.</span></span>
42. <span data-ttu-id="d7cb4-160">在树中，选择“内部统计\数据\按块的合计\块代码”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="d7cb4-161">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="d7cb4-162">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-162">Click Edit formula.</span></span>
45. <span data-ttu-id="d7cb4-163">在“公式”字段中，输如""块 id: " & '"。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="d7cb4-164">"块 id: " &</span><span class="sxs-lookup"><span data-stu-id="d7cb4-164">"Block id: " &</span></span>  
46. <span data-ttu-id="d7cb4-165">在树中，展开“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="d7cb4-166">在树中，选择“$BlocksList\值”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="d7cb4-167">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-167">Click Add data source.</span></span>
49. <span data-ttu-id="d7cb4-168">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-168">Click Save.</span></span>
50. <span data-ttu-id="d7cb4-169">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-169">Close the page.</span></span>
51. <span data-ttu-id="d7cb4-170">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-170">Click the Format tab.</span></span>
52. <span data-ttu-id="d7cb4-171">在树中，选择“内部统计\数据\按块的合计\行合计”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="d7cb4-172">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="d7cb4-173">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-173">Click Edit formula.</span></span>
    * <span data-ttu-id="d7cb4-174">为此报表中的每个块的行数创建输出。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="d7cb4-175">在“公式”字段中，输入“"此块中的行数: " & ”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="d7cb4-176">"此块中的行数: " &</span><span class="sxs-lookup"><span data-stu-id="d7cb4-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="d7cb4-177">在“公式”字段中，输入“"此块中的行数: & TEXT(”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="d7cb4-178">"此块中的行数: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="d7cb4-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="d7cb4-179">在此该树中，选择“数据收集函数\COUNTIFS”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="d7cb4-180">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-180">Click Add function.</span></span>
59. <span data-ttu-id="d7cb4-181">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-181">Click Add data source.</span></span>
60. <span data-ttu-id="d7cb4-182">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', ”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="d7cb4-183">"此块中的行数: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="d7cb4-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="d7cb4-184">在树中，展开“$BlocksList”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="d7cb4-185">在树中，选择“$BlocksList\值”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="d7cb4-186">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-186">Click Add data source.</span></span>
64. <span data-ttu-id="d7cb4-187">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="d7cb4-188">"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="d7cb4-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="d7cb4-189">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="d7cb4-190">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-190">Click Add data source.</span></span>
67. <span data-ttu-id="d7cb4-191">在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="d7cb4-192">"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="d7cb4-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="d7cb4-193">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-193">Click Save.</span></span>
69. <span data-ttu-id="d7cb4-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-194">Close the page.</span></span>
70. <span data-ttu-id="d7cb4-195">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-195">Click the Format tab.</span></span>
71. <span data-ttu-id="d7cb4-196">在树中，选择“内部统计\数据\按块的合计\总金额”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="d7cb4-197">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="d7cb4-198">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-198">Click Edit formula.</span></span>
    * <span data-ttu-id="d7cb4-199">创建将为此报表中的每个块的开票金额总和的输出。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="d7cb4-200">在“公式”字段中，输入“"开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="d7cb4-201">"开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="d7cb4-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="d7cb4-202">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-202">Click Save.</span></span>
76. <span data-ttu-id="d7cb4-203">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-203">Close the page.</span></span>
77. <span data-ttu-id="d7cb4-204">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-204">Click Save.</span></span>
78. <span data-ttu-id="d7cb4-205">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cb4-205">Close the page.</span></span>


