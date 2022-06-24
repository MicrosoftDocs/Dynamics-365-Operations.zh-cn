---
title: 扩展现有库存量数据实体
description: 本文提供了一个示例，演示如何向 INVENTORSITEONHANDENTITY 和 INVENTWAREHOUSEONHANDENTITY 视图添加扩展字段，以使现有库存量数据实体的功能可以使用扩展。
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906028"
---
# <a name="extend-inventory-on-hand-data-entities"></a>扩展现有库存量数据实体

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 提供[可扩展性](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)功能，让您可以[通过扩展将字段添加到表中](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md)。 本文提供了一个示例，演示如何向 `INVENTORSITEONHANDENTITY` 和 `INVENTWAREHOUSEONHANDENTITY` 视图添加扩展字段，以使现有库存量数据实体的功能可以使用扩展。 有关数据实体的详细信息，请参阅[数据管理概述](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)。

> [!NOTE]
> 以下是包含一部分现有库存量数据实体的列表：
>
> - 按站点分类的现有库存
> - 按站点分类的现有库存 V2
> - 现有库存(按仓库分类)
> - 按仓库分类的现有库存量 v2

在将字段添加到 `inventSiteOnHandView` 视图使用的表中之后，必须同步引擎，以正确识别扩展。

1. 通过添加扩展字段来扩展 `InventSiteOnHandView` 视图。
1. 使用扩展字段扩展 `InventSiteOnHandAggregatedView` 视图。
1. 通过修改 `getExtensionFields()` 方法来扩展 `InventSiteOnHandAggregatedViewBuilder` viewBuilder 类。 这样，您可以在运行 viewBuilder 同步时将旧视图字段映射到新视图字段。

例如，您通过扩展将以下四个字段添加到了 `InventTable` 表中：

- 自定义字段 1
- 自定义字段 2
- 自定义字段 3
- 自定义字段 4

在这种情况下，您必须按照以下方式修改 `getExtensionFields()` 方法。

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

完成这些步骤后，您可以通过添加新字段来扩展按站点分类的现有库存量和按仓库数据实体分类的现有库存量。 这样，您可以确保在使用这些数据实体的数据迁移期间扩展字段会被识别出并包含。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]