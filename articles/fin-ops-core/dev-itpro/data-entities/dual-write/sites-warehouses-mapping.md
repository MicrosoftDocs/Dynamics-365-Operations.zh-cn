---
title: 集成的站点和仓库
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的站点和仓库数据集成。
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173054"
---
# <a name="integrated-sites-and-warehouses"></a>集成的站点和仓库

[!include [banner](../../includes/banner.md)]



本主题介绍 Finance and Operations 与 Common Data Service 之间的站点和仓库数据集成。 运营站点和仓库是 Supply Chain Management 应用程序中的常见概念。 用于为公司的供应链建模。

## <a name="templates"></a>模板

通过与 Common Data Service 集成，Common Data Service 中使用下表中的站点和仓库数据提供这些概念及其所有相关信息。

Finance and Operations 应用 | 其他 Dynamics 365 应用 | 说明
--------------------------|---------------------------|---
站点 | msdyn_operationalsites | 
仓库 | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

