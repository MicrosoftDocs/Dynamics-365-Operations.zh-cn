---
title: 计划越库配送
description: 此主题介绍高级计划越库配送，在执行此类配送时，订单所需库存数量将在收到或创建时直接传输到正确的出货台或暂存区。 将通过常规储存流程把入库源中的所有剩余库存导向到正确存储货位。
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911240"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="77fe8-104">计划越库配送</span><span class="sxs-lookup"><span data-stu-id="77fe8-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77fe8-105">本主题介绍高级计划越库配送。</span><span class="sxs-lookup"><span data-stu-id="77fe8-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="77fe8-106">越库配送是在执行此类配送时，订单所需库存数量将在收到或创建时直接传输到正确的出货台或暂存区的仓库流程。</span><span class="sxs-lookup"><span data-stu-id="77fe8-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="77fe8-107">将通过常规储存流程把入库源中的所有剩余库存导向到正确存储货位。</span><span class="sxs-lookup"><span data-stu-id="77fe8-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="77fe8-108">越库配送让工作人员可以跳过已经为出库订单标记的库存的入库储存和出库领料。</span><span class="sxs-lookup"><span data-stu-id="77fe8-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="77fe8-109">因此，如果可以，将把接触库存的次数降到最低。</span><span class="sxs-lookup"><span data-stu-id="77fe8-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="77fe8-110">此外，因为与系统的交互减少，所以可以节约仓库中所用时间和空间。</span><span class="sxs-lookup"><span data-stu-id="77fe8-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="77fe8-111">您必须先配置新的越库配送模板（其中为越库配送指定供应源和其他要求集），然后才能运行越库配送。</span><span class="sxs-lookup"><span data-stu-id="77fe8-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="77fe8-112">创建出库订单时，必须根据包含同一个物料的入库订单标记行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="77fe8-113">您可以在越库配送模板上选择指令代码字段，类似于设置补货和采购订单的方式。</span><span class="sxs-lookup"><span data-stu-id="77fe8-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="77fe8-114">收到入库订单时，越库配送设置将自动确定是否需要越库配送，然后根据货位指令的设置为所需数量创建移动工作。</span><span class="sxs-lookup"><span data-stu-id="77fe8-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="77fe8-115">取消越库配送工作时，*不* 取消等记库存交易记录，即使在仓库管理参数中开启了此功能的设置也不例外。</span><span class="sxs-lookup"><span data-stu-id="77fe8-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="77fe8-116">开启计划越库配送功能</span><span class="sxs-lookup"><span data-stu-id="77fe8-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="77fe8-117">如果您的系统尚未包含本主题中所述的功能，请转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，按以下顺序打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="77fe8-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="77fe8-118">*计划越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="77fe8-119">*带有库位指令的越库配送模板*</span><span class="sxs-lookup"><span data-stu-id="77fe8-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="77fe8-120">此功能支持在越库配送模板上指定 **指令代码** 字段，类似于设置补货模板的方式。</span><span class="sxs-lookup"><span data-stu-id="77fe8-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="77fe8-121">启用此功能可防止您在最终 *放置* 行的越库配送工作模板行上添加指令代码。</span><span class="sxs-lookup"><span data-stu-id="77fe8-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="77fe8-122">这可确保在考虑工作模板之前，在工作创建期间确定最终放置库位。</span><span class="sxs-lookup"><span data-stu-id="77fe8-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="77fe8-123">设置</span><span class="sxs-lookup"><span data-stu-id="77fe8-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="77fe8-124">重新生成负荷过帐方法</span><span class="sxs-lookup"><span data-stu-id="77fe8-124">Regenerate load posting methods</span></span>

<span data-ttu-id="77fe8-125">计划越库配送以负荷过帐方法的形式实施。</span><span class="sxs-lookup"><span data-stu-id="77fe8-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="77fe8-126">开启此功能之后，必须重新生成这些方法。</span><span class="sxs-lookup"><span data-stu-id="77fe8-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="77fe8-127">转到 **仓库管理 \> 设置 \> 负荷过帐方法**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="77fe8-128">在操作窗格上，选择 **重新生成方法**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="77fe8-129">重新生成完成后，应该可以看到 **方法名称** 值为 *planCrossDocking* 的方法。</span><span class="sxs-lookup"><span data-stu-id="77fe8-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="77fe8-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77fe8-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="77fe8-131">创建越库配送模板</span><span class="sxs-lookup"><span data-stu-id="77fe8-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="77fe8-132">转到 **仓库管理 \> 设置 \> 工作 \> 越库配送模板**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="77fe8-133">在“操作窗格”中，选择 **新建** 创建一个模板。</span><span class="sxs-lookup"><span data-stu-id="77fe8-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="77fe8-134">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="77fe8-135">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="77fe8-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="77fe8-136">此字段定义模板的评估顺序。</span><span class="sxs-lookup"><span data-stu-id="77fe8-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="77fe8-137">**越库配送模板 ID**：*51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="77fe8-138">**说明**：*仓库 51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="77fe8-139">**需求下达策略**：*在供应收货前*</span><span class="sxs-lookup"><span data-stu-id="77fe8-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="77fe8-140">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77fe8-141">**计划** 快速选项卡中的设置控制模板的工作方式。</span><span class="sxs-lookup"><span data-stu-id="77fe8-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="77fe8-142">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-142">Set the following values:</span></span>

    - <span data-ttu-id="77fe8-143">**需求要求**：*无*</span><span class="sxs-lookup"><span data-stu-id="77fe8-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="77fe8-144">此字段定义需求库存的要求。</span><span class="sxs-lookup"><span data-stu-id="77fe8-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="77fe8-145">如果必须在下达前将需求链接到供应，请选择 *标记*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="77fe8-146">如果必须在下达前根据需求为订单预留需求，请选择 *订单预留*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="77fe8-147">**定位类型**：*装运货位*</span><span class="sxs-lookup"><span data-stu-id="77fe8-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="77fe8-148">此字段定义越库配送工作是否应使用装运中的暂存/负荷货位，或者是否应使用货位指令查找自己的暂存/负荷货位。</span><span class="sxs-lookup"><span data-stu-id="77fe8-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="77fe8-149">**工作模板**：将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="77fe8-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="77fe8-150">此字段定义创建越库配送工作时应该使用的工作模板。</span><span class="sxs-lookup"><span data-stu-id="77fe8-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="77fe8-151">**供应收货时重新验证**：*否*</span><span class="sxs-lookup"><span data-stu-id="77fe8-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="77fe8-152">此选项定义收货期间是否应重新验证供应。</span><span class="sxs-lookup"><span data-stu-id="77fe8-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="77fe8-153">如果此选项设置为 *是*，将检查最大时间范围和到期日期范围。</span><span class="sxs-lookup"><span data-stu-id="77fe8-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="77fe8-154">**指令代码：** 将此字段保留为空</span><span class="sxs-lookup"><span data-stu-id="77fe8-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="77fe8-155">通过 *带有库位指令的越库配送模板* 功能启用此选项。</span><span class="sxs-lookup"><span data-stu-id="77fe8-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="77fe8-156">系统使用库位指令帮助确定越库配送库存要移动到的最佳库位。</span><span class="sxs-lookup"><span data-stu-id="77fe8-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="77fe8-157">您可以通过为每个相关的越库配送模板分配指令代码来设置此选项。</span><span class="sxs-lookup"><span data-stu-id="77fe8-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="77fe8-158">如果设置指令代码，在生成工作时，系统将按指令代码搜索库位指令。</span><span class="sxs-lookup"><span data-stu-id="77fe8-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="77fe8-159">这样，您可以限制用于特定越库配送模板的库位指令。</span><span class="sxs-lookup"><span data-stu-id="77fe8-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="77fe8-160">**验证时间范围**：*是*</span><span class="sxs-lookup"><span data-stu-id="77fe8-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="77fe8-161">此选项定义在选择供应源时是否应评估最大时间范围。</span><span class="sxs-lookup"><span data-stu-id="77fe8-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="77fe8-162">如果此选项设置为 *是*，则可使用与最大和最小时间范围有关的字段。</span><span class="sxs-lookup"><span data-stu-id="77fe8-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="77fe8-163">**最大时间范围**：*5*</span><span class="sxs-lookup"><span data-stu-id="77fe8-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="77fe8-164">此选项定义供应物料到达与需求物料离开之间允许的最大时间段。</span><span class="sxs-lookup"><span data-stu-id="77fe8-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="77fe8-165">**最大时间范围单位**：*天*</span><span class="sxs-lookup"><span data-stu-id="77fe8-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="77fe8-166">**最小时间范围**：*0*</span><span class="sxs-lookup"><span data-stu-id="77fe8-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="77fe8-167">此选项定义供应物料到达与需求物料离开之间允许的最小时间段。</span><span class="sxs-lookup"><span data-stu-id="77fe8-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="77fe8-168">**最小时间范围单位**：*天*</span><span class="sxs-lookup"><span data-stu-id="77fe8-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="77fe8-169">**到期日期范围**：*0*</span><span class="sxs-lookup"><span data-stu-id="77fe8-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="77fe8-170">*先过期先出 (FEFO) 条件*：此字段定义仓库中现在的首先到期批次的到期日期与正在收货的批次的到期日期之间的最大天数。</span><span class="sxs-lookup"><span data-stu-id="77fe8-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="77fe8-171">在 **供应源** 快速选项卡中，指定此模板的有效供应类型。</span><span class="sxs-lookup"><span data-stu-id="77fe8-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="77fe8-172">选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="77fe8-173">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="77fe8-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77fe8-174">**供应源**：*采购订单*</span><span class="sxs-lookup"><span data-stu-id="77fe8-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="77fe8-175">创建工作类</span><span class="sxs-lookup"><span data-stu-id="77fe8-175">Create a work class</span></span>

1. <span data-ttu-id="77fe8-176">转到 **仓库管理 \> 设置 \> 工作 \> 工作类**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="77fe8-177">在“操作窗格”中，选择 **新建** 创建一个工作类。</span><span class="sxs-lookup"><span data-stu-id="77fe8-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="77fe8-178">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-178">Set the following values:</span></span>

    - <span data-ttu-id="77fe8-179">**工作类 ID**：*CrossDock*</span><span class="sxs-lookup"><span data-stu-id="77fe8-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="77fe8-180">**说明**：*越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="77fe8-181">**工作订单类型**：*越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="77fe8-182">创建工作模板</span><span class="sxs-lookup"><span data-stu-id="77fe8-182">Create a work template</span></span>

1. <span data-ttu-id="77fe8-183">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="77fe8-184">将 **工作订单类型** 字段设置为 *越库配送*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="77fe8-185">在操作窗格上，选择 **新建** 向 **概览** 选项卡添加一行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="77fe8-186">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-187">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="77fe8-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77fe8-188">**工作模板**：*51 越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="77fe8-189">**工作模板说明**：*51 越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="77fe8-190">选择 **保存** 激活 **工作模板详细信息** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77fe8-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="77fe8-191">在 **工作模板详细信息** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77fe8-192">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-193">**工作类型：** *领料*</span><span class="sxs-lookup"><span data-stu-id="77fe8-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="77fe8-194">**工作类 ID**：*CrossDock*</span><span class="sxs-lookup"><span data-stu-id="77fe8-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="77fe8-195">选择 **新建** 再添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="77fe8-196">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="77fe8-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="77fe8-197">**工作类 ID**：*CrossDock*</span><span class="sxs-lookup"><span data-stu-id="77fe8-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="77fe8-198">选择 **保存**，然后确认为 *51 越库配送* 模板选中了 **有效** 复选框。</span><span class="sxs-lookup"><span data-stu-id="77fe8-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="77fe8-199">*领料* 和 *放置* 工作类型的工作类 ID 必须相同。</span><span class="sxs-lookup"><span data-stu-id="77fe8-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="77fe8-200">创建货位指令</span><span class="sxs-lookup"><span data-stu-id="77fe8-200">Create location directives</span></span>

1. <span data-ttu-id="77fe8-201">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="77fe8-202">在左窗格中，将 **工作订单类型** 设置为 *越库配送*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="77fe8-203">在操作窗格中，选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="77fe8-204">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="77fe8-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77fe8-205">**名称**：*51 越库配送放置*</span><span class="sxs-lookup"><span data-stu-id="77fe8-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="77fe8-206">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="77fe8-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="77fe8-207">**站点：** *5*</span><span class="sxs-lookup"><span data-stu-id="77fe8-207">**Site:** *5*</span></span>
    - <span data-ttu-id="77fe8-208">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77fe8-209">选择 **保存** 激活 **行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77fe8-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="77fe8-210">在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77fe8-211">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-212">**起始数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="77fe8-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="77fe8-213">**目标数量：** *1000000*</span><span class="sxs-lookup"><span data-stu-id="77fe8-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="77fe8-214">选择 **保存** 激活 **货位指令操作** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77fe8-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="77fe8-215">在 **货位指令操作** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77fe8-216">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-217">**名称**：*Baydoor*</span><span class="sxs-lookup"><span data-stu-id="77fe8-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="77fe8-218">**固定货位使用情况**：*固定货位和非固定货位*</span><span class="sxs-lookup"><span data-stu-id="77fe8-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="77fe8-219">选择 **保存** 激活 **货位指令操作** 工具栏上的 **编辑查询** 按钮。</span><span class="sxs-lookup"><span data-stu-id="77fe8-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="77fe8-220">选择 **编辑查询** 打开查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="77fe8-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="77fe8-221">在 **范围** 选项卡上，确保配置下面的两行：</span><span class="sxs-lookup"><span data-stu-id="77fe8-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="77fe8-222">行 1：</span><span class="sxs-lookup"><span data-stu-id="77fe8-222">Line 1:</span></span>

        - <span data-ttu-id="77fe8-223">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="77fe8-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="77fe8-224">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="77fe8-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="77fe8-225">**字段**：*仓库*</span><span class="sxs-lookup"><span data-stu-id="77fe8-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="77fe8-226">**条件**：*51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="77fe8-227">行 2：</span><span class="sxs-lookup"><span data-stu-id="77fe8-227">Line 2:</span></span>

        - <span data-ttu-id="77fe8-228">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="77fe8-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="77fe8-229">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="77fe8-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="77fe8-230">**字段**：*货位*</span><span class="sxs-lookup"><span data-stu-id="77fe8-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="77fe8-231">**条件**：*Baydoor*</span><span class="sxs-lookup"><span data-stu-id="77fe8-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="77fe8-232">选择 **确定** 关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="77fe8-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="77fe8-233">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="77fe8-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="77fe8-234">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="77fe8-235">在左侧窗格中的菜单项列表内，选择 **采购储存**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="77fe8-236">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-236">Select **Edit**.</span></span>
1. <span data-ttu-id="77fe8-237">在 **工作类** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77fe8-238">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-239">**工作类 ID**：*CrossDock*</span><span class="sxs-lookup"><span data-stu-id="77fe8-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="77fe8-240">**工作订单类型**：*越库配送*</span><span class="sxs-lookup"><span data-stu-id="77fe8-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="77fe8-241">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="77fe8-242">应用场景</span><span class="sxs-lookup"><span data-stu-id="77fe8-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="77fe8-243">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="77fe8-243">Create a purchase order</span></span>

<span data-ttu-id="77fe8-244">执行以下步骤创建一个采购订单作为供应源。</span><span class="sxs-lookup"><span data-stu-id="77fe8-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="77fe8-245">转到 **采购 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="77fe8-246">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77fe8-247">在 **创建采购订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="77fe8-248">**供应商帐户**：*104*</span><span class="sxs-lookup"><span data-stu-id="77fe8-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="77fe8-249">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77fe8-250">选择 **确定**，并记下订单号。</span><span class="sxs-lookup"><span data-stu-id="77fe8-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="77fe8-251">将向 **采购订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="77fe8-252">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-253">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="77fe8-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="77fe8-254">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="77fe8-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="77fe8-255">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="77fe8-255">Create a sales order</span></span>

<span data-ttu-id="77fe8-256">执行以下步骤创建一个销售订单作为需求源。</span><span class="sxs-lookup"><span data-stu-id="77fe8-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="77fe8-257">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="77fe8-258">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77fe8-259">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="77fe8-260">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="77fe8-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="77fe8-261">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="77fe8-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77fe8-262">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-262">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-263">将向 **销售订单行** 快速选项卡添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77fe8-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="77fe8-264">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="77fe8-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="77fe8-265">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="77fe8-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="77fe8-266">**数量：** *3*</span><span class="sxs-lookup"><span data-stu-id="77fe8-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="77fe8-267">创建计划越库配送</span><span class="sxs-lookup"><span data-stu-id="77fe8-267">Create planned cross-docking</span></span>

<span data-ttu-id="77fe8-268">执行以下步骤根据销售订单创建计划越库配送。</span><span class="sxs-lookup"><span data-stu-id="77fe8-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="77fe8-269">在刚才创建的销售订单的 **销售订单详细信息** 页操作窗格中 **仓库** 选项卡上 **操作** 组内，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="77fe8-270">发放到仓库操作将为销售订单行创建装运和负荷行，并尝试分配库存。</span><span class="sxs-lookup"><span data-stu-id="77fe8-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="77fe8-271">您将收到参考消息。</span><span class="sxs-lookup"><span data-stu-id="77fe8-271">You receive an informational message.</span></span> <span data-ttu-id="77fe8-272">您还会收到以下警告消息：“未为波次 XXXX 创建任何工作。</span><span class="sxs-lookup"><span data-stu-id="77fe8-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="77fe8-273">有关详细信息，请参见工作创建历史记录日志。”</span><span class="sxs-lookup"><span data-stu-id="77fe8-273">See the work creation history log for details."</span></span> <span data-ttu-id="77fe8-274">这是正常行为，因为仓库中无库存。</span><span class="sxs-lookup"><span data-stu-id="77fe8-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="77fe8-275">在 **销售订单行** 快速选项卡上的 **仓库** 菜单中，选择 **装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="77fe8-276">将显示 **装运详细信息** 页面，其中显示为销售订单创建的装运。</span><span class="sxs-lookup"><span data-stu-id="77fe8-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="77fe8-277">请注意，**负荷行** 快速选项卡上的 **计划越库配送数量** 字段设置为 *3*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="77fe8-278">因为仓库中没有任何库存，但是在越库配送模板中定义的时间范围内将有一个有效供应源到达，所以创建了越库配送数量。</span><span class="sxs-lookup"><span data-stu-id="77fe8-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="77fe8-279">在 **负荷行** 快速选项卡中，选择 **计划越库配送** 查看创建的越库配送的详细信息。</span><span class="sxs-lookup"><span data-stu-id="77fe8-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="77fe8-280">处理越库配送</span><span class="sxs-lookup"><span data-stu-id="77fe8-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="77fe8-281">仓库移动应用中的采购订单收货</span><span class="sxs-lookup"><span data-stu-id="77fe8-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="77fe8-282">系统将接收采购订单中的 5 件并放入收货货位，再创建两份工作。</span><span class="sxs-lookup"><span data-stu-id="77fe8-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="77fe8-283">创建的第一个工作 ID 的 **工作订单类型** 值为 *越库配送*，并且该 ID 将链接到销售订单。</span><span class="sxs-lookup"><span data-stu-id="77fe8-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="77fe8-284">其数量为 3，并导向到最终装运货位，从而可以立即运出。</span><span class="sxs-lookup"><span data-stu-id="77fe8-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="77fe8-285">创建的第二个工作 ID 的 **工作订单类型** 值为 *采购订单*，并且该 ID 将链接到采购订单。</span><span class="sxs-lookup"><span data-stu-id="77fe8-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="77fe8-286">其未越库配送的剩余数量为 2，并将导向以储存。</span><span class="sxs-lookup"><span data-stu-id="77fe8-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="77fe8-287">以仓库 *51* 中的用户的身份登录移动设备。</span><span class="sxs-lookup"><span data-stu-id="77fe8-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="77fe8-288">转到 **入库 \> 采购收货**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="77fe8-289">在 **采购订单号** 字段中，输入您的采购订单号。</span><span class="sxs-lookup"><span data-stu-id="77fe8-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="77fe8-290">在 **数量** 字段中，输入 *5*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="77fe8-291">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-291">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-292">在下一页，将 **物料** 字段设置为 *A0001*。</span><span class="sxs-lookup"><span data-stu-id="77fe8-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="77fe8-293">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-293">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-294">在下一页，通过选择 **确定** 确认 **采购订单号**、**物料** 和 **数量** 值。</span><span class="sxs-lookup"><span data-stu-id="77fe8-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="77fe8-295">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="77fe8-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="77fe8-296">选择 **取消** 以退出。</span><span class="sxs-lookup"><span data-stu-id="77fe8-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="77fe8-297">储存以越库配送和批量处理</span><span class="sxs-lookup"><span data-stu-id="77fe8-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="77fe8-298">现在，两个工作 ID 的目标牌照相同。</span><span class="sxs-lookup"><span data-stu-id="77fe8-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="77fe8-299">若要完成后续步骤，必须获取工作 ID 和目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="77fe8-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="77fe8-300">可以从采购订单行和销售订单行的工作详细信息获取此信息。</span><span class="sxs-lookup"><span data-stu-id="77fe8-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="77fe8-301">也可以转到 **仓库管理 \> 工作 \> 工作详细信息**，然后筛选以查找其 **仓库** 值为 *51* 的工作。</span><span class="sxs-lookup"><span data-stu-id="77fe8-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="77fe8-302">在移动设备上，转到 **入库 \> 采购储存**，然后输入工作中的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="77fe8-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="77fe8-303">在 **ID** 字段中，输入工作详细信息中的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="77fe8-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="77fe8-304">越库配送领料页面显示领料货位 (*RECV*)、目标牌照（*牌照*）、物料 (*A0001*) 和数量 (*3*)。</span><span class="sxs-lookup"><span data-stu-id="77fe8-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="77fe8-305">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-305">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-306">在 **目标牌照** 字段中，输入应该放置（越库配送）到装运货位的牌照 ID 的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="77fe8-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="77fe8-307">可以选择所选任何牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="77fe8-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="77fe8-308">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-308">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-309">在下一页的 **ID** 字段中，输入目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="77fe8-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="77fe8-310">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-310">Select **OK**.</span></span>
1. <span data-ttu-id="77fe8-311">确认剩余数量 2 的领料工作，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="77fe8-312">在下一页上，选择 **完成** 结束领料流程，并开始储存流程。</span><span class="sxs-lookup"><span data-stu-id="77fe8-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="77fe8-313">移动应用将为您提供要将物料放置到的货位和牌照。</span><span class="sxs-lookup"><span data-stu-id="77fe8-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="77fe8-314">选择 **确定** 确认批量存储 **放置**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="77fe8-315">在下一页，选择 **确定** 确认越库配送 **放置**。</span><span class="sxs-lookup"><span data-stu-id="77fe8-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="77fe8-316">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="77fe8-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="77fe8-317">选择 **取消** 以退出。</span><span class="sxs-lookup"><span data-stu-id="77fe8-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="77fe8-318">下图显示 Microsoft Dynamics 365 Supply Chain Management 中可能如何显示已完成的越库配送工作。</span><span class="sxs-lookup"><span data-stu-id="77fe8-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="77fe8-319">![越库配送工作已完成](media/PlannedCrossDockingWork.png "越库配送工作已完成")</span><span class="sxs-lookup"><span data-stu-id="77fe8-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]