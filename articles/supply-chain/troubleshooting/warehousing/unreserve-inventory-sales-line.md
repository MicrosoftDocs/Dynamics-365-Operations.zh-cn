---
title: 无法取消预留销售订单行中的库存
description: 如果有针对销售订单行的未结工作，而您尝试取消预留该行中的库存，您将遇到错误。 请完成或删除工作以释放预留。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475697"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>无法取消预留销售订单行中的库存

## <a name="symptoms"></a>故障特征

如果有针对销售订单行的未结工作，而您尝试取消预留该行中的库存，您将收到以下错误消息：

> 已创建了依赖预留的工作，因此无法删除这些预留。

## <a name="resolution"></a>解决方法

调查是否存在要将物料从装箱工作站运送到另一个位置（如 *货架门*）的未结包装组工作。 查看 **工作创建历史记录日志** 和 **工作详细信息** 页的记录，确定哪个工作在实际预留库存，然后完成或删除工作，释放预留。
