---
title: 系统导向工作先后顺序
description: 本主题提供有关系统导向工作先后顺序的信息。 此功能用于对系统提供给用户执行的工作订单排序和筛选。 其在以下场景中很有帮助：需要更多条件才能推动仓库领料流程。
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017015"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="5ceeb-105">系统导向工作先后顺序</span><span class="sxs-lookup"><span data-stu-id="5ceeb-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ceeb-106">系统导向工作先后顺序功能用于对系统提供给用户执行的工作订单排序和筛选。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="5ceeb-107">其在以下场景中很有帮助：需要更多条件（如装运时间、领料区、货位模板或各种条件的组合）来推动仓库领料流程。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="5ceeb-108">此功能通过添加系统导向查询订单扩展现在的系统导向领料功能，因此，用户可以设置序列和一个或多个查询来评估创建的所有工作订单。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="5ceeb-109">将仅捕获和提供满足移动设备菜单项的设置中指定的条件的工作订单。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="5ceeb-110">因此，可通过此功能基于特定技能集、领料设备或其他要求进一步优化仓库领料流程，因为其可识别满足指定条件的工作订单，将其分配给正确的移动设备菜单项，然后将其提供给工作人员。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="5ceeb-111">如果需要其他条件，必须使用多个移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="5ceeb-112">开启组织范围的系统导向工作先后顺序功能</span><span class="sxs-lookup"><span data-stu-id="5ceeb-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="5ceeb-113">系统导向工作先后顺序功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="5ceeb-114">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5ceeb-115">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5ceeb-116">**模块** ： *仓库管理*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5ceeb-117">**功能名称** ： *组织范围内的系统导向工作先后顺序*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="5ceeb-118">设置</span><span class="sxs-lookup"><span data-stu-id="5ceeb-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="5ceeb-119">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="5ceeb-119">Make demo data available</span></span>

<span data-ttu-id="5ceeb-120">若要使用本主题中提供的值完成此场景，使用的系统中必须已安装标准演示数据。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="5ceeb-121">此外，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="5ceeb-122">此场景使用演示数据中的仓库 *51* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ceeb-123">在将订单下达到仓库之前，请确保领料货位有满足所有订单上的所有物料的足够库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="5ceeb-124">默认 USMF 数据应该会支持此场景。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="5ceeb-125">如果不使用演示数据，请查看 **货位指令** 设置了解哪些领料货位用于销售订单领料的。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="5ceeb-126">如果必须调整库存，可创建手动移动，使用补货，或使用其他任何流。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="5ceeb-127">设置移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="5ceeb-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="5ceeb-128">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5ceeb-129">在移动设备菜单项列表中，选择 **销售领料 – 系统** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="5ceeb-130">应该已存在必需的菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="5ceeb-131">确认以下设置：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="5ceeb-132">**常规** 快速选项卡中的 **导向方式** 字段应设置为 *系统导向* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="5ceeb-133">**工作类** 快速选项卡应显示以下设置。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="5ceeb-134">工作类 ID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-134">Work class ID</span></span> | <span data-ttu-id="5ceeb-135">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="5ceeb-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="5ceeb-136">销售额</span><span class="sxs-lookup"><span data-stu-id="5ceeb-136">Sales</span></span> | <span data-ttu-id="5ceeb-137">销售订单</span><span class="sxs-lookup"><span data-stu-id="5ceeb-137">Sales orders</span></span> |
        | <span data-ttu-id="5ceeb-138">SO 领料</span><span class="sxs-lookup"><span data-stu-id="5ceeb-138">SO Pick</span></span> | <span data-ttu-id="5ceeb-139">销售订单</span><span class="sxs-lookup"><span data-stu-id="5ceeb-139">Sales orders</span></span> |

1. <span data-ttu-id="5ceeb-140">在操作窗格上，选择 **系统导向工作序列查询** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="5ceeb-141">选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-141">Select **Edit**.</span></span>
1. <span data-ttu-id="5ceeb-142">删除现有行，然后选择 **是** 确认操作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="5ceeb-143">在“操作窗格”中，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="5ceeb-144">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-145">**序列号** ： *1*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="5ceeb-146">**说明字段** ： *工作数量低于 20 且排序方式为降序*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="5ceeb-147">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-147">Select **Save**.</span></span>
1. <span data-ttu-id="5ceeb-148">在操作窗格上，选择 **编辑查询** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="5ceeb-149">在 **联接** 选项卡上，展开联接层次结构显示 **工作行** 表。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="5ceeb-150">选择 **工作行** 表联接。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="5ceeb-151">选择 **添加表联接** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="5ceeb-152">在显示的列表中，找到并选择采用以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="5ceeb-153">**联接模式** ： *n:1*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="5ceeb-154">**关系** ： *货位（货位）*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="5ceeb-155">选择 **选择** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-155">Select **Select**.</span></span>

    <span data-ttu-id="5ceeb-156">将把货位添加到表联接。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="5ceeb-157">在 **排序** 选项卡中，选择 **添加** 添加一行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="5ceeb-158">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-159">**表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-160">**派生表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-161">**字段** ： *工作数量* （在显示的消息框中，选择 **是** 向此字段添加排序。）</span><span class="sxs-lookup"><span data-stu-id="5ceeb-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="5ceeb-162">**搜索方向** ： *降序*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="5ceeb-163">选择 **范围** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="5ceeb-164">如果先后顺序中应仅包含特定各种条件，可以在 **范围** 选项卡中指定。在此示例中，只需包含数量少于 20 个（最低度量单位）的工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="5ceeb-165">请注意，已经包含一些行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-165">Notice that some lines are already included.</span></span> <span data-ttu-id="5ceeb-166">不应删除这些行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="5ceeb-167">选择 **添加** 添加一行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="5ceeb-168">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-169">**表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-170">**派生表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-171">**字段** ： *库存工作数量*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="5ceeb-172">**条件** ： *\<20* （低于 20）</span><span class="sxs-lookup"><span data-stu-id="5ceeb-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="5ceeb-173">选择 **添加** 再添加一行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="5ceeb-174">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-175">**表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-176">**派生表** ： *工作行*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5ceeb-177">**字段** ： *工作类型*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="5ceeb-178">**条件** ： *领料*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="5ceeb-179">选择 **添加** 再添加一行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="5ceeb-180">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-181">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="5ceeb-182">**派生表** ： *货位*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="5ceeb-183">\**字段：\*\*\*位置模板 ID*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="5ceeb-184">**条件** ： *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="5ceeb-185">务必在 *STAGE* 前面包含感叹号 ( *!* )。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-185">Be sure to include the exclamation point ( *!* ) in front of *STAGE*.</span></span>

1. <span data-ttu-id="5ceeb-186">选择 **确定** 保存并关闭设置。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="5ceeb-187">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-187">Select **Save**.</span></span>
1. <span data-ttu-id="5ceeb-188">关闭页面回到 **移动设备菜单项** 页面。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="5ceeb-189">此步骤定义将用于向移动设备菜单项提供符合资格的工作的条件。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="5ceeb-190">如果向查询添加更多条件行，系统将先使用序列号最小的查询行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="5ceeb-191">换句话说，将首先把序列号 1 的所有合格工作提供给用户，然后提供序列号 2 的所有工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="5ceeb-192">因此，如果必须一起使用特定范围和排序，应该在同一个系统导向工作序列查询中指定。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="5ceeb-193">此设置将捕获至少有一个行，并且该行中的数量小于 20 个的所有工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="5ceeb-194">因此，如果工作有一行中数量正好是 20 个或超过 20 个，则该工作有效，前提是其还有至少一行中数量低于 20 个。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="5ceeb-195">位置指令</span><span class="sxs-lookup"><span data-stu-id="5ceeb-195">Location directives</span></span>

<span data-ttu-id="5ceeb-196">如果在使用默认 Contoso 数据，则不需要更改货位指令操作的查询。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="5ceeb-197">但是，若要确保在非 Contoso 环境中应用此功能时，货位指令将捕获销售订单中的物料，请创建一个新的货位指令。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="5ceeb-198">若要在演示环境中验证设置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="5ceeb-199">转到 **仓库管理** \> **设置** \> **货位指令** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="5ceeb-200">在 **工作订单类型** 字段中，选择 *销售订单* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="5ceeb-201">选择名称为 *51 Pick* 的货位指令。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="5ceeb-202">在 **货位指令操作** 快速选项卡上，选择 **领料** 操作的行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="5ceeb-203">选择网格上方的 **编辑查询** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="5ceeb-204">查看 **范围** 查询。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="5ceeb-205">找到其中的 **字段** 字段设置为 *货位* 的行。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="5ceeb-206">确保 **条件** 字段为空（即不限制）。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="5ceeb-207">应用场景</span><span class="sxs-lookup"><span data-stu-id="5ceeb-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="5ceeb-208">创建销售订单领料工作</span><span class="sxs-lookup"><span data-stu-id="5ceeb-208">Create sales order picking work</span></span>

<span data-ttu-id="5ceeb-209">运行系统导向领料之前，应创建一些出库工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="5ceeb-210">对于此场景，将创建四个基于指定的系统导向工作序列查询的销售订单。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="5ceeb-211">将为每个销售订单预留库存数量。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="5ceeb-212">因此，除非库存预留或部分库存预留已取消，否则不能从仓库中为其他订单提取预留库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="5ceeb-213">然后将把每个销售订单下达到仓库以创建出库工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="5ceeb-214">销售订单 1</span><span class="sxs-lookup"><span data-stu-id="5ceeb-214">Sales order 1</span></span>

1. <span data-ttu-id="5ceeb-215">转到 **销售和营销 \> 销售订单 \> 所有销售订单** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5ceeb-216">在“操作窗格”中，选择 **新建** 创建销售订单 1。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="5ceeb-217">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-218">在 **客户** 部分中，将 **客户帐户** 字段设置为 *US-004* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="5ceeb-219">在 **常规** 部分中，将 **仓库** 字段设置为 *51* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="5ceeb-220">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="5ceeb-221">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5ceeb-222">在新销售订单中添加一行，并设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-223">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="5ceeb-224">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="5ceeb-225">在网格上方的 **库存** 菜单中，选择 **预留** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5ceeb-226">在 **预留** 页面中，选择 **预留批次** 预留库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="5ceeb-227">关闭 **预留** 页面。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="5ceeb-228">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库** 为仓库创建工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="5ceeb-229">您将收到参考消息，其中显示为销售订单创建的波次 ID 和装运 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="5ceeb-230">销售订单 2</span><span class="sxs-lookup"><span data-stu-id="5ceeb-230">Sales order 2</span></span>

1. <span data-ttu-id="5ceeb-231">在“操作窗格”中，选择 **新建** 创建销售订单 2。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="5ceeb-232">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-233">**客户帐户** ： *US-007*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5ceeb-234">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="5ceeb-235">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="5ceeb-236">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5ceeb-237">在新销售订单中添加一行，并设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-238">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="5ceeb-239">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="5ceeb-240">选择 **添加行** 添加第二个行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-241">\**物料编号：\*\*\*M9201*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="5ceeb-242">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5ceeb-243">为两行预留库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="5ceeb-244">将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="5ceeb-245">销售订单 3</span><span class="sxs-lookup"><span data-stu-id="5ceeb-245">Sales order 3</span></span>

1. <span data-ttu-id="5ceeb-246">在“操作窗格”中，选择 **新建** 创建销售订单 3。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="5ceeb-247">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-248">**客户帐户** ： *US-009*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="5ceeb-249">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="5ceeb-250">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="5ceeb-251">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5ceeb-252">在新销售订单中添加一行，并设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-253">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="5ceeb-254">**数量：** *7*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="5ceeb-255">选择 **添加行** 添加第二个行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-256">\**物料编号：\*\*\*M9202*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="5ceeb-257">**数量：** *8*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="5ceeb-258">为两行预留库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="5ceeb-259">将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="5ceeb-260">销售订单 4</span><span class="sxs-lookup"><span data-stu-id="5ceeb-260">Sales order 4</span></span>

1. <span data-ttu-id="5ceeb-261">在“操作窗格”中，选择 **新建** 创建销售订单 4。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="5ceeb-262">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5ceeb-263">**客户帐户** ： *US-010*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="5ceeb-264">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="5ceeb-265">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="5ceeb-266">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5ceeb-267">在新销售订单中添加一行，并设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-268">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="5ceeb-269">**数量：** *25*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="5ceeb-270">选择 **添加行** 添加第二个行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="5ceeb-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="5ceeb-271">\**物料编号：\*\*\*M9202*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="5ceeb-272">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="5ceeb-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="5ceeb-273">为两行预留库存。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="5ceeb-274">将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="5ceeb-275">获取创建的工作的工作 ID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="5ceeb-276">转到 **仓库管理 \> 工作 \> 工作详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5ceeb-277">筛选 **仓库** 字段，以便仅显示仓库 *51* 的工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="5ceeb-278">应该已经创建了四个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-278">Four work IDs should have been created.</span></span> <span data-ttu-id="5ceeb-279">记下每个销售订单的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="5ceeb-280">销售订单 ID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-280">Sales order ID</span></span> | <span data-ttu-id="5ceeb-281">工作 ID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-281">Work ID</span></span> | <span data-ttu-id="5ceeb-282">工作数量</span><span class="sxs-lookup"><span data-stu-id="5ceeb-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="5ceeb-283">销售订单 1</span><span class="sxs-lookup"><span data-stu-id="5ceeb-283">Sales Order 1</span></span> | <span data-ttu-id="5ceeb-284">工作 ID 1</span><span class="sxs-lookup"><span data-stu-id="5ceeb-284">Work ID 1</span></span> | <span data-ttu-id="5ceeb-285">20 个</span><span class="sxs-lookup"><span data-stu-id="5ceeb-285">20 ea</span></span> |
    | <span data-ttu-id="5ceeb-286">销售订单 2</span><span class="sxs-lookup"><span data-stu-id="5ceeb-286">Sales Order 2</span></span> | <span data-ttu-id="5ceeb-287">工作 ID 2</span><span class="sxs-lookup"><span data-stu-id="5ceeb-287">Work ID 2</span></span> | <span data-ttu-id="5ceeb-288">6 个（两行之和）</span><span class="sxs-lookup"><span data-stu-id="5ceeb-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="5ceeb-289">销售订单 3</span><span class="sxs-lookup"><span data-stu-id="5ceeb-289">Sales Order 3</span></span> | <span data-ttu-id="5ceeb-290">工作 ID 3</span><span class="sxs-lookup"><span data-stu-id="5ceeb-290">Work ID 3</span></span> | <span data-ttu-id="5ceeb-291">15 个（两行之和）</span><span class="sxs-lookup"><span data-stu-id="5ceeb-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="5ceeb-292">销售订单 4</span><span class="sxs-lookup"><span data-stu-id="5ceeb-292">Sales Order 4</span></span> | <span data-ttu-id="5ceeb-293">工作 ID 4</span><span class="sxs-lookup"><span data-stu-id="5ceeb-293">Work ID 4</span></span> | <span data-ttu-id="5ceeb-294">35 个（两行之和）</span><span class="sxs-lookup"><span data-stu-id="5ceeb-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="5ceeb-295">在移动设备中运行流之前，请确保对于仓库 *51* 和 *销售订单* 工作订单类型，只有刚才创建的工作的状态才是 *未结* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="5ceeb-296">否则，测试结果可能不同，因为系统导向领料中将包含所有合格工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="5ceeb-297">转到 **仓库管理 \> 工作 \> 出库 \> 未结销售订单** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="5ceeb-298">在 **未结销售工作** 网格中，筛选 **仓库** 字段，以便仅显示仓库 *51* 的工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="5ceeb-299">确认仅显示前面创建的四个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="5ceeb-300">关闭 **工作** 页面。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="5ceeb-301">执行移动设备流</span><span class="sxs-lookup"><span data-stu-id="5ceeb-301">Mobile device flow execution</span></span>

<span data-ttu-id="5ceeb-302">系统将根据设置提供从最大工作行数量到最小排序的用户工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="5ceeb-303">每行中的数量将低于 20 个。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="5ceeb-304">请注意，此设置将捕获至少有一个行，并且该行中的数量小于 20 个的所有工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="5ceeb-305">因此，如果还有一行中的数量正好是 20 个或超过 20 个，该行也将有效。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="5ceeb-306">移动应用</span><span class="sxs-lookup"><span data-stu-id="5ceeb-306">Mobile app</span></span>

1. <span data-ttu-id="5ceeb-307">以仓库 *51* 用户身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="5ceeb-308">转到 **出库 \> 销售领料 - 系统** 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="5ceeb-309">将提供工作 ID *4* 的领料步骤。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="5ceeb-310">先提供此工作 ID 是因为系统导向查询订单的设置，在此设置中，应该根据降序工作行数量为工作排序。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="5ceeb-311">完成所需领料和放置以结束工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="5ceeb-312">接下来，提供工作 ID *3* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="5ceeb-313">其工作行之一根据工作行数量是序列中的下一项。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="5ceeb-314">完成领料和放置以结束工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="5ceeb-315">接下来，提供工作 ID *2* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="5ceeb-316">此工作的领料行是序列中的下一项。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="5ceeb-317">完成领料和放置以结束工作 ID。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="5ceeb-318">不应再向您提供任何工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-318">No further work should be presented to you.</span></span> <span data-ttu-id="5ceeb-319">工作 ID *1* 不符合此移动设备菜单项的资格，因为查询指定仅当工作行中的数量小于 20 个时，才考虑工作标题。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="5ceeb-320">提示</span><span class="sxs-lookup"><span data-stu-id="5ceeb-320">Tips</span></span>

<span data-ttu-id="5ceeb-321">系统导向工作序列查询为 *包含* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="5ceeb-322">务必为某些设置记住这一点。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="5ceeb-323">例如，您希望特定菜单项仅处理其工作单位为 *个* 的工作，并且在查询的 **范围** 选项卡中指定该限制。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-323">For example, you want a specific menu item to process only work where the work unit is *ea* , and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="5ceeb-324">在此情况下，将向工作人员提供至少有一个工作行的工作单位设置为 *个* 的所有工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="5ceeb-325">因此，此工作还包括其工作行的工作单位不是 *个* （如 *箱* 或 *托盘* ）的工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet* ).</span></span> <span data-ttu-id="5ceeb-326">此查询将仅排除没有工作行的工作单位设置为 *个* 的工作。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="5ceeb-327">因此，在此场景的示例中，查询还捕获了工作 ID *4* 。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="5ceeb-328">创建它时，添加了两行：一行为 25 个，另一行为 10 个。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="5ceeb-329">仍然将此工作提供给了用户，因为至少有一个工作行的数量少于 20 个。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="5ceeb-330">可以使用工作分解阻止此行为，具体取决于场景。</span><span class="sxs-lookup"><span data-stu-id="5ceeb-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
