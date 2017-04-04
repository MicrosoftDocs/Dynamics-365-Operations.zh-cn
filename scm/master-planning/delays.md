---
title: "延迟"
description: "本文提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9113c7728c5d23b70e3809bab31136aff63c6acf
ms.lasthandoff: 03/31/2017


---

# <a name="delays"></a>延迟

本文提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。

主计划可以基于提前期、物料可用性、产能可用性以及各种计划参数计算交易记录的最早履行日期。 

如果主计划计算早于当前日期的一个订单日期，订单不能准时履行。 因此，订单延期。 在这种情况下，主计划从当前日期正推计划订单并包括提前期。 这些提前期从任何更低级别构成物料开始。 该订单然后将收到一个延期的日期。 延期日期是基于当前数据的实际到期日期。 主计划还计算延迟的天数。 

在某些情况下，您可以选择不计算延迟，例如，当用户了解他们可以通过选择备选交货模式加速提前期时。 

您可以配置如何为覆盖范围组计算延迟。 然后您可以在以后将覆盖范围组附加到物料上。 

在**主计划参数**页上，您可以设置延迟计算的开始时间。 如果在此时间后履行某一订单，则在该订单的延迟日期上加上一天的延迟。 

**注释：**早期版本，在计算中*futures 的延迟 messages*，延迟的日期 (*futures，date*，并且一延迟的交易记录涉及为将来的 set*的*a 交易记录。

<a name="see-also"></a>请参阅
--------

[覆盖范围设置](coverage-settings.md)


