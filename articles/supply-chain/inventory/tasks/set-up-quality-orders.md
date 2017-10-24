---
title: "设置质检订单"
description: "此过程说明了如何启用到达登记后必须立即检查传入库存的质量管理流程。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="38e3f-103">设置质检订单</span><span class="sxs-lookup"><span data-stu-id="38e3f-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38e3f-104">此过程说明了如何启用到达登记后必须立即检查传入库存的质量管理流程。</span><span class="sxs-lookup"><span data-stu-id="38e3f-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="38e3f-105">该过程通常由质量经理执行。</span><span class="sxs-lookup"><span data-stu-id="38e3f-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="38e3f-106">流程包括创建质量组，以定义要进行抽样的物料，和分组要在质量组中对物料执行的测试的测试组。</span><span class="sxs-lookup"><span data-stu-id="38e3f-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="38e3f-107">您可以使用 USMF 演示数据公司运行此指南。</span><span class="sxs-lookup"><span data-stu-id="38e3f-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="38e3f-108">启用质量管理</span><span class="sxs-lookup"><span data-stu-id="38e3f-108">Enable quality management</span></span>
1. <span data-ttu-id="38e3f-109">转到“库存管理”>“设置”>“库存和仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="38e3f-110">单击“质量管理”选项卡。</span><span class="sxs-lookup"><span data-stu-id="38e3f-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="38e3f-111">将使用质量管理选项设置为是。</span><span class="sxs-lookup"><span data-stu-id="38e3f-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="38e3f-112">单击“报表设置”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-112">Click Report setup.</span></span>
    * <span data-ttu-id="38e3f-113">在 USMF 中，已定义了质量管理的报表设置。</span><span class="sxs-lookup"><span data-stu-id="38e3f-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="38e3f-114">如果尚未设置，最好在此处为不同报表类型添加新行，然后选择要用于各报表的单据类型。</span><span class="sxs-lookup"><span data-stu-id="38e3f-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="38e3f-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-115">Close the page.</span></span>
6. <span data-ttu-id="38e3f-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="38e3f-117">创建测试</span><span class="sxs-lookup"><span data-stu-id="38e3f-117">Create a test</span></span>
1. <span data-ttu-id="38e3f-118">转到“库存管理“>”设置“>”质量控制“>”测试“。</span><span class="sxs-lookup"><span data-stu-id="38e3f-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="38e3f-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-119">Click New.</span></span>
3. <span data-ttu-id="38e3f-120">在“测试”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="38e3f-121">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38e3f-122">在“类型”字段中，选择“选项”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="38e3f-123">在此示例中，我们将选择“选项”，这将可以基于预定义值分配测试结果。</span><span class="sxs-lookup"><span data-stu-id="38e3f-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="38e3f-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-124">Click Save.</span></span>
7. <span data-ttu-id="38e3f-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="38e3f-126">创建测试变量以定义记录测试结果的方式</span><span class="sxs-lookup"><span data-stu-id="38e3f-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="38e3f-127">转到“库存管理“>”设置“>”质量控制“>”测试变量”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="38e3f-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-128">Click New.</span></span>
3. <span data-ttu-id="38e3f-129">在“变量”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="38e3f-130">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38e3f-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-131">Click Save.</span></span>
6. <span data-ttu-id="38e3f-132">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-132">Click Outcomes.</span></span>
7. <span data-ttu-id="38e3f-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-133">Click New.</span></span>
8. <span data-ttu-id="38e3f-134">在 “结果”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="38e3f-135">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="38e3f-136">在“结果状态”字段中，选择“通过”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="38e3f-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-137">Click Save.</span></span>
12. <span data-ttu-id="38e3f-138">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-138">Click New.</span></span>
13. <span data-ttu-id="38e3f-139">在 “结果”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="38e3f-140">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="38e3f-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-141">Click Save.</span></span>
16. <span data-ttu-id="38e3f-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-142">Close the page.</span></span>
17. <span data-ttu-id="38e3f-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="38e3f-144">设置物料抽样</span><span class="sxs-lookup"><span data-stu-id="38e3f-144">Set up item sampling</span></span>
1. <span data-ttu-id="38e3f-145">转到“库存管理“>”设置“>”质量控制“>”物料抽样“。</span><span class="sxs-lookup"><span data-stu-id="38e3f-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="38e3f-146">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-146">Click New.</span></span>
3. <span data-ttu-id="38e3f-147">在“物料抽样”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="38e3f-148">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38e3f-149">在“值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="38e3f-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="38e3f-150">此值与在相邻字段中选择的“数量规范”有关。</span><span class="sxs-lookup"><span data-stu-id="38e3f-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="38e3f-151">展开或折叠“流程”部分。</span><span class="sxs-lookup"><span data-stu-id="38e3f-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="38e3f-152">选中或取消选中“完全锁定”复选框。</span><span class="sxs-lookup"><span data-stu-id="38e3f-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="38e3f-153">如果选择此选项，如果测试失败，全部批次或订单行数量均会被锁定。</span><span class="sxs-lookup"><span data-stu-id="38e3f-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="38e3f-154">如果不选中它，则只有质检订单中的物料被锁定。</span><span class="sxs-lookup"><span data-stu-id="38e3f-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="38e3f-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-155">Click Save.</span></span>
9. <span data-ttu-id="38e3f-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="38e3f-157">创建质检组</span><span class="sxs-lookup"><span data-stu-id="38e3f-157">Create a quality group</span></span>
1. <span data-ttu-id="38e3f-158">转到“库存管理“>”设置“>”质量控制“>”质量组“。</span><span class="sxs-lookup"><span data-stu-id="38e3f-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="38e3f-159">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-159">Click New.</span></span>
3. <span data-ttu-id="38e3f-160">在“质量组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="38e3f-161">使用描述性名称以帮助您确定该组将包含哪些物料类型（您的抽样标准）。</span><span class="sxs-lookup"><span data-stu-id="38e3f-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="38e3f-162">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38e3f-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-163">Click Save.</span></span>
6. <span data-ttu-id="38e3f-164">单击“添加物料”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-164">Click Add items.</span></span>
7. <span data-ttu-id="38e3f-165">选择物料编号行</span><span class="sxs-lookup"><span data-stu-id="38e3f-165">Select the Item number row</span></span>
    * <span data-ttu-id="38e3f-166">在此示例中，将根据物料编号运行筛选。</span><span class="sxs-lookup"><span data-stu-id="38e3f-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="38e3f-167">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="38e3f-168">例如，键入 T* 可对以 T 开头的物料编号进行筛选。</span><span class="sxs-lookup"><span data-stu-id="38e3f-168">For example, type T* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="38e3f-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-169">Click OK.</span></span>
10. <span data-ttu-id="38e3f-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-170">Click OK.</span></span>
11. <span data-ttu-id="38e3f-171">单击“物料质量组”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="38e3f-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-172">Close the page.</span></span>
13. <span data-ttu-id="38e3f-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="38e3f-174">创建测试组</span><span class="sxs-lookup"><span data-stu-id="38e3f-174">Create a test group</span></span>
1. <span data-ttu-id="38e3f-175">转到“库存管理“>”设置“>”质量控制“>”测试组”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="38e3f-176">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-176">Click New.</span></span>
3. <span data-ttu-id="38e3f-177">在“测试组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="38e3f-178">为测试取名称，这将帮助您记住有哪些测试类型正在运行及其应该关联哪个质量组。</span><span class="sxs-lookup"><span data-stu-id="38e3f-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="38e3f-179">例如，如果它将与选择以“T”开头的物料的质量组一起使用，则您可以称它为“T 物料测试”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="38e3f-180">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38e3f-181">在“物料抽样”字段中，选择您之前创建的物料抽样行。</span><span class="sxs-lookup"><span data-stu-id="38e3f-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="38e3f-182">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38e3f-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="38e3f-183">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-183">Click Add.</span></span>
8. <span data-ttu-id="38e3f-184">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="38e3f-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="38e3f-185">在“测试”字段中，选择您之前创建的测试。</span><span class="sxs-lookup"><span data-stu-id="38e3f-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="38e3f-186">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38e3f-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="38e3f-187">单击“测试”选项卡。</span><span class="sxs-lookup"><span data-stu-id="38e3f-187">Click the Test tab.</span></span>
12. <span data-ttu-id="38e3f-188">在“变量”字段中，选择您之前创建的测试变量</span><span class="sxs-lookup"><span data-stu-id="38e3f-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="38e3f-189">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38e3f-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="38e3f-190">在“默认结果”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="38e3f-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="38e3f-191">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="38e3f-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="38e3f-192">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-192">Click Save.</span></span>
17. <span data-ttu-id="38e3f-193">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="38e3f-194">定义将要创建质检订单的时间</span><span class="sxs-lookup"><span data-stu-id="38e3f-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="38e3f-195">转到“库存管理“>”设置“>”质量控制“>”质量关联”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="38e3f-196">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-196">Click New.</span></span>
3. <span data-ttu-id="38e3f-197">在“参考类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="38e3f-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="38e3f-198">在“物料代码”字段中，选择“组”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="38e3f-199">在此示例中，我们将选择“组”并使用我们以前创建的质量组。</span><span class="sxs-lookup"><span data-stu-id="38e3f-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="38e3f-200">您还可以将其设置为“表格”以手动指定物料，或选择“所有”以将所有物料添加到质检订单。</span><span class="sxs-lookup"><span data-stu-id="38e3f-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="38e3f-201">在“物料”字段中，选择您之前创建的质量组。</span><span class="sxs-lookup"><span data-stu-id="38e3f-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="38e3f-202">“物料”字段中的可用选项取决于您在“物料代码”字段中所做的设置。</span><span class="sxs-lookup"><span data-stu-id="38e3f-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="38e3f-203">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38e3f-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="38e3f-204">展开或折叠“流程”部分。</span><span class="sxs-lookup"><span data-stu-id="38e3f-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="38e3f-205">在“事件类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="38e3f-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="38e3f-206">它是触发此测试的事件。</span><span class="sxs-lookup"><span data-stu-id="38e3f-206">This is the event that triggers the test.</span></span> <span data-ttu-id="38e3f-207">此处可用的选项取决于您在“参考类型”字段中选择了哪个流程。</span><span class="sxs-lookup"><span data-stu-id="38e3f-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="38e3f-208">在“执行”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="38e3f-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="38e3f-209">展开或折叠“质检订单流程”部分。</span><span class="sxs-lookup"><span data-stu-id="38e3f-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="38e3f-210">在“事件阻止”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="38e3f-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="38e3f-211">此字段显示了在则质检订单仍然打开时可以阻止的流程列表。</span><span class="sxs-lookup"><span data-stu-id="38e3f-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="38e3f-212">这些选项取决于您在“事件类型”字段中所做的选择。</span><span class="sxs-lookup"><span data-stu-id="38e3f-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="38e3f-213">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="38e3f-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="38e3f-214">它将取决于之前所选的值。</span><span class="sxs-lookup"><span data-stu-id="38e3f-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="38e3f-215">当有未结质检订单链接至源文件行时，选择是否必须阻止以下流程。</span><span class="sxs-lookup"><span data-stu-id="38e3f-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="38e3f-216">展开或折叠“规范”部分。</span><span class="sxs-lookup"><span data-stu-id="38e3f-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="38e3f-217">在“测试组”字段中，选择您之前创建的测试组。</span><span class="sxs-lookup"><span data-stu-id="38e3f-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="38e3f-218">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38e3f-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="38e3f-219">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38e3f-219">Click Save.</span></span>
17. <span data-ttu-id="38e3f-220">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38e3f-220">Close the page.</span></span>
