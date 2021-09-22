---
title: 无法通过出站仓库操作发放销售订单
description: 可能收到无法发放销售订单的原因有多种。 此页面介绍此问题的原因和缓解方法。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475703"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>无法通过出站仓库操作发放销售订单

## <a name="symptoms"></a>故障特征

处理处站仓库工序时，您可能会收到以下错误消息：

> 无法发放销售订单。

## <a name="cause"></a>原因

出现此问题有多种原因。 例如，订单处于信用管理暂停状态，只有为与订单关联的所有销售行输入有效的邮政地址，才能创建装运。 或者，存在订单保留，要将订单下达到仓库必须对它进行处理。 此保留可能是特定于订单的，或者可能在客户帐户上。

## <a name="resolution"></a>解决方法

在销售订单和订单行上添加或更新地址，然后将订单下达到仓库。 仅当订单有有效的交货地址（按照 **组织管理** 模块中设置的地址格式）时，才能将订单下达到仓库。

调查订单保留，并解决问题。 然后从订单或客户中删除保留，将订单下达到仓库。
