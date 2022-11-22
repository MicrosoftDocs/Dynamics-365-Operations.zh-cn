---
title: Inventory Visibility 预留
description: 本文介绍如何设置预留功能，以使用库存可见性创建预留，使用预留和/或取消预留指定的库存数量。
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
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762714"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility 预留

[!include [banner](../includes/banner.md)]

本文介绍软预留的典型用例，并说明如何在库存可见性中设置它们。 其中包括有关如何创建软预留、在实际消耗时抵销这些预留以及调整或取消预留指定库存数量的信息。

## <a name="sample-use-case-for-soft-reservation"></a>软预留的示例用例

软预留可帮助组织实现有一个单一的可用库存真实来源，尤其是在订单履行过程中。 此功能对于存在以下条件的组织很有用：

- 组织至少有两个不同的系统直接接收出站订单。
- 组织非常严格，希望防止重复预订产品库存，当多个系统能够超额预订最后一件库存产品时，会发生这种情况。 当所有订单系统都可以对库存可见性发起即时软预留 API 调用时，这种情况就可以避免，因为这将为库存可用性提供单一的真实来源。

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="库存可见性软预留" width="720" />](media/inventory-visibility-soft-reservation.png)

上图显示了软预留的工作原理，突出显示以下操作：

- 您的初始库存水平从 Microsoft Dynamics 365 Supply Chain Management 同步到库存可见性。
- 软预留从您的每个订单渠道或系统发布到库存可见性。 库存可见性验证库存可用性并尝试进行软预留。 如果软预留成功，库存可见性将加上软预留数量，从可供预留 (AFR) 数量中扣减，并使用软预留 ID 响应。
- 此时，您的实际库存数量保持不变。
- 然后，您可以将单个或聚合的软预留订单（订单行）同步到 Supply Chain Management，以进行硬预留并发放到仓库或更新最终库存数量。
- 您可以将系统设置为在 Supply Chain Management 中更新实际库存时[抵销软预留](#offset-scm)。

软预留通常通过使用对库存可见性服务的 API 调用来创建、使用和取消。

> [!NOTE]
> 可选择将 Supply Chain Management（和其他第三方系统）设置为自动抵销已使用库存可见性预留的数量。 将从库存可见性中的预留记录内删除抵销的数量。
>
> 默认情况下，当您启用软预留功能时，抵销功能会自动打开。

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>开启和设置预留功能

若要打开预留功能，请执行以下步骤。

1. 登录 Power Apps，打开 **库存可见性**。
1. 打开 **管理** 页面。
1. 在 **功能管理** 选项卡上，打开 *OnHandReservation* 功能。
1. 登录到您的 Supply Chain Management 环境。
1. 转到 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区，然后启用 *带预留抵销的库存可见性集成* 功能（需要版本 10.0.22 或更高版本）。
1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**，打开 **预留抵销** 选项卡，然后进行以下设置：

    - **启用预留抵销** – 设置为 *是* 以启用此功能。
    - **预留抵销修饰符** – 选择将抵销在库存可见性中所做预留的库存交易记录状态。 此设置决定触发抵销的订单处理阶段。 此阶段通过订单的库存交易记录状态跟踪。 选择以下值之一：

        - *在单* – 状态为 *在单* 的订单在创建时将发送抵销请求。 抵销数量将为所创建订单（行）的数量。
        - *预留* – 当订单已预留或已实际预留时，状态为 *预留* 的订单将发送抵销请求。 当您在 *预留* 状态下进行抵销时，订单将在最接近已预留领料量的任何新库存状态（例如，领料、装箱单已过帐或已开票）发送抵销请求。 即使您跳过 Supply Chain Management 中的预留，继续进入另一个库存状态（例如，您从发放到仓库跳到领料和装箱），也会发生此行为。 此请求只会触发一次。 如果它已在领料时触发，则不会在过帐装箱单时重复抵销。 抵销数量将与触发抵销时库存交易状态的数量相同（即相应订单行上的 *已预留订购数量*/*已预留实际数量*，或后来的状态）。

1. 重新登录库存可见性应用，转到 **配置** 页面，然后在 **软预留** 选项卡上查看默认的软预留层次结构。 根据需要向层次结构添加新维度。
1. 在 **设置软预留映射** 部分，查看默认设置。 默认情况下，将根据数据源 `iv` 的 `softreservephysical` 实际度量记录软预留库存数量。 *可供预留* 计算度量将映射到 `availabletoreserve`。 如果您想要更新 `availabletoreserve` 计算度量值，转到 **配置** 页面，然后在 **计算量度** 选项卡上，展开并修改计算度量。

有关详细信息，请参阅[配置库存可见性](inventory-visibility-configuration.md)。

> [!NOTE]
> 预留层次结构描述在进行预留时必须指定的维度的序列。 它的工作方式与索引层次结构在现有量查询中使用的方式相同，但它是独立使用的，因此用户可以指定维度详细信息来进行更精确的预留。
>
> 软预留层次结构中应包含组件形式的 `SiteId` 和 `LocationId`，因为其构造库存可见性的分区配置。

有关如何配置预留的详细信息，请参阅[预留配置](inventory-visibility-configuration.md#reservation-configuration)。

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>使用库存可见性中的预留功能

在调用预留 API 时，系统将标记指定货物和数量的预留。

下面是一个示例场景和一个示例 API 查询正文。 Contoso 公司从其电子商务网站销售产品 D0002（柜子）。 一位客户通过网站下了一个销售订单，购买红色小柜子。 Contoso 决定使用以下维度来履行此订单：

- 组织 ID = usmf
- 站点 = 1
- 仓库 = 11
- 产品 = D0002
- 颜色 = 红色
- 尺寸 = 小

Contoso 已经从其自己的电子商务系统设置了与库存可见性的 API 连接。 收到订单后，系统会立即触发 API 调用，在库存可见性中对柜子进行软预留。

### <a name="create-soft-reservations-using-the-reservation-api"></a>使用预留 API 创建软预留

在库存可见性服务中创建预留的方法是，向服务的 URL（如 `/api/environment/{environmentId}/onhand/reserve`）提交 POST 请求。

对于预留，请求正文中必须包含组织 ID、产品 ID、预留数量和维度。

调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值为 `True` 表示需要验证，而值为 `False` 则表示不需要验证。 默认值为 `True`。

如果要取消预留或撤消指定的库存数量，请将数量设置为负数，然后将 `ifCheckAvailForReserv` 参数设置为 `False` 以跳过验证。

下面是引用先前上下文中的销售订单的请求正文示例。

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

成功的软预留请求为每个预留记录返回 *软预留 ID*。 软预留 ID 不是单个软预留记录的唯一标识符，而是与软预留请求关联的产品 ID 和维度值的组合。 当您将成功预留的订单同步到 Supply Chain Management 或另一个 ERP 系统进行抵销时，您可以在订单行上记录软预留 ID。

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>在 Supply Chain Management 中抵销软预留

在 Supply Chain Management 或另一个 ERP 系统中实际扣除订单上的数量后，您可以抵销软预留数量。 库存可见性提供现成的软预留抵销与 Supply Chain Management 的集成。

按照以下步骤抵销软预留。

1. 登录 Supply Chain Management。
1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 在操作窗格上，选择 **新建**。
1. 重新创建外部销售订单，并添加使用完全相同的产品 ID、组织、站点、仓库和维度值的销售行。
1. 在 **销售订单行** 快速选项卡上，选择您刚才输入的销售行，然后在工具栏上，选择 **库存 \> 预留**。
1. 按以下步骤之一：

    - 复制软预留请求响应中的软预留 ID，将其粘贴到 **预留 ID** 字段中。
    - 保留 **预留 ID** 字段为空，但选中 **库存服务自动抵销** 复选框。 系统将根据在选定行中输入的项目 ID 和维度值，自动确定要抵销的产品和产品维度。

1. 选择 **确定**。
1. 仍然选择相同的销售行，通过在 **销售订单行** 快速选项卡的工具栏上选择 **库存 \> 预留** 来实际预留订购数量。
1. 如果您之前将 **预留抵销修饰符** 字段设置为 *已预留*，当订单行的状态为 *预留实际数量* 或 *预留订购数量* 时，将触发抵销。 批处理作业每分钟运行一次，将来自 Supply Chain Management 的抵销请求同步到库存可见性。

> [!NOTE]
> 对于其中包含指定预留抵销修饰符的交易记录状态，如果满足下面的所有条件，交易记录更新将抵销相应的预留记录。
>
> - 库存交易记录中的预留 ID 与库存可见性中的预留记录的预留 ID 匹配。
> - 库存交易记录中的维度与库存可见性中的预留记录的维度匹配。
> - 当库存交易记录状态反映订单流程已完成或已跳过的事实时，库存交易记录状态的更改将触发预留抵销。

抵销数量遵从相关库存交易记录中指定的库存数量。 只有预留数量在库存可见性中保持不变时，抵销才会生效。

### <a name="cancel-or-revert-a-soft-reservation"></a>取消或恢复软预留

如果原始订单行被取消或删除，但您必须恢复相应的软预留，在您的 API 查询正文中发布具有完全相同信息的负数量。
