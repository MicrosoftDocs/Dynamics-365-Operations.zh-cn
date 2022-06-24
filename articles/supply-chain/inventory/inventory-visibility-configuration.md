---
title: 配置 Inventory Visibility
description: 本文介绍如何配置库存可见性。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2bdb2ca0067ea430b249ac619a38c8bcec75f2f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895806"
---
# <a name="configure-inventory-visibility"></a>配置 Inventory Visibility

[!include [banner](../includes/banner.md)]


本文介绍如何在 Power Apps 中使用库存可见性应用配置库存可见性。

## <a name="introduction"></a><a name="introduction"></a>简介

首先必须按照本文中的说明完成以下配置，才能开始使用库存可见性：

- [数据源配置](#data-source-configuration)
- [分区配置](#partition-configuration)
- [产品索引层次结构配置](#index-configuration)
- [预留配置（可选）](#reservation-configuration)
- [默认配置示例](#default-configuration-sample)

## <a name="prerequisites"></a>先决条件

首先，按照[安装和设置库存可见性](inventory-visibility-setup.md)中的说明安装并设置库存可见性加载项。

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>库存可见性应用的“配置”页面

在 Power Apps 中，[库存可见性应用](inventory-visibility-power-platform.md)的 **配置** 页面可帮助您设置现有库存配置和软预留配置。 安装此加载项后，默认配置中将包含来自 Microsoft Dynamics 365 Supply Chain Management（`fno` 数据源）的值。 可以查看默认设置。 此外，可根据您的业务要求和外部系统的库存过帐要求修改配置，以便标准化跨多个系统过帐，组织和查询库存更改的方法。 本文的其余几节介绍如何使用 **配置** 页面的各部分。

配置完成后，请务必在应用中选择 **更新配置**。

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>在 Power Apps 功能管理中启用库存可见性功能

库存可见性加载项将为您的 Power Apps 安装增加多项新功能。 默认情况下，这些功能处于关闭状态。 要使用它们，打开 **配置** 页，然后根据需要在 **功能管理** 选项卡上开启以下功能。

| 功能管理名称 | Description |
|---|---|
| *OnHandReservation* | 使用此功能，您可以使用库存可见性创建预留、使用预留和/或取消预留指定的库存数量。 有关详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。 |
| *OnHandMostSpecificBackgroundService* | 此功能提供产品的库存汇总以及所有维度。 将定期从库存可见性同步库存汇总数据。 有关详细信息，请参阅[库存汇总](inventory-visibility-power-platform.md#inventory-summary)。 |
| *OnhandChangeSchedule* | 此可选功能支持现有库存更改计划和可承诺 (ATP) 功能。 有关详细信息，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md)。 |
| *分配* | 此可选功能使库存可见性能够进行库存保护（圈护）和超额销售控制。 有关详细信息，请参阅[库存可见性库存分配](inventory-visibility-allocation.md)。 |
| *在库存可见性中启用仓库物料* | 此可选功能使库存可见性能够支持启用了高级仓库流程的物料（WHS 物料）。 有关详细信息，请参阅 [WHS 物料的库存可见性支持](inventory-visibility-whs-support.md)。 |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>查找服务终结点

如果不知道正确的库存可见性服务终结点，请在 Power Apps 中打开 **配置** 页，然后在右上角选择 **显示服务终结点**。 页面将显示正确的服务终结点。

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>数据源配置

各数据源表示您的数据的来源系统。 示例数据源名称包括 `fno`（代表“Dynamics 365 财务和运营应用”）和 `pos`（代表“销售点”）。 默认情况下，Supply Chain Management 在库存可见性中设置为默认数据源 (`fno`)。

> [!NOTE]
> `fno` 数据源是为 Supply Chain Management 预留的。 如果您的库存可见性加载项与 Supply Chain Management 环境集成，我们建议您不要删除数据源中与 `fno` 相关的配置。

若要添加数据源，请按以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上，选择 **新建数据源** 以添加数据源。

> [!NOTE]
> 添加数据源时，请务必先验证数据源名称、实际度量和维度映射，然后再更新库存可见性服务的配置。 选择 **更新配置** 之后，不能修改这些设置。

数据源配置包括以下部分：

- 维度（维度映射）
- 实际度量
- 计算度量

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>维度（维度映射）

维度配置的目的是根据维度组合标准化用于发布事件和查询的多系统集成。 库存可见性提供可从数据源的维度映射的基础维度的列表。 三十三个维度可供映射。

- 默认情况下，如果将 Supply Chain Management 用作一个数据源，将把 13 个维度映射到 Supply Chain Management 标准维度。 其他十二个维度（`inventDimension1` 到 `inventDimension12`）映射到 Supply Chain Management 中的自定义维度。 其余八个维度是可映射到外部数据源的扩展维度。
- 如果不将 Supply Chain Management 用作一个数据源，则可以自由映射维度。 下表显示可用维度的完整列表。

> [!NOTE]
> 如果默认维度列表中无您的维度，而您正在使用外部数据源，建议您使用 `ExtendedDimension1` 到 `ExtendedDimension8` 执行映射。

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
| 扩展 | `ExtendedDimension1` 到 `ExtendedDimension8` |
| System | `Empty` |

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

若要添加维度映射，请执行以下步骤。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上的 **维度映射** 部分中，选择 **添加** 添加维度映射。
    ![添加维度映射](media/inventory-visibility-dimension-mapping.png "添加维度映射")

1. 在 **维度名称** 字段中，指定源维度。
1. 在 **目标基础维度** 字段中，选择库存可见性中要映射的维度。
1. 选择 **保存**。

例如，如果您的数据源中包含产品颜色维度，则可以将其映射到 `ColorId` 基础维度，以便在 `exterchannel` 数据源中添加一个 `ProductColor` 自定义维度。 然后将其映射到 `ColorId` 基础维度。

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>实际度量

当数据源将库存更改发布到库存可见性时，它将使用 *实际度量* 发布该更改。 实际度量用于修改数量和反映库存状态。 可以根据要求定义自己的实际度量。 查询可以基于实际度量。

库存可见性提供一列链接到 Supply Chain Management（`fno` 数据源）的默认实际度量。 这些默认实际度量取自 Supply Chain Management 的 **现有库存列表** 页（**库存管理 \> 查询和报表 \> 现有库存列表**）中的库存交易记录状态。 下表提供实际度量的示例。

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

如果数据源为 Supply Chain Management，则不必重新创建默认实际度量。 但是，对于外部数据源，您可以通过执行以下步骤创建新的实际度量。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡的 **实际度量** 部分中，选择 **添加**，指定源度量名称，然后保存更改。

### <a name="calculated-measures"></a>计算度量

可以使用库存可见性对库存实际度量和 *自定义计算度量* 进行查询。 计算度量提供由实际度量组合构成的自定义计算公式。 该功能允许您定义一组将添加的实际度量，和/或一组将减去的实际度量，以便形成自定义度量。

> [!IMPORTANT]
> 计算的度量是实际度量的构成部分。 其公式只能包含不重复的实际度量，而不能包含计算的度量。

通过此配置，可以定义一组添加或减去的修饰符，以获取聚合输出数量总值。

若要设置自定义计算度量，请执行以下步骤。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **计算度量** 选项卡上，选择 **新建计算度量** 以添加计算度量。
1. 为新的计算度量值设置以下字段：

    - **新建计算度量值名称** – 输入计算度量值的名称。
    - **数据源** – 选择与新修饰符关联的数据源。 查询系统是数据源。

1. 选择 **添加** 将修饰符添加到新计算度量值。
1. 为新修饰符设置以下字段：

    - **修饰符** – 选择修饰符类型（*加* 或 *减*）。
    - **数据源** – 选择应在其中找到提供修饰符值的度量值的数据源。
    - **度量值** – 选择为修饰符提供值的度量值（从所选数据源）的名称。

1. 重复步骤 5 到 6，直到您添加了所有必需的修饰符。
1. 选择 **保存**。

例如，您可能具有以下查询结果。

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

`MyCustomAvailableforReservation` 输出基于自定义度量中的计算设置，为 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220。

## <a name="partition-configuration"></a><a name="partition-configuration"></a>分区配置

当前，分区配置由两个基本维度（`SiteId` 和 `LocationId`）组成，这两个维度指示数据的分配方式。 同一分区下的操作可以以更低的成本提供更高的性能。 下表显示了库存可见性加载项提供的默认分区配置。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

默认情况下，该解决方案包括此分区配置。 因此，*您不必亲自定义它*。

> [!IMPORTANT]
> 不自定义默认分区配置。 如果删除或更改它，则可能会导致意外错误。

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>产品索引层次结构配置

大多数时间，现有库存查询不会仅处于最高的“总计”级别。 相反，您还可能希望查看基于库存维度聚合的结果。

库存可见性通过允许您设置 _索引_ 来实现灵活性。 这些索引基于维度或维度的组合。 索引由 *集号*、*维度* 和 *层次结构* 构成，如下表中的定义。

| 姓名 | 说明 |
|---|---|
| 集号 | 属于同一集合（索引）的维度将组合在一起，并为其分配同一个集号。 |
| 维度 | 查询结果所聚合的基础维度。 |
| 层次结构 | 层次结构用于定义可查询的受支持维度组合。 例如，设置具有 `(ColorId, SizeId, StyleId)` 层次结构序列的维度集。 在此情况下，系统支持对四个维度组合进行查询。 第一个组合为空，第二个为 `(ColorId)`，第三个为 `(ColorId, SizeId)`，第四个为 `(ColorId, SizeId, StyleId)`。 不支持其他组合。 有关详细信息，请参阅以下示例。 |

若要设置产品层次结构索引，请按照以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **产品层次结构索引** 选项卡上的 **维度映射** 部分中，选择 **添加** 添加维度映射。
1. 默认情况下，将提供一列索引。 若要修改现有索引，请在相关索引的部分中进行 **编辑** 或 **添加**。 若要创建新索引集，请选择 **新建索引集**。 对于每个索引集中的每个行，在 **维度** 字段中，从基础维度列表中选择。 将自动生成以下字段的值：

    - **集号** – 属于同一组（索引）的维度将组合在一起，并为其分配同一个集号。
    - **层次结构** – 层次结构用于定义可在维度组（索引）中查询的受支持维度组合。 例如，如果设置的维度值具有层次结构序列 *样式*、*颜色* 和 *大小*，则系统支持三查询组结果。 第一个组为仅样式。 第二个组为样式和颜色的组合。 而第三个组为样式、颜色和大小的组合。 不支持其他组合。

> [!TIP]
> 以下是在设置索引层次结构时要注意的一些提示：
>
> - 不应在索引配置中定义在分区配置中定义的基础维度。 如果在索引配置中再次定义基础维度，您将无法按此索引进行查询。
> - 如果只需要查询由所有维度组合聚合的库存，则应设置包含基础维度 `Empty` 的单个索引。
> - 您必须至少有一个索引层次结构（例如，包含基础维度 `Empty`），否则查询将失败，显示错误“尚未设置索引层次结构”。

### <a name="example"></a>示例

此部分提供示例显示层次结构的工作方式。

下表提供此示例的可用库存列表。

| 物料 | ColorId | SizeId | StyleId | 数量 |
|---|---|---|---|---|
| T 恤杉 | 黑色 | 小 | 宽 | 1 |
| T 恤杉 | 黑色 | 小 | 常规 | 2 |
| T 恤杉 | 黑色 | 大 | 宽 | 3 |
| T 恤杉 | 黑色 | 大 | 常规 | 4 |
| T 恤杉 | 红色 | 小 | 宽 | 5 |
| T 恤杉 | 红色 | 小 | 常规 | 6 |
| T 恤杉 | 红色 | 大 | 常规 | 7 |

下表显示如何设置索引层次结构。

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

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>预留配置（可选）

如果要使用软预留功能，则需要预留配置。 该配置由两个基本部分构成：

- 软预留映射
- 软预留层次结构

### <a name="soft-reservation-mapping"></a>软预留映射

进行预留时，可能希望了解现有库存当前是否可用于预留。 验证将链接到计算度量，计算度量表示实际度量组合的计算公式。

通过设置从实际度量到计算度量的映射，可以启用库存可见性服务，以根据实际度量自动验证预留可用性。

在设置此映射之前，必须在 Power Apps 中的 **配置** 页 **数据源** 和 **计算度量** 选项卡上定义实际度量、计算度量和数据源（如本文前面所述）。

若要定义软预留映射，请按照以下步骤操作。

1. 定义用作软预留度量的实际度量（例如 `SoftReservOrdered`）。
1. 在 **配置** 页的 **计算度量** 选项卡上，定义其中包含要映射到实际度量的计算公式的 *可预留* (AFR) 计算度量。 例如，可设置 `AvailableToReserve`（可预留），以使其映射到之前定义的 `SoftReservOrdered` 实际度量。 这样就可以发现哪些具有 `SoftReservOrdered` 库存状态的数量可预留。 下表显示 AFR 计算公式。

    | 计算类型 | 数据源 | 实际度量 |
    |---|---|---|
    | 增加额 | `fno` | `AvailPhysical` |
    | 增加额 | `pos` | `Inbound` |
    | 减 | `pos` | `Outbound` |
    | 减 | `iv` | `SoftReservOrdered` |

    我们建议您设置计算度量，以使其包含预留度量所基于的实际度量。 这样，计算度量数量将受预留度量数量的影响。 因此，在此示例中，`iv` 数据源的 `AvailableToReserve` 计算度量应包含来自 `iv` 且形式为组件的  `SoftReservOrdered` 实际度量。

1. 打开 **管理** 页面。
1. 在 **软预留映射** 选项卡上，设置从实际度量到计算度量的映射。 对于上一个示例，可以使用以下设置将 `AvailableToReserve` 映射到之前定义的 `SoftReservOrdered` 实际度量。

    | 实际度量数据源 | 实际度量 | 可预留数据源 | 可预留计算度量 |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > 如果不能编辑 **软预留映射** 选项卡，可能需要在 **功能管理** 选项卡上开启 *OnHandReservation* 功能。

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

> [!NOTE]
> 调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值为 `True` 表示需要验证，而值为 `False` 则表示不需要验证。 默认值为 `True`。

### <a name="soft-reservation-hierarchy"></a>软预留层次结构

预留层次结构描述在进行预留时必须指定的维度的序列。 其工作方式与产品索引层次结构处理现有库存查询的工作方式相同。

预留层次结构与产品索引层次结构无关。 此独立性让您可以实施类别管理，从而让用户可以将维度细分为详细信息，以便指定有关进行更精确预留的要求。 软预留层次结构中应包含组件形式的 `SiteId` 和 `LocationId`，因为其构造分区配置。 当您进行预留时，必须为产品指定分区。

下面是软预留层次结构的示例。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

在此示例中，可以按以下维度序列执行预留。 当您进行预留时，必须为产品指定分区。 因此，您可以使用的基本层次结构为 `(SiteId, LocationId)`。

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

有效维度序列应逐个维度严格遵循预留层次结构。 例如，层次结构序列 `(SiteId, LocationId, SizeId)` 无效，因为缺少 `ColorId`。

## <a name="available-to-promise-configuration-optional"></a>可承诺配置（可选）

您可以设置库存可见性，以可以计划将来的现有库存更改并计算可承诺 (ATP) 数量。 ATP 是可用的并且可以在下一个期间向客户承诺的物料数量。 使用此计算可以大大提高您的订单履行能力。 要使用此功能，您必须在 **功能管理** 选项卡上启用它，然后在 **ATP 设置** 选项卡上进行设置。有关详细信息，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md)。

## <a name="complete-and-update-the-configuration"></a>完成和更新配置

完成配置后，必须将所有更改提交给库存可见性。 若要提交更改，请在 Power Apps 的 **配置** 页右上角中选择 **更新配置**。

首次选择 **更新配置** 时，系统会请求您的凭据。

- **客户端 ID** – 您为库存可见性创建的 Azure 应用程序 ID。
- **租户 ID** – 您的 Azure 租户 ID。
- **客户端密钥** – 您为库存可见性创建的 Azure 应用程序密钥。

登录后，库存可见性服务中将更新配置。

> [!NOTE]
> 请务必先验证数据源名称、实际度量和维度映射，然后再更新库存可见性服务的配置。 选择 **更新配置** 之后，不能修改这些设置。

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>默认配置示例

在其初始化阶段，库存可见性将设置默认配置；后文将详细介绍。 可以根据需要修改此配置。

### <a name="data-source-configuration"></a>数据源配置

#### <a name="configuration-of-the-iv-data-source"></a>iv 数据源的配置

此部分介绍如何配置 `iv` 数据源。

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>为“iv”数据源配置的实际度量

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
| 附加内容 | `fno` | `ReservPhysical` |
| 附加内容 | `fno` | `ReservOrdered` |
| 附加内容 | `iv` | `ReservPhysical` |
| 附加内容 | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>“fno”数据源的配置

此部分介绍如何配置 `fno` 数据源。

##### <a name="dimension-mappings-for-the-fno-data-source"></a>“fno”数据源的维度映射

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>为“fno”数据源配置的实际度量

将为 `fno` 数据源配置以下实际度量：

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>“pos”数据源的配置

此部分介绍如何配置数据源 `pos`。

##### <a name="physical-measures-for-the-pos-data-source"></a>“pos”数据源的实际度量

将为 `pos` 数据源配置以下实际度量：

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity 计算度量

将为 `pos` 数据源配置 `AvailQuantity` 计算度量，如下表中所示。

| 计算类型 | 数据源 | 实际度量 |
|---|---|---|
| 附加内容 | `fno` | `AvailPhysical` |
| 附加内容 | `pos` | `PosInbound` |
| 减 | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>“iom”数据源的配置

将为 `iom` (Intelligent Order Management) 数据源配置以下实际度量：

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>“erp”数据源的配置

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
