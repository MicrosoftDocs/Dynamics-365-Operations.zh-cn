---
title: 自动创建服务订单
description: 您可以生成基于服务协议的有效期间的服务协议的服务订单。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1acf4620556fe7ec5ae40f0a98b0a23602e2524a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565129"
---
# <a name="automatically-create-service-orders"></a>自动创建服务订单 

[!include [banner](../includes/banner.md)]


您可以生成基于服务协议的有效期间的服务协议的服务订单。

您基于某一服务协议生成的所有服务订单都附加到此服务协议上。

服务订单自动根据以下设置生成：

  - 在服务协议行中设置的服务协议间隔。 服务协议间隔指示创建服务订单行的频率。 有关服务间隔的详细信息，请参阅[服务间隔](service-intervals.md)。

  - 您在 **创建服务订单** 窗体的 **开始日期** 字段和 **结束日期** 字段中为定义服务期间而指定的期间。 有关如何创建服务订单的详细信息，请参阅[自动创建服务订单](create-service-orders-automatically.md)。

  - 服务协议标头上的 **合并服务订单** 选项。 此选项定义是否基于服务协议生成服务订单行，并根据员工、服务任务、服务对象或服务协议合并服务订单。 有关详细信息，请参阅[合并服务订单](combine-service-orders.md)。

  - 服务协议行上的 **时间范围** 选项。 时间范围定义某一服务订单行相对于其计算日期可以移动多远。 有关时间范围的详细信息，请参阅[时间范围](time-windows.md)。


> [!NOTE]
> <P>如果为某一服务订单指定的日期在您在<STRONG>服务管理参数</STRONG>窗体中选择的日历上未打开，则您将收到一个消息，指示存在日历冲突。 您可以放心地忽略这一消息；即使该日期在日历上已关闭，仍会创建该服务订单。</P>

## <a name="example-1"></a>示例 1

此服务协议从 2012 年 1 月 1 日持续到 2012 年 12 月 31 日。 如果您在 **创建服务订单** 窗体中指定的服务器为 2012 年 11 月 1 日到 2013 年 2 月 1 日，则从 2012 年 11 月 1 日到 2012 年 12 月 31 日创建服务订单。

## <a name="example-2"></a>示例 2

此服务协议从 2012 年 1 月 1 日持续到 2012 年 12 月 31 日。 将把两个服务协议行附加到此服务协议。 第一个服务协议行的开始日期为 2012 年 1 月 2 日，结束日期为 2012 年 3 月 1 日。 第二个服务协议行的开始日期为 2012 年 4 月 2 日，结束日期为 2012 年 12 月 31 日。 您将在 **创建服务订单** 窗体中指定一个从 2012 年 10 月 1 日到 2012 年 12 月 31 日的期间。 因此，只为第二个服务协议行生成服务订单，因为第一个协议行的开始日期和结束日期在您为该服务订单指定的期间之前。

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]