---
title: 采用双写入的库存可用性
description: 本文提供有关如何以双写入方式检查库存可用性的信息。
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 442486550d3a7c5132e26f663caaa7c2c02eeb6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289199"
---
# <a name="inventory-availability-in-dual-write"></a>采用双写入的库存可用性

[!include [banner](../../includes/banner.md)]

使用库存可用性，可以在 Microsoft Dynamics 365 Sales 中先检查库存，然后再将产品添加到 **报价单**、**订单** 或 **发票** 页面。 例如，检查库存并将履行日期确定为[目标客户到现金](dual-write-prospect-to-cash.md)流程的一个关键任务。

如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。 您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。

## <a name="on-hand-inventory"></a>现有库存

在 Dynamics 365 Sales 中，**报价单**、**订单** 和 **发票** 页面的标题中已经添加了一个新的 **现有库存量** 按钮。 选择此按钮时，将出现一个对话框，您可以在其中指定要检查其现有库存量的公司和产品。 此对话框显示的信息与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同。

此对话框返回 Dynamics 365 Supply Chain Management 中的库存信息。 此信息包括以下数量：

- 现有数量
- 预留现有数量
- 可用现有数量
- 订购数量
- 在单数量
- 预留的订购数量
- 可用总数

## <a name="atp-information"></a>ATP 信息

在 Sales 中，**报价单**、**订单** 和 **发票** 页面的行项中已经添加了新的 **ATP 信息** 按钮。 选择此按钮时，将出现一个对话框，您可以在其中指定公司、产品、库存站点、库存仓库和订单数量。 此对话框具有与[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置相同的设置。

此对话框返回 Supply Chain Management 中的 ATP 信息。 此信息包括以下数量：

- ATP 数量
- 收货数量
- 发货数量
- 现有数量

## <a name="how-it-works"></a>工作原理

当您在 **报价单**、**订单** 或 **发票** 页上选择 **现有库存量** 按钮时，会对 **现有库存量** API 进行实时双写入调用。 API 计算给定产品的现有库存量。 结果存储在 **InventCDSInventoryOnHandRequestEntity** 和 **InventCDSInventoryOnHandEntryEntity** 表中，然后通过双写入将其写入 Dataverse。 要使用此功能，您需要运行以下双写入映射。 运行映射时跳过初始同步。

- CDS 现有库存条目 (msdyn_inventoryonhandentries)
- CDS 现有库存请求 (msdyn_inventoryonhandrequests)

## <a name="templates"></a>模板

以下模板可用于公开现有库存量数据。

Finance and Operations 应用 | 客户互动应用     | 说明
---|---|---
[CDS 库存现有条目](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS 库存现有请求](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
