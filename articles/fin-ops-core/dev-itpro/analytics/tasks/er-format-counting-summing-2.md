---
title: ER 配置格式以执行盘点和合计（第 2 部分 - 配置计算）
description: 本主题介绍如何配置电子报告格式以基于已经生成的文本输出的数据执行盘点和合计。 （第 2 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565157"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="573e0-104">ER 配置格式以执行盘点和合计（第 2 部分 - 配置计算）</span><span class="sxs-lookup"><span data-stu-id="573e0-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="573e0-105">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="573e0-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="573e0-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="573e0-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="573e0-107">必须首先完成“ER 配置格式以执行盘点和合计（第 1 部分：创建格式）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="573e0-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="573e0-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="573e0-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="573e0-109">创建格式配置以添加盘点和合计详细信息</span><span class="sxs-lookup"><span data-stu-id="573e0-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="573e0-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="573e0-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="573e0-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="573e0-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="573e0-112">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="573e0-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="573e0-113">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="573e0-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="573e0-114">假设您需要通过在内部统计报表结尾添加包含摘要详细信息的行，自定义 Microsoft 提供的格式。</span><span class="sxs-lookup"><span data-stu-id="573e0-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="573e0-115">方法是从 Microsoft 实例派生自己的内部统计配置实例来进行修改。</span><span class="sxs-lookup"><span data-stu-id="573e0-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="573e0-116">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="573e0-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="573e0-117">在“新建”字段中，输入“从以下名称派生: 内部统计 (DE)、Microsoft”。</span><span class="sxs-lookup"><span data-stu-id="573e0-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="573e0-118">在“名称”字段中，键入“带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="573e0-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="573e0-119">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="573e0-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="573e0-120">配置此报表以基于输出详细信息执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="573e0-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="573e0-121">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="573e0-121">Click Designer.</span></span>
2. <span data-ttu-id="573e0-122">在“收集输出详细信息”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="573e0-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="573e0-123">此标记将在运行时激活收集输出详细信息的过程，以便生成内部统计文件。</span><span class="sxs-lookup"><span data-stu-id="573e0-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="573e0-124">您需要对不同内部统计放心执行盘点，以便向数据源的此格式配置列表添加专门的模型枚举。</span><span class="sxs-lookup"><span data-stu-id="573e0-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="573e0-125">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="573e0-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="573e0-126">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="573e0-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="573e0-127">在树结构中，选择“数据模型\枚举”。</span><span class="sxs-lookup"><span data-stu-id="573e0-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="573e0-128">在“名称”字段中，键入“Direction”。</span><span class="sxs-lookup"><span data-stu-id="573e0-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="573e0-129">在“模型枚举”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="573e0-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="573e0-130">选择值“方向”。</span><span class="sxs-lookup"><span data-stu-id="573e0-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="573e0-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="573e0-131">Click OK.</span></span>
9. <span data-ttu-id="573e0-132">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="573e0-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="573e0-133">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="573e0-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="573e0-134">在“名称”字段中，键入“$BlockName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="573e0-135">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="573e0-135">Click Edit formula.</span></span>
13. <span data-ttu-id="573e0-136">在“公式”字段中，输入“block”。</span><span class="sxs-lookup"><span data-stu-id="573e0-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="573e0-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-137">Click Save.</span></span>
15. <span data-ttu-id="573e0-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-138">Close the page.</span></span>
16. <span data-ttu-id="573e0-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="573e0-139">Click OK.</span></span>
17. <span data-ttu-id="573e0-140">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="573e0-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="573e0-141">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="573e0-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="573e0-142">在“名称”字段中，键入“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="573e0-143">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="573e0-143">Click Edit formula.</span></span>
21. <span data-ttu-id="573e0-144">在“公式”字段中，输入“record”。</span><span class="sxs-lookup"><span data-stu-id="573e0-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="573e0-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-145">Click Save.</span></span>
23. <span data-ttu-id="573e0-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-146">Close the page.</span></span>
24. <span data-ttu-id="573e0-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="573e0-147">Click OK.</span></span>
25. <span data-ttu-id="573e0-148">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="573e0-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="573e0-149">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="573e0-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="573e0-150">在“名称”字段中，键入“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="573e0-151">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="573e0-151">Click Edit formula.</span></span>
29. <span data-ttu-id="573e0-152">在“公式”字段中，输入“InvoicedAmountEUR”。</span><span class="sxs-lookup"><span data-stu-id="573e0-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="573e0-153">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-153">Click Save.</span></span>
31. <span data-ttu-id="573e0-154">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-154">Close the page.</span></span>
32. <span data-ttu-id="573e0-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="573e0-155">Click OK.</span></span>
33. <span data-ttu-id="573e0-156">在树结构中，选择“内部统计\数据”。</span><span class="sxs-lookup"><span data-stu-id="573e0-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="573e0-157">单击“已收集的数据键名”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="573e0-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="573e0-158">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="573e0-158">Click Add data source.</span></span>
    * <span data-ttu-id="573e0-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="573e0-159">$BlockName</span></span>  
36. <span data-ttu-id="573e0-160">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-160">Click Save.</span></span>
37. <span data-ttu-id="573e0-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-161">Close the page.</span></span>
38. <span data-ttu-id="573e0-162">单击“已收集的数据键值”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="573e0-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="573e0-163">在“公式”字段中，输入“IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”。</span><span class="sxs-lookup"><span data-stu-id="573e0-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="573e0-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="573e0-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="573e0-165">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-165">Click Save.</span></span>
41. <span data-ttu-id="573e0-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-166">Close the page.</span></span>
    * <span data-ttu-id="573e0-167">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="573e0-167">Count the lines of this sequence.</span></span> <span data-ttu-id="573e0-168">结果将与名称“block”一起单独用于不同方向。</span><span class="sxs-lookup"><span data-stu-id="573e0-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="573e0-169">值“Import”将用于任何到货内部统计交易。</span><span class="sxs-lookup"><span data-stu-id="573e0-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="573e0-170">值“Export”将用于任何内部统计发货交易。</span><span class="sxs-lookup"><span data-stu-id="573e0-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="573e0-171">请将其视为虚拟 Excel 电子表格。</span><span class="sxs-lookup"><span data-stu-id="573e0-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="573e0-172">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。</span><span class="sxs-lookup"><span data-stu-id="573e0-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="573e0-173">在树中，展开“内部统计\数据: 序列”。</span><span class="sxs-lookup"><span data-stu-id="573e0-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="573e0-174">在树中，选择“内部统计\数据: 序列\到货?”。</span><span class="sxs-lookup"><span data-stu-id="573e0-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="573e0-175">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="573e0-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="573e0-176">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="573e0-176">Count the lines of this sequence.</span></span> <span data-ttu-id="573e0-177">将使用名称“记录”记忆结果。</span><span class="sxs-lookup"><span data-stu-id="573e0-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="573e0-178">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="573e0-179">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="573e0-179">Click Add data source.</span></span>
47. <span data-ttu-id="573e0-180">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-180">Click Save.</span></span>
48. <span data-ttu-id="573e0-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-181">Close the page.</span></span>
49. <span data-ttu-id="573e0-182">单击“已收集的数据键值”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="573e0-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="573e0-183">在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。</span><span class="sxs-lookup"><span data-stu-id="573e0-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="573e0-184">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-184">Click Save.</span></span>
52. <span data-ttu-id="573e0-185">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-185">Close the page.</span></span>
    * <span data-ttu-id="573e0-186">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="573e0-186">Count the lines of this sequence.</span></span> <span data-ttu-id="573e0-187">结果将与名称“record”一起单独用于不同商品代码。</span><span class="sxs-lookup"><span data-stu-id="573e0-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="573e0-188">请将其视为虚拟 Excel 电子表格。</span><span class="sxs-lookup"><span data-stu-id="573e0-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="573e0-189">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”且第二个块“record”填充了商品代码值的行。</span><span class="sxs-lookup"><span data-stu-id="573e0-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="573e0-190">在树中，选择“内部统计\数据: 序列\发货?”。</span><span class="sxs-lookup"><span data-stu-id="573e0-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="573e0-191">单击“已收集的数据键名”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="573e0-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="573e0-192">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="573e0-193">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="573e0-193">Click Add data source.</span></span>
57. <span data-ttu-id="573e0-194">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-194">Click Save.</span></span>
58. <span data-ttu-id="573e0-195">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-195">Close the page.</span></span>
59. <span data-ttu-id="573e0-196">单击“已收集的数据键值”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="573e0-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="573e0-197">在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。</span><span class="sxs-lookup"><span data-stu-id="573e0-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="573e0-198">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-198">Click Save.</span></span>
62. <span data-ttu-id="573e0-199">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-199">Close the page.</span></span>
63. <span data-ttu-id="573e0-200">在树中，展开“内部统计\数据: 序列\发货: 序列?”。</span><span class="sxs-lookup"><span data-stu-id="573e0-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="573e0-201">在树中，展开“内部统计\数据: 序列\发货: 序列?\Record = Intrastat.CommodityRecord”。</span><span class="sxs-lookup"><span data-stu-id="573e0-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="573e0-202">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="573e0-202">Click the Format tab.</span></span>
66. <span data-ttu-id="573e0-203">在树中，选择“内部统计\数据\发货\记录\发票金额 EUR”。</span><span class="sxs-lookup"><span data-stu-id="573e0-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="573e0-204">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="573e0-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="573e0-205">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="573e0-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="573e0-206">在树中，选择“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="573e0-207">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="573e0-207">Click Add data source.</span></span>
71. <span data-ttu-id="573e0-208">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-208">Click Save.</span></span>
72. <span data-ttu-id="573e0-209">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-209">Close the page.</span></span>
    * <span data-ttu-id="573e0-210">汇总此序列的行的开票金额值。</span><span class="sxs-lookup"><span data-stu-id="573e0-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="573e0-211">结果将与名称“InvoicedAmountEUR”一起单独用于不同内部统计方向和商品代码。</span><span class="sxs-lookup"><span data-stu-id="573e0-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="573e0-212">请将其视为 Excel 电子表格中的虚拟创建。</span><span class="sxs-lookup"><span data-stu-id="573e0-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="573e0-213">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。</span><span class="sxs-lookup"><span data-stu-id="573e0-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="573e0-214">第二个块“record”填充了商品代码值，第三个列“InvoicedAmountEUR”则填充了发票金额值。</span><span class="sxs-lookup"><span data-stu-id="573e0-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="573e0-215">在树中，展开“内部统计\数据\到货?”。</span><span class="sxs-lookup"><span data-stu-id="573e0-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="573e0-216">在树中，展开“内部统计\数据: 序列\到货?\Record = Intrastat.CommodityRecord”。</span><span class="sxs-lookup"><span data-stu-id="573e0-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="573e0-217">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="573e0-217">Click the Format tab.</span></span>
76. <span data-ttu-id="573e0-218">在树中，选择“内部统计\数据\到货\记录\发票金额 EUR”。</span><span class="sxs-lookup"><span data-stu-id="573e0-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="573e0-219">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="573e0-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="573e0-220">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="573e0-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="573e0-221">在树中，选择“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="573e0-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="573e0-222">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="573e0-222">Click Add data source.</span></span>
81. <span data-ttu-id="573e0-223">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-223">Click Save.</span></span>
82. <span data-ttu-id="573e0-224">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-224">Close the page.</span></span>
83. <span data-ttu-id="573e0-225">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="573e0-225">Click Save.</span></span>
84. <span data-ttu-id="573e0-226">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="573e0-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]