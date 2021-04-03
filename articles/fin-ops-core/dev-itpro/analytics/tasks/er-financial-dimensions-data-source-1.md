---
title: ER 将财务维度用作数据源（第 1 部分 - 设计数据模型）
description: 本主题介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 1 部分）
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570184"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="d9e5b-104">ER 将财务维度用作数据源（第 1 部分 - 设计数据模型）</span><span class="sxs-lookup"><span data-stu-id="d9e5b-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9e5b-105">以下步骤说明系统管理员或电子申报开发人员可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d9e5b-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d9e5b-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="d9e5b-108">新建数据模型</span><span class="sxs-lookup"><span data-stu-id="d9e5b-108">Create a new data model</span></span>
1. <span data-ttu-id="d9e5b-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d9e5b-110">确保“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="d9e5b-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="d9e5b-111">提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="d9e5b-112">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d9e5b-113">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="d9e5b-114">在“名称”字段中，键入“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="d9e5b-115">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-115">Click Create configuration.</span></span>
6. <span data-ttu-id="d9e5b-116">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-116">Click Designer.</span></span>
7. <span data-ttu-id="d9e5b-117">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d9e5b-118">在“名称”字段中，键入“条目”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="d9e5b-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-119">Click Add.</span></span>
10. <span data-ttu-id="d9e5b-120">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="d9e5b-121">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="d9e5b-122">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-122">Click Add.</span></span>
    * <span data-ttu-id="d9e5b-123">我们将向模型添加一个新记录列表。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-123">We will add to our model a new record list.</span></span> <span data-ttu-id="d9e5b-124">此列表将（为使用此模型的任何 ER 报表）显示所选财务维度的设置。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="d9e5b-125">每个财务维度将在此列表中显示为一条记录，这些记录带有表示维度设置的相应字段。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="d9e5b-126">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="d9e5b-127">在“名称”字段中，键入“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="d9e5b-128">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="d9e5b-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-129">Click Add.</span></span>
17. <span data-ttu-id="d9e5b-130">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="d9e5b-131">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="d9e5b-132">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="d9e5b-133">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-133">Click Add.</span></span>
21. <span data-ttu-id="d9e5b-134">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d9e5b-135">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="d9e5b-136">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-136">Click Add.</span></span>
24. <span data-ttu-id="d9e5b-137">在树中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="d9e5b-138">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="d9e5b-139">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="d9e5b-140">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="d9e5b-141">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-141">Click Add.</span></span>
29. <span data-ttu-id="d9e5b-142">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="d9e5b-143">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="d9e5b-144">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="d9e5b-145">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-145">Click Add.</span></span>
33. <span data-ttu-id="d9e5b-146">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="d9e5b-147">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="d9e5b-148">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="d9e5b-149">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-149">Click Add.</span></span>
37. <span data-ttu-id="d9e5b-150">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="d9e5b-151">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="d9e5b-152">在“物料类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="d9e5b-153">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-153">Click Add.</span></span>
41. <span data-ttu-id="d9e5b-154">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="d9e5b-155">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="d9e5b-156">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="d9e5b-157">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-157">Click Add.</span></span>
45. <span data-ttu-id="d9e5b-158">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="d9e5b-159">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="d9e5b-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-160">Click Add.</span></span>
48. <span data-ttu-id="d9e5b-161">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="d9e5b-162">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="d9e5b-163">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="d9e5b-164">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-164">Click Add.</span></span>
52. <span data-ttu-id="d9e5b-165">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="d9e5b-166">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="d9e5b-167">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-167">Click Add.</span></span>
55. <span data-ttu-id="d9e5b-168">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="d9e5b-169">在“名称”字段中，键入“维度数据”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="d9e5b-170">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="d9e5b-171">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-171">Click Add.</span></span>
    * <span data-ttu-id="d9e5b-172">我们已向模型添加了一个新记录列表。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-172">We added to our model a new record list.</span></span> <span data-ttu-id="d9e5b-173">此列表将（为使用此模型的任何 ER 报表）显示所选财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="d9e5b-174">每个财务维度将在此列表中显示为一条记录，这些记录带有表示维度值的相应字段。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="d9e5b-175">如果需要，还将出于选择目的在此记录中把维度名称显示为要使用的字段。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="d9e5b-176">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="d9e5b-177">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="d9e5b-178">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="d9e5b-179">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-179">Click Add.</span></span>
63. <span data-ttu-id="d9e5b-180">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="d9e5b-181">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="d9e5b-182">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-182">Click Add.</span></span>
66. <span data-ttu-id="d9e5b-183">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="d9e5b-184">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="d9e5b-185">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-185">Click Add.</span></span>
69. <span data-ttu-id="d9e5b-186">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-186">Click Save.</span></span>
70. <span data-ttu-id="d9e5b-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d9e5b-187">Close the page.</span></span>

![ER 数据模型设计器页面](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]