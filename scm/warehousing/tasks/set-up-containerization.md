--- 
title: "设置集装化"
description: "此过程描述如何在“仓库管理”中自动进行装载集装化。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="f672c-103">设置集装化</span><span class="sxs-lookup"><span data-stu-id="f672c-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f672c-104">此过程描述如何在“仓库管理”中自动进行装载集装化。</span><span class="sxs-lookup"><span data-stu-id="f672c-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="f672c-105">自动执行集装化在处理波次，且工作行可以分解为适合集装箱的数量时，创建集装箱和用于装运的领料工作。</span><span class="sxs-lookup"><span data-stu-id="f672c-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="f672c-106">这有助于仓库工作人员将物料直接拣选到选择的集装箱内。</span><span class="sxs-lookup"><span data-stu-id="f672c-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="f672c-107">与手动包装流程对比，创建集装箱、分配物料和封闭集装箱等任务由系统自动执行。</span><span class="sxs-lookup"><span data-stu-id="f672c-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="f672c-108">此过程使用 USMF 演示公司，并由仓库经理执行。</span><span class="sxs-lookup"><span data-stu-id="f672c-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="f672c-109">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="f672c-109">Set up a wave template</span></span>
1. <span data-ttu-id="f672c-110">转到“仓库管理”>“设置”>“波次”>“波次模板”。</span><span class="sxs-lookup"><span data-stu-id="f672c-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="f672c-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-111">Click New.</span></span>
3. <span data-ttu-id="f672c-112">在“波次模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="f672c-113">在“波次模板描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="f672c-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f672c-115">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="f672c-116">展开“方法”部分。</span><span class="sxs-lookup"><span data-stu-id="f672c-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="f672c-117">“已选定方法”窗格列出了所选波模板类型的方法。</span><span class="sxs-lookup"><span data-stu-id="f672c-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="f672c-118">波次模板必须包括集装化方法。</span><span class="sxs-lookup"><span data-stu-id="f672c-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="f672c-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f672c-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f672c-120">在“波次步骤代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="f672c-121">键入添加方法的一个波次步骤代码，可以是任意代码。</span><span class="sxs-lookup"><span data-stu-id="f672c-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="f672c-122">可以多次添加方法，并分配不同的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="f672c-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="f672c-123">为此，在波次流程方法页上为此方法选择“可重复”。</span><span class="sxs-lookup"><span data-stu-id="f672c-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="f672c-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-124">Click Save.</span></span>
11. <span data-ttu-id="f672c-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f672c-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="f672c-126">设置集装箱类型</span><span class="sxs-lookup"><span data-stu-id="f672c-126">Set up a container type</span></span>
1. <span data-ttu-id="f672c-127">转到“仓库管理”>“设置”>“集装箱”>“集装箱类型”。</span><span class="sxs-lookup"><span data-stu-id="f672c-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="f672c-128">您可以在集装箱类型页定义您的集装箱。</span><span class="sxs-lookup"><span data-stu-id="f672c-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="f672c-129">您可以配置集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和高度。</span><span class="sxs-lookup"><span data-stu-id="f672c-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="f672c-130">在此示例中，我们有三种不同的箱尺寸。</span><span class="sxs-lookup"><span data-stu-id="f672c-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="f672c-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-131">Click New.</span></span>
3. <span data-ttu-id="f672c-132">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="f672c-133">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="f672c-134">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="f672c-135">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="f672c-136">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="f672c-137">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="f672c-138">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="f672c-139">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f672c-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-140">Click Save.</span></span>
12. <span data-ttu-id="f672c-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-141">Click New.</span></span>
13. <span data-ttu-id="f672c-142">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="f672c-143">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f672c-144">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="f672c-145">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="f672c-146">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="f672c-147">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="f672c-148">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="f672c-149">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="f672c-150">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-150">Click Save.</span></span>
22. <span data-ttu-id="f672c-151">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-151">Click New.</span></span>
23. <span data-ttu-id="f672c-152">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="f672c-153">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="f672c-154">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="f672c-155">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="f672c-156">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="f672c-157">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="f672c-158">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="f672c-159">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="f672c-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="f672c-160">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-160">Click Save.</span></span>
32. <span data-ttu-id="f672c-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f672c-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="f672c-162">设置集装箱组</span><span class="sxs-lookup"><span data-stu-id="f672c-162">Set up a container group</span></span>
1. <span data-ttu-id="f672c-163">转到“仓库管理”>“设置”>“集装箱”>“集装箱组”。</span><span class="sxs-lookup"><span data-stu-id="f672c-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="f672c-164">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-164">Click New.</span></span>
    * <span data-ttu-id="f672c-165">可以设置集装箱类型的逻辑组。</span><span class="sxs-lookup"><span data-stu-id="f672c-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="f672c-166">对于每个组，可以指定集装箱包装和集装箱填充百分比的序列。物料的尺寸维度用于决定其在集装箱中是否合适。</span><span class="sxs-lookup"><span data-stu-id="f672c-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="f672c-167">使用最接近物料尺寸维度的集装箱。</span><span class="sxs-lookup"><span data-stu-id="f672c-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="f672c-168">如果在组中有多个集装箱类型，我们建议您按尺寸排列顺序，因此最大的集装箱在序列中排第一，编号为 1，最小的集装箱排最后。</span><span class="sxs-lookup"><span data-stu-id="f672c-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="f672c-169">在“集装箱组 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="f672c-170">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f672c-171">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-171">Click New.</span></span>
6. <span data-ttu-id="f672c-172">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f672c-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f672c-173">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="f672c-174">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-174">Click New.</span></span>
9. <span data-ttu-id="f672c-175">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f672c-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f672c-176">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="f672c-177">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-177">Click New.</span></span>
12. <span data-ttu-id="f672c-178">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f672c-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f672c-179">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="f672c-180">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-180">Click Save.</span></span>
15. <span data-ttu-id="f672c-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f672c-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="f672c-182">设置集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="f672c-182">Set up a container build template</span></span>
1. <span data-ttu-id="f672c-183">转到“仓库管理”>“设置”>“集装箱”>“集装箱生成模板”。</span><span class="sxs-lookup"><span data-stu-id="f672c-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="f672c-184">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-184">Click New.</span></span>
    * <span data-ttu-id="f672c-185">集装箱生成模板基于执行的集装化流程。</span><span class="sxs-lookup"><span data-stu-id="f672c-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="f672c-186">每个集装箱生成模板定义波次模板将使用的一个集装化流程。</span><span class="sxs-lookup"><span data-stu-id="f672c-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="f672c-187">“编辑查询”选项允许您定义将处理所选模板的条件。</span><span class="sxs-lookup"><span data-stu-id="f672c-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="f672c-188">例如，您可能想要只运行特定客户、产品或者仓库的集装化，或您可以添加相应查询范围到该模板。</span><span class="sxs-lookup"><span data-stu-id="f672c-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="f672c-189">“波次步骤代码”字段是集装箱生成模板如何与波次模板中的步骤关联。</span><span class="sxs-lookup"><span data-stu-id="f672c-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="f672c-190">在执行波次时，它确定哪些集装箱生成模板用于启用集装化。</span><span class="sxs-lookup"><span data-stu-id="f672c-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="f672c-191">“基本查询类型”字段确定包装内容和筛选器查询的基础。</span><span class="sxs-lookup"><span data-stu-id="f672c-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="f672c-192">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f672c-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f672c-193">在“集装箱模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="f672c-194">在“集装箱组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="f672c-195">在“波次步骤代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="f672c-196">选中“允许拆分领料”复选框。</span><span class="sxs-lookup"><span data-stu-id="f672c-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="f672c-197">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f672c-197">Click Save.</span></span>
9. <span data-ttu-id="f672c-198">单击“集装箱混合约束”。</span><span class="sxs-lookup"><span data-stu-id="f672c-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="f672c-199">混合逻辑分隔符允许您为集装箱内的包装分配行设置规则。</span><span class="sxs-lookup"><span data-stu-id="f672c-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="f672c-200">例如，如果您添加物料编号字段，物料分配给集装箱，在存在新的物料编号时将创建新集装箱。</span><span class="sxs-lookup"><span data-stu-id="f672c-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="f672c-201">这将阻止工作人员在同一个集装箱中包装两个不同客户的分配行。</span><span class="sxs-lookup"><span data-stu-id="f672c-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="f672c-202">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f672c-202">Click New.</span></span>
11. <span data-ttu-id="f672c-203">在“表”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f672c-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="f672c-204">在“字段选择”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f672c-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="f672c-205">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f672c-205">Click OK.</span></span>

