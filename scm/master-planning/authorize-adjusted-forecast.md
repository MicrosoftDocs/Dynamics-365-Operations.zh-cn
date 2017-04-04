---
title: "授权进行调整的预测"
description: "不必立即授权所有预测数据。 本文介绍如何指定为预测授权的期间。 还说明如何可以授权特定公司和预测模型的预测。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>授权进行调整的预测

不必立即授权所有预测数据。 本文介绍如何指定为预测授权的期间。 还说明如何可以授权特定公司和预测模型的预测。

不必立即授权所有预测数据。 您可以指定预测授权期间的开始和结束日期。 此功能可以锁定特定时段。 

您指定的开始时间和结束日期必须与于时段的开始日期和结束日期预测生成。 如有必要，则系统，强制此限制和自动调整调整的日期。 

在**授权**页的**详细信息**选项卡上，您可以查看最近生成的预测的详细信息。 

您可以选择公司和预测模型以授权要使用的预测。 默认情况下，网格包括为其创建预测需求的所有公司。 对于每个公司，对应于在主计划参数中设置的当前预测计划的预测模型将被预填写。 不过，您可以将此预测模型更改为属于该公司的任何预测模型。 如果预测需求数据没有为一个所选公司生成，将在导入时收到警告消息。 

您知道复选框**保存对基准需求预测进行的手动调整**如何工作非常重要。 如果您进行了手动调整到基准统计预测，调整值的授权，即使为使用，清除此复选框。 但是，在此授权之后将放弃更改。 因此，下次预测生成时，该预测只是统计预测，不具有任何手动覆盖，即使选择了**转移对需求预测进行的手动调整**。 因此，您可以视**保存对基准需求预测进行的手动调整**复选框为可以保留或放弃所有手动更改的机制。

<a name="see-also"></a>请参阅
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


