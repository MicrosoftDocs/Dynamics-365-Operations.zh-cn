---
title: 设置固定资产过帐模板
description: 此任务指南将设置固定资产过帐模板。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8671d38098542afbd8d00e30e72de8dbd1fc4abb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994807"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="5ff9c-103">设置固定资产过帐模板</span><span class="sxs-lookup"><span data-stu-id="5ff9c-103">Set up fixed asset posting profiles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ff9c-104">此任务指南将设置固定资产过帐模板。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="5ff9c-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="5ff9c-106">在任务指南中给出的示例是一个基础过帐模板，但是必须针对您的特定会计科目表和财务报表要求创建过帐模板。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="5ff9c-107">在导航窗格中，转到 **模块 > 固定资产 > 设置 > 固定资产过帐模板**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-107">In the Navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset posting profiles**.</span></span>
2. <span data-ttu-id="5ff9c-108">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-108">Click **New**.</span></span>
3. <span data-ttu-id="5ff9c-109">在 **过帐模板** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-109">In the **Posting profile** field, type a value.</span></span>
4. <span data-ttu-id="5ff9c-110">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-110">In the **Description** field, type a value.</span></span> <span data-ttu-id="5ff9c-111">您将需要在处理固定资产时使用的每个固定资产交易类型创建过帐模板。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span> <span data-ttu-id="5ff9c-112">此任务指南将从购置交易类型开始。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="5ff9c-113">单击工具栏中的 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-113">In the toolbar, click **Add**.</span></span>
6. <span data-ttu-id="5ff9c-114">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-114">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="5ff9c-115">**分组** 字段可让您按表（为每个固定资产设置一个科目）或“组”（为每个固定资产组设置一个科目）定义过帐模板。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-115">The **Groupings** field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span> <span data-ttu-id="5ff9c-116">对于此任务指南，将此该值设置为“全部”以适用于有指定帐簿的所有固定资产。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-116">For this task guide, leave the value set to "All" to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="5ff9c-117">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-117">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="5ff9c-118">对于购置，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-118">For acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="5ff9c-119">在 **会计科目** 快速选项卡下的下拉菜单中，选择“购置调整”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-119">In the drop-down menu under the **Ledger accounts** fastTab, select 'Acquisition adjustment'.</span></span> <span data-ttu-id="5ff9c-120">对于购置调整交易记录，我们将使用与用于购置交易记录的相同科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-120">For acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="5ff9c-121">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-121">Click **Add**.</span></span>
10. <span data-ttu-id="5ff9c-122">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-122">In the **Book** field, enter or select a value.</span></span>
11. <span data-ttu-id="5ff9c-123">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-123">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="5ff9c-124">对于购置调整，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-124">For acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="5ff9c-125">在 **会计科目** 快速选项卡下的下拉菜单中，选择“折旧”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-125">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation'.</span></span>
13. <span data-ttu-id="5ff9c-126">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-126">Click **Add**.</span></span>
14. <span data-ttu-id="5ff9c-127">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-127">In the **Book** field, enter or select a value.</span></span>
15. <span data-ttu-id="5ff9c-128">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-128">In the **Main account** field, specify the desired values.</span></span>
16. <span data-ttu-id="5ff9c-129">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-129">In the **Offset account** field, specify the desired values.</span></span>
17. <span data-ttu-id="5ff9c-130">在 **会计科目** 快速选项卡下的下拉菜单中，选择“折旧调整”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-130">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation adjustment'.</span></span> <span data-ttu-id="5ff9c-131">对于折旧调整交易记录，我们将使用与用于折旧交易记录的相同科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-131">For depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="5ff9c-132">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-132">Click **Add**.</span></span>
19. <span data-ttu-id="5ff9c-133">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-133">In the **Book** field, enter or select a value.</span></span>
20. <span data-ttu-id="5ff9c-134">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-134">In the **Main account** field, specify the desired values.</span></span>
21. <span data-ttu-id="5ff9c-135">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-135">In the **Offset account** field, specify the desired values.</span></span>
22. <span data-ttu-id="5ff9c-136">在 **会计科目** 快速选项卡下的下拉菜单中，选择“处置 - 出售”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-136">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="5ff9c-137">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-137">Click **Add**.</span></span>
24. <span data-ttu-id="5ff9c-138">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-138">In the **Book** field, enter or select a value.</span></span>
25. <span data-ttu-id="5ff9c-139">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-139">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="5ff9c-140">对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-140">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="5ff9c-141">在 **会计科目** 快速选项卡下的下拉菜单中，选择“处置 - 报废”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-141">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - scrap'.</span></span> <span data-ttu-id="5ff9c-142">对“处置出售”和“处置报废”使用相同的科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-142">Use the same accounts for 'Disposal sale' and 'Disposal scrap'.</span></span>  
27. <span data-ttu-id="5ff9c-143">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-143">Click **Add**.</span></span>
28. <span data-ttu-id="5ff9c-144">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-144">In the **Book** field, enter or select a value.</span></span>
29. <span data-ttu-id="5ff9c-145">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-145">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="5ff9c-146">对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-146">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="5ff9c-147">展开 **处置** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-147">Expand the **Disposal** fastTab.</span></span> <span data-ttu-id="5ff9c-148">您必须对销售及报废设置处置过帐模板。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="5ff9c-149">我们从处置销售交易开始。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="5ff9c-150">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-150">Click **Add**.</span></span>
32. <span data-ttu-id="5ff9c-151">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-151">In the **Book** field, enter or select a value.</span></span>
33. <span data-ttu-id="5ff9c-152">在 **过帐值** 字段中，选择“购置值”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-152">In the **Post value** field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="5ff9c-153">购置价值将用于所有年度的购置和购置调整价值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span> <span data-ttu-id="5ff9c-154">您还可以为这些交易类型分别定义科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="5ff9c-155">根据处置是否造成收益或损失，您可以设置处置流程以使用不同科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span> <span data-ttu-id="5ff9c-156">我将“销售价值类型”设置为“全部”以对所有处置类型使用相同的科目。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-156">I will set the Sales value type to "All" to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="5ff9c-157">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-157">In the **Main account** field, specify the desired values.</span></span>
35. <span data-ttu-id="5ff9c-158">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-158">In the **Offset account** field, specify the desired values.</span></span>
36. <span data-ttu-id="5ff9c-159">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-159">Click **Add**.</span></span>
37. <span data-ttu-id="5ff9c-160">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-160">In the **Book** field, enter or select a value.</span></span>
38. <span data-ttu-id="5ff9c-161">在 **过帐值** 字段中，选择“折旧（往年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-161">In the **Post value** field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="5ff9c-162">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-162">In the **Main account** field, specify the desired values.</span></span>
39. <span data-ttu-id="5ff9c-163">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-163">In the **Offset account** field, specify the desired values.</span></span>
40. <span data-ttu-id="5ff9c-164">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-164">Click **Add**.</span></span>
41. <span data-ttu-id="5ff9c-165">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-165">In the **Book** field, enter or select a value.</span></span>
42. <span data-ttu-id="5ff9c-166">在 **过帐值** 字段中，选择“折旧（今年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-166">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="5ff9c-167">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-167">In the **Main account** field, specify the desired values.</span></span>
44. <span data-ttu-id="5ff9c-168">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-168">In the **Offset account** field, specify the desired values.</span></span>
45. <span data-ttu-id="5ff9c-169">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-169">Click **Add**.</span></span>
46. <span data-ttu-id="5ff9c-170">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-170">In the **Book** field, enter or select a value.</span></span>
47. <span data-ttu-id="5ff9c-171">在 **过帐值** 字段中，选择“折旧调整（往年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-171">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="5ff9c-172">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-172">In the **Main account** field, specify the desired values.</span></span>
49. <span data-ttu-id="5ff9c-173">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-173">In the **Offset account** field, specify the desired values.</span></span>
50. <span data-ttu-id="5ff9c-174">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-174">Click **Add**.</span></span>
51. <span data-ttu-id="5ff9c-175">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-175">In the **Book** field, enter or select a value.</span></span>
52. <span data-ttu-id="5ff9c-176">在 **过帐值** 字段中，选择“折旧调整（今年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-176">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="5ff9c-177">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-177">In the **Main account** field, specify the desired values.</span></span>
54. <span data-ttu-id="5ff9c-178">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-178">In the **Offset account** field, specify the desired values.</span></span>
55. <span data-ttu-id="5ff9c-179">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-179">Click **Add**.</span></span>
56. <span data-ttu-id="5ff9c-180">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-180">In the **Book** field, enter or select a value.</span></span>
57. <span data-ttu-id="5ff9c-181">在 **过帐值** 字段中，选择“帐面净值”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-181">In the **Post value** field, select 'Net book value'.</span></span>
58. <span data-ttu-id="5ff9c-182">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-182">In the **Main account** field, specify the desired values.</span></span>
59. <span data-ttu-id="5ff9c-183">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-183">In the **Offset account** field, specify the desired values.</span></span>
60. <span data-ttu-id="5ff9c-184">在 **出售还是报废** 字段中，选择“报废”</span><span class="sxs-lookup"><span data-stu-id="5ff9c-184">In the **Sale or scrap** field, select 'Scrap'.</span></span>
61. <span data-ttu-id="5ff9c-185">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-185">Click **Add**.</span></span>
62. <span data-ttu-id="5ff9c-186">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-186">In the **Book** field, enter or select a value.</span></span>
63. <span data-ttu-id="5ff9c-187">在 **过帐值** 字段中，选择“购置值”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-187">In the **Post value** field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="5ff9c-188">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-188">In the **Main account** field, specify the desired values.</span></span>
65. <span data-ttu-id="5ff9c-189">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-189">In the **Offset account** field, specify the desired values.</span></span>
66. <span data-ttu-id="5ff9c-190">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-190">Click **Add**.</span></span>
67. <span data-ttu-id="5ff9c-191">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-191">In the **Book** field, enter or select a value.</span></span>
67. <span data-ttu-id="5ff9c-192">在 **过帐值** 字段中，选择“折旧（往年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-192">In **Post value** field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="5ff9c-193">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-193">In the **Main account** field, specify the desired values.</span></span>
69. <span data-ttu-id="5ff9c-194">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-194">In the **Offset account** field, specify the desired values.</span></span>
70. <span data-ttu-id="5ff9c-195">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-195">Click **Add**.</span></span>
71. <span data-ttu-id="5ff9c-196">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-196">In the **Book** field, enter or select a value.</span></span>
72. <span data-ttu-id="5ff9c-197">在 **过帐值** 字段中，选择“折旧（今年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-197">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="5ff9c-198">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-198">In the **Main account** field, specify the desired values.</span></span>
74. <span data-ttu-id="5ff9c-199">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-199">In the **Offset account** field, specify the desired values.</span></span>
75. <span data-ttu-id="5ff9c-200">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-200">Click **Add**.</span></span>
76. <span data-ttu-id="5ff9c-201">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-201">In the **Book** field, enter or select a value.</span></span>
77. <span data-ttu-id="5ff9c-202">在 **过帐值** 字段中，选择“折旧调整（往年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-202">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="5ff9c-203">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-203">In the **Main account** field, specify the desired values.</span></span>
79. <span data-ttu-id="5ff9c-204">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-204">In the **Offset account** field, specify the desired values.</span></span>
80. <span data-ttu-id="5ff9c-205">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-205">Click **Add**.</span></span>
81. <span data-ttu-id="5ff9c-206">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-206">In the **Book** field, enter or select a value.</span></span>
82. <span data-ttu-id="5ff9c-207">在 **过帐值** 字段中，选择“折旧调整（今年）”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-207">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="5ff9c-208">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-208">In the **Main account** field, specify the desired values.</span></span>
84. <span data-ttu-id="5ff9c-209">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-209">In the **Offset account** field, specify the desired values.</span></span>
85. <span data-ttu-id="5ff9c-210">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-210">Click **Add**.</span></span>
86. <span data-ttu-id="5ff9c-211">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-211">In the **Book** field, enter or select a value.</span></span>
87. <span data-ttu-id="5ff9c-212">在 **过帐值** 字段中，选择“帐面净值”。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-212">In the **Post value** field, select 'Net book value'.</span></span>
88. <span data-ttu-id="5ff9c-213">在 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-213">In the **Main account** field, specify the desired values.</span></span>
89. <span data-ttu-id="5ff9c-214">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff9c-214">In the **Offset account** field, specify the desired values.</span></span>

