---
title: 登记入站订单时数量无效
description: 如果为牌照分配的数量超过针对当前维度仍必须收货的数量，您将收到错误消息“数量无效。”
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475728"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>登记入站订单时牌照数量无效

## <a name="symptoms"></a>故障特征

等记入站订单时，可能会收到以下错误消息：

> 此数量无效。

如果在用于登记入库订单的移动设备菜单项中，**牌照分组策略** 字段设置为 *用户定义*，您将此错误消息，并且无法完成登记。

## <a name="cause"></a>原因

当 *用户定义* 用作牌照分组策略时，系统将传入库存拆分为单独的牌照，如单位序列组所示。 如果批号或序列号用于跟踪将收货的物料，必须按登记的牌照指定每个批次或序列的数量。 如果为牌照指定的数量超过针对当前维度仍必须收货的数量，您将收到此错误消息。

## <a name="resolution"></a>解决方法

使用 **牌照分组策略** 字段设置为 *用户定义* 的移动设备菜单项登记物料时，系统可能会要求您确认或输入牌照编号、批号或序列号。

在牌照确认页面上，系统将显示为当前牌照分配的数量。 在批次或序列确认页面上，系统将显示在当前牌照上仍必须收货的数量。 它还将包含一个字段，您可以在其中输入为牌照和批号或序列号组合登记的数量。 在这种情况下，请确保为牌照登记的数量不超过仍必须收货的数量。

或者，如果在入库订单登记时生成了太多牌照，**牌照分组策略** 字段的值可以更改为 *牌照分组*，可以向物料分配新的单位序列组或者可以停用单位序列组的 **牌照分组** 选项。
