---
title: 集装化
description: 本主题介绍如何自动进行装载集装化。 在处理波次时，自动集装化创建集装箱和装运的领料工作。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: c62e2d1b361e0ed1ab1ced42997add157b30c828
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019043"
---
# <a name="containerization"></a><span data-ttu-id="e3cf8-104">集装化</span><span class="sxs-lookup"><span data-stu-id="e3cf8-104">Containerization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3cf8-105">本主题介绍如何自动进行装载集装化。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-105">This topic describes how to automate the containerization of loads.</span></span> <span data-ttu-id="e3cf8-106">在处理波次时，自动集装化创建集装箱和装运的领料工作。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-106">Automated containerization creates containers and the picking work for shipments when a wave is processed.</span></span>

<span data-ttu-id="e3cf8-107">若要设置集装化，必须创建以下内容：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-107">To set up containerization, you must create the following:</span></span>

- <span data-ttu-id="e3cf8-108">**集装箱类型** ─ 定义集装箱的物理特征。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-108">**Container type** ─ Define the physical characteristics of the containers.</span></span> <span data-ttu-id="e3cf8-109">使用集装箱类型将库存物料打包到特定类型和尺寸的包装中，例如储料箱或托盘。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-109">Use container types to pack inventory items into a specific type and size of packaging, such as bins or pallets.</span></span>
- <span data-ttu-id="e3cf8-110">**集装箱组** ─ 创建相似集装箱类型的组。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-110">**Container groups** ─ Create groups of container types that are similar.</span></span> <span data-ttu-id="e3cf8-111">例如，集装箱组可以包含相似尺寸维度的集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-111">For example, a container group can include container types that have similar size dimensions.</span></span> <span data-ttu-id="e3cf8-112">集装箱组指定集装箱打包的序列和每个集装箱的填充百分比。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-112">A container group specifies the sequence in which containers are packed, and the fill percentage of each container.</span></span>
- <span data-ttu-id="e3cf8-113">**集装箱生成模板** ─ 创建定义集装化规则的模板。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-113">**Container build template** ─ Create templates that define rules for containerization.</span></span> <span data-ttu-id="e3cf8-114">例如，混装库存和其他包装策略的规则。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-114">For example, rules for mixing inventory and other packing strategies.</span></span>
- <span data-ttu-id="e3cf8-115">**波次模板** – 设置一个或多个波次模板来为集装化创建领料工作。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-115">**Wave templates** – Set up one or more wave templates to create the picking work for containerization.</span></span>

## <a name="create-wave-templates-for-containerization"></a><span data-ttu-id="e3cf8-116">为集装化创建波次模板</span><span class="sxs-lookup"><span data-stu-id="e3cf8-116">Create wave templates for containerization</span></span>

<span data-ttu-id="e3cf8-117">必须为集装化设置一个或多个装运波次模板。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-117">You must set up one or more shipping wave templates for containerization.</span></span> <span data-ttu-id="e3cf8-118">波次模板包括确定以下内容的条件：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-118">Wave templates include criteria that determine the following:</span></span>

- <span data-ttu-id="e3cf8-119">如何处理波次。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-119">How to process waves.</span></span> <span data-ttu-id="e3cf8-120">这可以手动，也可以自动。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-120">This can be either manual or automatic.</span></span>
- <span data-ttu-id="e3cf8-121">如何创建领料工作。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-121">How to create picking work.</span></span> <span data-ttu-id="e3cf8-122">这由波次方法决定。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-122">This is determined by the wave methods.</span></span> <span data-ttu-id="e3cf8-123">波次模板必须包括 **集装化** 方法。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-123">The wave template must include the **containerization** method.</span></span>
- <span data-ttu-id="e3cf8-124">如何将物料或分配行与波次匹配。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-124">How to match items or allocation lines with a wave.</span></span>

<span data-ttu-id="e3cf8-125">有关详细信息，请参阅[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-125">For more information, see [Wave templates](wave-templates.md).</span></span>

## <a name="create-container-types"></a><span data-ttu-id="e3cf8-126">创建集装箱类型</span><span class="sxs-lookup"><span data-stu-id="e3cf8-126">Create container types</span></span>

<span data-ttu-id="e3cf8-127">使用集装箱类型来创建集装箱描述，包括实际尺寸维度和重量产能的最大值。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-127">Use container types to create descriptions of containers, including maximum values for physical size dimensions and weight capacity.</span></span> <span data-ttu-id="e3cf8-128">在处理集装化波次时，基于集装箱类型信息创建集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-128">When a containerized wave is processed, the containers are created based on the container type information.</span></span>

<span data-ttu-id="e3cf8-129">若要设置集装箱类型，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-129">To set up a container type, follow these steps:</span></span>

1. <span data-ttu-id="e3cf8-130">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱类型**。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-130">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container type**.</span></span>
1. <span data-ttu-id="e3cf8-131">选择 **新建** 以创建新的集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-131">Select **New** to create a new container type.</span></span>
1. <span data-ttu-id="e3cf8-132">输入集装箱类型的唯一标识符 (ID) 和描述。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-132">Enter a unique identifier (ID) and description for the container type.</span></span>
1. <span data-ttu-id="e3cf8-133">在 **皮重** 字段中，输入集装箱的实际重量或估计重量。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-133">In the **Tare weight** field, enter the actual or estimated weight of the container.</span></span>
1. <span data-ttu-id="e3cf8-134">在 **最大重量** 字段中，输入集装箱可承受的最大重量。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-134">In the **Maximum weight** field, enter the maximum weight that the container can hold.</span></span>
1. <span data-ttu-id="e3cf8-135">在 **集装化最大容量**、**集装化最大长度**、**集装化最大宽度** 和 **集装化最大高度** 字段中，指定集装箱的物理维度。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-135">In the **Containerization maximum volume**, **Containerization maximum length**, **Containerization maximum width**, and **Containerization maximum height** fields, specify the physical dimensions of the container.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3cf8-136">长度和宽度的值可以交换。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-136">The values for length and width are interchangeable.</span></span> <span data-ttu-id="e3cf8-137">如果需要，这意味着可以横向或在 x 轴上旋转物料。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-137">This means that you can rotate items laterally, or on the x-axis, if needed.</span></span> <span data-ttu-id="e3cf8-138">例如，如果该长度为 2 英尺，宽度为 1 英尺，则可以更改该长度为 1 英尺，宽度为 2 英尺。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-138">For example, if the length is 2 feet, and the width is 1 foot, you can change the length to 1 foot and the width to 2 feet.</span></span> <span data-ttu-id="e3cf8-139">请注意，这不适用于高度维度。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-139">Note that this does not apply to the height dimension.</span></span> <span data-ttu-id="e3cf8-140">不能更改高度值来垂直旋转物料。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-140">You cannot change the height value to rotate an item vertically.</span></span>

1. <span data-ttu-id="e3cf8-141">为集装箱的属性字段选择自定义属性值。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-141">Select custom attribute values for the container in the fields for attributes.</span></span> <span data-ttu-id="e3cf8-142">属性是自定义值，用于基于一个值筛选或排序，否则该值不可用。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-142">Attributes are custom values that are used to filter or sort items based on a value that is otherwise not available.</span></span> <span data-ttu-id="e3cf8-143">例如，如果要为特定客户包装物料，可以为客户名称创建一个属性。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-143">For example, if you want to pack items for a particular customer, you can create an attribute for the customer name.</span></span> <span data-ttu-id="e3cf8-144">在 **集装箱属性** 页面上创建属性。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-144">You create attributes on the **Container attributes** page.</span></span>

## <a name="create-container-groups"></a><span data-ttu-id="e3cf8-145">创建集装箱组</span><span class="sxs-lookup"><span data-stu-id="e3cf8-145">Create container groups</span></span>

<span data-ttu-id="e3cf8-146">可以设置集装箱类型的逻辑组。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-146">You can set up logical groups of container types.</span></span> <span data-ttu-id="e3cf8-147">对于每个组，您可以指定包装集装箱的顺序和要填充的集装箱的百分比。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-147">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="e3cf8-148">物料的尺寸维度可确定其是否适合集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-148">The size dimensions of the item determine whether it will fit in a container.</span></span> <span data-ttu-id="e3cf8-149">使用最接近物料尺寸维度的集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-149">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="e3cf8-150">如果在组中有多个集装箱类型，我们建议您按尺寸排列顺序，因此最大的集装箱在序列中排第一，编号为 1，最小的集装箱排最后。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-150">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>

<span data-ttu-id="e3cf8-151">若要设置集装箱组，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-151">To set up a container group, follow these steps:</span></span>

1. <span data-ttu-id="e3cf8-152">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱组**。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-152">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="e3cf8-153">选择 **新建** 以创建集装箱组。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-153">Select **New** to create a container group.</span></span>
1. <span data-ttu-id="e3cf8-154">输入集装箱组的唯一 ID 和描述。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-154">Enter a unique ID and description for the container group.</span></span>
1. <span data-ttu-id="e3cf8-155">在 **详细信息** 快速选项卡上，选择 **新建** 以向组添加集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-155">On the **Details** FastTab, select **New** to add a container type to the group.</span></span>
1. <span data-ttu-id="e3cf8-156">在 **集装箱类型** 字段中，选择集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-156">In the **Container type** field, select a container type.</span></span>
1. <span data-ttu-id="e3cf8-157">选择 **上移** 或 **下移** 以指定包装集装箱类型的顺序。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-157">Select **Move up** or **Move down** to specify the sequence in which the container types are packed.</span></span>

## <a name="create-container-build-templates"></a><span data-ttu-id="e3cf8-158">创建集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="e3cf8-158">Create container build templates</span></span>

<span data-ttu-id="e3cf8-159">可以设置集装化流程的规则，例如库存混装规则和其他包装策略。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-159">You can set up rules for the containerization process, such as inventory mixing rules and other packing strategies.</span></span> <span data-ttu-id="e3cf8-160">例如，可以设置规则，以便工作人员不能在同一集装箱内包装代表来自不同客户的销售订单的分配行。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-160">For example, you can set up a rule so that workers cannot pack allocation lines that represent sales orders from different customers in the same container.</span></span>

<span data-ttu-id="e3cf8-161">若要设置集装箱生成模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-161">To set up a container build template, follow these steps.</span></span>

1. <span data-ttu-id="e3cf8-162">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱生成模板**。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-162">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="e3cf8-163">创建新的集装箱生成模板。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-163">Create a new container build template.</span></span>
1. <span data-ttu-id="e3cf8-164">在 **集装化名称** 和 **序列号** 字段中，输入集装化模板的名称和与分配行匹配的订单名称。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-164">In the **Containerization name** and **Sequence number** fields, enter the name of the containerization template and the order that is matched to allocation lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3cf8-165">系统将应用满足分配行查询条件的第一个模板。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-165">The system will apply the first template that the allocation line meets the query criteria for.</span></span> <span data-ttu-id="e3cf8-166">因此，将具有最具体条件的模板放在列表顶部。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-166">Therefore, put the template with the most specific criteria at the top of the list.</span></span> <span data-ttu-id="e3cf8-167">条件越广泛，分配行满足条件的可能性越大。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-167">The broader the criteria, the more likely that an allocation line will meet the criteria.</span></span> <span data-ttu-id="e3cf8-168">这可能导致将行分配到错误的集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-168">This could lead to lines being assigned to the wrong container.</span></span> <span data-ttu-id="e3cf8-169">如果需要，您可以选择 **上移** 或 **下移** 更改模板的顺序。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-169">If needed, you can select **Move up** or **Move down** to change the sequence of templates.</span></span>

1. <span data-ttu-id="e3cf8-170">在 **集装箱组 ID** 字段中，选择创建集装箱的集装箱组。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-170">In the **Container group ID** field, select the container group from which to create containers.</span></span>
1. <span data-ttu-id="e3cf8-171">在 **基本查询类型** 字段中，选择决定包装内容和筛选器查询基础的查询类型。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-171">In the **Base query types** field, select the query type that will determine what to pack and what to base the filter query on.</span></span> <span data-ttu-id="e3cf8-172">选项如下：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-172">The following options are available:</span></span>

      - <span data-ttu-id="e3cf8-173">**销售分配行** ─ 为销售订单创建的包装分配行。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-173">**Sales allocation line** ─ Pack allocation lines that are created for sales orders.</span></span>
      - <span data-ttu-id="e3cf8-174">**转移分配行** ─ 为转移单创建的包装分配行。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-174">**Transfer allocation line** ─ Pack allocation lines that are created for transfer orders.</span></span>
      - <span data-ttu-id="e3cf8-175">**集装箱** ─ 包装已由集装化流程创建的集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-175">**Container** ─ Pack a container that was already created by the containerization process.</span></span> <span data-ttu-id="e3cf8-176">例如，这用于嵌套集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-176">For example, this is used for nesting containers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e3cf8-177">若要使用嵌套集装箱，必须使集装化方法可重复执行。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-177">To use nesting containers, you must make the containerization method repeatable.</span></span> <span data-ttu-id="e3cf8-178">有关详细信息，请参阅[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-178">For more information, see [Wave templates](wave-templates.md).</span></span>

1. <span data-ttu-id="e3cf8-179">在 **常规** 快速选项卡上的 **波次步骤代码** 字段中，输入将集装箱生成模板链接到波次模板中的步骤的波次流程方法的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-179">On the **General** FastTab, in the **Wave step code** field, enter the unique identifier of the wave process method that links the container build template to steps in a wave template.</span></span>
1. <span data-ttu-id="e3cf8-180">选中 **允许拆分领料** 复选框以允许工作人员在单独的集装箱内按工作订单包装物料。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-180">Select the **Allow split picks** check box to allow workers to pack items from a work order in separate containers.</span></span> <span data-ttu-id="e3cf8-181">这要求集装箱中的整个数量合适。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-181">This requires that the entire quantity fits in the container.</span></span> <span data-ttu-id="e3cf8-182">始终使用分配行中的最大度量单位。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-182">The largest unit of measure in the allocation line is always used.</span></span>
1. <span data-ttu-id="e3cf8-183">在 **按单位包装** 字段中，选择代表集装箱的度量单位。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-183">In the **Pack by unit** field, select the unit of measure that will represent the container.</span></span> <span data-ttu-id="e3cf8-184">例如，可以指示案例为集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-184">For example, you can indicate that a case is a container.</span></span> <span data-ttu-id="e3cf8-185">如果按度量单位包装，则无法再指定集装箱组，因为度量单位是集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-185">If you pack by the unit of measure, you cannot also specify a container group because the unit of measure is the container.</span></span>
1. <span data-ttu-id="e3cf8-186">在 **集装箱包装策略** 字段中，选择要使用的包装策略。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-186">In the **Container packing strategy** field, select the packing strategy to use.</span></span> <span data-ttu-id="e3cf8-187">选项如下：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-187">The following options are available:</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3cf8-188">此策略仅适用于销售分配行和转移分配行。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-188">The strategy applies only to sales allocation lines and transfer allocation lines.</span></span>

      - <span data-ttu-id="e3cf8-189">**包装到所有开放集装箱** – 系统评估分配行是否适合在集装化周期期间创建的任何集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-189">**Pack into all open containers** – The system evaluates whether the allocation line will fit in any container that was created during the containerization cycle.</span></span>
      - <span data-ttu-id="e3cf8-190">**仅包装到当前集装箱** – 系统只评估分配行是否适合最近创建的集装箱。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-190">**Pack into current container only** – The system only evaluates whether the allocation line will fit in the most recently created container.</span></span>

1. <span data-ttu-id="e3cf8-191">若要为集装箱中的包装分配行设置规则，请选择 **混合逻辑分隔符**。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-191">To set up rules for packing allocation lines in containers, select **Mixing Logic Breaks**.</span></span> <span data-ttu-id="e3cf8-192">例如，可以创建将允许工作人员在同一个集装箱内对两个不同物料包装分配行的规则。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-192">For example, you can create a rule that will allow workers to pack allocation lines for two different items in the same container.</span></span> <span data-ttu-id="e3cf8-193">若要定义混合规则，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e3cf8-193">To define a mixing rule, follow these steps:</span></span>

    1. <span data-ttu-id="e3cf8-194">在 **混合逻辑分隔符** 页面中，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-194">In the **Mixing Logic Breaks** page, select **New**.</span></span>
    1. <span data-ttu-id="e3cf8-195">在 **表** 字段中，选择包含要用作混合逻辑分隔符条件的字段的表。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-195">In the **Table** field, select the table that contains the field to use as a criterion for the mixing logic break.</span></span>
    1. <span data-ttu-id="e3cf8-196">在 **字段选择** 字段中，选择要用作混合逻辑分隔符条件的字段。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-196">In the **Field Select** field, select the field to use as a criterion for the mixing logic break.</span></span>
    1. <span data-ttu-id="e3cf8-197">重复这些步骤，直到添加了所有混合逻辑分隔符的条件。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-197">Repeat these steps until you have added all of the criteria for the mixing logic break.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3cf8-198">如果使用混合逻辑，我们建议您在筛选条件查询中按相同字段排序。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-198">If you use mixing logic, we recommend that you sort by the same fields in the filter criteria query.</span></span> <span data-ttu-id="e3cf8-199">这将减少创建的集装箱的数量。</span><span class="sxs-lookup"><span data-stu-id="e3cf8-199">This will reduce the number of containers that are created.</span></span>
