---
title: 库存可见性配置
description: 本主题介绍如何配置库存可见性。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345025"
---
# <a name="inventory-visibility-configuration"></a>库存可见性配置

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

本主题介绍如何配置库存可见性。

## <a name="introduction"></a><a name="introduction"></a>简介

首先必须按照本主题中的说明完成以下配置，才能开始使用库存可见性：

- [数据源配置](#data-source-configuration)
- [分区配置](#partition-configuration)
- [产品索引层次结构配置](#index-configuration)
- [预留配置（可选）](#reservation-configuration)
- [默认配置示例](#default-configuration-sample)

> [!NOTE]
> 可以在 [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration) 中查看和编辑库存可见性配置。 配置完成后，请在应用中选择 **更新配置**。

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>数据源配置

数据源表示您的数据的来源系统。 例如，`fno`（代表“Dynamics 365 Finance and Operations”应用）和 `pos`（代表“销售点”）。

数据源配置包括以下部分：

- 维度（维度映射）
- 实际度量
- 计算度量

> [!NOTE]
> `fno` 数据源是为 Dynamics 365 Supply Chain Management 保留的。

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>维度（维度映射）

维度配置的目的是根据维度组合标准化用于发布事件和查询的多系统集成。

库存可见性支持以下常规基础维度。

| 维度类型 | 基础维度 |
|---|---|
| 产品 | `ColorId` |
| 产品 | `SizeId` |
| 产品 | `StyleId` |
| 产品 | `ConfigId` |
| 跟踪 | `BatchId` |
| 跟踪 | `SerialId` |
| 库位 | `LocationId` |
| 库位 | `SiteId` |
| 库存状态 | `StatusId` |
| 仓库特定 | `WMSLocationId` |
| 仓库特定 | `WMSPalletId` |
| 仓库特定 | `LicensePlateId` |
| 其他 | `VersionId` |
| 库存（自定义） | `InventDimension1` 到 `InventDimension12` |
| 函授 | `ExtendedDimension1` 到 `ExtendedDimension8` |

> [!NOTE]
> 上表中列出的维度类型仅供参考。 不必在库存可见性中定义它们。
>
> 可以为 Supply Chain Management 预留库存（自定义）维度。 在此情况下，可以改用扩展维度。

外部系统可以通过其 RESTful API 访问库存可见性。 对于集成，库存可见性允许您配置 _外部数据源_，以及从 _外部维度_ 映射到 _基础维度_。 下面是维度映射表的示例。

| 外部维度 | 基础维度 |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

可通过配置维度映射将外部维度直接发送到库存可见性。 然后，库存可见性将自动把外部维度转换为基础维度。

### <a name="physical-measures"></a>实际度量

实际度量用于修改数量和反映库存状态。 可以根据要求定义自己的实际度量。

库存可见性提供一列链接到 Supply Chain Management（`fno` 数据源）的默认实际度量。 下表提供实际度量的示例。

| 实际度量名称 | 说明 |
|---|---|
| `NotSpecified` | 未指定 |
| `Arrived` | 已到达 |
| `AvailOrdered` | 已订购可用 |
| `AvailPhysical` | 实际可用 |
| `Deducted` | 已扣除 |
| `OnOrder` | OnOrder |
| `Ordered` | 订购时间 |
| `PhysicalInvent` | 实际库存 |
| `Picked` | 已领料 |
| `PostedQty` | 已过帐的数量 |
| `QuotationIssue` | 报价发出量 |
| `QuotationReceipt` | 报价收据 |
| `Received` | 已收到 |
| `Registered` | 已登记 |
| `ReservOrdered` | 订单预留 |
| `ReservPhysical` | 实际预留 |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>计算度量

计算度量提供由实际度量组合构成的自定义计算公式。 该功能允许您定义一组将添加的实际度量，和/或一组将减去的实际度量，以便形成自定义度量。

例如，您具有以下查询结果。

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

然后配置一个名称为 `MyCustomAvailableforReservation` 的计算度量，如下表中所示。 消耗系统将使用此计算度量。

| 消耗系统 | 计算度量 | 数据源 | 实际度量 | 计算类型 |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

使用此计算公式时，新查询结果中将包括自定义度量。

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` 输出基于自定义度量中的计算设置，为 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220。

## <a name="partition-configuration"></a><a name="partition-configuration"></a>分区配置

分区配置由基础维度组合构成。 其定义数据分发模式。 同一分区中的数据操作支持高性能，并且成本不高。 因此，良好的分区模式拥有显著的优点。

库存可见性提供以下默认分区配置。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> 默认分区配置仅供参考。 不必在库存可见性中定义。 现在不支持分区配置升级。

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>产品索引层次结构配置

大多数时间，现有库存查询不会仅处于最高的“总计”级别。 相反，您还可能希望查看基于库存维度聚合的结果。

库存可见性通过允许您设置 _索引_ 来实现灵活性。 这些索引基于维度或维度的组合。 索引由 *集号*、*维度* 和 *层次结构* 构成，如下表中的定义。

| 姓名 | 说明 |
|---|---|
| 集号 | 属于同一集合（索引）的维度将组合在一起，并为其分配同一个集号。 |
| 维度 | 查询结果所聚合的基础维度。 |
| 层次结构 | 层次结构用于定义可查询的受支持维度组合。 例如，设置具有 `(ColorId, SizeId, StyleId)` 层次结构序列的维度集。 在此情况下，系统支持对四个维度组合进行查询。 第一个组合为空，第二个为 `(ColorId)`，第三个为 `(ColorId, SizeId)`，第四个为 `(ColorId, SizeId, StyleId)`。 不支持其他组合。 有关详细信息，请参阅以下示例。 |

### <a name="example"></a>示例

此部分提供示例显示层次结构的工作方式。

您的库存中有以下项。

| 物料 | ColorId | SizeId | StyleId | 数量 |
|---|---|---|---|---|
| T 恤杉 | 黑色 | 小 | 宽 | 1 |
| T 恤杉 | 黑色 | 小 | 常规 | 2 |
| T 恤杉 | 黑色 | 大 | 宽 | 3 |
| T 恤杉 | 黑色 | 大 | 常规 | 4 |
| T 恤杉 | 红色 | 小 | 宽 | 5 |
| T 恤杉 | 红色 | 小 | 常规 | 6 |
| T 恤杉 | 红色 | 大 | 常规 | 7 |

下面是索引。

| 集号 | 维度 | 层次结构 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

该索引允许您以下面的方式查询现有库存：

- `()` – 按全部分组

    - T 恤杉，28

- `(ColorId)` – 按 `ColorId` 分组

    - T 恤杉，黑色，10
    - T 恤杉，红色，18

- `(ColorId, SizeId)` – 按 `ColorId` 和 `SizeId` 的组合分组

    - T 恤杉，黑色，小，3
    - T 恤杉，黑色，大，7
    - T 恤杉，红色，小，11
    - T 恤杉，红色，大，7

- `(ColorId, SizeId, StyleId)` – 按 `ColorId`、`SizeId` 和 `StyleId` 的组合分组

    - T 恤杉，黑色，小，宽，1
    - T 恤杉，黑色，小，正常，2
    - T 恤杉，黑色，大，宽，3
    - T 恤杉，黑色，大，正常，4
    - T 恤杉，红色，小，宽，5
    - T 恤杉，红色，小，正常，6
    - T 恤杉，红色，大，正常，7

> [!NOTE]
> 不应在索引配置中定义在分区配置中定义的基础维度。

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>预留配置（可选）

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

如果要使用软预留功能，则需要预留配置。 该配置由两个基本部分构成：

- 软预留映射
- 软预留层次结构

### <a name="soft-reservation-mapping"></a>软预留映射

进行预留时，可能希望了解现有库存当前是否可用于预留。 验证将链接到计算度量，计算度量表示实际度量组合的计算公式。

例如，预留度量基于来自 `iv`（库存可见性）数据源的 `SoftReservOrdered` 实际度量。 在此情况下，可设置 `iv` 数据源的 `AvailableToReserve` 计算度量，如此处所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `AvailPhysical` |
| 增加额 | `pos` | `Inbound` |
| 减 | `pos` | `Outbound` |
| 减 | `iv` | `SoftReservOrdered` |

然后设置软预留映射，以提供从 `SoftReservOrdered` 预留度量到 `AvailableToReserve` 计算度量的映射。

| 实际度量数据源 | 实际度量 | 可预留数据源 | 可预留计算度量 |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

现在，在 `SoftReservOrdered` 中进行预留时，库存可见性将自动查找 `AvailableToReserve` 及其相关计算公式以执行预留验证。

例如，您在库存可见性中具有以下现有库存。

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

在此示例中，将采用以下计算：

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

因此，如果尝试对 `iv.SoftReservOrdered` 进行预留，并且数量小于或等于 `AvailableToReserve` (10)，则可进行预留。

### <a name="soft-reservation-hierarchy"></a>软预留层次结构

预留层次结构描述在进行预留时必须指定的维度的序列。 其工作方式与产品索引层次结构处理现有库存查询的工作方式相同。

预留层次结构与产品索引层次结构无关。 此独立性让您可以实施类别管理，从而让用户可以将维度细分为详细信息，以便指定有关进行更精确预留的要求。

下面是软预留层次结构的示例。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

在此示例中，可以按以下维度序列执行预留：

- `()` – 不指定任何维度。
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

有效维度序列应逐个维度严格遵循预留层次结构。 例如，层次结构序列 `(SiteId, LocationId, SizeId)` 无效，因为缺少 `ColorId`。

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>默认配置示例

在其初始化阶段，库存可见性将设置默认配置。 可以根据需要修改配置。

### <a name="data-source-configuration"></a>数据源配置

#### <a name="configuration-of-the-iv-data-source"></a>iv 数据源的配置

此部分介绍如何配置 `iv` 数据源。

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>为 iv 数据源配置的实际度量

将为 `iv` 数据源配置以下实际度量：

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal 计算度量

将为 `iv` 数据源配置 `OrderedTotal` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `Ordered` |
| 增加额 | `fno` | `Arrived` |
| 增加额 | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>现有库存计算度量

将为 `iv` 数据源配置 `OnHand` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `PhysicalInvent` |
| 增加额 | `iom` | `OnHand` |
| 增加额 | `erp` | `Unrestricted` |
| 增加额 | `erp` | `QualityInspection` |
| 增加额 | `pos` | `PosInbound` |
| 减 | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReservedTotal 计算度量

将为 `iv` 数据源配置 `ReservedTotal` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `ReservPhysical` |
| 增加额 | `fno` | `ReservOrdered` |
| 增加额 | `iv` | `SoftReservPhysical` |
| 增加额 | `iv` | `SoftReservOrdered` |
| 增加额 | `iv` | `ReservPhysical` |
| 增加额 | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved 计算度量

将为 `iv` 数据源配置 `SoftReserved` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `iv` | `SoftReservPhysical` |
| 增加额 | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved 计算度量

将为 `iv` 数据源配置 `HardReserved` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `ReservPhysical` |
| 增加额 | `fno` | `ReservOrdered` |
| 增加额 | `iv` | `ReservPhysical` |
| 增加额 | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder 计算度量

将为 `iv` 数据源配置 `OpenOrder` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `OnOrder` |
| 增加额 | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable 计算度量

将为 `iv` 数据源配置 `OnHandAvailable` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `PhysicalInvent` |
| 增加额 | `iom` | `OnHand` |
| 增加额 | `erp` | `Unrestricted` |
| 增加额 | `erp` | `QualityInspection` |
| 增加额 | `pos` | `PosInbound` |
| 减 | `fno` | `ReservPhysical` |
| 减 | `iv` | `SoftReservPhysical` |
| 减 | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve 计算度量

将为 `iv` 数据源配置 `AvailableToReserve` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `PhysicalInvent` |
| 增加额 | `iom` | `OnHand` |
| 增加额 | `erp` | `Unrestricted` |
| 增加额 | `erp` | `QualityInspection` |
| 增加额 | `pos` | `PosInbound` |
| 增加额 | `fno` | `Ordered` |
| 增加额 | `fno` | `Arrived` |
| 增加额 | `iv` | `Ordered` |
| 减 | `fno` | `ReservPhysical` |
| 减 | `fno` | `ReservOrdered` |
| 减 | `iv` | `SoftReservPhysical` |
| 减 | `iv` | `SoftReservOrdered` |
| 减 | `iv` | `ReservPhysical` |
| 减 | `iv` | `ReservOrdered` |
| 减 | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply 计算度量

将为 `iv` 数据源配置 `InventorySupply` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `Ordered` |
| 增加额 | `fno` | `Arrived` |
| 增加额 | `iv` | `Ordered` |
| 增加额 | `fno` | `PhysicalInvent` |
| 增加额 | `iom` | `OnHand` |
| 增加额 | `erp` | `Unrestricted` |
| 增加额 | `erp` | `QualityInspection` |
| 增加额 | `pos` | `PosInbound` |
| 减 | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand 计算度量

将为 `iv` 数据源配置 `InventoryDemand` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `OnOrder` |
| 增加额 | `iom` | `OnOrder` |
| 增加额 | `iv` | `SoftReservPhysical` |
| 增加额 | `iv` | `SoftReservOrdered` |
| 增加额 | `fno` | `ReservPhysical` |
| 增加额 | `fno` | `ReservOrdered` |
| 增加额 | `iv` | `ReservPhysical` |
| 增加额 | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>fno 数据源的配置

此部分介绍如何配置 `fno` 数据源。

##### <a name="dimension-mappings-for-the-fno-data-source"></a>fno 数据源的维度映射

将为 `fno` 数据源配置下表中列出的维度映射。

| 外部维度 | 基础维度 |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>为 fno 数据源配置的实际度量

将为 `fno` 数据源配置以下实际度量：

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>pos 数据源的配置

此部分介绍如何配置数据源 `pos`。

##### <a name="physical-measures-for-the-pos-data-source"></a>pos 数据源的实际度量

将为 `pos` 数据源配置以下实际度量：

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity 计算度量

将为 `pos` 数据源配置 `AvailQuantity` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 增加额 | `fno` | `AvailPhysical` |
| 增加额 | `pos` | `PosInbound` |
| 减 | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>iom 数据源的配置

将为 `iom` (Intelligent Order Management) 数据源配置以下实际度量：

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>erp 数据源的配置

将为 `erp`（企业资源规划）数据源配置以下实际度量：

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>分区配置

下表显示默认分区配置。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>索引配置

下表显示默认索引配置。

| 集号 | 维度 | 层次结构 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>预留配置

此部分介绍默认预留配置。

#### <a name="reservation-mapping"></a>预留映射

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

下表显示默认预留映射。

| 实际度量数据源 | 实际度量 | 可预留数据源 | 可预留计算度量 |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>预留层次结构

下表显示默认预留层次结构。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
