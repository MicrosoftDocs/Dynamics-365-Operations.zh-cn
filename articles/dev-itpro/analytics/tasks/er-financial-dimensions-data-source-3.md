---
title: ER 将财务维度用作数据源（第 3 部分 - 设计报表）
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。
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
ms.openlocfilehash: 45096a728ad6f9e331b53b4e12ca0ff9317a3939
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544717"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="ee16f-103">ER 将财务维度用作数据源（第 3 部分：设计报表）</span><span class="sxs-lookup"><span data-stu-id="ee16f-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee16f-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="ee16f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ee16f-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="ee16f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ee16f-106">若要完成这些步骤，必须首先完成“ER 将财务维度用作数据源（第 2 部分：模型映射）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ee16f-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="ee16f-107">设计报表以表示财务维度</span><span class="sxs-lookup"><span data-stu-id="ee16f-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="ee16f-108">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ee16f-109">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ee16f-110">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ee16f-111">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="ee16f-112">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="ee16f-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="ee16f-113">在“名称”字段中，键入“分类日记帐报表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="ee16f-114">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="ee16f-115">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-115">Click Create configuration.</span></span>
8. <span data-ttu-id="ee16f-116">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-116">Click Designer.</span></span>
9. <span data-ttu-id="ee16f-117">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="ee16f-118">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="ee16f-119">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="ee16f-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-120">Click OK.</span></span>
13. <span data-ttu-id="ee16f-121">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="ee16f-122">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="ee16f-123">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="ee16f-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-124">Click OK.</span></span>
17. <span data-ttu-id="ee16f-125">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="ee16f-126">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="ee16f-127">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="ee16f-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-128">Click OK.</span></span>
21. <span data-ttu-id="ee16f-129">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="ee16f-130">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ee16f-131">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="ee16f-132">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="ee16f-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-133">Click OK.</span></span>
26. <span data-ttu-id="ee16f-134">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="ee16f-135">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="ee16f-136">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="ee16f-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-137">Click OK.</span></span>
30. <span data-ttu-id="ee16f-138">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="ee16f-139">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="ee16f-140">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="ee16f-141">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="ee16f-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-142">Click OK.</span></span>
35. <span data-ttu-id="ee16f-143">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="ee16f-144">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="ee16f-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-145">Click OK.</span></span>
38. <span data-ttu-id="ee16f-146">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="ee16f-147">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="ee16f-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-148">Click OK.</span></span>
41. <span data-ttu-id="ee16f-149">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="ee16f-150">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="ee16f-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-151">Click OK.</span></span>
44. <span data-ttu-id="ee16f-152">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="ee16f-153">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="ee16f-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-154">Click OK.</span></span>
47. <span data-ttu-id="ee16f-155">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="ee16f-156">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="ee16f-157">在“名称”字段中，键入“维度”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="ee16f-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-158">Click OK.</span></span>
51. <span data-ttu-id="ee16f-159">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="ee16f-160">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee16f-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="ee16f-161">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="ee16f-162">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="ee16f-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-163">Click OK.</span></span>
56. <span data-ttu-id="ee16f-164">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="ee16f-165">在“名称”字段中，键入“值”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="ee16f-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-166">Click OK.</span></span>
59. <span data-ttu-id="ee16f-167">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="ee16f-168">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="ee16f-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="ee16f-170">将报表元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="ee16f-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="ee16f-171">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ee16f-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ee16f-172">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ee16f-173">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="ee16f-174">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="ee16f-175">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="ee16f-176">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\描述: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="ee16f-177">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\描述: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="ee16f-178">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-178">Click Bind.</span></span>
9. <span data-ttu-id="ee16f-179">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="ee16f-180">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="ee16f-181">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-181">Click Bind.</span></span>
12. <span data-ttu-id="ee16f-182">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性\代码: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="ee16f-183">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串\名称: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="ee16f-184">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-184">Click Bind.</span></span>
15. <span data-ttu-id="ee16f-185">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="ee16f-186">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="ee16f-187">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-187">Click Bind.</span></span>
18. <span data-ttu-id="ee16f-188">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\贷方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="ee16f-189">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="ee16f-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-190">Click Bind.</span></span>
21. <span data-ttu-id="ee16f-191">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\借方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="ee16f-192">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="ee16f-193">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-193">Click Bind.</span></span>
24. <span data-ttu-id="ee16f-194">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\币种: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="ee16f-195">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="ee16f-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-196">Click Bind.</span></span>
27. <span data-ttu-id="ee16f-197">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\日期: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="ee16f-198">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="ee16f-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-199">Click Bind.</span></span>
30. <span data-ttu-id="ee16f-200">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\凭证: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="ee16f-201">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="ee16f-202">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-202">Click Bind.</span></span>
33. <span data-ttu-id="ee16f-203">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="ee16f-204">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="ee16f-205">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-205">Click Bind.</span></span>
36. <span data-ttu-id="ee16f-206">在树中，选择“根: XML 元素\日记帐: XML 元素\批次: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="ee16f-207">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="ee16f-208">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-208">Click Bind.</span></span>
39. <span data-ttu-id="ee16f-209">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="ee16f-210">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="ee16f-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-211">Click Bind.</span></span>
42. <span data-ttu-id="ee16f-212">在树中，选择“根: XML 元素\公司: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="ee16f-213">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="ee16f-214">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-214">Click Bind.</span></span>
45. <span data-ttu-id="ee16f-215">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ee16f-215">Click Save.</span></span>
46. <span data-ttu-id="ee16f-216">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ee16f-216">Close the page.</span></span>

