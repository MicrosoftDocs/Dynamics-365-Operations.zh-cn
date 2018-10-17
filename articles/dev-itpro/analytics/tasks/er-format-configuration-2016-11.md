--- 
title: "ER 创建格式配置（2016 年 11 月）"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="0bf75-103">ER 创建格式配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="0bf75-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0bf75-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。</span><span class="sxs-lookup"><span data-stu-id="0bf75-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="0bf75-105">此格式配置定义用于处理付款的电子单据的格式。</span><span class="sxs-lookup"><span data-stu-id="0bf75-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="0bf75-106">为了完成这些步骤，您首先必须完成“映射模型到所选数据源”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="0bf75-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="0bf75-107">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="0bf75-107">Create a new format configuration</span></span>
1. <span data-ttu-id="0bf75-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0bf75-109">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0bf75-110">在树结构中，选择“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="0bf75-111">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="0bf75-112">在“新建”字段中，输入“基于数据模型付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="0bf75-113">在“名称”字段中，键入“银行自动对帐系统（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="0bf75-114">银行自动对帐系统（英国虚构）</span><span class="sxs-lookup"><span data-stu-id="0bf75-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="0bf75-115">在“描述”字段中，键入“银行自动对帐系统供应商付款格式（英国虚拟）”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="0bf75-116">银行自动对帐系统供应商付款格式（英国虚构）</span><span class="sxs-lookup"><span data-stu-id="0bf75-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="0bf75-117">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="0bf75-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0bf75-118">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="0bf75-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0bf75-119">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="0bf75-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="0bf75-120">电子文档的特定格式可进行定义。</span><span class="sxs-lookup"><span data-stu-id="0bf75-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="0bf75-121">如果您想要选择运行时间的格式，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="0bf75-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="0bf75-122">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0bf75-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="0bf75-123">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-123">Click Create configuration.</span></span>
    * <span data-ttu-id="0bf75-124">已创建新的配置。</span><span class="sxs-lookup"><span data-stu-id="0bf75-124">A new configuration has been created.</span></span> <span data-ttu-id="0bf75-125">草稿版本可用于存储用于管理电子文档的设计格式。</span><span class="sxs-lookup"><span data-stu-id="0bf75-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="0bf75-126">设计电子单据的格式</span><span class="sxs-lookup"><span data-stu-id="0bf75-126">Design format of electronic document</span></span>
1. <span data-ttu-id="0bf75-127">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-127">Click Designer.</span></span>
2. <span data-ttu-id="0bf75-128">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0bf75-129">在树结构中，选择“常见\文件”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="0bf75-130">在“名称”字段中，键入“Xml”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="0bf75-131">Xml</span><span class="sxs-lookup"><span data-stu-id="0bf75-131">Xml</span></span>  
5. <span data-ttu-id="0bf75-132">在“编码”字段中，键入“UTF-8”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0bf75-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0bf75-133">UTF-8</span></span>  
6. <span data-ttu-id="0bf75-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-134">Click OK.</span></span>
7. <span data-ttu-id="0bf75-135">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="0bf75-136">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="0bf75-137">在“名称”字段中，键入“消息”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="0bf75-138">消息</span><span class="sxs-lookup"><span data-stu-id="0bf75-138">Message</span></span>  
10. <span data-ttu-id="0bf75-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-139">Click OK.</span></span>
11. <span data-ttu-id="0bf75-140">在树结构中，选择“Xml\消息”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="0bf75-141">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-141">Click Add Element.</span></span>
13. <span data-ttu-id="0bf75-142">在“名称”字段中，键入“处理日期”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="0bf75-143">处理日期</span><span class="sxs-lookup"><span data-stu-id="0bf75-143">ProcessingDate</span></span>  
14. <span data-ttu-id="0bf75-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-144">Click OK.</span></span>
15. <span data-ttu-id="0bf75-145">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-145">Click Add Element.</span></span>
16. <span data-ttu-id="0bf75-146">在“名称”字段中，键入“消息 ID”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="0bf75-147">消息标识</span><span class="sxs-lookup"><span data-stu-id="0bf75-147">MessageId</span></span>  
17. <span data-ttu-id="0bf75-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-148">Click OK.</span></span>
18. <span data-ttu-id="0bf75-149">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-149">Click Add Element.</span></span>
19. <span data-ttu-id="0bf75-150">在“名称”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0bf75-151">付款</span><span class="sxs-lookup"><span data-stu-id="0bf75-151">Payments</span></span>  
20. <span data-ttu-id="0bf75-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-152">Click OK.</span></span>
21. <span data-ttu-id="0bf75-153">在树结构中，选择“Xml\消息\付款”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="0bf75-154">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-154">Click Add Element.</span></span>
23. <span data-ttu-id="0bf75-155">在“名称”字段中，键入“物料”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="0bf75-156">项目</span><span class="sxs-lookup"><span data-stu-id="0bf75-156">Item</span></span>  
24. <span data-ttu-id="0bf75-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-157">Click OK.</span></span>
25. <span data-ttu-id="0bf75-158">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="0bf75-159">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0bf75-160">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="0bf75-161">在“名称”字段中，键入“ID”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="0bf75-162">ID</span><span class="sxs-lookup"><span data-stu-id="0bf75-162">Id</span></span>  
29. <span data-ttu-id="0bf75-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-163">Click OK.</span></span>
30. <span data-ttu-id="0bf75-164">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="0bf75-165">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="0bf75-166">在“名称”字段中，键入“供应商”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="0bf75-167">供应商</span><span class="sxs-lookup"><span data-stu-id="0bf75-167">Vendor</span></span>  
33. <span data-ttu-id="0bf75-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-168">Click OK.</span></span>
34. <span data-ttu-id="0bf75-169">在树结构中，选择“Xml\消息\付款\项\供应商”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="0bf75-170">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-170">Click Add Element.</span></span>
36. <span data-ttu-id="0bf75-171">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0bf75-172">姓名</span><span class="sxs-lookup"><span data-stu-id="0bf75-172">Name</span></span>  
37. <span data-ttu-id="0bf75-173">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-173">Click OK.</span></span>
38. <span data-ttu-id="0bf75-174">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-174">Click Add Element.</span></span>
39. <span data-ttu-id="0bf75-175">在“名称”字段中，键入“银行”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="0bf75-176">银行</span><span class="sxs-lookup"><span data-stu-id="0bf75-176">Bank</span></span>  
40. <span data-ttu-id="0bf75-177">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-177">Click OK.</span></span>
41. <span data-ttu-id="0bf75-178">在树结构中，选择“Xml\消息\付款\项\供应商\银行”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="0bf75-179">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-179">Click Add Element.</span></span>
43. <span data-ttu-id="0bf75-180">在“名称”字段中，键入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0bf75-181">银行代号</span><span class="sxs-lookup"><span data-stu-id="0bf75-181">RoutingNumber</span></span>  
44. <span data-ttu-id="0bf75-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-182">Click OK.</span></span>
45. <span data-ttu-id="0bf75-183">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-183">Click Add Element.</span></span>
46. <span data-ttu-id="0bf75-184">在“名称”字段中，键入“帐号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="0bf75-185">帐号</span><span class="sxs-lookup"><span data-stu-id="0bf75-185">AccountNumber</span></span>  
47. <span data-ttu-id="0bf75-186">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-186">Click OK.</span></span>
48. <span data-ttu-id="0bf75-187">在树结构中，选择“Xml\消息\付款\项\供应商”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="0bf75-188">单击“复制”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-188">Click Copy.</span></span>
50. <span data-ttu-id="0bf75-189">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="0bf75-190">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-190">Click Paste.</span></span>
52. <span data-ttu-id="0bf75-191">在“名称”字段中，键入“付款人”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="0bf75-192">付款人</span><span class="sxs-lookup"><span data-stu-id="0bf75-192">Payer</span></span>  
53. <span data-ttu-id="0bf75-193">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="0bf75-194">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-194">Click Add Element.</span></span>
55. <span data-ttu-id="0bf75-195">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0bf75-196">币种</span><span class="sxs-lookup"><span data-stu-id="0bf75-196">Currency</span></span>  
56. <span data-ttu-id="0bf75-197">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-197">Click OK.</span></span>
57. <span data-ttu-id="0bf75-198">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-198">Click Add Element.</span></span>
58. <span data-ttu-id="0bf75-199">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0bf75-200">说明</span><span class="sxs-lookup"><span data-stu-id="0bf75-200">Description</span></span>  
59. <span data-ttu-id="0bf75-201">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-201">Click OK.</span></span>
60. <span data-ttu-id="0bf75-202">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-202">Click Add Element.</span></span>
61. <span data-ttu-id="0bf75-203">在“名称”字段中，键入“交易日期”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="0bf75-204">交易日期</span><span class="sxs-lookup"><span data-stu-id="0bf75-204">TransDate</span></span>  
62. <span data-ttu-id="0bf75-205">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-205">Click OK.</span></span>
63. <span data-ttu-id="0bf75-206">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-206">Click Add Element.</span></span>
64. <span data-ttu-id="0bf75-207">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="0bf75-208">本币金额</span><span class="sxs-lookup"><span data-stu-id="0bf75-208">Amount</span></span>  
65. <span data-ttu-id="0bf75-209">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="0bf75-210">准备映射到数据模型元素的格式部分</span><span class="sxs-lookup"><span data-stu-id="0bf75-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="0bf75-211">在树结构中，选择“Xml\消息\处理日期”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="0bf75-212">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="0bf75-213">在树结构中，选择“文本'日期时间”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="0bf75-214">在“格式”字段中，键入“年-月-日”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0bf75-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0bf75-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="0bf75-216">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-216">Click OK.</span></span>
6. <span data-ttu-id="0bf75-217">在树结构中，选择“Xml\消息\付款\项\交易日期”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="0bf75-218">单击"添加日期时间"。</span><span class="sxs-lookup"><span data-stu-id="0bf75-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="0bf75-219">在“格式”字段中，键入“年-月-日”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0bf75-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0bf75-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="0bf75-221">在“日期时间类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="0bf75-222">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-222">Click OK.</span></span>
11. <span data-ttu-id="0bf75-223">在树结构中，选择“Xml\消息\消息标识”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="0bf75-224">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0bf75-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="0bf75-225">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="0bf75-226">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-226">Click OK.</span></span>
15. <span data-ttu-id="0bf75-227">在树结构中，选择“Xml\消息\付款\项\供应商\名称”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="0bf75-228">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-228">Click Add String.</span></span>
17. <span data-ttu-id="0bf75-229">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-229">Click OK.</span></span>
18. <span data-ttu-id="0bf75-230">在树结构中，选择“Xml\消息\付款\项\供应商\银行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="0bf75-231">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-231">Click Add String.</span></span>
20. <span data-ttu-id="0bf75-232">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-232">Click OK.</span></span>
21. <span data-ttu-id="0bf75-233">在树结构中，选择“Xml\消息\付款\项\供应商\银行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="0bf75-234">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-234">Click Add String.</span></span>
23. <span data-ttu-id="0bf75-235">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-235">Click OK.</span></span>
24. <span data-ttu-id="0bf75-236">在树结构中，选择“Xml\消息\付款\项\付款人\名称”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="0bf75-237">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-237">Click Add String.</span></span>
26. <span data-ttu-id="0bf75-238">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-238">Click OK.</span></span>
27. <span data-ttu-id="0bf75-239">在树结构中，选择“Xml\消息\付款\项\付款人\银行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="0bf75-240">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-240">Click Add String.</span></span>
29. <span data-ttu-id="0bf75-241">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-241">Click OK.</span></span>
30. <span data-ttu-id="0bf75-242">在树结构中，选择“Xml\消息\付款\项\付款人\银行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="0bf75-243">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-243">Click Add String.</span></span>
32. <span data-ttu-id="0bf75-244">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-244">Click OK.</span></span>
33. <span data-ttu-id="0bf75-245">在树结构中，选择“Xml\消息\付款\项\货币”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="0bf75-246">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-246">Click Add String.</span></span>
35. <span data-ttu-id="0bf75-247">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-247">Click OK.</span></span>
36. <span data-ttu-id="0bf75-248">在树结构中，选择“Xml\消息\付款\项\描述”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="0bf75-249">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-249">Click Add String.</span></span>
38. <span data-ttu-id="0bf75-250">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-250">Click OK.</span></span>
39. <span data-ttu-id="0bf75-251">在树结构中，选择“Xml\消息\付款\项\金额”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="0bf75-252">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-252">Click Add String.</span></span>
41. <span data-ttu-id="0bf75-253">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-253">Click OK.</span></span>
42. <span data-ttu-id="0bf75-254">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0bf75-254">Click Save.</span></span>
43. <span data-ttu-id="0bf75-255">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0bf75-255">Close the page.</span></span>


