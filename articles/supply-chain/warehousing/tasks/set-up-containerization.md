--- 
title: "设置集装化"
description: "此过程描述如何在“仓库管理”中自动进行装载集装化。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4e7a2fde65c8dba8b16c5a87eae0ec2bbebc3388
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="a9092-103">设置集装化</span><span class="sxs-lookup"><span data-stu-id="a9092-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9092-104">此过程描述如何在“仓库管理”中自动进行装载集装化。</span><span class="sxs-lookup"><span data-stu-id="a9092-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="a9092-105">自动执行集装化在处理波次，且工作行可以分解为适合集装箱的数量时，创建集装箱和用于装运的领料工作。</span><span class="sxs-lookup"><span data-stu-id="a9092-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="a9092-106">这有助于仓库工作人员将物料直接拣选到选择的集装箱内。</span><span class="sxs-lookup"><span data-stu-id="a9092-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="a9092-107">与手动包装流程对比，创建集装箱、分配物料和封闭集装箱等任务由系统自动执行。</span><span class="sxs-lookup"><span data-stu-id="a9092-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="a9092-108">此过程使用 USMF 演示公司，并由仓库经理执行。</span><span class="sxs-lookup"><span data-stu-id="a9092-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="a9092-109">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="a9092-109">Set up a wave template</span></span>
1. <span data-ttu-id="a9092-110">转到“仓库管理”>“设置”>“波次”>“波次模板”。</span><span class="sxs-lookup"><span data-stu-id="a9092-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="a9092-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-111">Click New.</span></span>
3. <span data-ttu-id="a9092-112">在“波次模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="a9092-113">在“波次模板描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="a9092-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="a9092-115">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="a9092-116">展开“方法”部分。</span><span class="sxs-lookup"><span data-stu-id="a9092-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="a9092-117">“已选定方法”窗格列出了所选波模板类型的方法。</span><span class="sxs-lookup"><span data-stu-id="a9092-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="a9092-118">波次模板必须包括集装化方法。</span><span class="sxs-lookup"><span data-stu-id="a9092-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="a9092-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a9092-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a9092-120">在“波次步骤代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="a9092-121">键入添加方法的一个波次步骤代码，可以是任意代码。</span><span class="sxs-lookup"><span data-stu-id="a9092-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="a9092-122">可以多次添加方法，并分配不同的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="a9092-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="a9092-123">为此，在波次流程方法页上为此方法选择“可重复”。</span><span class="sxs-lookup"><span data-stu-id="a9092-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="a9092-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-124">Click Save.</span></span>
11. <span data-ttu-id="a9092-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a9092-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="a9092-126">设置集装箱类型</span><span class="sxs-lookup"><span data-stu-id="a9092-126">Set up a container type</span></span>
1. <span data-ttu-id="a9092-127">转到“仓库管理”>“设置”>“集装箱”>“集装箱类型”。</span><span class="sxs-lookup"><span data-stu-id="a9092-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="a9092-128">您可以在集装箱类型页定义您的集装箱。</span><span class="sxs-lookup"><span data-stu-id="a9092-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="a9092-129">您可以配置集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和高度。</span><span class="sxs-lookup"><span data-stu-id="a9092-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="a9092-130">在此示例中，我们有三种不同的箱尺寸。</span><span class="sxs-lookup"><span data-stu-id="a9092-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="a9092-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-131">Click New.</span></span>
3. <span data-ttu-id="a9092-132">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="a9092-133">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="a9092-134">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="a9092-135">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="a9092-136">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="a9092-137">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="a9092-138">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="a9092-139">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="a9092-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-140">Click Save.</span></span>
12. <span data-ttu-id="a9092-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-141">Click New.</span></span>
13. <span data-ttu-id="a9092-142">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="a9092-143">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="a9092-144">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="a9092-145">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="a9092-146">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="a9092-147">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="a9092-148">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="a9092-149">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="a9092-150">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-150">Click Save.</span></span>
22. <span data-ttu-id="a9092-151">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-151">Click New.</span></span>
23. <span data-ttu-id="a9092-152">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="a9092-153">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="a9092-154">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="a9092-155">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="a9092-156">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="a9092-157">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="a9092-158">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="a9092-159">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="a9092-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="a9092-160">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-160">Click Save.</span></span>
32. <span data-ttu-id="a9092-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a9092-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="a9092-162">设置集装箱组</span><span class="sxs-lookup"><span data-stu-id="a9092-162">Set up a container group</span></span>
1. <span data-ttu-id="a9092-163">转到“仓库管理”>“设置”>“集装箱”>“集装箱组”。</span><span class="sxs-lookup"><span data-stu-id="a9092-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="a9092-164">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-164">Click New.</span></span>
    * <span data-ttu-id="a9092-165">可以设置集装箱类型的逻辑组。</span><span class="sxs-lookup"><span data-stu-id="a9092-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="a9092-166">对于每个组，您可以指定包装集装箱的顺序和要填充的集装箱的百分比。</span><span class="sxs-lookup"><span data-stu-id="a9092-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="a9092-167">物料的尺寸维度用来确定其是否适合集装箱。</span><span class="sxs-lookup"><span data-stu-id="a9092-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="a9092-168">使用最接近物料尺寸维度的集装箱。</span><span class="sxs-lookup"><span data-stu-id="a9092-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="a9092-169">如果在组中有多个集装箱类型，我们建议您按尺寸排列顺序，因此最大的集装箱在序列中排第一，编号为 1，最小的集装箱排最后。</span><span class="sxs-lookup"><span data-stu-id="a9092-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="a9092-170">在“集装箱组 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="a9092-171">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a9092-172">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-172">Click New.</span></span>
6. <span data-ttu-id="a9092-173">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a9092-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a9092-174">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="a9092-175">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-175">Click New.</span></span>
9. <span data-ttu-id="a9092-176">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a9092-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="a9092-177">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="a9092-178">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-178">Click New.</span></span>
12. <span data-ttu-id="a9092-179">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a9092-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a9092-180">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="a9092-181">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-181">Click Save.</span></span>
15. <span data-ttu-id="a9092-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a9092-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="a9092-183">设置集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="a9092-183">Set up a container build template</span></span>
1. <span data-ttu-id="a9092-184">转到“仓库管理”>“设置”>“集装箱”>“集装箱生成模板”。</span><span class="sxs-lookup"><span data-stu-id="a9092-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="a9092-185">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-185">Click New.</span></span>
    * <span data-ttu-id="a9092-186">集装箱生成模板基于执行的集装化流程。</span><span class="sxs-lookup"><span data-stu-id="a9092-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="a9092-187">每个集装箱生成模板定义波次模板将使用的一个集装化流程。</span><span class="sxs-lookup"><span data-stu-id="a9092-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="a9092-188">“编辑查询”选项允许您定义将处理所选模板的条件。</span><span class="sxs-lookup"><span data-stu-id="a9092-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="a9092-189">例如，您可能想要只运行特定客户、产品或者仓库的集装化，或您可以添加相应查询范围到该模板。</span><span class="sxs-lookup"><span data-stu-id="a9092-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="a9092-190">“波次步骤代码”字段是集装箱生成模板如何与波次模板中的步骤关联。</span><span class="sxs-lookup"><span data-stu-id="a9092-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="a9092-191">在执行波次时，它确定哪些集装箱生成模板用于启用集装化。</span><span class="sxs-lookup"><span data-stu-id="a9092-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="a9092-192">“基本查询类型”字段确定包装内容和筛选器查询的基础。</span><span class="sxs-lookup"><span data-stu-id="a9092-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="a9092-193">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a9092-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a9092-194">在“集装箱模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="a9092-195">在“集装箱组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="a9092-196">在“波次步骤代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="a9092-197">选中“允许拆分领料”复选框。</span><span class="sxs-lookup"><span data-stu-id="a9092-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="a9092-198">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a9092-198">Click Save.</span></span>
9. <span data-ttu-id="a9092-199">单击“集装箱混合约束”。</span><span class="sxs-lookup"><span data-stu-id="a9092-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="a9092-200">混合逻辑分隔符允许您为集装箱内的包装分配行设置规则。</span><span class="sxs-lookup"><span data-stu-id="a9092-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="a9092-201">例如，如果您添加物料编号字段，物料分配给集装箱，在存在新的物料编号时将创建新集装箱。</span><span class="sxs-lookup"><span data-stu-id="a9092-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="a9092-202">这将阻止工作人员在同一个集装箱中包装两个不同客户的分配行。</span><span class="sxs-lookup"><span data-stu-id="a9092-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="a9092-203">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a9092-203">Click New.</span></span>
11. <span data-ttu-id="a9092-204">在“表”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a9092-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="a9092-205">在“字段选择”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a9092-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="a9092-206">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a9092-206">Click OK.</span></span>


