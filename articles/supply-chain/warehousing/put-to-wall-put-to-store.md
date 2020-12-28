---
title: 放置 - 存放
description: 本主题提供有关“放置 - 存放”功能的信息。 通过此功能，您可以根据可配置的条件处理必须将产品合并到预装箱暂存区的情况。 它有助于减少领料时间，因为它允许领料到单个目标牌照，并且可以比群集领料使用更多放置位置。
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423333"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="dd46f-105">放置 - 存放</span><span class="sxs-lookup"><span data-stu-id="dd46f-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd46f-106">通过 *放置 - 存放* 功能，您可以根据可配置的条件处理必须将产品合并到预装箱暂存区的情况。</span><span class="sxs-lookup"><span data-stu-id="dd46f-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="dd46f-107">由于此功能允许领料到单个目标牌照，并且可以比群集领料使用更多放置位置，因此装运到商店或处理小型物料的公司将从减少的领料时间中受益。</span><span class="sxs-lookup"><span data-stu-id="dd46f-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="dd46f-108">此功能的工作流将领料的产品引导到分类位置，以分配到各种类型的集装箱。</span><span class="sxs-lookup"><span data-stu-id="dd46f-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="dd46f-109">通常，每个分类位置包括多个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="dd46f-110">每个分类位置根据业务流程设置的条件分配。</span><span class="sxs-lookup"><span data-stu-id="dd46f-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="dd46f-111">典型条件是最终目标位置、装运或负荷。</span><span class="sxs-lookup"><span data-stu-id="dd46f-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="dd46f-112">产品到达后，根据与订单、目标位置、装运或负荷关联的数量，将其分配到每个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="dd46f-113">集装箱装满或完成后，将根据业务流程将其移至暂存位置或装运位置进行进一步处理。</span><span class="sxs-lookup"><span data-stu-id="dd46f-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="dd46f-114">此仓储功能也会被冠以其他名称，如“电子分拣”和“打开”。</span><span class="sxs-lookup"><span data-stu-id="dd46f-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="dd46f-115">打开出站分类功能</span><span class="sxs-lookup"><span data-stu-id="dd46f-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="dd46f-116">必须先在系统中打开 *出站分类* 功能，然后才能使用 *放置 - 存放* 功能。</span><span class="sxs-lookup"><span data-stu-id="dd46f-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="dd46f-117">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="dd46f-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="dd46f-118">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="dd46f-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dd46f-119">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="dd46f-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dd46f-120">**功能名称**：*出站分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="dd46f-121">*出站分类* 功能可以与 *组织范围内的波次步骤代码* 功能一起使用（如果此功能已打开）。</span><span class="sxs-lookup"><span data-stu-id="dd46f-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="dd46f-122">如果要使用在波次步骤代码中设置的预定义代码，也必须打开此功能。</span><span class="sxs-lookup"><span data-stu-id="dd46f-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="dd46f-123">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="dd46f-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="dd46f-124">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="dd46f-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dd46f-125">**功能名称**：*组织范围内的波次步骤代码*</span><span class="sxs-lookup"><span data-stu-id="dd46f-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="dd46f-126">设置</span><span class="sxs-lookup"><span data-stu-id="dd46f-126">Setup</span></span>

<span data-ttu-id="dd46f-127">在此演示中，使用了标准 Contoso 数据和仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="dd46f-128">还使用了其他一些内容，后面会提到。</span><span class="sxs-lookup"><span data-stu-id="dd46f-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="dd46f-129">库位类型</span><span class="sxs-lookup"><span data-stu-id="dd46f-129">Location type</span></span>

1. <span data-ttu-id="dd46f-130">转到 **仓库管理 \> 设置 \> 仓库 \> 位置类型**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="dd46f-131">在“操作窗格”上，选择 **新建** 创建用于分类的位置类型。</span><span class="sxs-lookup"><span data-stu-id="dd46f-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="dd46f-132">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-132">Set the following values:</span></span>

    - <span data-ttu-id="dd46f-133">**位置类型**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="dd46f-134">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="dd46f-135">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="dd46f-136">仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="dd46f-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="dd46f-137">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="dd46f-138">在 **常规** 选项卡上的 **位置类型** 快速选项卡上，在 **分类位置类型** 字段中，输入 *分类*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="dd46f-139">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="dd46f-140">位置模板</span><span class="sxs-lookup"><span data-stu-id="dd46f-140">Location profile</span></span>

1. <span data-ttu-id="dd46f-141">转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="dd46f-142">在“操作窗格”上，选择 **新建** 为分类位置创建位置模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="dd46f-143">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd46f-144">**位置模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-145">**名称**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="dd46f-146">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd46f-147">**位置格式**：*装箱*</span><span class="sxs-lookup"><span data-stu-id="dd46f-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="dd46f-148">**位置类型**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="dd46f-149">**使用牌照跟踪**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="dd46f-150">**允许混合物料**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="dd46f-151">**允许混合库存状态**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="dd46f-152">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="dd46f-153">位置</span><span class="sxs-lookup"><span data-stu-id="dd46f-153">Locations</span></span>

1. <span data-ttu-id="dd46f-154">转到 **仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="dd46f-155">清除 **生成位置校验位** 复选框。</span><span class="sxs-lookup"><span data-stu-id="dd46f-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="dd46f-156">在“操作窗格”中，选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="dd46f-157">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd46f-158">**位置**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-159">**位置模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="dd46f-160">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="dd46f-161">包装模板</span><span class="sxs-lookup"><span data-stu-id="dd46f-161">Packing profiles</span></span>

1. <span data-ttu-id="dd46f-162">转到 **仓库管理 \> 设置 \> 装箱 \> 装箱模板**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="dd46f-163">在“操作窗格”中，选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="dd46f-164">**装箱模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-165">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-166">**集装箱装箱策略：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="dd46f-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="dd46f-167">**集装箱 ID 模式**：*自动*</span><span class="sxs-lookup"><span data-stu-id="dd46f-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="dd46f-168">**集装箱类型**：*托盘 48X48*</span><span class="sxs-lookup"><span data-stu-id="dd46f-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="dd46f-169">**在集装箱封闭时自动创建集装箱：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="dd46f-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="dd46f-170">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="dd46f-171">波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="dd46f-171">Wave step codes</span></span>

<span data-ttu-id="dd46f-172">如果您打开了 *组织范围内的波次步骤代码* 功能，设置以下代码。</span><span class="sxs-lookup"><span data-stu-id="dd46f-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="dd46f-173">转到 **仓库管理 \> 设置 \> 波次 \> 波次步骤代码**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="dd46f-174">在“操作窗格”中，选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="dd46f-175">**波次步骤代码**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-176">**波次步骤描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-177">**波次步骤类型**：*分类模板*</span><span class="sxs-lookup"><span data-stu-id="dd46f-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="dd46f-178">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="dd46f-179">出站排序模板</span><span class="sxs-lookup"><span data-stu-id="dd46f-179">Outbound sorting template</span></span>

<span data-ttu-id="dd46f-180">分类模板控制是否创建分类位置，使用什么条件以及分类流程的其他属性。</span><span class="sxs-lookup"><span data-stu-id="dd46f-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="dd46f-181">转到 **仓库管理 \> 设置 \> 装箱 \> 出站分类模板**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="dd46f-182">在“操作窗格”中，选择 **新建** 创建一个分类模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="dd46f-183">在新模板的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="dd46f-184">**出站分类模板 ID**：*Wave Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="dd46f-185">**描述**：*波次分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="dd46f-186">**波次模板类型**：*波次需求*</span><span class="sxs-lookup"><span data-stu-id="dd46f-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="dd46f-187">此字段定义分类模板用于的流程。</span><span class="sxs-lookup"><span data-stu-id="dd46f-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="dd46f-188">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-188">The following values are available:</span></span>

        - <span data-ttu-id="dd46f-189">**波次需求** – 此分类模板用于 *放置* 流程。</span><span class="sxs-lookup"><span data-stu-id="dd46f-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="dd46f-190">此模板类型用于绕过装箱工作站，直接在波次外处理库存。</span><span class="sxs-lookup"><span data-stu-id="dd46f-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="dd46f-191">仅当波次模板中包含 **分类** 波次处理方法时，才能使用此类型。</span><span class="sxs-lookup"><span data-stu-id="dd46f-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="dd46f-192">**集装箱** – 此分类模板用于 *装箱后建立托盘* 流程。</span><span class="sxs-lookup"><span data-stu-id="dd46f-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="dd46f-193">此模板类型用于处理在装箱工作站封闭、必须分类到托盘的集装箱。</span><span class="sxs-lookup"><span data-stu-id="dd46f-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="dd46f-194">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd46f-195">**位置**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="dd46f-196">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd46f-197">**分类验证**：*位置扫描*</span><span class="sxs-lookup"><span data-stu-id="dd46f-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="dd46f-198">此字段定义分类期间所需的验证。</span><span class="sxs-lookup"><span data-stu-id="dd46f-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="dd46f-199">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-199">The following values are available:</span></span>

        - <span data-ttu-id="dd46f-200">None</span><span class="sxs-lookup"><span data-stu-id="dd46f-200">None</span></span>
        - <span data-ttu-id="dd46f-201">牌照扫描</span><span class="sxs-lookup"><span data-stu-id="dd46f-201">License plate scan</span></span>
        - <span data-ttu-id="dd46f-202">位置扫描</span><span class="sxs-lookup"><span data-stu-id="dd46f-202">Position scan</span></span>

    - <span data-ttu-id="dd46f-203">**在位置关闭时创建工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="dd46f-204">如果此选项设置为 *是*，在位置关闭时，将创建工作以将库存移至最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="dd46f-205">如果设置为 *否*，在位置关闭时，库存将被立即领取到订单。</span><span class="sxs-lookup"><span data-stu-id="dd46f-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="dd46f-206">**位置分配**：*手动*</span><span class="sxs-lookup"><span data-stu-id="dd46f-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="dd46f-207">此字段定义位置分配的类型。</span><span class="sxs-lookup"><span data-stu-id="dd46f-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="dd46f-208">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-208">The following values are available:</span></span>

        - <span data-ttu-id="dd46f-209">**手动** – 用户必须始终指出库存应分类到的位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="dd46f-210">**自动** – 系统会根据分类模板中断自动将库存引导至某个位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="dd46f-211">**分配分类位置条件**：*只使用空位置*</span><span class="sxs-lookup"><span data-stu-id="dd46f-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="dd46f-212">此字段控制在为需求分配位置时是否考虑分类位置已经存在的库存。</span><span class="sxs-lookup"><span data-stu-id="dd46f-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="dd46f-213">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-213">The following values are available:</span></span>

        - <span data-ttu-id="dd46f-214">**只使用空位置** – 将考虑已经关联了库存的位置</span><span class="sxs-lookup"><span data-stu-id="dd46f-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="dd46f-215">**假定位置为空** – 分配过程中将忽略已在位置上的任何库存。</span><span class="sxs-lookup"><span data-stu-id="dd46f-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="dd46f-216">将使用所有可用位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-216">All available positions will be used.</span></span>

    - <span data-ttu-id="dd46f-217">**波次步骤代码**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="dd46f-218">如果 *组织范围内的波次步骤代码* 功能打开，*分类* 波次步骤代码也必须在波次步骤代码中设置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="dd46f-219">**自动关闭分类位置**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="dd46f-220">如果此选项设置为 *是*，当进入位置的所有工作都完成时，分类位置将自动关闭。</span><span class="sxs-lookup"><span data-stu-id="dd46f-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="dd46f-221">**分类位置数**：*3*</span><span class="sxs-lookup"><span data-stu-id="dd46f-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="dd46f-222">此字段定义系统将创建的最大分类位置数。</span><span class="sxs-lookup"><span data-stu-id="dd46f-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="dd46f-223">**分类位置前缀**：*SP-*</span><span class="sxs-lookup"><span data-stu-id="dd46f-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="dd46f-224">此字段定义系统在位置编号之前分配的前缀。</span><span class="sxs-lookup"><span data-stu-id="dd46f-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="dd46f-225">**自动装箱分类位置**：*是*</span><span class="sxs-lookup"><span data-stu-id="dd46f-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="dd46f-226">如果此选项设置为 *是*，在关闭位置时，该分类位置的库存将装箱至集装箱。</span><span class="sxs-lookup"><span data-stu-id="dd46f-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="dd46f-227">**装箱模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="dd46f-228">此字段定义将分类位置装箱至集装箱时要使用的装箱模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="dd46f-229">在“操作窗格”上，选择 **编辑查询** 指定用于此分类模板的条件。</span><span class="sxs-lookup"><span data-stu-id="dd46f-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="dd46f-230">在查询对话框的 **分类** 选项卡上，选择 **新** 添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="dd46f-231">**表**：*负荷详细信息*</span><span class="sxs-lookup"><span data-stu-id="dd46f-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="dd46f-232">**派生表**：*负荷详细信息*</span><span class="sxs-lookup"><span data-stu-id="dd46f-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="dd46f-233">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="dd46f-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="dd46f-234">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="dd46f-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="dd46f-235">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-235">Select **OK**.</span></span>
1. <span data-ttu-id="dd46f-236">您可能会收到以下消息：“分组将重置，是否继续？”</span><span class="sxs-lookup"><span data-stu-id="dd46f-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="dd46f-237">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-237">Select **Yes**.</span></span>

    <span data-ttu-id="dd46f-238">“操作窗格”上的 **出站分类模板中断** 按钮将变为可用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="dd46f-239">在“操作窗格”上，选择 **出站分类模板中断**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="dd46f-240">选中 **按字段分组** 复选框按装运 ID 分组。</span><span class="sxs-lookup"><span data-stu-id="dd46f-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="dd46f-241">此设置将为在波次中属于集装箱的每个装运创建一个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="dd46f-242">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="dd46f-243">波次处理方法</span><span class="sxs-lookup"><span data-stu-id="dd46f-243">Wave process methods</span></span>

1. <span data-ttu-id="dd46f-244">转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="dd46f-245">在操作窗格上，选择 **重新生成方法**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="dd46f-246">**分类** 方法将添加到可用方法列表中，并为其选择 *装运* 波次模板类型。</span><span class="sxs-lookup"><span data-stu-id="dd46f-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="dd46f-247">波动模板</span><span class="sxs-lookup"><span data-stu-id="dd46f-247">Wave templates</span></span>

<span data-ttu-id="dd46f-248">编辑用于波次需求分类的波次模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="dd46f-249">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="dd46f-250">在 **波次模板类型** 字段中，选择 *装运*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="dd46f-251">选择现有的 **62 装运（默认）** 模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="dd46f-252">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dd46f-253">在 **常规** 快速选项卡上，进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="dd46f-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="dd46f-254">设置 **在发放到仓库时处理波次** 选项为 *否*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="dd46f-255">将 **分配给开放波次** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="dd46f-256">在 **方法** 快速选项卡上，设置 **分类** 方法：</span><span class="sxs-lookup"><span data-stu-id="dd46f-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="dd46f-257">在 **其余方法** 网格中，选择 **分类**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="dd46f-258">选择向右箭头按钮将 **分类** 移到 **选定方法** 网格中。</span><span class="sxs-lookup"><span data-stu-id="dd46f-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="dd46f-259">在 **选定方法** 网格中，选择 **分类**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="dd46f-260">将 **波次步骤代码** 字段设置为 *Sort*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="dd46f-261">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="dd46f-262">移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="dd46f-262">Mobile device menu items</span></span>

1. <span data-ttu-id="dd46f-263">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="dd46f-264">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd46f-265">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd46f-266">**菜单项名称**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-267">**标题**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="dd46f-268">**模式**：*间接*</span><span class="sxs-lookup"><span data-stu-id="dd46f-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="dd46f-269">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="dd46f-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="dd46f-270">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd46f-271">**活动代码**：*Outbound sorting*</span><span class="sxs-lookup"><span data-stu-id="dd46f-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="dd46f-272">**使用流程指南**：*是*（默认值）</span><span class="sxs-lookup"><span data-stu-id="dd46f-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="dd46f-273">**出站分类模板 ID**：*Wave Sort*</span><span class="sxs-lookup"><span data-stu-id="dd46f-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="dd46f-274">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="dd46f-275">移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="dd46f-275">Mobile device menu</span></span>

1. <span data-ttu-id="dd46f-276">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="dd46f-277">在菜单列表中，选择 **出站**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="dd46f-278">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dd46f-279">在 **可用菜单和菜单项** 网格中，找到并选择刚才创建的 **分类** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="dd46f-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="dd46f-280">选择向右箭头按钮，将 **分类** 移至 **菜单结构** 网格中。</span><span class="sxs-lookup"><span data-stu-id="dd46f-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="dd46f-281">这样，就将此菜单项添加到了 **出站** 菜单中。</span><span class="sxs-lookup"><span data-stu-id="dd46f-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="dd46f-282">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="dd46f-283">位置指令</span><span class="sxs-lookup"><span data-stu-id="dd46f-283">Location directives</span></span>

<span data-ttu-id="dd46f-284">您必须创建位置指令来指导分类完成后创建的工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="dd46f-285">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dd46f-286">在 **工作订单类型** 字段中，选择 *分类库存领料*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="dd46f-287">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd46f-288">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd46f-289">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="dd46f-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd46f-290">**名称**：*放到货架门*</span><span class="sxs-lookup"><span data-stu-id="dd46f-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="dd46f-291">在 **位置指令** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd46f-292">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="dd46f-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dd46f-293">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="dd46f-293">**Site:** *6*</span></span>
    - <span data-ttu-id="dd46f-294">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd46f-295">**指令代码：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="dd46f-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="dd46f-296">**多 SKU**：*否*</span><span class="sxs-lookup"><span data-stu-id="dd46f-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="dd46f-297">选择 **保存** 激活 **行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="dd46f-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="dd46f-298">在 **行** 快速选项卡上，选择 **新建**，然后设置以下值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="dd46f-299">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd46f-300">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="dd46f-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dd46f-301">\**起始数量：\*\*\*0*</span><span class="sxs-lookup"><span data-stu-id="dd46f-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="dd46f-302">**目标数量：** *1000000*</span><span class="sxs-lookup"><span data-stu-id="dd46f-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="dd46f-303">选择 **保存** 激活 **货位指令操作** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="dd46f-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="dd46f-304">在 **位置指令操作** 快速选项卡上，选择 **新建**，然后设置以下值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="dd46f-305">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd46f-306">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="dd46f-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dd46f-307">**名称**：*Baydoor*</span><span class="sxs-lookup"><span data-stu-id="dd46f-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="dd46f-308">选择 **保存** 让 **位置指令操作** 快速选项卡上的 **编辑查询** 按钮可用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="dd46f-309">在 **位置指令操作** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="dd46f-310">在查询对话框中的 **范围** 选项卡上，找到 **字段** 字段设置为 *位置* 的行。</span><span class="sxs-lookup"><span data-stu-id="dd46f-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="dd46f-311">将此行的 **条件** 字段设置为 *货架门*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="dd46f-312">选择 **确定** 确认编辑。</span><span class="sxs-lookup"><span data-stu-id="dd46f-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="dd46f-313">工作类</span><span class="sxs-lookup"><span data-stu-id="dd46f-313">Work classes</span></span>

1. <span data-ttu-id="dd46f-314">转到 **仓库管理 \> 设置 \> 工作 \> 工作类**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="dd46f-315">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd46f-316">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd46f-317">**工作类 ID**：*Sorting*</span><span class="sxs-lookup"><span data-stu-id="dd46f-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="dd46f-318">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="dd46f-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="dd46f-319">**工作订单类型**：*分类库存领料*</span><span class="sxs-lookup"><span data-stu-id="dd46f-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="dd46f-320">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="dd46f-321">工作模板</span><span class="sxs-lookup"><span data-stu-id="dd46f-321">Work templates</span></span>

1. <span data-ttu-id="dd46f-322">转到 **仓库管理 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="dd46f-323">在 **工作订单类型** 字段中，选择 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="dd46f-324">在网格中，选择 **62 领料装箱** 工作模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="dd46f-325">在“操作窗格”中选择 **工作标题中断**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="dd46f-326">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dd46f-327">在 **字段名称** 字段设置为 *装运 ID* 的行上，清除 **按此字段分组** 复选框。</span><span class="sxs-lookup"><span data-stu-id="dd46f-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="dd46f-328">选择 **保存**，然后关闭 **工作标题中断** 对话框。</span><span class="sxs-lookup"><span data-stu-id="dd46f-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="dd46f-329">在 **工作订单类型** 字段中，选择 *分类库存领料*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="dd46f-330">选择 **新建** 创建工作模板。</span><span class="sxs-lookup"><span data-stu-id="dd46f-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="dd46f-331">在 **概览** 部分，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="dd46f-332">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="dd46f-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd46f-333">**工作模板**：*分类领料*</span><span class="sxs-lookup"><span data-stu-id="dd46f-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="dd46f-334">**工作模板描述**：*分类领料*</span><span class="sxs-lookup"><span data-stu-id="dd46f-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="dd46f-335">选择 **保存** 让 **工作模板详细信息** 部分可用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="dd46f-336">在 **工作模板详细信息** 部分，您将创建两行。</span><span class="sxs-lookup"><span data-stu-id="dd46f-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="dd46f-337">选择 **新建**，然后为行 1 设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="dd46f-338">**工作类型：** *领料*</span><span class="sxs-lookup"><span data-stu-id="dd46f-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="dd46f-339">**必需：** 选定（= *是*）</span><span class="sxs-lookup"><span data-stu-id="dd46f-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="dd46f-340">**工作类 ID**：*Sorting*</span><span class="sxs-lookup"><span data-stu-id="dd46f-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="dd46f-341">再次选择 **新建**，然后为行 2 设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="dd46f-342">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="dd46f-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dd46f-343">**必需：** 选定（= *是*）</span><span class="sxs-lookup"><span data-stu-id="dd46f-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="dd46f-344">**工作类 ID**：*Sorting*</span><span class="sxs-lookup"><span data-stu-id="dd46f-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="dd46f-345">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="dd46f-346">示例场景</span><span class="sxs-lookup"><span data-stu-id="dd46f-346">Example scenario</span></span>

<span data-ttu-id="dd46f-347">此方案模拟一种情况：仓库将小型物料存储在位置内，必须在装运前将它们装箱到箱中，但装箱工作站功能实际上并不适用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="dd46f-348">工作人员同时为多个客户和不同地址领取订单，以提高领料速度。</span><span class="sxs-lookup"><span data-stu-id="dd46f-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="dd46f-349">领料完成后，工作人员到达分类位置，在这里可以根据所需条件将领取的物料分类到正确的箱中。</span><span class="sxs-lookup"><span data-stu-id="dd46f-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="dd46f-350">在此示例中，装运 ID 将用于确定正确的箱子，因为每个装运都有不同的地址。</span><span class="sxs-lookup"><span data-stu-id="dd46f-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="dd46f-351">将所有负荷的物料装箱并按装运分类后，箱子将被移到暂存区，最终装载到卡车上。</span><span class="sxs-lookup"><span data-stu-id="dd46f-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="dd46f-352">在开始方案之前，请确保您已为仓库正确设置了所有标准仓库功能。</span><span class="sxs-lookup"><span data-stu-id="dd46f-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="dd46f-353">标准 Contoso 仓库 *62* 用于此目的。</span><span class="sxs-lookup"><span data-stu-id="dd46f-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="dd46f-354">除了设置中介绍的部分外，标准配置未更改。</span><span class="sxs-lookup"><span data-stu-id="dd46f-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="dd46f-355">创建需求</span><span class="sxs-lookup"><span data-stu-id="dd46f-355">Create demand</span></span>

<span data-ttu-id="dd46f-356">必须先创建一些需求，才能够演示功能。</span><span class="sxs-lookup"><span data-stu-id="dd46f-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="dd46f-357">对于此方案，您将为三个不同的客户创建三个销售订单，来模拟不同的交货地址。</span><span class="sxs-lookup"><span data-stu-id="dd46f-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="dd46f-358">这样，您将创建三个单独的装运。</span><span class="sxs-lookup"><span data-stu-id="dd46f-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="dd46f-359">在创建销售订单和装运之前，请确保领料位置有订单中所有物料的足够库存。</span><span class="sxs-lookup"><span data-stu-id="dd46f-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="dd46f-360">查看位置指令设置，确认用于销售订单领料的领料位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="dd46f-361">如果必须调整库存，可创建手动移动，使用补货，或使用其他任何流。</span><span class="sxs-lookup"><span data-stu-id="dd46f-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="dd46f-362">然后预留库存。</span><span class="sxs-lookup"><span data-stu-id="dd46f-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="dd46f-363">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dd46f-364">选择 **新建** 为订单 1 创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="dd46f-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="dd46f-365">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd46f-366">**客户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="dd46f-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="dd46f-367">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="dd46f-368">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-368">Select **OK**.</span></span>
1. <span data-ttu-id="dd46f-369">将向 **销售订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="dd46f-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd46f-370">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-370">Set the following values:</span></span>

    - <span data-ttu-id="dd46f-371">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="dd46f-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dd46f-372">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="dd46f-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="dd46f-373">选择 **添加行** 添加第二个行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="dd46f-374">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="dd46f-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="dd46f-375">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="dd46f-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="dd46f-376">对订单上的每个销售行重复以下步骤来为其预留库存：</span><span class="sxs-lookup"><span data-stu-id="dd46f-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="dd46f-377">在 **销售订单行** 快速选项卡上的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="dd46f-378">在 **预留** 页上，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="dd46f-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="dd46f-379">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-379">Select **Save**.</span></span>

1. <span data-ttu-id="dd46f-380">选择 **新建** 为订单 2 创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="dd46f-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="dd46f-381">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd46f-382">**客户**：*US-004*</span><span class="sxs-lookup"><span data-stu-id="dd46f-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="dd46f-383">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="dd46f-384">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-384">Select **OK**.</span></span>
1. <span data-ttu-id="dd46f-385">将向 **销售订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="dd46f-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd46f-386">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-386">Set the following values:</span></span>

    - <span data-ttu-id="dd46f-387">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="dd46f-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dd46f-388">**数量：** *7*</span><span class="sxs-lookup"><span data-stu-id="dd46f-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="dd46f-389">选择 **添加行** 添加第二个行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="dd46f-390">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="dd46f-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="dd46f-391">**数量：** *3*</span><span class="sxs-lookup"><span data-stu-id="dd46f-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="dd46f-392">对订单上的每个销售行重复以下步骤来为其预留库存：</span><span class="sxs-lookup"><span data-stu-id="dd46f-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="dd46f-393">在 **销售订单行** 快速选项卡上的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="dd46f-394">在 **预留** 页上，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="dd46f-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="dd46f-395">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-395">Select **Save**.</span></span>

1. <span data-ttu-id="dd46f-396">选择 **新建** 为订单 3 创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="dd46f-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="dd46f-397">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd46f-398">**客户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="dd46f-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="dd46f-399">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="dd46f-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="dd46f-400">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-400">Select **OK**.</span></span>
1. <span data-ttu-id="dd46f-401">将向 **销售订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="dd46f-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd46f-402">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="dd46f-402">Set the following values:</span></span>

    - <span data-ttu-id="dd46f-403">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="dd46f-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dd46f-404">**数量：** *8*</span><span class="sxs-lookup"><span data-stu-id="dd46f-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="dd46f-405">按照以下步骤为销售行预留库存：</span><span class="sxs-lookup"><span data-stu-id="dd46f-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="dd46f-406">在 **销售订单行** 快速选项卡上的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="dd46f-407">在 **预留** 页上，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="dd46f-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="dd46f-408">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-408">Select **Save**.</span></span>

<span data-ttu-id="dd46f-409">完成以下过程将每个销售订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="dd46f-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="dd46f-410">将创建三个不同的装运。</span><span class="sxs-lookup"><span data-stu-id="dd46f-410">Three different shipments will be created.</span></span> <span data-ttu-id="dd46f-411">然后，将所有三个装运添加到一个新波次中。</span><span class="sxs-lookup"><span data-stu-id="dd46f-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="dd46f-412">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dd46f-413">在网格中，选择您创建的第一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="dd46f-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="dd46f-414">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="dd46f-415">您将收到显示创建的波次 ID 和装运 ID 的信息性消息。</span><span class="sxs-lookup"><span data-stu-id="dd46f-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="dd46f-416">重复上述步骤，将销售订单 2 和 3 下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="dd46f-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="dd46f-417">请注意，您收到的信息性消息将指示已将装运添加到下达销售订单 1 时创建的波次。</span><span class="sxs-lookup"><span data-stu-id="dd46f-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="dd46f-418">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="dd46f-419">选择从销售订单下达创建的波次 ID 来打开 **波次** 页。</span><span class="sxs-lookup"><span data-stu-id="dd46f-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="dd46f-420">此页面将显示波次详细信息。</span><span class="sxs-lookup"><span data-stu-id="dd46f-420">This page shows the wave details.</span></span> <span data-ttu-id="dd46f-421">**波次行** 快速选项卡显示已创建的装运。</span><span class="sxs-lookup"><span data-stu-id="dd46f-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="dd46f-422">现在，您必须创建工作以将物料从领料位置带入分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="dd46f-423">在“操作窗格”上，选择 **流程**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="dd46f-424">在波次处理期间，分类方法将使用分类模板将库存分配到分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="dd46f-425">波次处理完成后，您会收到一条信息性消息，指出该波次已过帐并已创建工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="dd46f-426">在“操作窗格”上的 **波次** 选项卡上，在 **相关信息** 组中，选择 **工作** 查看创建的工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="dd46f-427">记录工作 ID。</span><span class="sxs-lookup"><span data-stu-id="dd46f-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="dd46f-428">转到 **仓库管理 \> 装箱和集装化 \> 出站分类位置分配**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="dd46f-429">在左列中，您可以查看为每个装运创建的出站分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="dd46f-430">在 **分类位置条件** 快速选项卡上，您可以查看该位置的装运 ID。</span><span class="sxs-lookup"><span data-stu-id="dd46f-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="dd46f-431">已创建一个工作 ID，以将库存从领料位置带入分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="dd46f-432">要完成工作，您需要在波次处理期间创建的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="dd46f-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="dd46f-433">销售订单领料到分类位置</span><span class="sxs-lookup"><span data-stu-id="dd46f-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="dd46f-434">以仓库 *62* 中的工作人员身份登录移动应用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="dd46f-435">在主菜单上，选择 **出站**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd46f-436">在 **出站** 菜单上，选择 **销售领料**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="dd46f-437">选择 **ID** 字段，然后输入波次处理中的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="dd46f-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="dd46f-438">确认您的输入。</span><span class="sxs-lookup"><span data-stu-id="dd46f-438">Confirm your entry.</span></span>

    <span data-ttu-id="dd46f-439">接下来，将提示您输入目标牌照 (LP)。</span><span class="sxs-lookup"><span data-stu-id="dd46f-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="dd46f-440">请注意，必须领取销售订单 1 的行 1，并将其添加到目标牌照。</span><span class="sxs-lookup"><span data-stu-id="dd46f-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="dd46f-441">物料编号、数量、物料描述和领料位置将显示。</span><span class="sxs-lookup"><span data-stu-id="dd46f-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="dd46f-442">在 **目标牌照** 字段中，输入牌照编号。</span><span class="sxs-lookup"><span data-stu-id="dd46f-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="dd46f-443">您要将从已处理的波次创建的所有行领取到同一目标牌照。</span><span class="sxs-lookup"><span data-stu-id="dd46f-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="dd46f-444">确认您的输入。</span><span class="sxs-lookup"><span data-stu-id="dd46f-444">Confirm your entry.</span></span>

    <span data-ttu-id="dd46f-445">现在，移动应用会显示一系列 **领料** 页面，这些页面将向您指示领料位置以及必须领取的物料和数量。</span><span class="sxs-lookup"><span data-stu-id="dd46f-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="dd46f-446">将领取的物料添加到牌照后，您将确认领料工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="dd46f-447">最后一页是将领取的物料放入分类位置的工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="dd46f-448">确认第一个领料工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="dd46f-449">下一个领料工作将显示。</span><span class="sxs-lookup"><span data-stu-id="dd46f-449">The next pick work is shown.</span></span> <span data-ttu-id="dd46f-450">确认领料。</span><span class="sxs-lookup"><span data-stu-id="dd46f-450">Confirm the pick.</span></span>
1. <span data-ttu-id="dd46f-451">继续确认其余领料工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="dd46f-452">最后一步是完成放置工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-452">The last step is to complete the put work.</span></span> <span data-ttu-id="dd46f-453">确认储存到分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="dd46f-454">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="dd46f-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="dd46f-455">在移动应用上退出 **销售领料**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="dd46f-456">分类/放置</span><span class="sxs-lookup"><span data-stu-id="dd46f-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="dd46f-457">现在，所有库存都已放入分类位置，必须将其分类到正确的分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="dd46f-458">登录到移动应用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="dd46f-459">在主菜单上，选择 **出站**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd46f-460">在 **出站** 菜单上，选择 **分类** 开始对物料分类。</span><span class="sxs-lookup"><span data-stu-id="dd46f-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="dd46f-461">在 **牌照/集装箱** 字段中，输入已领取销售订单工作的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="dd46f-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="dd46f-462">确认您的输入。</span><span class="sxs-lookup"><span data-stu-id="dd46f-462">Confirm your entry.</span></span>
1. <span data-ttu-id="dd46f-463">输入要首先分类的物料编号。</span><span class="sxs-lookup"><span data-stu-id="dd46f-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="dd46f-464">系统将确定应显示的第一个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="dd46f-465">确认分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="dd46f-466">将提示您将牌照分配到分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="dd46f-467">选择 **牌照** 字段，输入牌照编号，然后确认输入。</span><span class="sxs-lookup"><span data-stu-id="dd46f-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="dd46f-468">由于分类位置与装运 ID 相关，因此您要将领取的物料分类到特定于出站装运和销售订单的牌照。</span><span class="sxs-lookup"><span data-stu-id="dd46f-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="dd46f-469">下一页显示物料 ID、数量、分类位置 ID 以及“从”（领料）和“到”（分类）牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="dd46f-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="dd46f-470">此页面上的信息将指示您将指定物料和数量从领料牌照分类到分类牌照。</span><span class="sxs-lookup"><span data-stu-id="dd46f-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="dd46f-471">确认分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="dd46f-472">在第一个分类位置对物料进行分类。</span><span class="sxs-lookup"><span data-stu-id="dd46f-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="dd46f-473">完成后，系统会将您定向到下一个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="dd46f-474">对工作订单上所有已领料的行重复此流程。</span><span class="sxs-lookup"><span data-stu-id="dd46f-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="dd46f-475">当有多个具有相同物料编号的领料行时，也应使用此流程。</span><span class="sxs-lookup"><span data-stu-id="dd46f-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="dd46f-476">当您对所有物料重复此流程时，系统会评估下一个扫描物料（工作行）的条件，并确定应将其放置在哪个分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="dd46f-477">系统会自动指示您将物料放置到正确的分类位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="dd46f-478">根据确认设置，您还可能被指示通过输入位置编号或牌照 ID 来确认此操作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd46f-479">如果打开了自动分类，手动覆盖将不可用。</span><span class="sxs-lookup"><span data-stu-id="dd46f-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="dd46f-480">完成后，在 Microsoft Dynamics 365 Supply Chain Management 中，打开 **出站分类位置分配** 页面查看位置的状态。</span><span class="sxs-lookup"><span data-stu-id="dd46f-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="dd46f-481">如果位置已自动关闭，选择 **显示已关闭** 显示关闭的位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="dd46f-482">请注意，将显示分类位置事务。</span><span class="sxs-lookup"><span data-stu-id="dd46f-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="dd46f-483">通过此位置处理的物料和数量将显示。</span><span class="sxs-lookup"><span data-stu-id="dd46f-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="dd46f-484">设置出站分类模板时，您将 **自动关闭分类位置** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="dd46f-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="dd46f-485">因此，在最后一个预期库存被放置到此位置后，此位置将自动关闭。</span><span class="sxs-lookup"><span data-stu-id="dd46f-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="dd46f-486">分类位置处于 **关闭** 状态，工作已创建以将分类的库存移至 *货架门* 位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="dd46f-487">完成已分类库存的领料工作，以将库存移至装运位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="dd46f-488">库存准备就绪后，对其进行装运确认。</span><span class="sxs-lookup"><span data-stu-id="dd46f-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="dd46f-489">为了正确处理已分类库存的领料工作，应在移动和装载流程中使用具有将 **工作订单类型** 字段设置为 *分类库存领料* 的工作类 ID 的移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="dd46f-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="dd46f-490">手动关闭位置（可选）</span><span class="sxs-lookup"><span data-stu-id="dd46f-490">Manually close a position (optional)</span></span>

<span data-ttu-id="dd46f-491">如果应该手动关闭分类位置，必须将出站分类模板的 **自动关闭分类位置** 选项设置为 *否*，并且必须先进行关闭，然后才能将库存移至货架门区域。</span><span class="sxs-lookup"><span data-stu-id="dd46f-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="dd46f-492">可以通过多种方式关闭位置：</span><span class="sxs-lookup"><span data-stu-id="dd46f-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="dd46f-493">通过仓库应用：</span><span class="sxs-lookup"><span data-stu-id="dd46f-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="dd46f-494">用户可以扫描已经在位置上的物料之一，然后选择 **关闭** 来关闭位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="dd46f-495">如果用户扫描已经分类的集装箱，将显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="dd46f-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="dd46f-496">不过，用户仍然可以继续关闭位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="dd46f-497">从 Microsoft Dynamics 365 Supply Chain Management **出站分类位置分配** 页面：</span><span class="sxs-lookup"><span data-stu-id="dd46f-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="dd46f-498">用户可以选择出站分类位置记录，然后在“操作窗格”上选择 **关闭位置**。</span><span class="sxs-lookup"><span data-stu-id="dd46f-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="dd46f-499">提示</span><span class="sxs-lookup"><span data-stu-id="dd46f-499">Tips</span></span>

- <span data-ttu-id="dd46f-500">将物料分配到一个位置后，它们无法在位置之间移动。</span><span class="sxs-lookup"><span data-stu-id="dd46f-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="dd46f-501">系统将评估每个物料应有多少移至特定位置。</span><span class="sxs-lookup"><span data-stu-id="dd46f-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="dd46f-502">分类模板可以配置为在关闭位置时自动创建集装箱。</span><span class="sxs-lookup"><span data-stu-id="dd46f-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="dd46f-503">此方法将创建基于指定装箱模板的标准集装箱 ID 结构。</span><span class="sxs-lookup"><span data-stu-id="dd46f-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd46f-504">从分类位置创建移动工作后，不能取消工作。</span><span class="sxs-lookup"><span data-stu-id="dd46f-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="dd46f-505">否则，该位置及其中的集装箱将从系统中删除，无法进一步处理。</span><span class="sxs-lookup"><span data-stu-id="dd46f-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="dd46f-506">库存也将被删除。</span><span class="sxs-lookup"><span data-stu-id="dd46f-506">The inventory will also be removed.</span></span>
