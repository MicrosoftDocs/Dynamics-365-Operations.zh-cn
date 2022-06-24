---
title: 将具有库存单位的产品从 Supply Chain Management 同步到 Field Service
description: 本文介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887245"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>将具有库存单位的产品从 Supply Chain Management 同步到 Field Service

[!include[banner](../includes/banner.md)]

本文介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步。](./media/FSProductsOW.png)](./media/FSProductsOW.png)

所用 **具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板。 有关详细信息，请参阅[将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品](field-service-product.md)。

本文仅介绍这两个模板之间的区别： 
- **具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）**
- **Field Service 产品（Supply Chain Management 到 Field Service）** 

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称：**

- 具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）

**数据集成项目中的任务名称：**

- 产品

**具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板中包含 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板中不包含的一个映射。 此映射确保包括库存水平同步所需的库存单位。

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）：产品

[![数据集成中的模板映射。](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]