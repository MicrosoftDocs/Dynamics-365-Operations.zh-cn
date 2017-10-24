--- 
title: "针对电子申报 (ER) 配置计算以执行盘点和合计"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7b9035d8e7baf3c7ecb063b104b9a567be60840
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="configure-computations-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="6c3e6-103">针对电子申报 (ER) 配置计算以执行盘点和合计</span><span class="sxs-lookup"><span data-stu-id="6c3e6-103">Configure computations to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c3e6-104">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6c3e6-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6c3e6-106">必须首先完成“ER 配置格式以执行盘点和合计（第 1 部分：创建格式）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="6c3e6-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="6c3e6-108">创建格式配置以添加盘点和合计详细信息</span><span class="sxs-lookup"><span data-stu-id="6c3e6-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="6c3e6-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6c3e6-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6c3e6-111">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="6c3e6-112">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="6c3e6-113">假设您需要通过在内部统计报表结尾添加包含摘要详细信息的行，自定义 Microsoft 提供的格式。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="6c3e6-114">方法是从 Microsoft 实例派生自己的内部统计配置实例来进行修改。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="6c3e6-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="6c3e6-116">在“新建”字段中，输入“从以下名称派生: 内部统计 (DE)、Microsoft”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="6c3e6-117">在“名称”字段中，键入“带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="6c3e6-118">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="6c3e6-119">配置此报表以基于输出详细信息执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="6c3e6-120">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-120">Click Designer.</span></span>
2. <span data-ttu-id="6c3e6-121">在“收集输出详细信息”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="6c3e6-122">此标记将在运行时激活收集输出详细信息的过程，以便生成内部统计文件。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="6c3e6-123">您需要对不同内部统计放心执行盘点，以便向数据源的此格式配置列表添加专门的模型枚举。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="6c3e6-124">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="6c3e6-125">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="6c3e6-126">在树结构中，选择“数据模型\枚举”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="6c3e6-127">在“名称”字段中，键入“Direction”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="6c3e6-128">在“模型枚举”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="6c3e6-129">选择值“方向”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="6c3e6-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-130">Click OK.</span></span>
9. <span data-ttu-id="6c3e6-131">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="6c3e6-132">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="6c3e6-133">在“名称”字段中，键入“$BlockName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="6c3e6-134">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-134">Click Edit formula.</span></span>
13. <span data-ttu-id="6c3e6-135">在“公式”字段中，输入“block”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="6c3e6-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-136">Click Save.</span></span>
15. <span data-ttu-id="6c3e6-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-137">Close the page.</span></span>
16. <span data-ttu-id="6c3e6-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-138">Click OK.</span></span>
17. <span data-ttu-id="6c3e6-139">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="6c3e6-140">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="6c3e6-141">在“名称”字段中，键入“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="6c3e6-142">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-142">Click Edit formula.</span></span>
21. <span data-ttu-id="6c3e6-143">在“公式”字段中，输入“record”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="6c3e6-144">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-144">Click Save.</span></span>
23. <span data-ttu-id="6c3e6-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-145">Close the page.</span></span>
24. <span data-ttu-id="6c3e6-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-146">Click OK.</span></span>
25. <span data-ttu-id="6c3e6-147">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="6c3e6-148">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="6c3e6-149">在“名称”字段中，键入“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="6c3e6-150">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-150">Click Edit formula.</span></span>
29. <span data-ttu-id="6c3e6-151">在“公式”字段中，输入“InvoicedAmountEUR”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="6c3e6-152">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-152">Click Save.</span></span>
31. <span data-ttu-id="6c3e6-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-153">Close the page.</span></span>
32. <span data-ttu-id="6c3e6-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-154">Click OK.</span></span>
33. <span data-ttu-id="6c3e6-155">在树结构中，选择“内部统计\数据”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="6c3e6-156">单击“已收集的数据键名”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="6c3e6-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="6c3e6-157">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-157">Click Add data source.</span></span>
    * <span data-ttu-id="6c3e6-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="6c3e6-158">$BlockName</span></span>  
36. <span data-ttu-id="6c3e6-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-159">Click Save.</span></span>
37. <span data-ttu-id="6c3e6-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-160">Close the page.</span></span>
38. <span data-ttu-id="6c3e6-161">单击“已收集的数据键值”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="6c3e6-162">在“公式”字段中，输入“IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="6c3e6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="6c3e6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="6c3e6-164">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-164">Click Save.</span></span>
41. <span data-ttu-id="6c3e6-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-165">Close the page.</span></span>
    * <span data-ttu-id="6c3e6-166">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-166">Count the lines of this sequence.</span></span> <span data-ttu-id="6c3e6-167">结果将与名称“block”一起单独用于不同方向。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="6c3e6-168">值“Import”将用于任何到货内部统计交易。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="6c3e6-169">值“Export”将用于任何内部统计发货交易。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="6c3e6-170">请将其视为虚拟 Excel 电子表格。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="6c3e6-171">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="6c3e6-172">在树中，展开“内部统计\数据: 序列”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="6c3e6-173">在树中，选择“内部统计\数据: 序列\到货?”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="6c3e6-174">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="6c3e6-175">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-175">Count the lines of this sequence.</span></span> <span data-ttu-id="6c3e6-176">将使用名称“记录”记忆结果。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="6c3e6-177">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="6c3e6-178">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-178">Click Add data source.</span></span>
47. <span data-ttu-id="6c3e6-179">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-179">Click Save.</span></span>
48. <span data-ttu-id="6c3e6-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-180">Close the page.</span></span>
49. <span data-ttu-id="6c3e6-181">单击“已收集的数据键值”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="6c3e6-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="6c3e6-182">在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="6c3e6-183">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-183">Click Save.</span></span>
52. <span data-ttu-id="6c3e6-184">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-184">Close the page.</span></span>
    * <span data-ttu-id="6c3e6-185">统计此序列的行数。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-185">Count the lines of this sequence.</span></span> <span data-ttu-id="6c3e6-186">结果将与名称“record”一起单独用于不同商品代码。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="6c3e6-187">请将其视为虚拟 Excel 电子表格。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="6c3e6-188">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”且第二个块“record”填充了商品代码值的行。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="6c3e6-189">在树中，选择“内部统计\数据: 序列\发货?”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="6c3e6-190">单击“已收集的数据键名”字段中的“编辑”按钮</span><span class="sxs-lookup"><span data-stu-id="6c3e6-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="6c3e6-191">在树中，选择“$RecName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="6c3e6-192">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-192">Click Add data source.</span></span>
57. <span data-ttu-id="6c3e6-193">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-193">Click Save.</span></span>
58. <span data-ttu-id="6c3e6-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-194">Close the page.</span></span>
59. <span data-ttu-id="6c3e6-195">单击“已收集的数据键值”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="6c3e6-196">在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="6c3e6-197">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-197">Click Save.</span></span>
62. <span data-ttu-id="6c3e6-198">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-198">Close the page.</span></span>
63. <span data-ttu-id="6c3e6-199">在树中，展开“内部统计\数据: 序列\发货: 序列?”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="6c3e6-200">在树中，展开“内部统计\数据: 序列\发货: 序列?\Record = Intrastat.CommodityRecord”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="6c3e6-201">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-201">Click the Format tab.</span></span>
66. <span data-ttu-id="6c3e6-202">在树中，选择“内部统计\数据\发货\记录\发票金额 EUR”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="6c3e6-203">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="6c3e6-204">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="6c3e6-205">在树中，选择“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="6c3e6-206">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-206">Click Add data source.</span></span>
71. <span data-ttu-id="6c3e6-207">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-207">Click Save.</span></span>
72. <span data-ttu-id="6c3e6-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-208">Close the page.</span></span>
    * <span data-ttu-id="6c3e6-209">汇总此序列的行的开票金额值。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="6c3e6-210">结果将与名称“InvoicedAmountEUR”一起单独用于不同内部统计方向和商品代码。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="6c3e6-211">请将其视为 Excel 电子表格中的虚拟创建。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="6c3e6-212">对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="6c3e6-213">第二个块“record”填充了商品代码值，第三个列“InvoicedAmountEUR”则填充了发票金额值。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="6c3e6-214">在树中，展开“内部统计\数据\到货?”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="6c3e6-215">在树中，展开“内部统计\数据: 序列\到货?\Record = Intrastat.CommodityRecord”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="6c3e6-216">单击“公式”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-216">Click the Format tab.</span></span>
76. <span data-ttu-id="6c3e6-217">在树中，选择“内部统计\数据\到货\记录\发票金额 EUR”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="6c3e6-218">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="6c3e6-219">单击“已收集的数据键名”字段中的“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="6c3e6-220">在树中，选择“$InvName”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="6c3e6-221">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-221">Click Add data source.</span></span>
81. <span data-ttu-id="6c3e6-222">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-222">Click Save.</span></span>
82. <span data-ttu-id="6c3e6-223">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-223">Close the page.</span></span>
83. <span data-ttu-id="6c3e6-224">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-224">Click Save.</span></span>
84. <span data-ttu-id="6c3e6-225">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-225">Close the page.</span></span>

