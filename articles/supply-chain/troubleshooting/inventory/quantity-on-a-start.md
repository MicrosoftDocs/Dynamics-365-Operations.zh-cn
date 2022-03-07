---
title: 拆分订单后，已开始的隔离订单上的数量不更新
description: 当您创建隔离订单并尝试拆分它时，订单数量未更新为拆分后的剩余数量。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026316"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>拆分订单后，已开始的隔离订单上的数量不更新

知识库编号：4613113

## <a name="symptoms"></a>故障特征

当您创建隔离订单并尝试拆分它时，订单数量未更新为拆分之后的剩余数量。

## <a name="resolution"></a>解决方法

系统不会更改隔离订单的原始数量，以确保您可以跟踪为该隔离订单创建的原始数量。 但是，系统会跟踪从隔离订单拆分的数量。 为进行此跟踪，它使用名为 `QuantityThatHasSplitIntoOtherQuarantineOrders` 的数据库字段。 但是，此字段在用户界面 (UI) 中不可见。
