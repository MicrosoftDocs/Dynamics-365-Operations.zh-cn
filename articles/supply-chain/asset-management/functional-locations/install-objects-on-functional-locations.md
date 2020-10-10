---
title: 在功能位置安装资产
description: 本主题介绍如何在资产管理中在功能位置安装资产。
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85b9f473cc725896a00501510eea02d7cfb21782
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888863"
---
# <a name="install-assets-on-functional-locations"></a><span data-ttu-id="eb666-103">在功能位置安装资产</span><span class="sxs-lookup"><span data-stu-id="eb666-103">Install assets on functional locations</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="eb666-104">创建功能位置结构之后，下一步是在相关功能位置安装资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-104">After you've created functional location structures, the next step is to install assets on the relevant functional locations.</span></span> <span data-ttu-id="eb666-105">本主题介绍如何在资产管理中在这些功能位置安装资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-105">This topic explains how to install assets on those functional locations in Asset Management.</span></span> <span data-ttu-id="eb666-106">有关如何创建资产的详细信息，请参阅[资产简介](../objects/introduction-to-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="eb666-106">For information about how to create assets, see [Introduction to assets](../objects/introduction-to-objects.md).</span></span>

<span data-ttu-id="eb666-107">如果已创建了资产结构，则必须将整个资产结构安装到功能位置。</span><span class="sxs-lookup"><span data-stu-id="eb666-107">If you've created an asset structure, the whole asset structure must be installed on a functional location.</span></span> <span data-ttu-id="eb666-108">因此，只能在功能位置选择父资产（即无父资产的顶级资产）。</span><span class="sxs-lookup"><span data-stu-id="eb666-108">Therefore, only parent assets (top-level assets that have no parent asset) can be selected on a functional location.</span></span> <span data-ttu-id="eb666-109">还会将所有相关子资产安装到功能位置。</span><span class="sxs-lookup"><span data-stu-id="eb666-109">All related child assets (sub-assets) will also be installed on the functional location.</span></span> <span data-ttu-id="eb666-110">在功能位置安装资产时，可能会将功能位置的财务维度自动传输到这些资产，具体取决于为功能位置选择的功能位置类型的设置。</span><span class="sxs-lookup"><span data-stu-id="eb666-110">When you install assets on a functional location, the financial dimensions of the functional location might be automatically transferred to them, depending on the setup on the functional location type that is selected for the functional location.</span></span> <span data-ttu-id="eb666-111">有关如何设置功能位置类型的详细信息，请参阅[功能位置类型](../setup-for-functional-locations/functional-location-types.md)。</span><span class="sxs-lookup"><span data-stu-id="eb666-111">For more information about how to set up functional location types, see [Functional location types](../setup-for-functional-locations/functional-location-types.md).</span></span>

> [!NOTE]
> <span data-ttu-id="eb666-112">可以为用于功能位置的功能位置类型设置资产类型。</span><span class="sxs-lookup"><span data-stu-id="eb666-112">You can set up asset types on the functional location type that is used for a functional location.</span></span> <span data-ttu-id="eb666-113">在此情况下，在功能位置安装资产时，该功能位置可安装的资产的列表中将仅显示具有相同资产类型的父资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-113">In this case, when you install assets on the functional location, only parent assets that have the same asset type are shown in the list of assets that can be installed on the functional location.</span></span>

<span data-ttu-id="eb666-114">在功能位置安装资产之后，可以根据需要替换父资产或资产结构。</span><span class="sxs-lookup"><span data-stu-id="eb666-114">After you've installed assets on a functional location, you can replace a parent asset or an asset structure as you require.</span></span> <span data-ttu-id="eb666-115">就像在安装资产时一样，只能选择替换父资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-115">As when you install assets, you select a parent asset to replace.</span></span> <span data-ttu-id="eb666-116">也将替换所有相关子资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-116">All related child assets will also be replaced.</span></span> 


## <a name="install-an-asset-structure-on-a-functional-location"></a><span data-ttu-id="eb666-117">在功能位置安装资产结构</span><span class="sxs-lookup"><span data-stu-id="eb666-117">Install an asset structure on a functional location</span></span>

1. <span data-ttu-id="eb666-118">选择**资产管理** \> **常用** \> **功能位置** \> **所有功能位置**或**有效功能位置**。</span><span class="sxs-lookup"><span data-stu-id="eb666-118">Select **Asset management** \> **Common** \> **Functional locations** \> **All Functional locations** or **Active functional locations**.</span></span>
2. <span data-ttu-id="eb666-119">选择要安装资产的功能位置。</span><span class="sxs-lookup"><span data-stu-id="eb666-119">Select the functional location to install an asset on.</span></span>
3. <span data-ttu-id="eb666-120">选择**安装资产**。</span><span class="sxs-lookup"><span data-stu-id="eb666-120">Select **Install asset**.</span></span>

    <span data-ttu-id="eb666-121">**属性**部分显示对为功能位置选择的功能位置类型设置的资产属性要求的列表。</span><span class="sxs-lookup"><span data-stu-id="eb666-121">The **Attributes** section shows a list of the asset attribute requirements that are set up on the functional location type that is selected for the functional location.</span></span> <span data-ttu-id="eb666-122">这些属性仅供参考。</span><span class="sxs-lookup"><span data-stu-id="eb666-122">The attributes are for informational purposes only.</span></span> <span data-ttu-id="eb666-123">系统不会针对为要安装的资产设置的资产属性验证属性。</span><span class="sxs-lookup"><span data-stu-id="eb666-123">The system doesn't validate the attributes against the asset attributes that are set up on the asset that you're installing.</span></span> <span data-ttu-id="eb666-124">在**资产**字段中选择资产之后，必须执行此项验证。</span><span class="sxs-lookup"><span data-stu-id="eb666-124">You must do that validation after you select an asset in the **Asset** field.</span></span>

4. <span data-ttu-id="eb666-125">在**资产**字段中，选择要安装的父资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-125">In the **Asset** field, select the parent asset to install.</span></span> <span data-ttu-id="eb666-126">安装中将自动包含所有相关子资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-126">All related child assets are automatically included in the installation.</span></span>

    <span data-ttu-id="eb666-127">资产列表右侧的**资产属性**部分显示与所选资产有关的资产属性。</span><span class="sxs-lookup"><span data-stu-id="eb666-127">The **Asset attributes** section to the right of the asset list shows the asset attributes that are related to the selected asset.</span></span>

5. <span data-ttu-id="eb666-128">在**生效**字段中，选择资产安装的生效日期和时间。</span><span class="sxs-lookup"><span data-stu-id="eb666-128">In the **Effective** field, select the date and time that the asset installation is valid from.</span></span> <span data-ttu-id="eb666-129">该日期和时间之后，将把资产和相关子资产的成本与功能位置关联。</span><span class="sxs-lookup"><span data-stu-id="eb666-129">After that date and time, costs for the asset and related sub-assets will be related to the functional location.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eb666-130">将把为资产设置的资产属性添加到**属性**部分。</span><span class="sxs-lookup"><span data-stu-id="eb666-130">The asset attributes that are set up on the asset are added to the **Attributes** section.</span></span> <span data-ttu-id="eb666-131">例如，**重量**属性要求已同时添加为资产和功能位置的要求。</span><span class="sxs-lookup"><span data-stu-id="eb666-131">For example, the **Weight** attribute requirement has been added as a requirement on both the asset and the functional location.</span></span> <span data-ttu-id="eb666-132">如果资产与功能位置具有相同类型的属性要求，则将在**值**字段中输入资产的属性要求值。</span><span class="sxs-lookup"><span data-stu-id="eb666-132">If the asset has attribute requirements of the same type as the functional location, the values of the asset's attribute requirements are entered in the **Value** fields.</span></span> <span data-ttu-id="eb666-133">因此，可针对为功能位置设置的属性要求验证资产值。</span><span class="sxs-lookup"><span data-stu-id="eb666-133">Therefore, you can validate the asset values against the attribute requirements that are set up on the functional location.</span></span> <span data-ttu-id="eb666-134">将使用选中标记来标记为功能位置设置的属性要求。</span><span class="sxs-lookup"><span data-stu-id="eb666-134">The attribute requirements that are set up on the functional location are marked with a check mark.</span></span>

6. <span data-ttu-id="eb666-135">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="eb666-135">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eb666-136">若要通过将资产安装到新功能位置来更改该资产的安装，请执行此过程的步骤 1 到 6。</span><span class="sxs-lookup"><span data-stu-id="eb666-136">To change the installation of an asset by installing it on a new functional location, follow steps 1 through 6 of this procedure.</span></span> <span data-ttu-id="eb666-137">如果资产安装到新功能位置，将从上一个功能位置自动卸载该资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-137">When you install an asset on a new functional location, the asset is automatically uninstalled from the previous functional location.</span></span> <span data-ttu-id="eb666-138">**不会**将资产安装到新功能位置之前为该资产创建的所有有效维护请求或工作订单自动传输到新功能位置。</span><span class="sxs-lookup"><span data-stu-id="eb666-138">Any active maintenance requests or work orders that were created on the asset before you installed it on a new functional location are **not** automatically transferred to the new functional location.</span></span> <span data-ttu-id="eb666-139">如果资产仍然需要这些维护请求和工作订单，必须在将资产安装到新位置之后重新创建它们。</span><span class="sxs-lookup"><span data-stu-id="eb666-139">If those maintenance requests and work orders are still required for the asset, you must manually re-create them after the asset is installed on the new location.</span></span>

7. <span data-ttu-id="eb666-140">若要查看功能位置安装的所有资产的列表（包括子资产），请在**所有功能位置**页选择该功能位置，然后选择**资产**。</span><span class="sxs-lookup"><span data-stu-id="eb666-140">To view a list of all the assets, including sub-assets, that are installed on the functional location, select the functional location on the **All Functional locations** page, and then select **Assets**.</span></span>
8. <span data-ttu-id="eb666-141">若要查看与功能位置安装的资产关联的有效维护请求、有效工作订单或故障登记的列表，请在**所有功能位置**页选择该功能位置，然后选择**请求**、**工作订单**或**故障**。</span><span class="sxs-lookup"><span data-stu-id="eb666-141">To view a list of active maintenance requests, active work orders, or fault registrations that are related to the assets that are installed on a functional location, select the functional location on the **All Functional locations** page, and then select **Requests**, **Work orders**, or **Faults**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb666-142">如果更改了与资产有关的数据，也会在安装该资产的功能位置自动更新这些数据。</span><span class="sxs-lookup"><span data-stu-id="eb666-142">When asset-related data is changed, it's automatically updated on the functional location that the asset is installed on.</span></span> <span data-ttu-id="eb666-143">此项自动更新与对维护请求、工作订单、资产故障登记、维护停机时间登记和资产度量登记的更改有关。</span><span class="sxs-lookup"><span data-stu-id="eb666-143">This automatic update pertains to changes to maintenance requests, work orders, asset fault registrations, maintenance downtime registrations, and asset measure registrations.</span></span>

## <a name="automatically-create-one-asset-on-a-functional-location"></a><span data-ttu-id="eb666-144">在功能位置自动创建一个资产</span><span class="sxs-lookup"><span data-stu-id="eb666-144">Automatically create one asset on a functional location</span></span>

<span data-ttu-id="eb666-145">可设置功能位置阶段和功能位置类型，以便处理功能位置*一个*资产的自动创建。</span><span class="sxs-lookup"><span data-stu-id="eb666-145">You can set up functional location stages and functional location types to handle the automatic creation of *one* asset on a functional location.</span></span> <span data-ttu-id="eb666-146">该资产获取的 ID 和名称与功能位置的相同。</span><span class="sxs-lookup"><span data-stu-id="eb666-146">The asset gets the same ID and name as the functional location.</span></span> <span data-ttu-id="eb666-147">处理对大型静态资产（如建筑物）的维护时，此功能可能非常有用。</span><span class="sxs-lookup"><span data-stu-id="eb666-147">This functionality might be useful when you're handling maintenance on a large, static asset, such as a building.</span></span>

<span data-ttu-id="eb666-148">必须有以下设置数据，才能在功能位置自动创建资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-148">Before you can automatically create an asset on a functional location, the following setup data must be available:</span></span>

- <span data-ttu-id="eb666-149">创建功能位置类型以处理资产的自动创建。</span><span class="sxs-lookup"><span data-stu-id="eb666-149">Create a functional location type to handle the automatic creation of an asset.</span></span> <span data-ttu-id="eb666-150">在**资产类型**字段中，选择资产类型。</span><span class="sxs-lookup"><span data-stu-id="eb666-150">In the **Asset type** field, select an asset type.</span></span> <span data-ttu-id="eb666-151">有关详细信息，请参阅[功能位置类型](../setup-for-functional-locations/functional-location-types.md)。</span><span class="sxs-lookup"><span data-stu-id="eb666-151">For more information, see [Functional location types](../setup-for-functional-locations/functional-location-types.md).</span></span>
- <span data-ttu-id="eb666-152">创建功能位置生命周期状态以处理资产的自动创建。</span><span class="sxs-lookup"><span data-stu-id="eb666-152">Create a functional location lifecycle state to handle the automatic creation of an asset.</span></span> <span data-ttu-id="eb666-153">将**创建资产**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="eb666-153">Set the **Create asset** option to **Yes**.</span></span> <span data-ttu-id="eb666-154">有关详细信息，请参阅[功能位置生命周期状态](../setup-for-functional-locations/functional-location-stages.md)。</span><span class="sxs-lookup"><span data-stu-id="eb666-154">For more information, see [Functional location lifecycle states](../setup-for-functional-locations/functional-location-stages.md).</span></span>

<span data-ttu-id="eb666-155">有设置数据之后，即可创建资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-155">After the setup data is available, you're ready to create an asset.</span></span>

1. <span data-ttu-id="eb666-156">在**所有功能位置**页中，确保要自动创建资产的功能位置使用您为此目的创建的功能位置类型。</span><span class="sxs-lookup"><span data-stu-id="eb666-156">On the **All Functional locations** page, make sure that the functional location where you want the asset to be automatically created uses the functional location type that you created for this purpose.</span></span>
2. <span data-ttu-id="eb666-157">在列表中选择功能位置。</span><span class="sxs-lookup"><span data-stu-id="eb666-157">Select the functional location in the list.</span></span>
3. <span data-ttu-id="eb666-158">选择**更新功能位置状态**，然后选择为此目的创建的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="eb666-158">Select **Update functional location state**, and then select the lifecycle state that you created for this purpose.</span></span> <span data-ttu-id="eb666-159">现在将在该功能位置自动安装一个资产。</span><span class="sxs-lookup"><span data-stu-id="eb666-159">One asset is now automatically installed on the functional location.</span></span> <span data-ttu-id="eb666-160">该资产与功能位置同名。</span><span class="sxs-lookup"><span data-stu-id="eb666-160">This asset has the same name as the functional location.</span></span>
