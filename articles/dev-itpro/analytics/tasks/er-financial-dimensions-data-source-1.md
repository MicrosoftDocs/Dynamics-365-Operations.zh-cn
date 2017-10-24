--- 
title: "针对电子申报 (ER) 将数据模型设计为使用财务维度作为数据源"
description: "以下步骤说明系统管理员或电子申报开发人员可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d8a03c4b85666975a7b42d46f3afdd35019e9b93
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="c4596-103">针对电子申报 (ER) 将数据模型设计为使用财务维度作为数据源</span><span class="sxs-lookup"><span data-stu-id="c4596-103">Design data model to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4596-104">以下步骤说明系统管理员或电子申报开发人员可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="c4596-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c4596-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="c4596-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c4596-106">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c4596-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="c4596-107">新建数据模型</span><span class="sxs-lookup"><span data-stu-id="c4596-107">Create a new data model</span></span>
1. <span data-ttu-id="c4596-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="c4596-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c4596-109">确保“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="c4596-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="c4596-110">提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="c4596-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="c4596-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="c4596-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c4596-112">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c4596-113">在“名称”字段中，键入“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="c4596-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="c4596-114">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="c4596-114">Click Create configuration.</span></span>
6. <span data-ttu-id="c4596-115">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="c4596-115">Click Designer.</span></span>
7. <span data-ttu-id="c4596-116">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c4596-117">在“名称”字段中，键入“条目”。</span><span class="sxs-lookup"><span data-stu-id="c4596-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="c4596-118">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-118">Click Add.</span></span>
10. <span data-ttu-id="c4596-119">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="c4596-120">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="c4596-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="c4596-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-121">Click Add.</span></span>
    * <span data-ttu-id="c4596-122">我们将向模型添加一个新记录列表。</span><span class="sxs-lookup"><span data-stu-id="c4596-122">We will add to our model a new record list.</span></span> <span data-ttu-id="c4596-123">此列表将（为使用此模型的任何 ER 报表）显示所选财务维度的设置。</span><span class="sxs-lookup"><span data-stu-id="c4596-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="c4596-124">每个财务维度将在此列表中显示为一条记录，这些记录带有表示维度设置的相应字段。</span><span class="sxs-lookup"><span data-stu-id="c4596-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="c4596-125">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="c4596-126">在“名称”字段中，键入“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="c4596-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="c4596-127">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="c4596-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="c4596-128">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-128">Click Add.</span></span>
17. <span data-ttu-id="c4596-129">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="c4596-130">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="c4596-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="c4596-131">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="c4596-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="c4596-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-132">Click Add.</span></span>
21. <span data-ttu-id="c4596-133">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="c4596-134">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="c4596-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="c4596-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-135">Click Add.</span></span>
24. <span data-ttu-id="c4596-136">在树中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="c4596-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="c4596-137">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="c4596-138">在“名称”字段中，键入“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="c4596-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="c4596-139">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="c4596-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="c4596-140">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-140">Click Add.</span></span>
29. <span data-ttu-id="c4596-141">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="c4596-142">在“名称”字段中，键入“批次”。</span><span class="sxs-lookup"><span data-stu-id="c4596-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="c4596-143">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="c4596-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="c4596-144">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-144">Click Add.</span></span>
33. <span data-ttu-id="c4596-145">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="c4596-146">在“名称”字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="c4596-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="c4596-147">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="c4596-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="c4596-148">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-148">Click Add.</span></span>
37. <span data-ttu-id="c4596-149">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="c4596-150">在“名称”字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="c4596-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="c4596-151">在“物料类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="c4596-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="c4596-152">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-152">Click Add.</span></span>
41. <span data-ttu-id="c4596-153">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="c4596-154">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="c4596-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="c4596-155">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="c4596-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="c4596-156">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-156">Click Add.</span></span>
45. <span data-ttu-id="c4596-157">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="c4596-158">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="c4596-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="c4596-159">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-159">Click Add.</span></span>
48. <span data-ttu-id="c4596-160">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="c4596-161">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="c4596-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="c4596-162">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="c4596-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="c4596-163">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-163">Click Add.</span></span>
52. <span data-ttu-id="c4596-164">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="c4596-165">在“名称”字段中，键入“凭证”。</span><span class="sxs-lookup"><span data-stu-id="c4596-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="c4596-166">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-166">Click Add.</span></span>
55. <span data-ttu-id="c4596-167">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="c4596-168">在“名称”字段中，键入“维度数据”。</span><span class="sxs-lookup"><span data-stu-id="c4596-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="c4596-169">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="c4596-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="c4596-170">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-170">Click Add.</span></span>
    * <span data-ttu-id="c4596-171">我们已向模型添加了一个新记录列表。</span><span class="sxs-lookup"><span data-stu-id="c4596-171">We added to our model a new record list.</span></span> <span data-ttu-id="c4596-172">此列表将（为使用此模型的任何 ER 报表）显示所选财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="c4596-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="c4596-173">每个财务维度将在此列表中显示为一条记录，这些记录带有表示维度值的相应字段。</span><span class="sxs-lookup"><span data-stu-id="c4596-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="c4596-174">如果需要，还将出于选择目的在此记录中把维度名称显示为要使用的字段。</span><span class="sxs-lookup"><span data-stu-id="c4596-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="c4596-175">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="c4596-176">在“名称”字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="c4596-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="c4596-177">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="c4596-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="c4596-178">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-178">Click Add.</span></span>
63. <span data-ttu-id="c4596-179">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="c4596-180">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="c4596-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="c4596-181">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-181">Click Add.</span></span>
66. <span data-ttu-id="c4596-182">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="c4596-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="c4596-183">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="c4596-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="c4596-184">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c4596-184">Click Add.</span></span>
69. <span data-ttu-id="c4596-185">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c4596-185">Click Save.</span></span>
70. <span data-ttu-id="c4596-186">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4596-186">Close the page.</span></span>

