---
title: 其他货位区域
description: 本主题概述已向 Microsoft Dynamics 365 Supply Chain Management 添加的新货位区域。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423364"
---
# <a name="additional-location-zones"></a><span data-ttu-id="05502-103">其他货位区域</span><span class="sxs-lookup"><span data-stu-id="05502-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05502-104">Microsoft Dynamics 365 Supply Chain Management 中新增了三个区域字段。</span><span class="sxs-lookup"><span data-stu-id="05502-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="05502-105">仓库经理可将其用于定义更多仓库组织或布局。</span><span class="sxs-lookup"><span data-stu-id="05502-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="05502-106">可以手动或通过使用 **货位设置** 向导设置新区域字段。</span><span class="sxs-lookup"><span data-stu-id="05502-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="05502-107">可以在任何使用“货位”表的查询或筛选中使用这些字段。</span><span class="sxs-lookup"><span data-stu-id="05502-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="05502-108">无需进行更多设置即可使用区域字段。</span><span class="sxs-lookup"><span data-stu-id="05502-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="05502-109">开启“其他货位区域”功能</span><span class="sxs-lookup"><span data-stu-id="05502-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="05502-110">*其他货位区域* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="05502-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="05502-111">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="05502-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="05502-112">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="05502-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="05502-113">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="05502-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="05502-114">**功能名称**：*其他货位区域*</span><span class="sxs-lookup"><span data-stu-id="05502-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="05502-115">使用货位区域</span><span class="sxs-lookup"><span data-stu-id="05502-115">Use location zones</span></span>

1. <span data-ttu-id="05502-116">转到 **仓库管理 \> 设置 \> 仓库 \> 货位设置向导**。</span><span class="sxs-lookup"><span data-stu-id="05502-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="05502-117">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="05502-117">Set the following values:</span></span>

    - <span data-ttu-id="05502-118">在 **仓库** 字段中，选择 _62_。</span><span class="sxs-lookup"><span data-stu-id="05502-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="05502-119">在 **区域 ID** 字段中，选择 _FLOOR_。</span><span class="sxs-lookup"><span data-stu-id="05502-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="05502-120">在 **其他区域 1** 字段中，选择 _PICKZONE1_。</span><span class="sxs-lookup"><span data-stu-id="05502-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="05502-121">在 **其他区域 2** 字段中，选择 _WEBSHOP1_。</span><span class="sxs-lookup"><span data-stu-id="05502-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="05502-122">在 **货位模板 ID** 字段中，选择 _FLOOR_。</span><span class="sxs-lookup"><span data-stu-id="05502-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="05502-123">选择 **场地** 行。</span><span class="sxs-lookup"><span data-stu-id="05502-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="05502-124">在 **起始编号** 字段中，输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="05502-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="05502-125">在 **结束编号** 字段中，输入 _3_。</span><span class="sxs-lookup"><span data-stu-id="05502-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="05502-126">选择 **通道** 行。</span><span class="sxs-lookup"><span data-stu-id="05502-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="05502-127">在 **起始编号** 字段中，输入 _1_。</span><span class="sxs-lookup"><span data-stu-id="05502-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="05502-128">在 **结束编号** 字段中，输入 _5_。</span><span class="sxs-lookup"><span data-stu-id="05502-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="05502-129">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="05502-129">Select **Create**.</span></span>
8. <span data-ttu-id="05502-130">将收到消息，说明已添加了新货位。</span><span class="sxs-lookup"><span data-stu-id="05502-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="05502-131">选择 **显示消息** 按钮查看消息。</span><span class="sxs-lookup"><span data-stu-id="05502-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="05502-132">转到 **仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="05502-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="05502-133">将在列表中显示新货位，并且可使用所有区域字段（即，现有区域字段和新的其他区域字段）。</span><span class="sxs-lookup"><span data-stu-id="05502-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
