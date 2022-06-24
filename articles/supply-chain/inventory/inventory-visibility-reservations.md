---
title: Inventory Visibility 预留
description: 本文介绍如何设置预留功能，以使用库存可见性创建预留，使用预留和/或取消预留指定的库存数量。
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
ms.openlocfilehash: 3b74907709ab97ddf4cc829dba324df213ca229f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895719"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility 预留

[!include [banner](../includes/banner.md)]


本文介绍如何设置预留功能，以使用库存可见性创建预留，使用预留和/或取消预留指定的库存数量。

预留将标记以后将使用的一定数量的库存。 在创建预留时，系统将阻止其他订单预留或使用预留的货物，直至使用或取消预留了该预留。 可通过对库存可见性服务执行 API 调用来创建，使用和取消预留。

可选择将 Microsoft Dynamics 365 Supply Chain Management（和其他第三方系统）设置为自动抵销已使用库存可见性预留的数量。 将从库存可见性中的预留记录内删除抵销的数量。

如果开启预留功能，Supply Chain Management 将自动为抵销使用库存可见性进行的预留做好准备。

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>开启和设置预留功能

若要打开预留功能，请执行以下步骤。

1. 登录 Power Apps，然后打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **功能管理** 选项卡上，打开 *OnHandReservation* 功能。
1. 登录 Supply Chain Management。
1. 转到 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区，然后启用 *带预留抵销的库存可见性集成* 功能（需要版本 10.0.22 或更高版本）。
1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**，打开 **预留抵销** 选项卡，然后进行以下设置：
    - **启用预留抵销** – 设置为 *是* 以启用此功能。
    - **预留抵销修饰符** – 选择将抵销在库存可见性中所做预留的库存交易记录状态。 此设置决定触发抵销的订单处理阶段。 此阶段通过订单的库存交易记录状态跟踪。 选择以下各项之一：
        - *在单* – 对于 *在交易记录* 状态，创建订单时间发送抵销请求。 抵销数量将为所创建订单的数量。
        - *预留* – 对于 *预留订购的交易记录* 状态，对订单进行预留，拣货，过帐装箱单或开票时，订单将发送抵销请求。 此请求仅在上述流程发生时为第一个步骤触发一次。 抵销数量将为其中的相应订单行上库存交易记录状态已从 *在单* 更改为 *订购预留*（或更晚状态）的数量。

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>使用库存可见性中的预留功能

在调用预留 API 时，系统将标记指定货物和数量的预留。 必须定义预留层次结构并过帐与该预留层次结构匹配的请求。 然后可以通过直接调用预留 API 来创建预留。

### <a name="configure-the-reservation-hierarchy"></a>配置预留层次结构

预留层次结构描述在进行预留时必须指定的维度的序列。 其工作方式与索引层次结构处理现有库存查询的工作方式相同。

预留层次结构可能与索引层次结构不同。 此独立性让您可以实施类别管理，从而让用户可以将维度细分为详细信息，以便指定有关进行更精确预留的要求。

若要在 Power Apps 中配置软预留层次结构，请打开 **配置** 页面，然后在 **软预留层次结构** 选项卡上，通过添加和/或修改维度及其层次结构级别设置预留层次结构。

软预留层次结构中应包含组件形式的 `SiteId` 和 `LocationId`，因为其构造分区配置。

有关如何配置预留的详细信息，请参阅[预留配置](inventory-visibility-configuration.md#reservation-configuration)。

### <a name="call-the-reservation-api"></a>调用预留 API

在库存可见性服务中创建预留的方法是，向服务的 URL（如 `/api/environment/{environment-ID}/onhand/reserve`）提交 POST 请求。

对于预留，请求正文中必须包含组织 ID、产品 ID、预留数量和维度。 该请求将为每个预留记录生成一个唯一预留 ID。 预留记录中包含产品 ID 和维度的唯一组合。

调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值为 `True` 表示需要验证，而值为 `False` 则表示不需要验证。 默认值为 `True`。

如果要取消预留或撤消指定的库存数量，请将数量设置为负数，然后将 `ifCheckAvailForReserv` 参数设置为 `False` 以跳过验证。

下面是请求正文的示例，供您参考。

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>在 Supply Chain Management 中抵销预留

对于其中包含指定预留抵销修饰符的库存交易状态，如果满足下面的所有条件，更新交易将抵销相应预留记录。

- 库存交易记录中的预留 ID 与库存可见性服务中的预留记录的预留 ID 匹配。
- 库存交易记录中的维度与库存可见性服务中的预留记录的维度相同。
- 当库存交易记录状态反映订单流程已完成或已跳过的事实时，库存交易记录状态的更改将触发预留抵销。

抵销数量遵循在库存交易记录中指定的库存数量。 如果库存可见性服务中没有预留数量，则抵销不会生效。

### <a name="set-up-the-reservation-offset-modifier"></a>设置预留抵销修饰符

如果尚未执行此操作，请按照[开启和设置预留功能](#turn-on)中的说明设置预留修饰符。

### <a name="set-up-reservation-ids"></a>设置预留 ID

预留 ID 唯一标记库存可见性中的预留记录。 在 Supply Chain Management 中，用户在订单行中放置预留以标记相应预留记录的抵销。

若要在 Supply Chain Management 中设置预留 ID，请按照以下步骤操作。

1. 打开销售订单（例如，从 **所有销售订单** 页面打开）。
1. 在 **销售订单行** 快速选项卡上，选择一个订单行。
1. 在工具栏上的 **销售订单行** 快速选项卡上，选择 **更新行 \> 库存 \> 库存可见性集成**。
1. 输入相关的预留 ID。

库存状态更改将与抵销修饰符设置匹配。
