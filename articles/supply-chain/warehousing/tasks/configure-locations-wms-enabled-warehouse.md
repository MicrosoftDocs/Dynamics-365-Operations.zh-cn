---
title: 配置启用了 WMS 的仓库中的位置
description: 本指南会显示如何配置启用 WMS 的新仓库的位置设置（使用高级仓库管理流程的仓库）。
author: perlynne
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43fd5a293671d63c1c0db3019ba89fdf84f9fff8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146161"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="9a80b-103">配置启用了 WMS 的仓库中的位置</span><span class="sxs-lookup"><span data-stu-id="9a80b-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a80b-104">本指南会显示如何配置启用 WMS 的新仓库的位置设置（使用高级仓库管理流程的仓库）。</span><span class="sxs-lookup"><span data-stu-id="9a80b-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="9a80b-105">该流程通常由仓库经理完成。</span><span class="sxs-lookup"><span data-stu-id="9a80b-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="9a80b-106">您可以使用演示数据公司 USMF 或您自己的数据运行本指南。</span><span class="sxs-lookup"><span data-stu-id="9a80b-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9a80b-107">先决条件是您至少配置了一个站点。</span><span class="sxs-lookup"><span data-stu-id="9a80b-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="9a80b-108">新建仓库</span><span class="sxs-lookup"><span data-stu-id="9a80b-108">Create a new warehouse</span></span>
1. <span data-ttu-id="9a80b-109">转到**导航窗格 > 模块 > 库存管理 > 设置 > 库存细分 > 仓库**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="9a80b-110">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-110">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-111">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-111">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-112">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-113">在**站点**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-113">In the **Site** field, type a value.</span></span>
6. <span data-ttu-id="9a80b-114">展开**仓库**部分。</span><span class="sxs-lookup"><span data-stu-id="9a80b-114">Expand the **Warehouse** section.</span></span>
7. <span data-ttu-id="9a80b-115">将**使用仓库管理流程选项**设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="9a80b-115">Set the **Use warehouse management processes option** to Yes.</span></span> <span data-ttu-id="9a80b-116">此设置可使您使用仓库工作和移动设备运行高级仓储流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-116">This setting allows you to run advanced warehousing processes using warehouse work and mobile devices.</span></span>
8. <span data-ttu-id="9a80b-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="9a80b-118">定义位置格式</span><span class="sxs-lookup"><span data-stu-id="9a80b-118">Define a location format</span></span>
1. <span data-ttu-id="9a80b-119">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 位置格式**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-119">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse >Location formats**.</span></span> <span data-ttu-id="9a80b-120">位置格式是一个命名系统，用于为仓库内使用的不同位置箱位置创建一致的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="9a80b-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="9a80b-121">它对于使用分隔符作为位置格式的一部分，以更轻松地确定位置组件（例如通道编号）很有用。</span><span class="sxs-lookup"><span data-stu-id="9a80b-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="9a80b-122">在本示例中，我们将使用四个组件创建一个名称。</span><span class="sxs-lookup"><span data-stu-id="9a80b-122">In this example, we'll create a name with four components.</span></span> <span data-ttu-id="9a80b-123">例如，这些可能是通道、货架、搁架和储料箱。</span><span class="sxs-lookup"><span data-stu-id="9a80b-123">For example, these could be aisle, rack, shelf, and bin.</span></span>
2. <span data-ttu-id="9a80b-124">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-124">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-125">在**位置格式**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-125">In the **Location format** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-126">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-126">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-127">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-127">In the **Segment description** field, type a value.</span></span> <span data-ttu-id="9a80b-128">这描述位置名称的第一个组件代表什么。</span><span class="sxs-lookup"><span data-stu-id="9a80b-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="9a80b-129">例如，它可能是“通道”。</span><span class="sxs-lookup"><span data-stu-id="9a80b-129">For example, it could be 'Aisle'.</span></span>
6. <span data-ttu-id="9a80b-130">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-130">In the **Length** field, enter a number.</span></span> <span data-ttu-id="9a80b-131">这可以决定此部分的位置名称必须拥有多少个字符。</span><span class="sxs-lookup"><span data-stu-id="9a80b-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="9a80b-132">请注意，名称中所有组件的合计总数（包括分隔符）不得超过 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="9a80b-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>    
7. <span data-ttu-id="9a80b-133">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-133">In the **Separator** field, type a value.</span></span> <span data-ttu-id="9a80b-134">这可以决定名称的第一个和第二个组件之间使用哪个字符或符号。</span><span class="sxs-lookup"><span data-stu-id="9a80b-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="9a80b-135">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-135">In the **Details** section, click **New**.</span></span>
9. <span data-ttu-id="9a80b-136">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-136">In the **Segment description** field, type a value.</span></span>
10. <span data-ttu-id="9a80b-137">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-137">In the **Length** field, enter a number.</span></span>
11. <span data-ttu-id="9a80b-138">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-138">In the **Separator** field, type a value.</span></span>
12. <span data-ttu-id="9a80b-139">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-139">In the **Details** section, click **New**.</span></span>
13. <span data-ttu-id="9a80b-140">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-140">In the **Segment description** field, type a value.</span></span>
14. <span data-ttu-id="9a80b-141">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-141">In the **Length** field, enter a number.</span></span>
15. <span data-ttu-id="9a80b-142">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-142">In the **Separator** field, type a value.</span></span>
16. <span data-ttu-id="9a80b-143">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-143">In the **Details** section, click **New**.</span></span>
17. <span data-ttu-id="9a80b-144">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-144">In the **Segment description** field, type a value.</span></span>
18. <span data-ttu-id="9a80b-145">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-145">In the **Length** field, enter a number.</span></span>
19. <span data-ttu-id="9a80b-146">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-146">Click **Save**.</span></span>
20. <span data-ttu-id="9a80b-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="9a80b-148">定义位置类型</span><span class="sxs-lookup"><span data-stu-id="9a80b-148">Define location types</span></span>
1. <span data-ttu-id="9a80b-149">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 库位类型**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-149">Go to **Navigation pane > Modules > Warehouse management > setup > Warehouse > Location types**.</span></span> <span data-ttu-id="9a80b-150">位置类型可以用作筛选选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="9a80b-151">您至少需要创建暂存和最终装运位置类型，以便定义输出仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span> 
2. <span data-ttu-id="9a80b-152">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-152">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-153">在**库位**类型字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-153">In the **Location** type field, type a value.</span></span>
4. <span data-ttu-id="9a80b-154">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-154">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="9a80b-156">定义位置模板</span><span class="sxs-lookup"><span data-stu-id="9a80b-156">Define location profile</span></span>
1. <span data-ttu-id="9a80b-157">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 位置模板**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-157">Go to **Navigation pane > modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span> <span data-ttu-id="9a80b-158">位置模板的定义非常重要。</span><span class="sxs-lookup"><span data-stu-id="9a80b-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="9a80b-159">分组位置容量，以及存储哪些库存的测量和如何存储都可以在此进行控制。</span><span class="sxs-lookup"><span data-stu-id="9a80b-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="9a80b-160">位置模板可以用作筛选选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="9a80b-161">您至少必须创建用户位置模板，以便启用仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>
2. <span data-ttu-id="9a80b-162">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-162">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-163">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-163">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-164">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-164">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-165">在**位置格式**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-165">In the **Location format** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9a80b-166">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9a80b-167">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9a80b-168">在**库位类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-168">In the **Location type** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9a80b-169">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9a80b-170">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9a80b-171">选中或取消选中**允许混合库存状态**复选框。</span><span class="sxs-lookup"><span data-stu-id="9a80b-171">Select or clear the **Allow mixed inventory statuses** check box.</span></span> <span data-ttu-id="9a80b-172">启用此选项，如果您想要允许位置中的混合库存状态值将根据此位置模板进行分组。</span><span class="sxs-lookup"><span data-stu-id="9a80b-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span> 
12. <span data-ttu-id="9a80b-173">选中或取消选中**覆盖批处理天数的规则**复选框。</span><span class="sxs-lookup"><span data-stu-id="9a80b-173">Select or clear the **Override rules for batch days** check box.</span></span> <span data-ttu-id="9a80b-174">启用此选项，以覆写库存批次到期日期可以相差多少天的规则，以允许混合不遵守此规则的库存批次。</span><span class="sxs-lookup"><span data-stu-id="9a80b-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don't obeying this rule.</span></span>  
13. <span data-ttu-id="9a80b-175">选择或取消选择**允许周期盘点**复选框。</span><span class="sxs-lookup"><span data-stu-id="9a80b-175">Select or clear the **Allow cycle counting** check box.</span></span> <span data-ttu-id="9a80b-176">启用此选项，允许所有位置中的周期盘点处理将根据此位置模板进行分组。</span><span class="sxs-lookup"><span data-stu-id="9a80b-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span> 
14. <span data-ttu-id="9a80b-177">展开或折叠**维度**部分。</span><span class="sxs-lookup"><span data-stu-id="9a80b-177">Expand or collapse the **Dimensions** section.</span></span> <span data-ttu-id="9a80b-178">“维度”选项卡可使您定义参数和方法，以使每个位置中的容量负荷能够进行精确计算。</span><span class="sxs-lookup"><span data-stu-id="9a80b-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="9a80b-179">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="9a80b-180">启用仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="9a80b-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="9a80b-181">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-181">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span> <span data-ttu-id="9a80b-182">为了能够处理仓库工作，您需要设置用户位置模板的参数、暂存位置类型和最终装运位置类型。一旦输出流程在您定义的最终装运位置类型结束，相关的输出试图将被更新为“已领取”。</span><span class="sxs-lookup"><span data-stu-id="9a80b-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to "Picked".</span></span>
2. <span data-ttu-id="9a80b-183">展开**位置模板**部分。</span><span class="sxs-lookup"><span data-stu-id="9a80b-183">Expand the **Location profiles** section.</span></span>
3. <span data-ttu-id="9a80b-184">在**用户位置**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-184">In the **User location** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9a80b-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9a80b-186">展开**库位类型**部分。</span><span class="sxs-lookup"><span data-stu-id="9a80b-186">Expand the **Location types** section.</span></span>
6. <span data-ttu-id="9a80b-187">在**暂存位置类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-187">In the **Staging location type** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9a80b-188">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9a80b-189">在**最终装运位置类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-189">In the **Final shipping location type** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9a80b-190">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9a80b-191">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="9a80b-192">定义仓库区域组</span><span class="sxs-lookup"><span data-stu-id="9a80b-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="9a80b-193">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 仓库区域组**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-193">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Warehouse zone groups**.</span></span> <span data-ttu-id="9a80b-194">仓库区域可以用作筛选器选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9a80b-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="9a80b-195">在您能够定义区域之前，您需要创建区域组。</span><span class="sxs-lookup"><span data-stu-id="9a80b-195">You need to create a zone group before you can define a zone.</span></span>   
2. <span data-ttu-id="9a80b-196">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-196">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-197">在**区域组 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-197">In the **Zone group ID** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-198">在**区域组名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-198">In the **Zone group name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-199">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="9a80b-200">定义“仓库区域”</span><span class="sxs-lookup"><span data-stu-id="9a80b-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="9a80b-201">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 区域**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-201">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Zones**.</span></span>
2. <span data-ttu-id="9a80b-202">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-202">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-203">在**区域 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-203">In the **Zone ID** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-204">在**区域名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-204">In the **Zone name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-205">在**区域组 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-205">In the **Zone group ID** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9a80b-206">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9a80b-207">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9a80b-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="9a80b-209">使用位置设置向导创建位置</span><span class="sxs-lookup"><span data-stu-id="9a80b-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="9a80b-210">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 库位设置向导**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-210">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Location setup wizard**.</span></span>
2. <span data-ttu-id="9a80b-211">在**仓库**字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-211">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9a80b-212">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9a80b-213">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9a80b-214">在**区域 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-214">In the **Zone ID** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9a80b-215">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9a80b-216">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9a80b-217">在**位置模板 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-217">In the **Location profile ID** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9a80b-218">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9a80b-219">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9a80b-220">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9a80b-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9a80b-221">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-221">In the **From number** field, enter a number.</span></span> <span data-ttu-id="9a80b-222">“起始数字”和“截止数字”字段定义了要创建多少位置。</span><span class="sxs-lookup"><span data-stu-id="9a80b-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="9a80b-223">例如，如果您将位置格式中的全部四行的“起始数字”设置为 1，并将“截止数字”设置为 3，则会创建 81 个位置（3x3x3x3）。</span><span class="sxs-lookup"><span data-stu-id="9a80b-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>   
13. <span data-ttu-id="9a80b-224">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-224">In the **To number** field, enter a number.</span></span>
14. <span data-ttu-id="9a80b-225">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9a80b-226">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-226">In the **From number** field, enter a number.</span></span>
16. <span data-ttu-id="9a80b-227">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-227">In the **To number** field, enter a number.</span></span>
17. <span data-ttu-id="9a80b-228">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="9a80b-229">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-229">In the **From number** field, enter a number.</span></span>
19. <span data-ttu-id="9a80b-230">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-230">In the **To number** field, enter a number.</span></span>
20. <span data-ttu-id="9a80b-231">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a80b-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9a80b-232">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-232">In the **From number** field, enter a number.</span></span>
22. <span data-ttu-id="9a80b-233">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-233">In the **To number** field, enter a number.</span></span>
23. <span data-ttu-id="9a80b-234">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="9a80b-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="9a80b-235">手动创建位置</span><span class="sxs-lookup"><span data-stu-id="9a80b-235">Create locations manually</span></span>
1. <span data-ttu-id="9a80b-236">转到**仓库管理 > 设置 > 仓库 > 位置**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-236">Go to **Warehouse management > Setup > Warehouse > Locations**.</span></span> <span data-ttu-id="9a80b-237">可以轻松地在仓库内手动创建位置。</span><span class="sxs-lookup"><span data-stu-id="9a80b-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="9a80b-238">位置名称和“位置模板 ID”是必填值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-238">The location name and the location profile ID are mandatory values.</span></span> 
2. <span data-ttu-id="9a80b-239">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-239">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-240">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-240">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-241">在**位置**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-241">In the **Location** field, type a value.</span></span> <span data-ttu-id="9a80b-242">请注意，您正在此创建新位置，因此您需要键入一个新的唯一名称，而不是选择一个现有名称。</span><span class="sxs-lookup"><span data-stu-id="9a80b-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>
5. <span data-ttu-id="9a80b-243">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-243">In the **Location profile ID** field, type a value.</span></span>
6. <span data-ttu-id="9a80b-244">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="9a80b-245">定义“包装尺寸类别”</span><span class="sxs-lookup"><span data-stu-id="9a80b-245">Define Pack size categories</span></span>
1. <span data-ttu-id="9a80b-246">转到**仓库管理 > 设置 > 仓库 > 包装尺寸类别**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-246">Go to **Warehouse management > Setup > Warehouse > Pack size categories**.</span></span> <span data-ttu-id="9a80b-247">包装尺寸类别可用于对实际包装尺寸类似的物料进行分组。</span><span class="sxs-lookup"><span data-stu-id="9a80b-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="9a80b-248">在此示例中，包装尺寸类别将用于控制仓库特定区域中的领取位置容量。</span><span class="sxs-lookup"><span data-stu-id="9a80b-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="9a80b-249">请注意，必须给发布产品实体分配包装尺寸类别 ID，以便用作储存限值处理的一部分。</span><span class="sxs-lookup"><span data-stu-id="9a80b-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="9a80b-250">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-250">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-251">在**包装尺寸类别 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-251">In the **Pack size category ID** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-252">在**包装尺寸类别名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-252">In the **Pack size category name** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-253">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="9a80b-254">定义位置库存限制</span><span class="sxs-lookup"><span data-stu-id="9a80b-254">Define location stocking limits</span></span>
1. <span data-ttu-id="9a80b-255">转到**仓库管理 > 设置 > 仓库 > 位置库存限制**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-255">Go to **Warehouse management > Setup > Warehouse > Location stocking limits**.</span></span> <span data-ttu-id="9a80b-256">位置储存限值有助于确保未创建工作，以请求将库存存放到实际容量不足以容纳该库存的位置。</span><span class="sxs-lookup"><span data-stu-id="9a80b-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="9a80b-257">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-257">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-258">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-258">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-259">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-259">In the **Location profile ID** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-260">在**包装尺寸类别 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-260">In the **Pack size category ID** field, type a value.</span></span>
6. <span data-ttu-id="9a80b-261">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a80b-261">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="9a80b-262">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-262">Click **Save**.</span></span>
8. <span data-ttu-id="9a80b-263">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="9a80b-264">定义“固定领料位置”</span><span class="sxs-lookup"><span data-stu-id="9a80b-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="9a80b-265">转到**仓库管理 > 设置 > 仓库 > 固定位置**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-265">Go to **Warehouse management > Setup > Warehouse > Fixed locations**.</span></span> <span data-ttu-id="9a80b-266">您可以定义每个产品或每个产品变型使用的位置。</span><span class="sxs-lookup"><span data-stu-id="9a80b-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="9a80b-267">有可能为同一仓库中的同一产品创造多个固定位置。</span><span class="sxs-lookup"><span data-stu-id="9a80b-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>     
2. <span data-ttu-id="9a80b-268">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a80b-268">Click **New**.</span></span>
3. <span data-ttu-id="9a80b-269">在**项目编号**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-269">In the **Item number** field, type a value.</span></span>
4. <span data-ttu-id="9a80b-270">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a80b-270">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="9a80b-271">在**位置**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9a80b-271">In the **Location** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9a80b-272">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9a80b-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9a80b-273">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a80b-273">Close the page.</span></span>

