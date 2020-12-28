---
title: 资产度量
description: 本主题介绍如何在资产管理中创建资产度量类型。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423106"
---
# <a name="counters"></a><span data-ttu-id="a120a-103">计数器</span><span class="sxs-lookup"><span data-stu-id="a120a-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a120a-104">本主题介绍如何在资产管理中创建计数器类型。</span><span class="sxs-lookup"><span data-stu-id="a120a-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="a120a-105">计数器类型用于创建资产的计数器登记，如有关资产的生产工时数或生产数量。</span><span class="sxs-lookup"><span data-stu-id="a120a-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="a120a-106">资产类型与计数器类型关联。</span><span class="sxs-lookup"><span data-stu-id="a120a-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="a120a-107">这表示如果为资产使用的资产类型设置了计数器，则该计数器只能用于这个资产。</span><span class="sxs-lookup"><span data-stu-id="a120a-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="a120a-108">创建资产的计数器登记时，请首先在 **计数器** 中创建要使用的计数器类型。</span><span class="sxs-lookup"><span data-stu-id="a120a-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="a120a-109">然后，在 **计数器** 中创建资产的计数器登记。</span><span class="sxs-lookup"><span data-stu-id="a120a-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="a120a-110">可以在维护计划中使用计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="a120a-111">维护计划行的类型可以为“计数器”，例如，与生产工时数或生产数量有关。</span><span class="sxs-lookup"><span data-stu-id="a120a-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="a120a-112">可以根据生产工或生产的数量手动或自动更新计数器登记。</span><span class="sxs-lookup"><span data-stu-id="a120a-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="a120a-113">可设置计数器以使用三种更新方法之一（在 **计数器** 中 **更新** 字段内所选）：</span><span class="sxs-lookup"><span data-stu-id="a120a-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="a120a-114">手动 - 必须手动登记计数器值。</span><span class="sxs-lookup"><span data-stu-id="a120a-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="a120a-115">生产工时 - 根据生产工时数自动更新计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="a120a-116">生产数量 - 根据生产数量自动更新计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="a120a-117">如果使用生产数量，则计数器登记中包含 *所有* 已登记物料、良品数量，以及错误数量。</span><span class="sxs-lookup"><span data-stu-id="a120a-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="a120a-118">如果需要，始终可以手动登记计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="a120a-119">为资产计数器登记创建计数器类型</span><span class="sxs-lookup"><span data-stu-id="a120a-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="a120a-120">选择 **资产管理** > **设置** > **资产类型** > **计数器**。</span><span class="sxs-lookup"><span data-stu-id="a120a-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="a120a-121">选择 **新建** 以创建新计数器类型。</span><span class="sxs-lookup"><span data-stu-id="a120a-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="a120a-122">在 **计数器** 字段中插入 ID，在 **名称** 字段中插入计数器名称。</span><span class="sxs-lookup"><span data-stu-id="a120a-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="a120a-123">在 **常规** 快速选项卡上的 **单位** 字段中选择计数器单位。</span><span class="sxs-lookup"><span data-stu-id="a120a-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="a120a-124">在 **更新** 字段中，选择要用于计数器的更新方法。</span><span class="sxs-lookup"><span data-stu-id="a120a-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="a120a-125">如果资产结构中的子资产应该自动继承为父资产创建的计数器登记，请在 **继承计数器值** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="a120a-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="a120a-126">在 **聚合总计** 字段中，选择要用于使用此计数器类型的计数器的汇总方法。</span><span class="sxs-lookup"><span data-stu-id="a120a-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="a120a-127">“求和”是用于将登记的值连续相加到总和值中的标准选择。</span><span class="sxs-lookup"><span data-stu-id="a120a-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="a120a-128">如果设置计数器以监视阈值（如资产的相关温度、振动或磨损），可使用“平均值”。</span><span class="sxs-lookup"><span data-stu-id="a120a-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="a120a-129">在 **偏差上限** 字段中，插入以百分比表示的上限，以便验证手动计数器登记是否未超过预期范围。</span><span class="sxs-lookup"><span data-stu-id="a120a-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="a120a-130">此项验证基于现有计数器登记中的线性增加。</span><span class="sxs-lookup"><span data-stu-id="a120a-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="a120a-131">在 **偏差下限** 字段中，插入以百分比表示的下限，以便验证手动计数器登记是否未超过预期范围。</span><span class="sxs-lookup"><span data-stu-id="a120a-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="a120a-132">此项验证基于现有计数器登记中的线性减少。</span><span class="sxs-lookup"><span data-stu-id="a120a-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="a120a-133">在 **类型** 字段中，选择如果偏差超出在创建手动计数器登记时定义的范围，要显示的消息类型（参考、警告、错误）。</span><span class="sxs-lookup"><span data-stu-id="a120a-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="a120a-134">在 **资产类型** 快速选项卡上，添加应该可以使用计数器的资产类型。</span><span class="sxs-lookup"><span data-stu-id="a120a-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="a120a-135">在 **关联的资产计数器** 快速选项卡上，添加当更新此计数器时要自动更新的计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="a120a-136">仅当关联的计数器具有在计数器设置中与其关联的资产类型，才会自动更新此计数器。</span><span class="sxs-lookup"><span data-stu-id="a120a-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="a120a-137">例如：为“生产工时”设置计数器，并添加资产类型“卡车引擎”。</span><span class="sxs-lookup"><span data-stu-id="a120a-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="a120a-138">更新该计数器时，也将使用相同的计数器值更新关联的计数器“燃油”。</span><span class="sxs-lookup"><span data-stu-id="a120a-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="a120a-139">**计数器** 中的设置包含“工时”的设置。</span><span class="sxs-lookup"><span data-stu-id="a120a-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="a120a-140">此外，在“燃油”计数器中，应该将资产类型“卡车引擎”添加到 **资产类型** 快速选项卡上，以确保计数器关联。</span><span class="sxs-lookup"><span data-stu-id="a120a-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="a120a-141">有关“工时”和“燃油”计数器的设置示例，请参见下面的屏幕截图。</span><span class="sxs-lookup"><span data-stu-id="a120a-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="a120a-142">在 **计数器** 中向计数器类型添加资产类型时，将把该计数器自动添加到 [资产类型](../setup-for-objects/object-types.md)中 **计数器** 快速选项卡上的资产类型。</span><span class="sxs-lookup"><span data-stu-id="a120a-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![图 1](media/071-setup-for-objects.png)

