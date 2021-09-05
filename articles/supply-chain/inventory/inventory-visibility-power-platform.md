---
title: 库存可见性应用
description: 本主题介绍如何使用库存可见性应用。
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344994"
---
# <a name="inventory-visibility-app"></a>库存可见性应用

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

本主题介绍如何使用库存可见性应用。

库存可见性提供模型驱动应用以进行可视化。 此应用中包含三个页面：**配置**、**操作可见性** 和 **库存汇总**。 它具有以下功能：

- 为现有库存配置和软预留配置提供用户接口 (UI)。
- 支持对各种维度组合执行实时现有库存查询。
- 提供用于发布预留请求的 UI。
- 提供产品的现有库存与所有维度的自定义视图

## <a name="prerequisites"></a>先决条件

首先，按照[安装库存可见性](inventory-visibility-setup.md)中的说明安装并设置库存可见性加载项。

## <a name="configuration"></a><a name="configuration"></a>配置

**配置** 页面可帮助您设置现有库存配置和软预留配置。 安装此加载项后，默认配置中将包含来自 Microsoft Dynamics 365 Supply Chain Management（`fno` 数据源）的值。 可以查看默认设置。 此外，可根据您的业务要求和外部系统的库存过帐要求修改 [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) 中的配置，以便标准化跨多个系统过帐，组织和查询库存更改的方法。

### <a name="define-data-sources"></a>定义数据源

定义要与库存可见性集成的每个 *数据源*。 库存可见性支持与各种数据源（如销售点 (POS) 系统、Supply Chain Management 和其他外部系统）集成。 默认情况下，Supply Chain Management 在库存可见性中设置为默认数据源 (`fno`)。

若要添加数据源，请按以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上，选择 **新建数据源** 以添加数据源。

> [!NOTE]
> 添加数据源时，请务必先验证数据源名称、实际度量和维度映射，然后再更新库存可见性服务的配置。 选择 **更新配置** 之后，不能修改这些设置。

### <a name="set-up-dimension-mappings"></a>设置维度映射

库存可见性提供可从数据源的维度映射的基础维度的列表。 三十三个维度可供映射。

- 默认情况下，如果将 Supply Chain Management 用作一个数据源，将把 13 个维度映射到 Supply Chain Management 标准维度。 其他十二个维度（`inventDimension1` 到 `inventDimension12`）映射到 Supply Chain Management 中的自定义维度。 其余八个维度是可映射到外部数据源的扩展维度。
- 如果不将 Supply Chain Management 用作一个数据源，则可以自由映射维度。 下表显示可用维度的完整列表。

> [!NOTE]
> 如果默认维度列表中无您的维度，而您正在使用外部数据源，建议您使用 `ExtendedDimension1` 到 `ExtendedDimension8` 执行映射。

| 维度类型 | 维度名称 |
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
| 其他 | `ExtendedDimension1` 到 `ExtendedDimension8` |

若要添加维度映射，请执行以下步骤。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡上的 **维度映射** 部分中，选择 **添加** 添加维度映射。
1. 在 **维度名称** 字段中，指定源维度。
1. 在 **目标基础维度** 字段中，选择库存可见性中要映射的维度。
1. 选择 **保存**。

![添加维度映射](media/inventory-visibility-dimension-mapping.png "添加维度映射")

例如，如果您的数据源中包含产品颜色维度，则可以将其映射到 `ColorId` 基础维度，以便在 `exterchannel` 数据源中添加一个 `ProductColor` 自定义维度。 然后将其映射到 `ColorId` 基础维度。

## <a name="create-a-physical-measure"></a>创建实际度量

当数据源将库存更改发布到库存可见性时，它将使用 *实际度量* 发布该更改。 实际度量是反映汇总库存交易记录状态的修饰符。 查询可以基于实际度量。

库存可见性有一列默认实际度量。 这些默认实际度量取自 Supply Chain Management 的 **现有库存列表** 页（**库存管理 \> 查询和报表 \> 现有库存列表**）中的库存交易记录状态。

| 修饰符 | 姓名 |
|---|---|
| `PhysicalInvent` | 实际库存 |
| `ReservPhysical` | 实际预留 |
| `AvailPhysical` | 实际可用 |
| `ReservOrdered` | 订单预留 |
| `PostedQty` | 已过帐的数量 |
| `Deducted` | 已扣除 |
| `Picked` | 已领料 |
| `Received` | 已收到 |
| `Registered` | 已登记 |
| `Arrived` | 已到达 |
| `Ordered` | 订购时间 |
| `OnOrder` | 在单 |
| `QuotationReceipt` | 报价收据 |
| `QuotationIssue` | 报价发出量 |

如果数据源为 Supply Chain Management，则不必重新创建默认实际度量。 但是，对于外部数据源，您可以通过执行以下步骤创建新的实际度量。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **数据源** 选项卡的 **实际度量** 部分中，选择 **添加**，指定源度量名称，然后保存更改。

## <a name="define-the-product-hierarchy-index"></a>定义产品层次结构索引

可以通过设置聚合维度组，使用库存可见性查询现有库存状态。 在库存可见性中，每个维度组称为一个 *索引*。 每个索引对应于一个集号。 您可以根据您对库存可见性进行查询的方式，确定哪些维度将用于设置索引。

若要设置产品层次结构索引，请按照以下步骤操作。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **产品层次结构索引** 选项卡上的 **维度映射** 部分中，选择 **添加** 添加维度映射。
1. 默认情况下，将提供一列索引。 若要修改现有索引，请在相关索引的部分中进行 **编辑** 或 **添加**。 若要创建新索引集，请选择 **新建索引集**。 对于每个索引集中的每个行，在 **维度** 字段中，从基础维度列表中选择。 将自动生成以下字段的值：

    - **集号** – 属于同一组（索引）的维度将组合在一起，并为其分配同一个集号。
    - **层次结构** – 层次结构用于定义可在维度组（索引）中查询的受支持维度组合。 例如，如果设置的维度值具有层次结构序列 *样式*、*颜色* 和 *大小*，则系统支持三查询组结果。 第一个组为仅样式。 第二个组为样式和颜色的组合。 而第三个组为样式、颜色和大小的组合。 不支持其他组合。

有关详细信息，请参阅[产品索引层次结构配置](inventory-visibility-configuration.md#index-configuration)。

### <a name="example"></a>示例

此部分提供示例显示层次结构的工作方式。 下表提供此示例的可用库存列表。

| 物料 | 样式 | 颜色 | 大小 | 数量 |
|---|---|---|---|---|
| I0001 | 宽 | 黑色 | 小 | 1 |
| I0001 | 宽 | 黑色 | 大 | 2 |
| I0001 | 宽 | 红色 | 小 | 3 |
| I0001 | 常规 | 黑色 | 小 | 4 |
| I0001 | 常规 | 黑色 | 大 | 5 |
| I0001 | 常规 | 红色 | 小 | 6 |
| I0001 | 常规 | 红色 | 大 | 7 |

下表显示如何设置索引层次结构。

| 键 | 集号 | 层次结构 |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

根据之前的设置，库存可见性查询的维度组合为 *样式*、*颜色* 和 *大小*。 该层次结构设置允许外部系统以以下方式查询现有库存：

- `()` – 按全部分组。 下面是输出。

    - I0001，28

- `(StyleId)` – 按样式分组。 下面是输出。

    - I0001，白色，6
    - I0001，正常，22

- `(StyleId, ColorId)` – 按样式和颜色的组合分组。 下面是输出。

    - I0001，宽，黑色，3
    - I0001，宽，红色，3
    - I0001，正常，黑色，9
    - I0001，正常，红色，13

- `(StyleId, ColorId, SizeId)` – 按样式、颜色和大小的组合分组。 下面是输出。

    - I0001，宽，黑，小，1
    - I0001，宽，黑色，大，2
    - I0001，宽，红色，小，3
    - I0001，正常，黑色，小，4
    - I0001，正常，黑色，大，5
    - I0001，正常，红色，小，6
    - I0001，正常，红色，大，7

## <a name="set-up-a-custom-calculated-measure"></a>设置自定义计算度量

可以使用库存可见性对库存实际度量和 *自定义计算度量* 进行查询。

通过此配置，可以定义一组添加或减去的修饰符，以获取聚合输出数量总值。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **计算度量** 选项卡上，选择 **新建计算度量** 以添加计算度量。 然后，如下表所述设置字段。

    | 字段 | 值 |
    |---|---|
    | 新建计算度量名称 | 输入计算度量的名称。 |
    | 数据源 | 查询系统是数据源。 |
    | 修饰符数据源 | 输入修饰符的数据源。 |
    | 修饰符 | 输入修饰符名称。 |
    | 修饰符类型 | 选择修饰符类型（*加* 或 *减*）。 |

下表显示 `MyCustomAvailableforReservation` 自定义计算度量的示例。 有关此示例的详细信息，请参阅[数据源配置](inventory-visibility-configuration.md#data-source-configuration)。

| 计算度量数据源 | 计算度量 | 修饰符数据源 | 修饰符 | 修饰符类型 |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>设置软预留映射

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

在编辑 **软预留映射** 选项卡之前，必须在 **功能管理** 选项卡上开启 *OnHandReservation* 功能。

通过设置从实际度量到计算度量的映射，可以启用库存可见性服务，以根据实际度量自动验证预留可用性。

在设置此映射之前，必须在 Power Apps 中的 **配置** 页 **数据源** 和 **计算度量** 选项卡上定义实际度量、计算度量和数据源（如本主题前文所述）。

若要定义软预留映射，请按照以下步骤操作。

1. 定义用作软预留度量的实际度量（例如 `softreservordered`）。
1. 在 **配置** 页的 **计算度量** 选项卡上，定义其中包含要映射到实际度量的计算公式的 *可预留* (AFR) 计算度量。 例如，可设置 `availforreserv`（可预留），以使其映射到之前定义的 `softreservordered` 实际度量。 这样就可以发现哪些具有 `softreservordered` 库存状态的数量可预留。 下表显示 AFR 计算公式。

    | 修饰符 | 数据源 | 度量 |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. 打开 **管理** 页面。
1. 在 **软预留映射** 选项卡上，设置从实际度量到计算度量的映射。 对于上一个示例，可以使用以下设置将 `availforreserv` 映射到之前定义的 `softreservordered` 实际度量。

    | 实际度量数据源 | 实际度量 | 可预留数据源 | 可预留计算度量 |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>设置软预留层次结构

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

在编辑 **软预留层次结构** 选项卡之前，必须在 **功能管理** 选项卡上开启 *OnHandReservation* 功能。

预留层次结构描述在进行预留时必须指定的维度的序列。 其工作方式与产品索引层次结构处理现有库存查询的工作方式相同。

预留层次结构可能与现有库存索引层次结构不同。 此独立性让您可以实施类别管理，从而让用户可以将维度细分为详细信息，以便指定有关进行更精确预留的要求。

#### <a name="example"></a>示例

将在您的系统中设置以下预留层次结构。

| 维度 | 层次结构 |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

考虑到此预留层次结构，您可以按以下维度顺序执行预留：

- `()` – 不提供任何维度。
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

维度顺序应逐个维度严格遵循预留层次结构序列。 例如，此示例中不允许具有 `(ColorId, StyleId)` 的预留，因为预留层次结构中未定义此序列。

### <a name="control-feature-management"></a><a name="feature-switch"></a>控制功能管理

库存可见性加载项提供 *OnHandReservation* 和 *OnHandMostSpecificBackgroundService* 之类功能。 默认情况下，这些功能处于关闭状态。 若要使用它们，请在 Power Apps 中打开 **配置** 页，然后在 **功能管理** 选项卡上打开它们。

### <a name="complete-and-update-the-configuration"></a>完成和更新配置

完成配置后，必须将所有更改提交给库存可见性。 若要提交更改，请在 Power Apps 的 **配置** 页右上角中选择 **更新配置**。

首次选择 **更新配置** 时，系统会请求您的凭据。

- **客户端 ID** – 您为库存可见性创建的 Azure 应用程序 ID。
- **租户 ID** – 您的 Azure 租户 ID。
- **客户端密钥** – 您为库存可见性创建的 Azure 应用程序密钥。

登录后，库存可见性服务中将更新配置。

> [!NOTE]
> 请务必先验证数据源名称、实际度量和维度映射，然后再更新库存可见性服务的配置。 选择 **更新配置** 之后，不能修改这些设置。

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>查找服务终结点

如果不知道正确的库存可见性服务终结点，请在 Power Apps 中打开 **配置** 页，然后在右上角选择 **显示服务终结点**。 页面将显示正确的服务终结点。

## <a name="operational-visibility"></a>操作可见性

**操作可见性** 页根据各种维度组合提供实时现有库存查询的结果。 如果开启了 *OnHandReservation* 功能，也可从 **操作可见性** 页发布预留请求。

### <a name="on-hand-query"></a>现有库存查询

**现场库存查询** 选项卡显示实时现有库存查询的结果。

选择 **现有库存查询** 选项卡时，系统将索取您的凭证，以便获取查询库存可见性服务所需持有者令牌。 只能将持有者令牌粘贴到 **BearerToken** 字段中，然后关闭对话框。 然后可以发布现有库存查询请求。

如果持有者令牌无效，或者其已过期，则必须将新令牌粘贴到 **BearerToken** 字段中。 输入正确的 **客户端 ID**、**租户 ID**、**客户端密钥** 值，然后选择 **刷新**。 系统将自动获取新的有效持有者令牌。

若要发布现有查询，请在请求正文中输入查询。 使用[使用发布方法查询](inventory-visibility-api.md#query-with-post-method)中介绍的模式。

![现有库存查询设置](media/inventory-visibility-query-settings.png "现有库存查询设置")

### <a name="reservation-posting"></a>预留发布

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

可使用 **预留发布** 选项卡发布预留请求。 必须先开启 *OnHandReservation* 功能，才能发布预留请求。 有关此功能的详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

若要发布预留请求，必须在请求正文中输入一个值。 请使用[创建一个预留事件](inventory-visibility-api.md#create-one-reservation-event)中介绍的模式。 然后选择 **发布**。 若要查看请求响应详细信息，请选择 **显示详细信息**。 也可以从响应详细信息获取 **reservationId** 值。

## <a name="inventory-summary"></a>库存汇总

**库存汇总** 是 *现有库存总和实体* 的自定义视图。 其提供产品的库存汇总以及所有维度。 可以通过使用 Dataverse 提供的 **高级筛选器**，创建个人视图以显示对您至关重要的行。 可使用高级筛选器选项创建从简单到复杂的大量视图。 还可用于向筛选器添加组合嵌套条件。

若要了解有关如何使用 **高级筛选器** 的详细信息，请参阅[使用高级网格筛选器编辑或创建个人视图](/powerapps/user/grid-filters-advanced)

这个自定义视图的顶部显示三个字段：**默认维度**、**自定义维度** 和 **度量**。 可以使用这些字段控制哪些列可见。

可以选择列标题，以便筛选当前结果或为当前结果排序。

这个自定义视图的底部显示信息，如“50 条记录（29 条已选）”或“50 条记录”。 此信息指的是当前从 **高级筛选器** 结果加载的记录。 文本“29 条已选”指的是通过对加载的记录使用列标题选择的记录的数量。

视图底部是可用于从 Dataverse 加载更多记录的 **加载更多** 按钮。 加载的默认记录的数量为 50。 选择 **加载更多** 时，将在视图中加载下 1,000 条可用记录。 **加载更多** 按钮上的数字指示当前加载的记录数和 **高级筛选器** 结果的记录总数。

![库存汇总](media/inventory-visibility-onhand-list.png "库存汇总")
