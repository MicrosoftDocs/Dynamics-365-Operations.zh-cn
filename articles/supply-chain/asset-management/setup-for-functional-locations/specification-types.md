---
title: 维护属性类型
description: 本主题介绍如何在资产管理中创建属性类型。
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b221e9168fc60b5927bb92de80bd6b9614ad591c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019796"
---
# <a name="maintenance-attribute-types"></a>维护属性类型

[!include [banner](../../includes/banner.md)]

 

本主题介绍如何在资产管理中创建属性类型。 属性用于描述各种元素的属性。 可为以下元素设置属性：

- [功能位置类型](../setup-for-functional-locations/functional-location-types.md)
- [创建功能位置](../functional-locations/create-functional-locations.md)
- [资产类型](../setup-for-objects/object-types.md)
- 资产

可设置的属性取决于元素。 例如，对于功能位置，可为位置的配置和物理大小设置属性。 对于资产类型或资产，可设置引擎体积、功耗和最大容量负荷在不同条件下的属性。

## <a name="create-attribute-types"></a>创建属性类型

可以创建自己的属性类型。 错误，还可以将产品维度转移到 **属性类型** 页。

1. 选择 **拥有管理** \> **设置** \> **属性类型**。
2. 首次设置属性类型时，选择 **创建产品属性** 以自动转移标准产品维度。
3. 选择 **新建** 以创建新属性类型。
4. 在 **属性类型** 字段中，输入属性类型的名称。
5. 在 **描述** 字段中，输入描述。
6. 在 **单位** 字段中，根据需要选择相关属性单位。
7. 在 **数据类型** 字段中，选择单位的数据类型。
8. 如果数据类型选择的是 **字符串**，则执行以下步骤创建属性类型的值：

    1. 选择属性类型，然后选择 **值**。
    2. 在 **属性值** 字段中，选择 **新建**。
    3. 在 **属性类型** 字段中，选择一个属性类型（维度）。
    4. 在 **值** 字段中，输入一个相关值。
    5. 在 **描述** 字段中，输入描述。
    6. 保存该记录。
    7. 回到 **属性类型** 页。

9. 保存该记录。

    **功能位置类型** 字段显示使用属性类型的功能位置的数量。 **资产类型** 字段显示正在使用功能位置的资产类型的数量。
