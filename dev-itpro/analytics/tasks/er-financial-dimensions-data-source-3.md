--- 
title: "针对电子申报 (ER) 将报表设计为使用财务维度作为数据源"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。"
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02787c96077e8bae54d8073e8d0770613ea2b49a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="bee9a-103">针对电子申报 (ER) 将报表设计为使用财务维度作为数据源</span><span class="sxs-lookup"><span data-stu-id="bee9a-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bee9a-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="bee9a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="bee9a-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="bee9a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bee9a-106">若要完成这些步骤，必须首先完成“ER 将财务维度用作数据源（第 2 部分：模型映射）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="bee9a-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="bee9a-107">设计报表以表示财务维度</span><span class="sxs-lookup"><span data-stu-id="bee9a-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="bee9a-108">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bee9a-109">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bee9a-110">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="bee9a-111">在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="bee9a-112">将提前创建的模型用作新报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="bee9a-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="bee9a-113">在“名称”字段中，键入“分类日记帐报表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="bee9a-114">在“数据模型定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="bee9a-115">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-115">Click Create configuration.</span></span>
8. <span data-ttu-id="bee9a-116">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-116">Click Designer.</span></span>
9. <span data-ttu-id="bee9a-117">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="bee9a-118">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="bee9a-119">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="bee9a-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-120">Click OK.</span></span>
13. <span data-ttu-id="bee9a-121">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="bee9a-122">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="bee9a-123">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="bee9a-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-124">Click OK.</span></span>
17. <span data-ttu-id="bee9a-125">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="bee9a-126">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="bee9a-127">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="bee9a-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-128">Click OK.</span></span>
21. <span data-ttu-id="bee9a-129">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="bee9a-130">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="bee9a-131">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="bee9a-132">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="bee9a-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-133">Click OK.</span></span>
26. <span data-ttu-id="bee9a-134">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="bee9a-135">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="bee9a-136">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="bee9a-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-137">Click OK.</span></span>
30. <span data-ttu-id="bee9a-138">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="bee9a-139">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="bee9a-140">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="bee9a-141">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="bee9a-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-142">Click OK.</span></span>
35. <span data-ttu-id="bee9a-143">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="bee9a-144">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="bee9a-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-145">Click OK.</span></span>
38. <span data-ttu-id="bee9a-146">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="bee9a-147">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="bee9a-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-148">Click OK.</span></span>
41. <span data-ttu-id="bee9a-149">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="bee9a-150">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="bee9a-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-151">Click OK.</span></span>
44. <span data-ttu-id="bee9a-152">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="bee9a-153">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="bee9a-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-154">Click OK.</span></span>
47. <span data-ttu-id="bee9a-155">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="bee9a-156">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="bee9a-157">在“名称”字段中，键入“维度”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="bee9a-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-158">Click OK.</span></span>
51. <span data-ttu-id="bee9a-159">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="bee9a-160">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="bee9a-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="bee9a-161">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="bee9a-162">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="bee9a-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-163">Click OK.</span></span>
56. <span data-ttu-id="bee9a-164">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="bee9a-165">在“名称”字段中，键入“值”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="bee9a-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-166">Click OK.</span></span>
59. <span data-ttu-id="bee9a-167">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="bee9a-168">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="bee9a-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="bee9a-170">将报表元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="bee9a-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="bee9a-171">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="bee9a-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="bee9a-172">在树中，展开“模型: 数据模型财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bee9a-173">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="bee9a-174">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="bee9a-175">在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="bee9a-176">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\描述: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="bee9a-177">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\描述: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="bee9a-178">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-178">Click Bind.</span></span>
9. <span data-ttu-id="bee9a-179">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="bee9a-180">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="bee9a-181">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-181">Click Bind.</span></span>
12. <span data-ttu-id="bee9a-182">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素\值: XML 属性\代码: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="bee9a-183">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串\名称: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="bee9a-184">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-184">Click Bind.</span></span>
15. <span data-ttu-id="bee9a-185">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="bee9a-186">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\维度: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="bee9a-187">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-187">Click Bind.</span></span>
18. <span data-ttu-id="bee9a-188">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\贷方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="bee9a-189">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="bee9a-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-190">Click Bind.</span></span>
21. <span data-ttu-id="bee9a-191">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\借方: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="bee9a-192">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="bee9a-193">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-193">Click Bind.</span></span>
24. <span data-ttu-id="bee9a-194">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\币种: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="bee9a-195">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="bee9a-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-196">Click Bind.</span></span>
27. <span data-ttu-id="bee9a-197">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\日期: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="bee9a-198">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="bee9a-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-199">Click Bind.</span></span>
30. <span data-ttu-id="bee9a-200">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素\凭证: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="bee9a-201">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="bee9a-202">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-202">Click Bind.</span></span>
33. <span data-ttu-id="bee9a-203">在树中，选择“根: XML 元素\日记帐: XML 元素\交易: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="bee9a-204">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="bee9a-205">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-205">Click Bind.</span></span>
36. <span data-ttu-id="bee9a-206">在树中，选择“根: XML 元素\日记帐: XML 元素\批次: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="bee9a-207">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="bee9a-208">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-208">Click Bind.</span></span>
39. <span data-ttu-id="bee9a-209">在树中，选择“根: XML 元素\日记帐: XML 元素”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="bee9a-210">在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="bee9a-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-211">Click Bind.</span></span>
42. <span data-ttu-id="bee9a-212">在树中，选择“根: XML 元素\公司: XML 属性”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="bee9a-213">在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="bee9a-214">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-214">Click Bind.</span></span>
45. <span data-ttu-id="bee9a-215">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bee9a-215">Click Save.</span></span>
46. <span data-ttu-id="bee9a-216">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bee9a-216">Close the page.</span></span>


