---
title: 将具有库存单位的产品从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "359236"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>将具有库存单位的产品从 Finance and Operations 同步到 Field Service

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)

使用的 **Field Service 产品（Finance and Operations 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Finance and Operations 到Sales）– 直接**模板。 有关详细信息，请参阅[产品（Finance and Operations 到 Sales）– 直接](products-template-mapping-direct.md)。

本主题仅介绍 **Field Service 产品（Finance and Operations 到 Field Service）** 与 **Field Service 产品（Finance and Operations 到Sales）– 直接**模板之间的差异。

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称：**

- 具有库存单位的 Field Service 产品（Finance and Operations 到 Sales）

**数据集成项目中的任务名称：**

- 产品

**具有库存单位的 Field Service 产品（Finance and Operations 到 Field Service）** 模板包括 **Field Service 产品（Finance and Operations 到 Field Service）** 模板中不包括的一个映射。 此映射确保包括库存水平同步所需的库存单位。

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>具有库存单位的 Field Service 产品（Finance and Operations 到 Field Service）：产品

[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)
