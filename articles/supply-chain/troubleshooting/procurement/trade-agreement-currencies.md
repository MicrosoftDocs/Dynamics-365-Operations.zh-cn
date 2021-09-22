---
title: 贸易协议货币转换问题
description: 当采购订单上的货币不同时，不会根据货币重新计算贸易协议价格
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475652"
---
# <a name="trade-agreement-currency-conversion-issues"></a>贸易协议货币转换问题

## <a name="symptoms"></a>故障特征

当采购订单上的货币不同时，不会根据货币重新计算贸易协议价格。

## <a name="resolution"></a>解决方法

*通用货币* 功能可让您仅使用一种货币定义价格和折扣。 然后，您可以根据需要转换为其他货币。 而且，转换完成后，此功能还可以自动应用智能舍入。
