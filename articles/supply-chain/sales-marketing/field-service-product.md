---
title: 将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的产品的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546354"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品

[!include[banner](../includes/banner.md)]

此主题介绍用于将产品从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Field Service 的模板和基础任务。

使用的 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Supply Chain Management 到 Sales）– 直接**模板。 有关详细信息，请参阅[产品（Supply Chain Management 到 Sales）– 直接](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。

本主题仅介绍 **Field Service 产品（Supply Chain Management 到 Field Service）** 与**产品（Supply Chain Management 到Sales）– 直接**模板之间的差异。

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称**

- Field Service 产品（Supply Chain Management 到 Field Service）

**数据集成项目中的任务名称**

- 产品 - 产品

**Field Service 产品（Supply Chain Management 到 Field Service）** 模板中包含**产品（Supply Chain Management 到 Sales）– 直接**模板中不包含的一个映射。 此映射确保正确设置所需的 Field Service 特定的 **Field Service 产品类型**。

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

使用以下值映射。

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

在 Supply Chain Management 中，**适售的已发布产品**数据实体的 **Field Service 产品类型**值的计算方法如下：

- **库存：** 产品类型 = 产品和物料模型组，贮存的产品 = True
- **非库存：** 产品类型 = 产品和物料模型组，贮存的产品 = False
- **服务：** 产品类型 = 服务

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service 产品（Supply Chain Management 到 Field Service）：产品 - 产品

[![数据集成中的模板映射](./media/FSProduct.png)](./media/FSProduct.png)
