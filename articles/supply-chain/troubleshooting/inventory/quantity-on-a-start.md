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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713486"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>拆分订单后，已开始的隔离订单上的数量不更新

知识库编号：4613113

## <a name="symptoms"></a>故障特征

当您创建隔离订单并尝试拆分它时，订单数量未更新为拆分之后的剩余数量。

## <a name="resolution"></a>解决方法

系统不会更改隔离订单的原始数量，以确保您可以跟踪为该隔离订单创建的原始数量。 但是，系统会跟踪从隔离订单拆分的数量。 为进行此跟踪，它使用名为 `QuantityThatHasSplitIntoOtherQuarantineOrders` 的数据库字段。 但是，此字段在用户界面 (UI) 中不可见。
