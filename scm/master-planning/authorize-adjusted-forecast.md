---
title: "授权调整后的预测"
description: "不必立即授权所有预测数据。 本文介绍如何指定为预测授权的期间。 还说明如何可以授权特定公司和预测模型的预测。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 324f7385e8064eedcf35f0f07bb3b2ef6474f410
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="authorize-an-adjusted-forecast"></a>授权调整后的预测

[!include[banner](../includes/banner.md)]


不必立即授权所有预测数据。 本文介绍如何指定为预测授权的期间。 还说明如何可以授权特定公司和预测模型的预测。

不必立即授权所有预测数据。 您可以指定预测授权期间的开始和结束日期。 此功能可以锁定特定时段。 

您指定的开始日期和结束日期必须对应预测生成的时段的开始日期和结束日期。 如果需要调整，此系统强制执行此限制和自动调整日期。 

在**授权**页的**详细信息**选项卡上，您可以查看最近生成的预测的详细信息。 

您可以选择公司和预测模型以授权要使用的预测。 默认情况下，网格包括为其创建预测需求的所有公司。 对于每个公司，对应于在主计划参数中设置的当前预测计划的预测模型将被预填写。 不过，您可以将此预测模型更改为属于该公司的任何预测模型。 如果预测需求数据没有为一个所选公司生成，将在导入时收到警告消息。 

您知道复选框**保存对基准需求预测进行的手动调整**如何工作非常重要。 如果您已手动调整统计基准预测，则授权使用调整的值，即使清除此复选框也是如此。 但是，在此授权之后将放弃更改。 因此，下次预测生成时，该预测只是统计预测，不具有任何手动覆盖，即使选择了**转移对需求预测进行的手动调整**。 因此，您可以视**保存对基准需求预测进行的手动调整**复选框为可以保留或放弃所有手动更改的机制。

<a name="see-also"></a>请参阅
--------

[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)

[监控预测准确性](monitor-forecast-accuracy.md)




