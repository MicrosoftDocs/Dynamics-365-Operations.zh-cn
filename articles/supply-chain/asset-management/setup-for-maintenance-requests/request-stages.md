---
title: 维护请求生命周期状态
description: 本主题介绍如何在资产管理中设置维护请求生命周期状态。
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9022d866bf0da08a72ba9169587f87c1b77527a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217213"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="b99f6-103">维护请求生命周期状态</span><span class="sxs-lookup"><span data-stu-id="b99f6-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="b99f6-104">维护请求生命周期状态定义请求可以经历的阶段。</span><span class="sxs-lookup"><span data-stu-id="b99f6-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="b99f6-105">示例包括 **已创建**、**活动** 和 **已结束**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="b99f6-106">将维护请求转化为工作订单时，硬件维护请求生命周期状态更新为 **已结束** 或 **已关闭**，以指示维护请求不再处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="b99f6-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="b99f6-107">在 **所有维护请求** 列表页上，可以查看所有维护请求，不受其生命周期状态影响。</span><span class="sxs-lookup"><span data-stu-id="b99f6-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="b99f6-108">设置维护请求生命周期状态</span><span class="sxs-lookup"><span data-stu-id="b99f6-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="b99f6-109">选择 **资产管理** \> **设置** \> **维护请求** \> **生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="b99f6-110">选择 **新建** 创建维护请求生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b99f6-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="b99f6-111">在 **生命周期状态** 字段中，输入生命周期状态的 ID。</span><span class="sxs-lookup"><span data-stu-id="b99f6-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="b99f6-112">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="b99f6-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="b99f6-113">**详细信息** 快速选项卡上的 **生命周期模型** 字段显示使用此生命周期状态的维护请求生命周期模型的数量。</span><span class="sxs-lookup"><span data-stu-id="b99f6-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="b99f6-114">如果维护请求在此生命周期状态期间应该处于活动状态，请在 **常规** 快速选项卡上将 **活动** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="b99f6-115">如果应该为处于此生命周期状态的维护请求自动输入实际结束日期和时间，请将 **设置实际结束时间** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="b99f6-116">如果可以从处于此生命周期状态的维护请求创建工作订单，请将 **创建工作订单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="b99f6-117">如果可以删除处于此生命周期状态的维护请求，请将 **删除** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="b99f6-118">如果您使用仓库维修，则在 **更新** 快速选项卡上，**资产** 部分中的 **收货** 和 **出货** 选项是相关的。</span><span class="sxs-lookup"><span data-stu-id="b99f6-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="b99f6-119">如果当维护请求的维护请求生命周期状态设置为 **收货** 或 **出货** 时，该维护请求中选择的资产的资产生命周期状态应自动更新为 **收货** 或 **出货**，则将适当的选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="b99f6-120">下图显示 **维护请求生命周期状态** 页的示例。</span><span class="sxs-lookup"><span data-stu-id="b99f6-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![维护请求生命周期状态页面](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="b99f6-122">维护请求生命周期状态、生命周期状态组和类型与工作订单生命周期状态、生命周期状态组和类型关联，并按照相同方法使用。</span><span class="sxs-lookup"><span data-stu-id="b99f6-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="b99f6-123">设置维护请求生命周期模型</span><span class="sxs-lookup"><span data-stu-id="b99f6-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="b99f6-124">创建了维护请求所需生命周期状态之后，可以将其拆分为生命周期状态组或生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="b99f6-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="b99f6-125">维护请求生命周期模型用于创建可用于不同类型的维护请求的流。</span><span class="sxs-lookup"><span data-stu-id="b99f6-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="b99f6-126">至少应创建一个标准维护请求生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="b99f6-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="b99f6-127">选择 **资产管理** \> **设置** \> **维护请求** \> **生命周期模型**。</span><span class="sxs-lookup"><span data-stu-id="b99f6-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="b99f6-128">选择 **新建** 创建维护请求生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="b99f6-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="b99f6-129">在 **生命周期模型** 字段中，输入生命周期模型的 ID。</span><span class="sxs-lookup"><span data-stu-id="b99f6-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="b99f6-130">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="b99f6-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="b99f6-131">**详细信息** 快速选项卡上的 **生命周期状态** 字段显示此生命周期模型中选择的生命周期状态的数量。</span><span class="sxs-lookup"><span data-stu-id="b99f6-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="b99f6-132">**维护请求类型** 字段显示使用此生命周期模型的维护请求类型的数量。</span><span class="sxs-lookup"><span data-stu-id="b99f6-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="b99f6-133">在 **生命周期状态** 快速选项卡上，选择生命周期模型中应包含的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b99f6-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="b99f6-134">若要在生命周期模型中包含生命周期状态，请在 **其余生命周期状态** 部分中选择该生命周期状态，然后选择向右箭头按钮 ![向右箭头](media/03-setup-for-requests.png) 将其移到 **所选生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="b99f6-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="b99f6-135">若要在生命周期模型中包含所有可用生命周期状态，请选择 **选择所有可用状态** 按钮 ![选择所有可用状态](media/04-setup-for-requests.png)。</span><span class="sxs-lookup"><span data-stu-id="b99f6-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="b99f6-136">将把所有生命周期状态移到 **所选生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="b99f6-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="b99f6-137">若要从生命周期模型中删除生命周期状态，请在 **所选生命周期状态** 部分中选择该生命周期状态，然后选择向左箭头按钮 ![向左箭头](media/05-setup-for-requests.png) 将其移到 **其余生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="b99f6-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="b99f6-138">如果使用仓库维修，则 **常规** 快速选项卡上 **更新** 部分中的字段相关。</span><span class="sxs-lookup"><span data-stu-id="b99f6-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="b99f6-139">在 **接收的资产的生命周期** 字段中，选择在收到维护请求中选择要进行仓库维修的资产时，应将该资产自动更新为的资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b99f6-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="b99f6-140">在 **交付的资产的生命周期** 字段中，选择在维护请求中选择的资产在维修后退回时，应将该资产自动更新为的资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b99f6-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="b99f6-141">下图显示 **维护请求生命周期模型** 页的示例。</span><span class="sxs-lookup"><span data-stu-id="b99f6-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![维护请求生命周期模型页面](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]