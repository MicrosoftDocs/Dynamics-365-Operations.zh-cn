---
title: ER 创建格式配置（2016 年 11 月）
description: 本主题说明如何为电子报告 (ER) 创建格式配置。
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9404d1e242c83d2103d1f24c42589c33b9f57f02
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092242"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="61630-103">ER 创建格式配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="61630-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61630-104">此主题说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。</span><span class="sxs-lookup"><span data-stu-id="61630-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="61630-105">此格式配置定义用于处理付款的电子单据的格式。</span><span class="sxs-lookup"><span data-stu-id="61630-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="61630-106">为了完成这些步骤，您首先必须完成“映射模型到所选数据源”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="61630-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="61630-107">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="61630-107">Create a new format configuration</span></span>
1. <span data-ttu-id="61630-108">转到 **组织管理 > 工作区 > 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="61630-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="61630-109">单击 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="61630-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="61630-110">在树结构中，选择 **付款（简化模型）**。</span><span class="sxs-lookup"><span data-stu-id="61630-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="61630-111">单击 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="61630-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="61630-112">如果您没有看到 **创建配置**，您必须在 **电子申报参数** 页启用设计模式。</span><span class="sxs-lookup"><span data-stu-id="61630-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="61630-113">在 **新建** 字段中，输入 **基于数据模型付款模型的格式**。</span><span class="sxs-lookup"><span data-stu-id="61630-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="61630-114">在 **名称** 字段中，键入 **银行自动对帐系统（英国虚构）**。</span><span class="sxs-lookup"><span data-stu-id="61630-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="61630-115">在 **描述** 字段中，键入 **银行自动对帐系统供应商付款格式（英国虚拟）**。</span><span class="sxs-lookup"><span data-stu-id="61630-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="61630-116">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="61630-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="61630-117">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="61630-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="61630-118">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="61630-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="61630-119">电子文档的特定格式可进行定义。</span><span class="sxs-lookup"><span data-stu-id="61630-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="61630-120">如果您想要选择运行时间的格式，则将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="61630-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="61630-121">在 **数据模型定义** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="61630-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="61630-122">单击 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="61630-122">Click **Create configuration**.</span></span> <span data-ttu-id="61630-123">已创建新的配置。</span><span class="sxs-lookup"><span data-stu-id="61630-123">A new configuration has been created.</span></span> <span data-ttu-id="61630-124">草稿版本可用于存储用于管理电子文档的设计格式。</span><span class="sxs-lookup"><span data-stu-id="61630-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="61630-125">设计电子单据的格式</span><span class="sxs-lookup"><span data-stu-id="61630-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="61630-126">单击 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="61630-126">Click **Designer**.</span></span>
2. <span data-ttu-id="61630-127">单击 **添加根** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="61630-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="61630-128">在树结构中，选择 **常见\文件**。</span><span class="sxs-lookup"><span data-stu-id="61630-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="61630-129">在 **名称** 字段中，键入 **Xml**。</span><span class="sxs-lookup"><span data-stu-id="61630-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="61630-130">在 **编码** 字段中，键入 **UTF-8**。</span><span class="sxs-lookup"><span data-stu-id="61630-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="61630-131">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-131">Click **OK**.</span></span>
7. <span data-ttu-id="61630-132">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="61630-132">Click **Add**.</span></span>
8. <span data-ttu-id="61630-133">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="61630-134">在 **名称** 字段中，键入 **消息**。</span><span class="sxs-lookup"><span data-stu-id="61630-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="61630-135">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-135">Click **OK**.</span></span>
11. <span data-ttu-id="61630-136">在树结构中，选择 **Xml\消息**。</span><span class="sxs-lookup"><span data-stu-id="61630-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="61630-137">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="61630-138">在 **名称** 字段中，键入 **处理日期**。</span><span class="sxs-lookup"><span data-stu-id="61630-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="61630-139">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-139">Click **OK**.</span></span>
15. <span data-ttu-id="61630-140">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="61630-141">在“名称”字段中，键入 **消息 ID**。</span><span class="sxs-lookup"><span data-stu-id="61630-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="61630-142">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-142">Click **OK**.</span></span>
18. <span data-ttu-id="61630-143">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="61630-144">在 **名称** 字段中，键入 **付款**。</span><span class="sxs-lookup"><span data-stu-id="61630-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="61630-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-145">Click **OK**.</span></span>
21. <span data-ttu-id="61630-146">在树结构中，选择 **Xml\消息\付款**。</span><span class="sxs-lookup"><span data-stu-id="61630-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="61630-147">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="61630-148">在 **名称** 字段中，键入 **物料**。</span><span class="sxs-lookup"><span data-stu-id="61630-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="61630-149">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-149">Click **OK**.</span></span>
25. <span data-ttu-id="61630-150">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="61630-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="61630-151">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="61630-151">Click **Add**.</span></span>
27. <span data-ttu-id="61630-152">在树结构中，选择 **XML\属性**。</span><span class="sxs-lookup"><span data-stu-id="61630-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="61630-153">在“名称”字段中，键入 **Id**。</span><span class="sxs-lookup"><span data-stu-id="61630-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="61630-154">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-154">Click **OK**.</span></span>
30. <span data-ttu-id="61630-155">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="61630-155">Click **Add**.</span></span>
31. <span data-ttu-id="61630-156">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="61630-157">在“名称”字段中，键入 **供应商**。</span><span class="sxs-lookup"><span data-stu-id="61630-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="61630-158">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-158">Click **OK**.</span></span>
34. <span data-ttu-id="61630-159">在树结构中，选择 **Xml\消息\付款\项\供应商**。</span><span class="sxs-lookup"><span data-stu-id="61630-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="61630-160">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="61630-161">在“名称”字段中，键入 **名称**。</span><span class="sxs-lookup"><span data-stu-id="61630-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="61630-162">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-162">Click **OK**.</span></span>
38. <span data-ttu-id="61630-163">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="61630-164">在 **名称** 字段中，键入 **银行**。</span><span class="sxs-lookup"><span data-stu-id="61630-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="61630-165">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-165">Click **OK**.</span></span>
41. <span data-ttu-id="61630-166">在树结构中，选择 **Xml\消息\付款\项\供应商\银行**。</span><span class="sxs-lookup"><span data-stu-id="61630-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="61630-167">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="61630-168">在 **名称** 字段中，键入 **银行代号**。</span><span class="sxs-lookup"><span data-stu-id="61630-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="61630-169">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-169">Click **OK**.</span></span>
45. <span data-ttu-id="61630-170">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="61630-171">在 **名称** 字段中，键入 **帐号**。</span><span class="sxs-lookup"><span data-stu-id="61630-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="61630-172">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-172">Click **OK**.</span></span>
48. <span data-ttu-id="61630-173">在树结构中，选择 **Xml\消息\付款\项\供应商**。</span><span class="sxs-lookup"><span data-stu-id="61630-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="61630-174">单击 **复制**。</span><span class="sxs-lookup"><span data-stu-id="61630-174">Click **Copy**.</span></span>
50. <span data-ttu-id="61630-175">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="61630-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="61630-176">单击 **粘贴**。</span><span class="sxs-lookup"><span data-stu-id="61630-176">Click **Paste**.</span></span>
52. <span data-ttu-id="61630-177">在 **名称** 字段中，键入 **付款人**。</span><span class="sxs-lookup"><span data-stu-id="61630-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="61630-178">在树结构中，选择 **Xml\消息\付款\项**。</span><span class="sxs-lookup"><span data-stu-id="61630-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="61630-179">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="61630-180">在 **名称** 字段中，键入 **货币**。</span><span class="sxs-lookup"><span data-stu-id="61630-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="61630-181">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-181">Click **OK**.</span></span>
57. <span data-ttu-id="61630-182">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="61630-183">在 **名称** 字段中，键入 **描述**。</span><span class="sxs-lookup"><span data-stu-id="61630-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="61630-184">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-184">Click **OK**.</span></span>
60. <span data-ttu-id="61630-185">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="61630-186">在“名称”字段中，键入 **交易日期**。</span><span class="sxs-lookup"><span data-stu-id="61630-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="61630-187">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-187">Click **OK**.</span></span>
63. <span data-ttu-id="61630-188">单击 **添加元素**。</span><span class="sxs-lookup"><span data-stu-id="61630-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="61630-189">在“名称”字段中，键入 **金额**。</span><span class="sxs-lookup"><span data-stu-id="61630-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="61630-190">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="61630-191">准备映射到数据模型元素的格式部分</span><span class="sxs-lookup"><span data-stu-id="61630-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="61630-192">在树结构中，选择 **Xml\消息\处理日期**。</span><span class="sxs-lookup"><span data-stu-id="61630-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="61630-193">单击 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="61630-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="61630-194">在树结构中，选择 **文本\日期时间**。</span><span class="sxs-lookup"><span data-stu-id="61630-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="61630-195">在 **格式** 字段中，键入 **年-月-日**。</span><span class="sxs-lookup"><span data-stu-id="61630-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="61630-196">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-196">Click **OK**.</span></span>
6. <span data-ttu-id="61630-197">在树结构中，选择 **Xml\消息\付款\项\交易日期**。</span><span class="sxs-lookup"><span data-stu-id="61630-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="61630-198">单击 **添加日期时间**。</span><span class="sxs-lookup"><span data-stu-id="61630-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="61630-199">在 **格式** 字段中，键入 **年-月-日**。</span><span class="sxs-lookup"><span data-stu-id="61630-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="61630-200">在 **日期时间** 类型字段中，选择 **日期**。</span><span class="sxs-lookup"><span data-stu-id="61630-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="61630-201">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-201">Click **OK**.</span></span>
11. <span data-ttu-id="61630-202">在树结构中，选择 **Xml\消息\消息标识**。</span><span class="sxs-lookup"><span data-stu-id="61630-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="61630-203">单击 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="61630-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="61630-204">在树结构中，选择 **文本\字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="61630-205">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-205">Click **OK**.</span></span>
15. <span data-ttu-id="61630-206">在树结构中，选择 **Xml\消息\付款\项\供应商\名称**。</span><span class="sxs-lookup"><span data-stu-id="61630-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="61630-207">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-207">Click **Add String**.</span></span>
17. <span data-ttu-id="61630-208">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-208">Click **OK**.</span></span>
18. <span data-ttu-id="61630-209">在树结构中，选择 **Xml\消息\付款\项\供应商\银行\银行代号**。</span><span class="sxs-lookup"><span data-stu-id="61630-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="61630-210">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-210">Click **Add String**.</span></span>
20. <span data-ttu-id="61630-211">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-211">Click **OK**.</span></span>
21. <span data-ttu-id="61630-212">在树结构中，选择 **Xml\消息\付款\项\供应商\银行\帐号**。</span><span class="sxs-lookup"><span data-stu-id="61630-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="61630-213">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-213">Click **Add String**.</span></span>
23. <span data-ttu-id="61630-214">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-214">Click **OK**.</span></span>
24. <span data-ttu-id="61630-215">在树结构中，选择 **Xml\消息\付款\项\付款人\名称**。</span><span class="sxs-lookup"><span data-stu-id="61630-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="61630-216">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-216">Click **Add String**.</span></span>
26. <span data-ttu-id="61630-217">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-217">Click **OK**.</span></span>
27. <span data-ttu-id="61630-218">在树结构中，选择 **Xml\消息\付款\项\付款人\银行\银行代号**。</span><span class="sxs-lookup"><span data-stu-id="61630-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="61630-219">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-219">Click **Add String**.</span></span>
29. <span data-ttu-id="61630-220">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-220">Click **OK**.</span></span>
30. <span data-ttu-id="61630-221">在树结构中，选择 **Xml\消息\付款\项\付款人\银行\帐号**。</span><span class="sxs-lookup"><span data-stu-id="61630-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="61630-222">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-222">Click **Add String**.</span></span>
32. <span data-ttu-id="61630-223">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-223">Click **OK**.</span></span>
33. <span data-ttu-id="61630-224">在树结构中，选择 **Xml\消息\付款\项\货币**。</span><span class="sxs-lookup"><span data-stu-id="61630-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="61630-225">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-225">Click **Add String**.</span></span>
35. <span data-ttu-id="61630-226">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-226">Click **OK**.</span></span>
36. <span data-ttu-id="61630-227">在树结构中，选择 **Xml\消息\付款\项\描述**。</span><span class="sxs-lookup"><span data-stu-id="61630-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="61630-228">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-228">Click **Add String**.</span></span>
38. <span data-ttu-id="61630-229">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-229">Click **OK**.</span></span>
39. <span data-ttu-id="61630-230">在树结构中，选择 **Xml\消息\付款\项\金额**。</span><span class="sxs-lookup"><span data-stu-id="61630-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="61630-231">单击 **添加字符串**。</span><span class="sxs-lookup"><span data-stu-id="61630-231">Click **Add String**.</span></span>
41. <span data-ttu-id="61630-232">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="61630-232">Click **OK**.</span></span>
42. <span data-ttu-id="61630-233">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="61630-233">Click **Save**.</span></span>
43. <span data-ttu-id="61630-234">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="61630-234">Close the page.</span></span>

