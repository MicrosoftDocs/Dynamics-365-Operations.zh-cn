---
title: 将资产管理与固定资产进行集成
description: 本主题说明如何集成资产管理和固定资产模块，以便可以将固定资产与维护资产关联起来。
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809846"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="efd28-103">将资产管理与固定资产进行集成</span><span class="sxs-lookup"><span data-stu-id="efd28-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efd28-104">通过集成 **资产管理** 和 **固定资产** 模块，您可以将固定资产与维护资产关联起来。</span><span class="sxs-lookup"><span data-stu-id="efd28-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="efd28-105">然后，固定资产用户可以从新的或现有固定资产创建维护资产，资产管理用户可以将维护资产与现有的固定资产相关联。</span><span class="sxs-lookup"><span data-stu-id="efd28-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="efd28-106">此功能还使固定资产用户可以轻松查看从工作订单过帐的相关维护资产的成本。</span><span class="sxs-lookup"><span data-stu-id="efd28-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="efd28-107">在本主题中，*维护资产* 指 **资产管理** 模块中的资产，*固定资产* 指 **固定资产** 模块中的资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="efd28-108">为从固定资产创建的新维护资产设置默认位置（可选）</span><span class="sxs-lookup"><span data-stu-id="efd28-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="efd28-109">通过此可选配置，您可以为从固定资产创建的新维护资产设置默认功能位置。</span><span class="sxs-lookup"><span data-stu-id="efd28-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="efd28-110">如果您已经完全完成此配置，通常只需配置这一次即可。</span><span class="sxs-lookup"><span data-stu-id="efd28-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="efd28-111">若要完成此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="efd28-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="efd28-112">转到 **资产管理 \> 设置 \> 资产管理参数**。</span><span class="sxs-lookup"><span data-stu-id="efd28-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="efd28-113">在 **固定资产** 选项卡的 **功能位置** 字段中，选择默认位置。</span><span class="sxs-lookup"><span data-stu-id="efd28-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="efd28-114">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="efd28-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="efd28-115">处理集成的维护资产和固定资产</span><span class="sxs-lookup"><span data-stu-id="efd28-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="efd28-116">本节提供了一系列过程，这些过程显示可以用来处理集成的资产管理和固定资产功能的各种方式。</span><span class="sxs-lookup"><span data-stu-id="efd28-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="efd28-117">将现有维护资产与固定资产相关联</span><span class="sxs-lookup"><span data-stu-id="efd28-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="efd28-118">要将现有维护资产与固定资产相关联，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-119">转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。</span><span class="sxs-lookup"><span data-stu-id="efd28-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="efd28-120">选择一个资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-120">Select an asset.</span></span>
1. <span data-ttu-id="efd28-121">在 **固定资产** 快速选项卡上，在 **固定资产编号** 字段中，选择一个现有的固定资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="efd28-122">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="efd28-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="efd28-123">查看与选定维护资产关联的固定资产</span><span class="sxs-lookup"><span data-stu-id="efd28-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="efd28-124">要查看与选定维护资产关联的固定资产，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-125">转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。</span><span class="sxs-lookup"><span data-stu-id="efd28-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="efd28-126">选择一个资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-126">Select an asset.</span></span>
1. <span data-ttu-id="efd28-127">在 **固定资产** 快速选项卡上，在 **固定资产编号** 字段中，选择链接。</span><span class="sxs-lookup"><span data-stu-id="efd28-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="efd28-128">所选资产的 **固定资产** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="efd28-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="efd28-129">（通常，此页面位于 **固定资产 \> 固定资产 \> 固定资产**。）</span><span class="sxs-lookup"><span data-stu-id="efd28-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="efd28-130">查看与选定固定资产关联的维护资产</span><span class="sxs-lookup"><span data-stu-id="efd28-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="efd28-131">要查看与选定固定资产关联的维护资产，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-132">转到 **固定资产 \> 固定资产 \> 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="efd28-133">选择一个资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-133">Select an asset.</span></span>
1. <span data-ttu-id="efd28-134">在操作窗格上，在 **资产管理** 选项卡的 **视图** 组中，选择 **维护资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="efd28-135">与所选固定资产关联的资产的 **维护资产** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="efd28-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="efd28-136">（通常，此页面位于 **资产管理 \> 资产 \> 所有资产**。）</span><span class="sxs-lookup"><span data-stu-id="efd28-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="efd28-137">查看与固定资产相关联的维护成本</span><span class="sxs-lookup"><span data-stu-id="efd28-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="efd28-138">可以过帐维护资产的资产管理工作订单，每个工作订单通常都有成本。</span><span class="sxs-lookup"><span data-stu-id="efd28-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="efd28-139">当固定资产与维护资产相关联时，您可以直接从固定资产查看相关成本。</span><span class="sxs-lookup"><span data-stu-id="efd28-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="efd28-140">要查看与固定资产关联的维护成本，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-141">转到 **固定资产 \> 固定资产 \> 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="efd28-142">选择一个资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-142">Select an asset.</span></span>
1. <span data-ttu-id="efd28-143">在操作窗格上，在 **资产管理** 选项卡的 **视图** 组中，选择 **维护成本**。</span><span class="sxs-lookup"><span data-stu-id="efd28-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="efd28-144">**维护成本** 页面将打开，显示相关成本。</span><span class="sxs-lookup"><span data-stu-id="efd28-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="efd28-145">为现有固定资产创建新维护资产</span><span class="sxs-lookup"><span data-stu-id="efd28-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="efd28-146">要为现有固定资产创建新维护资产，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-147">转到 **固定资产 \> 固定资产 \> 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="efd28-148">选择一个资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-148">Select an asset.</span></span>
1. <span data-ttu-id="efd28-149">在操作窗格上，在 **资产管理** 选项卡的 **新建** 组中，选择 **创建维护资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="efd28-150">（如果此选项不可用，说明维护资产可能已经与所选固定资产关联。）</span><span class="sxs-lookup"><span data-stu-id="efd28-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="efd28-151">按照[创建资产](../objects/create-an-object.md)中所述完成资产创建。</span><span class="sxs-lookup"><span data-stu-id="efd28-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="efd28-152">创建新固定资产并为其添加新维护资产</span><span class="sxs-lookup"><span data-stu-id="efd28-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="efd28-153">要创建新固定资产并为其添加新维护资产，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="efd28-154">转到 **固定资产 \> 固定资产 \> 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="efd28-155">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="efd28-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="efd28-156">按照[创建固定资产](../../../finance/fixed-assets/tasks/create-fixed-asset.md)中所述完成固定资产的创建。</span><span class="sxs-lookup"><span data-stu-id="efd28-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="efd28-157">在操作窗格上，在 **资产管理** 选项卡的 **新建** 组中，选择 **创建维护资产**。</span><span class="sxs-lookup"><span data-stu-id="efd28-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="efd28-158">按照[创建资产](../objects/create-an-object.md)中所述完成资产创建。</span><span class="sxs-lookup"><span data-stu-id="efd28-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="efd28-159">删除两个资产之间的关联</span><span class="sxs-lookup"><span data-stu-id="efd28-159">Remove the association between two assets</span></span>

<span data-ttu-id="efd28-160">在某些情况下，您可能必须解除维护资产与其固定资产的关联。</span><span class="sxs-lookup"><span data-stu-id="efd28-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="efd28-161">例如，如果您想要从固定资产[创建新维护资产](#new-maintenance-from-fixed)，您必须先删除所有现有关联。</span><span class="sxs-lookup"><span data-stu-id="efd28-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="efd28-162">要删除维护资产和固定资产之间的现有关联，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="efd28-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="efd28-163">转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。</span><span class="sxs-lookup"><span data-stu-id="efd28-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="efd28-164">查找并打开固定资产。</span><span class="sxs-lookup"><span data-stu-id="efd28-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="efd28-165">在 **固定资产** 快速选项卡上，清除 **功能位置** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="efd28-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="efd28-166">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="efd28-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]