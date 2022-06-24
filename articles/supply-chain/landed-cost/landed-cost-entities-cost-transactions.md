---
title: 成本交易记录实体
description: 本文提供有关成本交易实体的信息，通过选择分摊方法，可以在成本区域的内容中拆分成本的值。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860803"
---
# <a name="cost-transaction-entities"></a>成本交易实体

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>分摊

通过选择分摊方法，到岸成本可使成本值在成本区域（航行、装运集装箱等）的内容之间拆分。 分摊方法设置为基于业务规则的自动成本配置的一部分。 创建航行行时，它作为成本的一部分被提取。

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>配置分摊映射以供数据实体使用

从外部源（如货运转运商）创建成本后，外部源无法指定用于分摊成本值的首选方法。 分摊映射定义每个成本类型代码的默认分摊方法。 分摊映射表从 Microsoft Dynamics 365 Supply Chain Management 内的 **分摊映射** 页（**到岸成本 \> 成本 计算设置 \> 分摊映射**）中访问。

如果已定义映射组合，并且使用成本交易实体创建了与成本类型代码匹配的成本，则将使用映射的分摊方法，而不是提供给实体的任何值。

如果映射表中不存在值，但已向实体提供值，则将使用提供的值。

如果映射表或已提交到实体的记录中不存在值，则创建将失败。

### <a name="apportionment-mapping-itmapportionmentmapping"></a>分摊映射 (ITMApportionmentMapping)

分摊映射实体 (`ITMApportionmentMapping`) 创建分摊映射关系，并允许用户创建或更新记录。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分摊方法 | ITMApportionmentMapping.ApportionmentMethod | Int | 否 | 否 |
| 成本类型代码 | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **是** | 否 |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>航行成本 (ITMCostTransVoyageEntity)

航行成本实体 (`ITMCostTransVoyageEntity`) 创建在航行级别应用的航行成本交易。 在导入过程中，系统使用实体中包含的 **类别** 和 **分摊方法** 值，来确定如何在航行内容中分摊成本值。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分摊方法 | ITMCostTrans.ApportionmentMethod | Int | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 航行 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>装运集装箱成本 (ITMCostTransShippingContainerEntity)

装运集装箱成本实体 (`ITMCostTransShippingContainerEntity`) 创建在装运集装箱级别应用的装运集装箱成本。 在导入过程中，系统使用实体中包含的 **类别** 和 **分摊方法** 值，来确定如何在装运集装箱内容中分摊成本值。

**聚合**、**支线** 和 **链接支线** 字段特定于 **成本区域** 值为 *装运集装箱* 的记录。 因此，它们在其他成本区域的数据实体中不存在。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 聚合 | ITMCostTrans.AggregatedCost | Int | 否 | 否 |
| 分摊方法 | ITMCostTrans.ApportionmentMethod | Int | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 链接的支线 | ITMCostTrans.LinkLegId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 装运集装箱 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 航行 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 支线 | ITMCostTrans.ShipLegId | Nvarchar(20) | 否 | 否 |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |

## <a name="folio-costs-itmcosttransfolioentity"></a>帐页成本 (ITMCostTransFolioEntity)

帐页成本实体 (`ITMCostTransFolioEntity`) 创建适用于帐页级别的成本交易记录。 在导入过程中，系统使用实体中包含的 **类别** 和 **分摊方法** 值，来确定如何在帐页成本内容中分摊成本值。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分摊方法 | ITMCostTrans.ApportionmentMethod | Int | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 帐页 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>采购订单成本 (ITMCostTransPurchaseEntity)

采购订单成本实体 (`ITMCostTransPurchaseEntity`) 创建适用于采购订单标题的成本交易。 在导入过程中，系统使用实体中包含的 **类别** 和 **分摊方法** 值，来确定如何在帐页成本内容中分摊成本值。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分摊方法 | ITMCostTrans.ApportionmentMethod | Int | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 采购订单 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |

## <a name="item-costs-itmcosttransitementity"></a>物料成本 (ITMCostTransItemEntity)

物料成本实体 (`ITMCostTransItemEntity`) 创建适用于物料级别的成本交易。 此实体特定于采购订单行上的物料。 成本值已完全应用于行。

**调整金额** 和 **值调整** 字段特定于行级别成本区域。 因此，它们在其他成本区域的数据实体中不存在。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 调整金额 | ITMCostTrans.AdjustmentAmount | 数字(32, 6) | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 采购订单 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 采购订单行编号 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |
| 值调整 | ITMCostTrans.ValueAdjustmentMethod | Int | 否 | 否 |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>转移行成本 (ITMCostTransTransferLineEntity)

转移行成本实体 (`ITMCostTransTransferLineEntity`) 创建适用于转移单行级别的成本交易。 这些成本的值已完全应用于转移单行。

**调整金额** 和 **值调整** 字段特定于行级别成本区域。 因此，它们在其他成本区域的数据实体中不存在。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 调整金额 | ITMCostTrans.AdjustmentAmount | 数字(32, 6) | 否 | 否 |
| 成本价值 | ITMCostTrans.CostValue | 数字(32, 6) | 否 | 否 |
| 货币 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 否 | **是** |
| 行号 | ITMCostTrans.LineNum | 数字(32, 16) | **是** | 否 |
| 链接的成本类型 | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 否 | 否 |
| 最低成本 | ITMCostTrans.MinCostAmount | 数字(32, 6) | 否 | 否 |
| 类别 | ITMCostTrans.ShipCostCategory | Int | 否 | 否 |
| 成本类型代码 | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 否 | 否 |
| 公司 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 转移单 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 转移单行编号 | ITMCostTrans.TransRecId | Nvarchar(20) | **是** | 否 |
| 物料销售税组 | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 否 | 否 |
| 值调整 | ITMCostTrans.ValueAdjustmentMethod | Int | 否 | 否 |

### <a name="transaction-table"></a>交易记录表

通过分配交易表编号 (`TransTableId`)，成本交易记录与成本区域关联。 当需要特定表标识号时，将基于这些值拆分实体，以便每个成本区域都存在实体。

在选择成本交易实体时，交易表 (`TransTableId`) 的值是隐式值。

### <a name="calculated-fields"></a>计算字段

使用成本交易实体时，无法插入或更新以下字段，因为仅在针对航行记录执行特定操作时才设置这些字段：

- **估计成本** - 在为航行（采购订单）过帐发票或接收转移时设置此字段。
- **估计成本货币** - 在为航行（采购订单）过帐发票或接收转移时设置此字段。
- **实际成本** - 在过帐供应商发票时设置此字段。 它与成本关联。

### <a name="find-auto-costs"></a>查找自动成本

适用于每个成本区域（航行、装运集装箱等）的 **查找自动成本** 按钮提供了一种从配置表中的信息更新该成本区域的成本交易的方法。 当您选择成本区域的按钮时，系统将清除该成本区域的现有成本，并根据自动成本设置表的当前配置创建新记录。

使用数据实体创建的成本交易记录标记为已导入。 当您选择 **查找自动成本** 时，将不会删除这些记录，因为不会从自动成本设置表中重新创建这些记录。 但是，仍可以删除标记为已导入的成本交易记录。

### <a name="linked-fields"></a>链接的字段

每个成本交易都可以与同一成本区域中的另一个记录关联。 此关联是通过 **链接的成本类型** 字段建立的。 它允许将成本值计算为其他成本的百分比。

仅当首先处理所引用的记录或者该字段已存在于表中时，才能验证 **链接的成本类型** 字段。 这一相同要求适用于仅用于装运集装箱成本区域中的成本的 **链接支线** 字段。
