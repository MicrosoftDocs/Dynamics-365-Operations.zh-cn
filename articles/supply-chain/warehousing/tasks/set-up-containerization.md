---
title: 设置集装化
description: 本主题描述如何在“仓库管理”中自动进行装载集装化。
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f961dc379ceeeae9bbceec1baaa9b9be21316f3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017774"
---
# <a name="set-up-containerization"></a><span data-ttu-id="c48cf-103">设置集装化</span><span class="sxs-lookup"><span data-stu-id="c48cf-103">Set up containerization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c48cf-104">本主题描述如何在“仓库管理”中自动进行装载集装化。</span><span class="sxs-lookup"><span data-stu-id="c48cf-104">This topic describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="c48cf-105">自动执行集装化在处理波次，且工作行可以分解为适合集装箱的数量时，创建集装箱和用于装运的领料工作。</span><span class="sxs-lookup"><span data-stu-id="c48cf-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="c48cf-106">这有助于仓库工作人员将物料直接拣选到选择的集装箱内。</span><span class="sxs-lookup"><span data-stu-id="c48cf-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="c48cf-107">与手动包装流程对比，创建集装箱、分配物料和封闭集装箱等任务由系统自动执行。</span><span class="sxs-lookup"><span data-stu-id="c48cf-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="c48cf-108">此过程使用 USMF 演示公司，并由仓库经理执行。</span><span class="sxs-lookup"><span data-stu-id="c48cf-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="c48cf-109">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="c48cf-109">Set up a wave template</span></span>
1. <span data-ttu-id="c48cf-110">在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 波次 > 波次模板** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Waves > Wave templates**.</span></span>
2. <span data-ttu-id="c48cf-111">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-111">Select **New**.</span></span>
3. <span data-ttu-id="c48cf-112">在 **波次模板名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-112">In the **Wave template name** field, type a value.</span></span>
4. <span data-ttu-id="c48cf-113">在 **波次模板描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-113">In the **Wave template description** field, type a value.</span></span>
5. <span data-ttu-id="c48cf-114">在 **站点** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-114">In the **Site** field, enter or select a value.</span></span>
6. <span data-ttu-id="c48cf-115">在 **仓库** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-115">In the **Warehouse** field, enter or select a value.</span></span>
7. <span data-ttu-id="c48cf-116">展开 **方法** 部分。</span><span class="sxs-lookup"><span data-stu-id="c48cf-116">Expand the **Methods** section.</span></span> <span data-ttu-id="c48cf-117">**已选定方法** 窗格列出了所选波模板类型的方法。</span><span class="sxs-lookup"><span data-stu-id="c48cf-117">The **Selected methods** pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="c48cf-118">波次模板必须包括集装化方法。</span><span class="sxs-lookup"><span data-stu-id="c48cf-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="c48cf-119">在 **波次步骤代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-119">In the **Wave step code** field, type a value.</span></span> <span data-ttu-id="c48cf-120">键入添加方法的一个波次步骤代码，可以是任意代码。</span><span class="sxs-lookup"><span data-stu-id="c48cf-120">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="c48cf-121">可以多次添加方法，并分配不同的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="c48cf-121">It's possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="c48cf-122">为此，在 **波次流程方法** 页上选择 **对此方法可重复** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-122">To do this, select **Repeatable for this method** in the **Wave process methods** page.</span></span>  
9. <span data-ttu-id="c48cf-123">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-123">Select **Save**.</span></span>
10. <span data-ttu-id="c48cf-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c48cf-124">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="c48cf-125">设置集装箱类型</span><span class="sxs-lookup"><span data-stu-id="c48cf-125">Set up a container type</span></span>
1. <span data-ttu-id="c48cf-126">在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱类型** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-126">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container types**.</span></span> <span data-ttu-id="c48cf-127">您可以在 **集装箱类型** 页定义您的集装箱。</span><span class="sxs-lookup"><span data-stu-id="c48cf-127">You can define your containers in the **Container types** page.</span></span> <span data-ttu-id="c48cf-128">您可以配置集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和高度。</span><span class="sxs-lookup"><span data-stu-id="c48cf-128">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="c48cf-129">在此示例中，我们有三种不同的箱尺寸。</span><span class="sxs-lookup"><span data-stu-id="c48cf-129">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="c48cf-130">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-130">Select **New**.</span></span>
3. <span data-ttu-id="c48cf-131">在 **集装箱类型代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-131">In the **Container type code** field, type a value.</span></span>
4. <span data-ttu-id="c48cf-132">在 **皮重** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-132">In the **Tare weight** field, enter a number.</span></span>
5. <span data-ttu-id="c48cf-133">在 **最大重量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-133">In the **Maximum weight** field, enter a number.</span></span>
6. <span data-ttu-id="c48cf-134">在 **体积** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-134">In the **Volume** field, enter a number.</span></span>
7. <span data-ttu-id="c48cf-135">在 **长度** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-135">In the **Length** field, enter a number.</span></span>
8. <span data-ttu-id="c48cf-136">在 **宽度** 字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-136">In the **Width** field, enter a number.</span></span>
9. <span data-ttu-id="c48cf-137">在 **高度** 字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="c48cf-137">In the **Height** field, enter a number.</span></span>
10. <span data-ttu-id="c48cf-138">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-138">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="c48cf-139">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-139">Select **Save**.</span></span>
13. <span data-ttu-id="c48cf-140">再重复执行步骤 2-11 两次，以便创建总计三个集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="c48cf-140">Repeat steps 2-11 two more times to make three total container types.</span></span>
14. <span data-ttu-id="c48cf-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c48cf-141">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="c48cf-142">设置集装箱组</span><span class="sxs-lookup"><span data-stu-id="c48cf-142">Set up a container group</span></span>
1. <span data-ttu-id="c48cf-143">在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱组** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-143">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container groups**.</span></span>
2. <span data-ttu-id="c48cf-144">在操作窗格上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-144">On the Action Pane, select **New**.</span></span> <span data-ttu-id="c48cf-145">可以设置集装箱类型的逻辑组。</span><span class="sxs-lookup"><span data-stu-id="c48cf-145">You can set up logical groups of container types.</span></span> <span data-ttu-id="c48cf-146">对于每个组，可以指定集装箱包装和集装箱填充百分比的序列。物料的尺寸维度用于决定其在集装箱中是否合适。</span><span class="sxs-lookup"><span data-stu-id="c48cf-146">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="c48cf-147">使用最接近物料尺寸维度的集装箱。</span><span class="sxs-lookup"><span data-stu-id="c48cf-147">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="c48cf-148">如果在组中有多个集装箱类型，我们建议您按尺寸排列顺序，因此最大的集装箱在序列中排第一，编号为 1，最小的集装箱排最后。</span><span class="sxs-lookup"><span data-stu-id="c48cf-148">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="c48cf-149">在 **集装箱组 ID** 字段中，键入您之前创建的值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-149">In the **Container group ID** field, type a value that you created earlier.</span></span>
4. <span data-ttu-id="c48cf-150">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-150">In the **Description field** , type a value.</span></span>
5. <span data-ttu-id="c48cf-151">对前面创建的所有三个集装箱类型重复执行步骤 2-4。</span><span class="sxs-lookup"><span data-stu-id="c48cf-151">Repeat steps 2-4 for all three container types you created earlier.</span></span>
6. <span data-ttu-id="c48cf-152">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-152">Select **Save**.</span></span>
7. <span data-ttu-id="c48cf-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c48cf-153">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="c48cf-154">设置集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="c48cf-154">Set up a container build template</span></span>
1. <span data-ttu-id="c48cf-155">在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱生成模板** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-155">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container build templates**.</span></span>
2. <span data-ttu-id="c48cf-156">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-156">Select **New**.</span></span> <span data-ttu-id="c48cf-157">集装箱生成模板基于执行的集装化流程。</span><span class="sxs-lookup"><span data-stu-id="c48cf-157">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="c48cf-158">每个集装箱生成模板定义波次模板将使用的一个集装化流程。</span><span class="sxs-lookup"><span data-stu-id="c48cf-158">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="c48cf-159">**编辑查询** 选项允许您定义将处理所选模板的条件。</span><span class="sxs-lookup"><span data-stu-id="c48cf-159">The **Edit query** option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="c48cf-160">例如，您可能想要只运行特定客户、产品或者仓库的集装化，或您可以添加相应查询范围到该模板。</span><span class="sxs-lookup"><span data-stu-id="c48cf-160">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="c48cf-161">**波次步骤代码** 字段是集装箱生成模板如何与波次模板中的步骤关联。</span><span class="sxs-lookup"><span data-stu-id="c48cf-161">The **Wave step code** field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="c48cf-162">在执行波次时，它确定哪些集装箱生成模板用于启用集装化。</span><span class="sxs-lookup"><span data-stu-id="c48cf-162">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="c48cf-163">“基本查询类型”字段确定包装内容和筛选器查询的基础。</span><span class="sxs-lookup"><span data-stu-id="c48cf-163">The Base query type field determines what to pack and what to base the filter query on.</span></span> 
3. <span data-ttu-id="c48cf-164">在 **集装箱模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-164">In the **Container template ID** field, type a value.</span></span>
4. <span data-ttu-id="c48cf-165">在 **集装箱组 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-165">In the **Container group ID** field, enter or select a value.</span></span>
5. <span data-ttu-id="c48cf-166">在 **波次步骤代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-166">In the **Wave step code** field, type a value.</span></span>
6. <span data-ttu-id="c48cf-167">选中 **允许拆分领料** 复选框。</span><span class="sxs-lookup"><span data-stu-id="c48cf-167">Select the **Allow split picks** check box.</span></span>
7. <span data-ttu-id="c48cf-168">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-168">Select **Save**.</span></span>
8. <span data-ttu-id="c48cf-169">选择 **集装箱混合约束** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-169">Select **Container mixing constraints**.</span></span> <span data-ttu-id="c48cf-170">混合逻辑分隔符允许您为集装箱内的包装分配行设置规则。</span><span class="sxs-lookup"><span data-stu-id="c48cf-170">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="c48cf-171">例如，如果您添加 **物料编号字段** ，物料分配给集装箱，在存在新的物料编号时将创建新集装箱。</span><span class="sxs-lookup"><span data-stu-id="c48cf-171">For example, if you add the **Item number field** , when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="c48cf-172">这将阻止工作人员在同一个集装箱中包装两个不同客户的分配行。</span><span class="sxs-lookup"><span data-stu-id="c48cf-172">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
9. <span data-ttu-id="c48cf-173">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-173">Select **New**.</span></span>
10. <span data-ttu-id="c48cf-174">在 **表** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="c48cf-174">In the **Table** field, select an option.</span></span>
11. <span data-ttu-id="c48cf-175">在 **字段选择** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c48cf-175">In the **Field Select** field, enter or select a value.</span></span>
12. <span data-ttu-id="c48cf-176">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="c48cf-176">Select **OK**.</span></span>

