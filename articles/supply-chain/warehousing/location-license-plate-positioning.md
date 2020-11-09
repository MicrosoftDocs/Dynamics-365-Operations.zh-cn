---
title: 货位牌照定位
description: 货位牌照定位功能用于查看牌照在多托盘货位（如使用双深托盘货架的货位）中的位置。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017108"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="f8895-103">货位牌照定位</span><span class="sxs-lookup"><span data-stu-id="f8895-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8895-104">货位牌照定位功能用于查看牌照在多托盘货位（如使用双深托盘货架的货位）中的位置。</span><span class="sxs-lookup"><span data-stu-id="f8895-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="f8895-105">此功能为放入存储货位的每个牌照添加一个序列号。</span><span class="sxs-lookup"><span data-stu-id="f8895-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="f8895-106">此序列号用于为存储货位中的牌照排序。</span><span class="sxs-lookup"><span data-stu-id="f8895-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="f8895-107">因此，此功能智能支持以下场景：客户使用重力货架系统，并且出于领料目的，一定知道哪个牌照正面朝外。</span><span class="sxs-lookup"><span data-stu-id="f8895-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="f8895-108">本主题提供的场景显示如何设置和使用此功能。</span><span class="sxs-lookup"><span data-stu-id="f8895-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="f8895-109">开启“货位指令牌照定位”功能</span><span class="sxs-lookup"><span data-stu-id="f8895-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="f8895-110">牌照货位定位功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="f8895-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="f8895-111">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="f8895-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f8895-112">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="f8895-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f8895-113">**模块** ： *仓库管理*</span><span class="sxs-lookup"><span data-stu-id="f8895-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f8895-114">**功能名称** ： *货位牌照定位*</span><span class="sxs-lookup"><span data-stu-id="f8895-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f8895-115">示例场景</span><span class="sxs-lookup"><span data-stu-id="f8895-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="f8895-116">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="f8895-116">Make sample data available</span></span>

<span data-ttu-id="f8895-117">若要使用此处推荐的值完成此场景，使用的系统中必须已安装示例数据。</span><span class="sxs-lookup"><span data-stu-id="f8895-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="f8895-118">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="f8895-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="f8895-119">为此场景设置功能</span><span class="sxs-lookup"><span data-stu-id="f8895-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="f8895-120">完成以下过程为本主题中提供的场景设置 *货位牌照定位* 功能。</span><span class="sxs-lookup"><span data-stu-id="f8895-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="f8895-121">货位模板</span><span class="sxs-lookup"><span data-stu-id="f8895-121">Location profiles</span></span>

<span data-ttu-id="f8895-122">必须在要使用此功能的每个货位的货位模板中开启此功能。</span><span class="sxs-lookup"><span data-stu-id="f8895-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="f8895-123">转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="f8895-124">在左侧窗格的货位模板列表中，选择 **BULK-06** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="f8895-125">此功能已经在 **常规** 快速选项卡上添加了两个新选项。</span><span class="sxs-lookup"><span data-stu-id="f8895-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="f8895-126">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-126">Set the following values:</span></span>

    - <span data-ttu-id="f8895-127">**启用牌照位置** ： *是*</span><span class="sxs-lookup"><span data-stu-id="f8895-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="f8895-128">如果此选项设置为 *是* ，将保留牌照在货位中的牌照位置。</span><span class="sxs-lookup"><span data-stu-id="f8895-128">When this option is set to *Yes* , the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="f8895-129">**显示移动设备牌照定位** ： *是*</span><span class="sxs-lookup"><span data-stu-id="f8895-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="f8895-130">如果此选项设置为 *是* ，将在调整和盘点期间向移动设备用户显示牌照位置。</span><span class="sxs-lookup"><span data-stu-id="f8895-130">When this option is set to *Yes* , the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="f8895-131">只能在已开启了此功能时更改此选项的设置。</span><span class="sxs-lookup"><span data-stu-id="f8895-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="f8895-132">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="f8895-133">位置指令</span><span class="sxs-lookup"><span data-stu-id="f8895-133">Location directives</span></span>

1. <span data-ttu-id="f8895-134">转到 **库存管理 \> 设置 \> 位置指令** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f8895-135">在左侧窗格中，确保 **工作订单类型** 字段设置为 *销售订单* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="f8895-136">在货位指令列表中，选择 **61 SO 领料单** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="f8895-137">在操作窗格上，选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f8895-138">在 **行** 快速选项卡中，选择 **序列号** 值为 *2* 的行。</span><span class="sxs-lookup"><span data-stu-id="f8895-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="f8895-139">在 **货位指令操作** 快速选项卡上，选择 **名称** 值为 *不足托盘领料* 的行（这应该是唯一行），然后将其 **序列号** 值更改为 *2* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="f8895-140">选择网格上方的 **新建** 为新货位指令操作添加一行。</span><span class="sxs-lookup"><span data-stu-id="f8895-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="f8895-141">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f8895-142">**序列号** ： *1*</span><span class="sxs-lookup"><span data-stu-id="f8895-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="f8895-143">**名称** ： *领料位置 1*</span><span class="sxs-lookup"><span data-stu-id="f8895-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="f8895-144">在新行仍处于选中状态的情况下，选择网格上方的 **编辑查询** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="f8895-145">在查询编辑器中，选择 **联接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f8895-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="f8895-146">展开 **货位** 表联接显示 **库存维度** 表的联接。</span><span class="sxs-lookup"><span data-stu-id="f8895-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="f8895-147">展开 **库存维度** 表联接显示 **现有库存** 表的联接。</span><span class="sxs-lookup"><span data-stu-id="f8895-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="f8895-148">选择 **库存维度** ，然后选择 **添加表联接** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-148">Select **Inventory dimensions** , and then select **Add table join**.</span></span>
1. <span data-ttu-id="f8895-149">在显示的表列表的 **关系** 列中，选择 **牌照（牌照）** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="f8895-150">然后选择 **选择** 将 **牌照** 添加到 **库存维度** 表联接。</span><span class="sxs-lookup"><span data-stu-id="f8895-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="f8895-151">在 **牌照** 仍处于选中状态的情况下，选择 **添加表联接** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="f8895-152">在显示的表列表的 **关系** 列中，选择 **货位牌照定位（牌照）** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="f8895-153">然后选择 **选择** 将 **货位牌照定位** 添加到 **库存维度** 表联接。</span><span class="sxs-lookup"><span data-stu-id="f8895-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="f8895-154">![表联接](media/LpTableJoin.png "表联接")</span><span class="sxs-lookup"><span data-stu-id="f8895-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="f8895-155">选择 **确定** 确认更新后的联接表，然后关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="f8895-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="f8895-156">在 **位置指令操作** 快速选项卡上，再次选择 **编辑查询** 重新打开查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="f8895-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="f8895-157">在 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="f8895-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f8895-158">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f8895-159">**表** ： *货位牌照定位*</span><span class="sxs-lookup"><span data-stu-id="f8895-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="f8895-160">**派生表** ： *货位牌照定位*</span><span class="sxs-lookup"><span data-stu-id="f8895-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="f8895-161">**字段** ： *牌照定位*</span><span class="sxs-lookup"><span data-stu-id="f8895-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="f8895-162">**条件** ： *1*</span><span class="sxs-lookup"><span data-stu-id="f8895-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="f8895-163">![新范围](media/LpPositionCriteria.png "新范围")</span><span class="sxs-lookup"><span data-stu-id="f8895-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="f8895-164">选择 **确定** 确认范围，然后关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="f8895-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="f8895-165">为此场景设置示例数据</span><span class="sxs-lookup"><span data-stu-id="f8895-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="f8895-166">对于此场景，用户必须使用为仓库 *61* 设置的工作人员登录仓库移动应用，才能执行工作。</span><span class="sxs-lookup"><span data-stu-id="f8895-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="f8895-167">用户还必须完成事务。</span><span class="sxs-lookup"><span data-stu-id="f8895-167">The user must also complete transactions.</span></span>

<span data-ttu-id="f8895-168">因为 *货位牌照定位* 功能会在货位中为牌照位置添加一个新标识符，所以您首先必须创建一些数据来支持此场景。</span><span class="sxs-lookup"><span data-stu-id="f8895-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="f8895-169">盘点第一个货位</span><span class="sxs-lookup"><span data-stu-id="f8895-169">Spot-count the first location</span></span>

1. <span data-ttu-id="f8895-170">打开仓库移动应用，然后登录仓库 *61* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="f8895-171">转到 **库存 \> 盘点** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="f8895-172">在 **盘点** 页面中，将 **货位** 字段设置为 *01A01R1S1B* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="f8895-173">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-173">Select **OK**.</span></span>

    <span data-ttu-id="f8895-174">此页面将显示您输入的货位。</span><span class="sxs-lookup"><span data-stu-id="f8895-174">The page shows the location that you entered.</span></span> <span data-ttu-id="f8895-175">还会显示以下消息：“货位设置完成，是否添加新牌照或物料？”</span><span class="sxs-lookup"><span data-stu-id="f8895-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f8895-176">选择 **刷新** 在货位中添加计数。</span><span class="sxs-lookup"><span data-stu-id="f8895-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="f8895-177">在 **周期盘点：添加新牌照或物料** 页面中，选择 **物料** 字段，然后输入值 *A0001* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="f8895-178">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-178">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-179">在 **周期盘点：添加新牌照或物料** 页面中，选择 **牌照** 字段，然后输入值 *LP1001* （或您选择的其他任何牌照编号）。</span><span class="sxs-lookup"><span data-stu-id="f8895-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="f8895-180">**周期盘点：添加新牌照或物料** 页面将显示 **牌照位置 1** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="f8895-181">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-181">Select **OK**.</span></span>

    <span data-ttu-id="f8895-182">现在必须指定在牌照中盘点的物料数量。</span><span class="sxs-lookup"><span data-stu-id="f8895-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="f8895-183">将 **数量** 字段设置为 *10* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f8895-184">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-184">Select **OK**.</span></span>

    <span data-ttu-id="f8895-185">此页面将显示您输入的货位。</span><span class="sxs-lookup"><span data-stu-id="f8895-185">The page shows the location that you entered.</span></span> <span data-ttu-id="f8895-186">还会显示以下消息：“货位设置完成，是否添加新牌照或物料？”</span><span class="sxs-lookup"><span data-stu-id="f8895-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f8895-187">选择 **刷新** 在货位中再添加一个计数。</span><span class="sxs-lookup"><span data-stu-id="f8895-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="f8895-188">在 **周期盘点：添加新牌照或物料** 页面中，选择 **物料** 字段，然后输入值 *A0002* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="f8895-189">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-189">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-190">在 **周期盘点：添加新牌照或物料** 页面中，选择 **牌照** 字段，然后输入值 *LP1002* （或您选择的其他任何牌照编号，前提是该编号与前面指定的牌照编号不同）。</span><span class="sxs-lookup"><span data-stu-id="f8895-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="f8895-191">将 **牌照位置** 字段更改为 *2* 来更改牌照位置。</span><span class="sxs-lookup"><span data-stu-id="f8895-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="f8895-192">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-192">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-193">通过将 **数量** 字段设置为 *10* 指定在牌照中盘点的物料数量。</span><span class="sxs-lookup"><span data-stu-id="f8895-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f8895-194">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-194">Select **OK**.</span></span>

    <span data-ttu-id="f8895-195">此页面将显示您输入的货位。</span><span class="sxs-lookup"><span data-stu-id="f8895-195">The page shows the location that you entered.</span></span> <span data-ttu-id="f8895-196">还会显示以下消息：“货位设置完成，是否添加新牌照或物料？”</span><span class="sxs-lookup"><span data-stu-id="f8895-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f8895-197">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-197">Select **OK**.</span></span>

<span data-ttu-id="f8895-198">工作现在已完成。</span><span class="sxs-lookup"><span data-stu-id="f8895-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="f8895-199">盘点第二个货位</span><span class="sxs-lookup"><span data-stu-id="f8895-199">Spot-count the second location</span></span>

1. <span data-ttu-id="f8895-200">在 **盘点** 页面中，将 **货位** 字段设置为 *01A01R1S2B* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="f8895-201">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-201">Select **OK**.</span></span>

    <span data-ttu-id="f8895-202">此页面将显示您输入的货位。</span><span class="sxs-lookup"><span data-stu-id="f8895-202">The page shows the location that you entered.</span></span> <span data-ttu-id="f8895-203">还会显示以下消息：“货位设置完成，是否添加新牌照或物料？”</span><span class="sxs-lookup"><span data-stu-id="f8895-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f8895-204">选择 **刷新** 在货位中添加计数。</span><span class="sxs-lookup"><span data-stu-id="f8895-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="f8895-205">在 **周期盘点：添加新牌照或物料** 页面中，选择 **物料** 字段，然后输入值 *A0002* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="f8895-206">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-206">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-207">在 **周期盘点：添加新牌照或物料** 页面中，选择 **牌照** 字段，然后输入值 *LP1003* （或您选择的其他任何牌照编号，前提是该编号与上一过程中指定的两个牌照编号不同）。</span><span class="sxs-lookup"><span data-stu-id="f8895-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="f8895-208">**周期盘点：添加新牌照或物料** 页面将显示 **牌照位置 1** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="f8895-209">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-209">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-210">通过将 **数量** 字段设置为 *10* 指定在牌照中盘点的物料数量。</span><span class="sxs-lookup"><span data-stu-id="f8895-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f8895-211">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-211">Select **OK**.</span></span>

    <span data-ttu-id="f8895-212">此页面将显示您输入的货位。</span><span class="sxs-lookup"><span data-stu-id="f8895-212">The page shows the location that you entered.</span></span> <span data-ttu-id="f8895-213">还会显示以下消息：“货位设置完成，是否添加新牌照或物料？”</span><span class="sxs-lookup"><span data-stu-id="f8895-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f8895-214">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-214">Select **OK**.</span></span>

<span data-ttu-id="f8895-215">工作现在已完成。</span><span class="sxs-lookup"><span data-stu-id="f8895-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="f8895-216">工作详细信息</span><span class="sxs-lookup"><span data-stu-id="f8895-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="f8895-217">从移动应用盘点会在 Microsoft Dynamics 365 中创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="f8895-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="f8895-218">该工作要求先接受盘点，才能将其过帐到库存。</span><span class="sxs-lookup"><span data-stu-id="f8895-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="f8895-219">登录 Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="f8895-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="f8895-220">转到 **仓库管理 \> 工作 \> 工作详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="f8895-221">在 **概览** 选项卡上，查找具有以下值的行：</span><span class="sxs-lookup"><span data-stu-id="f8895-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="f8895-222">**工作订单类型** ： *周期盘点*</span><span class="sxs-lookup"><span data-stu-id="f8895-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="f8895-223">**仓库** ： *61*</span><span class="sxs-lookup"><span data-stu-id="f8895-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f8895-224">**工作状态** ： *待核查*</span><span class="sxs-lookup"><span data-stu-id="f8895-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="f8895-225">应该已经为这些行创建了两个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="f8895-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="f8895-226">必须接受这些工作 ID 的盘点。</span><span class="sxs-lookup"><span data-stu-id="f8895-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="f8895-227">在网格中，选择 *周期盘点* 工作订单类型的第一个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="f8895-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="f8895-228">在操作窗格 **工作** 选项卡上的 **工作** 组中，选择 **周期盘点** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="f8895-229">将显示两行，每个物料和牌照一行。</span><span class="sxs-lookup"><span data-stu-id="f8895-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="f8895-230">**盘点数量** 、 **货位** 、 **牌照** 和 **物料** 字段中的值应该与您在移动设备中创建的盘点条目匹配。</span><span class="sxs-lookup"><span data-stu-id="f8895-230">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="f8895-231">如果不显示这些字段中的任何一个，请选择操作窗格上的 **显示维度** 将其添加到网格。</span><span class="sxs-lookup"><span data-stu-id="f8895-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="f8895-232">选择这两行。</span><span class="sxs-lookup"><span data-stu-id="f8895-232">Select both lines.</span></span>
1. <span data-ttu-id="f8895-233">在操作窗格上，选择 **接受盘点** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="f8895-234">将收到“正在过帐 - 日记帐”消息。</span><span class="sxs-lookup"><span data-stu-id="f8895-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="f8895-235">选择 **消息详细信息** 查看过帐的日记帐编号。</span><span class="sxs-lookup"><span data-stu-id="f8895-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="f8895-236">关闭消息详细信息。</span><span class="sxs-lookup"><span data-stu-id="f8895-236">Close the message details.</span></span>
1. <span data-ttu-id="f8895-237">刷新 **工作** 页面。</span><span class="sxs-lookup"><span data-stu-id="f8895-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="f8895-238">第一个工作 ID 已关闭，并且不再显示。</span><span class="sxs-lookup"><span data-stu-id="f8895-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="f8895-239">若要查看已关闭的工作，请选中网格上方的 **显示已关闭** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="f8895-240">现在将接受 *01A01R1S2B* 货位中的牌照的工作。</span><span class="sxs-lookup"><span data-stu-id="f8895-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="f8895-241">在 **概览** 选项卡上，选择 *周期盘点* 工作订单类型的第二个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="f8895-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="f8895-242">在操作窗格 **工作** 选项卡上的 **工作** 组中，选择 **周期盘点** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="f8895-243">将为物料和牌照显示一行。</span><span class="sxs-lookup"><span data-stu-id="f8895-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="f8895-244">**盘点数量** 、 **货位** 、 **牌照** 和 **物料** 字段中的值应该与您在移动设备中创建的盘点条目匹配。</span><span class="sxs-lookup"><span data-stu-id="f8895-244">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="f8895-245">选择该行。</span><span class="sxs-lookup"><span data-stu-id="f8895-245">Select the line.</span></span>
1. <span data-ttu-id="f8895-246">在操作窗格上，选择 **接受盘点** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="f8895-247">将收到“正在过帐 - 日记帐”消息。</span><span class="sxs-lookup"><span data-stu-id="f8895-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="f8895-248">选择 **消息详细信息** 查看过帐的日记帐编号。</span><span class="sxs-lookup"><span data-stu-id="f8895-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="f8895-249">关闭消息详细信息。</span><span class="sxs-lookup"><span data-stu-id="f8895-249">Close the message details.</span></span>
1. <span data-ttu-id="f8895-250">刷新 **工作** 页面。</span><span class="sxs-lookup"><span data-stu-id="f8895-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="f8895-251">第二个工作 ID 已关闭，并且不再显示。</span><span class="sxs-lookup"><span data-stu-id="f8895-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="f8895-252">若要查看已关闭的工作，请选中网格上方的 **显示已关闭** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="f8895-253">按货位显示的现有量</span><span class="sxs-lookup"><span data-stu-id="f8895-253">On-hand by location</span></span>

1. <span data-ttu-id="f8895-254">转到 **仓库管理 \> 查询和报表 \> 现有货位** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="f8895-255">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-255">Set the following values:</span></span>

    - <span data-ttu-id="f8895-256">**站点** ： *6*</span><span class="sxs-lookup"><span data-stu-id="f8895-256">**Site:** *6*</span></span>
    - <span data-ttu-id="f8895-257">**仓库** ： *61*</span><span class="sxs-lookup"><span data-stu-id="f8895-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f8895-258">**跨货位刷新** ： *是*</span><span class="sxs-lookup"><span data-stu-id="f8895-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="f8895-259">请注意，货位 *01A01R1S1B* 有两个牌照：</span><span class="sxs-lookup"><span data-stu-id="f8895-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="f8895-260">**A0001** ，其中的 **牌照位置** 字段设置为 *1*</span><span class="sxs-lookup"><span data-stu-id="f8895-260">**A0001** , where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="f8895-261">**A0002** ，其中的 **牌照位置** 字段设置为 *2*</span><span class="sxs-lookup"><span data-stu-id="f8895-261">**A0002** , where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="f8895-262">请注意，货位 *01A01R1S2B* 有一个牌照：</span><span class="sxs-lookup"><span data-stu-id="f8895-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="f8895-263">**A0002** ，其中的 **牌照位置** 字段设置为 *1*</span><span class="sxs-lookup"><span data-stu-id="f8895-263">**A0002** , where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="f8895-264">销售订单场景</span><span class="sxs-lookup"><span data-stu-id="f8895-264">Sales order scenario</span></span>

<span data-ttu-id="f8895-265">现在已经设置了 *货位牌照定位* 功能，并且已暂存了库存，所以必须创建销售订单以生成领料工作来指导仓库工作人员从托盘 ID 位于货位 *1* 的库存货位中领取物料 *A0002* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="f8895-266">转到 **销售和营销 \> 销售订单 \> 所有销售订单** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f8895-267">在操作窗格上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f8895-268">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f8895-269">**客户帐户** ： *US-004*</span><span class="sxs-lookup"><span data-stu-id="f8895-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="f8895-270">**仓库** ： *61*</span><span class="sxs-lookup"><span data-stu-id="f8895-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="f8895-271">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-271">Select **OK**.</span></span>
1. <span data-ttu-id="f8895-272">将向 **销售订单行** 快速选项卡中的网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="f8895-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f8895-273">在这个新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f8895-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="f8895-274">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="f8895-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f8895-275">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="f8895-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="f8895-276">在网格上方的 **库存** 菜单中，选择 **预留** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f8895-277">在 **预留** 页面的操作窗格中，选择 **预留批次** 为订单行预留库存。</span><span class="sxs-lookup"><span data-stu-id="f8895-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="f8895-278">关闭 **预留** 页面。</span><span class="sxs-lookup"><span data-stu-id="f8895-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="f8895-279">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f8895-280">您将收到指示为订单创建的波次 ID 和装运 ID 的参考消息。</span><span class="sxs-lookup"><span data-stu-id="f8895-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="f8895-281">在 **销售订单行** 快速选项卡上网格上方的 **仓库** 菜单中，选择 **工作详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="f8895-282">将显示 **工作** 页面，其中显示为销售行创建的工作。</span><span class="sxs-lookup"><span data-stu-id="f8895-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="f8895-283">记下显示的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="f8895-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="f8895-284">销售领料场景</span><span class="sxs-lookup"><span data-stu-id="f8895-284">Sales picking scenario</span></span>

1. <span data-ttu-id="f8895-285">打开移动应用，然后登录仓库 *61* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="f8895-286">转到 **出库 \> 销售领料** 。</span><span class="sxs-lookup"><span data-stu-id="f8895-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="f8895-287">在 **扫描工作 ID/牌照 ID** 页面中，选择 **ID** 字段，然后输入销售行中的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="f8895-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="f8895-288">请注意，领料工作将指示您从货位 *01A01R1S2B* 领物料 *A0002* 。</span><span class="sxs-lookup"><span data-stu-id="f8895-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="f8895-289">您收到此指示是因为，物料 *A0002* 所在牌照位于该货位的位置 *1* 中。</span><span class="sxs-lookup"><span data-stu-id="f8895-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="f8895-290">![位置 1 货位](media/LocationLicensePlatePositioning.png "位置 1 货位")</span><span class="sxs-lookup"><span data-stu-id="f8895-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="f8895-291">输入您为该货位创建的牌照 ID，然后按照提示为销售订单领料。</span><span class="sxs-lookup"><span data-stu-id="f8895-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
