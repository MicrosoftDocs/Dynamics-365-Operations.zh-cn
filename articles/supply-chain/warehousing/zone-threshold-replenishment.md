---
title: 区域阈值补货
description: 基于区域的补货使用最小/最大补货策略，但是会评估所有仓库区域，而不仅是评估单个货位。 因此，仓库经理可以更快地确定领料区中是否需要更多库存。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6aaa139fb206c035b25b7056e681d086fde6447f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245050"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="6d4bb-104">区域阈值补货</span><span class="sxs-lookup"><span data-stu-id="6d4bb-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d4bb-105">基于区域的补货使用最小/最大[补货](replenishment.md)策略，但是会评估所有仓库区域，而不仅是评估单个货位。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="6d4bb-106">因此，仓库经理可以更快地确定领料区中是否需要更多库存。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="6d4bb-107">此功能的设置类似基于货位的补货的设置。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="6d4bb-108">但是，为最小/最大补货设置模板时，也可以指定应该按货位还是按区域评估阈值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="6d4bb-109">如果设置基于区域的评估，则必须向区域选择查询添加特定区域。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="6d4bb-110">与基于货位的最小/最大补货一样，基于区域的最小/最大补货基于最小库存阈值的设置，该阈值触发所选物料的补货工作创建。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="6d4bb-111">此补货工作将把库存最大提高到为区域指定的最大阈值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="6d4bb-112">当前版本不支持产品变型的区域补货过程。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="6d4bb-113">与基于货位的最小/最大补货不同，基于区域的最小/最大补货不需要固定货位即可评估货位是否应该存储特定物料。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="6d4bb-114">因此，即使仓库中的每个物料或物料变型没有固定货位，基于区域的补货也允许您使用最小/最大补货。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="6d4bb-115">当区域中的数量降至指定的最小阈值以下时，将创建补货工作。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="6d4bb-116">货位指令决定应将库存放入哪个特定货位中。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="6d4bb-117">开启“区域阈值补货”功能</span><span class="sxs-lookup"><span data-stu-id="6d4bb-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="6d4bb-118">*区域阈值补货* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="6d4bb-119">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6d4bb-120">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6d4bb-121">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6d4bb-122">**功能名称**：*区域阈值补货*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="6d4bb-123">设置基于区域的补货</span><span class="sxs-lookup"><span data-stu-id="6d4bb-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="6d4bb-124">若要设置基于区域的补货，必须配置系统的多个部分。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="6d4bb-125">本部分介绍各种设置，并提供在您要完成本主题结尾的场景时可输入的示例数据值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="6d4bb-126">设置指令代码</span><span class="sxs-lookup"><span data-stu-id="6d4bb-126">Set up directive codes</span></span>

<span data-ttu-id="6d4bb-127">定义工作模板中使用的货位模板时，[指令代码](control-warehouse-location-directives.md)可以提高具体程度。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="6d4bb-128">每个代码建立一个公共值，可在配置各种模板时引用。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="6d4bb-129">查看和编辑指令代码</span><span class="sxs-lookup"><span data-stu-id="6d4bb-129">View and edit directive codes</span></span>

<span data-ttu-id="6d4bb-130">若要查看或编辑指令代码，请转到 **仓库管理 \> 设置 \> 指令代码**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="6d4bb-131">准备演示数据指令代码</span><span class="sxs-lookup"><span data-stu-id="6d4bb-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="6d4bb-132">本示例说明如何准备指令代码。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="6d4bb-133">如果计划完成本主题结尾的场景，请使用此处提供的演示数据值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="6d4bb-134">否则，请使用您自己的值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="6d4bb-135">选择法人 **USMF** 使用这些演示数据。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="6d4bb-136">转到 **库存管理 \> 设置 \> 指令代码**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="6d4bb-137">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-138">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-139">**指令代码：**_区域补货_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="6d4bb-140">**指令说明：**_区域补货_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="6d4bb-141">选择 **保存** 以保存新代码。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="6d4bb-142">设置补货模板</span><span class="sxs-lookup"><span data-stu-id="6d4bb-142">Set up replenishment templates</span></span>

<span data-ttu-id="6d4bb-143">[最小/最大补货模板](tasks/set-up-min-max-replenishment-process.md)是用于维护领料货位最佳级别的主要机制。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="6d4bb-144">在这些模板中，必须设置将用于在仓库中为库存补货的规则。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="6d4bb-145">模板可用于的补货中包含基于区域的补货。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="6d4bb-146">查看和编辑补货模板</span><span class="sxs-lookup"><span data-stu-id="6d4bb-146">View and edit replenishment templates</span></span>

<span data-ttu-id="6d4bb-147">补货模板是控制何时和如何为货位补货的一系列规则。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="6d4bb-148">选择模板以控制何时和如何进行补货。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="6d4bb-149">若要查看或编辑补货模板，请转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="6d4bb-150">准备演示数据补货模板</span><span class="sxs-lookup"><span data-stu-id="6d4bb-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="6d4bb-151">本示例说明如何准备补货模板。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="6d4bb-152">如果计划完成本主题结尾的场景，请使用此处提供的演示数据值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="6d4bb-153">否则，请使用您自己的值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="6d4bb-154">选择法人 **USMF** 使用这些演示数据。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="6d4bb-155">转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="6d4bb-156">选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="6d4bb-157">在操作窗格上，选择 **新建** 向 **概览** 网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="6d4bb-158">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-158">In the new row, set the following values.</span></span> <span data-ttu-id="6d4bb-159">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="6d4bb-160">**补货模板：**_区域最小/最大补货_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="6d4bb-161">**说明：**_区域最小/最大补货_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="6d4bb-162">**补货类型：**_最小或最大_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="6d4bb-163">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-163">Select **Save**.</span></span>
1. <span data-ttu-id="6d4bb-164">**概览** 网格中的新行仍处于选中状态时，选择 **补货模板详细信息** 网格上方的 **新建** 添加与您刚才创建的 *区域最小/最大补货* 补货模板关联的行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="6d4bb-165">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-166">**序列号：** 输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="6d4bb-167">**说明：** 输入 _领料区补货_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="6d4bb-168">**补货单位：** 选择 _每个_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="6d4bb-169">**请求类型：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="6d4bb-170">**指令代码：** 此字段将补货模板与货位指令关联。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="6d4bb-171">选择前面创建的演示数据指令代码（_区域补货_）。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="6d4bb-172">**工作模板**：将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="6d4bb-173">**最小数量：** 此字段设置触发补货的数量。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="6d4bb-174">输入 _50_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-174">Enter _50_.</span></span>
    - <span data-ttu-id="6d4bb-175">**最大数量：** 此字段设置某个物料在区域中可存在的最大数量。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="6d4bb-176">生成的补货工作将把库存提高到此数量。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="6d4bb-177">输入 _150_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-177">Enter _150_.</span></span>
    - <span data-ttu-id="6d4bb-178">**单位：** 此字段设置最小值和最大值的单位。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="6d4bb-179">选择 _每个_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-179">Select _ea_.</span></span>
    - <span data-ttu-id="6d4bb-180">**需求增加：** 选择 _进位_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="6d4bb-181">**对空固定货位补货：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="6d4bb-182">**仅对固定货位补货：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-183">**产品查询模式：** 选择 _产品查询_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="6d4bb-184">**补货阈值范围：** 此字段定义模板应该按区域还是按特定货位评估。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="6d4bb-185">选择 _区域_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-185">Select _Zone_.</span></span>
    - <span data-ttu-id="6d4bb-186">**仓库：** 选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="6d4bb-187">选择 **补货模板详细信息** 网格上方的 **选择产品**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="6d4bb-188">在 **产品查询** 对话框的 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-189">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-190">**表：**_物料_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="6d4bb-191">**派生表：**_物料_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="6d4bb-192">**字段：**_物料编号_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="6d4bb-193">**条件：** _A0001_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="6d4bb-194">选择 **确定** 保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="6d4bb-195">选择 **补货模板详细信息** 网格上方的 **选择要补货的区域**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="6d4bb-196">在 **区域查询** 对话框的 **范围** 选项卡中，向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-197">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-198">**表：**_仓库区域_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="6d4bb-199">**派生表：**_仓库区域_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="6d4bb-200">**字段：** _区域 ID_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="6d4bb-201">**条件：**_FLOOR_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="6d4bb-202">选择 **确定** 保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="6d4bb-203">设置货位指令</span><span class="sxs-lookup"><span data-stu-id="6d4bb-203">Set up location directives</span></span>

<span data-ttu-id="6d4bb-204">与基于货位的最小/最大补货不同，基于区域的最小/最大补货需要您同时设置领料货位指令和放置货位指令，因为系统会评估整个区域，而不仅仅是评估出库工作的领料货位。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="6d4bb-205">查看和编辑货位指令</span><span class="sxs-lookup"><span data-stu-id="6d4bb-205">View and edit location directives</span></span>

<span data-ttu-id="6d4bb-206">若要查看或编辑货位指令，请转到 **仓库管理 \> 设置 \> 货位指令**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="6d4bb-207">有关显示如何使用设置创建所需领料货位指令和放置货位指令的示例，请参阅下一部分。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="6d4bb-208">准备演示数据货位指令</span><span class="sxs-lookup"><span data-stu-id="6d4bb-208">Prepare demo data location directives</span></span>

<span data-ttu-id="6d4bb-209">若要准备演示数据以便在本主题结尾的场景中使用，必须创建两个货位指令：一个用于领料，一个用于放置。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="6d4bb-210">创建补货领料指令</span><span class="sxs-lookup"><span data-stu-id="6d4bb-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="6d4bb-211">选择法人 **USMF** 使用这些演示数据。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="6d4bb-212">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="6d4bb-213">在左窗格中，将 **工作订单类型** 设置为 _补货_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="6d4bb-214">在“操作窗格”中，选择 **新建** 创建新指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="6d4bb-215">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-215">Set the following values:</span></span>

    - <span data-ttu-id="6d4bb-216">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="6d4bb-217">**名称：** 输入 _区域领料_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="6d4bb-218">**工作类型：** 选择 _领料_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="6d4bb-219">**站点：** 选择 _6_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="6d4bb-220">**仓库：** 选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="6d4bb-221">**指令代码：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="6d4bb-222">**多个 SKU：** 将此选项设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="6d4bb-223">选择 **保存** 创建具有您迄今为止配置的设置的指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="6d4bb-224">在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6d4bb-225">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-226">**序列号：** 输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="6d4bb-227">**起始数量：** 输入 _0_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="6d4bb-228">**截止数量：** 输入 _10000000_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="6d4bb-229">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="6d4bb-230">**查找数量：** 选择 _无_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="6d4bb-231">**按单位施加的限制：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-232">**进位到单位：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-233">**查找包装数量：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-234">**允许拆分：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="6d4bb-235">选择 **保存** 以保存新行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="6d4bb-236">**行** 网格中的新行仍处于选中状态时，选择 **货位指令操作** 快速选项卡上的 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-237">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-238">**序列号：** 输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="6d4bb-239">**名称：** 输入 _批量领料_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="6d4bb-240">**固定货位使用情况：** 选择 _固定货位和非固定货位_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="6d4bb-241">**允许负库存：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-242">**批处理已启用：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-243">**策略：** 选择 _无_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="6d4bb-244">选择 **保存** 以保存新操作。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="6d4bb-245">新操作仍处于选中状态时，选择 **货位指令操作** 网格上方的 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="6d4bb-246">将显示查询对话框，可在其中选择补货来源货位。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="6d4bb-247">在 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-248">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-249">**表：** _位置_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="6d4bb-250">**派生表：**_货位_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="6d4bb-251">**字段：** _区域 ID_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="6d4bb-252">**条件：** _BULK_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="6d4bb-253">选择 **确定** 保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="6d4bb-254">选择 **保存** 保存货位指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="6d4bb-255">创建补货放置指令</span><span class="sxs-lookup"><span data-stu-id="6d4bb-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="6d4bb-256">在 **货位指令** 页的左窗格中，确保 **工作订单类型** 字段仍然设置为 _补货_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="6d4bb-257">在“操作窗格”中，选择 **新建** 再创建一个新指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="6d4bb-258">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-258">Set the following values:</span></span>

    - <span data-ttu-id="6d4bb-259">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="6d4bb-260">**名称：** 输入 _区域放置_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="6d4bb-261">**工作订单类型：** 选择 _放置_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="6d4bb-262">**站点：** 选择 _6_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="6d4bb-263">**仓库：** 选择 _61_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="6d4bb-264">**指令代码：** 选择 _区域补货_ 将此货位指令与前面使用之前创建的代码创建的补货模板链接。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="6d4bb-265">**多个 SKU：** 将此选项设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="6d4bb-266">选择 **保存** 创建具有您迄今为止配置的设置的指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="6d4bb-267">在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6d4bb-268">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-269">**序列号：** 输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="6d4bb-270">**起始数量：** 输入 _0_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="6d4bb-271">**截止数量：** 输入 _10000000_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="6d4bb-272">**单位**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="6d4bb-273">**查找数量：** 选择 _无_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="6d4bb-274">**按单位施加的限制：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-275">**进位到单位：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-276">**查找包装数量：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-277">**允许拆分：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="6d4bb-278">选择 **保存** 以保存新行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="6d4bb-279">**行** 网格中的新行仍处于选中状态时，选择 **货位指令操作** 快速选项卡上的 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-280">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-281">**序列号：** 输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="6d4bb-282">**名称：** 输入 _区域放置_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="6d4bb-283">**固定货位使用情况：** 选择 _固定货位和非固定货位_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="6d4bb-284">**允许负库存：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-285">**批处理已启用：** 清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="6d4bb-286">**策略：** 选择 _合并_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="6d4bb-287">选择 **保存** 以保存新操作。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="6d4bb-288">新操作仍处于选中状态时，选择 **货位指令操作** 网格上方的 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="6d4bb-289">将显示查询对话框，可在其中选择补货目标区域。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="6d4bb-290">此区域应该是补货模板中指定的同一个区域。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="6d4bb-291">在 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="6d4bb-292">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="6d4bb-293">**表：** _位置_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="6d4bb-294">**派生表：**_货位_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="6d4bb-295">**字段：** _区域 ID_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="6d4bb-296">**条件：**_FLOOR_</span><span class="sxs-lookup"><span data-stu-id="6d4bb-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="6d4bb-297">选择 **确定** 保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="6d4bb-298">选择 **保存** 保存货位指令。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="6d4bb-299">应用场景</span><span class="sxs-lookup"><span data-stu-id="6d4bb-299">Scenario</span></span>

<span data-ttu-id="6d4bb-300">此部分提供一个示例场景，该场景演示如何使用此功能。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="6d4bb-301">准备示例场景所需的示例数据</span><span class="sxs-lookup"><span data-stu-id="6d4bb-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="6d4bb-302">开始完成此场景之前，必须按照本部分中和本主题前面部分中的说明激活示例数据和设置功能。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="6d4bb-303">使用 USMF 法人</span><span class="sxs-lookup"><span data-stu-id="6d4bb-303">Use the USMF legal entity</span></span>

<span data-ttu-id="6d4bb-304">若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="6d4bb-305">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="6d4bb-306">准备其他示例数据</span><span class="sxs-lookup"><span data-stu-id="6d4bb-306">Prepare additional sample data</span></span>

<span data-ttu-id="6d4bb-307">选择法人 **USMF** 之后，请按照本主题前面的[设置基于区域的补货](#setup)部分中的说明添加需要的更多示例数据。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="6d4bb-308">检查现有库存</span><span class="sxs-lookup"><span data-stu-id="6d4bb-308">Check your on-hand inventory</span></span>

<span data-ttu-id="6d4bb-309">执行以下步骤确保系统中有足够库存来支持示例场景。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="6d4bb-310">确保补货模板中指定的领料区 (*FLOOR*) 的两个不同货位内有物料 *A0001* 的现成库存。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="6d4bb-311">但是，库存总量应小于补货模板中指定的最小必需数量 (*50*)。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="6d4bb-312">这样，就可以模拟如何为整个区域进行计算，而不是模拟仅为单个货位进行计算。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="6d4bb-313">**根据需要使用任何仓库流程调整库存。**</span><span class="sxs-lookup"><span data-stu-id="6d4bb-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="6d4bb-314">确保区域领料货位指令中指定的堆放货位（此处补货工作应该从区域 ID *BULK* 领取物料）处有物料 *A0001* 的充足库存。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="6d4bb-315">库存总量必须大于补货模板中指定的最大必需数量 (*150*)。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="6d4bb-316">可选，但是建议：执行以下步骤创建库存调整日记帐：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="6d4bb-317">转到 **库存管理 \> 日记帐条目 \> 物料 \> 库存调整**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="6d4bb-318">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-318">Select **New**.</span></span>
    1. <span data-ttu-id="6d4bb-319">在 **创建库存日记帐** 对话框的 **仓库** 字段中，选择 *61*。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="6d4bb-320">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-320">Select **OK**.</span></span>
    1. <span data-ttu-id="6d4bb-321">在 **日记帐行** 快速选项卡中，使用 **新建** 按钮向网格添加三行，然后设置以下值。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="6d4bb-322">每行设置完毕之后，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="6d4bb-323">**行 1：**</span><span class="sxs-lookup"><span data-stu-id="6d4bb-323">**Line 1:**</span></span>

            - <span data-ttu-id="6d4bb-324">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="6d4bb-325">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-325">**Site:** *6*</span></span>
            - <span data-ttu-id="6d4bb-326">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="6d4bb-327">**货位**：*02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="6d4bb-328">**牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="6d4bb-329">**数量：** *1000*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="6d4bb-330">**行 2：**</span><span class="sxs-lookup"><span data-stu-id="6d4bb-330">**Line 2:**</span></span>

            - <span data-ttu-id="6d4bb-331">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="6d4bb-332">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-332">**Site:** *6*</span></span>
            - <span data-ttu-id="6d4bb-333">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="6d4bb-334">**货位**：*07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="6d4bb-335">**牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="6d4bb-336">**数量：** *15*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="6d4bb-337">**行 3：**</span><span class="sxs-lookup"><span data-stu-id="6d4bb-337">**Line 3:**</span></span>

            - <span data-ttu-id="6d4bb-338">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="6d4bb-339">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-339">**Site:** *6*</span></span>
            - <span data-ttu-id="6d4bb-340">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="6d4bb-341">**货位**：*07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="6d4bb-342">**牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="6d4bb-343">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="6d4bb-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="6d4bb-344">在操作窗格上，选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="6d4bb-345">前往下一步之前，解决发现的所有错误。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="6d4bb-346">在操作窗格上，选择 **过帐** 将库存过帐到仓库。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="6d4bb-347">示例场景：运行基于区域的最小/最大补货</span><span class="sxs-lookup"><span data-stu-id="6d4bb-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="6d4bb-348">准备好所有先决示例数据之后，可以执行以下步骤触发补货。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="6d4bb-349">转到 **仓库管理 \> 补货 \> 补货**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="6d4bb-350">在 **补货** 对话框的 **要包括的记录** 快速选项卡上，选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="6d4bb-351">在 **查询** 对话框的 **范围** 选项卡中，按照以下方式编辑默认表行：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="6d4bb-352">**表：** 选择 _补货模板_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="6d4bb-353">**派生表：** 选择 _补货模板_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="6d4bb-354">**字段：** 选择 _补货模板_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="6d4bb-355">**条件：** 选择 _区域最小/最大补货_。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="6d4bb-356">此补货模板是您在为此场景准备演示数据时创建的补货模板。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="6d4bb-357">选择 **确定** 保存查询并回到 **补货** 对话框。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="6d4bb-358">选择 **确定** 运行补货模板。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="6d4bb-359">现在已创建了补货工作，以便从 *BULK* 区域领取库存，然后将其补给 *FLOOR* 区域。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="6d4bb-360">说明和提示</span><span class="sxs-lookup"><span data-stu-id="6d4bb-360">Notes and tips</span></span>

<span data-ttu-id="6d4bb-361">下面是有关使用此功能的一些说明和提示：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="6d4bb-362">若要设置针对所需区域的补货工作，可以按照下面的一种方法链接补货模板行和货位指令：</span><span class="sxs-lookup"><span data-stu-id="6d4bb-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="6d4bb-363">编辑货位指令标题查询，然后筛选所选补货模板行。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="6d4bb-364">使用补货模板行中的指令代码，然后将其与放置货位指令比对。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="6d4bb-365">如果使用动态货位，并且将货位指令操作设置为使用 **合并** 策略，将为第一个可用货位或为已经包含库存的货位创建补货工作。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="6d4bb-366">如果使用固定货位而不是区域，则应使用[标准最小/最大补货](tasks/set-up-min-max-replenishment-process.md)。</span><span class="sxs-lookup"><span data-stu-id="6d4bb-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]