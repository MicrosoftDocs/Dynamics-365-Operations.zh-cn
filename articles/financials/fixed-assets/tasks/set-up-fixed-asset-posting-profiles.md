--- 
title: "设置固定资产过帐模板"
description: "此任务指南将设置固定资产过帐模板。"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="2cb9a-103">设置固定资产过帐模板</span><span class="sxs-lookup"><span data-stu-id="2cb9a-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cb9a-104">此任务指南将设置固定资产过帐模板。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="2cb9a-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="2cb9a-106">在任务指南中给出的示例是一个基础过帐模板，但是必须针对您的特定会计科目表和财务报表要求创建过帐模板。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="2cb9a-107">转到“固定资产”>“设置”>“固定资产过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="2cb9a-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-108">Click New.</span></span>
3. <span data-ttu-id="2cb9a-109">在“过帐模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="2cb9a-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2cb9a-111">您将需要在处理固定资产时使用的每个固定资产交易类型创建过帐模板。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="2cb9a-112">此任务指南将从购置交易类型开始。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="2cb9a-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-113">Click Add.</span></span>
6. <span data-ttu-id="2cb9a-114">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="2cb9a-115">“分组”字段可让您按表（为每个固定资产设置一个科目）或“组”（为每个固定资产组设置一个科目）定义过帐模板。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="2cb9a-116">对于此任务指南，我将此该值设置为“全部”以适用于有指定帐簿的所有固定资产。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="2cb9a-117">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="2cb9a-118">对于购置，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="2cb9a-119">在“交易类型”字段中，选择“购置调整”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="2cb9a-120">对于购置调整交易记录，我们将使用与用于购置交易记录的相同科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="2cb9a-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-121">Click Add.</span></span>
10. <span data-ttu-id="2cb9a-122">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="2cb9a-123">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="2cb9a-124">对于购置调整，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="2cb9a-125">在“交易类型”字段中，选择“折旧”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="2cb9a-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-126">Click Add.</span></span>
14. <span data-ttu-id="2cb9a-127">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="2cb9a-128">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="2cb9a-129">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="2cb9a-130">在“交易类型”字段中，选择“折旧调整”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="2cb9a-131">对于折旧调整交易记录，我们将使用与用于折旧交易记录的相同科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="2cb9a-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-132">Click Add.</span></span>
19. <span data-ttu-id="2cb9a-133">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="2cb9a-134">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="2cb9a-135">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="2cb9a-136">在“交易类型”字段中，选择“处置 - 销售”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="2cb9a-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-137">Click Add.</span></span>
24. <span data-ttu-id="2cb9a-138">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="2cb9a-139">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="2cb9a-140">对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="2cb9a-141">在“交易类型”字段中，选择“处置 - 报废”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="2cb9a-142">我们将对处理销售和处理报废使用相同的科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="2cb9a-143">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-143">Click Add.</span></span>
28. <span data-ttu-id="2cb9a-144">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="2cb9a-145">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="2cb9a-146">对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="2cb9a-147">展开“处置”部分。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="2cb9a-148">您必须对销售及报废设置处置过帐模板。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="2cb9a-149">我们从处置销售交易开始。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="2cb9a-150">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-150">Click Add.</span></span>
32. <span data-ttu-id="2cb9a-151">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="2cb9a-152">在“过帐值”字段中，选择“购置值”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="2cb9a-153">购置价值将用于所有年度的购置和购置调整价值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="2cb9a-154">您还可以为这些交易类型分别定义科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="2cb9a-155">根据处置是否造成收益或损失，您可以设置处置流程以使用不同科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="2cb9a-156">我将“销售价值类型”设置为“全部”以对所有处置类型使用相同的科目。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="2cb9a-157">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="2cb9a-158">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="2cb9a-159">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-159">Click Add.</span></span>
37. <span data-ttu-id="2cb9a-160">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="2cb9a-161">在“过帐值”字段中，选择“折旧（往年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="2cb9a-162">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="2cb9a-163">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="2cb9a-164">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-164">Click Add.</span></span>
41. <span data-ttu-id="2cb9a-165">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="2cb9a-166">在“过帐值”字段中，选择“折旧（今年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="2cb9a-167">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="2cb9a-168">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="2cb9a-169">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-169">Click Add.</span></span>
46. <span data-ttu-id="2cb9a-170">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="2cb9a-171">在“过帐值”字段中，选择“折旧调整（往年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="2cb9a-172">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="2cb9a-173">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="2cb9a-174">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-174">Click Add.</span></span>
51. <span data-ttu-id="2cb9a-175">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="2cb9a-176">在“过帐值”字段中，选择“折旧调整（今年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="2cb9a-177">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="2cb9a-178">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="2cb9a-179">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-179">Click Add.</span></span>
56. <span data-ttu-id="2cb9a-180">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="2cb9a-181">在“过帐值”字段中，选择“帐面净值”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="2cb9a-182">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="2cb9a-183">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="2cb9a-184">在“销售或报废”字段中，选择“报废”</span><span class="sxs-lookup"><span data-stu-id="2cb9a-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="2cb9a-185">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-185">Click Add.</span></span>
62. <span data-ttu-id="2cb9a-186">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="2cb9a-187">在“过帐值”字段中，选择“购置值”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="2cb9a-188">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="2cb9a-189">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="2cb9a-190">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-190">Click Add.</span></span>
67. <span data-ttu-id="2cb9a-191">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="2cb9a-192">在“过帐值”字段中，选择“折旧（往年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="2cb9a-193">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="2cb9a-194">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="2cb9a-195">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-195">Click Add.</span></span>
71. <span data-ttu-id="2cb9a-196">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="2cb9a-197">在“过帐值”字段中，选择“折旧（今年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="2cb9a-198">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="2cb9a-199">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="2cb9a-200">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-200">Click Add.</span></span>
76. <span data-ttu-id="2cb9a-201">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="2cb9a-202">在“过帐值”字段中，选择“折旧调整（往年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="2cb9a-203">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="2cb9a-204">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="2cb9a-205">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-205">Click Add.</span></span>
81. <span data-ttu-id="2cb9a-206">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="2cb9a-207">在“过帐值”字段中，选择“折旧调整（今年）”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="2cb9a-208">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="2cb9a-209">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="2cb9a-210">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-210">Click Add.</span></span>
86. <span data-ttu-id="2cb9a-211">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="2cb9a-212">在“过帐值”字段中，选择“帐面净值”。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="2cb9a-213">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="2cb9a-214">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2cb9a-214">In the Offset account field, specify the desired values.</span></span>


