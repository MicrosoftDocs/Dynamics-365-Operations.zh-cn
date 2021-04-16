---
title: 装运集装箱
description: 本主题介绍如何为登陆成本模块设置装运集装箱。
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833705"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="e20e3-103">装运集装箱设置</span><span class="sxs-lookup"><span data-stu-id="e20e3-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e20e3-104">本主题介绍如何为 **登陆成本** 模块设置装运集装箱。</span><span class="sxs-lookup"><span data-stu-id="e20e3-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="e20e3-105">设置装运集装箱类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-105">Set up shipping container types</span></span>

<span data-ttu-id="e20e3-106">装运集装箱类型定义在装运和航行中可以使用的装运集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="e20e3-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="e20e3-107">要使用装运集装箱类型，转到 **登陆成本 \> 集装箱设置 \> 装运集装箱类型**。</span><span class="sxs-lookup"><span data-stu-id="e20e3-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="e20e3-108">您可以在那里查看、添加和删除集装箱类型的记录。</span><span class="sxs-lookup"><span data-stu-id="e20e3-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="e20e3-109">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="e20e3-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="e20e3-110">字段</span><span class="sxs-lookup"><span data-stu-id="e20e3-110">Field</span></span> | <span data-ttu-id="e20e3-111">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-111">Description</span></span> |
|---|---|
| <span data-ttu-id="e20e3-112">装运集装箱类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-112">Shipping container type</span></span> | <span data-ttu-id="e20e3-113">为装运集装箱类型输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="e20e3-114">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-114">Description</span></span> | <span data-ttu-id="e20e3-115">输入装运集装箱类型的描述。</span><span class="sxs-lookup"><span data-stu-id="e20e3-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="e20e3-116">体积</span><span class="sxs-lookup"><span data-stu-id="e20e3-116">Volume</span></span> | <span data-ttu-id="e20e3-117">输入此类型的装运集装箱允许的最大体积。</span><span class="sxs-lookup"><span data-stu-id="e20e3-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="e20e3-118">粗细</span><span class="sxs-lookup"><span data-stu-id="e20e3-118">Weight</span></span> | <span data-ttu-id="e20e3-119">输入此类型的装运集装箱允许的最大重量。</span><span class="sxs-lookup"><span data-stu-id="e20e3-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="e20e3-120">可退</span><span class="sxs-lookup"><span data-stu-id="e20e3-120">Returnable</span></span> | <span data-ttu-id="e20e3-121">指定此类型的装运集装箱是否可以在航行中使用后退还给供应商。</span><span class="sxs-lookup"><span data-stu-id="e20e3-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="e20e3-122">如果此选项设置为 *是*，将此类型的装运集装箱退回到始发港口可能需要支付额外成本。</span><span class="sxs-lookup"><span data-stu-id="e20e3-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="e20e3-123">设置装运集装箱</span><span class="sxs-lookup"><span data-stu-id="e20e3-123">Set up shipping containers</span></span>

<span data-ttu-id="e20e3-124">您可以使用装运集装箱记录来识别您在航行中使用的每个集装箱。</span><span class="sxs-lookup"><span data-stu-id="e20e3-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="e20e3-125">创建航行时，您可以在您在此处定义的所有装运集装箱记录的列表中为航行选择特定集装箱。</span><span class="sxs-lookup"><span data-stu-id="e20e3-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="e20e3-126">如果您的公司有自己的装运集装箱，此功能尤其有用。</span><span class="sxs-lookup"><span data-stu-id="e20e3-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="e20e3-127">您不必为仅使用一次的装运集装箱输入装运集装箱编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="e20e3-128">而是可以在创建航行时添加装运集装箱编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="e20e3-129">装运集装箱记录仅在登陆成本中使用。</span><span class="sxs-lookup"><span data-stu-id="e20e3-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="e20e3-130">它们在标准 **运输管理** 模块 (TMS) 中不可用。</span><span class="sxs-lookup"><span data-stu-id="e20e3-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="e20e3-131">要使用装运集装箱，转到 **登陆成本 \> 集装箱设置 \> 装运集装箱**。</span><span class="sxs-lookup"><span data-stu-id="e20e3-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="e20e3-132">您可以在那里查看、添加和删除装运集装箱的记录。</span><span class="sxs-lookup"><span data-stu-id="e20e3-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="e20e3-133">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="e20e3-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="e20e3-134">字段</span><span class="sxs-lookup"><span data-stu-id="e20e3-134">Field</span></span> | <span data-ttu-id="e20e3-135">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-135">Description</span></span> |
|---|---|
| <span data-ttu-id="e20e3-136">装运集装箱</span><span class="sxs-lookup"><span data-stu-id="e20e3-136">Shipping container</span></span> | <span data-ttu-id="e20e3-137">为装运集装箱输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="e20e3-138">装运集装箱类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-138">Shipping container type</span></span> | <span data-ttu-id="e20e3-139">选择装运集装箱的类型。</span><span class="sxs-lookup"><span data-stu-id="e20e3-139">Select the type of shipping container.</span></span> <span data-ttu-id="e20e3-140">有关详细信息，请参阅本主题前面的[设置装运集装箱类型](#shipping-container-types)一节。</span><span class="sxs-lookup"><span data-stu-id="e20e3-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="e20e3-141">装运集装箱设置是可选的。</span><span class="sxs-lookup"><span data-stu-id="e20e3-141">The shipping container setup is optional.</span></span> <span data-ttu-id="e20e3-142">通常，仅当您的公司有自己的装运集装箱或经常重复使用相同的装运集装箱时，您才会使用它。</span><span class="sxs-lookup"><span data-stu-id="e20e3-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="e20e3-143">不会为装运集装箱编号计算校验位。</span><span class="sxs-lookup"><span data-stu-id="e20e3-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="e20e3-144">设置单位类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-144">Set up unit types</span></span>

<span data-ttu-id="e20e3-145">单位类型为装运集装箱设定额外的分组和标识方法。</span><span class="sxs-lookup"><span data-stu-id="e20e3-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="e20e3-146">单位类型通常用于标识包装货物的集装箱的类型，如托盘或桶。</span><span class="sxs-lookup"><span data-stu-id="e20e3-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="e20e3-147">在 **所有装运集装箱** 页上设置集装箱时，您可以选择单位类型。</span><span class="sxs-lookup"><span data-stu-id="e20e3-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="e20e3-148">单位类型仅在登陆成本中使用。</span><span class="sxs-lookup"><span data-stu-id="e20e3-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="e20e3-149">它们在 TMS 中不可用。</span><span class="sxs-lookup"><span data-stu-id="e20e3-149">They aren't available in TMS.</span></span>

<span data-ttu-id="e20e3-150">要使用单位类型，转到 **登陆成本 \> 集装箱设置 \> 单位类型**。</span><span class="sxs-lookup"><span data-stu-id="e20e3-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="e20e3-151">您可以在那里查看、添加和删除单位类型的记录。</span><span class="sxs-lookup"><span data-stu-id="e20e3-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="e20e3-152">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="e20e3-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="e20e3-153">字段</span><span class="sxs-lookup"><span data-stu-id="e20e3-153">Field</span></span> | <span data-ttu-id="e20e3-154">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-154">Description</span></span> |
|---|---|
| <span data-ttu-id="e20e3-155">单位类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-155">Unit type</span></span> | <span data-ttu-id="e20e3-156">为单位类型输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="e20e3-157">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-157">Description</span></span> | <span data-ttu-id="e20e3-158">输入单位类型的描述。</span><span class="sxs-lookup"><span data-stu-id="e20e3-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="e20e3-159">设置冷冻类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-159">Set up refrigeration types</span></span>

<span data-ttu-id="e20e3-160">冷冻类型为装运集装箱（通常是冷藏集装箱）设定额外的分组和标识方法。</span><span class="sxs-lookup"><span data-stu-id="e20e3-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="e20e3-161">在 **所有装运集装箱** 页上设置集装箱时，您可以选择冷冻类型。</span><span class="sxs-lookup"><span data-stu-id="e20e3-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="e20e3-162">要使用冷冻类型，转到 **登陆成本 \> 集装箱设置 \> 冷冻类型**。</span><span class="sxs-lookup"><span data-stu-id="e20e3-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="e20e3-163">您可以在那里查看、添加和删除冷冻类型的记录。</span><span class="sxs-lookup"><span data-stu-id="e20e3-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="e20e3-164">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="e20e3-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="e20e3-165">字段</span><span class="sxs-lookup"><span data-stu-id="e20e3-165">Field</span></span> | <span data-ttu-id="e20e3-166">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-166">Description</span></span> |
|---|---|
| <span data-ttu-id="e20e3-167">冷冻类型</span><span class="sxs-lookup"><span data-stu-id="e20e3-167">Refrigeration type</span></span> | <span data-ttu-id="e20e3-168">为冷冻类型输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="e20e3-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="e20e3-169">说明</span><span class="sxs-lookup"><span data-stu-id="e20e3-169">Description</span></span> | <span data-ttu-id="e20e3-170">输入冷冻类型的描述。</span><span class="sxs-lookup"><span data-stu-id="e20e3-170">Enter a description of the refrigeration type.</span></span> |