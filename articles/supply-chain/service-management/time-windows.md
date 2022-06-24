---
title: 时间范围
description: 您可以使用时间范围优化服务订单行的计划。
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccbb9cf71ff1df7aa336deb5bf9d7dacb8004134
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862386"
---
# <a name="time-windows"></a>时间范围  

[!include [banner](../includes/banner.md)]

您可以使用时间范围优化服务订单行的计划。 您可以设置系统，以便自动创建服务订单。 基于时间范围指定的条件，您可以将尽可能多的服务订单行连接到尽可能少的服务订单。

时间范围指定某一服务订单行从其计算日期中可以移动多远。 在计划发生服务订单行时，计算日期为日期。 该日期基于其间隔设置和您在 **创建服务订单** 页面中定义的服务期间。 您使用以下表中的值定义时间范围：

| 方法 | 说明                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 周   | 服务订单行可以移到与初始计算日期处于同一周内的任何开放日期的日期。                                                                                                                                                                                    |
| 月  | 服务订单行可以移到与初始计算日期处于同一月内的任何开放日期的日期。 例如，一个服务订单行的计算日期为 2017 年 2 月 15 日。 可将该服务订单行安排到 2017 年 2 月 1 日到 2 月 28 日之间的任何一个工作日。 |
| 手动 | 您定义服务订单行可移动的最初计算日期之前或之后的最大天数。                                                                                                                                                                           |

如果没有为某一服务协议行指定时间范围，则从该服务协议派生的服务订单行必须就在最初计划的那一日期执行。

## <a name="related-articles"></a>相关文章

[创建时间范围](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]