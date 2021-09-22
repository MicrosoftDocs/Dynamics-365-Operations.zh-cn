---
title: 采购订单上的单位价格不是基于单位转换来计算的
description: 采购订单上的单位价格不是基于单位转换来计算的
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
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475683"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>采购订单上的单位价格不是基于单位转换来计算的

## <a name="symptoms"></a>故障特征

在采购订单上更改单位时，不会根据单位转换定义重新计算贸易协议价格。

## <a name="cause"></a>原因

价格始终从贸易协议（或系统中的其他价格设置，如销售协议或物料价格）获取，它们是针对单位设置的。

如果在订单行上更改了单位，系统将为新单位查找价格并应用该价格。 如果未为该单位找到价格，系统不会应用价格。 单位转换不能用于将价格重新计算为另一个单位。 从理论上讲，一盒十个的价格可能不等于一盒价格的十倍。

## <a name="workaround"></a>解决方法

解决此问题的一种方法是，确保有您预期的单位的贸易协议将用于物料的订单行。
