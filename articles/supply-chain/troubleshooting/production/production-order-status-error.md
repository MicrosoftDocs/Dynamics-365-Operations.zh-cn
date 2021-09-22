---
title: 将状态从“完工入库”更改为“结束”时出错
description: 将生产订单的状态从“完工入库”更改为“结束”时，可能会出错。 此页面介绍如何缓解该问题。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475694"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>将生产订单的状态从“完工入库”更改为“结束”时出错

## <a name="symptoms"></a>故障特征

当生产订单的状态从“完工入库”更改为“结束”时，您收到以下错误消息之一：

> 更新冲突。 标准成本在更新后与财务库存值不匹配。

> 函数 InventCostMovement.checkVariance 中发生严重错误。

## <a name="cause"></a>原因

发生此问题的原因是基础数据被另一个流程更改。 此流程最多会尝试更新数据五次。 如果五次尝试后冲突仍然存在，您将收到上列消息之一。

## <a name="resolution"></a>解决方法

此为有意行为。 要缓解此问题，请继续批处理作业。 它应该完成运行。

如果批处理作业在您恢复后持续失败，请验证分类帐默认货币的舍入精度是否符合应用于 InventSum 表中的值的舍入要求。 如果舍入精度更改为不符合要求的值，您可能必须将其重新更改为符合要求的值。 查找 **ModifiedDateTime**。 在这种情况下，此值通常会显示舍入精度最近已更改。
