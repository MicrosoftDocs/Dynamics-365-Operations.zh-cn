--- 
title: "ER 创建格式配置（2016 年 11 月）"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。"
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
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
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="2ded3-103">ER 创建格式配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="2ded3-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ded3-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。</span><span class="sxs-lookup"><span data-stu-id="2ded3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="2ded3-105">此格式配置定义用于处理付款的电子单据的格式。</span><span class="sxs-lookup"><span data-stu-id="2ded3-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="2ded3-106">为了完成这些步骤，您首先必须完成“映射模型到所选数据源”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="2ded3-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="2ded3-107">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="2ded3-107">Create a new format configuration</span></span>
1. <span data-ttu-id="2ded3-108">转到**组织管理 > 工作区 > 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="2ded3-109">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="2ded3-110">在树结构中，选择**付款（简化模型）**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="2ded3-111">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2ded3-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2ded3-112">如果您没有看到**创建配置**，您必须在**电子申报参数**页启用设计模式。</span><span class="sxs-lookup"><span data-stu-id="2ded3-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="2ded3-113">在**新建**字段中，输入**基于数据模型付款模型的格式**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="2ded3-114">在**名称**字段中，键入**银行自动对帐系统（英国虚构）**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="2ded3-115">在**描述**字段中，键入**银行自动对帐系统供应商付款格式（英国虚拟）**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="2ded3-116">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="2ded3-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="2ded3-117">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="2ded3-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="2ded3-118">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="2ded3-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="2ded3-119">电子文档的特定格式可进行定义。</span><span class="sxs-lookup"><span data-stu-id="2ded3-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="2ded3-120">如果您想要选择运行时间的格式，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="2ded3-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="2ded3-121">在**数据模型定义**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ded3-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="2ded3-122">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-122">Click **Create configuration**.</span></span> <span data-ttu-id="2ded3-123">已创建新的配置。</span><span class="sxs-lookup"><span data-stu-id="2ded3-123">A new configuration has been created.</span></span> <span data-ttu-id="2ded3-124">草稿版本可用于存储用于管理电子文档的设计格式。</span><span class="sxs-lookup"><span data-stu-id="2ded3-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="2ded3-125">如果您没有看到**创建配置**，您必须在**电子申报参数**页启用设计模式。</span><span class="sxs-lookup"><span data-stu-id="2ded3-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="2ded3-126">设计电子单据的格式</span><span class="sxs-lookup"><span data-stu-id="2ded3-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="2ded3-127">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-127">Click **Designer**.</span></span>
2. <span data-ttu-id="2ded3-128">单击**添加根**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2ded3-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="2ded3-129">在树结构中，选择**常见\文件**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="2ded3-130">在**名称**字段中，键入 **Xml**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="2ded3-131">在**编码**字段中，键入 **UTF-8**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="2ded3-132">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-132">Click **OK**.</span></span>
7. <span data-ttu-id="2ded3-133">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-133">Click **Add**.</span></span>
8. <span data-ttu-id="2ded3-134">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="2ded3-135">在**名称**字段中，键入**消息**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="2ded3-136">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-136">Click **OK**.</span></span>
11. <span data-ttu-id="2ded3-137">在树结构中，选择 **Xml\消息**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="2ded3-138">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="2ded3-139">在**名称**字段中，键入**处理日期**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="2ded3-140">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-140">Click **OK**.</span></span>
15. <span data-ttu-id="2ded3-141">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="2ded3-142">在“名称”字段中，键入**消息 ID**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="2ded3-143">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-143">Click **OK**.</span></span>
18. <span data-ttu-id="2ded3-144">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="2ded3-145">在**名称**字段中，键入**付款**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="2ded3-146">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-146">Click **OK**.</span></span>
21. <span data-ttu-id="2ded3-147">在树结构中，选择 **Xml\消息\付款**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="2ded3-148">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="2ded3-149">在**名称**字段中，键入**物料**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="2ded3-150">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-150">Click **OK**.</span></span>
25. <span data-ttu-id="2ded3-151">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="2ded3-152">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-152">Click **Add**.</span></span>
27. <span data-ttu-id="2ded3-153">在树结构中，选择 **XML\属性**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="2ded3-154">在“名称”字段中，键入 **Id**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="2ded3-155">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-155">Click **OK**.</span></span>
30. <span data-ttu-id="2ded3-156">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-156">Click **Add**.</span></span>
31. <span data-ttu-id="2ded3-157">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="2ded3-158">在“名称”字段中，键入**供应商**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="2ded3-159">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-159">Click **OK**.</span></span>
34. <span data-ttu-id="2ded3-160">在树结构中，选择 **Xml\消息\付款\项\供应商**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="2ded3-161">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="2ded3-162">在“名称”字段中，键入**名称**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="2ded3-163">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-163">Click **OK**.</span></span>
38. <span data-ttu-id="2ded3-164">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="2ded3-165">在**名称**字段中，键入**银行**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="2ded3-166">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-166">Click **OK**.</span></span>
41. <span data-ttu-id="2ded3-167">在树结构中，选择 **Xml\消息\付款\项\供应商\银行**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="2ded3-168">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="2ded3-169">在**名称**字段中，键入**银行代号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="2ded3-170">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-170">Click **OK**.</span></span>
45. <span data-ttu-id="2ded3-171">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="2ded3-172">在**名称**字段中，键入**帐号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="2ded3-173">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-173">Click **OK**.</span></span>
48. <span data-ttu-id="2ded3-174">在树结构中，选择 **Xml\消息\付款\项\供应商**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="2ded3-175">单击**复制**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-175">Click **Copy**.</span></span>
50. <span data-ttu-id="2ded3-176">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="2ded3-177">单击**粘贴**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-177">Click **Paste**.</span></span>
52. <span data-ttu-id="2ded3-178">在**名称**字段中，键入**付款人**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="2ded3-179">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="2ded3-180">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="2ded3-181">在**名称**字段中，键入**货币**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="2ded3-182">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-182">Click **OK**.</span></span>
57. <span data-ttu-id="2ded3-183">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="2ded3-184">在**名称**字段中，键入**描述**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="2ded3-185">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-185">Click **OK**.</span></span>
60. <span data-ttu-id="2ded3-186">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="2ded3-187">在“名称”字段中，键入**交易日期**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="2ded3-188">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-188">Click **OK**.</span></span>
63. <span data-ttu-id="2ded3-189">单击**添加元素**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="2ded3-190">在“名称”字段中，键入**金额**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="2ded3-191">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="2ded3-192">准备映射到数据模型元素的格式部分</span><span class="sxs-lookup"><span data-stu-id="2ded3-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="2ded3-193">在树结构中，选择 **Xml\消息\处理日期**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="2ded3-194">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2ded3-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="2ded3-195">在树结构中，选择**文本\日期时间**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="2ded3-196">在**格式**字段中，键入**年-月-日**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="2ded3-197">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-197">Click **OK**.</span></span>
6. <span data-ttu-id="2ded3-198">在树结构中，选择 **Xml\消息\付款\项\交易日期**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="2ded3-199">单击**添加日期时间**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="2ded3-200">在**格式**字段中，键入**年-月-日**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="2ded3-201">在**日期时间**类型字段中，选择**日期**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="2ded3-202">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-202">Click **OK**.</span></span>
11. <span data-ttu-id="2ded3-203">在树结构中，选择 **Xml\消息\消息标识**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="2ded3-204">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2ded3-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="2ded3-205">在树结构中，选择**文本\字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="2ded3-206">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-206">Click **OK**.</span></span>
15. <span data-ttu-id="2ded3-207">在树结构中，选择 **Xml\消息\付款\项\供应商\名称**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="2ded3-208">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-208">Click **Add String**.</span></span>
17. <span data-ttu-id="2ded3-209">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-209">Click **OK**.</span></span>
18. <span data-ttu-id="2ded3-210">在树结构中，选择 **Xml\消息\付款\项\供应商\银行\银行代号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="2ded3-211">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-211">Click **Add String**.</span></span>
20. <span data-ttu-id="2ded3-212">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-212">Click **OK**.</span></span>
21. <span data-ttu-id="2ded3-213">在树结构中，选择 **Xml\消息\付款\项\供应商\银行\帐号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="2ded3-214">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-214">Click **Add String**.</span></span>
23. <span data-ttu-id="2ded3-215">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-215">Click **OK**.</span></span>
24. <span data-ttu-id="2ded3-216">在树结构中，选择 **Xml\消息\付款\项\付款人\名称**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="2ded3-217">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-217">Click **Add String**.</span></span>
26. <span data-ttu-id="2ded3-218">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-218">Click **OK**.</span></span>
27. <span data-ttu-id="2ded3-219">在树结构中，选择 **Xml\消息\付款\项\付款人\银行\银行代号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="2ded3-220">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-220">Click **Add String**.</span></span>
29. <span data-ttu-id="2ded3-221">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-221">Click **OK**.</span></span>
30. <span data-ttu-id="2ded3-222">在树结构中，选择 **Xml\消息\付款\项\付款人\银行\帐号**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="2ded3-223">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-223">Click **Add String**.</span></span>
32. <span data-ttu-id="2ded3-224">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-224">Click **OK**.</span></span>
33. <span data-ttu-id="2ded3-225">在树结构中，选择 **Xml\消息\付款\项\货币**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="2ded3-226">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-226">Click **Add String**.</span></span>
35. <span data-ttu-id="2ded3-227">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-227">Click **OK**.</span></span>
36. <span data-ttu-id="2ded3-228">在树结构中，选择 **Xml\消息\付款\项\描述**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="2ded3-229">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-229">Click **Add String**.</span></span>
38. <span data-ttu-id="2ded3-230">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-230">Click **OK**.</span></span>
39. <span data-ttu-id="2ded3-231">在树结构中，选择 **Xml\消息\付款\项\金额**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="2ded3-232">单击**添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-232">Click **Add String**.</span></span>
41. <span data-ttu-id="2ded3-233">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-233">Click **OK**.</span></span>
42. <span data-ttu-id="2ded3-234">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="2ded3-234">Click **Save**.</span></span>
43. <span data-ttu-id="2ded3-235">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2ded3-235">Close the page.</span></span>


