---
title: 确认并转移
description: 本主题介绍如何使用“确认并转移”功能，用户可在完成与负荷关联的所有工作之前，使用此功能将这些负荷运出仓库。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6104e457a62f340951c187d0f2dbe48b0dffdf7f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422765"
---
# <a name="confirm-and-transfer"></a><span data-ttu-id="d6c92-103">确认并转移</span><span class="sxs-lookup"><span data-stu-id="d6c92-103">Confirm and transfer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6c92-104">用户可在完成与负荷关联的所有工作之前，使用 *确认并转移* 将这些负荷运出仓库。</span><span class="sxs-lookup"><span data-stu-id="d6c92-104">The *Confirm and transfer* feature lets users ship loads out of the warehouse before they complete all the work that is associated with those loads.</span></span> <span data-ttu-id="d6c92-105">如果收到的装运中包含未完全领料的负荷行，系统将提示确认用户将剩余数量拆分到新负荷中或取消未完成数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-105">When a shipment is received that includes load lines that weren't fully picked, the confirming user is prompted either to split the remaining quantities onto a new load or to cancel the incomplete quantities.</span></span>

<span data-ttu-id="d6c92-106">设置为允许拆分负荷的系统支持以下场景：必须调整因为新情况或情况改变而必须调整计划的负荷或部分装载的负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-106">Systems that are set up to allow load splitting support scenarios where planned and partially loaded loads must be adapted because of new or changing circumstances.</span></span>

<span data-ttu-id="d6c92-107">客户端中包含让部分装载的负荷以已装运状态结束和确认的逻辑。</span><span class="sxs-lookup"><span data-stu-id="d6c92-107">The client includes logic that enables a partially loaded load to be closed and confirmed as shipped.</span></span> <span data-ttu-id="d6c92-108">然后，如果需要且设置也允许，将所有剩余装运和负荷行（包括完整或部分行数量）转移到新建的负荷和装运。</span><span class="sxs-lookup"><span data-stu-id="d6c92-108">All remaining shipments and load lines (including full or partial line quantities) are then rolled over to a newly created load and shipment, if this rollover is required and the setup allows for it.</span></span> <span data-ttu-id="d6c92-109">将根据装运和负荷的初始创建条件自动创建新装运和负荷，并且其主属性不变。</span><span class="sxs-lookup"><span data-stu-id="d6c92-109">New shipments and loads are automatically created based on the initial criteria for shipment and load creation, and their main attributes remain unchanged.</span></span> <span data-ttu-id="d6c92-110">如果尚未创建工作订单，而用户认为必须取消剩余数量，也可以通过一个选项自动取消这些数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-110">There is also an option to automatically cancel remaining quantities if a work order hasn't yet been created and the user deems this cancellation necessary.</span></span>

<span data-ttu-id="d6c92-111">此功能支持以下场景：一辆开车装不下所有负荷，或者部分负荷应该在其余负荷准备好装运之前离开仓库。</span><span class="sxs-lookup"><span data-stu-id="d6c92-111">This functionality supports scenarios where the full load doesn't fit onto a single truck, or where some of the load should leave the warehouse before the rest of the load is ready for shipment.</span></span> <span data-ttu-id="d6c92-112">在这些场景下，可以将剩余产品转移到新负荷，从而转移到新卡车。</span><span class="sxs-lookup"><span data-stu-id="d6c92-112">In these scenarios, the remaining products can be transferred to a new load and therefore to a new truck.</span></span> <span data-ttu-id="d6c92-113">因为此功能可以用于不然应该需要完整负荷装运的负荷，所以灵活性特别高，可帮助运输经理应对非常规场景或意外场景。</span><span class="sxs-lookup"><span data-stu-id="d6c92-113">Because this feature can be used with loads that are otherwise intended to require full-load shipment, it provides extra flexibility so that transport managers can solve nonstandard or unforeseen scenarios.</span></span>

<span data-ttu-id="d6c92-114">拆分负荷时，*确认并转移* 功能执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d6c92-114">When a load is split, the *Confirm and transfer* feature performs the following actions:</span></span>

- <span data-ttu-id="d6c92-115">因为需要，创建新负荷和装运。</span><span class="sxs-lookup"><span data-stu-id="d6c92-115">New loads and shipments are created as they are required.</span></span> <span data-ttu-id="d6c92-116">每个负荷或装运的大多数属性与原始负荷或装运的相同。</span><span class="sxs-lookup"><span data-stu-id="d6c92-116">Each load or shipment will have most of the same attributes as the original load or shipment.</span></span> <span data-ttu-id="d6c92-117">除了负荷状态，将根据工作状态重新计算负荷状态。</span><span class="sxs-lookup"><span data-stu-id="d6c92-117">The exception is the load status, which will be recalculated based on the work status.</span></span>
- <span data-ttu-id="d6c92-118">将通知用户，说明已创建了新负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-118">The user is informed that a new load has been created.</span></span> <span data-ttu-id="d6c92-119">还会通知用户新负荷的 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-119">The user is also notified about the ID of the new load.</span></span>
- <span data-ttu-id="d6c92-120">将使用新的负荷和装运信息更新拆分的负荷行、工作标题和工作行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-120">The load lines, work headers, and work lines that were split are updated with the new load and shipment information.</span></span>
- <span data-ttu-id="d6c92-121">如果拆分整个装运，将保留该装运，仅更新负荷引用。</span><span class="sxs-lookup"><span data-stu-id="d6c92-121">If a whole shipment is being split, the shipment is maintained, and only the load references are updated.</span></span> <span data-ttu-id="d6c92-122">如果必须拆分装运，将创建一个新装运。</span><span class="sxs-lookup"><span data-stu-id="d6c92-122">If the shipment must be split, a new shipment is created.</span></span>

<span data-ttu-id="d6c92-123">取消剩余数量时，将从负荷中删除尚未领料的和未与非取消工作关联的所有负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-123">When remaining quantities are canceled, any load line quantities that haven't been picked and that don't have non-canceled work associated with them are removed from the load.</span></span> <span data-ttu-id="d6c92-124">如果正在进行任何工作，则用户只能拆分负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-124">If any work is in process, the user can only split the load.</span></span> <span data-ttu-id="d6c92-125">不能取消剩余数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-125">Remaining quantities can't be canceled.</span></span>

<span data-ttu-id="d6c92-126">只能拆分满足下面的所有条件的负荷：</span><span class="sxs-lookup"><span data-stu-id="d6c92-126">You can split only loads that meet all the following criteria:</span></span>

- <span data-ttu-id="d6c92-127">一个或多个负荷行具有已领料数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-127">One or more load lines have picked quantities.</span></span>
- <span data-ttu-id="d6c92-128">负荷状态为低于已装载数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-128">The load status is less than loaded.</span></span>
- <span data-ttu-id="d6c92-129">无负荷行数据。</span><span class="sxs-lookup"><span data-stu-id="d6c92-129">There is no load line data.</span></span> <span data-ttu-id="d6c92-130">（此数据通过在暂存阶段合并牌照创建，而 *确认并转移* 功能不支持合并牌照。）</span><span class="sxs-lookup"><span data-stu-id="d6c92-130">(This data is created through license plate consolidation on the staging location, and the *Confirm and transfer* feature doesn't support license plate consolidation.)</span></span>
- <span data-ttu-id="d6c92-131">包装货位现在没有任何库存在等待包装。</span><span class="sxs-lookup"><span data-stu-id="d6c92-131">No inventory is currently awaiting packing at a packing location.</span></span> <span data-ttu-id="d6c92-132">（*确认并转移* 功能不支持已领到打包站但尚未打包的库存。）</span><span class="sxs-lookup"><span data-stu-id="d6c92-132">(The *Confirm and transfer* feature doesn't support inventory that has been picked to the pack station but hasn't yet been packed.)</span></span>

> [!NOTE]
> <span data-ttu-id="d6c92-133">此功能与运输负荷功能不同，后者在领料前不可计划和创建负荷，但是领料完成后使用可用运输空间装运的仓库中使用。</span><span class="sxs-lookup"><span data-stu-id="d6c92-133">This functionality differs from the transport load functionality, which should be used in warehouses that can never plan and create loads before picking, but that instead load the available transportation space after picking is completed.</span></span>
>
> <span data-ttu-id="d6c92-134">以下情况下使用 *确认并转移* 功能：通常提前规划和创建负荷，但是有时可用运输工具（如卡车）装不完负荷时除外。</span><span class="sxs-lookup"><span data-stu-id="d6c92-134">Use the *Confirm and transfer* feature in situations where loads are usually planned and created ahead of time, but where exceptions sometimes occur in which the load doesn't fit the available transport (such as a truck).</span></span>

## <a name="turn-on-confirm-and-transfer"></a><span data-ttu-id="d6c92-135">开启确认并转移功能</span><span class="sxs-lookup"><span data-stu-id="d6c92-135">Turn on confirm and transfer</span></span>

<span data-ttu-id="d6c92-136">*确认并转移* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="d6c92-136">Before you can use the *Confirm and transfer* feature, it must be turned on in your system.</span></span> <span data-ttu-id="d6c92-137">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="d6c92-137">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d6c92-138">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="d6c92-138">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d6c92-139">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="d6c92-139">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6c92-140">**功能名称**：*确认并转移*</span><span class="sxs-lookup"><span data-stu-id="d6c92-140">**Feature name:** *Confirm and transfer*</span></span>

## <a name="set-up-confirm-and-transfer"></a><span data-ttu-id="d6c92-141">设置确认并转移功能</span><span class="sxs-lookup"><span data-stu-id="d6c92-141">Set up confirm and transfer</span></span>

<span data-ttu-id="d6c92-142">若要使用 *确认并转移* 功能，必须在每个相关负荷模板中开启该功能。</span><span class="sxs-lookup"><span data-stu-id="d6c92-142">To use the *Confirm and transfer* feature, you must turn it on in every relevant load template.</span></span> <span data-ttu-id="d6c92-143">除外，还可能希望准备工作模板以支持此功能，具体取决于要求。</span><span class="sxs-lookup"><span data-stu-id="d6c92-143">In addition, depending on your requirements, you might want to prepare your work templates to support the feature.</span></span> <span data-ttu-id="d6c92-144">如果要完成本主题后文提供的示例场景，请按照本部分中的说明设置系统。</span><span class="sxs-lookup"><span data-stu-id="d6c92-144">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span> <span data-ttu-id="d6c92-145">（此场景基于 **USMF** 演示数据。）</span><span class="sxs-lookup"><span data-stu-id="d6c92-145">(That scenario is based on **USMF** demo data.)</span></span>

### <a name="prepare-your-load-templates"></a><span data-ttu-id="d6c92-146">准备负荷模板</span><span class="sxs-lookup"><span data-stu-id="d6c92-146">Prepare your load templates</span></span>

1. <span data-ttu-id="d6c92-147">转到 **仓库管理 \> 设置 \> 负荷 \> 负荷模板**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-147">Go to **Warehouse management \> Setup \> Load \> Load templates**.</span></span>
1. <span data-ttu-id="d6c92-148">在操作窗格上，选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="d6c92-148">On the Action Pane, select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="d6c92-149">选中要开启此功能的每个现有模板的 **允许装运确认期间拆分负荷** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-149">Select the **Allow load split during ship confirm** check box for each existing template where you want to turn on the feature.</span></span> <span data-ttu-id="d6c92-150">或者选择 **新建** 创建新模板，然后根据需要进行配置。</span><span class="sxs-lookup"><span data-stu-id="d6c92-150">Alternatively, select **New** to create a new template, and configure it as you require.</span></span> <span data-ttu-id="d6c92-151">使用该模板创建的每个负荷都将基础此功能。</span><span class="sxs-lookup"><span data-stu-id="d6c92-151">Every load that you create by using that template will inherit this functionality.</span></span> <span data-ttu-id="d6c92-152">（如果在使用 **USMF** 演示数据，请为 **20' 容器** 负荷模板开启此功能。）</span><span class="sxs-lookup"><span data-stu-id="d6c92-152">(If you're working with the **USMF** demo data, turn on the feature for the **20' Container** load template.)</span></span>

### <a name="prepare-your-work-templates"></a><span data-ttu-id="d6c92-153">准备工作模板</span><span class="sxs-lookup"><span data-stu-id="d6c92-153">Prepare your work templates</span></span>

<span data-ttu-id="d6c92-154">任何情况下均不需要进行此设置。</span><span class="sxs-lookup"><span data-stu-id="d6c92-154">This setup isn't required in all situations.</span></span> <span data-ttu-id="d6c92-155">此处的示例可以确保按装运分解工作以支持本主题后文提供的示例场景。</span><span class="sxs-lookup"><span data-stu-id="d6c92-155">The example that is shown here ensures that work can be broken by shipment to support the example scenario that is provided later in this topic.</span></span> <span data-ttu-id="d6c92-156">还可以通过其他方法取得此结果。</span><span class="sxs-lookup"><span data-stu-id="d6c92-156">There are also other ways to achieve this result.</span></span>

1. <span data-ttu-id="d6c92-157">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-157">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d6c92-158">在页面上部的网格中，选择要在其中设置 *确认并转移* 功能的现有工作模板。</span><span class="sxs-lookup"><span data-stu-id="d6c92-158">In the grid in the upper part of the page, select an existing work template where you want to set up the *Confirm and transfer* feature.</span></span> <span data-ttu-id="d6c92-159">（如果在使用 **USMF** 演示数据，请选择 **51 Pick to stage** 工作模板。）也可以创建新的工作模板。</span><span class="sxs-lookup"><span data-stu-id="d6c92-159">(If you're working with the **USMF** demo data, select the **51 Pick to stage** work template.) Alternatively, create a new work template.</span></span>
1. <span data-ttu-id="d6c92-160">在操作窗格上，选择 **编辑查询** 打开 **销售** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-160">On the Action Pane, select **Edit query** to open the **Sales** dialog box.</span></span>
1. <span data-ttu-id="d6c92-161">在 **销售** 对话框的 **排序** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-161">In the **Sales** dialog box, on the **Sorting** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="d6c92-162">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d6c92-162">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d6c92-163">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="d6c92-163">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="d6c92-164">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="d6c92-164">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="d6c92-165">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="d6c92-165">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="d6c92-166">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="d6c92-166">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="d6c92-167">选择 **确定** 保存设置并关闭 **销售** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-167">Select **OK** to save your settings and close the **Sales** dialog box.</span></span>
1. <span data-ttu-id="d6c92-168">如果收到消息说明将重置分组，请选择 **是** 继续操作。</span><span class="sxs-lookup"><span data-stu-id="d6c92-168">If you receive a message that states that grouping will be reset, select **Yes** to continue.</span></span>
1. <span data-ttu-id="d6c92-169">在 **工作模板** 页上部的网格中，选择刚才编辑的模板，然后在操作窗格中，选择 **工作标题分解**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-169">In the grid in the upper part of the **Work templates** page, select the template that you just edited, and then, on the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="d6c92-170">在操作窗格上，选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="d6c92-170">On the Action Pane, select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="d6c92-171">在网格中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d6c92-171">In the grid, set the following values:</span></span>

    - <span data-ttu-id="d6c92-172">**表名**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="d6c92-172">**Table name:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="d6c92-173">**字段名**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="d6c92-173">**Field name:** *Shipment ID*</span></span>
    - <span data-ttu-id="d6c92-174">**按此字段分组：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-174">**Group by this field:** Select this check box.</span></span>

1. <span data-ttu-id="d6c92-175">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-175">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d6c92-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d6c92-176">Close the page.</span></span>

## <a name="scenario"></a><span data-ttu-id="d6c92-177">应用场景</span><span class="sxs-lookup"><span data-stu-id="d6c92-177">Scenario</span></span>

<span data-ttu-id="d6c92-178">此场景显示以下示例：领料流程尚未完成，但是无论如何必须将已领物料装载到卡车上并装运。</span><span class="sxs-lookup"><span data-stu-id="d6c92-178">This scenario shows an example where the picking process isn't yet completed, but the items that have been picked so far must be loaded onto a truck and shipped anyway.</span></span> <span data-ttu-id="d6c92-179">因此，用户可以将未打包负荷行拆分到新负荷中。</span><span class="sxs-lookup"><span data-stu-id="d6c92-179">Therefore, the user can split the unpicked load lines onto a new load.</span></span> <span data-ttu-id="d6c92-180">然后将自动更新所有数据关系。</span><span class="sxs-lookup"><span data-stu-id="d6c92-180">All the data relationships will then automatically be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="d6c92-181">此场景中描述的具体值基于 **USMF** 演示数据。</span><span class="sxs-lookup"><span data-stu-id="d6c92-181">The specific values that are described in this scenario are based on the **USMF** demo data.</span></span> <span data-ttu-id="d6c92-182">监视在演示或了解如何使用此功能时使用这些演示数据。</span><span class="sxs-lookup"><span data-stu-id="d6c92-182">We recommend that you use this demo data while you're demonstrating or learning how to use the feature.</span></span> <span data-ttu-id="d6c92-183">如果不使用 **USMF** 演示数据，请根据需要替换为您自己的值。</span><span class="sxs-lookup"><span data-stu-id="d6c92-183">If you aren't using the **USMF** demo data, substitute your own values as required.</span></span>

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a><span data-ttu-id="d6c92-184">步骤 1：创建具有多个负荷行的负荷</span><span class="sxs-lookup"><span data-stu-id="d6c92-184">Step 1: Create a load that has multiple load lines</span></span>

<span data-ttu-id="d6c92-185">必须有包含多个负荷行的负荷，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="d6c92-185">Before you can use this functionality, you must have a load that contains multiple load lines.</span></span> <span data-ttu-id="d6c92-186">还必须确保领料货位有满足将创建的销售订单上的所有物料的足够库存。</span><span class="sxs-lookup"><span data-stu-id="d6c92-186">You must also make sure that the pick locations have enough inventory for all the items on the sales orders that you will create.</span></span> <span data-ttu-id="d6c92-187">检查货位指令的设置（**仓库管理 \> 设置 \> 货位指令**），并记下用于销售订单领料的领料货位。</span><span class="sxs-lookup"><span data-stu-id="d6c92-187">Review the setup of the location directive (**Warehouse management \> Setup \> Location directives**), and make a note of the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="d6c92-188">如果必须调整库存，请根据需要创建手动移动，使用补货，或使用其他任何流。</span><span class="sxs-lookup"><span data-stu-id="d6c92-188">If you must adjust the inventory, create manual movements, use replenishment, or use any other flow, as required.</span></span>

<span data-ttu-id="d6c92-189">若要创建授予资格负荷，请首先执行以下步骤创建三个销售订单。</span><span class="sxs-lookup"><span data-stu-id="d6c92-189">To create a qualifying load, first create three sales orders by following these steps.</span></span>

1. <span data-ttu-id="d6c92-190">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-190">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6c92-191">在操作窗格上，选择 **新建** 以打开 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-191">On the Action Pane, select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="d6c92-192">在 **创建销售订单** 对话框中，（至少）设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d6c92-192">In the **Create sales order** dialog box, set the following values (at a minimum):</span></span>

    - <span data-ttu-id="d6c92-193">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-004* (*Cave Wholesales*)。</span><span class="sxs-lookup"><span data-stu-id="d6c92-193">On the **Customer** FastTab, set the **Customer account** field to *US-004* (*Cave Wholesales*).</span></span>
    - <span data-ttu-id="d6c92-194">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 *51*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-194">On the **General** FastTab, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="d6c92-195">选择 **确定** 创建销售订单，然后关闭 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-195">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="d6c92-196">将打开您的新销售订单。</span><span class="sxs-lookup"><span data-stu-id="d6c92-196">Your new sales order is opened.</span></span> <span data-ttu-id="d6c92-197">在 **销售订单行** 网格中，添加具有以下值的行：</span><span class="sxs-lookup"><span data-stu-id="d6c92-197">In the **Sales order lines** grid, add a line that has the following values:</span></span>

    - <span data-ttu-id="d6c92-198">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="d6c92-198">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="d6c92-199">**数量：** *40*</span><span class="sxs-lookup"><span data-stu-id="d6c92-199">**Quantity:** *40*</span></span>
    - <span data-ttu-id="d6c92-200">**单位：** *ea*</span><span class="sxs-lookup"><span data-stu-id="d6c92-200">**Unit:** *ea*</span></span>

1. <span data-ttu-id="d6c92-201">在网格上方的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-201">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d6c92-202">在操作窗格上，选择 **预留批次** 打开 **预留** 页面。</span><span class="sxs-lookup"><span data-stu-id="d6c92-202">On the Action Pane, select **Reserve lot** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="d6c92-203">预留销售行中的库存，然后关闭 **预留** 页面。</span><span class="sxs-lookup"><span data-stu-id="d6c92-203">Reserve the inventory on the sales line, and then close the **Reservation** page.</span></span>
1. <span data-ttu-id="d6c92-204">重复步骤 1 到 4，为相同客户和仓库添加第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="d6c92-204">Repeat steps 1 through 4 to add a second sales order for the same customer and warehouse.</span></span>
1. <span data-ttu-id="d6c92-205">添加两个具有以下值的销售行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-205">Add two sales lines that have the following values.</span></span> <span data-ttu-id="d6c92-206">添加各行后，按照步骤 6 到 8 中的说明预留库存。</span><span class="sxs-lookup"><span data-stu-id="d6c92-206">After you add each line, reserve inventory for it as described in steps 6 through 8.</span></span>

    - <span data-ttu-id="d6c92-207">**行 1：** 将 **物料编号** 字段设置为 *M9200*，将 **数量** 字段设置为 *30*，将 **单位** 字段设置为 *个*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-207">**Line 1:** Set the **Item number** field to *M9200*, the **Quantity** field to *30*, and the **Unit** field to *ea*.</span></span>
    - <span data-ttu-id="d6c92-208">**行 2：** 将 **物料编号** 字段设置为 *M9201*，将 **数量** 字段设置为 *20*，将 **单位** 字段设置为 *个*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-208">**Line 2:** Set the **Item number** field to *M9201*, the **Quantity** field to *20*, and the **Unit** field to *ea*.</span></span>

1. <span data-ttu-id="d6c92-209">重复步骤 1 到 4，为相同客户和仓库添加第三个销售订单。</span><span class="sxs-lookup"><span data-stu-id="d6c92-209">Repeat steps 1 through 4 to add a third sales order for the same customer and warehouse.</span></span>
1. <span data-ttu-id="d6c92-210">添加两个具有以下值的销售行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-210">Add two sales lines that have the following values.</span></span> <span data-ttu-id="d6c92-211">添加各行后，按照步骤 6 到 8 中的说明预留库存。</span><span class="sxs-lookup"><span data-stu-id="d6c92-211">After you add each line, reserve inventory for it as described in steps 6 through 8.</span></span>

    - <span data-ttu-id="d6c92-212">**行 1：** 将 **物料编号** 字段设置为 *M9201*，将 **数量** 字段设置为 *20*，将 **单位** 字段设置为 *个*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-212">**Line 1:** Set the **Item number** field to *M9201*, the **Quantity** field to *20*, and the **Unit** field to *ea*.</span></span>
    - <span data-ttu-id="d6c92-213">**行 2：** 将 **物料编号** 字段设置为 *M9202*，将 **数量** 字段设置为 *60*，将 **单位** 字段设置为 *个*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-213">**Line 2:** Set the **Item number** field to *M9202*, the **Quantity** field to *60*, and the **Unit** field to *ea*.</span></span>

#### <a name="load-planning-workbench"></a><span data-ttu-id="d6c92-214">装载计划工作台</span><span class="sxs-lookup"><span data-stu-id="d6c92-214">Load planning workbench</span></span>

<span data-ttu-id="d6c92-215">负荷计划工作台将使用负荷模板 ID 生成装运，并将销售订单行发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="d6c92-215">The load planning workbench will use the load template ID to build the shipments and release the sales order lines to the warehouse.</span></span>

1. <span data-ttu-id="d6c92-216">转到 **仓库管理 \> 装载 \> 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-216">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="d6c92-217">在 **仓库** 字段中，选择 *51*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-217">In the **Warehouse** field, select *51*.</span></span>

    <span data-ttu-id="d6c92-218">现在将生成您刚创建的销售订单的负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-218">You will now build the load for the sales orders that you just created.</span></span>

1. <span data-ttu-id="d6c92-219">在 **销售行** 选项卡的网格中，选择新销售订单的销售行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-219">On the **Sales lines** tab, in the grid, select the sales lines for the new sales orders.</span></span>
1. <span data-ttu-id="d6c92-220">在操作窗格上 **供应与需求** 选项卡上 **添加** 组中，选择 **至新负荷**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-220">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="d6c92-221">在 **负荷模板分配** 对话框中，在 **负荷模板 ID** 字段中，选择 *20' 容器*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-221">In the **Load template assignment** dialog box, in the **Load template ID** field, select *20' Container*.</span></span>
1. <span data-ttu-id="d6c92-222">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-222">Select **OK**.</span></span>
1. <span data-ttu-id="d6c92-223">在 **负荷计划工作台** 页面 **负荷** 部分的网格中，找到为仓库 *51* 新建的负荷 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-223">In the **Loads** section of the **Load planning workbench** page, in the grid, find the newly created load ID for warehouse *51*.</span></span> <span data-ttu-id="d6c92-224">向右滚动，直到看到 **允许装运确认期间拆分负荷** 列。</span><span class="sxs-lookup"><span data-stu-id="d6c92-224">Scroll right until you see the **Allow load split during ship confirm** column.</span></span> <span data-ttu-id="d6c92-225">应该选中您的负荷的复选框。</span><span class="sxs-lookup"><span data-stu-id="d6c92-225">The check box should be selected for your load.</span></span>
1. <span data-ttu-id="d6c92-226">选择负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-226">Select the load.</span></span>
1. <span data-ttu-id="d6c92-227">在网格上方的 **下达** 菜单中，选择 **发放到仓库** 以创建工作。</span><span class="sxs-lookup"><span data-stu-id="d6c92-227">On the **Release** menu above the grid, select **Release to warehouse** to create work.</span></span>
1. <span data-ttu-id="d6c92-228">在 **将负荷发放到仓库** 对话框中，验证 **要包括的记录** 快速选项卡显示您的负荷 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-228">In the **Release load to warehouse** dialog box, verify that the **Records to include** FastTab shows your load ID.</span></span>
1. <span data-ttu-id="d6c92-229">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-229">Select **OK**.</span></span>

    <span data-ttu-id="d6c92-230">在系统创建装运和工作时，您可能会收到“正在处理操作”消息。</span><span class="sxs-lookup"><span data-stu-id="d6c92-230">You might receive a "Processing operation" message while the system creates the shipments and work.</span></span>

1. <span data-ttu-id="d6c92-231">在 **负荷计划工作台** 页面的 **负荷** 部分中，您的负荷现在的负荷状态应该为 *已分波次*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-231">In the **Loads** section of the **Load planning workbench** page, your load should now have a load status of *Waved*.</span></span> <span data-ttu-id="d6c92-232">选择负荷，然后在网格上方的 **相关信息** 菜单中，选择 **波次详细信息** 查看创建的装运 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-232">Select the load, and then, on the **Related information** menu above the grid, select **Wave details** to view the shipment IDs that were created.</span></span> <span data-ttu-id="d6c92-233">完成后，关闭 **波次** 页面。</span><span class="sxs-lookup"><span data-stu-id="d6c92-233">When you've finished, close the **Waves** page.</span></span>
1. <span data-ttu-id="d6c92-234">在 **负荷计划工作台** 页面的 **负荷** 部分中，选择负荷，然后在网格上方的 **相关信息** 菜单中，选择 **工作详细信息** 查看为销售订单创建的工作。</span><span class="sxs-lookup"><span data-stu-id="d6c92-234">In the **Loads** section of the **Load planning workbench** page, select the load, and then, on the **Related information** menu above the grid, select **Work details** to view the work that was created for the sales orders.</span></span>
1. <span data-ttu-id="d6c92-235">记下创建的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-235">Make a note of the work IDs that were created.</span></span> <span data-ttu-id="d6c92-236">可能必须向右滚动才能看到与工作 ID 关联的销售订单编号和装运 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-236">You might have to scroll right to see the sales order number and shipment ID that are associated with the work ID.</span></span>

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a><span data-ttu-id="d6c92-237">步骤 2：设置适用于移动设备的执行流</span><span class="sxs-lookup"><span data-stu-id="d6c92-237">Step 2: Set up the execution flow for mobile devices</span></span>

<span data-ttu-id="d6c92-238">移动设备任务需要用户输入信息，如工作 ID 或牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-238">Mobile device tasks will require user input of information, such as the work ID or license plate ID.</span></span> <span data-ttu-id="d6c92-239">在字段中，通常以文档、包装或搭架上的条形码的形式提供给仓库用户。</span><span class="sxs-lookup"><span data-stu-id="d6c92-239">In the fields, this information is typically provided for warehouse users in the form of bar codes that are found on documentation, packaging, or racking.</span></span> <span data-ttu-id="d6c92-240">若要完成场景的移动设备步骤，请确保在事务中识别事务的工作 ID，以及物料和货位的牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-240">To complete the mobile device steps for scenarios, make sure that you've identified the work IDs for the transactions, and the license plate IDs for the item and location in the transactions.</span></span>

1. <span data-ttu-id="d6c92-241">使用仓库 *51* 的用户 ID 和密码登录移动设备。</span><span class="sxs-lookup"><span data-stu-id="d6c92-241">Sign in to the mobile device by using a user ID and password for warehouse *51*.</span></span>
1. <span data-ttu-id="d6c92-242">选择 **出库**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-242">Select **Outbound**.</span></span>
1. <span data-ttu-id="d6c92-243">选择 **销售领料**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-243">Select **Sales Picking**.</span></span>
1. <span data-ttu-id="d6c92-244">可选择输入工作 ID 或牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-244">You have the option to enter the work ID or the license plate ID.</span></span> <span data-ttu-id="d6c92-245">输入第一个销售订单的工作 ID，然后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-245">Enter the work ID for the first sales order, and then select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-246">在 **货位** 字段中，输入显示的货位以确认领料货位。</span><span class="sxs-lookup"><span data-stu-id="d6c92-246">In the **Loc** field, enter the location that is shown to confirm the picking location.</span></span> <span data-ttu-id="d6c92-247">然后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-247">Then select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-248">在 **牌照** 字段中，输入牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-248">In the **LP** field, enter the license plate ID.</span></span> <span data-ttu-id="d6c92-249">牌照 ID 必须是物料、仓库和正在从所选货位领取的物料货位的匹配项。</span><span class="sxs-lookup"><span data-stu-id="d6c92-249">The license plate ID must be a match for the item, warehouse, and location of the item that is being picked from the selected location.</span></span> <span data-ttu-id="d6c92-250">当您完成时，选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-250">When you've finished, select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-251">在 **物料** 字段中，输入物料编号确认正在领取物料，然后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-251">In the **Item** field, enter the item number to confirm the item that is being picked, and then select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-252">在 **数量** 字段中，输入正在领取的物料的数量，然后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-252">In the **Qty** field, enter the quantity of the item that is being picked, and then select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-253">在 **目标牌照** 字段中，输入目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-253">In the **Target LP** field, enter a target license plate ID.</span></span> <span data-ttu-id="d6c92-254">目标牌照是用户定义的。</span><span class="sxs-lookup"><span data-stu-id="d6c92-254">Target license plates are user-defined.</span></span> <span data-ttu-id="d6c92-255">务必输入可记住的牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-255">Be sure to enter a license plate ID that you will remember.</span></span> <span data-ttu-id="d6c92-256">建议使用当前日期加两位数序列 (YYMMDD\#\#) 作为格式，如 *19112301*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-256">We recommend that you use the current date plus a two-digit sequence (YYMMDD\#\#) as the format, such as *19112301*.</span></span> <span data-ttu-id="d6c92-257">当您完成时，选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-257">When you've finished, select **Enter**.</span></span>
1. <span data-ttu-id="d6c92-258">查看显示的信息。</span><span class="sxs-lookup"><span data-stu-id="d6c92-258">Review information that is shown.</span></span> <span data-ttu-id="d6c92-259">此信息是现在将成为放置事务的 *放置* 数据的 *领料* 信息。</span><span class="sxs-lookup"><span data-stu-id="d6c92-259">This information is the *Pick* information that will now become the *Put* data for the put transaction.</span></span> <span data-ttu-id="d6c92-260">当您完成时，选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-260">When you've finished, select **Enter**.</span></span>

    - <span data-ttu-id="d6c92-261">您将收到 **工作已完成** 消息。</span><span class="sxs-lookup"><span data-stu-id="d6c92-261">You receive a **Work Completed** message.</span></span>

1. <span data-ttu-id="d6c92-262">为第二个销售订单的工作 ID 重复步骤 4 到 10。</span><span class="sxs-lookup"><span data-stu-id="d6c92-262">Repeat steps 4 through 10 for the work ID of the second sales order.</span></span>

<span data-ttu-id="d6c92-263">下一步是将领到的两个牌照装载到卡车中。</span><span class="sxs-lookup"><span data-stu-id="d6c92-263">The next step is to load the two picked license plates to the truck.</span></span>

1. <span data-ttu-id="d6c92-264">使用仓库 *51* 的用户 ID 和密码登录移动设备。</span><span class="sxs-lookup"><span data-stu-id="d6c92-264">Sign in to the mobile device by using a user ID and password for warehouse *51*.</span></span>
1. <span data-ttu-id="d6c92-265">选择 **出库**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-265">Select **Outbound**.</span></span>
1. <span data-ttu-id="d6c92-266">选择 **销售装载**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-266">Select **Sales Loading**.</span></span>
1. <span data-ttu-id="d6c92-267">输入在上一个过程中为第一个工作 ID 创建的用户定义的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-267">Enter the user-defined target license plate ID that you created for the first work ID in the previous procedure.</span></span> <span data-ttu-id="d6c92-268">然后选择 **输入** 将目标牌照放入 **STAGE** 位置。</span><span class="sxs-lookup"><span data-stu-id="d6c92-268">Then select **Enter** to put the target license plate into the **STAGE** location.</span></span>
1. <span data-ttu-id="d6c92-269">再次输入目标牌照 ID，然后选择 **输入** 将牌照放入 **BAYDOOR** 货位。</span><span class="sxs-lookup"><span data-stu-id="d6c92-269">Enter the target license plate ID again, and then select **Enter** to put the license plate into the **BAYDOOR** location.</span></span>
1. <span data-ttu-id="d6c92-270">对为第二个工作 ID 创建的目标牌照 ID 重复步骤 4 到 5。</span><span class="sxs-lookup"><span data-stu-id="d6c92-270">Repeat steps 4 through 5 for the target license plate ID that you created for the second work ID.</span></span>

<span data-ttu-id="d6c92-271">现在将结束（装载）这两个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-271">The two work IDs will now be closed (loaded).</span></span>

### <a name="step-3-confirm-the-outbound-shipment"></a><span data-ttu-id="d6c92-272">步骤 3：确认出库装运</span><span class="sxs-lookup"><span data-stu-id="d6c92-272">Step 3: Confirm the outbound shipment</span></span>

<span data-ttu-id="d6c92-273">在此步骤中，将确认这两个销售订单和已经为负荷完成的工作，以便装运领取的负荷物料和为未领物料创建新负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-273">In this step, you will confirm the two sales orders and work that have been completed for the load to ship the picked items of the load and create a new load for the unpicked items.</span></span> <span data-ttu-id="d6c92-274">必须在 **负荷详细信息** 页面中进行出库装运确认。</span><span class="sxs-lookup"><span data-stu-id="d6c92-274">Outbound shipment confirmation must be done on the **Load details** page.</span></span>

1. <span data-ttu-id="d6c92-275">转到 **仓库管理 \> 装载 \> 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-275">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="d6c92-276">在 **负荷** 部分的网格中，为创建的负载 ID 选择行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-276">In the **Loads** section, in the grid, select the row for the load ID that you created.</span></span>
1. <span data-ttu-id="d6c92-277">选择负荷 ID 链接打开 **负荷详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="d6c92-277">Select the load ID link to open the **Load details** page.</span></span>
1. <span data-ttu-id="d6c92-278">在 **负荷详细信息** 页操作窗格中 **装运与收货** 选项卡上的 **确认** 组中，选择 **出库装运** 开始确认。</span><span class="sxs-lookup"><span data-stu-id="d6c92-278">On the **Load details** page, on the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Outbound shipment** to initiate the confirmation.</span></span>
1. <span data-ttu-id="d6c92-279">在 **装运确认** 对话框的 **装运确认期间的负荷拆分方法** 字段中，选择 *将数量拆分至新负荷*。</span><span class="sxs-lookup"><span data-stu-id="d6c92-279">In the **Ship confirm** dialog box, in the **Load split method during ship confirm** field, select *Split quantity to new load*.</span></span>
1. <span data-ttu-id="d6c92-280">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6c92-280">Select **OK**.</span></span>

    <span data-ttu-id="d6c92-281">您可能会收到“正在处理操作”消息。</span><span class="sxs-lookup"><span data-stu-id="d6c92-281">You might receive a "Processing operation" message.</span></span>

    <span data-ttu-id="d6c92-282">您将收到参考消息，说明已确认负荷的装运，并且已经根据拆分数量创建了新负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-282">You receive informational messages that indicate that the shipment for your load has been confirmed, and that a new load has been created from the split quantity.</span></span>

<span data-ttu-id="d6c92-283">刷新 **负荷计划工作台** 页面查看新建的负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-283">Refresh the **Load planning workbench** page to see the newly created load.</span></span>

<span data-ttu-id="d6c92-284">也可以按照下面的方法确认已更新了事务关系：</span><span class="sxs-lookup"><span data-stu-id="d6c92-284">You can also confirm that transaction relations have been updated in the following ways:</span></span>

- <span data-ttu-id="d6c92-285">使用新负荷 ID 更新了剩余（即未处理的）装运和装运行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-285">The remaining (unprocessed) shipment and shipment lines are updated with the new load ID.</span></span>
- <span data-ttu-id="d6c92-286">销售订单已链接到新负荷 ID。</span><span class="sxs-lookup"><span data-stu-id="d6c92-286">The sales order is linked to the new load ID.</span></span>
- <span data-ttu-id="d6c92-287">原始负荷中不包含剩余负荷行。</span><span class="sxs-lookup"><span data-stu-id="d6c92-287">The original load doesn't include the remaining load lines.</span></span>
- <span data-ttu-id="d6c92-288">已经使用新负荷 ID 更新了剩余工作。</span><span class="sxs-lookup"><span data-stu-id="d6c92-288">The remaining work has been updated with the new load ID.</span></span>
- <span data-ttu-id="d6c92-289">波次保持不变。</span><span class="sxs-lookup"><span data-stu-id="d6c92-289">The wave remains the same.</span></span>
- <span data-ttu-id="d6c92-290">已正确更新了新负荷的状态。</span><span class="sxs-lookup"><span data-stu-id="d6c92-290">The status of the new load is correctly updated.</span></span> <span data-ttu-id="d6c92-291">（如果工作状态为 _进行中_，负荷状态也应该为 _进行中_。）</span><span class="sxs-lookup"><span data-stu-id="d6c92-291">(If the work status is _In process_, the load status should also be _In process_.)</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="d6c92-292">说明和提示</span><span class="sxs-lookup"><span data-stu-id="d6c92-292">Notes and tips</span></span>

- <span data-ttu-id="d6c92-293">也可以在关闭了 **负荷模板** 参数的情况下创建了负荷之后，但是在开始执行装载流程之前，开启 **允许装运确认期间拆分负荷** 参数。</span><span class="sxs-lookup"><span data-stu-id="d6c92-293">You can also turn on the **Allow load split during ship confirm** parameter after the load has been created with the **Load template** parameter turned off but before the loading process has started.</span></span> <span data-ttu-id="d6c92-294">转到所需负荷，然后在标题视图中开启该参数。</span><span class="sxs-lookup"><span data-stu-id="d6c92-294">Go to the desired load, and then, in the header view, turn on the parameter.</span></span>
- <span data-ttu-id="d6c92-295">当部分剩余工作标题的状态为 *进行中* 时，也可以使用 **将数量拆分到新负荷** 选项。</span><span class="sxs-lookup"><span data-stu-id="d6c92-295">The **Split quantity to new load** option also works when some of the remaining work headers have a status of *In process*.</span></span> <span data-ttu-id="d6c92-296">因此，即使工作人员仍在使用领料单，也可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="d6c92-296">Therefore, you can still use the functionality even if workers are already running the pick orders.</span></span>
- <span data-ttu-id="d6c92-297">如果在有剩余工作的状态为 *未结* 或 *进行中* 的情况下选择 **取消未履行数量**，将收到以下错误消息：“无法取消负荷的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="d6c92-297">If you select **Cancel unfulfilled quantity** while there is remaining work that has a status of *Open* or *In progress*, you receive the following error message: "Unable to cancel remaining qty for load.</span></span> <span data-ttu-id="d6c92-298">负荷有工作。”</span><span class="sxs-lookup"><span data-stu-id="d6c92-298">Work exists for load."</span></span>
- <span data-ttu-id="d6c92-299">如果在不存在剩余工作，但是负荷中有未下达负荷行的情况下选择 **取消未履行数量**，将收到以下错误消息：“无法确认负荷的装运，因为物料的数量超过了定义的待交付百分比。”</span><span class="sxs-lookup"><span data-stu-id="d6c92-299">If you select **Cancel unfulfilled quantity** when there is no remaining work but there are unreleased load lines on the load, you receive the following error message: "The shipment for load could not be confirmed because the quantity for item exceeds the percentage that is defined for under delivery."</span></span> <span data-ttu-id="d6c92-300">若要避免此错误，可以将未下达负荷行中的 **待交付** 百分比设置为 100%。</span><span class="sxs-lookup"><span data-stu-id="d6c92-300">To avoid the error, you can set the **Under delivery** percentage on the unreleased load line to 100 percent.</span></span> <span data-ttu-id="d6c92-301">不会将未下达行移到新负荷，但是将使用待交付确认当前负荷。</span><span class="sxs-lookup"><span data-stu-id="d6c92-301">Unreleased lines won't be moved to a new load, but the current load will be confirmed with under-delivery.</span></span> <span data-ttu-id="d6c92-302">在这种情况下，不能重新下达原始订单。</span><span class="sxs-lookup"><span data-stu-id="d6c92-302">In this case, you won't be able to re-release the original order.</span></span> <span data-ttu-id="d6c92-303">因此，必须以其他方式处理。</span><span class="sxs-lookup"><span data-stu-id="d6c92-303">Therefore, so you will have to handle it in some other way.</span></span>
