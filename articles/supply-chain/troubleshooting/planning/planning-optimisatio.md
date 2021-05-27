---
title: 负数天内存在采购时会创建计划采购订单
description: 如果覆盖范围代码为“最小值/最大值”，在负数天内存在采购时，计划优化会创建计划采购订单。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026309"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>负数天内存在采购时会创建计划采购订单

知识库编号：4614298

## <a name="symptoms"></a>故障特征

如果覆盖范围代码为 *最小值/最大值*，在负数天内存在采购时，计划优化会创建计划采购订单。

## <a name="resolution"></a>解决方法

计划优化不支持负天数。 但是，它始终确保不会在相对于当前日期的提前时间内安排计划订单。 例如，采购提前期为 10 天，采购订单预计从今天起八天到达。 在这种情况下，采购订单将用作从今天起五天的需求供应。

因此，我们建议您调整提前期来覆盖所有（或几乎所有）场景。
