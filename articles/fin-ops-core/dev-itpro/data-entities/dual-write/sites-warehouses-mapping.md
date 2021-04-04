---
title: 集成的站点和仓库
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560353"
---
# <a name="integrated-sites-and-warehouses"></a>集成的站点和仓库

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。 运营站点和仓库是 Supply Chain Management 应用程序中的常见概念。 用于为公司的供应链建模。

## <a name="templates"></a>模板

通过与 Dataverse 集成，Dataverse 中使用下表中的站点和仓库数据表提供这些概念及其所有相关信息。

Finance and Operations 应用 | 其他 Dynamics 365 应用 | 说明
--------------------------|---------------------------|---
站点 | msdyn_operationalsites | 
仓库 | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]