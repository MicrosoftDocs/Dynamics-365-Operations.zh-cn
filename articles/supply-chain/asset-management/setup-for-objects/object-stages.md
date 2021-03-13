---
title: 资产生命周期状态
description: 本主题介绍资产管理中的资产生命周期状态和生命周期模型。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dffedfafd9d75320accf0e27f072bab6fd51f135
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016544"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="26819-103">资产生命周期状态</span><span class="sxs-lookup"><span data-stu-id="26819-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="26819-104">本主题介绍资产管理中的资产生命周期状态和生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="26819-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="26819-105">资产生命周期状态用于定义资产有效还是无效。</span><span class="sxs-lookup"><span data-stu-id="26819-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="26819-106">例如，可将资产生命周期状态设置为 **已创建**、**有效** 和 **已终止**。</span><span class="sxs-lookup"><span data-stu-id="26819-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="26819-107">请求生命周期状态与资产生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="26819-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="26819-108">因此，如果将请求更改为新的请求生命周期状态，与该请求关联的资产将更改为新的资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="26819-109">例如，如果将一个请求的生命周期状态更改为 **入站**，则关联资产的生命周期状态将更改为 **资产生命周期状态模型** 页 **资产生命周期状态** 快速选项卡上 **入站生命周期状态** 字段中选择的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="26819-110">可在资产生命周期模型（其中定义各种资产类型需要的生命周期状态）中设置资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="26819-111">设置第一个生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-111">You first set up lifecycle states.</span></span> <span data-ttu-id="26819-112">然后创建一个生命周期模型，并为该生命周期模型选择这个生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="26819-113">选择 **资产管理** \> **设置** \> **资产** \> **生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="26819-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="26819-114">选择 **新建** 以创建新资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="26819-115">在 **生命周期状态** 字段中，输入生命周期状态 ID。</span><span class="sxs-lookup"><span data-stu-id="26819-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="26819-116">在 **名称** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="26819-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="26819-117">**生命周期模型** 字段显示使用此资产生命周期状态的资产生命周期模型的数量。</span><span class="sxs-lookup"><span data-stu-id="26819-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="26819-118">如果此生命周期状态应该为无效生命周期状态（换句话说，可以为此生命周期状态的资产创建工作订单），请将 **有效** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="26819-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="26819-119">如果应该在处于此生命周期状态时删除资产生命周期状态为 **已创建** 的未结束资产日历行，请将 **删除未结束日历行** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="26819-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="26819-120">如果要清除资产的所有不再相关的未结束维护计划（例如，如果资产不再有效），此设置非常有用。</span><span class="sxs-lookup"><span data-stu-id="26819-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="26819-121">资产生命周期状态、资产生命周期模型和资产类型相互关联。</span><span class="sxs-lookup"><span data-stu-id="26819-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="26819-122">其使用方法与工作订单生命周期状态、工作订单生命周期模型和工作订单类型的使用方法相同。</span><span class="sxs-lookup"><span data-stu-id="26819-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="26819-123">创建所需资产生命周期状态之后，可以在资产生命周期模型中设置生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="26819-124">选择 **资产管理** \> **设置** \> **资产** \> **生命周期模型**。</span><span class="sxs-lookup"><span data-stu-id="26819-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="26819-125">选择 **新建** 以创建新资产生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="26819-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="26819-126">在 **生命周期模型** 字段中，输入生命周期模型 ID。</span><span class="sxs-lookup"><span data-stu-id="26819-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="26819-127">在 **名称** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="26819-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="26819-128">**生命周期状态** 字段显示生命周期模型中选择的资产生命周期状态的数量。</span><span class="sxs-lookup"><span data-stu-id="26819-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="26819-129">**资产类型** 字段显示使用此生命周期模型的资产类型的数量。</span><span class="sxs-lookup"><span data-stu-id="26819-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="26819-130">在 **生命周期状态** 快速选项卡上，选择资产生命周期模型中应包含的资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="26819-131">若要为模型使用某个生命周期状态，请在 **其余生命周期状态** 部分中选择该生命周期状态，然后选择向右箭头按钮 ![向右箭头](media/15-setup-for-objects.png) 将其移到 **所选生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="26819-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="26819-132">若要为模型使用所有可用生命周期状态，请选择 **所有可用生命周期状态** 按钮 ![所有可用生命周期状态](media/20-setup-for-objects.png)。</span><span class="sxs-lookup"><span data-stu-id="26819-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="26819-133">将把所有生命周期状态移到 **所选生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="26819-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="26819-134">若要从模型中删除生命周期状态，请在 **生命周期状态模型** 部分中选择该生命周期状态，然后选择向左箭头按钮 ![向左箭头](media/16-setup-for-objects.png) 将其移到 **其余生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="26819-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="26819-135">要定义可采用所选生命周期状态的资产生命周期状态，选择 **生命周期状态更新**。</span><span class="sxs-lookup"><span data-stu-id="26819-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="26819-136">如果要处理收到待维修的资产，请使用 **资产状态** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="26819-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="26819-137">在 **入站/出站** 部分中，可选择资产生命周期状态以指示收到待维修的资产的工作流。</span><span class="sxs-lookup"><span data-stu-id="26819-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="26819-138">如果为客户或部门提供出借资产，可在 **借出** 部分中为出借资产选择生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="26819-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
