---
title: 将具有库存单位的产品从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835686"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>将具有库存单位的产品从 Finance and Operations 同步到 Field Service

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)

所用**具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）** 模板基于 **Field Service 产品（Fin and Ops 到 Field Service）** 模板。 有关详细信息，请参阅 [Field Service 产品（Finance and Operations 到 Field Service）](field-service-product.md)。

本主题仅介绍这两个模板之间的区别： 
- **具有库存单位的 Field Service 产品（Fin and Ops 到 Sales）**
- **Field Service 产品（Fin and Ops 到 Field Service）** 

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称：**

- 具有库存单位的 Field Service 产品（Fin and Ops 到 Sales）

**数据集成项目中的任务名称：**

- 产品

**具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）** 模板包括 **Field Service 产品（Fin and Ops 到 Field Service）** 模板中不包括的一个映射。 此映射确保包括库存水平同步所需的库存单位。

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）：产品

[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)
