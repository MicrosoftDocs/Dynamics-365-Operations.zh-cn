---
title: 仓库时隙
description: 文主题提供有关仓库时隙的信息。 仓库时隙用于按物料和度量单位合并状态为“订购”、“预留”或“下达”的订单中的需求。 其可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料货位。
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d9080f192db0c59b4b4bc74468491e86ba0b7471
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530343"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="f3c84-105">仓库时隙</span><span class="sxs-lookup"><span data-stu-id="f3c84-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3c84-106">仓库时隙用于按物料和度量单位合并状态为*订购*、*预留*或*下达*的订单中的需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="f3c84-107">然后可以根据数量、单位、物理维度、固定货位等将生成的需求应用于将用于领料的货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="f3c84-108">建立时隙计划之后，可以创建补货工作以将相应数量的库存运到各货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="f3c84-109">此功能可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="f3c84-110">开启“仓库时隙”功能</span><span class="sxs-lookup"><span data-stu-id="f3c84-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="f3c84-111">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="f3c84-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f3c84-112">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="f3c84-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f3c84-113">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="f3c84-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f3c84-114">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="f3c84-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f3c84-115">**功能名称**：*仓库时隙功能*</span><span class="sxs-lookup"><span data-stu-id="f3c84-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="f3c84-116">设置仓库时隙功能</span><span class="sxs-lookup"><span data-stu-id="f3c84-116">Set up warehouse slotting</span></span>

<span data-ttu-id="f3c84-117">若要使用仓库时隙功能，必须在系统中设置以下元素。</span><span class="sxs-lookup"><span data-stu-id="f3c84-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="f3c84-118">为时隙创建度量单位层</span><span class="sxs-lookup"><span data-stu-id="f3c84-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="f3c84-119">可通过度量单位层将多个度量单位组合到一起来达到时隙目的。</span><span class="sxs-lookup"><span data-stu-id="f3c84-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="f3c84-120">例如，如果多个尺寸的箱子全部从同一个箱子领取区领取，则可以为所有这些尺寸创建一个层。</span><span class="sxs-lookup"><span data-stu-id="f3c84-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="f3c84-121">**必须为应该属于层的每个度量单位创建一行。**</span><span class="sxs-lookup"><span data-stu-id="f3c84-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="f3c84-122">转到**仓库管理 \> 设置 \> 补货 \> 时隙度量单位层**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="f3c84-123">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-123">Select **New**.</span></span>
1. <span data-ttu-id="f3c84-124">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="f3c84-125">**度量单位层**：*EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="f3c84-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="f3c84-126">**说明**：*每个箱托盘*</span><span class="sxs-lookup"><span data-stu-id="f3c84-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="f3c84-127">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-127">Select **Save**.</span></span>
1. <span data-ttu-id="f3c84-128">在**度量单位**快速选项卡上，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f3c84-129">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-130">**单位**：*箱*</span><span class="sxs-lookup"><span data-stu-id="f3c84-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="f3c84-131">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f3c84-132">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="f3c84-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f3c84-133">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="f3c84-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f3c84-134">选择**新建**向网格添加第二行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="f3c84-135">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-136">**单位：** *ea*</span><span class="sxs-lookup"><span data-stu-id="f3c84-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="f3c84-137">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f3c84-138">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="f3c84-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f3c84-139">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="f3c84-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f3c84-140">选择**新建**向网格添加第三行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="f3c84-141">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-142">**单位**：*PL*</span><span class="sxs-lookup"><span data-stu-id="f3c84-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="f3c84-143">**说明：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f3c84-144">保存更改时，将自动填写。</span><span class="sxs-lookup"><span data-stu-id="f3c84-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f3c84-145">**单位类**：*数量*</span><span class="sxs-lookup"><span data-stu-id="f3c84-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f3c84-146">选择**保存**以保存层。</span><span class="sxs-lookup"><span data-stu-id="f3c84-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="f3c84-147">为时隙创建指令代码</span><span class="sxs-lookup"><span data-stu-id="f3c84-147">Create a directive code for slotting</span></span>

<span data-ttu-id="f3c84-148">必须选择应与模板关联的指令代码。</span><span class="sxs-lookup"><span data-stu-id="f3c84-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="f3c84-149">转到**库存管理 \> 设置 \> 指令代码**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="f3c84-150">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f3c84-151">在**指令代码**字段中，输入*时隙*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="f3c84-152">在**指令说明**字段中，输入*时隙*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="f3c84-153">设置时隙模板</span><span class="sxs-lookup"><span data-stu-id="f3c84-153">Set up slotting templates</span></span>

<span data-ttu-id="f3c84-154">各时隙模板控制如何将库存分配给特定仓库的货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="f3c84-155">每个时隙规范在每个模板中必须有一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="f3c84-156">可使用此部分中的过程设置时隙模板。</span><span class="sxs-lookup"><span data-stu-id="f3c84-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="f3c84-157">转到**仓库管理 \> 设置 \> 补货 \> 时隙模板**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="f3c84-158">选择**新建**以创建模板。</span><span class="sxs-lookup"><span data-stu-id="f3c84-158">Select **New** to create a template.</span></span>

<span data-ttu-id="f3c84-159">接下来，必须按照下面子部分中的说明设置模板标题、时隙规范和货位指令。</span><span class="sxs-lookup"><span data-stu-id="f3c84-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="f3c84-160">设置时隙模板标题</span><span class="sxs-lookup"><span data-stu-id="f3c84-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="f3c84-161">在模板的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="f3c84-162">**时隙模板：**_61_</span><span class="sxs-lookup"><span data-stu-id="f3c84-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="f3c84-163">**说明：**_61_</span><span class="sxs-lookup"><span data-stu-id="f3c84-163">**Description:** _61_</span></span>
    - <span data-ttu-id="f3c84-164">**需求类型**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="f3c84-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="f3c84-165">现在，*销售订单*是唯一支持的需求类型。</span><span class="sxs-lookup"><span data-stu-id="f3c84-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="f3c84-166">**需求策略：**_订购_</span><span class="sxs-lookup"><span data-stu-id="f3c84-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="f3c84-167">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="f3c84-168">**订购** – 应该将销售订单中的所有订购数量视为需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="f3c84-169">**预留** – 仅应将预留的销售订单行数量（订购的实物）视为需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="f3c84-170">**仓库**：_61_</span><span class="sxs-lookup"><span data-stu-id="f3c84-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f3c84-171">**允许波次需求使用未预留数量：**_是_</span><span class="sxs-lookup"><span data-stu-id="f3c84-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="f3c84-172">还可以指定查询以缩小评估的需求范围。</span><span class="sxs-lookup"><span data-stu-id="f3c84-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="f3c84-173">为每个模板设置时隙规范</span><span class="sxs-lookup"><span data-stu-id="f3c84-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="f3c84-174">对于创建的每个模板，执行以下步骤为每个时隙规范添加一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="f3c84-175">在**时隙模板详细信息**快速选项卡上，选择**新建**创建一个模板行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="f3c84-176">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-177">**序列：** _1_</span><span class="sxs-lookup"><span data-stu-id="f3c84-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="f3c84-178">**说明：**_固定货位_</span><span class="sxs-lookup"><span data-stu-id="f3c84-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="f3c84-179">**最小数量：**_1_</span><span class="sxs-lookup"><span data-stu-id="f3c84-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="f3c84-180">此字段定义行需要的最小需求数量。</span><span class="sxs-lookup"><span data-stu-id="f3c84-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="f3c84-181">**最大数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="f3c84-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="f3c84-182">此字段定义行的最大有效需求数量。</span><span class="sxs-lookup"><span data-stu-id="f3c84-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="f3c84-183">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="f3c84-184">此字段定义最小数量和最大数量引用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="f3c84-185">**度量单位层：**_EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f3c84-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="f3c84-186">此字段定义行的有效需求度量单位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="f3c84-187">（有关详细信息，请参阅本主题前面的[为时隙设置度量单位层](#unit-tiers)部分。）</span><span class="sxs-lookup"><span data-stu-id="f3c84-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="f3c84-188">**分配时隙条件：**_考虑数量_</span><span class="sxs-lookup"><span data-stu-id="f3c84-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="f3c84-189">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="f3c84-190">**假设为空** – 该系统应假设领料区中的所有货位均为空，并且不应检查这些货位是否有库存。</span><span class="sxs-lookup"><span data-stu-id="f3c84-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="f3c84-191">**考虑数量** – 系统应检查领料区中的货位是否有库存，并且应该跳过所有非空货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="f3c84-192">**指令代码：**_时隙_</span><span class="sxs-lookup"><span data-stu-id="f3c84-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="f3c84-193">此字段定义货位指令，用于查找补货工作的领料货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="f3c84-194">**溢出货位：** 将此字段保持为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="f3c84-195">此字段定义如果在处理行时找不到货位，应将库存放入的货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="f3c84-196">**允许放弃：**_是_</span><span class="sxs-lookup"><span data-stu-id="f3c84-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="f3c84-197">如果此选项设置为*是*，并且不能为任何需求划分时隙，将创建移动工作把库存移出有库存，但未划分时隙的货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="f3c84-198">然后再次运行模板。</span><span class="sxs-lookup"><span data-stu-id="f3c84-198">The template is then run again.</span></span> <span data-ttu-id="f3c84-199">这次将忽略货位中的库存。</span><span class="sxs-lookup"><span data-stu-id="f3c84-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="f3c84-200">如果**分配时隙条件**字段设置为_考虑数量_，此功能效果最好。</span><span class="sxs-lookup"><span data-stu-id="f3c84-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="f3c84-201">**固定货位用法：**_仅限产品的固定货位_</span><span class="sxs-lookup"><span data-stu-id="f3c84-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="f3c84-202">此字段中提供以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="f3c84-203">**固定货位和非固定货位** – 不应将系统限制为只能使用固定货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="f3c84-204">**仅限产品的固定货位** – 系统应该将货位的时隙划分给仅限产品的固定货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="f3c84-205">**仅限产品变型的固定货位** – 系统应该将货位的时隙划分给仅限产品变型的固定货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="f3c84-206">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-206">Select **Save**.</span></span>
1. <span data-ttu-id="f3c84-207">选择**新建**创建第二个模板行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="f3c84-208">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-209">**序列：** _2_</span><span class="sxs-lookup"><span data-stu-id="f3c84-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="f3c84-210">**说明：**_其他_</span><span class="sxs-lookup"><span data-stu-id="f3c84-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="f3c84-211">**最小数量：**_1_</span><span class="sxs-lookup"><span data-stu-id="f3c84-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="f3c84-212">**最大数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="f3c84-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="f3c84-213">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="f3c84-214">**度量单位层：**_EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f3c84-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="f3c84-215">**分配时隙条件：**_考虑数量_</span><span class="sxs-lookup"><span data-stu-id="f3c84-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="f3c84-216">**指令代码：**_时隙_</span><span class="sxs-lookup"><span data-stu-id="f3c84-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="f3c84-217">**溢出货位：** 将此字段保持为空。</span><span class="sxs-lookup"><span data-stu-id="f3c84-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="f3c84-218">**允许放弃：**_是_</span><span class="sxs-lookup"><span data-stu-id="f3c84-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="f3c84-219">**使用固定货位：**_固定货位和非固定货位_</span><span class="sxs-lookup"><span data-stu-id="f3c84-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="f3c84-220">在查询第二个行时，现在指定用于确定可以将该行的需求时隙划分给哪些货位。</span><span class="sxs-lookup"><span data-stu-id="f3c84-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="f3c84-221">选择其中的**序列**字段设置为 *2* 的行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="f3c84-222">选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="f3c84-223">在**范围**选项卡中，选择**添加**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f3c84-224">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-225">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="f3c84-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f3c84-226">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="f3c84-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f3c84-227">\**字段：\*\*\*位置模板 ID*</span><span class="sxs-lookup"><span data-stu-id="f3c84-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="f3c84-228">**条件**：*Pick-06*（选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Pick-06* - *领料点 6*。）</span><span class="sxs-lookup"><span data-stu-id="f3c84-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="f3c84-229">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="f3c84-230">设置货位指令</span><span class="sxs-lookup"><span data-stu-id="f3c84-230">Set up location directives</span></span>

<span data-ttu-id="f3c84-231">必须设置至少一个货位指令来支持时隙领料。</span><span class="sxs-lookup"><span data-stu-id="f3c84-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="f3c84-232">请按照此部分中的过程为时隙领料设置一个新的*补货货位指令*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="f3c84-233">转到**库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f3c84-234">在左窗格的**工作订单类型**字段中，选择*补货*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="f3c84-235">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f3c84-236">在新货位指令的标题中**名称**字段内，输入 *61 时隙领料*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="f3c84-237">配置“货位指令”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="f3c84-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="f3c84-238">在**货位指令**快速选项卡上，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="f3c84-239">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f3c84-240">**工作类型：**_领料_</span><span class="sxs-lookup"><span data-stu-id="f3c84-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="f3c84-241">**站点**：_6_</span><span class="sxs-lookup"><span data-stu-id="f3c84-241">**Site:** _6_</span></span>
    - <span data-ttu-id="f3c84-242">**仓库**：_61_</span><span class="sxs-lookup"><span data-stu-id="f3c84-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f3c84-243">**指令代码**：_时隙_</span><span class="sxs-lookup"><span data-stu-id="f3c84-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="f3c84-244">选择**保存**激活**行**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f3c84-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="f3c84-245">配置“行”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="f3c84-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="f3c84-246">在**行**快速选项卡上，选择**新建**创建一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f3c84-247">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-247">On the new line, set the following values.</span></span> <span data-ttu-id="f3c84-248">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f3c84-249">**起始数量：**_0_</span><span class="sxs-lookup"><span data-stu-id="f3c84-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="f3c84-250">**目标数量：**_1000000_</span><span class="sxs-lookup"><span data-stu-id="f3c84-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="f3c84-251">选择**保存**激活**货位指令操作**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f3c84-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="f3c84-252">配置“货位指令操作”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="f3c84-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="f3c84-253">在**货位指令操作**快速选项卡上，选择**新建**创建一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f3c84-254">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-254">On the new line, set the following values.</span></span> <span data-ttu-id="f3c84-255">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="f3c84-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f3c84-256">**名称**：_Bulk_</span><span class="sxs-lookup"><span data-stu-id="f3c84-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="f3c84-257">**策略**：_无_</span><span class="sxs-lookup"><span data-stu-id="f3c84-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="f3c84-258">选择**保存**激活**编辑查询**按钮。</span><span class="sxs-lookup"><span data-stu-id="f3c84-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="f3c84-259">编辑查询</span><span class="sxs-lookup"><span data-stu-id="f3c84-259">Edit the query</span></span>

1. <span data-ttu-id="f3c84-260">在**位置指令操作**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="f3c84-261">在**范围**选项卡中，选择**添加**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f3c84-262">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-263">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="f3c84-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f3c84-264">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="f3c84-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f3c84-265">**字段：** *区域 ID*</span><span class="sxs-lookup"><span data-stu-id="f3c84-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="f3c84-266">**条件**：*Bulk*（选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Bulk*。）</span><span class="sxs-lookup"><span data-stu-id="f3c84-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="f3c84-267">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="f3c84-268">应用场景</span><span class="sxs-lookup"><span data-stu-id="f3c84-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="f3c84-269">设置场景</span><span class="sxs-lookup"><span data-stu-id="f3c84-269">Set up the scenario</span></span>

<span data-ttu-id="f3c84-270">对于此场景，请使用内置示例数据，然后创建本部分中介绍的记录。</span><span class="sxs-lookup"><span data-stu-id="f3c84-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="f3c84-271">使用 USMF 示例数据</span><span class="sxs-lookup"><span data-stu-id="f3c84-271">Use the USMF sample data</span></span>

<span data-ttu-id="f3c84-272">若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="f3c84-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f3c84-273">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="f3c84-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="f3c84-274">创建需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-274">Create demand</span></span>

<span data-ttu-id="f3c84-275">执行以下步骤创建将为其应用时隙的需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="f3c84-276">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="f3c84-277">选择**新建**以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="f3c84-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f3c84-278">在**创建销售订单**对话框的**客户帐户**字段中，选择 _US-007_。</span><span class="sxs-lookup"><span data-stu-id="f3c84-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="f3c84-279">在**仓库**字段中，选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="f3c84-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f3c84-280">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-280">Select **OK**.</span></span>
1. <span data-ttu-id="f3c84-281">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="f3c84-281">The new sales order is opened.</span></span> <span data-ttu-id="f3c84-282">将在**销售订单行**快速选项卡中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f3c84-283">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-284">**物料：**_L0101_</span><span class="sxs-lookup"><span data-stu-id="f3c84-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="f3c84-285">**数量：** _20_</span><span class="sxs-lookup"><span data-stu-id="f3c84-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="f3c84-286">选择**添加行**添加新行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="f3c84-287">**物料：**_T0100_</span><span class="sxs-lookup"><span data-stu-id="f3c84-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f3c84-288">**数量：** _8_</span><span class="sxs-lookup"><span data-stu-id="f3c84-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="f3c84-289">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-289">Select **Save**.</span></span>
1. <span data-ttu-id="f3c84-290">选择**新建**以创建第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="f3c84-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="f3c84-291">在**创建销售订单**对话框的**客户帐户**字段中，选择 _US-008_。</span><span class="sxs-lookup"><span data-stu-id="f3c84-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="f3c84-292">在**仓库**字段中，选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="f3c84-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f3c84-293">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="f3c84-293">The new sales order is opened.</span></span> <span data-ttu-id="f3c84-294">将在**销售订单行**快速选项卡中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f3c84-295">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f3c84-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="f3c84-296">**物料：**_T0100_</span><span class="sxs-lookup"><span data-stu-id="f3c84-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f3c84-297">**数量：** _1_</span><span class="sxs-lookup"><span data-stu-id="f3c84-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="f3c84-298">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="f3c84-299">完成典型时隙场景</span><span class="sxs-lookup"><span data-stu-id="f3c84-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="f3c84-300">按照上一部分中的说明准备好所有先决元素之后，可以通过完成本部分中的每个练习试用此功能。</span><span class="sxs-lookup"><span data-stu-id="f3c84-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="f3c84-301">生成需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-301">Generate demand</span></span>

1. <span data-ttu-id="f3c84-302">转到**仓库管理 \> 设置 \> 补货 \> 时隙模板**，然后选择前面创建的时隙模板。</span><span class="sxs-lookup"><span data-stu-id="f3c84-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="f3c84-303">在操作窗格上，选择**生成需求**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="f3c84-304">此命令评估系统中的所有需求，并且与时隙模板查询匹配。</span><span class="sxs-lookup"><span data-stu-id="f3c84-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="f3c84-305">然后将所有订单中的总需求合并到行，每个数量/度量单位一行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="f3c84-306">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="f3c84-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="f3c84-307">时隙需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-307">Slotting demand</span></span>

<span data-ttu-id="f3c84-308">*时隙需求*根据时隙模板的设置显示生成需求的结果。</span><span class="sxs-lookup"><span data-stu-id="f3c84-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="f3c84-309">在操作窗格上，选择**时隙需求**查看**生成需求**命令的结果。</span><span class="sxs-lookup"><span data-stu-id="f3c84-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="f3c84-310">可以编辑时隙需求中的行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="f3c84-311">可以删除行，添加新行，或编辑行详细信息。</span><span class="sxs-lookup"><span data-stu-id="f3c84-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="f3c84-312">可以手动编辑需求，也可以使用数据管理从外部系统导入需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="f3c84-313">无论时隙中是什么，也无论其来自何处，都将在下一步使用需求。</span><span class="sxs-lookup"><span data-stu-id="f3c84-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="f3c84-314">查找需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-314">Locate demand</span></span>

<span data-ttu-id="f3c84-315">生成需求后，必须使用**查找需求**命令生成*时隙计划*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="f3c84-316">在操作窗格上，选择**查找需求**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="f3c84-317">将运行时隙流程。</span><span class="sxs-lookup"><span data-stu-id="f3c84-317">The slotting process runs.</span></span> <span data-ttu-id="f3c84-318">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="f3c84-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="f3c84-319">时隙计划</span><span class="sxs-lookup"><span data-stu-id="f3c84-319">Slotting plan</span></span>

<span data-ttu-id="f3c84-320">时隙计划显示将每个物料/数量分配给了哪个货位，是否使用了溢出，是否创建了放弃工作，以及是否使用了模板行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="f3c84-321">**所有无法划分时隙的需求均以红色突出显示。**</span><span class="sxs-lookup"><span data-stu-id="f3c84-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="f3c84-322">在操作窗格上，选择**时隙计划**查看结果。</span><span class="sxs-lookup"><span data-stu-id="f3c84-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="f3c84-323">创建补货</span><span class="sxs-lookup"><span data-stu-id="f3c84-323">Create replenishment</span></span>

<span data-ttu-id="f3c84-324">创建时隙计划之后，必须根据计划创建*补货工作*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="f3c84-325">在操作窗格上，选择**运行补货**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="f3c84-326">完成此流程时，将显示参考消息。</span><span class="sxs-lookup"><span data-stu-id="f3c84-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="f3c84-327">此消息指示为工作生成 ID 创建的标题的数量。</span><span class="sxs-lookup"><span data-stu-id="f3c84-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="f3c84-328">将根据在每个模板行中指定的指令代码确定将使用的货位指令。</span><span class="sxs-lookup"><span data-stu-id="f3c84-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="f3c84-329">提示</span><span class="sxs-lookup"><span data-stu-id="f3c84-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="f3c84-330">设置自动时隙</span><span class="sxs-lookup"><span data-stu-id="f3c84-330">Set up automatic slotting</span></span>

<span data-ttu-id="f3c84-331">准备好所有必需元素之后，可以执行以下步骤将时隙设置为自动运行。</span><span class="sxs-lookup"><span data-stu-id="f3c84-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="f3c84-332">转到**仓库管理 \> 补货 \> 运行时隙**。</span><span class="sxs-lookup"><span data-stu-id="f3c84-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="f3c84-333">指定要运行的时隙步骤。</span><span class="sxs-lookup"><span data-stu-id="f3c84-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="f3c84-334">选择下面的一个或多个时隙步骤：</span><span class="sxs-lookup"><span data-stu-id="f3c84-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="f3c84-335">生成需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-335">Generate demand</span></span>
    - <span data-ttu-id="f3c84-336">查找需求</span><span class="sxs-lookup"><span data-stu-id="f3c84-336">Locate demand</span></span>
    - <span data-ttu-id="f3c84-337">创建补货工作</span><span class="sxs-lookup"><span data-stu-id="f3c84-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3c84-338">时隙步骤是渐进的。</span><span class="sxs-lookup"><span data-stu-id="f3c84-338">The slotting steps are progressive.</span></span> <span data-ttu-id="f3c84-339">如果要选择*查找需求*，必须先选择*生成需求*。</span><span class="sxs-lookup"><span data-stu-id="f3c84-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="f3c84-340">指定要使用的时隙模板。</span><span class="sxs-lookup"><span data-stu-id="f3c84-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="f3c84-341">如果需要，设置要自动运行的发生次数。</span><span class="sxs-lookup"><span data-stu-id="f3c84-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="f3c84-342">对于此场景中的练习，请**勿**设置自动时隙。</span><span class="sxs-lookup"><span data-stu-id="f3c84-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
