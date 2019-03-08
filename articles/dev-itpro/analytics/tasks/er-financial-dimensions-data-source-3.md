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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "362985"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="1c016-103">ER 将财务维度用作数据源（第 3 部分：设计报表）</span><span class="sxs-lookup"><span data-stu-id="1c016-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c016-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="1c016-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="1c016-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="1c016-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1c016-106">若要完成这些步骤，必须首先完成“ER 将财务维度用作数据源（第 2 部分：模型映射）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c016-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="1c016-107">设计报表以表示财务维度</span><span class="sxs-lookup"><span data-stu-id="1c016-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="1c016-108">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="1c016-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1c016-109">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1c016-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1c016-110">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1c016-111">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1c016-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="1c016-112">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="1c016-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="1c016-113">在“名称”字段中，键入“分类日记帐报表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="1c016-114">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="1c016-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="1c016-115">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="1c016-115">Click Create configuration.</span></span>
8. <span data-ttu-id="1c016-116">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="1c016-116">Click Designer.</span></span>
9. <span data-ttu-id="1c016-117">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="1c016-118">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="1c016-119">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="1c016-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="1c016-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-120">Click OK.</span></span>
13. <span data-ttu-id="1c016-121">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="1c016-122">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="1c016-123">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="1c016-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="1c016-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-124">Click OK.</span></span>
17. <span data-ttu-id="1c016-125">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="1c016-126">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="1c016-127">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="1c016-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="1c016-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-128">Click OK.</span></span>
21. <span data-ttu-id="1c016-129">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="1c016-130">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="1c016-131">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="1c016-132">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="1c016-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="1c016-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-133">Click OK.</span></span>
26. <span data-ttu-id="1c016-134">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="1c016-135">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="1c016-136">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="1c016-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="1c016-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-137">Click OK.</span></span>
30. <span data-ttu-id="1c016-138">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="1c016-139">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="1c016-140">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="1c016-141">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="1c016-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="1c016-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-142">Click OK.</span></span>
35. <span data-ttu-id="1c016-143">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="1c016-144">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="1c016-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="1c016-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-145">Click OK.</span></span>
38. <span data-ttu-id="1c016-146">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="1c016-147">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="1c016-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="1c016-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-148">Click OK.</span></span>
41. <span data-ttu-id="1c016-149">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="1c016-150">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="1c016-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="1c016-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-151">Click OK.</span></span>
44. <span data-ttu-id="1c016-152">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="1c016-153">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="1c016-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="1c016-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-154">Click OK.</span></span>
47. <span data-ttu-id="1c016-155">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="1c016-156">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="1c016-157">在“名称”字段中，键入“维度”。</span><span class="sxs-lookup"><span data-stu-id="1c016-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="1c016-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-158">Click OK.</span></span>
51. <span data-ttu-id="1c016-159">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="1c016-160">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1c016-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="1c016-161">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="1c016-162">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="1c016-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="1c016-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-163">Click OK.</span></span>
56. <span data-ttu-id="1c016-164">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="1c016-165">在“名称”字段中，键入“值”。</span><span class="sxs-lookup"><span data-stu-id="1c016-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="1c016-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-166">Click OK.</span></span>
59. <span data-ttu-id="1c016-167">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="1c016-168">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="1c016-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="1c016-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="1c016-170">将报表元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="1c016-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="1c016-171">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="1c016-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1c016-172">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="1c016-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1c016-173">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="1c016-174">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="1c016-175">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="1c016-176">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\描述: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="1c016-177">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\描述: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="1c016-178">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-178">Click Bind.</span></span>
9. <span data-ttu-id="1c016-179">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="1c016-180">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="1c016-181">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-181">Click Bind.</span></span>
12. <span data-ttu-id="1c016-182">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性\代码: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="1c016-183">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串\名称: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="1c016-184">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-184">Click Bind.</span></span>
15. <span data-ttu-id="1c016-185">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="1c016-186">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="1c016-187">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-187">Click Bind.</span></span>
18. <span data-ttu-id="1c016-188">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\贷方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="1c016-189">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="1c016-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="1c016-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-190">Click Bind.</span></span>
21. <span data-ttu-id="1c016-191">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\借方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="1c016-192">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="1c016-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="1c016-193">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-193">Click Bind.</span></span>
24. <span data-ttu-id="1c016-194">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\币种: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="1c016-195">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="1c016-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-196">Click Bind.</span></span>
27. <span data-ttu-id="1c016-197">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\日期: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="1c016-198">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="1c016-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="1c016-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-199">Click Bind.</span></span>
30. <span data-ttu-id="1c016-200">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\凭证: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="1c016-201">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="1c016-202">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-202">Click Bind.</span></span>
33. <span data-ttu-id="1c016-203">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="1c016-204">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="1c016-205">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-205">Click Bind.</span></span>
36. <span data-ttu-id="1c016-206">在树中，选择“根: XML 元素\日记帐: XML 元素\批次: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="1c016-207">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="1c016-208">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-208">Click Bind.</span></span>
39. <span data-ttu-id="1c016-209">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="1c016-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="1c016-210">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="1c016-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="1c016-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-211">Click Bind.</span></span>
42. <span data-ttu-id="1c016-212">在树中，选择“根: XML 元素\公司: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="1c016-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="1c016-213">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="1c016-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="1c016-214">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="1c016-214">Click Bind.</span></span>
45. <span data-ttu-id="1c016-215">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="1c016-215">Click Save.</span></span>
46. <span data-ttu-id="1c016-216">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1c016-216">Close the page.</span></span>

