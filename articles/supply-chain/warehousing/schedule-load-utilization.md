---
title: 计划负载利用率
description: 本主题介绍如何设置和计划仓库的负载。
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac4dcba153b8da3d62261326c3c4e169325c2210
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977380"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="7ba27-103">计划负载利用率</span><span class="sxs-lookup"><span data-stu-id="7ba27-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7ba27-104">您可以为所选位置类型计划负载利用率，也可以预测当前和未来的负载利用率。</span><span class="sxs-lookup"><span data-stu-id="7ba27-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="7ba27-105">您可以预测一个或多个站点、负载单位（区域或仓库）或区域和仓库的组合的负载。</span><span class="sxs-lookup"><span data-stu-id="7ba27-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="7ba27-106">安排和查看仓库或站点的负荷</span><span class="sxs-lookup"><span data-stu-id="7ba27-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="7ba27-107">若要为站点、仓库或区域安排负载，您可以创建空间利用率并将其与主计划关联。</span><span class="sxs-lookup"><span data-stu-id="7ba27-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="7ba27-108">在设置空间利用率时，可使用库位类型（如 **堆放库位** 和 **领料库位**）指定应如何预测空间利用率。</span><span class="sxs-lookup"><span data-stu-id="7ba27-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="7ba27-109">您还可以指定存储负载模式，例如 **区域**。</span><span class="sxs-lookup"><span data-stu-id="7ba27-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="7ba27-110">将来空间利用率的计划是基于在相关主计划上计算的信息的。</span><span class="sxs-lookup"><span data-stu-id="7ba27-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="7ba27-111">主计划预测为生产和工序传入和传出订单的资源计划。</span><span class="sxs-lookup"><span data-stu-id="7ba27-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="7ba27-112">可用空间的计划是基于空间利用率设置和所选主计划之间的关系的。</span><span class="sxs-lookup"><span data-stu-id="7ba27-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="7ba27-113">通过使用您在空间利用率设置中选择的存储负载模式，可以指定是否应为各个仓库或区域预测负载，或者预测是否应包括有关仓库和区域的信息。</span><span class="sxs-lookup"><span data-stu-id="7ba27-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="7ba27-114">您还可以指定是否应将锁定库位排除在负载利用率的计算范围之外。</span><span class="sxs-lookup"><span data-stu-id="7ba27-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="7ba27-115">您可以通过生成 **仓库负载利用率** 报表预测空间利用率。</span><span class="sxs-lookup"><span data-stu-id="7ba27-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="7ba27-116">生成此报表时，可以指定是否应为各个站点或跨站点或所选的负载单位预测负载利用率，例如区域或仓库。</span><span class="sxs-lookup"><span data-stu-id="7ba27-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="7ba27-117">为仓库创建空间利用率设置</span><span class="sxs-lookup"><span data-stu-id="7ba27-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="7ba27-118">选择 **库存管理** \> **设置** \> **仓库监视** \> **空间利用率**。</span><span class="sxs-lookup"><span data-stu-id="7ba27-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="7ba27-119">选择 **新建** 创建空间利用率设置。</span><span class="sxs-lookup"><span data-stu-id="7ba27-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="7ba27-120">为新设置指定 ID 和名称。</span><span class="sxs-lookup"><span data-stu-id="7ba27-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="7ba27-121">在 **存储负载模式** 字段中，选择空间利用率概览是否应按仓库、区域或仓库和区域显示信息。</span><span class="sxs-lookup"><span data-stu-id="7ba27-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="7ba27-122">将 **排除锁定的库位** 选项设置为 **是** 将在计算可用空间时排除锁定的库存库位。</span><span class="sxs-lookup"><span data-stu-id="7ba27-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="7ba27-123">可通过在 **库存库位** 页面 **其他** 快速选项卡上的 **输入已锁定** 或 **输出已锁定** 字段中指定库位的锁定原因来锁定输入和输出的库存库位。</span><span class="sxs-lookup"><span data-stu-id="7ba27-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="7ba27-124">在 **库位类型** 快速选项卡上，选择要包括在空间利用率计算中的库位类型。</span><span class="sxs-lookup"><span data-stu-id="7ba27-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="7ba27-125">您必须为计划至少选择一个库位类型。</span><span class="sxs-lookup"><span data-stu-id="7ba27-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="7ba27-126">将空间利用率设置与主计划关联</span><span class="sxs-lookup"><span data-stu-id="7ba27-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="7ba27-127">选择 **库存管理** \> **定期任务** \> **计划负载利用率**。</span><span class="sxs-lookup"><span data-stu-id="7ba27-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="7ba27-128">在 **主计划** 字段中，选择一个主计划。</span><span class="sxs-lookup"><span data-stu-id="7ba27-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="7ba27-129">在 **天数** 字段中，指定要包括在当前和未来工作量预测中的天数。</span><span class="sxs-lookup"><span data-stu-id="7ba27-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="7ba27-130">在 **空间利用率** 字段中，选择要用于当前和未来工作量的预测的空间利用率设置。</span><span class="sxs-lookup"><span data-stu-id="7ba27-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="7ba27-131">指定负载利用率计划并查看信息</span><span class="sxs-lookup"><span data-stu-id="7ba27-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="7ba27-132">选择 **库存管理** \> **查询和报表** \> **实际库存报表** \> **仓库负载利用率**。</span><span class="sxs-lookup"><span data-stu-id="7ba27-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="7ba27-133">在 **显示依据** 字段中，选择 空间利用率预测的级别：</span><span class="sxs-lookup"><span data-stu-id="7ba27-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="7ba27-134">**站点** – 预测各站点的空间利用率。</span><span class="sxs-lookup"><span data-stu-id="7ba27-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="7ba27-135">例如，如果您要查看站点的所有仓库，以便您可以在仓库之间平衡空间利用率，那么此信息很有用。</span><span class="sxs-lookup"><span data-stu-id="7ba27-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="7ba27-136">**负载单位** – 预测区域或仓库的空间利用率。</span><span class="sxs-lookup"><span data-stu-id="7ba27-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="7ba27-137">然后根据您创建空间利用率设置时在 **空间利用率** 页面 **存储负载模式** 字段中选择的值预测可用空间。</span><span class="sxs-lookup"><span data-stu-id="7ba27-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="7ba27-138">执行以下步骤之一，具体取决于您在上一步中选择的值：</span><span class="sxs-lookup"><span data-stu-id="7ba27-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="7ba27-139">如果在 **显示依据** 字段中选择的是 **站点**，则 **站点** 字段可用。</span><span class="sxs-lookup"><span data-stu-id="7ba27-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="7ba27-140">选择一个或多个要包括在预测中的站点。</span><span class="sxs-lookup"><span data-stu-id="7ba27-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="7ba27-141">如果在 **显示依据** 字段中选择的是 **负载单位**，则 **负载单位** 字段可用。</span><span class="sxs-lookup"><span data-stu-id="7ba27-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="7ba27-142">选择负载单位。</span><span class="sxs-lookup"><span data-stu-id="7ba27-142">Select the load unit.</span></span>

4. <span data-ttu-id="7ba27-143">在 **负载类型** 字段中，选择 **体积** 或 **重量** 以指定要预测的空间所属的仓库运营单位。</span><span class="sxs-lookup"><span data-stu-id="7ba27-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="7ba27-144">在 **空间利用率设置** 字段中，选择应充当预测基础的空间利用率设置。</span><span class="sxs-lookup"><span data-stu-id="7ba27-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
