---
title: 仓库时隙
description: 文主题提供有关仓库时隙的信息。 仓库时隙用于按物料和度量单位合并状态为“订购”、“预留”或“下达”的订单中的需求。 其可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料货位。
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993745"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="b2c98-105">仓库时隙</span><span class="sxs-lookup"><span data-stu-id="b2c98-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2c98-106">有多个仓库时隙功能可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料位置。</span><span class="sxs-lookup"><span data-stu-id="b2c98-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="b2c98-107">*仓库时隙功能* 用于按物料和度量单位合并状态为 *已订购*、*已预留* 或 *已下达* 的订单中的需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="b2c98-108">然后可以根据数量、单位、物理维度、固定货位等将生成的需求应用于将用于领料的货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="b2c98-109">建立时隙计划之后，可以创建补货工作以将相应数量的库存运到各货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="b2c98-110">*转移单的仓库时隙* 功能让仓库经理可以根据尚未下达到仓库的转移单的需求为领料位置补货。</span><span class="sxs-lookup"><span data-stu-id="b2c98-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="b2c98-111">它确保领料位置在转移单下达到仓库后会包括转移单所需的所有物料。</span><span class="sxs-lookup"><span data-stu-id="b2c98-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="b2c98-112">此功能还需要您打开 *仓库时隙功能*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="b2c98-113">*仓库时隙分配增强* 功能为 *仓库时隙功能* 使用的模板行添加了一个选项。</span><span class="sxs-lookup"><span data-stu-id="b2c98-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="b2c98-114">此选项让系统能够考虑目标位置现有的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="b2c98-115">因此，可以为时隙生成更少的补货。</span><span class="sxs-lookup"><span data-stu-id="b2c98-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="b2c98-116">*仓库时隙分配增强* 功能还需要您打开 *仓库时隙功能*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="b2c98-117">可以有选择地将它与 *转移单的仓库时隙* 功能一起使用。</span><span class="sxs-lookup"><span data-stu-id="b2c98-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="b2c98-118">开启仓库时隙功能</span><span class="sxs-lookup"><span data-stu-id="b2c98-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="b2c98-119">这些功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b2c98-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="b2c98-120">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查这些功能的状态，并在需要这些功能时将其开启。</span><span class="sxs-lookup"><span data-stu-id="b2c98-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="b2c98-121">根据需要开启以下功能：</span><span class="sxs-lookup"><span data-stu-id="b2c98-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="b2c98-122">仓库开槽功能</span><span class="sxs-lookup"><span data-stu-id="b2c98-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="b2c98-123">转移单的仓库时隙</span><span class="sxs-lookup"><span data-stu-id="b2c98-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b2c98-124">*仓库时隙功能* 必须先于此功能打开。</span><span class="sxs-lookup"><span data-stu-id="b2c98-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="b2c98-125">仓库时隙分配增强</span><span class="sxs-lookup"><span data-stu-id="b2c98-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b2c98-126">*仓库时隙功能* 必须先于此功能打开。</span><span class="sxs-lookup"><span data-stu-id="b2c98-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="b2c98-127">设置仓库时隙功能</span><span class="sxs-lookup"><span data-stu-id="b2c98-127">Set up warehouse slotting</span></span>

<span data-ttu-id="b2c98-128">若要使用仓库时隙功能，必须在系统中设置以下元素：</span><span class="sxs-lookup"><span data-stu-id="b2c98-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="b2c98-129">时隙度量单位层</span><span class="sxs-lookup"><span data-stu-id="b2c98-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="b2c98-130">指令代码</span><span class="sxs-lookup"><span data-stu-id="b2c98-130">Directive codes</span></span>
- <span data-ttu-id="b2c98-131">时隙模板</span><span class="sxs-lookup"><span data-stu-id="b2c98-131">Slotting templates</span></span>
- <span data-ttu-id="b2c98-132">位置指令</span><span class="sxs-lookup"><span data-stu-id="b2c98-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="b2c98-133">为时隙创建度量单位层</span><span class="sxs-lookup"><span data-stu-id="b2c98-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="b2c98-134">可通过度量单位层将多个度量单位组合到一起来达到时隙目的。</span><span class="sxs-lookup"><span data-stu-id="b2c98-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="b2c98-135">例如，如果多个尺寸的箱子全部从同一个箱子领取区领取，则可以为所有这些尺寸创建一个层。</span><span class="sxs-lookup"><span data-stu-id="b2c98-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="b2c98-136">**必须为应该属于层的每个度量单位创建一行。**</span><span class="sxs-lookup"><span data-stu-id="b2c98-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="b2c98-137">转到 **仓库管理 \> 设置 \> 补货 \> 时隙度量单位层**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="b2c98-138">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-138">Select **New**.</span></span>
1. <span data-ttu-id="b2c98-139">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="b2c98-140">**度量单位层**：*EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="b2c98-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="b2c98-141">**说明**：*每个箱托盘*</span><span class="sxs-lookup"><span data-stu-id="b2c98-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="b2c98-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-142">Select **Save**.</span></span>
1. <span data-ttu-id="b2c98-143">在 **度量单位** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2c98-144">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-145">**单位**：*箱*</span><span class="sxs-lookup"><span data-stu-id="b2c98-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="b2c98-146">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2c98-147">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="b2c98-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2c98-148">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="b2c98-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2c98-149">选择 **新建** 向网格添加第二行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="b2c98-150">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-151">**单位：** *ea*</span><span class="sxs-lookup"><span data-stu-id="b2c98-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="b2c98-152">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2c98-153">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="b2c98-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2c98-154">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="b2c98-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2c98-155">选择 **新建** 向网格添加第三行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="b2c98-156">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-157">**单位**：*PL*</span><span class="sxs-lookup"><span data-stu-id="b2c98-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="b2c98-158">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2c98-159">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="b2c98-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2c98-160">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="b2c98-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2c98-161">选择 **保存** 以保存层。</span><span class="sxs-lookup"><span data-stu-id="b2c98-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="b2c98-162">为时隙创建指令代码</span><span class="sxs-lookup"><span data-stu-id="b2c98-162">Create a directive code for slotting</span></span>

<span data-ttu-id="b2c98-163">必须选择应与模板关联的指令代码。</span><span class="sxs-lookup"><span data-stu-id="b2c98-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="b2c98-164">转到 **库存管理 \> 设置 \> 指令代码**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b2c98-165">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2c98-166">在 **指令代码** 字段中，输入 *时隙*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="b2c98-167">在 **指令说明** 字段中，输入 *时隙*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="b2c98-168">设置时隙模板</span><span class="sxs-lookup"><span data-stu-id="b2c98-168">Set up slotting templates</span></span>

<span data-ttu-id="b2c98-169">各时隙模板控制如何将库存分配给特定仓库的货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="b2c98-170">每个时隙规范在每个模板中必须有一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="b2c98-171">可使用此部分中的过程设置时隙模板。</span><span class="sxs-lookup"><span data-stu-id="b2c98-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="b2c98-172">转到 **仓库管理 \> 设置 \> 补货 \> 时隙模板**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="b2c98-173">选择 **新建** 以创建模板。</span><span class="sxs-lookup"><span data-stu-id="b2c98-173">Select **New** to create a template.</span></span>

<span data-ttu-id="b2c98-174">接下来，必须按照下面子部分中的说明设置模板标题、时隙规范和货位指令。</span><span class="sxs-lookup"><span data-stu-id="b2c98-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="b2c98-175">转移单的时隙设置类似于销售订单的时隙设置，但是 **需求类型** 字段设置为 *转移单* 而不是 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="b2c98-176">设置销售订单时隙模板的标题</span><span class="sxs-lookup"><span data-stu-id="b2c98-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="b2c98-177">在模板的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="b2c98-178">**时隙模板：**_61_</span><span class="sxs-lookup"><span data-stu-id="b2c98-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="b2c98-179">**说明：**_61_</span><span class="sxs-lookup"><span data-stu-id="b2c98-179">**Description:** _61_</span></span>
    - <span data-ttu-id="b2c98-180">**需求类型**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="b2c98-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="b2c98-181">目前，*销售订单* 和 *转移单* 是唯一受支持的需求类型。</span><span class="sxs-lookup"><span data-stu-id="b2c98-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="b2c98-182">仅当 *转移单的仓库时隙* 功能打开时，才可以选择 *转移单*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="b2c98-183">**需求策略：**_订购_</span><span class="sxs-lookup"><span data-stu-id="b2c98-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="b2c98-184">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2c98-185">**订购** – 应该将销售订单中的所有订购数量视为需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="b2c98-186">**预留** – 仅应将预留的销售订单行数量（订购的实物）视为需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="b2c98-187">**已下达** – 已下达数量应视为需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="b2c98-188">**仓库**：_61_</span><span class="sxs-lookup"><span data-stu-id="b2c98-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="b2c98-189">**允许波次需求使用未预留数量：**_是_</span><span class="sxs-lookup"><span data-stu-id="b2c98-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="b2c98-190">还可以指定查询以缩小评估的需求范围。</span><span class="sxs-lookup"><span data-stu-id="b2c98-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="b2c98-191">为每个模板设置时隙规范</span><span class="sxs-lookup"><span data-stu-id="b2c98-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="b2c98-192">对于创建的每个销售订单模板，执行以下步骤为每个时隙规范添加一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="b2c98-193">在 **时隙模板详细信息** 快速选项卡上，选择 **新建** 创建一个模板行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="b2c98-194">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-195">**序列：** _1_</span><span class="sxs-lookup"><span data-stu-id="b2c98-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="b2c98-196">**说明：**_固定货位_</span><span class="sxs-lookup"><span data-stu-id="b2c98-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="b2c98-197">**最小数量：**_1_</span><span class="sxs-lookup"><span data-stu-id="b2c98-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="b2c98-198">此字段定义行需要的最小需求数量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="b2c98-199">**最大数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="b2c98-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="b2c98-200">此字段定义行的最大有效需求数量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="b2c98-201">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="b2c98-202">此字段定义最小数量和最大数量引用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="b2c98-203">**度量单位层：**_EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="b2c98-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="b2c98-204">此字段定义行的有效需求度量单位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="b2c98-205">（有关详细信息，请参阅本主题前面的[为时隙设置度量单位层](#unit-tiers)部分。）</span><span class="sxs-lookup"><span data-stu-id="b2c98-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="b2c98-206">**分配时隙条件：**_考虑数量_</span><span class="sxs-lookup"><span data-stu-id="b2c98-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="b2c98-207">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2c98-208">**假设为空** – 该系统应假设领料区中的所有货位均为空，并且不应检查这些货位是否有库存。</span><span class="sxs-lookup"><span data-stu-id="b2c98-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="b2c98-209">**考虑数量** – 系统应检查领料区中的货位是否有库存，并且应该跳过所有非空货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="b2c98-210">**考虑现有量** – 系统应检查任何目标位置是否在需求行上包含物料的未预留数量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="b2c98-211">如果数量大到足以满足需求行的至少一个单位，生成的时隙计划记录将减少可用数量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="b2c98-212">例如，如果需求为 10 箱，一箱是现有量，那么找到的需求将为 9 箱。</span><span class="sxs-lookup"><span data-stu-id="b2c98-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="b2c98-213">如果需求为 10 箱，现有量是各一箱，那么找到的需求将为 10 箱。</span><span class="sxs-lookup"><span data-stu-id="b2c98-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="b2c98-214">仅在启用 *仓库时隙分配增强* 打开时，此值才可用。</span><span class="sxs-lookup"><span data-stu-id="b2c98-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="b2c98-215">**指令代码**：_时隙_</span><span class="sxs-lookup"><span data-stu-id="b2c98-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="b2c98-216">此字段定义货位指令，用于查找补货工作的领料货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="b2c98-217">**溢出货位：** 将此字段保持为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="b2c98-218">此字段定义如果在处理行时找不到货位，应将库存放入的货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="b2c98-219">**允许放弃：**_是_</span><span class="sxs-lookup"><span data-stu-id="b2c98-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="b2c98-220">如果此选项设置为 *是*，并且不能为任何需求划分时隙，将创建移动工作把库存移出有库存，但未划分时隙的货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="b2c98-221">然后再次运行模板。</span><span class="sxs-lookup"><span data-stu-id="b2c98-221">The template is then run again.</span></span> <span data-ttu-id="b2c98-222">这次将忽略货位中的库存。</span><span class="sxs-lookup"><span data-stu-id="b2c98-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="b2c98-223">如果 **分配时隙条件** 字段设置为 _考虑数量_，此功能效果最好。</span><span class="sxs-lookup"><span data-stu-id="b2c98-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="b2c98-224">**固定货位用法：**_仅限产品的固定货位_</span><span class="sxs-lookup"><span data-stu-id="b2c98-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="b2c98-225">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2c98-226">**固定货位和非固定货位** – 不应将系统限制为只能使用固定货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="b2c98-227">**仅限产品的固定货位** – 系统应该将货位的时隙划分给仅限产品的固定货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="b2c98-228">**仅限产品变型的固定货位** – 系统应该将货位的时隙划分给仅限产品变型的固定货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="b2c98-229">如果时隙模板包含至少一行，其中 **分配时隙条件** 字段设置为 *考虑现有量*，模板中的任何一行都不再允许减少。</span><span class="sxs-lookup"><span data-stu-id="b2c98-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="b2c98-230">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-230">Select **Save**.</span></span>
1. <span data-ttu-id="b2c98-231">选择 **新建** 创建第二个模板行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="b2c98-232">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-233">**序列：** _2_</span><span class="sxs-lookup"><span data-stu-id="b2c98-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="b2c98-234">**说明：**_其他_</span><span class="sxs-lookup"><span data-stu-id="b2c98-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="b2c98-235">**最小数量：**_1_</span><span class="sxs-lookup"><span data-stu-id="b2c98-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="b2c98-236">**最大数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="b2c98-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="b2c98-237">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2c98-238">**度量单位层：**_EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="b2c98-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="b2c98-239">**分配时隙条件：**_考虑数量_</span><span class="sxs-lookup"><span data-stu-id="b2c98-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="b2c98-240">**指令代码：**_时隙_</span><span class="sxs-lookup"><span data-stu-id="b2c98-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="b2c98-241">**溢出货位：** 将此字段保持为空。</span><span class="sxs-lookup"><span data-stu-id="b2c98-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2c98-242">**允许放弃：**_是_</span><span class="sxs-lookup"><span data-stu-id="b2c98-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="b2c98-243">**使用固定货位：**_固定货位和非固定货位_</span><span class="sxs-lookup"><span data-stu-id="b2c98-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="b2c98-244">在查询第二个行时，现在指定用于确定可以将该行的需求时隙划分给哪些货位。</span><span class="sxs-lookup"><span data-stu-id="b2c98-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="b2c98-245">选择其中的 **序列** 字段设置为 *2* 的行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="b2c98-246">选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="b2c98-247">在 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2c98-248">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-249">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="b2c98-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b2c98-250">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="b2c98-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b2c98-251">\**字段：\*\*\*位置模板 ID*</span><span class="sxs-lookup"><span data-stu-id="b2c98-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="b2c98-252">**条件**：*Pick-06*（选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Pick-06* - *领料点 6*。）</span><span class="sxs-lookup"><span data-stu-id="b2c98-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="b2c98-253">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="b2c98-254">设置货位指令</span><span class="sxs-lookup"><span data-stu-id="b2c98-254">Set up location directives</span></span>

<span data-ttu-id="b2c98-255">必须设置至少一个货位指令来支持时隙领料。</span><span class="sxs-lookup"><span data-stu-id="b2c98-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="b2c98-256">请按照此部分中的过程为时隙领料设置一个新的 *补货货位指令*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="b2c98-257">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b2c98-258">在左窗格的 **工作订单类型** 字段中，选择 *补货*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="b2c98-259">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2c98-260">在新货位指令的标题中 **名称** 字段内，输入 *61 时隙领料*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="b2c98-261">在 **序列号** 字段中，接受默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="b2c98-262">配置“货位指令”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="b2c98-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="b2c98-263">在 **货位指令** 快速选项卡上，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="b2c98-264">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b2c98-265">**工作类型：**_领料_</span><span class="sxs-lookup"><span data-stu-id="b2c98-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="b2c98-266">**站点**：_6_</span><span class="sxs-lookup"><span data-stu-id="b2c98-266">**Site:** _6_</span></span>
    - <span data-ttu-id="b2c98-267">**仓库**：_61_</span><span class="sxs-lookup"><span data-stu-id="b2c98-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="b2c98-268">**指令代码**：_时隙_</span><span class="sxs-lookup"><span data-stu-id="b2c98-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="b2c98-269">选择 **保存** 激活 **行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2c98-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="b2c98-270">配置“行”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="b2c98-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="b2c98-271">在 **行** 快速选项卡上，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="b2c98-272">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="b2c98-273">**起始数量：**_0_</span><span class="sxs-lookup"><span data-stu-id="b2c98-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="b2c98-274">**目标数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="b2c98-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="b2c98-275">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="b2c98-276">选择 **保存** 激活 **货位指令操作** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2c98-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="b2c98-277">配置“货位指令操作”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="b2c98-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="b2c98-278">在 **货位指令操作** 快速选项卡上，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="b2c98-279">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-279">On the new line, set the following values.</span></span> <span data-ttu-id="b2c98-280">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b2c98-281">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b2c98-282">**名称**：_Bulk_</span><span class="sxs-lookup"><span data-stu-id="b2c98-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="b2c98-283">**策略**：_无_</span><span class="sxs-lookup"><span data-stu-id="b2c98-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="b2c98-284">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="b2c98-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="b2c98-285">选择 **保存** 激活 **编辑查询** 按钮。</span><span class="sxs-lookup"><span data-stu-id="b2c98-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="b2c98-286">编辑查询</span><span class="sxs-lookup"><span data-stu-id="b2c98-286">Edit the query</span></span>

1. <span data-ttu-id="b2c98-287">在 **位置指令操作** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b2c98-288">在 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2c98-289">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-290">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="b2c98-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b2c98-291">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="b2c98-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b2c98-292">**字段：** *区域 ID*</span><span class="sxs-lookup"><span data-stu-id="b2c98-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="b2c98-293">**条件**：*Bulk*（选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Bulk*。）</span><span class="sxs-lookup"><span data-stu-id="b2c98-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="b2c98-294">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b2c98-295">应用场景</span><span class="sxs-lookup"><span data-stu-id="b2c98-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="b2c98-296">设置场景</span><span class="sxs-lookup"><span data-stu-id="b2c98-296">Set up the scenario</span></span>

<span data-ttu-id="b2c98-297">对于此场景，请使用内置示例数据，然后创建本部分中介绍的记录。</span><span class="sxs-lookup"><span data-stu-id="b2c98-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="b2c98-298">使用 USMF 示例数据</span><span class="sxs-lookup"><span data-stu-id="b2c98-298">Use the USMF sample data</span></span>

<span data-ttu-id="b2c98-299">若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="b2c98-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b2c98-300">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="b2c98-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="b2c98-301">创建需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-301">Create demand</span></span>

<span data-ttu-id="b2c98-302">执行以下步骤创建将为其应用时隙的需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="b2c98-303">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="b2c98-304">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="b2c98-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b2c98-305">在 **创建销售订单** 对话框的 **客户帐户** 字段中，选择 _US-007_。</span><span class="sxs-lookup"><span data-stu-id="b2c98-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="b2c98-306">在 **仓库** 字段中，选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="b2c98-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="b2c98-307">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-307">Select **OK**.</span></span>
1. <span data-ttu-id="b2c98-308">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="b2c98-308">The new sales order is opened.</span></span> <span data-ttu-id="b2c98-309">将在 **销售订单行** 快速选项卡中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2c98-310">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-311">**物料：**_L0101_</span><span class="sxs-lookup"><span data-stu-id="b2c98-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="b2c98-312">**数量：** _20_</span><span class="sxs-lookup"><span data-stu-id="b2c98-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="b2c98-313">选择 **添加行** 添加新行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="b2c98-314">**物料：**_T0100_</span><span class="sxs-lookup"><span data-stu-id="b2c98-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="b2c98-315">**数量：** _8_</span><span class="sxs-lookup"><span data-stu-id="b2c98-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="b2c98-316">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-316">Select **Save**.</span></span>
1. <span data-ttu-id="b2c98-317">选择 **新建** 以创建第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="b2c98-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="b2c98-318">在 **创建销售订单** 对话框的 **客户帐户** 字段中，选择 _US-008_。</span><span class="sxs-lookup"><span data-stu-id="b2c98-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="b2c98-319">在 **仓库** 字段中，选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="b2c98-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="b2c98-320">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="b2c98-320">The new sales order is opened.</span></span> <span data-ttu-id="b2c98-321">将在 **销售订单行** 快速选项卡中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2c98-322">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b2c98-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2c98-323">**物料：**_T0100_</span><span class="sxs-lookup"><span data-stu-id="b2c98-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="b2c98-324">**数量：** _1_</span><span class="sxs-lookup"><span data-stu-id="b2c98-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="b2c98-325">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="b2c98-326">完成典型时隙场景</span><span class="sxs-lookup"><span data-stu-id="b2c98-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="b2c98-327">按照上一部分中的说明准备好所有先决元素之后，可以通过完成本部分中的每个练习试用此功能。</span><span class="sxs-lookup"><span data-stu-id="b2c98-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="b2c98-328">生成需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-328">Generate demand</span></span>

1. <span data-ttu-id="b2c98-329">转到 **仓库管理 \> 设置 \> 补货 \> 时隙模板**，然后选择前面创建的时隙模板。</span><span class="sxs-lookup"><span data-stu-id="b2c98-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="b2c98-330">在操作窗格上，选择 **生成需求**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="b2c98-331">此命令评估系统中的所有需求，并且与时隙模板查询匹配。</span><span class="sxs-lookup"><span data-stu-id="b2c98-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="b2c98-332">然后将所有订单中的总需求合并到行，每个数量/度量单位一行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="b2c98-333">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="b2c98-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="b2c98-334">时隙需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-334">Slotting demand</span></span>

<span data-ttu-id="b2c98-335">*时隙需求* 根据时隙模板的设置显示生成需求的结果。</span><span class="sxs-lookup"><span data-stu-id="b2c98-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="b2c98-336">在操作窗格上，选择 **时隙需求** 查看 **生成需求** 命令的结果。</span><span class="sxs-lookup"><span data-stu-id="b2c98-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="b2c98-337">可以编辑时隙需求中的行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="b2c98-338">可以删除行，添加新行，或编辑行详细信息。</span><span class="sxs-lookup"><span data-stu-id="b2c98-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="b2c98-339">可以手动编辑需求，也可以使用数据管理从外部系统导入需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="b2c98-340">无论时隙中是什么，也无论其来自何处，都将在下一步使用需求。</span><span class="sxs-lookup"><span data-stu-id="b2c98-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="b2c98-341">查找需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-341">Locate demand</span></span>

<span data-ttu-id="b2c98-342">生成需求后，必须使用 **查找需求** 命令生成 *时隙计划*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="b2c98-343">在操作窗格上，选择 **查找需求**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="b2c98-344">将运行时隙流程。</span><span class="sxs-lookup"><span data-stu-id="b2c98-344">The slotting process runs.</span></span> <span data-ttu-id="b2c98-345">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="b2c98-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="b2c98-346">时隙计划</span><span class="sxs-lookup"><span data-stu-id="b2c98-346">Slotting plan</span></span>

<span data-ttu-id="b2c98-347">时隙计划显示将每个物料/数量分配给了哪个货位，是否使用了溢出，是否创建了放弃工作，以及是否使用了模板行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="b2c98-348">*所有无法划分时隙的需求均以红色突出显示。*</span><span class="sxs-lookup"><span data-stu-id="b2c98-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="b2c98-349">在操作窗格上，选择 **时隙计划** 查看结果。</span><span class="sxs-lookup"><span data-stu-id="b2c98-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="b2c98-350">**生成需求**、**查找需求** 和 **运行补货** 流程现在在沙盒中运行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="b2c98-351">（这些流程可以从 **时隙模板** 页的操作窗格中找到。）</span><span class="sxs-lookup"><span data-stu-id="b2c98-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="b2c98-352">**生成需求**、**查找需求** 和 **运行补货** 流程带有锁定功能，以确保不会被同时触发。</span><span class="sxs-lookup"><span data-stu-id="b2c98-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="b2c98-353">否则，使用的数据可能被删除。</span><span class="sxs-lookup"><span data-stu-id="b2c98-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="b2c98-354">如果运行未生成记录或记录缺少信息，**生成需求** 和 **查找需求** 流程会显示警告。</span><span class="sxs-lookup"><span data-stu-id="b2c98-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="b2c98-355">当您选择 **时隙计划** 时，页面在操作窗格上没有 **新建**、**编辑** 或 **删除** 按钮，因为数据源不能进行编辑。</span><span class="sxs-lookup"><span data-stu-id="b2c98-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="b2c98-356">当您选择 **运行补货** 时，系统将验证所选的时隙模板和流程。</span><span class="sxs-lookup"><span data-stu-id="b2c98-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="b2c98-357">创建补货</span><span class="sxs-lookup"><span data-stu-id="b2c98-357">Create replenishment</span></span>

<span data-ttu-id="b2c98-358">创建时隙计划之后，必须根据计划创建 *补货工作*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="b2c98-359">在操作窗格上，选择 **运行补货**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="b2c98-360">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="b2c98-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="b2c98-361">此消息指示为工作生成 ID 创建的标题的数量。</span><span class="sxs-lookup"><span data-stu-id="b2c98-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="b2c98-362">将根据在每个模板行中指定的指令代码确定将使用的货位指令。</span><span class="sxs-lookup"><span data-stu-id="b2c98-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="b2c98-363">提示</span><span class="sxs-lookup"><span data-stu-id="b2c98-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="b2c98-364">设置自动时隙</span><span class="sxs-lookup"><span data-stu-id="b2c98-364">Set up automatic slotting</span></span>

<span data-ttu-id="b2c98-365">准备好所有必需元素之后，可以执行以下步骤将时隙设置为自动运行。</span><span class="sxs-lookup"><span data-stu-id="b2c98-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="b2c98-366">转到 **仓库管理 \> 补货 \> 运行时隙**。</span><span class="sxs-lookup"><span data-stu-id="b2c98-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="b2c98-367">指定要运行的时隙步骤。</span><span class="sxs-lookup"><span data-stu-id="b2c98-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="b2c98-368">选择下面的一个或多个时隙步骤：</span><span class="sxs-lookup"><span data-stu-id="b2c98-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="b2c98-369">生成需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-369">Generate demand</span></span>
    - <span data-ttu-id="b2c98-370">查找需求</span><span class="sxs-lookup"><span data-stu-id="b2c98-370">Locate demand</span></span>
    - <span data-ttu-id="b2c98-371">创建补货工作</span><span class="sxs-lookup"><span data-stu-id="b2c98-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2c98-372">时隙步骤是渐进的。</span><span class="sxs-lookup"><span data-stu-id="b2c98-372">The slotting steps are progressive.</span></span> <span data-ttu-id="b2c98-373">如果要选择 *查找需求*，必须先选择 *生成需求*。</span><span class="sxs-lookup"><span data-stu-id="b2c98-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="b2c98-374">指定要使用的时隙模板。</span><span class="sxs-lookup"><span data-stu-id="b2c98-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="b2c98-375">如果需要，设置要自动运行的发生次数。</span><span class="sxs-lookup"><span data-stu-id="b2c98-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="b2c98-376">对于此场景中的练习，请 **勿** 设置自动时隙。</span><span class="sxs-lookup"><span data-stu-id="b2c98-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
