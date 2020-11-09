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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997162"
---
# <a name="in-house-assets-for-servicing"></a>需服务的内部资产

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service 用于服务客户资产。 Dynamics 365 Supply Chain Management 的资产管理用于维护内部资产。 这两个应用程序的集成让您可以使用 Field Service 服务客户资产和内部资产。 也可以根据功能位置层次结构为资产分类，以及以详细级别跟踪服务。

有关详细信息，请参阅[集成 Dynamics 365 Field Service 和 Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration)。

## <a name="templates"></a>模板

内部资产包括核心实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| Finance and Operations 应用 | Dynamics 365 中的模型驱动应用 | 说明 |
|-----------------------------|-----------------------------------|-------------|
| 资产管理资产生命周期模型 | msdyn\_assetlifecyclemodels | |
| 资产管理资产生命周期状态 | msdyn\_assetlifecyclestates | |
| 资产管理资产 | msdyn\_customerassets | |
| 资产管理资产类型 | msdyn\_customerassetcategories | |
| 资产管理功能位置生命周期模型 | msdyn\_functionallocationlifecyclemodels | |
| 资产管理功能位置生命周期状态 | msdyn\_functionallocationlifecyclestates | |
| 资产管理功能位置 | msdyn\_functionallocations | |
| 资产管理功能位置类型 | msdyn\_functionallocationtypes | |
| 资产管理制造商 | msdyn\_manufacturers | |
| 资产管理模型 | msdyn\_models | |
| 资产管理保修 | msdyn\_warranties | |

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
