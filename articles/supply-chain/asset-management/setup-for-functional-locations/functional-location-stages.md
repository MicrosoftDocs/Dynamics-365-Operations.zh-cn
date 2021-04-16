---
title: 功能位置生命周期状态
description: 本主题介绍如何在资产管理中设置功能位置状态和生命周期模型。
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1ab19358857440e46d3df2323fbcea19a476903
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837745"
---
# <a name="functional-location-lifecycle-states"></a><span data-ttu-id="6b9a7-103">功能位置生命周期状态</span><span class="sxs-lookup"><span data-stu-id="6b9a7-103">Functional location lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6b9a7-104">本主题介绍如何在资产管理中设置功能位置生命周期状态和生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-104">This topic describes how to set up functional location lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="6b9a7-105">功能位置生命周期状态定义功能位置可以经历的状态，如已创建、有效和已结束。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-105">Functional location lifecycle states define the states that a functional location can go through, for example, created, active, and ended.</span></span> <span data-ttu-id="6b9a7-106">无论功能位置处于哪种生命周期状态，您都可以在 **所有功能位置** 列表页中查看所有功能位置。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-106">You are able to view all functional locations, regardless of their lifecycle state, in the **All functional locations** list page.</span></span> <span data-ttu-id="6b9a7-107">可以更改功能位置的状态，方法是在 **所有功能位置** 列表页中选择功能位置，然后选择 **更新功能位置状态**。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-107">You can change the state of a functional location by selecting it in the **All functional locations** list page and selecting **Update functional location state**.</span></span>

## <a name="set-up-functional-location-lifecycle-states"></a><span data-ttu-id="6b9a7-108">设置功能位置生命周期状态</span><span class="sxs-lookup"><span data-stu-id="6b9a7-108">Set up functional location lifecycle states</span></span>

1. <span data-ttu-id="6b9a7-109">选择 **资产管理** > **设置** > **功能位置** > **生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-109">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle states**.</span></span>
2. <span data-ttu-id="6b9a7-110">选择 **新建** 创建新的功能位置状态。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-110">Select **New** to create a new functional location state.</span></span>
3. <span data-ttu-id="6b9a7-111">在 **生命周期状态** 字段中插入状态 ID，在 **名称** 字段中插入功能位置状态的名称。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-111">Insert the state ID in the **Lifecycle state** field and a name for the functional location state in the **Name** field.</span></span> <span data-ttu-id="6b9a7-112">在 **生命周期模型** 字段中，可查看使用该功能位置状态的功能位置生命周期模型的数量。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-112">In the **Lifecycle models** field, you can see the number of functional location lifecycle models that uses the functional location state.</span></span>
4. <span data-ttu-id="6b9a7-113">如果在此状态时功能位置应有效，请在 **常规** 快速选项卡的 **有效** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-113">On the **General** FastTab, select "Yes" on the **Active** toggle button if the functional location should be active at this state.</span></span>
5. <span data-ttu-id="6b9a7-114">如果应该可以在此状态时自动创建与功能位置同名的资产并安装到这个功能位置，请在 **创建资产** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-114">Select "Yes" on the **Create assets** toggle button if it should be possible to automatically create an asset with the same name as the functional location and install it on the functional location at this state.</span></span>  
>[!NOTE]
><span data-ttu-id="6b9a7-115">此切换按钮与 **功能位置类型** 窗体（**资产管理** > **设置** > **功能位置** > **功能位置类型**）中 **常规** 快速选项卡上的 **资产类型** 字段关联。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-115">This toggle button relates to the **Asset type** field on the **General** FastTab in the **Functional location types** form (**Asset management** > **Setup** > **Functional locations** > **Functional location types**).</span></span>
6. <span data-ttu-id="6b9a7-116">如果应该可以在此状态更改功能位置的名称，请在 **重命名位置** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-116">Select "Yes" on the **Rename location** toggle button if it should be possible to change the name of the functional location at this state.</span></span>
7. <span data-ttu-id="6b9a7-117">如果应该可以在此状态向功能位置添加新的子位置，请在 **新建子位置** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-117">Select "Yes" on the **New sub locations** toggle button if it should be possible to add new sub locations to the functional location at this state.</span></span>
8. <span data-ttu-id="6b9a7-118">如果应该可以在此状态在功能位置安装资产，请在 **安装资产** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-118">Select "Yes" on the **Install assets** toggle button if it should be possible to install assets on the functional location at this state.</span></span>
9. <span data-ttu-id="6b9a7-119">如果应该可以在此状态删除功能位置，请在 **删除功能位置** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-119">Select "Yes" on the **Delete functional location** toggle button if it should be possible to delete the functional location at this state.</span></span>
10. <span data-ttu-id="6b9a7-120">如果希望在此状态自动更新在功能位置安装的所有支持的资产生命周期状态，请在 **生命周期状态** 字段中选择资产状态。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-120">Select an asset state in the **Lifecycle state** field if you want the asset lifecycle state for all assets installed on the functional location to be automatically updated at this state.</span></span> <span data-ttu-id="6b9a7-121">示例：如果关闭一个功能位置，然后将该功能位置的生命周期状态设置为“已结束”，您可能希望将在该功能位置安装的资产的生命周期状态更改为“未在使用中”。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-121">Example: If you close down a functional location, and set the functional location lifecycle state to "Ended", you may want to automatically change the lifecycle state of the assets installed on that functional location to "Not in use".</span></span>


>[!NOTE]
><span data-ttu-id="6b9a7-122">功能位置生命周期状态、生命周期模型和类型与工作订单生命周期状态、工作订单生命周期模型和工作订单类型的关联方法和使用方法相同。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-122">Functional location lifecycle states, lifecycle models, and types are related and used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 

## <a name="set-up-functional-location-lifecycle-models"></a><span data-ttu-id="6b9a7-123">设置功能位置生命周期模型</span><span class="sxs-lookup"><span data-stu-id="6b9a7-123">Set up functional location lifecycle models</span></span>

<span data-ttu-id="6b9a7-124">创建功能位置所需生命周期状态之后，可将这些状态拆分为组。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-124">When you have created the lifecycle states required for your functional locations, they can be divided into groups.</span></span> <span data-ttu-id="6b9a7-125">目的是创建可用于不同类型功能位置的生命周期模型流。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-125">This is done to create the lifecycle model flow that may be used for different types of functional locations.</span></span> <span data-ttu-id="6b9a7-126">至少应创建一个标准功能位置生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-126">As a minimum, one standard functional location lifecycle model should be created.</span></span>

1. <span data-ttu-id="6b9a7-127">选择 **资产管理** > **设置** > **功能位置** > **生命周期模型**。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-127">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle models**.</span></span>
2. <span data-ttu-id="6b9a7-128">选择 **新建** 以创建新的生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-128">Select **New** to create a new lifecycle model.</span></span>
3. <span data-ttu-id="6b9a7-129">在 **生命周期模型** 字段中插入生命周期模型 ID，在 **名称** 字段中插入生命周期模型的名称。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-129">Insert the lifecycle model ID in the **Lifecycle model** field and a name for the lifecycle model in the **Name** field.</span></span> <span data-ttu-id="6b9a7-130">在 **功能位置类型** 和 **生命周期状态** 字段中，可查看使用该生命周期模型的功能位置类型数量和生命周期模型中选择的状态数量。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-130">In the **Functional location types** and **Lifecycle states** fields, you can see the number of functional location types that uses the lifecycle model and the number of states selected in the lifecycle model.</span></span>
4. <span data-ttu-id="6b9a7-131">在 **生命周期状态** 快速选项卡上，选择模型中应包含的状态。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-131">On the **Lifecycle states** FastTab, select the states that should be included in the model.</span></span> <span data-ttu-id="6b9a7-132">方法是单击 **其余生命周期状态** 部分中的状态，然后单击 ![前进箭头](media/02-setup-for-functional-locations.png) 按钮。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-132">This is done by clicking on a state in the **Lifecycle states remaining** section and clicking the ![forward arrow](media/02-setup-for-functional-locations.png) button.</span></span>
5. <span data-ttu-id="6b9a7-133">如果要为模型选择所有可用状态，请单击![选择所有可用阶段](media/03-setup-for-functional-locations.png)按钮。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-133">If you want to select all the available states for a model, click the ![select all available stages](media/03-setup-for-functional-locations.png) button.</span></span> <span data-ttu-id="6b9a7-134">将把所有状态移到 **所选生命周期状态** 部分。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-134">All states are transferred to the **Lifecycle states selected** section.</span></span>
6. <span data-ttu-id="6b9a7-135">如果要从模型删除所选状态，请在 **所选生命周期状态** 部分中选择状态，然后单击 ![后退箭头](media/04-setup-for-functional-locations.png) 按钮。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-135">If you want to remove a selected state from the model, select the state in the **Lifecycle states selected** section and then select the ![back arrow](media/04-setup-for-functional-locations.png) button.</span></span>
7. <span data-ttu-id="6b9a7-136">要定义哪些生命周期状态可采用所选状态，选择 **生命周期状态更新**。</span><span class="sxs-lookup"><span data-stu-id="6b9a7-136">Select **Lifecycle state updates** to define which lifecycle states can follow a selected state.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]