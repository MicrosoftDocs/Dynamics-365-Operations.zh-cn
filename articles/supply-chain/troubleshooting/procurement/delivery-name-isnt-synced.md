---
title: 更改采购订单交货地址后交货名称不同步
description: 更改采购订单标题上的交货地址后，交货名称没有同步
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475656"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>更改采购订单交货地址后交货名称不同步

## <a name="symptoms"></a>故障特征

采购订单标题上的地址将更新为不是交货地址的地址。 虽然地址在采购订单上已更新，但交货名称不会根据更新的地址进行更新。

## <a name="resolution"></a>解决方法

此为有意行为。 所选地址必须分类为交货地址。 否则，交货名称不会根据所选地址更新。
