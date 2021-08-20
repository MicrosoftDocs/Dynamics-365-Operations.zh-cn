---
title: 时间范围
description: 您可以使用时间范围优化服务订单行的计划。
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29c43d5c21d435086bcc272e89b4c877f4057a44374e4d0005a842e10fe43a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741229"
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

## <a name="related-topics"></a>相关主题

[创建时间范围](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]