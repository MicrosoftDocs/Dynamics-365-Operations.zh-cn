---
title: 移动，替换和安装资产
description: 本主题介绍如何在资产管理中移动，替换和安装资产。
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30145a56de4f7e3dce039968791d2fc9b960077f
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571522"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="25116-103">移动，替换和安装资产</span><span class="sxs-lookup"><span data-stu-id="25116-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="25116-104">本主题介绍如何在资产管理中移动，替换和安装资产。</span><span class="sxs-lookup"><span data-stu-id="25116-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="25116-105">可创建与不与其他资产关联的单个资产，也可以创建包含父资产（顶级资产）和相关子资产的资产结构。</span><span class="sxs-lookup"><span data-stu-id="25116-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="25116-106">在资产管理中，可通过三种方法移动和更改资产的位置。</span><span class="sxs-lookup"><span data-stu-id="25116-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="25116-107">**移动** – 将资产移动到其他资产结构或同一个资产结构中的其他位置。</span><span class="sxs-lookup"><span data-stu-id="25116-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="25116-108">**替换** – 暂时从资产结构删除某个资产，以便修复或补充该资产，以便以后将补充的资产添加回资产结构。</span><span class="sxs-lookup"><span data-stu-id="25116-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="25116-109">也可以将已用资产永久替换为新资产。</span><span class="sxs-lookup"><span data-stu-id="25116-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="25116-110">**安装** – 在功能位置安装父资产和任何关联的子资产。</span><span class="sxs-lookup"><span data-stu-id="25116-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="25116-111">可以将移动，替换或安装的资产与其他功能位置关联。</span><span class="sxs-lookup"><span data-stu-id="25116-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="25116-112">在此情况下，该资产可使用这个功能位置的财务维度。</span><span class="sxs-lookup"><span data-stu-id="25116-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="25116-113">在**功能位置类型**页中，可设置对功能位置的财务维度的处理。</span><span class="sxs-lookup"><span data-stu-id="25116-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="25116-114">移动资产</span><span class="sxs-lookup"><span data-stu-id="25116-114">Move asset</span></span>

<span data-ttu-id="25116-115">可使用**移动资产**功能资产移动到其他资产结构或同一个资产结构中的其他位置。</span><span class="sxs-lookup"><span data-stu-id="25116-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="25116-116">也可以将资产移出资产结构，使其成为无结构关联的独立资产。</span><span class="sxs-lookup"><span data-stu-id="25116-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="25116-117">如果正在修复或暂时替换资产，请勿使用此功能。</span><span class="sxs-lookup"><span data-stu-id="25116-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="25116-118">请改用本主题后文介绍的**替换资产**功能。</span><span class="sxs-lookup"><span data-stu-id="25116-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="25116-119">选择**资产管理** \> **常用** \> **资产** \> **所有资产**或**有效资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="25116-120">在列表中选择要移动的资产。</span><span class="sxs-lookup"><span data-stu-id="25116-120">In the list, select the asset to move.</span></span> <span data-ttu-id="25116-121">如果该资产有子资产，也会移动这些资产。</span><span class="sxs-lookup"><span data-stu-id="25116-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="25116-122">选择**移动资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="25116-123">若要移动资产以使其成为资产结构的一部分，请在**父资产**字段中选择新的父资产。</span><span class="sxs-lookup"><span data-stu-id="25116-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="25116-124">如果要移动子资产，并且希望使其成为不具有结构关联的独立资产，请将**父资产**字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="25116-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="25116-125">默认情况下，**生效**字段设置为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="25116-126">但是，可选择其他日期和时间来充当资产移动的生效日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="25116-127">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="25116-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="25116-128">替换资产</span><span class="sxs-lookup"><span data-stu-id="25116-128">Replace asset</span></span>

<span data-ttu-id="25116-129">**替换资产**功能可以与破损资产的修复、补充或永久性替换为新资产结合使用。</span><span class="sxs-lookup"><span data-stu-id="25116-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="25116-130">此功能用于替换资产结构中的子资产。</span><span class="sxs-lookup"><span data-stu-id="25116-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="25116-131">对于父资产（即当前无父资产的资产），此类替换在功能位置进行。</span><span class="sxs-lookup"><span data-stu-id="25116-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="25116-132">有关如何替换功能位置的父资产的详细信息，请参阅[在功能位置安装资产](../functional-locations/install-objects-on-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="25116-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="25116-133">如果已将维修车间与生产部门关联，则可创建**维修**、**报废**和**存储**之类功能位置来处理资产的维修和替换。</span><span class="sxs-lookup"><span data-stu-id="25116-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="25116-134">选择**资产管理** \> **常用** \> **资产** \> **所有资产**或**有效资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="25116-135">在列表中，选择要替换的子资产。</span><span class="sxs-lookup"><span data-stu-id="25116-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="25116-136">如果该资产有子资产，也会替换这些资产。</span><span class="sxs-lookup"><span data-stu-id="25116-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="25116-137">选择**替换资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="25116-138">**结构更改**字段显示上次在资产结构中移动所选资产和关联的子资产的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="25116-139">在**所选资产**部分的**目标功能位置**字段中，选择要将资产移到的功能位置。</span><span class="sxs-lookup"><span data-stu-id="25116-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="25116-140">例如，选择**维修**或**报废**位置。</span><span class="sxs-lookup"><span data-stu-id="25116-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="25116-141">**父资产**部分中的**生效**字段显示上次在当前功能位置安装或移动父资产和关联的子资产的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="25116-142">在**新资产**部分的**资产**字段中，选择要插入来充当所选资产的临时或永久替代品的资产。</span><span class="sxs-lookup"><span data-stu-id="25116-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="25116-143">此资产现在可能位于其他功能位置，如**存储**。</span><span class="sxs-lookup"><span data-stu-id="25116-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="25116-144">默认情况下，**生效时间**部分中的**生效**字段设置为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="25116-145">但是，可选择其他日期和时间来充当资产替换的生效日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="25116-146">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="25116-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="25116-147">安装资产</span><span class="sxs-lookup"><span data-stu-id="25116-147">Install asset</span></span>

<span data-ttu-id="25116-148">**安装资产**功能用于在功能位置安装资产结构。</span><span class="sxs-lookup"><span data-stu-id="25116-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="25116-149">请始终选择父资产。</span><span class="sxs-lookup"><span data-stu-id="25116-149">Always select a parent asset.</span></span> <span data-ttu-id="25116-150">将把父资产和关联的子资产移动到所选功能位置。</span><span class="sxs-lookup"><span data-stu-id="25116-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="25116-151">选择**资产管理** \> **常用** \> **资产** \> **所有资产**或**有效资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="25116-152">在列表中，选择要安装到其他功能位置的父资产。</span><span class="sxs-lookup"><span data-stu-id="25116-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="25116-153">选择**安装资产**。</span><span class="sxs-lookup"><span data-stu-id="25116-153">Select **Install asset**.</span></span>

    <span data-ttu-id="25116-154">**属性**部分显示为父资产设置的资产属性。</span><span class="sxs-lookup"><span data-stu-id="25116-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="25116-155">在**功能位置**字段中，选择新位置。</span><span class="sxs-lookup"><span data-stu-id="25116-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="25116-156">默认情况下，**生效**字段设置为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="25116-157">但是，可选择资产结构上的安装的其他生效日期和时间。</span><span class="sxs-lookup"><span data-stu-id="25116-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="25116-158">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="25116-158">Select **OK**.</span></span>
