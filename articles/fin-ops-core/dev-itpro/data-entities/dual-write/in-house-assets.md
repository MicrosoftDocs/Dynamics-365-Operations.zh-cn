---
title: 需服务的内部资产
description: 此主题介绍如何使用 Microsoft Dtnamics 365 Field Service 服务客户资产和内部资产。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112397"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="53f1f-103">需服务的内部资产</span><span class="sxs-lookup"><span data-stu-id="53f1f-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="53f1f-104">Microsoft Dynamics 365 Field Service 用于服务客户资产。</span><span class="sxs-lookup"><span data-stu-id="53f1f-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="53f1f-105">Dynamics 365 Supply Chain Management 的资产管理用于维护内部资产。</span><span class="sxs-lookup"><span data-stu-id="53f1f-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="53f1f-106">这两个应用程序的集成让您可以使用 Field Service 服务客户资产和内部资产。</span><span class="sxs-lookup"><span data-stu-id="53f1f-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="53f1f-107">也可以根据功能位置层次结构为资产分类，以及以详细级别跟踪服务。</span><span class="sxs-lookup"><span data-stu-id="53f1f-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="53f1f-108">有关详细信息，请参阅[集成 Dynamics 365 Field Service 和 Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration)。</span><span class="sxs-lookup"><span data-stu-id="53f1f-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="53f1f-109">模板</span><span class="sxs-lookup"><span data-stu-id="53f1f-109">Templates</span></span>

<span data-ttu-id="53f1f-110">内部资产包括核心实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="53f1f-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="53f1f-111">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="53f1f-111">Finance and Operations apps</span></span> | <span data-ttu-id="53f1f-112">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="53f1f-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="53f1f-113">说明</span><span class="sxs-lookup"><span data-stu-id="53f1f-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="53f1f-114">资产管理资产生命周期模型</span><span class="sxs-lookup"><span data-stu-id="53f1f-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="53f1f-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="53f1f-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="53f1f-116">资产管理资产生命周期状态</span><span class="sxs-lookup"><span data-stu-id="53f1f-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="53f1f-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="53f1f-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="53f1f-118">资产管理资产</span><span class="sxs-lookup"><span data-stu-id="53f1f-118">Asset management assets</span></span> | <span data-ttu-id="53f1f-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="53f1f-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="53f1f-120">资产管理资产类型</span><span class="sxs-lookup"><span data-stu-id="53f1f-120">Asset management asset types</span></span> | <span data-ttu-id="53f1f-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="53f1f-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="53f1f-122">资产管理功能位置生命周期模型</span><span class="sxs-lookup"><span data-stu-id="53f1f-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="53f1f-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="53f1f-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="53f1f-124">资产管理功能位置生命周期状态</span><span class="sxs-lookup"><span data-stu-id="53f1f-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="53f1f-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="53f1f-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="53f1f-126">资产管理功能位置</span><span class="sxs-lookup"><span data-stu-id="53f1f-126">Asset management functional locations</span></span> | <span data-ttu-id="53f1f-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="53f1f-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="53f1f-128">资产管理功能位置类型</span><span class="sxs-lookup"><span data-stu-id="53f1f-128">Asset management functional location types</span></span> | <span data-ttu-id="53f1f-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="53f1f-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="53f1f-130">资产管理制造商</span><span class="sxs-lookup"><span data-stu-id="53f1f-130">Asset management manufacturers</span></span> | <span data-ttu-id="53f1f-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="53f1f-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="53f1f-132">资产管理模型</span><span class="sxs-lookup"><span data-stu-id="53f1f-132">Asset management models</span></span> | <span data-ttu-id="53f1f-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="53f1f-133">msdyn\_models</span></span> | |
| <span data-ttu-id="53f1f-134">资产管理保修</span><span class="sxs-lookup"><span data-stu-id="53f1f-134">Asset management warranty</span></span> | <span data-ttu-id="53f1f-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="53f1f-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
