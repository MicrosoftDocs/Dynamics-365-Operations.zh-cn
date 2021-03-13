---
title: 手动创建的工作订单
description: 本主题介绍如何在资产管理中手动创建工作订单。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017860"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="487e7-103">手动创建的工作订单</span><span class="sxs-lookup"><span data-stu-id="487e7-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="487e7-104">可以通过两种途径手动创建工作订单：</span><span class="sxs-lookup"><span data-stu-id="487e7-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="487e7-105">在 **所有工作订单** 或 **有效工作订单** 页面</span><span class="sxs-lookup"><span data-stu-id="487e7-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="487e7-106">在 **所有维护请求**、**有效维护请求** 或 **我的功能位置维护请求** 页面</span><span class="sxs-lookup"><span data-stu-id="487e7-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="487e7-107">创建工作订单</span><span class="sxs-lookup"><span data-stu-id="487e7-107">Create work order</span></span>

1. <span data-ttu-id="487e7-108">选择 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="487e7-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="487e7-109">Select **New**.</span></span>

3. <span data-ttu-id="487e7-110">在 **创建工作订单** 对话框中，在 **工作订单类型** 字段中选择工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="487e7-111">如果需要，选择一个 **描述**。</span><span class="sxs-lookup"><span data-stu-id="487e7-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="487e7-112">在 **资产** 字段中选择资产。</span><span class="sxs-lookup"><span data-stu-id="487e7-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="487e7-113">选择资产时，**资产** 下拉菜单中可能会提供三个选项卡：</span><span class="sxs-lookup"><span data-stu-id="487e7-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="487e7-114">**有效资产** - 此选项卡中包含资产生命周期状态为“有效”的所有资产的列表。</span><span class="sxs-lookup"><span data-stu-id="487e7-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="487e7-115">**资产视图** - 此选项卡显示功能位置及其中安装的资产的树视图。</span><span class="sxs-lookup"><span data-stu-id="487e7-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="487e7-116">**我的资产** - 此选项卡中包含与可能分配给您（即已登录系统的工作人员）的功能位置关联的资产。</span><span class="sxs-lookup"><span data-stu-id="487e7-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="487e7-117">（有关设置的信息，请参阅 [维护工人和工作人员组](../setup-for-objects/workers-and-worker-groups.md)。）如果在 [维护工人和工作人员组](../setup-for-objects/workers-and-worker-groups.md)中未在工作人员上设置功能位置，则 **我的资产** 选项卡不可用。</span><span class="sxs-lookup"><span data-stu-id="487e7-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="487e7-118">在 **维护作业类型** 字段中，选择工作订单的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="487e7-119">如果需要，请选择 **维护作业类型变型** 和 **工种**。</span><span class="sxs-lookup"><span data-stu-id="487e7-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="487e7-120">如果需要，可以在 **服务级别** 字段中更改工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="487e7-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="487e7-121">在相关字段中选择 **预计开始** 和 **预计结束** 日期。</span><span class="sxs-lookup"><span data-stu-id="487e7-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="487e7-122">单击 **确定** 以创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="487e7-123">在 **所有工作订单** 列表页上，您可以根据需要编辑工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="487e7-124">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="487e7-124">Note the following points:</span></span>

- <span data-ttu-id="487e7-125">在 **所有工作订单** 列表页的详细信息视图中，可以向工作订单添加多个资产，方法是在 **工作订单维护作业** 快速选项卡上添加行。</span><span class="sxs-lookup"><span data-stu-id="487e7-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="487e7-126">对于资产，您只能选择对为该资产选择的资产类型定义的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="487e7-127">如果在工作订单中使用资产后更改了资产服务级别或资产关键性，将不会相应更新工作订单中的服务级别或关键性。</span><span class="sxs-lookup"><span data-stu-id="487e7-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="487e7-128">有关服务级别和关键性的详细信息，请参阅[资产服务级别](../setup-for-objects/object-priorities.md)和[资产关键性类型](../setup-for-objects/object-criticalities.md)。</span><span class="sxs-lookup"><span data-stu-id="487e7-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="487e7-129">只要在工作订单中添加或删除工作订单作业，都将重新计算该工作订单中的关键性。</span><span class="sxs-lookup"><span data-stu-id="487e7-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="487e7-130">可在 **所有工作订单** 详细信息视图 > **标题** 选项卡 > **计划** 快速选项卡上的 **负责组** 或 **负责人** 字段中选择负责维护工人组或负责维护工人。</span><span class="sxs-lookup"><span data-stu-id="487e7-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="487e7-131">这些设置可以在工作订单活动时更改。</span><span class="sxs-lookup"><span data-stu-id="487e7-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="487e7-132">例如，当工作订单生命周期状态更改时，可以更改它们。</span><span class="sxs-lookup"><span data-stu-id="487e7-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="487e7-133">创建工作订单期间进行的自动选择基于 **负责的维护工人** 页面的设置。</span><span class="sxs-lookup"><span data-stu-id="487e7-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="487e7-134">如果在创建工作订单之后添加或删除工作订单作业，并且更新该工作订单时 **负责组** 和 **负责人** 字段为空，资产管理将尝试在设置页面上查找负责维护工人组或负责维护工人以寻找可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="487e7-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="487e7-135">如果更新工作订单时已经设置了 **负责组** 或 **负责人** 字段，则不进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="487e7-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="487e7-136">有关负责维护工人和工作人员组的详细信息，请参阅[负责维护工人](../setup-for-maintenance-requests/responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="487e7-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="487e7-137">从[维护状态](../controlling-and-reporting/maintenance-status.md)页面，可创建计算以获取传入工作订单和已完成工作订单的工作负载的概览。</span><span class="sxs-lookup"><span data-stu-id="487e7-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="487e7-138">在 **所有工作订单** 页面的详细信息视图中的 **行明细** 快速选项卡上，您可以使用 **纬度** 和 **经度** 字段为在工作订单作业上选择的资产添加地理坐标。</span><span class="sxs-lookup"><span data-stu-id="487e7-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="487e7-139">创建相关工作订单</span><span class="sxs-lookup"><span data-stu-id="487e7-139">Create related work order</span></span>

<span data-ttu-id="487e7-140">您可以创建与现有工作订单相关的工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="487e7-141">比如，如果要处理主工作订单和次级工作订单，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="487e7-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="487e7-142">新工作订单基于现有工作订单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="487e7-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="487e7-143">选择 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="487e7-144">选择要创建相关工作订单的工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="487e7-145">在“操作窗格”的 **工作订单** 选项卡上的 **新** 组中，选择 **相关工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="487e7-146">在 **创建相关工作订单** 对话框的 **工作订单作业** 字段中，选择要为其创建相关工作订单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="487e7-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="487e7-147">在 **维护作业类型** 字段中，选择维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="487e7-148">在 **维护作业类型变型** 和 **工种** 字段中，根据需要选择相关维护作业类型变型和工种。</span><span class="sxs-lookup"><span data-stu-id="487e7-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="487e7-149">如果此工作订单是为所选工作订单创建的第一个相关工作订单，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="487e7-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="487e7-150">选择 **新建工作订单** 选项。</span><span class="sxs-lookup"><span data-stu-id="487e7-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="487e7-151">在 **工作订单类型** 字段中，选择一个工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="487e7-152">在 **描述** 中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="487e7-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="487e7-153">根据需要，在 **服务级别** 字段中更改工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="487e7-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="487e7-154">在 **预计开始日期** 和 **预计结束日期** 字段中，选择预计的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="487e7-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="487e7-155">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="487e7-155">Select **OK**.</span></span> <span data-ttu-id="487e7-156">将在 **所有工作订单** 列表页显示新的相关工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="487e7-157">如果您要为其创建此相关工作订单的工作订单已经有相关工作订单，请按照以下步骤将新工作订单作业添加到现有相关工作订单中：</span><span class="sxs-lookup"><span data-stu-id="487e7-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="487e7-158">选择 **添加到相关工作订单** 选项。</span><span class="sxs-lookup"><span data-stu-id="487e7-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="487e7-159">在 **工作订单** 字段中，选择要向其添加新工作订单作业的相关工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="487e7-160">根据需要，在 **服务级别** 字段中更改工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="487e7-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="487e7-161">在 **预计开始日期** 和 **预计结束日期** 字段中，根据需要更改预计的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="487e7-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="487e7-162">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="487e7-162">Select **OK**.</span></span> <span data-ttu-id="487e7-163">将把工作订单作业添加到现有关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="487e7-164">下图显示 **创建相关工作订单** 对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="487e7-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![图 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="487e7-166">如果已经在 **资产管理参数** > **工作订单** 选项卡 > **相关工作订单掩码** 字段中设置了相关工作订单掩码，将根据掩码设置创建工作订单 ID。</span><span class="sxs-lookup"><span data-stu-id="487e7-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="487e7-167">如果未设置相关工作订单掩码，将把下一个可用工作订单 ID 用于相关工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="487e7-168">复制工作订单</span><span class="sxs-lookup"><span data-stu-id="487e7-168">Copy a work order</span></span>

<span data-ttu-id="487e7-169">您可以基于现有工作订单快速创建新的工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="487e7-170">这种工作订单处理方法与基于[维护计划](../preventive-and-reactive-maintenance/maintenance-plans.md)创建工作订单不同。</span><span class="sxs-lookup"><span data-stu-id="487e7-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="487e7-171">这在有一个工作订单中包含大量工作订单作业，这些工作订单作业具有不同资产的应该定期完成的各种作业之类情况下非常有用。</span><span class="sxs-lookup"><span data-stu-id="487e7-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="487e7-172">选择 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="487e7-173">选择要复制其内容的工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="487e7-174">在“操作窗格”> **工作订单** 选项卡 > **新** 组中，选择 **复制工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="487e7-175">将显示所选工作订单的工作订单设置。</span><span class="sxs-lookup"><span data-stu-id="487e7-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="487e7-176">可以根据需要编辑某些字段。</span><span class="sxs-lookup"><span data-stu-id="487e7-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="487e7-177">选择 **确定** 以创建新工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="487e7-178">在 **所有工作订单** 列表页上，您可以根据需要编辑工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="487e7-179">创建新工作订单时，将直接从现有工作订单复制一些信息。</span><span class="sxs-lookup"><span data-stu-id="487e7-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="487e7-180">不会复制有关预测、工具、维护清单、功能位置、地址和计划的信息。</span><span class="sxs-lookup"><span data-stu-id="487e7-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="487e7-181">而是从资产管理中的当前设置进行初始化。</span><span class="sxs-lookup"><span data-stu-id="487e7-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="487e7-182">因此，如果在创建第一个工作订单的时间到您复制工作订单的时间之间更改了该信息，则这些更改将包括在新工作订单中。</span><span class="sxs-lookup"><span data-stu-id="487e7-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="487e7-183">例如，包括对预测的更改和对维护清单的更新。</span><span class="sxs-lookup"><span data-stu-id="487e7-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="487e7-184">下图显示了 **复制工作订单** 对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="487e7-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![图 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="487e7-186">基于维护请求创建工作订单</span><span class="sxs-lookup"><span data-stu-id="487e7-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="487e7-187">选择 **资产管理** > **常用** > **维护请求** > **所有维护请求** 或 **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="487e7-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="487e7-188">选择要为其创建工作订单的维护请求，然后单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="487e7-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="487e7-189">在“操作窗格”> **维护请求** 选项卡 > **新** 组中，选择 **工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="487e7-190">在 **工作订单** 对话框中，设置字段。</span><span class="sxs-lookup"><span data-stu-id="487e7-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="487e7-191">如果已经在维护请求中选择了维护作业类型，根据需要，可在创建工作订单时选择其他维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="487e7-192">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="487e7-192">Select **OK**.</span></span> <span data-ttu-id="487e7-193">消息通知您，已创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="487e7-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="487e7-194">若要查看与维护请求相连的工作订单，请在 **所有维护请求** 或 **有效维护请求** 列表页上选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="487e7-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="487e7-195">然后，在“操作窗格”上，在 **维护请求** 选项卡的 **视图** 组中，选择 **工作订单**。</span><span class="sxs-lookup"><span data-stu-id="487e7-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="487e7-196">下图显示了 **创建工作订单** 对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="487e7-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![图 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="487e7-198">如果您希望自动创建工作订单，可以计划维护计划作业或为资产设置“自动创建”[维护计划](../preventive-and-reactive-maintenance/maintenance-plans.md)或[维护阶段](../preventive-and-reactive-maintenance/maintenance-rounds.md)。</span><span class="sxs-lookup"><span data-stu-id="487e7-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="487e7-199">从 **所有维护安排** 列表页的维护请求创建的工作订单具有在维护请求中选择的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="487e7-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

