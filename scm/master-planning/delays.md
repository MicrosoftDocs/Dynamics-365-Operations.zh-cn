---
title: "延迟"
description: "本文提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 84682e08da6da8928004c7971cd2c2a3725446c0
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="delays"></a>延迟

[!include[banner](../includes/banner.md)]


本文提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。

主计划可以基于提前期、物料可用性、产能可用性以及各种计划参数计算交易记录的最早履行日期。 

如果主计划计算早于当前日期的一个订单日期，订单不能准时履行。 因此，订单延期。 在这种情况下，主计划从当前日期正推计划订单并包括提前期。 这些提前期从任何更低级别构成物料开始。 该订单然后将收到一个延期的日期。 延期日期是基于当前数据的实际到期日期。 主计划还计算延迟的天数。 

在某些情况下，您可以选择不计算延迟，例如，当用户了解他们可以通过选择备选交货模式加速提前期时。 

您可以配置如何为覆盖范围组计算延迟。 然后您可以在以后将覆盖范围组附加到物料上。 

在**主计划参数**页上，您可以设置延迟计算的开始时间。 如果在此时间后履行某一订单，则在该订单的延迟日期上加上一天的延迟。 

**注意：**在较早版本中，计算的延迟称为*先期备货消息*，延迟的日期称为*将来日期*，延期的交易记录称作*为将来设置的交易记录*。

<a name="see-also"></a>请参阅
--------

[覆盖范围设置](coverage-settings.md)




