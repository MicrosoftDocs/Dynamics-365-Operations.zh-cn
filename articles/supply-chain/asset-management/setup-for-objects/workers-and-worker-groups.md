---
title: 维护工人和工人组
description: 本主题介绍资产管理中的维护工人和工人组。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553dce8df5e91cce58b64e340d8ff72586d8d46d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838554"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="72ccc-103">维护工人和工人组</span><span class="sxs-lookup"><span data-stu-id="72ccc-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="72ccc-104">本主题介绍资产管理中的维护工人和工人组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="72ccc-105">在资产管理中，可将维护工人连接到功能位置。</span><span class="sxs-lookup"><span data-stu-id="72ccc-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="72ccc-106">（有关功能位置的详细信息，请参阅[创建功能位置](../functional-locations/create-functional-locations.md)。）此功能在如下场景中可能非常有用：您对功能位置 01 中的机器安排了维护作业，而您希望分配同一个位置的维护工人执行该作业。</span><span class="sxs-lookup"><span data-stu-id="72ccc-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="72ccc-107">也可以创建维护工人组并为其关联维护工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="72ccc-108">如果要执行简单工作订单安排，并且希望为工作订单安排一组维护工人，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="72ccc-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="72ccc-109">可使用维护工人和维护工人组设置首选维护工人和负责的维护工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="72ccc-110">创建工作人员</span><span class="sxs-lookup"><span data-stu-id="72ccc-110">Create workers</span></span>

1. <span data-ttu-id="72ccc-111">选择 **资产管理** \> **设置** \> **工人** \> **工人**。</span><span class="sxs-lookup"><span data-stu-id="72ccc-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="72ccc-112">选择 **新建** 向列表添加工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="72ccc-113">在 **工人** 字段中，选择工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="72ccc-114">将 **活动** 选项设置为 **是**，以便为工作订单安排工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="72ccc-115">如果已经为工人选择了资源，将自动填写 **常规** 快速选项卡上的 **资源** 和 **说明** 字段。</span><span class="sxs-lookup"><span data-stu-id="72ccc-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="72ccc-116">也将自动填写 **常规** 字段，前提是已将工人设置为资源，并且已在 **资源** 页（**组织管理** \> **资源** \> **资源**）上为该资源分配了日历。</span><span class="sxs-lookup"><span data-stu-id="72ccc-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="72ccc-117">在 **组** 快速选项卡上，选择 **添加**，然后为工人选择维护工人组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="72ccc-118">一个工人可以隶属多个组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="72ccc-119">在标准设置中，工人与组之间的隶属关系从添加组的日期开始生效，从不过期。</span><span class="sxs-lookup"><span data-stu-id="72ccc-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="72ccc-120">此日期在 **生效** 字段中显示。</span><span class="sxs-lookup"><span data-stu-id="72ccc-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="72ccc-121">若要查看 **生效** 字段，请选择 **查看** \> **所有**。</span><span class="sxs-lookup"><span data-stu-id="72ccc-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="72ccc-122">如果工人与组之间的隶属关系应该限制到特定期间，请使用 **生效** 和 **到期** 字段定义该期间。</span><span class="sxs-lookup"><span data-stu-id="72ccc-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="72ccc-123">在 **功能位置** 快速选项卡上，选择 **添加**，然后为维护工人选择功能位置。</span><span class="sxs-lookup"><span data-stu-id="72ccc-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="72ccc-124">并且指定哪个位置是工人的主功能位置。</span><span class="sxs-lookup"><span data-stu-id="72ccc-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72ccc-125">向工人添加功能位置时，将在各菜单项（如 **我的有效资产** 和 **我的有效功能位置**）上显示与这些功能位置有关的所有有效资产。</span><span class="sxs-lookup"><span data-stu-id="72ccc-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="72ccc-126">还在当您新建资产、维护请求或工作订单时显示的资产查找中显示。</span><span class="sxs-lookup"><span data-stu-id="72ccc-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="72ccc-127">**详细信息** 快速选项卡上的字段显示与所选维护工人关联的维护工人组和功能位置的数量。</span><span class="sxs-lookup"><span data-stu-id="72ccc-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="72ccc-128">创建工人组</span><span class="sxs-lookup"><span data-stu-id="72ccc-128">Create worker groups</span></span>

1. <span data-ttu-id="72ccc-129">选择 **资产管理** \> **设置** \> **工人** \> **维护工人组**。</span><span class="sxs-lookup"><span data-stu-id="72ccc-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="72ccc-130">选择 **新建** 向列表添加工人组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="72ccc-131">在 **维护工人组** 字段中，输入组 ID。</span><span class="sxs-lookup"><span data-stu-id="72ccc-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="72ccc-132">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="72ccc-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="72ccc-133">在 **工人** 快速选项卡上，选择 **添加**，然后为工人组选择维护工人。</span><span class="sxs-lookup"><span data-stu-id="72ccc-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="72ccc-134">有关 **生效** 和 **到期** 字段的信息，请参见上一过程中的步骤 6。</span><span class="sxs-lookup"><span data-stu-id="72ccc-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="72ccc-135">如果应将资源组与所选维护工人组关联，请选择 **从资源组复制**。</span><span class="sxs-lookup"><span data-stu-id="72ccc-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="72ccc-136">在 **组** 字段中，选择要从中复制日历设置的资源组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="72ccc-137">然后，在 **工人组** 字段中，选择要将资源组的日历设置复制到的工人组。</span><span class="sxs-lookup"><span data-stu-id="72ccc-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="72ccc-138">仅当希望在执行工作订单计划期间维护工人使用与资源（工作中心）关联的日历，此步骤才相关。</span><span class="sxs-lookup"><span data-stu-id="72ccc-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="72ccc-139">**详细信息** 快速选项卡上的字段显示已经为所选维护工人组设置的维护工人的数量。</span><span class="sxs-lookup"><span data-stu-id="72ccc-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]