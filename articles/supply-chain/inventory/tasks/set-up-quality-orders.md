---
title: 设置质检订单
description: 此过程说明了如何启用到达登记后必须立即检查传入库存的质量管理流程。
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4577b8b189403b3d71eb634e159d51d2fa53ce12
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3268785"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="f7b65-103">设置质检订单</span><span class="sxs-lookup"><span data-stu-id="f7b65-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7b65-104">此过程说明了如何启用到达登记后必须立即检查传入库存的质量管理流程。</span><span class="sxs-lookup"><span data-stu-id="f7b65-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="f7b65-105">该过程通常由质量经理执行。</span><span class="sxs-lookup"><span data-stu-id="f7b65-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="f7b65-106">流程包括创建质量组，以定义要进行抽样的物料，和分组要在质量组中对物料执行的测试的测试组。</span><span class="sxs-lookup"><span data-stu-id="f7b65-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="f7b65-107">您可以使用 USMF 演示数据公司运行此指南。</span><span class="sxs-lookup"><span data-stu-id="f7b65-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="f7b65-108">启用质量管理</span><span class="sxs-lookup"><span data-stu-id="f7b65-108">Enable quality management</span></span>
1. <span data-ttu-id="f7b65-109">转到**导航窗格 > 模块 > 库存管理 > 设置 > 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="f7b65-110">单击**质量管理**选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7b65-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="f7b65-111">将**使用质量管理选项**设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="f7b65-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="f7b65-112">单击**报表设置**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-112">Click **Report setup**.</span></span> <span data-ttu-id="f7b65-113">在 USMF 中，已定义了质量管理的报表设置。</span><span class="sxs-lookup"><span data-stu-id="f7b65-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="f7b65-114">如果尚未设置，最好在此处为不同报表类型添加新行，然后选择要用于各报表的单据类型。</span><span class="sxs-lookup"><span data-stu-id="f7b65-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="f7b65-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-115">Close the page.</span></span>
6. <span data-ttu-id="f7b65-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="f7b65-117">创建测试</span><span class="sxs-lookup"><span data-stu-id="f7b65-117">Create a test</span></span>
1. <span data-ttu-id="f7b65-118">转到**库存管理 > 设置 > 质量控制 > 测试**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="f7b65-119">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-119">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-120">在**测试**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="f7b65-121">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f7b65-122">在**类型**字段中，选择“选项”。</span><span class="sxs-lookup"><span data-stu-id="f7b65-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="f7b65-123">在此示例中，我们将选择“选项”，这将可以基于预定义值分配测试结果。</span><span class="sxs-lookup"><span data-stu-id="f7b65-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="f7b65-124">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-124">Click **Save**.</span></span>
7. <span data-ttu-id="f7b65-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="f7b65-126">创建测试变量以定义记录测试结果的方式</span><span class="sxs-lookup"><span data-stu-id="f7b65-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="f7b65-127">转到**库存管理 > 设置 > 质量控制 > 测试变量**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="f7b65-128">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-128">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-129">在**变量**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="f7b65-130">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f7b65-131">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-131">Click **Save**.</span></span>
6. <span data-ttu-id="f7b65-132">单击**结果**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="f7b65-133">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-133">Click **New**.</span></span>
8. <span data-ttu-id="f7b65-134">在**结果**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="f7b65-135">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="f7b65-136">在**结果状态**字段中，选择“通过”。</span><span class="sxs-lookup"><span data-stu-id="f7b65-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="f7b65-137">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-137">Click **Save**.</span></span>
12. <span data-ttu-id="f7b65-138">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-138">Click **New**.</span></span>
13. <span data-ttu-id="f7b65-139">在**结果**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="f7b65-140">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="f7b65-141">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-141">Click **Save**.</span></span>
16. <span data-ttu-id="f7b65-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-142">Close the page.</span></span>
17. <span data-ttu-id="f7b65-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="f7b65-144">设置物料抽样</span><span class="sxs-lookup"><span data-stu-id="f7b65-144">Set up item sampling</span></span>
1. <span data-ttu-id="f7b65-145">转到**库存管理 > 设置 > 质量控制 > 物料抽样**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="f7b65-146">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-146">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-147">在**物料抽样**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="f7b65-148">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f7b65-149">在**值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f7b65-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="f7b65-150">此值与在相邻字段中选择的“数量规范”有关。</span><span class="sxs-lookup"><span data-stu-id="f7b65-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="f7b65-151">展开或折叠**流程**部分。</span><span class="sxs-lookup"><span data-stu-id="f7b65-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="f7b65-152">选中或取消选中**完全锁定**复选框。</span><span class="sxs-lookup"><span data-stu-id="f7b65-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="f7b65-153">如果选择此选项，如果测试失败，全部批次或订单行数量均会被锁定。</span><span class="sxs-lookup"><span data-stu-id="f7b65-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="f7b65-154">如果不选中它，则只有质检订单中的物料被锁定。</span><span class="sxs-lookup"><span data-stu-id="f7b65-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="f7b65-155">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-155">Click **Save**.</span></span>
9. <span data-ttu-id="f7b65-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-156">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="f7b65-157">*仓库流程质量管理*功能提供其他的物料抽样功能。</span><span class="sxs-lookup"><span data-stu-id="f7b65-157">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="f7b65-158">它增加了*物料抽样范围*概念以及将完整牌照定义为数量规范的能力。</span><span class="sxs-lookup"><span data-stu-id="f7b65-158">It adds a concept of *item sampling scope* and the ability to define a full license plate as the quantity specification.</span></span> <span data-ttu-id="f7b65-159">如果已启用此功能，请参阅[仓库流程质量管理](../quality-management-for-warehouses-processes.md)了解详细信息。</span><span class="sxs-lookup"><span data-stu-id="f7b65-159">If you have enabled this feature, then see [Quality management for warehouse processes](../quality-management-for-warehouses-processes.md) for details.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="f7b65-160">创建质检组</span><span class="sxs-lookup"><span data-stu-id="f7b65-160">Create a quality group</span></span>
1. <span data-ttu-id="f7b65-161">转到**库存管理 > 设置 > 质量控制 > 质量组**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-161">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="f7b65-162">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-162">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-163">在**质量组**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-163">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="f7b65-164">使用描述性名称以帮助您确定该组将包含哪些物料类型（您的抽样标准）。</span><span class="sxs-lookup"><span data-stu-id="f7b65-164">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="f7b65-165">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-165">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f7b65-166">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-166">Click **Save**.</span></span>
6. <span data-ttu-id="f7b65-167">单击**添加物料**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-167">Click **Add items**.</span></span>
7. <span data-ttu-id="f7b65-168">选择**物料编号**行。</span><span class="sxs-lookup"><span data-stu-id="f7b65-168">Select the **Item number** row.</span></span> <span data-ttu-id="f7b65-169">在此示例中，将根据物料编号运行筛选。</span><span class="sxs-lookup"><span data-stu-id="f7b65-169">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="f7b65-170">在**条件**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-170">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="f7b65-171">例如，键入 T\* 可对以 T 开头的物料编号进行筛选。</span><span class="sxs-lookup"><span data-stu-id="f7b65-171">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="f7b65-172">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-172">Click **OK**.</span></span>
10. <span data-ttu-id="f7b65-173">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-173">Click **OK**.</span></span>
11. <span data-ttu-id="f7b65-174">单击**物料质量组**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-174">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="f7b65-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-175">Close the page.</span></span>
13. <span data-ttu-id="f7b65-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-176">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="f7b65-177">创建测试组</span><span class="sxs-lookup"><span data-stu-id="f7b65-177">Create a test group</span></span>
1. <span data-ttu-id="f7b65-178">转到**库存管理 > 设置 > 质量控制 > 测试组**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-178">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="f7b65-179">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-179">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-180">在**测试组**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-180">In the **Test group** field, type a value.</span></span> <span data-ttu-id="f7b65-181">为**测试组**命名，这将帮助您记住有哪些测试类型正在运行及其应该关联哪个质量组。</span><span class="sxs-lookup"><span data-stu-id="f7b65-181">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="f7b65-182">例如，如果它将与选择以“T”开头的物料的质量组一起使用，则您可以称它为“T 物料测试”。</span><span class="sxs-lookup"><span data-stu-id="f7b65-182">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="f7b65-183">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-183">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f7b65-184">在**物料抽样**字段中，选择您之前创建的物料抽样行。</span><span class="sxs-lookup"><span data-stu-id="f7b65-184">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="f7b65-185">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b65-185">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f7b65-186">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-186">Click **Add**.</span></span>
8. <span data-ttu-id="f7b65-187">在**序列号**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f7b65-187">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="f7b65-188">在**测试**字段中，选择您之前创建的测试。</span><span class="sxs-lookup"><span data-stu-id="f7b65-188">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="f7b65-189">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b65-189">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f7b65-190">单击**测试**选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7b65-190">Click the **Test** tab.</span></span>
12. <span data-ttu-id="f7b65-191">在**变量**字段中，选择您之前创建的测试变量</span><span class="sxs-lookup"><span data-stu-id="f7b65-191">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="f7b65-192">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b65-192">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f7b65-193">在**默认结果**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f7b65-193">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f7b65-194">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f7b65-194">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f7b65-195">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-195">Click **Save**.</span></span>
17. <span data-ttu-id="f7b65-196">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-196">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="f7b65-197">定义将要创建质检订单的时间</span><span class="sxs-lookup"><span data-stu-id="f7b65-197">Define when quality orders will be created</span></span>
1. <span data-ttu-id="f7b65-198">转到**库存管理 > 设置 > 质量控制 > 质量关联**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-198">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="f7b65-199">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-199">Click **New**.</span></span>
3. <span data-ttu-id="f7b65-200">在**参考类型**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f7b65-200">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="f7b65-201">在**物料代码**字段中，选择“组”。</span><span class="sxs-lookup"><span data-stu-id="f7b65-201">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="f7b65-202">在此示例中，我们将选择“组”并使用我们以前创建的质量组。</span><span class="sxs-lookup"><span data-stu-id="f7b65-202">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="f7b65-203">您还可以将其设置为“表格”以手动指定物料，或选择“所有”以将所有物料添加到质检订单。</span><span class="sxs-lookup"><span data-stu-id="f7b65-203">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="f7b65-204">在**物料**字段中，选择您之前创建的质量组。</span><span class="sxs-lookup"><span data-stu-id="f7b65-204">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="f7b65-205">“物料”字段中的可用选项取决于您在“物料代码”字段中所做的设置。</span><span class="sxs-lookup"><span data-stu-id="f7b65-205">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="f7b65-206">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b65-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f7b65-207">展开或折叠“流程”部分。</span><span class="sxs-lookup"><span data-stu-id="f7b65-207">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="f7b65-208">在**事件类型**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f7b65-208">In the **Event type** field, select an option.</span></span> <span data-ttu-id="f7b65-209">它是触发此测试的事件。</span><span class="sxs-lookup"><span data-stu-id="f7b65-209">This is the event that triggers the test.</span></span> <span data-ttu-id="f7b65-210">此处可用的选项取决于您在“参考类型”字段中选择了哪个流程。</span><span class="sxs-lookup"><span data-stu-id="f7b65-210">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="f7b65-211">在**执行**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f7b65-211">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="f7b65-212">展开或折叠**质检订单流程**部分。</span><span class="sxs-lookup"><span data-stu-id="f7b65-212">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="f7b65-213">在**事件阻止**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f7b65-213">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f7b65-214">此字段显示了在则质检订单仍然打开时可以阻止的流程列表。</span><span class="sxs-lookup"><span data-stu-id="f7b65-214">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="f7b65-215">这些选项取决于您在“事件类型”字段中所做的选择。</span><span class="sxs-lookup"><span data-stu-id="f7b65-215">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="f7b65-216">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f7b65-216">In the list, click the link in the selected row.</span></span> <span data-ttu-id="f7b65-217">它将取决于之前所选的值。</span><span class="sxs-lookup"><span data-stu-id="f7b65-217">This will be depending on the previous selected values.</span></span> <span data-ttu-id="f7b65-218">当有未结质检订单链接至源文件行时，选择是否必须阻止以下流程。</span><span class="sxs-lookup"><span data-stu-id="f7b65-218">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="f7b65-219">展开或折叠**规范**部分。</span><span class="sxs-lookup"><span data-stu-id="f7b65-219">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="f7b65-220">在**测试组**字段中，选择您之前创建的测试组。</span><span class="sxs-lookup"><span data-stu-id="f7b65-220">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="f7b65-221">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b65-221">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f7b65-222">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f7b65-222">Click **Save**.</span></span>
17. <span data-ttu-id="f7b65-223">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b65-223">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="f7b65-224">*仓库流程质量管理*功能提供设置质量关联的其他选项。</span><span class="sxs-lookup"><span data-stu-id="f7b65-224">The *Quality management for warehouse processes* feature provides additional options for setting up quality associations.</span></span> <span data-ttu-id="f7b65-225">它增加了一个新条件（**适用仓库类型**）和一个新设置（**质量处理策略**）。</span><span class="sxs-lookup"><span data-stu-id="f7b65-225">It adds a new condition (**Applicable warehouse type**) and a new setting (**Quality processing policy**).</span></span> <span data-ttu-id="f7b65-226">如果已启用此功能，请参阅[仓库流程质量管理](../quality-management-for-warehouses-processes.md)了解详细信息。</span><span class="sxs-lookup"><span data-stu-id="f7b65-226">If you have enabled this feature, then see [Quality management for warehouse processes](../quality-management-for-warehouses-processes.md) for details.</span></span>