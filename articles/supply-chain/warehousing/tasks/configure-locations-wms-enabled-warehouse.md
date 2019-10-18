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
ms.openlocfilehash: fca4d8673ef7ccb00bc1b216fbe7d56acc2ff142
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2019
ms.locfileid: "1994973"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="9b22a-103">配置启用了 WMS 的仓库中的位置</span><span class="sxs-lookup"><span data-stu-id="9b22a-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b22a-104">本指南会显示如何配置启用 WMS 的新仓库的位置设置（使用高级仓库管理流程的仓库）。</span><span class="sxs-lookup"><span data-stu-id="9b22a-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="9b22a-105">该流程通常由仓库经理完成。</span><span class="sxs-lookup"><span data-stu-id="9b22a-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="9b22a-106">您可以使用演示数据公司 USMF 或您自己的数据运行本指南。</span><span class="sxs-lookup"><span data-stu-id="9b22a-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9b22a-107">先决条件是您至少配置了一个站点。</span><span class="sxs-lookup"><span data-stu-id="9b22a-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="9b22a-108">新建仓库</span><span class="sxs-lookup"><span data-stu-id="9b22a-108">Create a new warehouse</span></span>
1. <span data-ttu-id="9b22a-109">转到**导航窗格 > 模块 > 库存管理 > 设置 > 库存细分 > 仓库**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="9b22a-110">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-110">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-111">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-111">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-112">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-113">在**站点**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-113">In the **Site** field, type a value.</span></span>
6. <span data-ttu-id="9b22a-114">展开**仓库**部分。</span><span class="sxs-lookup"><span data-stu-id="9b22a-114">Expand the **Warehouse** section.</span></span>
7. <span data-ttu-id="9b22a-115">将**使用仓库管理流程选项**设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="9b22a-115">Set the **Use warehouse management processes option** to Yes.</span></span> <span data-ttu-id="9b22a-116">此设置可使您使用仓库工作和移动设备运行高级仓储流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-116">This setting allows you to run advanced warehousing processes using warehouse work and mobile devices.</span></span>
8. <span data-ttu-id="9b22a-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="9b22a-118">定义位置格式</span><span class="sxs-lookup"><span data-stu-id="9b22a-118">Define a location format</span></span>
1. <span data-ttu-id="9b22a-119">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 位置格式**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-119">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse >Location formats**.</span></span> <span data-ttu-id="9b22a-120">位置格式是一个命名系统，用于为仓库内使用的不同位置箱位置创建一致的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="9b22a-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="9b22a-121">它对于使用分隔符作为位置格式的一部分，以更轻松地确定位置组件（例如通道编号）很有用。</span><span class="sxs-lookup"><span data-stu-id="9b22a-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="9b22a-122">在本示例中，我们将使用四个组件创建一个名称。</span><span class="sxs-lookup"><span data-stu-id="9b22a-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="9b22a-123">例如，这些可能是通道、货架、搁架和储料箱。</span><span class="sxs-lookup"><span data-stu-id="9b22a-123">For example, these could be aisle, rack, shelf, and bin.</span></span>
2. <span data-ttu-id="9b22a-124">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-124">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-125">在**位置格式**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-125">In the **Location format** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-126">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-126">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-127">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-127">In the **Segment description** field, type a value.</span></span> <span data-ttu-id="9b22a-128">这描述位置名称的第一个组件代表什么。</span><span class="sxs-lookup"><span data-stu-id="9b22a-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="9b22a-129">例如，它可能是“通道”。</span><span class="sxs-lookup"><span data-stu-id="9b22a-129">For example, it could be 'Aisle'.</span></span>
6. <span data-ttu-id="9b22a-130">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-130">In the **Length** field, enter a number.</span></span> <span data-ttu-id="9b22a-131">这可以决定此部分的位置名称必须拥有多少个字符。</span><span class="sxs-lookup"><span data-stu-id="9b22a-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="9b22a-132">请注意，名称中所有组件的合计总数（包括分隔符）不得超过 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="9b22a-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>    
7. <span data-ttu-id="9b22a-133">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-133">In the **Separator** field, type a value.</span></span> <span data-ttu-id="9b22a-134">这可以决定名称的第一个和第二个组件之间使用哪个字符或符号。</span><span class="sxs-lookup"><span data-stu-id="9b22a-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="9b22a-135">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-135">In the **Details** section, click **New**.</span></span>
9. <span data-ttu-id="9b22a-136">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-136">In the **Segment description** field, type a value.</span></span>
10. <span data-ttu-id="9b22a-137">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-137">In the **Length** field, enter a number.</span></span>
11. <span data-ttu-id="9b22a-138">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-138">In the **Separator** field, type a value.</span></span>
12. <span data-ttu-id="9b22a-139">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-139">In the **Details** section, click **New**.</span></span>
13. <span data-ttu-id="9b22a-140">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-140">In the **Segment description** field, type a value.</span></span>
14. <span data-ttu-id="9b22a-141">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-141">In the **Length** field, enter a number.</span></span>
15. <span data-ttu-id="9b22a-142">在**分隔符**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-142">In the **Separator** field, type a value.</span></span>
16. <span data-ttu-id="9b22a-143">在**详细信息**部分中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-143">In the **Details** section, click **New**.</span></span>
17. <span data-ttu-id="9b22a-144">在**节段描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-144">In the **Segment description** field, type a value.</span></span>
18. <span data-ttu-id="9b22a-145">在**长度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-145">In the **Length** field, enter a number.</span></span>
19. <span data-ttu-id="9b22a-146">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-146">Click **Save**.</span></span>
20. <span data-ttu-id="9b22a-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="9b22a-148">定义位置类型</span><span class="sxs-lookup"><span data-stu-id="9b22a-148">Define location types</span></span>
1. <span data-ttu-id="9b22a-149">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 库位类型**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-149">Go to **Navigation pane > Modules > Warehouse management > setup > Warehouse > Location types**.</span></span> <span data-ttu-id="9b22a-150">位置类型可以用作筛选选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="9b22a-151">您至少需要创建暂存和最终装运位置类型，以便定义输出仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span> 
2. <span data-ttu-id="9b22a-152">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-152">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-153">在**库位**类型字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-153">In the **Location** type field, type a value.</span></span>
4. <span data-ttu-id="9b22a-154">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-154">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="9b22a-156">定义位置模板</span><span class="sxs-lookup"><span data-stu-id="9b22a-156">Define location profile</span></span>
1. <span data-ttu-id="9b22a-157">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 位置模板**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-157">Go to **Navigation pane > modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span> <span data-ttu-id="9b22a-158">位置模板的定义非常重要。</span><span class="sxs-lookup"><span data-stu-id="9b22a-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="9b22a-159">分组位置容量，以及存储哪些库存的测量和如何存储都可以在此进行控制。</span><span class="sxs-lookup"><span data-stu-id="9b22a-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="9b22a-160">位置模板可以用作筛选选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="9b22a-161">您至少必须创建用户位置模板，以便启用仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>
2. <span data-ttu-id="9b22a-162">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-162">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-163">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-163">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-164">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-164">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-165">在**位置格式**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-165">In the **Location format** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b22a-166">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b22a-167">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b22a-168">在**库位类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-168">In the **Location type** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9b22a-169">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9b22a-170">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9b22a-171">选中或取消选中**允许混合库存状态**复选框。</span><span class="sxs-lookup"><span data-stu-id="9b22a-171">Select or clear the **Allow mixed inventory statuses** check box.</span></span> <span data-ttu-id="9b22a-172">启用此选项，如果您想要允许位置中的混合库存状态值将根据此位置模板进行分组。</span><span class="sxs-lookup"><span data-stu-id="9b22a-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span> 
12. <span data-ttu-id="9b22a-173">选中或取消选中**覆盖批处理天数的规则**复选框。</span><span class="sxs-lookup"><span data-stu-id="9b22a-173">Select or clear the **Override rules for batch days** check box.</span></span> <span data-ttu-id="9b22a-174">启用此选项，以覆写库存批次到期日期可以相差多少天的规则，以允许混合不遵守此规则的库存批次。</span><span class="sxs-lookup"><span data-stu-id="9b22a-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="9b22a-175">选择或取消选择**允许周期盘点**复选框。</span><span class="sxs-lookup"><span data-stu-id="9b22a-175">Select or clear the **Allow cycle counting** check box.</span></span> <span data-ttu-id="9b22a-176">启用此选项，允许所有位置中的周期盘点处理将根据此位置模板进行分组。</span><span class="sxs-lookup"><span data-stu-id="9b22a-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span> 
14. <span data-ttu-id="9b22a-177">展开或折叠**维度**部分。</span><span class="sxs-lookup"><span data-stu-id="9b22a-177">Expand or collapse the **Dimensions** section.</span></span> <span data-ttu-id="9b22a-178">“维度”选项卡可使您定义参数和方法，以使每个位置中的容量负荷能够进行精确计算。</span><span class="sxs-lookup"><span data-stu-id="9b22a-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="9b22a-179">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="9b22a-180">启用仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="9b22a-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="9b22a-181">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-181">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span> <span data-ttu-id="9b22a-182">为了能够处理仓库工作，您需要设置用户位置模板的参数、暂存位置类型和最终装运位置类型。一旦输出流程在您定义的最终装运位置类型结束，相关的输出试图将被更新为“已领取”。</span><span class="sxs-lookup"><span data-stu-id="9b22a-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to "Picked".</span></span>
2. <span data-ttu-id="9b22a-183">展开**位置模板**部分。</span><span class="sxs-lookup"><span data-stu-id="9b22a-183">Expand the **Location profiles** section.</span></span>
3. <span data-ttu-id="9b22a-184">在**用户位置**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-184">In the **User location** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9b22a-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9b22a-186">展开**库位类型**部分。</span><span class="sxs-lookup"><span data-stu-id="9b22a-186">Expand the **Location types** section.</span></span>
6. <span data-ttu-id="9b22a-187">在**暂存位置类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-187">In the **Staging location type** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9b22a-188">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b22a-189">在**最终装运位置类型**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-189">In the **Final shipping location type** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9b22a-190">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9b22a-191">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="9b22a-192">定义仓库区域组</span><span class="sxs-lookup"><span data-stu-id="9b22a-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="9b22a-193">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 仓库区域组**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-193">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Warehouse zone groups**.</span></span> <span data-ttu-id="9b22a-194">仓库区域可以用作筛选器选项，以控制不同的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="9b22a-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="9b22a-195">在您能够定义区域之前，您需要创建区域组。</span><span class="sxs-lookup"><span data-stu-id="9b22a-195">You need to create a zone group before you can define a zone.</span></span>   
2. <span data-ttu-id="9b22a-196">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-196">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-197">在**区域组 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-197">In the **Zone group ID** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-198">在**区域组名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-198">In the **Zone group name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-199">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="9b22a-200">定义“仓库区域”</span><span class="sxs-lookup"><span data-stu-id="9b22a-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="9b22a-201">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 区域**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-201">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Zones**.</span></span>
2. <span data-ttu-id="9b22a-202">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-202">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-203">在**区域 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-203">In the **Zone ID** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-204">在**区域名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-204">In the **Zone name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-205">在**区域组 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-205">In the **Zone group ID** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b22a-206">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b22a-207">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b22a-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="9b22a-209">使用位置设置向导创建位置</span><span class="sxs-lookup"><span data-stu-id="9b22a-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="9b22a-210">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库 > 库位设置向导**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-210">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse > Location setup wizard**.</span></span>
2. <span data-ttu-id="9b22a-211">在**仓库**字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-211">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9b22a-212">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9b22a-213">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9b22a-214">在**区域 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-214">In the **Zone ID** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b22a-215">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b22a-216">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b22a-217">在**位置模板 ID** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-217">In the **Location profile ID** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9b22a-218">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9b22a-219">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9b22a-220">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9b22a-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9b22a-221">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-221">In the **From number** field, enter a number.</span></span> <span data-ttu-id="9b22a-222">“起始数字”和“截止数字”字段定义了要创建多少位置。</span><span class="sxs-lookup"><span data-stu-id="9b22a-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="9b22a-223">例如，如果您将位置格式中的全部四行的“起始数字”设置为 1，并将“截止数字”设置为 3，则会创建 81 个位置（3x3x3x3）。</span><span class="sxs-lookup"><span data-stu-id="9b22a-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>   
13. <span data-ttu-id="9b22a-224">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-224">In the **To number** field, enter a number.</span></span>
14. <span data-ttu-id="9b22a-225">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9b22a-226">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-226">In the **From number** field, enter a number.</span></span>
16. <span data-ttu-id="9b22a-227">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-227">In the **To number** field, enter a number.</span></span>
17. <span data-ttu-id="9b22a-228">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="9b22a-229">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-229">In the **From number** field, enter a number.</span></span>
19. <span data-ttu-id="9b22a-230">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-230">In the **To number** field, enter a number.</span></span>
20. <span data-ttu-id="9b22a-231">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b22a-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9b22a-232">在**起始数值**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-232">In the **From number** field, enter a number.</span></span>
22. <span data-ttu-id="9b22a-233">在**截止数字**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-233">In the **To number** field, enter a number.</span></span>
23. <span data-ttu-id="9b22a-234">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="9b22a-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="9b22a-235">手动创建位置</span><span class="sxs-lookup"><span data-stu-id="9b22a-235">Create locations manually</span></span>
1. <span data-ttu-id="9b22a-236">转到**仓库管理 > 设置 > 仓库 > 位置**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-236">Go to **Warehouse management > Setup > Warehouse > Locations**.</span></span> <span data-ttu-id="9b22a-237">可以轻松地在仓库内手动创建位置。</span><span class="sxs-lookup"><span data-stu-id="9b22a-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="9b22a-238">位置名称和“位置模板 ID”是必填值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-238">The location name and the location profile ID are mandatory values.</span></span> 
2. <span data-ttu-id="9b22a-239">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-239">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-240">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-240">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-241">在**位置**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-241">In the **Location** field, type a value.</span></span> <span data-ttu-id="9b22a-242">请注意，您正在此创建新位置，因此您需要键入一个新的唯一名称，而不是选择一个现有名称。</span><span class="sxs-lookup"><span data-stu-id="9b22a-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>
5. <span data-ttu-id="9b22a-243">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-243">In the **Location profile ID** field, type a value.</span></span>
6. <span data-ttu-id="9b22a-244">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="9b22a-245">定义“包装尺寸类别”</span><span class="sxs-lookup"><span data-stu-id="9b22a-245">Define Pack size categories</span></span>
1. <span data-ttu-id="9b22a-246">转到**仓库管理 > 设置 > 仓库 > 包装尺寸类别**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-246">Go to **Warehouse management > Setup > Warehouse > Pack size categories**.</span></span> <span data-ttu-id="9b22a-247">包装尺寸类别可用于对实际包装尺寸类似的物料进行分组。</span><span class="sxs-lookup"><span data-stu-id="9b22a-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="9b22a-248">在此示例中，包装尺寸类别将用于控制仓库特定区域中的领取位置容量。</span><span class="sxs-lookup"><span data-stu-id="9b22a-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="9b22a-249">请注意，必须给发布产品实体分配包装尺寸类别 ID，以便用作储存限值处理的一部分。</span><span class="sxs-lookup"><span data-stu-id="9b22a-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="9b22a-250">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-250">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-251">在**包装尺寸类别 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-251">In the **Pack size category ID** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-252">在**包装尺寸类别名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-252">In the **Pack size category name** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-253">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="9b22a-254">定义位置库存限制</span><span class="sxs-lookup"><span data-stu-id="9b22a-254">Define location stocking limits</span></span>
1. <span data-ttu-id="9b22a-255">转到**仓库管理 > 设置 > 仓库 > 位置库存限制**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-255">Go to **Warehouse management > Setup > Warehouse > Location stocking limits**.</span></span> <span data-ttu-id="9b22a-256">位置储存限值有助于确保未创建工作，以请求将库存存放到实际容量不足以容纳该库存的位置。</span><span class="sxs-lookup"><span data-stu-id="9b22a-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="9b22a-257">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-257">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-258">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-258">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-259">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-259">In the **Location profile ID** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-260">在**包装尺寸类别 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-260">In the **Pack size category ID** field, type a value.</span></span>
6. <span data-ttu-id="9b22a-261">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9b22a-261">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="9b22a-262">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-262">Click **Save**.</span></span>
8. <span data-ttu-id="9b22a-263">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="9b22a-264">定义“固定领料位置”</span><span class="sxs-lookup"><span data-stu-id="9b22a-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="9b22a-265">转到**仓库管理 > 设置 > 仓库 > 固定位置**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-265">Go to **Warehouse management > Setup > Warehouse > Fixed locations**.</span></span> <span data-ttu-id="9b22a-266">您可以定义每个产品或每个产品变型使用的位置。</span><span class="sxs-lookup"><span data-stu-id="9b22a-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="9b22a-267">有可能为同一仓库中的同一产品创造多个固定位置。</span><span class="sxs-lookup"><span data-stu-id="9b22a-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>     
2. <span data-ttu-id="9b22a-268">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b22a-268">Click **New**.</span></span>
3. <span data-ttu-id="9b22a-269">在**项目编号**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-269">In the **Item number** field, type a value.</span></span>
4. <span data-ttu-id="9b22a-270">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b22a-270">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="9b22a-271">在**位置**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b22a-271">In the **Location** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b22a-272">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b22a-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9b22a-273">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b22a-273">Close the page.</span></span>

