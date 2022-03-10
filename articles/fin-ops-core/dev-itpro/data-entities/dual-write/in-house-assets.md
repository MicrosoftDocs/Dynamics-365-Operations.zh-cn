---
title: 用于服务的内部资产
description: 本主题介绍如何使用 Microsoft Dynamics 365 Field Service 为客户资产和内部资产服务。
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 8048a99951eea3fbae34e56c1b444c75ad3d199d
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781408"
---
# <a name="in-house-assets-for-servicing"></a>用于服务的内部资产

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service 用于服务客户资产。 Dynamics 365 Supply Chain Management 的资产管理用于维护内部资产。 这两个应用程序的集成让您可以使用 Field Service 服务客户资产和内部资产。 也可以根据功能位置层次结构为资产分类，以及以详细级别跟踪服务。

有关详细信息，请参阅[集成 Dynamics 365 Field Service 和 Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration)。

## <a name="templates"></a>模板

内部资产包括核心表映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| Finance and Operations 应用 | 客户互动应用 | 说明 |
|-----------------------------|-----------------------------------|-------------|
[资产管理资产生命周期模型](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[资产管理资产生命周期状态](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[资产管理资产类型](mapping-reference.md#124) | msdyn_customerassetcategories | |
[资产管理资产](mapping-reference.md#125) | msdyn_customerassets | |
[资产管理功能位置生命周期模型](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[资产管理功能位置生命周期状态](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[资产管理功能位置类型](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[资产管理功能位置](mapping-reference.md#136) | msdyn_functionallocations | |
[资产管理制造商](mapping-reference.md#153) | msdyn_manufacturers | |
[资产管理模型](mapping-reference.md#154) | msdyn_models | |
[资产管理保修](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
