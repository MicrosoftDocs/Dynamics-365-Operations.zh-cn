--- 
title: "针对电子申报 (ER) 创建格式配置"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef33fec0162e3b379bc8fe563d37a88fa35dfc85
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="3d9f2-103">针对电子申报 (ER) 创建格式配置</span><span class="sxs-lookup"><span data-stu-id="3d9f2-103">Create a format configuration for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d9f2-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="3d9f2-105">此格式配置定义用于处理付款的电子单据的格式。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="3d9f2-106">为了完成这些步骤，您首先必须完成“映射模型到所选数据源”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="3d9f2-107">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="3d9f2-107">Create a new format configuration</span></span>
1. <span data-ttu-id="3d9f2-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3d9f2-109">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3d9f2-110">在树结构中，选择“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="3d9f2-111">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="3d9f2-112">在“新建”字段中，输入“基于数据模型付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="3d9f2-113">在“名称”字段中，键入“银行自动对帐系统（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="3d9f2-114">银行自动对帐系统（英国虚构）</span><span class="sxs-lookup"><span data-stu-id="3d9f2-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="3d9f2-115">在“描述”字段中，键入“银行自动对帐系统供应商付款格式（英国虚拟）”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="3d9f2-116">银行自动对帐系统供应商付款格式（英国虚构）</span><span class="sxs-lookup"><span data-stu-id="3d9f2-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="3d9f2-117">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="3d9f2-118">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="3d9f2-119">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="3d9f2-120">电子文档的特定格式可进行定义。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="3d9f2-121">如果您想要选择运行时间的格式，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="3d9f2-122">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="3d9f2-123">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-123">Click Create configuration.</span></span>
    * <span data-ttu-id="3d9f2-124">已创建新的配置。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-124">A new configuration has been created.</span></span> <span data-ttu-id="3d9f2-125">草稿版本可用于存储用于管理电子文档的设计格式。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="3d9f2-126">设计电子单据的格式</span><span class="sxs-lookup"><span data-stu-id="3d9f2-126">Design format of electronic document</span></span>
1. <span data-ttu-id="3d9f2-127">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-127">Click Designer.</span></span>
2. <span data-ttu-id="3d9f2-128">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="3d9f2-129">在树结构中，选择“常见\文件”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="3d9f2-130">在“名称”字段中，键入“Xml”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="3d9f2-131">Xml</span><span class="sxs-lookup"><span data-stu-id="3d9f2-131">Xml</span></span>  
5. <span data-ttu-id="3d9f2-132">在“编码”字段中，键入“UTF-8”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="3d9f2-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="3d9f2-133">UTF-8</span></span>  
6. <span data-ttu-id="3d9f2-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-134">Click OK.</span></span>
7. <span data-ttu-id="3d9f2-135">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="3d9f2-136">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="3d9f2-137">在“名称”字段中，键入“消息”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="3d9f2-138">消息</span><span class="sxs-lookup"><span data-stu-id="3d9f2-138">Message</span></span>  
10. <span data-ttu-id="3d9f2-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-139">Click OK.</span></span>
11. <span data-ttu-id="3d9f2-140">在树结构中，选择“Xml\消息”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="3d9f2-141">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-141">Click Add Element.</span></span>
13. <span data-ttu-id="3d9f2-142">在“名称”字段中，键入“处理日期”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="3d9f2-143">处理日期</span><span class="sxs-lookup"><span data-stu-id="3d9f2-143">ProcessingDate</span></span>  
14. <span data-ttu-id="3d9f2-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-144">Click OK.</span></span>
15. <span data-ttu-id="3d9f2-145">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-145">Click Add Element.</span></span>
16. <span data-ttu-id="3d9f2-146">在“名称”字段中，键入“消息 ID”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="3d9f2-147">消息标识</span><span class="sxs-lookup"><span data-stu-id="3d9f2-147">MessageId</span></span>  
17. <span data-ttu-id="3d9f2-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-148">Click OK.</span></span>
18. <span data-ttu-id="3d9f2-149">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-149">Click Add Element.</span></span>
19. <span data-ttu-id="3d9f2-150">在“名称”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="3d9f2-151">付款</span><span class="sxs-lookup"><span data-stu-id="3d9f2-151">Payments</span></span>  
20. <span data-ttu-id="3d9f2-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-152">Click OK.</span></span>
21. <span data-ttu-id="3d9f2-153">在树结构中，选择“Xml\消息\付款”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="3d9f2-154">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-154">Click Add Element.</span></span>
23. <span data-ttu-id="3d9f2-155">在“名称”字段中，键入“物料”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="3d9f2-156">项目</span><span class="sxs-lookup"><span data-stu-id="3d9f2-156">Item</span></span>  
24. <span data-ttu-id="3d9f2-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-157">Click OK.</span></span>
25. <span data-ttu-id="3d9f2-158">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="3d9f2-159">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="3d9f2-160">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="3d9f2-161">在“名称”字段中，键入“ID”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="3d9f2-162">ID</span><span class="sxs-lookup"><span data-stu-id="3d9f2-162">Id</span></span>  
29. <span data-ttu-id="3d9f2-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-163">Click OK.</span></span>
30. <span data-ttu-id="3d9f2-164">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="3d9f2-165">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="3d9f2-166">在“名称”字段中，键入“供应商”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="3d9f2-167">供应商</span><span class="sxs-lookup"><span data-stu-id="3d9f2-167">Vendor</span></span>  
33. <span data-ttu-id="3d9f2-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-168">Click OK.</span></span>
34. <span data-ttu-id="3d9f2-169">在树结构中，选择“Xml\消息\付款\项\供应商”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="3d9f2-170">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-170">Click Add Element.</span></span>
36. <span data-ttu-id="3d9f2-171">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="3d9f2-172">姓名</span><span class="sxs-lookup"><span data-stu-id="3d9f2-172">Name</span></span>  
37. <span data-ttu-id="3d9f2-173">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-173">Click OK.</span></span>
38. <span data-ttu-id="3d9f2-174">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-174">Click Add Element.</span></span>
39. <span data-ttu-id="3d9f2-175">在“名称”字段中，键入“银行”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="3d9f2-176">银行</span><span class="sxs-lookup"><span data-stu-id="3d9f2-176">Bank</span></span>  
40. <span data-ttu-id="3d9f2-177">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-177">Click OK.</span></span>
41. <span data-ttu-id="3d9f2-178">在树结构中，选择“Xml\消息\付款\项\供应商\银行”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="3d9f2-179">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-179">Click Add Element.</span></span>
43. <span data-ttu-id="3d9f2-180">在“名称”字段中，键入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="3d9f2-181">银行代号</span><span class="sxs-lookup"><span data-stu-id="3d9f2-181">RoutingNumber</span></span>  
44. <span data-ttu-id="3d9f2-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-182">Click OK.</span></span>
45. <span data-ttu-id="3d9f2-183">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-183">Click Add Element.</span></span>
46. <span data-ttu-id="3d9f2-184">在“名称”字段中，键入“帐号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="3d9f2-185">帐号</span><span class="sxs-lookup"><span data-stu-id="3d9f2-185">AccountNumber</span></span>  
47. <span data-ttu-id="3d9f2-186">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-186">Click OK.</span></span>
48. <span data-ttu-id="3d9f2-187">在树结构中，选择“Xml\消息\付款\项\供应商”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="3d9f2-188">单击“复制”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-188">Click Copy.</span></span>
50. <span data-ttu-id="3d9f2-189">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="3d9f2-190">单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-190">Click Paste.</span></span>
52. <span data-ttu-id="3d9f2-191">在“名称”字段中，键入“付款人”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="3d9f2-192">付款人</span><span class="sxs-lookup"><span data-stu-id="3d9f2-192">Payer</span></span>  
53. <span data-ttu-id="3d9f2-193">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="3d9f2-194">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-194">Click Add Element.</span></span>
55. <span data-ttu-id="3d9f2-195">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="3d9f2-196">币种</span><span class="sxs-lookup"><span data-stu-id="3d9f2-196">Currency</span></span>  
56. <span data-ttu-id="3d9f2-197">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-197">Click OK.</span></span>
57. <span data-ttu-id="3d9f2-198">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-198">Click Add Element.</span></span>
58. <span data-ttu-id="3d9f2-199">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="3d9f2-200">说明</span><span class="sxs-lookup"><span data-stu-id="3d9f2-200">Description</span></span>  
59. <span data-ttu-id="3d9f2-201">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-201">Click OK.</span></span>
60. <span data-ttu-id="3d9f2-202">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-202">Click Add Element.</span></span>
61. <span data-ttu-id="3d9f2-203">在“名称”字段中，键入“交易日期”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="3d9f2-204">交易日期</span><span class="sxs-lookup"><span data-stu-id="3d9f2-204">TransDate</span></span>  
62. <span data-ttu-id="3d9f2-205">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-205">Click OK.</span></span>
63. <span data-ttu-id="3d9f2-206">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-206">Click Add Element.</span></span>
64. <span data-ttu-id="3d9f2-207">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="3d9f2-208">本币金额</span><span class="sxs-lookup"><span data-stu-id="3d9f2-208">Amount</span></span>  
65. <span data-ttu-id="3d9f2-209">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="3d9f2-210">准备映射到数据模型元素的格式部分</span><span class="sxs-lookup"><span data-stu-id="3d9f2-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="3d9f2-211">在树结构中，选择“Xml\消息\处理日期”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="3d9f2-212">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="3d9f2-213">在树结构中，选择“文本'日期时间”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="3d9f2-214">在“格式”字段中，键入“年-月-日”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="3d9f2-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="3d9f2-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="3d9f2-216">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-216">Click OK.</span></span>
6. <span data-ttu-id="3d9f2-217">在树结构中，选择“Xml\消息\付款\项\交易日期”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="3d9f2-218">单击"添加日期时间"。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="3d9f2-219">在“格式”字段中，键入“年-月-日”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="3d9f2-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="3d9f2-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="3d9f2-221">在“日期时间类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="3d9f2-222">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-222">Click OK.</span></span>
11. <span data-ttu-id="3d9f2-223">在树结构中，选择“Xml\消息\消息标识”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="3d9f2-224">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="3d9f2-225">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="3d9f2-226">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-226">Click OK.</span></span>
15. <span data-ttu-id="3d9f2-227">在树结构中，选择“Xml\消息\付款\项\供应商\名称”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="3d9f2-228">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-228">Click Add String.</span></span>
17. <span data-ttu-id="3d9f2-229">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-229">Click OK.</span></span>
18. <span data-ttu-id="3d9f2-230">在树结构中，选择“Xml\消息\付款\项\供应商\银行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="3d9f2-231">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-231">Click Add String.</span></span>
20. <span data-ttu-id="3d9f2-232">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-232">Click OK.</span></span>
21. <span data-ttu-id="3d9f2-233">在树结构中，选择“Xml\消息\付款\项\供应商\银行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="3d9f2-234">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-234">Click Add String.</span></span>
23. <span data-ttu-id="3d9f2-235">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-235">Click OK.</span></span>
24. <span data-ttu-id="3d9f2-236">在树结构中，选择“Xml\消息\付款\项\付款人\名称”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="3d9f2-237">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-237">Click Add String.</span></span>
26. <span data-ttu-id="3d9f2-238">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-238">Click OK.</span></span>
27. <span data-ttu-id="3d9f2-239">在树结构中，选择“Xml\消息\付款\项\付款人\银行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="3d9f2-240">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-240">Click Add String.</span></span>
29. <span data-ttu-id="3d9f2-241">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-241">Click OK.</span></span>
30. <span data-ttu-id="3d9f2-242">在树结构中，选择“Xml\消息\付款\项\付款人\银行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="3d9f2-243">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-243">Click Add String.</span></span>
32. <span data-ttu-id="3d9f2-244">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-244">Click OK.</span></span>
33. <span data-ttu-id="3d9f2-245">在树结构中，选择“Xml\消息\付款\项\货币”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="3d9f2-246">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-246">Click Add String.</span></span>
35. <span data-ttu-id="3d9f2-247">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-247">Click OK.</span></span>
36. <span data-ttu-id="3d9f2-248">在树结构中，选择“Xml\消息\付款\项\描述”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="3d9f2-249">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-249">Click Add String.</span></span>
38. <span data-ttu-id="3d9f2-250">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-250">Click OK.</span></span>
39. <span data-ttu-id="3d9f2-251">在树结构中，选择“Xml\消息\付款\项\金额”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="3d9f2-252">单击“添加字符串”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-252">Click Add String.</span></span>
41. <span data-ttu-id="3d9f2-253">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-253">Click OK.</span></span>
42. <span data-ttu-id="3d9f2-254">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-254">Click Save.</span></span>
43. <span data-ttu-id="3d9f2-255">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3d9f2-255">Close the page.</span></span>


