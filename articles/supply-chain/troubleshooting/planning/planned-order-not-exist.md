---
title: 系统在多个订单的操作期间找不到计划订单
description: 对多个计划订单执行操作时出现“计划订单不存在”错误，并且至少两个订单属于同一物料 ID。
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920791"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>系统在多个订单的操作期间找不到计划订单

错误代码：SYS24774

## <a name="symptoms"></a>故障特征

尝试同时对多个计划订单执行操作时，您收到以下错误消息，并且至少有两个订单属于同一物料 ID。 例如，当已确认订单或已更改订单类型时，可能会出错。

> 计划订单 %1 不存在。

## <a name="cause"></a>原因

当系统确定或更改订单类型时，它必须重新考虑该物料的现有计划订单，以确保计划供应与需求和现有供应匹配。 作为此流程的一部分，系统将重新创建物料的计划订单。 因此，系统希望处理的第二个计划订单不再存在。

## <a name="workaround"></a>解决方法

在处理订单之前审核订单。 这样，当系统处理物料的第一个订单时，将不会删除订单。
