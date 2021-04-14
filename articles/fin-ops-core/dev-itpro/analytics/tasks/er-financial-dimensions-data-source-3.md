---
title: ER 将财务维度用作数据源（第 3 部分 - 设计报表）
description: 本主题介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 3 部分）
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752404"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="1fc5a-104">ER 将财务维度用作数据源（第 3 部分 - 设计报表）</span><span class="sxs-lookup"><span data-stu-id="1fc5a-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1fc5a-105">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="1fc5a-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="1fc5a-107">若要完成这些步骤，必须首先完成“ER 将财务维度用作数据源（第 2 部分：模型映射）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="1fc5a-108">设计报表以表示财务维度</span><span class="sxs-lookup"><span data-stu-id="1fc5a-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="1fc5a-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1fc5a-110">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1fc5a-111">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1fc5a-112">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="1fc5a-113">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="1fc5a-114">在“名称”字段中，键入“分类日记帐报表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="1fc5a-115">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="1fc5a-116">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-116">Click Create configuration.</span></span>
8. <span data-ttu-id="1fc5a-117">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-117">Click Designer.</span></span>
9. <span data-ttu-id="1fc5a-118">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="1fc5a-119">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="1fc5a-120">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="1fc5a-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-121">Click OK.</span></span>
13. <span data-ttu-id="1fc5a-122">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="1fc5a-123">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="1fc5a-124">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="1fc5a-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-125">Click OK.</span></span>
17. <span data-ttu-id="1fc5a-126">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="1fc5a-127">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="1fc5a-128">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="1fc5a-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-129">Click OK.</span></span>
21. <span data-ttu-id="1fc5a-130">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="1fc5a-131">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="1fc5a-132">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="1fc5a-133">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="1fc5a-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-134">Click OK.</span></span>
26. <span data-ttu-id="1fc5a-135">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="1fc5a-136">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="1fc5a-137">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="1fc5a-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-138">Click OK.</span></span>
30. <span data-ttu-id="1fc5a-139">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="1fc5a-140">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="1fc5a-141">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="1fc5a-142">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="1fc5a-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-143">Click OK.</span></span>
35. <span data-ttu-id="1fc5a-144">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="1fc5a-145">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="1fc5a-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-146">Click OK.</span></span>
38. <span data-ttu-id="1fc5a-147">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="1fc5a-148">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="1fc5a-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-149">Click OK.</span></span>
41. <span data-ttu-id="1fc5a-150">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="1fc5a-151">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="1fc5a-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-152">Click OK.</span></span>
44. <span data-ttu-id="1fc5a-153">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="1fc5a-154">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="1fc5a-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-155">Click OK.</span></span>
47. <span data-ttu-id="1fc5a-156">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="1fc5a-157">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="1fc5a-158">在“名称”字段中，键入“维度”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="1fc5a-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-159">Click OK.</span></span>
51. <span data-ttu-id="1fc5a-160">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="1fc5a-161">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="1fc5a-162">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="1fc5a-163">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="1fc5a-164">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-164">Click OK.</span></span>
56. <span data-ttu-id="1fc5a-165">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="1fc5a-166">在“名称”字段中，键入“值”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="1fc5a-167">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-167">Click OK.</span></span>
59. <span data-ttu-id="1fc5a-168">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="1fc5a-169">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="1fc5a-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-170">Click OK.</span></span>
<span data-ttu-id="1fc5a-171">![ER Operations 设计器页](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="1fc5a-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="1fc5a-172">将报表元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="1fc5a-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="1fc5a-173">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1fc5a-174">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1fc5a-175">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="1fc5a-176">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="1fc5a-177">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="1fc5a-178">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\描述: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="1fc5a-179">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\描述: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="1fc5a-180">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-180">Click Bind.</span></span>
9. <span data-ttu-id="1fc5a-181">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="1fc5a-182">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="1fc5a-183">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-183">Click Bind.</span></span>
12. <span data-ttu-id="1fc5a-184">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性\代码: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="1fc5a-185">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串\名称: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="1fc5a-186">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-186">Click Bind.</span></span>
15. <span data-ttu-id="1fc5a-187">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="1fc5a-188">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="1fc5a-189">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-189">Click Bind.</span></span>
18. <span data-ttu-id="1fc5a-190">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\贷方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="1fc5a-191">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="1fc5a-192">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-192">Click Bind.</span></span>
21. <span data-ttu-id="1fc5a-193">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\借方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="1fc5a-194">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="1fc5a-195">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-195">Click Bind.</span></span>
24. <span data-ttu-id="1fc5a-196">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\币种: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="1fc5a-197">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="1fc5a-198">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-198">Click Bind.</span></span>
27. <span data-ttu-id="1fc5a-199">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\日期: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="1fc5a-200">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="1fc5a-201">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-201">Click Bind.</span></span>
30. <span data-ttu-id="1fc5a-202">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\凭证: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="1fc5a-203">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="1fc5a-204">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-204">Click Bind.</span></span>
33. <span data-ttu-id="1fc5a-205">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="1fc5a-206">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="1fc5a-207">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-207">Click Bind.</span></span>
36. <span data-ttu-id="1fc5a-208">在树中，选择“根: XML 元素\日记帐: XML 元素\批次: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="1fc5a-209">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="1fc5a-210">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-210">Click Bind.</span></span>
39. <span data-ttu-id="1fc5a-211">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="1fc5a-212">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="1fc5a-213">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-213">Click Bind.</span></span>
42. <span data-ttu-id="1fc5a-214">在树中，选择“根: XML 元素\公司: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="1fc5a-215">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="1fc5a-216">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-216">Click Bind.</span></span>
45. <span data-ttu-id="1fc5a-217">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-217">Click Save.</span></span>
46. <span data-ttu-id="1fc5a-218">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1fc5a-218">Close the page.</span></span>
<span data-ttu-id="1fc5a-219">![ER Operations 设计器页](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="1fc5a-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]