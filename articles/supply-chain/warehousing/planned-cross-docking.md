---
title: 计划越库配送
description: 此主题介绍高级计划越库配送，在执行此类配送时，订单所需库存数量将在收到或创建时直接传输到正确的出货台或暂存区。 将通过常规储存流程把入库源中的所有剩余库存导向到正确存储货位。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017751"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="b55b7-104">计划越库配送</span><span class="sxs-lookup"><span data-stu-id="b55b7-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b55b7-105">本主题介绍高级计划越库配送。</span><span class="sxs-lookup"><span data-stu-id="b55b7-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="b55b7-106">越库配送是在执行此类配送时，订单所需库存数量将在收到或创建时直接传输到正确的出货台或暂存区的仓库流程。</span><span class="sxs-lookup"><span data-stu-id="b55b7-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="b55b7-107">将通过常规储存流程把入库源中的所有剩余库存导向到正确存储货位。</span><span class="sxs-lookup"><span data-stu-id="b55b7-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="b55b7-108">越库配送让工作人员可以跳过已经为出库订单标记的库存的入库储存和出库领料。</span><span class="sxs-lookup"><span data-stu-id="b55b7-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="b55b7-109">因此，如果可以，将把接触库存的次数降到最低。</span><span class="sxs-lookup"><span data-stu-id="b55b7-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="b55b7-110">此外，因为与系统的交互减少，所以可以节约仓库中所用时间和空间。</span><span class="sxs-lookup"><span data-stu-id="b55b7-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="b55b7-111">用户必须先配置新的越库配送模板（其中为越库配送指定供应源和其他要求组合），才能使用越库配送。</span><span class="sxs-lookup"><span data-stu-id="b55b7-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="b55b7-112">创建出库订单时，必须根据包含同一个物料的入库订单标记行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="b55b7-113">收到入库订单时，越库配送设置将自动确定是否需要越库配送，然后根据货位指令的设置为所需数量创建移动工作。</span><span class="sxs-lookup"><span data-stu-id="b55b7-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="b55b7-114">取消越库配送工作时， **不** 取消等记库存交易记录，即使在仓库管理参数中开启了此功能的设置也不例外。</span><span class="sxs-lookup"><span data-stu-id="b55b7-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="b55b7-115">开启计划越库配送功能</span><span class="sxs-lookup"><span data-stu-id="b55b7-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="b55b7-116">越库配送功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b55b7-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="b55b7-117">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="b55b7-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b55b7-118">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="b55b7-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b55b7-119">**模块** ： *仓库管理*</span><span class="sxs-lookup"><span data-stu-id="b55b7-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b55b7-120">**功能名称** ： *计划越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="b55b7-121">设置</span><span class="sxs-lookup"><span data-stu-id="b55b7-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="b55b7-122">重新生成负荷过帐方法</span><span class="sxs-lookup"><span data-stu-id="b55b7-122">Regenerate load posting methods</span></span>

<span data-ttu-id="b55b7-123">计划越库配送以负荷过帐方法的形式实施。</span><span class="sxs-lookup"><span data-stu-id="b55b7-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="b55b7-124">开启此功能之后，必须重新生成这些方法。</span><span class="sxs-lookup"><span data-stu-id="b55b7-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="b55b7-125">转到 **仓库管理 \> 设置 \> 负荷过帐方法** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="b55b7-126">在操作窗格上，选择 **重新生成方法** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="b55b7-127">重新生成完成后，应该可以看到 **方法名称** 值为 *planCrossDocking* 的方法。</span><span class="sxs-lookup"><span data-stu-id="b55b7-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="b55b7-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b55b7-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="b55b7-129">创建越库配送模板</span><span class="sxs-lookup"><span data-stu-id="b55b7-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="b55b7-130">转到 **仓库管理 \> 设置 \> 工作 \> 越库配送模板** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="b55b7-131">在“操作窗格”中，选择 **新建** 创建一个模板。</span><span class="sxs-lookup"><span data-stu-id="b55b7-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="b55b7-132">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="b55b7-133">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b55b7-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="b55b7-134">此字段定义模板的评估顺序。</span><span class="sxs-lookup"><span data-stu-id="b55b7-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="b55b7-135">**越库配送模板 ID** ： *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="b55b7-136">**说明** ： *仓库 51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="b55b7-137">**需求下达策略** ： *在供应收货前*</span><span class="sxs-lookup"><span data-stu-id="b55b7-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="b55b7-138">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b55b7-139">**计划** 快速选项卡中的设置控制模板的工作方式。</span><span class="sxs-lookup"><span data-stu-id="b55b7-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="b55b7-140">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-140">Set the following values:</span></span>

    - <span data-ttu-id="b55b7-141">**需求要求** ： *无*</span><span class="sxs-lookup"><span data-stu-id="b55b7-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="b55b7-142">此字段定义需求库存的要求。</span><span class="sxs-lookup"><span data-stu-id="b55b7-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="b55b7-143">如果必须在下达前将需求链接到供应，请选择 *标记* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="b55b7-144">如果必须在下达前根据需求为订单预留需求，请选择 *订单预留* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="b55b7-145">**定位类型** ： *装运货位*</span><span class="sxs-lookup"><span data-stu-id="b55b7-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="b55b7-146">此字段定义越库配送工作是否应使用装运中的暂存/负荷货位，或者是否应使用货位指令查找自己的暂存/负荷货位。</span><span class="sxs-lookup"><span data-stu-id="b55b7-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="b55b7-147">**工作模板** ：将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="b55b7-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="b55b7-148">此字段定义创建越库配送工作时应该使用的工作模板。</span><span class="sxs-lookup"><span data-stu-id="b55b7-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="b55b7-149">**供应收货时重新验证** ： *否*</span><span class="sxs-lookup"><span data-stu-id="b55b7-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="b55b7-150">此选项定义收货期间是否应重新验证供应。</span><span class="sxs-lookup"><span data-stu-id="b55b7-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="b55b7-151">如果此选项设置为 *是* ，将检查最大时间范围和到期日期范围。</span><span class="sxs-lookup"><span data-stu-id="b55b7-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="b55b7-152">**验证时间范围** ： *是*</span><span class="sxs-lookup"><span data-stu-id="b55b7-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="b55b7-153">此选项定义在选择供应源时是否应评估最大时间范围。</span><span class="sxs-lookup"><span data-stu-id="b55b7-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="b55b7-154">如果此选项设置为 *是* ，则可使用与最大和最小时间范围有关的字段。</span><span class="sxs-lookup"><span data-stu-id="b55b7-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="b55b7-155">**最大时间范围** ： *5*</span><span class="sxs-lookup"><span data-stu-id="b55b7-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="b55b7-156">此选项定义供应物料到达与需求物料离开之间允许的最大时间段。</span><span class="sxs-lookup"><span data-stu-id="b55b7-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b55b7-157">**最大时间范围单位** ： *天*</span><span class="sxs-lookup"><span data-stu-id="b55b7-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b55b7-158">**最小时间范围** ： *0*</span><span class="sxs-lookup"><span data-stu-id="b55b7-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="b55b7-159">此选项定义供应物料到达与需求物料离开之间允许的最小时间段。</span><span class="sxs-lookup"><span data-stu-id="b55b7-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b55b7-160">**最小时间范围单位** ： *天*</span><span class="sxs-lookup"><span data-stu-id="b55b7-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b55b7-161">**到期日期范围** ： *0*</span><span class="sxs-lookup"><span data-stu-id="b55b7-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="b55b7-162">*先过期先出 (FEFO) 条件* ：此字段定义仓库中现在的首先到期批次的到期日期与正在收货的批次的到期日期之间的最大天数。</span><span class="sxs-lookup"><span data-stu-id="b55b7-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="b55b7-163">在 **供应源** 快速选项卡中，指定此模板的有效供应类型。</span><span class="sxs-lookup"><span data-stu-id="b55b7-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="b55b7-164">选择 **新建** ，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="b55b7-165">**序列号** ： *1*</span><span class="sxs-lookup"><span data-stu-id="b55b7-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b55b7-166">**供应源** ： *采购订单*</span><span class="sxs-lookup"><span data-stu-id="b55b7-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="b55b7-167">创建工作类</span><span class="sxs-lookup"><span data-stu-id="b55b7-167">Create a work class</span></span>

1. <span data-ttu-id="b55b7-168">转到 **仓库管理 \> 设置 \> 工作 \> 工作类** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b55b7-169">在“操作窗格”中，选择 **新建** 创建一个工作类。</span><span class="sxs-lookup"><span data-stu-id="b55b7-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="b55b7-170">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-170">Set the following values:</span></span>

    - <span data-ttu-id="b55b7-171">**工作类 ID** ： *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b55b7-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b55b7-172">**说明** ： *越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="b55b7-173">**工作订单类型** ： *越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="b55b7-174">创建工作模板</span><span class="sxs-lookup"><span data-stu-id="b55b7-174">Create a work template</span></span>

1. <span data-ttu-id="b55b7-175">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b55b7-176">将 **工作订单类型** 字段设置为 *越库配送* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b55b7-177">在操作窗格上，选择 **新建** 向 **概览** 选项卡添加一行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="b55b7-178">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-179">**序列号** ： *1*</span><span class="sxs-lookup"><span data-stu-id="b55b7-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b55b7-180">**工作模板** ： *51 越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="b55b7-181">**工作模板说明** ： *51 越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="b55b7-182">选择 **保存** 激活 **工作模板详细信息** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b55b7-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b55b7-183">在 **工作模板详细信息** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b55b7-184">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-185">**工作类型：** *领料*</span><span class="sxs-lookup"><span data-stu-id="b55b7-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b55b7-186">**工作类 ID** ： *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b55b7-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b55b7-187">选择 **新建** 再添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="b55b7-188">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="b55b7-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b55b7-189">**工作类 ID** ： *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b55b7-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b55b7-190">选择 **保存** ，然后确认为 *51 越库配送* 模板选中了 **有效** 复选框。</span><span class="sxs-lookup"><span data-stu-id="b55b7-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="b55b7-191">*领料* 和 *放置* 工作类型的工作类 ID 必须相同。</span><span class="sxs-lookup"><span data-stu-id="b55b7-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="b55b7-192">创建货位指令</span><span class="sxs-lookup"><span data-stu-id="b55b7-192">Create location directives</span></span>

1. <span data-ttu-id="b55b7-193">转到 **库存管理 \> 设置 \> 位置指令** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b55b7-194">在左窗格中，将 **工作订单类型** 设置为 *越库配送* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b55b7-195">在操作窗格中，选择 **新建** ，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="b55b7-196">**序列号** ： *1*</span><span class="sxs-lookup"><span data-stu-id="b55b7-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b55b7-197">**名称** ： *51 越库配送放置*</span><span class="sxs-lookup"><span data-stu-id="b55b7-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="b55b7-198">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="b55b7-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b55b7-199">**站点：** *5*</span><span class="sxs-lookup"><span data-stu-id="b55b7-199">**Site:** *5*</span></span>
    - <span data-ttu-id="b55b7-200">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b55b7-201">选择 **保存** 激活 **行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b55b7-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b55b7-202">在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b55b7-203">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-204">**起始数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b55b7-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b55b7-205">**目标数量：** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b55b7-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="b55b7-206">选择 **保存** 激活 **货位指令操作** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b55b7-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b55b7-207">在 **货位指令操作** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b55b7-208">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-209">**名称** ： *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b55b7-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="b55b7-210">**固定货位使用情况** ： *固定货位和非固定货位*</span><span class="sxs-lookup"><span data-stu-id="b55b7-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="b55b7-211">选择 **保存** 激活 **货位指令操作** 工具栏上的 **编辑查询** 按钮。</span><span class="sxs-lookup"><span data-stu-id="b55b7-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="b55b7-212">选择 **编辑查询** 打开查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="b55b7-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="b55b7-213">在 **范围** 选项卡上，确保配置下面的两行：</span><span class="sxs-lookup"><span data-stu-id="b55b7-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="b55b7-214">行 1：</span><span class="sxs-lookup"><span data-stu-id="b55b7-214">Line 1:</span></span>

        - <span data-ttu-id="b55b7-215">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="b55b7-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b55b7-216">**派生表** ： *货位*</span><span class="sxs-lookup"><span data-stu-id="b55b7-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b55b7-217">**字段** ： *仓库*</span><span class="sxs-lookup"><span data-stu-id="b55b7-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="b55b7-218">**条件** ： *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="b55b7-219">行 2：</span><span class="sxs-lookup"><span data-stu-id="b55b7-219">Line 2:</span></span>

        - <span data-ttu-id="b55b7-220">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="b55b7-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b55b7-221">**派生表** ： *货位*</span><span class="sxs-lookup"><span data-stu-id="b55b7-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b55b7-222">**字段** ： *货位*</span><span class="sxs-lookup"><span data-stu-id="b55b7-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="b55b7-223">**条件** ： *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b55b7-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="b55b7-224">选择 **确定** 关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="b55b7-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b55b7-225">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="b55b7-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b55b7-226">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b55b7-227">在左侧窗格中的菜单项列表内，选择 **采购储存** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="b55b7-228">选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-228">Select **Edit**.</span></span>
1. <span data-ttu-id="b55b7-229">在 **工作类** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b55b7-230">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-231">**工作类 ID** ： *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b55b7-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b55b7-232">**工作订单类型** ： *越库配送*</span><span class="sxs-lookup"><span data-stu-id="b55b7-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="b55b7-233">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b55b7-234">应用场景</span><span class="sxs-lookup"><span data-stu-id="b55b7-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b55b7-235">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="b55b7-235">Create a purchase order</span></span>

<span data-ttu-id="b55b7-236">执行以下步骤创建一个采购订单作为供应源。</span><span class="sxs-lookup"><span data-stu-id="b55b7-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="b55b7-237">转到 **采购 \> 采购订单 \> 所有采购订单** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b55b7-238">在操作窗格上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b55b7-239">在 **创建采购订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b55b7-240">**供应商帐户** ： *104*</span><span class="sxs-lookup"><span data-stu-id="b55b7-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b55b7-241">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b55b7-242">选择 **确定** ，并记下订单号。</span><span class="sxs-lookup"><span data-stu-id="b55b7-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="b55b7-243">将向 **采购订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b55b7-244">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-245">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="b55b7-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b55b7-246">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="b55b7-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b55b7-247">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="b55b7-247">Create a sales order</span></span>

<span data-ttu-id="b55b7-248">执行以下步骤创建一个销售订单作为需求源。</span><span class="sxs-lookup"><span data-stu-id="b55b7-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="b55b7-249">转到 **销售和营销 \> 销售订单 \> 所有销售订单** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b55b7-250">在操作窗格上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b55b7-251">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b55b7-252">**客户帐户** ： *US-002*</span><span class="sxs-lookup"><span data-stu-id="b55b7-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b55b7-253">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="b55b7-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b55b7-254">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-254">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-255">将向 **销售订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="b55b7-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b55b7-256">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b55b7-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="b55b7-257">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="b55b7-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b55b7-258">**数量：** *3*</span><span class="sxs-lookup"><span data-stu-id="b55b7-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="b55b7-259">创建计划越库配送</span><span class="sxs-lookup"><span data-stu-id="b55b7-259">Create planned cross-docking</span></span>

<span data-ttu-id="b55b7-260">执行以下步骤根据销售订单创建计划越库配送。</span><span class="sxs-lookup"><span data-stu-id="b55b7-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="b55b7-261">在刚才创建的销售订单的 **销售订单详细信息** 页操作窗格中 **仓库** 选项卡上 **操作** 组内，选择 **发放到仓库** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b55b7-262">发放到仓库操作将为销售订单行创建装运和负荷行，并尝试分配库存。</span><span class="sxs-lookup"><span data-stu-id="b55b7-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="b55b7-263">您将收到参考消息。</span><span class="sxs-lookup"><span data-stu-id="b55b7-263">You receive an informational message.</span></span> <span data-ttu-id="b55b7-264">您还会收到以下警告消息：“未为波次 XXXX 创建任何工作。</span><span class="sxs-lookup"><span data-stu-id="b55b7-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="b55b7-265">有关详细信息，请参见工作创建历史记录日志。”</span><span class="sxs-lookup"><span data-stu-id="b55b7-265">See the work creation history log for details."</span></span> <span data-ttu-id="b55b7-266">这是正常行为，因为仓库中无库存。</span><span class="sxs-lookup"><span data-stu-id="b55b7-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="b55b7-267">在 **销售订单行** 快速选项卡上的 **仓库** 菜单中，选择 **装运详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="b55b7-268">将显示 **装运详细信息** 页面，其中显示为销售订单创建的装运。</span><span class="sxs-lookup"><span data-stu-id="b55b7-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="b55b7-269">请注意， **负荷行** 快速选项卡上的 **计划越库配送数量** 字段设置为 *3* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="b55b7-270">因为仓库中没有任何库存，但是在越库配送模板中定义的时间范围内将有一个有效供应源到达，所以创建了越库配送数量。</span><span class="sxs-lookup"><span data-stu-id="b55b7-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="b55b7-271">在 **负荷行** 快速选项卡中，选择 **计划越库配送** 查看创建的越库配送的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b55b7-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="b55b7-272">处理越库配送</span><span class="sxs-lookup"><span data-stu-id="b55b7-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="b55b7-273">仓库移动应用中的采购订单收货</span><span class="sxs-lookup"><span data-stu-id="b55b7-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="b55b7-274">系统将接收采购订单中的 5 件并放入收货货位，再创建两份工作。</span><span class="sxs-lookup"><span data-stu-id="b55b7-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="b55b7-275">创建的第一个工作 ID 的 **工作订单类型** 值为 *越库配送* ，并且该 ID 将链接到销售订单。</span><span class="sxs-lookup"><span data-stu-id="b55b7-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="b55b7-276">其数量为 3，并导向到最终装运货位，从而可以立即运出。</span><span class="sxs-lookup"><span data-stu-id="b55b7-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="b55b7-277">创建的第二个工作 ID 的 **工作订单类型** 值为 *采购订单* ，并且该 ID 将链接到采购订单。</span><span class="sxs-lookup"><span data-stu-id="b55b7-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="b55b7-278">其未越库配送的剩余数量为 2，并将导向以储存。</span><span class="sxs-lookup"><span data-stu-id="b55b7-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="b55b7-279">以仓库 *51* 中的用户的身份登录移动设备。</span><span class="sxs-lookup"><span data-stu-id="b55b7-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b55b7-280">转到 **入库 \> 采购收货** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="b55b7-281">在 **采购订单号** 字段中，输入您的采购订单号。</span><span class="sxs-lookup"><span data-stu-id="b55b7-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="b55b7-282">在 **数量** 字段中，输入 *5* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="b55b7-283">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-283">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-284">在下一页，将 **物料** 字段设置为 *A0001* 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="b55b7-285">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-285">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-286">在下一页，通过选择 **确定** 确认 **采购订单号** 、 **物料** 和 **数量** 值。</span><span class="sxs-lookup"><span data-stu-id="b55b7-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="b55b7-287">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b55b7-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b55b7-288">选择 **取消** 以退出。</span><span class="sxs-lookup"><span data-stu-id="b55b7-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="b55b7-289">储存以越库配送和批量处理</span><span class="sxs-lookup"><span data-stu-id="b55b7-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="b55b7-290">现在，两个工作 ID 的目标牌照相同。</span><span class="sxs-lookup"><span data-stu-id="b55b7-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="b55b7-291">若要完成后续步骤，必须获取工作 ID 和目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b55b7-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="b55b7-292">可以从采购订单行和销售订单行的工作详细信息获取此信息。</span><span class="sxs-lookup"><span data-stu-id="b55b7-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="b55b7-293">也可以转到 **仓库管理 \> 工作 \> 工作详细信息** ，然后筛选以查找其 **仓库** 值为 *51* 的工作。</span><span class="sxs-lookup"><span data-stu-id="b55b7-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="b55b7-294">在移动设备上，转到 **入库 \> 采购储存** ，然后输入工作中的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b55b7-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="b55b7-295">在 **ID** 字段中，输入工作详细信息中的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b55b7-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="b55b7-296">越库配送领料页面显示领料货位 ( *RECV* )、目标牌照（ *牌照* ）、物料 ( *A0001* ) 和数量 ( *3* )。</span><span class="sxs-lookup"><span data-stu-id="b55b7-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="b55b7-297">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-297">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-298">在 **目标牌照** 字段中，输入应该放置（越库配送）到装运货位的牌照 ID 的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b55b7-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="b55b7-299">可以选择所选任何牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b55b7-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="b55b7-300">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-300">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-301">在下一页的 **ID** 字段中，输入目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b55b7-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="b55b7-302">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-302">Select **OK**.</span></span>
1. <span data-ttu-id="b55b7-303">确认剩余数量 2 的领料工作，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="b55b7-304">在下一页上，选择 **完成** 结束领料流程，并开始储存流程。</span><span class="sxs-lookup"><span data-stu-id="b55b7-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="b55b7-305">移动应用将为您提供要将物料放置到的货位和牌照。</span><span class="sxs-lookup"><span data-stu-id="b55b7-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="b55b7-306">选择 **确定** 确认批量存储 **放置** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="b55b7-307">在下一页，选择 **确定** 确认越库配送 **放置** 。</span><span class="sxs-lookup"><span data-stu-id="b55b7-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="b55b7-308">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b55b7-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b55b7-309">选择 **取消** 以退出。</span><span class="sxs-lookup"><span data-stu-id="b55b7-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="b55b7-310">下图显示 Microsoft Dynamics 365 Supply Chain Management 中可能如何显示已完成的越库配送工作。</span><span class="sxs-lookup"><span data-stu-id="b55b7-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b55b7-311">![越库配送工作已完成](media/PlannedCrossDockingWork.png "越库配送工作已完成")</span><span class="sxs-lookup"><span data-stu-id="b55b7-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
