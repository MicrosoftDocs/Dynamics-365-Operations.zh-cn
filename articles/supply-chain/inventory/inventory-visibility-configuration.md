---
title: 配置 Inventory Visibility
description: 本文介绍如何配置库存可见性。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850015"
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
- [查询预加载配置（可选）](#query-preload-configuration)
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
| *OnHandMostSpecificBackgroundService* | 此功能提供产品的库存汇总以及所有维度。 将定期从库存可见性同步库存汇总数据。 默认同步频率为每 15 分钟一次，最高可设置为每 5 分钟一次。 有关详细信息，请参阅[库存汇总](inventory-visibility-power-platform.md#inventory-summary)。 |
| *OnHandIndexQueryPreloadBackgroundService* | 此功能会根据您预先配置的维度定期获取和存储一组现有库存摘要数据。 它提供的库存摘要仅包括与您的日常业务相关的维度，并且与为仓库管理流程 (WMS) 启用的项兼容。 有关详细信息，请参阅[打开和配置预加载的现有查询](#query-preload-configuration)和 [预加载简化的现有查询](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)。 |
| *OnhandChangeSchedule* | 此可选功能支持现有库存更改计划和可承诺 (ATP) 功能。 有关详细信息，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md)。 |
| *分配* | 此可选功能使库存可见性能够进行库存保护（圈护）和超额销售控制。 有关详细信息，请参阅[库存可见性库存分配](inventory-visibility-allocation.md)。 |
| *在库存可见性中启用仓库物料* | 此可选功能使库存可见性能够支持启用了仓库管理流程 (WMS)。 有关详细信息，请参阅 [WMS 物料的库存可见性支持](inventory-visibility-whs-support.md)。 |

> [!IMPORTANT]
> 我们建议您使用 *OnHandIndexQueryPreloadBackgroundService* 功能或 *OnHandMostSpecificBackgroundService* 功能，而不是同时使用这两种功能。 启用这两个功能将影响性能。

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>查找服务终结点

如果不知道正确的库存可见性服务终结点，请在 Power Apps 中打开 **配置** 页，然后在右上角选择 **显示服务详细信息**。 页面将显示正确的服务终结点。 您还可以在 Microsoft Dynamics Lifecycle Services 中查找终结点，如[根据 Lifecycle Services 环境查找终结点](inventory-visibility-api.md#endpoint-lcs)中所述。

> [!NOTE]
> 使用不正确的终结点可能会导致库存可见性安装失败，并会在 Supply Chain Management 与库存可见性同步时出现错误。 如果您不确定您的终结点是哪一个，请联系您的系统管理员。 终结点 URL 使用以下格式：
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>数据源配置

各数据源表示您的数据的来源系统。 示例数据源名称包括 `fno`（对应 Supply Chain Management）和 `pos`（代表“销售点”）。 默认情况下，Supply Chain Management 在库存可见性中设置为默认数据源 (`fno`)。

> [!NOTE]
> `fno` 数据源是为 Supply Chain Management 预留的。 如果您的库存可见性加载项与 Supply Chain Management 环境集成，我们建议您不要删除数据源中与 `fno` 相关的配置。

若要添加数据源，请按以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上，选择 **新建数据源** 添加数据源（例如，`ecommerce` 或另一个有意义的数据源 ID）。

> [!NOTE]
> 添加数据源时，请务必先验证数据源名称、实际度量和维度映射，然后再更新库存可见性服务的配置。 选择 **更新配置** 之后，不能修改这些设置。

数据源配置包括以下部分：

- 维度（维度映射）
- 实际度量
- 计算度量

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>维度（维度映射）

维度配置的目的是根据维度组合标准化用于发布事件和查询的多系统集成。 库存可见性提供可从数据源的维度映射的基础维度的列表。 三十三个维度可供映射。

- 如果将 Supply Chain Management 用作一个数据源，13 个维度会默认映射到 Supply Chain Management 标准维度。 其他 12 个维度（`inventDimension1` 到 `inventDimension12`）还会映射到 Supply Chain Management 中的自定义维度。 其余 8 个维度（`ExtendedDimension1` 到 `ExtendedDimension8`）是可映射到外部数据源的扩展维度。
- 如果不将 Supply Chain Management 用作一个数据源，则可以自由映射维度。 下表显示可用维度的完整列表。

> [!NOTE]
> 如果您使用 Supply Chain Management，当更改 Supply Chain Management 和库存可见性之间的默认维度映射时，更改后的维度不会同步数据。 因此，如果您的维度不在默认维度列表中，而您正在使用外部数据源，建议您使用 `ExtendedDimension1` 到 `ExtendedDimension8` 执行映射。

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
> 上表中列出的维度类型仅供您参考。 不必在库存可见性中定义它们。
>
> 可以为 Supply Chain Management 预留库存（自定义）维度。 在此情况下，改用扩展维度。

外部系统可以通过其 RESTful API 访问库存可见性。 对于集成，库存可见性允许您配置 *外部数据源*，以及从 *外部维度* 映射到 *基础维度*。 下面是维度映射表的示例。

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
1. 在 **数据源** 选项卡上，选择要进行维度映射的数据源。 然后，在 **维度映射** 部分，选择 **添加** 添加维度映射。

    ![添加维度映射](media/inventory-visibility-dimension-mapping.png "添加维度映射")

1. 在 **维度名称** 字段中，指定源维度。
1. 在 **目标基础维度** 字段中，选择库存可见性中要映射的维度。
1. 选择 **保存**。

例如，您已经创建了一个名为 `ecommerce` 的数据源，其包含一个产品颜色维度。 在这种情况下，要进行映射，您可以首先将 `ProductColor` 添加到 `ecommerce` 数据源中的 **维度名称** 字段中，然后在 **目标基础维度** 字段中选择 `ColorId`。

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>实际度量

当数据源将库存更改发布到库存可见性时，它将使用 *实际度量* 发布该更改。 实际度量用于修改数量和反映库存状态。 可以根据要求定义自己的实际度量。 查询可以基于实际度量。

库存可见性提供映射到 Supply Chain Management（`fno` 数据源）的默认实际度量的列表。 这些默认实际度量取自 Supply Chain Management 的 **现有库存列表** 页（**库存管理 \> 查询和报表 \> 现有库存列表**）中的库存交易记录状态。 下表提供实际度量的示例。

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
| `Received` | 已接收 |
| `Registered` | 已登记 |
| `ReservOrdered` | 订单预留 |
| `ReservPhysical` | 实际预留 |

如果您的数据源为 Supply Chain Management，则不必重新创建默认实际度量。 但是，对于外部数据源，您可以通过执行以下步骤创建新的实际度量。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上，选择要添加实际度量的数据源（例如，`ecommerce` 数据源）。 然后，在 **实际度量** 部分，选择 **添加**，指定度量名称（例如，如果要将此数据源中返回的数量记录到库存可见性中，则为 `Returned`）。 保存所做的更改。

### <a name="extended-dimensions"></a>扩展的维度

想要在数据源中使用外部数据源的客户可以通过为 `InventOnHandChangeEventDimensionSet` 和 `InventInventoryDataServiceBatchJobTask` 类创建[类扩展](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md)来利用 Dynamics 365 提供的可扩展性。

请务必在创建扩展后与数据库同步，以便将自定义字段添加到 `InventSum` 表中。 然后，您可以参考本文前面的“维度”部分，以将您的自定义维度映射到库存系统内 `BaseDimensions` 中八个扩展维度中的任意一个。

> [!NOTE] 
> 有关创建扩展的更多详细信息，请参阅[可扩展性主页](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)。

### <a name="calculated-measures"></a>计算度量

可以使用库存可见性对库存实际度量和 *自定义计算度量* 进行查询。 计算度量提供由实际度量组合构成的自定义计算公式。 该功能允许您定义一组将添加的实际度量，和/或一组将减去的实际度量，以便形成自定义度量。

> [!IMPORTANT]
> 计算的度量是实际度量的构成部分。 其公式只能包含不重复的实际度量，而不能包含计算的度量。

通过此配置，您可以定义一组计算度量公式，其中包括加法或减法的修饰符，来获取聚合输出数量总值。

若要设置自定义计算度量，请执行以下步骤。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **计算度量** 选项卡上，选择 **新建计算度量** 以添加计算度量。
1. 为新的计算度量值设置以下字段：

    - **新建计算度量值名称** – 输入计算度量值的名称。
    - **数据源** – 选择要包含新的计算度量的数据源。 查询系统是数据源。

1. 选择 **添加** 将修饰符添加到新计算度量值。
1. 为新修饰符设置以下字段：

    - **修饰符** – 选择修饰符类型（*加* 或 *减*）。
    - **数据源** – 选择应在其中找到提供修饰符值的度量值的数据源。
    - **度量值** – 选择为修饰符提供值的度量值（从所选数据源）的名称。

1. 重复步骤 5 到 6，直到您添加了所有必需的修饰符并完成了计算度量的公式。
1. 选择 **保存**。

例如，一家时装公司跨三个数据源运营：

- `pos` – 对应商店渠道。
- `fno` – 对应 Supply Chain Management。
- `ecommerce` – 对应您的 Web 渠道。

如果没有计算度量，当您在站点 1、仓库 11 和 `Red` 的 `ColorID` 维度值下查询产品 D0002（机柜）时，可能会得到以下查询结果，其中显示每个预配置的实际度量下的库存数量。 但是，您无法了解数据源中可用于预留的总数。

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

使用此计算公式时，新查询结果中将包括自定义度量。

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
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

库存可见性通过允许您设置 *索引* 来提高查询性能，从而提供灵活性。 这些索引基于维度或维度的组合。 索引由 *集号*、*维度* 和 *层次结构* 构成，如下表中的定义。

| 姓名 | 说明 |
|---|---|
| 集号 | 属于同一集合（索引）的维度将组合在一起，并为其分配同一个集号。 |
| 维度 | 查询结果所聚合的基础维度。 |
| 层次结构 | 层次结构可让您在用于筛选器和分组依据查询参数时提高特定维度组合的性能。 例如，如果您设置了一个层次结构序列为 `(ColorId, SizeId, StyleId)` 的维度集，那么系统可以更快地处理与四个维度组合相关的查询。 第一个组合为空，第二个为 `(ColorId)`，第三个为 `(ColorId, SizeId)`，第四个为 `(ColorId, SizeId, StyleId)`。 其他组合不会被加速。 筛选器不受顺序限制，但如果您想要提高其性能，筛选器必须在这些维度内。 有关详细信息，请参阅以下示例。 |

若要设置产品层次结构索引，请按照以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **产品层次结构索引** 选项卡上的 **维度映射** 部分中，选择 **添加** 添加维度映射。
1. 默认情况下，将提供一列索引。 若要修改现有索引，请在相关索引的部分中进行 **编辑** 或 **添加**。 若要创建新索引集，请选择 **新建索引集**。 对于每个索引集中的每个行，在 **维度** 字段中，从基础维度列表中选择。 将自动生成以下字段的值：

    - **集号** – 属于同一组（索引）的维度将组合在一起，并为其分配同一个集号。
    - **层次结构** – 层次结构可以在特定维度组合用于筛选器和分组依据查询参数时提高其性能。

> [!TIP]
> 以下是在设置索引层次结构时要注意的一些提示：
>
> - 不应在索引配置中定义在分区配置中定义的基础维度。 如果在索引配置中再次定义基础维度，您将无法按此索引进行查询。
> - 如果只需要查询由所有维度组合聚合的库存，则应设置包含基础维度 `Empty` 的单个索引。

### <a name="example"></a>示例

此部分提供示例显示层次结构的工作方式。

下表提供此示例的可用库存列表。

| 项目 | ColorId | SizeId | StyleId | Quantity |
|---|---|---|---|---|
| D0002 | 黑色 | 小 | 宽 | 1 |
| D0002 | 黑色 | 小 | 常规 | 2 |
| D0002 | 黑色 | 大 | 宽 | 3 |
| D0002 | 黑色 | 大 | 常规 | 4 |
| D0002 | 红色 | 小 | 宽 | 5 |
| D0002 | 红色 | 小 | 常规 | 6 |
| D0002 | 红色 | 大 | 常规 | 7 |

下表显示如何设置索引层次结构。

| 集号 | 维度 | 层次结构 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

该索引允许您以下面的方式查询现有库存：

- `()` – 按全部分组

    - D0002，28

- `(ColorId)` – 按 `ColorId` 分组

    - D0002，黑色，10
    - D0002，红色，18

- `(ColorId, SizeId)` – 按 `ColorId` 和 `SizeId` 的组合分组

    - D0002，黑色，小，3
    - D0002，黑色，大，7
    - D0002，红色，小，11
    - D0002，红色，大，7

- `(ColorId, SizeId, StyleId)` – 按 `ColorId`、`SizeId` 和 `StyleId` 的组合分组

    - D0002，黑色，小，宽，1
    - D0002，黑色，小，正常，2
    - D0002，黑色，大，宽，3
    - D0002，黑色，大，正常，4
    - D0002，红色，小，宽，5
    - D0002，红色，小，正常，6
    - D0002，红色，大，正常，7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>预留配置（可选）

如果要使用软预留功能，则需要预留配置。 该配置由两个基本部分构成：

- 软预留映射
- 软预留层次结构

### <a name="soft-reservation-mapping"></a>软预留映射

进行预留时，可能希望了解现有库存当前是否可用于预留。 验证将链接到计算度量，计算度量表示实际度量组合的计算公式。

通过设置从实际度量到计算度量的映射，可以启用库存可见性服务，以根据实际度量自动验证预留可用性。

在设置此映射之前，必须在 Power Apps 中的 **配置** 页 **数据源** 和 **计算度量** 选项卡上定义实际度量、计算度量和数据源（如本文前面所述）。

若要定义软预留映射，请按照以下步骤操作。

1. 定义用作软预留度量的实际度量（例如 `SoftReservPhysical`）。
1. 在 **配置** 页的 **计算度量** 选项卡上，定义其中包含要映射到实际度量的计算公式的 *可预留* (AFR) 计算度量。 例如，可设置 `AvailableToReserve`（可预留），以使其映射到之前定义的 `SoftReservPhysical` 实际度量。 这样就可以发现哪些具有 `SoftReservPhysical` 库存状态的数量可预留。 下表显示 AFR 计算公式。

    | 计算类型 | 数据源 | 实际度量 |
    |---|---|---|
    | 增加额 | `fno` | `AvailPhysical` |
    | 增加额 | `pos` | `Inbound` |
    | 减 | `pos` | `Outbound` |
    | 减 | `iv` | `SoftReservPhysical` |

    我们建议您设置计算度量，以使其包含预留度量所基于的实际度量。 这样，计算度量数量将受预留度量数量的影响。 因此，在此示例中，`iv` 数据源的 `AvailableToReserve` 计算度量应包含来自 `iv` 且形式为组件的  `SoftReservPhysical` 实际度量。

1. 打开 **管理** 页面。
1. 在 **软预留映射** 选项卡上，设置从实际度量到计算度量的映射。 对于上一个示例，可以使用以下设置将 `AvailableToReserve` 映射到之前定义的 `SoftReservPhysical` 实际度量。

    | 实际度量数据源 | 实际度量 | 可预留数据源 | 可预留计算度量 |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > 如果不能编辑 **软预留映射** 选项卡，可能需要在 **功能管理** 选项卡上开启 *OnHandReservation* 功能。

现在，在 `SoftReservPhysical` 中进行预留时，库存可见性将自动查找 `AvailableToReserve` 及其相关计算公式以执行预留验证。

例如，您在库存可见性中具有以下现有库存。

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

因此，如果尝试对 `iv.SoftReservPhysical` 进行预留，并且数量小于或等于 `AvailableToReserve` (10)，软预留请求将成功。

> [!NOTE]
> 调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值 `True` 意味着需要验证，而值 `False` 意味着不需要验证（虽然您最终可能会得到负 `AvailableToReserve` 数量，但系统仍会允许您进行软预留）。 默认值为 `True`。

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

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>打开并配置预加载的现有查询（可选）

库存可见性会根据您预先配置的维度定期获取和存储一组现有库存摘要数据。 这功能提供了以下优点：

- 一个更清晰的视图，用于存储仅包含与您的日常业务相关的维度的库存摘要。
- 与为仓库管理流程 (WMS) 启用的项兼容的库存摘要。

请参阅[预加载简化的现有库存查询](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)，了解有关如何在设置后使用此功能的更多信息。

> [!IMPORTANT]
> 我们建议您使用 *OnHandIndexQueryPreloadBackgroundService* 功能或 *OnHandMostSpecificBackgroundService* 功能，而不是同时使用这两种功能。 启用这两个功能将影响性能。

请按照以下步骤设置此功能：

1. 登录到库存可见性 Power App。
1. 转到 **配置 \> 功能管理和设置**。
1. 如果 *OnHandIndexQueryPreloadBackgroundService* 功能已启用，则我们建议您暂时关闭它，因为清理过程可能需要很长时间才能完成。 您将在此过程的后面再次打开它。
1. 打开 **预加载设置** 选项卡。
1. 在 **第 1 步：清理预加载存储** 部分，选择 **清理** 以清理数据库，并使其准备就绪以接受您的新分组依据设置。
1. 在 **第 2 步：设置分组依据值** 部分，在 **结果分组依据** 字段中，输入以逗号分隔的字段名称列表，您可以根据这些字段名称对查询结果进行分组。 一旦预加载存储数据库中有数据，您将无法更改此设置，直到您清理数据库为止，如上一步所述。
1. 转到 **配置 \> 功能管理和设置**。
1. 打开 *OnHandIndexQueryPreloadBackgroundService* 功能。
1. 在 **配置** 页右上角中选择 **更新配置** 以提交更改。

## <a name="complete-and-update-the-configuration"></a>完成和更新配置

完成配置后，必须将所有更改提交给库存可见性。 按照以下步骤提交更改。

1. 在 Power Apps 中，在 **配置** 页面上，选择右上角的 **更新配置**。 
1. 系统要求提供登录凭据。 输入以下值：

    - **客户端 ID** – 您为库存可见性创建的 Azure 应用程序 ID。
    - **租户 ID** – 您的 Azure 租户 ID。
    - **客户端密钥** – 您为库存可见性创建的 Azure 应用程序密钥。

    有关这些凭据以及如何查找凭据的更多信息，请参阅[安装和设置库存可见性](inventory-visibility-setup.md)。

    > [!IMPORTANT]
    > 务必先验证数据源名称、实际度量和维度映射，然后再更新配置。 更新后，您将无法修改这些设置。

1. 登录后，再次选择 **更新配置**。 系统将应用您的设置并显示更改的内容。

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

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

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
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>预留层次结构

下表显示默认预留层次结构。

| 基础维度 | 层次结构 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
