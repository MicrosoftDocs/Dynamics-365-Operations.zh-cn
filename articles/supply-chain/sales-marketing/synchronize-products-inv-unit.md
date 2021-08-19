---
title: 将具有库存单位的产品从 Supply Chain Management 同步到 Field Service
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
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
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1312015fe5b9b95a341e9e7170dfc5106f47f0875f89224983e5ec61dd8de5ff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717859"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>将具有库存单位的产品从 Supply Chain Management 同步到 Field Service

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步。](./media/FSProductsOW.png)](./media/FSProductsOW.png)

所用 **具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板。 有关详细信息，请参阅[将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品](field-service-product.md)。

本主题仅介绍这两个模板之间的区别： 
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