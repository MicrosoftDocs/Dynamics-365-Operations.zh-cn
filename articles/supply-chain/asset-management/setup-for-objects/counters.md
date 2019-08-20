---
title: 资产度量
description: 本主题介绍如何在资产管理中创建资产度量类型。
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
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783105"
---
# <a name="asset-measures"></a><span data-ttu-id="b37c9-103">资产度量</span><span class="sxs-lookup"><span data-stu-id="b37c9-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b37c9-104">本主题介绍如何在资产管理中创建资产度量类型。</span><span class="sxs-lookup"><span data-stu-id="b37c9-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="b37c9-105">资产度量类型用于创建资产的度量登记，如有关资产的生产工时数或生产数量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="b37c9-106">资产类型与资产度量类型关联。</span><span class="sxs-lookup"><span data-stu-id="b37c9-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="b37c9-107">这表示如果为资产使用的资产类型设置了资产度量，则该资产度量只能用于这个资产。</span><span class="sxs-lookup"><span data-stu-id="b37c9-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="b37c9-108">创建资产的度量登记时，请首先在**计数器**中创建要使用的资产度量类型。</span><span class="sxs-lookup"><span data-stu-id="b37c9-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="b37c9-109">然后，在**资产度量**中创建资产的度量登记。</span><span class="sxs-lookup"><span data-stu-id="b37c9-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="b37c9-110">可以在维护计划中使用资产度量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="b37c9-111">维护计划行的类型可以为“计数器”，例如，与生产工时数或生产数量有关。</span><span class="sxs-lookup"><span data-stu-id="b37c9-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="b37c9-112">可以根据生产工或生产的数量手动或自动更新资产度量登记。</span><span class="sxs-lookup"><span data-stu-id="b37c9-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="b37c9-113">可设置资产度量以使用三种更新方法之一（在**计数器**中**更新**字段内所选）：</span><span class="sxs-lookup"><span data-stu-id="b37c9-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="b37c9-114">手动 - 必须手动登记资产度量值。</span><span class="sxs-lookup"><span data-stu-id="b37c9-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="b37c9-115">生产工时 - 根据生产工时数自动更新计数器。</span><span class="sxs-lookup"><span data-stu-id="b37c9-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="b37c9-116">生产数量 - 根据生产数量自动更新计数器。</span><span class="sxs-lookup"><span data-stu-id="b37c9-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="b37c9-117">如果使用生产数量，则度量登记中包含*所有*已登记物料、良品数量，以及错误数量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="b37c9-118">如果需要，始终可以手动登记资产度量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="b37c9-119">为资产计数器登记创建计数器类型</span><span class="sxs-lookup"><span data-stu-id="b37c9-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="b37c9-120">选择**资产管理** > **设置** > **资产类型** > **计数器**。</span><span class="sxs-lookup"><span data-stu-id="b37c9-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="b37c9-121">选择**新建**以创建新资产度量类型。</span><span class="sxs-lookup"><span data-stu-id="b37c9-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="b37c9-122">在**计数器**字段中插入 ID，在**名称**字段中插入计数器名称。</span><span class="sxs-lookup"><span data-stu-id="b37c9-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="b37c9-123">在**常规**快速选项卡上的**单位**字段中选择度量单位。</span><span class="sxs-lookup"><span data-stu-id="b37c9-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="b37c9-124">在**更新**字段中，选择要用于资产度量的更新方法。</span><span class="sxs-lookup"><span data-stu-id="b37c9-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="b37c9-125">如果资产结构中的子资产应该自动继承为父资产创建的资产度量登记，请在**继承计数器值**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="b37c9-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="b37c9-126">在**聚合总计**字段中，选择要用于使用此资产度量类型的资产度量的汇总方法。</span><span class="sxs-lookup"><span data-stu-id="b37c9-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="b37c9-127">“求和”是用于将登记的值连续相加到总和值中的标准选择。</span><span class="sxs-lookup"><span data-stu-id="b37c9-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="b37c9-128">如果设置资产度量以监视阈值（如资产的相关温度、振动或磨损），可使用“平均值”。</span><span class="sxs-lookup"><span data-stu-id="b37c9-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="b37c9-129">在**偏差上限**字段中，插入以百分比表示的上限，以便验证手动资产度量登记是否未超过预期范围。</span><span class="sxs-lookup"><span data-stu-id="b37c9-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="b37c9-130">此项验证基于现有资产度量登记中的线性增加。</span><span class="sxs-lookup"><span data-stu-id="b37c9-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="b37c9-131">在**偏差下限**字段中，插入以百分比表示的下限，以便验证手动资产度量登记是否未超过预期范围。</span><span class="sxs-lookup"><span data-stu-id="b37c9-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="b37c9-132">此项验证基于现有资产度量登记中的线性下降。</span><span class="sxs-lookup"><span data-stu-id="b37c9-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="b37c9-133">在**类型**字段中，选择如果偏差超出在创建手动资产度量登记时定义的范围，要显示的消息类型（参考、警告、错误）。</span><span class="sxs-lookup"><span data-stu-id="b37c9-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="b37c9-134">在**资产类型**快速选项卡上，添加应该可以使用资产度量的资产类型。</span><span class="sxs-lookup"><span data-stu-id="b37c9-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="b37c9-135">在**关联的资产度量**快速选项卡上，添加当更新此资产度量时要自动更新的资产度量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="b37c9-136">仅当关联的资产度量具有在资产度量设置中与其关联的资产类型，才会自动更新此资产度量。</span><span class="sxs-lookup"><span data-stu-id="b37c9-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="b37c9-137">例如：为“生产工时”设置资产度量，并添加资产类型“卡车引擎”。</span><span class="sxs-lookup"><span data-stu-id="b37c9-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="b37c9-138">更新该资产度量时，也将使用相同的资产度量值更新关联的计数器“燃油”。</span><span class="sxs-lookup"><span data-stu-id="b37c9-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="b37c9-139">**计数器**中的设置包含“工时”的设置。</span><span class="sxs-lookup"><span data-stu-id="b37c9-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="b37c9-140">此外，在“燃油”资产度量中，应该将资产类型“卡车引擎”添加到**资产类型**快速选项卡上，以确保资产度量关联。</span><span class="sxs-lookup"><span data-stu-id="b37c9-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="b37c9-141">有关“工时”和“燃油”资产度量的设置示例，请参见下面的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="b37c9-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="b37c9-142">在**计数器**中向资产度量类型添加资产类型时，将把该资产度量自动添加到[资产类型](../setup-for-objects/object-types.md)中**计数器**快速选项卡上的资产类型。</span><span class="sxs-lookup"><span data-stu-id="b37c9-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![图 1](media/071-setup-for-objects.png)


