---
title: Inventory Visibility 库存分配
description: 本文介绍如何设置和使用库存分配功能，通过此功能，您可以预留专用库存，以确保您可以获得最有利可图的渠道或客户。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762664"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility 库存分配

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>业务背景和用途

组织通常必须将现有库存量预先分配给最重要的销售渠道、客户群、地区和促销活动，以确保预先分配的库存受到保护，不会用于任何其他用途，只能通过与分配相关的销售交易消耗。 库存可见性中的库存分配是销售运营计划流程的一个组成部分，在任何实际销售活动发生或创建销售订单之前完成。

例如，名为 Contoso 的公司生产流行的自行车。 不幸的是，由于最近的供应链中断影响了该自行车的所有在途库存，Contoso 的现有库存量有限，必须加以充分利用。 Contoso 同时经营线上销售和店内销售。 在每个销售渠道中，此公司都有一些重要的公司合作伙伴（商城和大型零售商），他们要求为他们保存自行车可用库存的特定部分。 因此，此自行车公司必须能够平衡跨渠道存货分配，并达到其 VIP 合作伙伴的期望。 实现这两个目标的最佳方法是使用库存分配，以便每个渠道和零售商都可以收到以后可向消费者出售的特定分配数量。

库存分配具有两个基本业务用途：

- **库存保护（圈护）**– 组织希望将受限或有限的库存预分配到优先的渠道、区域、VIP 客户和子公司。 库存可见性分配功能旨在保护分配的库存，以便其他分配、预留或其他销售需求不会影响先前分配的库存。
- **超额销售控制** - 库存可见性分配功能旨在对先前分配的数量施加限制，以便当基于软性预留的实际销售交易生效时，接收方（例如渠道或客户组）不会过度使用它们。

## <a name="allocation-definition-in-inventory-visibility-service"></a>库存可见性服务中的分配定义

### <a name="allocation-virtual-pool"></a>分配虚拟池

虽然库存可见性中的分配功能未预留实际库存数量，但它确实引用了可用的实际库存数量来定义其初始 *可用于分配* 的虚拟池数量。 库存可见性中的库存分配是软分配。 此分配在实际销售交易发生之前已完成，不依赖于销售订单。 例如，在任何最终客户访问销售渠道或零售商店以购买商品之前，您可以将存货分配到最重要的销售渠道或大型公司零售商。

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>库存分配和软预留之间的区别

[软预留](inventory-visibility-reservations.md)通常链接到实际销售交易（销售订单行）。 分配和软预留都可以单独使用，但如果您想要一起使用，则应在分配后进行软预留。 我们建议您首先进行库存分配，然后根据分配的数量进行软预留，以实现近乎实时的基于分配的消耗。 有关详细信息，请参阅[以软性预留形式使用](#consume-to-soft-reserved)。

通过库存分配功能，销售计划员或关键客户经理可以跨分配组（如渠道、区域和客户组）管理和预分配重要库存。 它还支持针对分配的数量实时跟踪、调整和分析消耗量，以确保可以按时进行补货或重新分配。 这种能够实时了解分配、消耗量和分配余额的功能在快速销售或促销活动中尤为重要。

## <a name="terminology"></a>术语

以下条款和概念在讨论库存分配时很有用：

- **分配组** - 负责分配的组，如销售渠道、客户组或订单类型。
- **分配组值** - 每个分配组的值。 例如，*Web* 或 *商店* 可能是销售渠道分配组的值，而 *VIP* 或 *普通* 值可能是客户分配组的值。
- **分配层次结构** - 以分层方式组合分配组的一种方法。 例如，您可以将 *渠道* 定义为层次结构级别 1，将 *区域* 定义为级别 2，将 *客户组* 定义为级别 3。 在库存分配期间，当您指定分配组的值时，必须遵循分配层次结构序列。 例如，您可能会将 200 辆红色自行车分配给 *Web* 渠道、*伦敦* 地区和 *VIP* 客户组。
- **可用于分配** - 指示可用于进一步分配的数量的 *虚拟公共池*。 这是一个计算的度量，您可以使用自己的公式自由定义。 如果您还使用软性预留功能，我们建议您使用相同的公式来计算可用于分配和可用于预留的数量。
- **已分配** - 显示分配组可使用的分配配额的实际度量。 在添加消耗数量的同时扣除。
- **已消耗** - 一种实际度量，指示已根据原始分配数量消耗的数量。 将数字添加到此实际度量时，将自动减少分配的实际度量。

下图显示了库存分配的业务工作流。

![库存可见性分配业务工作流。](media/inventory-visibility-allocation-flow.png "库存可见性分配业务工作流。")

下图显示了分配层次结构和分配组。 此处显示的 *虚拟公共池* 是可用于分配的数量。

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="库存可见性分配层次结构" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>设置库存分配

库存分配功能由以下组件组成：

- 预定义的与分配相关的数据源、实际度量和计算的度量。
- 最多具有 8 个级别的可自定义分配组。
- 一组分配应用编程接口 (API)：

    - 分配
    - 重新分配
    - 取消分配
    - 使用
    - 查询

配置分配功能的过程有三个步骤：

- 转到 **配置 \> 功能管理和设置 \> 分配**，启用库存可见性应用中的功能。
- 设置[数据源](inventory-visibility-configuration.md#data-source-configuration)及其[度量](inventory-visibility-configuration.md#data-source-configuration-physical-measures)。
- 设置分配组名称和层次结构。

### <a name="predefined-data-source"></a>预定义的数据源

当您启用分配功能并调用配置更新 API 时，库存可见性将创建一个预定义的数据源和多个初始度量。

数据源名为 `@iv`。 它包括一组默认物理度量。 您可以转到 **配置 \> 数据源** 从库存可见性应用查看这些度量。 您应该会看到 **Datasource - @IV**。 展开 `@iv` 数据源查看初始物理度量列表：

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

选择 **计算度量** 选项卡查看初始计算度量，名为 `@iv.@available_to_allocate`：

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>将其他实际度量添加到可用于分配的计算度量

要使用分配，您必须为可用于分配的计算度量 (`@iv.@available_to_allocate`) 正确设置公式。 例如，您有 `fno` 数据源和 `onordered` 度量、`pos` 数据源和 `inbound` 度量，并且您希望对 `fno.onordered` 和 `pos.inbound` 的总现有库存量进行分配。 在此情况下，`@iv.@available_to_allocate` 应在公式中包含 `pos.inbound` 和 `fno.onordered`。 下面是一个示例：

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> 数据源 `@iv` 是预定义的数据源，在 `@iv` 中定义的带有前缀 `@` 的物理度量是预定义的度量。 这些度量是分配功能的预定义配置，因此请勿更改或删除它们，否则在使用分配功能时可能会遇到意外错误。
>
> 您可以将新的物理度量添加到预定义的计算度量 `@iv.@available_to_allocate`，但不得更改其名称。

### <a name="manage-allocation-groups"></a>管理分配组

最多可设置 8 个分配组名称。 这些组具有层次结构。 按照以下步骤查看和更新分配组。

1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **配置** 页面，然后，在 **分配** 选项卡上，选择 **编辑配置**。 默认情况下，分配层次结构有四层：`Channel`（顶层）、`customerGroup`（第二层）、`Region`（第三层）和 `OrderType`（第四层）。
1. 您可以通过选择现有分配组旁边的 **X** 来删除该分配组。 您还可以通过直接在字段中输入每个新组的名称来将新分配组添加到层次结构中。

    > [!IMPORTANT]
    > 删除或更改分配层次结构映射时要小心。 相关指南请参阅[使用分配的提示](#allocation-tips)。

1. 配置完分配组和层次结构设置后，保存更改，然后选择右上角的 **更新配置**。 使用用户界面或 API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate) 创建分配时，将更新配置的分配组的值。 本文稍后将提供有关这两种方法的详细信息。

如果您使用四个组名称并将其设置为 \[`channel`、`customerGroup`、`region`、`orderType`\]，则当您调用配置更新 API 时，这些名称将对与分配相关的请求有效。

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>使用分配的提示

- 对于每个产品，应根据您在 [产品索引层次结构配置](inventory-visibility-configuration.md#index-configuration)中设置的产品索引层次结构在同一 *维度级别* 中使用分配函数。 例如，假设您的索引层次结构是 \[`Site`、`Location`、`Color`、`Size`\]。 如果您在维度级别 \[`Site`、`Location`、`Color`\] 为一个产品分配了一些数量，那么下次您要分配此产品时，您也应该在同一级别 \[`Site`、`Location`、`Color`\] 分配。 如果使用级别 \[`Site`、`Location`、`Color`、`Size`\] 或 \[`Site`、`Location`\]，数据将不一致。
- **修改分配组和层次结构：** 如果系统中已经存在分配数据，删除现有分配组或改变分配组层次结构将破坏分配组之间的现有映射。 因此，请务必在更新新配置之前手动清理所有旧数据。 但是，由于将新分配组添加到最低层次结构不会影响现有映射，您不需要清理数据。
- 只有当产品 `available_to_allocate` 数量为正时，分配才会成功。
- 要将产品从高 *分配级别* 组分配到子组，使用 `Reallocate` API。 例如，您有一个分配组层次结构 \[`channel`、`customerGroup`、`region`、`orderType`\]，您想要从分配组\[在线、VIP\] 分配一些产品到子分配组\[在线、VIP、EU\]，应使用 `Reallocate` API 移动数量。 如果使用 `Allocate` API，它将从虚拟公共池分配数量。
- 要查看整体产品可用性（公共池），使用 [查询现有量](inventory-visibility-api.md#query-on-hand) API 请求 *可用于分配* 的库存量。 然后，您可以根据此信息作出分配决定。

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>使用分配 API

当前，已打开五个分配 API：

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – 此 API 用于创建初始分配。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – 此 API 用于恢复或删除分配的数量。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – 此 API 用于将分配的数量从现有分配移到其他分配组。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – 此 API 用于扣除（使用）分配的数量。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – 此 API 用于根据分配组和层次结构检查现有分配记录。

### <a name="allocate"></a>分配

调用 `Allocate` API 以分配具有特定维度的产品。 以下是请求正文的架构。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

例如，您要针对 *自行车* 产品、站点 *1*、位置 *11*、*红色* 颜色、*在线* 渠道、*VIP* 客户组和 *美国* 区域分配数量 10。 要执行此分配，您可以进行具有以下正文内容的调用。

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

数量必须始终大于 0（零）。

### <a name="unallocate"></a>取消分配

使用 `Unallocate` API 撤销 `Allocate` 操作。 `Allocate` 操作中不允许存在负数量。 `Unallocate` 的正文与 `Allocate` 的正文完全相同。

### <a name="reallocate"></a>重新分配

使用 `Reallocate` API 将一些分配的数量移动到其他组组合。 以下是请求正文的架构。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

例如，通过调用 `Reallocate` API 并提供以下正文文本，您可以将维度为 \[站点=1、位置=11、颜色=红色\] 的两辆自行车从 \[在线、VIP、美国\] 分配组移到 \[在线、VIP、EU\] 分配组。

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>使用

使用 `Consume` API 根据分配过帐消耗量。 例如，您可能会使用此 API 将分配的数量移到一些实际度量。 以下是请求正文的架构。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

例如，为 \[在线、VIP、US\] 分配组分配了 8 辆维度为 \[站点=1、位置=11、颜色=红色\] 的自行车。 使用了以下可用于分配的公式：

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

从 `pos.inbound` 度量中分配了八辆自行车。

现在，已售出三辆自行车，这些自行车是从分配池中购买的。 要登记此变动，您可以进行具有以下请求正文的调用。

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

进行此调用后，产品的分配数量将减少 3。 此外，库存可见性将生成一个 `pos.inbound` = *-3* 的现有更改事件。 或者，您可以将 `pos.inbound` 值保持原样，并且仅使用分配的数量。 但是，在这种情况下，您必须创建另一个实际度量，以保留消耗的数量或使用预定义的度量 `@iv.@consumed`。

在此请求中，请注意您在 consume 请求正文中使用的实际度量应使用与计算量度中使用的修饰符类型相反的修饰符类型（加法或减法）。 因此，在此 consume 正文中，`iv.inbound` 具有的值是 `Subtraction`，而不是 `Addition`。

`fno` 数据源不能在 consume 正文中使用，因为我们一直声称库存可见性不能更改 `fno` 数据源的任何数据。 数据流是单向的，这意味着 `fno` 数据源的所有数量变化都必须来自您的 Supply Chain Management 环境。

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>以软性预留形式使用

`Consume` API 还可以将分配的数量用作软性预留。 在这种情况下，`Consume` 操作将减少分配的数量，然后对该数量执行软性预留。 要使用此方法，您还必须使用库存可见性的[软性预留](inventory-visibility-reservations.md)功能。

例如，您已将软预留实际度量设置为 `iv.softreserved`。 以下公式用于可用于预留的计算度量：

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

要将此设置与分配功能结合使用，请将 `@iv.@allocated` 添加到 `iv.available_to_reserve` 以生成以下公式：

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

然后将 `@iv.@available_to_allocate` 更新为相同的值。

当您想要使用值为 3 的数量并直接预留此数量时，您可以进行具有以下请求正文的调用。

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

在此请求中，请注意，`iv.softreserved` 具有的值是 `Addition`，而不是 `Subtraction`。

### <a name="query"></a>查询

使用 `Query` API 检索某些产品的分配相关信息。 您可以使用维度筛选器和分配组筛选器缩小结果范围。 维度必须与您要检索的项完全匹配，例如，与 \[站点=1、位置=11、颜色=红色\] 相比，\[站点=1、位置=11\] 将具有不相关的结果。

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

例如，使用 \[站点=1、位置=11、颜色=红色\] 和空组字段获取所有分配记录：

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

使用 \[站点=1、位置=11、颜色=红色\] 和组 \[渠道=线上、CustomerGroup=VIP、区域=美国\] 获取此组的分配记录：

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>使用分配用户界面

您可以通过用户界面手动管理分配，方法是打开“库存可见性”应用，转到 **运营可见性 \> 分配**。 从那里，您可以执行以下各小节描述的任何操作。

### <a name="create-an-allocation"></a>创建分配

按照以下步骤从“库存可见性”应用的 **分配** 页面创建分配。

1. 选择 **分配**。
1. 设置基本字段、维度和目标分配组值。 （在 **维度** 部分选择收集数据源时，首先使用下拉列表指定维度(例如，`siteId`)。 然后在出现的字段中输入维度值。）
1. 选择 **提交**。

### <a name="consume-an-allocation"></a>使用分配

选择 **使用** 使用分配。 为确保您在正确的分配组和层次结构中使用，请输入您在创建分配时输入的相同组织和维度详细信息集。

### <a name="reallocate-an-allocation"></a>重新分配分配

选择 **重新分配** 将现有的已分配数量从一组分配组移到另一组。

### <a name="query-existing-allocations"></a>查询现有分配

选择 **查询**，然后输入产品、组织、维度和分配组值获取现有分配的查询结果。
